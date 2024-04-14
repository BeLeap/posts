---
title: "Aws ProfilE Switcher"
date: "2022-09-20T00:00:00+09:00"
tldr: "apes는 여러 개의 AWS Profile을 사용할 때 AWS Profile간의 변경을 쉽게 만들어주는 커맨드라인 유틸리티이다."
draft: true
tags: ["AWS"]
---

apes는 여러 개의 AWS Profile을 사용할 때 AWS Profile간의 변경을 쉽게 만들어주는 커맨드라인 유틸리티이다.

## 개발동기

Riiid에서는 `dev`, `stg`, `prod`간에 격리를 위해 완전히 분리된 AWS Profile을 사용하고 있는데,
DevOps로 근무하면서 Profile간에 변경하며 작업을 하는 것이 매우 귀찮은 일이었다.
더 쉬운 변경을 위해 원하는 command를 subcommand로 받아 원하는 AWS Profile을 설정한 후
command를 실행해주는 유틸리티를 만들게 되었다.

## 참고

- 여러 개의 AWS Profile에서 원하는 Profile 선택은 fuzzy_finder를 사용했다.
