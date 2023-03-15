---
layout: post
title: "[cmake] find_package, pkg_check_modules 사용"
summary: "cmake find_package, pkg_check_modules"
thumbnail:
category: dev
tags: [cmake]
comments: true
date: "2023-03-15 11:36:00"
lastmod: "2023-03-15 12:00:00"
series: blog
sitemap:
  changefreq: daily
  priority: 1.0
---

# cmake lib 사용 정리
- [IPC] D-Bus와 관련하여 [예제](https://www.kernelpanic.kr/23) 테스트 중 cmake lib 설정 관련 정리
```
gcc server.c -o server `pkg-config --cflags 
--libs libsystemd`
```
- find_package(systemd) 동작하지 않음.

# 처리
```
find_package(PkgConfig REQUIRED)
pkg_check_modules(SDBUS REQUIRED libsystemd)
target_link_libraries(dbus-server ${SDBUS_LIBRARIES})
```

# 참조
- CMake 관련 정리 github 페이지
- [jacking75/examples_CMake](https://github.com/jacking75/examples_CMake/blob/master/find_package_And_pkg_check_modules.md)
- [pkg_check_modules](https://cmake.org/cmake/help/latest/module/FindPkgConfig.html?highlight=pkg_check_modules#command:pkg_check_modules)