---
layout: post
title: "[install] Choco 설치"
summary: "Choco 설치"
thumbnail:
category: dev
tags: [install]
comments: true
date: "2023-02-16 00:00:00"
lastmod: "2022-02-17 00:00:00"
series: install
sitemap:
  changefreq: daily
  priority: 1.0
---

# Way? chocolatey

[참조](https://namu.wiki/w/%ED%8C%A8%ED%82%A4%EC%A7%80%20%EA%B4%80%EB%A6%AC%EC%9E%90)

Windows의 터미널 패키지 관리자 중 하나.

# Chchocolatey 설치

참조 : [https://chocolatey.org](https://chocolatey.org)

Windows PowerShell 관리자 권한으로 실행 후 다음 명령어 실행
'''
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

PS C:\> choco -v
1.3.0
'''
