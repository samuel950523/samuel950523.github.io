---
title: "[Python] BOJ 1764번. 듣보잡"
layout: single
author_profile: true
read_time: true
comments: true
share: true
related: true
categories: Algorithm BOJ Implement Silver4
meta_keywords: 알고리즘,백준,파이썬,1764번
date: 2020-05-22 03:36:17 -0400
last_modified_at: 2020-05-22T03:36:17+08:00
---

# 1764번. 듣보잡

### 문제 링크
- <https://www.acmicpc.net/problem/1764>{: target="\_blank"}

### 풀이 코드

```python
# 1764번. 듣보잡


import sys
input = sys.stdin.readline

n, m = map(int, input().split())
hear_see = [0 for i in range(n+m)]

for i in range(n+m):
    hear_see[i] = input().rstrip()

# 모두 넣어준 뒤에 sort
hear_see.sort()

answer = 0
job = []

# 앞뒤 비교해서 같으면 듣보잡
for i in range(len(hear_see)-1):
    if hear_see[i] == hear_see[i+1]:
        job.append(hear_see[i])
        answer += 1

print(answer)
for row in job:
    print(row)
```

### 비고