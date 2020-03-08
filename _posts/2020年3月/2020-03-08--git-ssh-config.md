---
layout: post
title:  "配置git代理"
categories: ssh,config
tags:  config
author: Mullen
excerpt: "speed up from github"
---

* content
{:toc}
## github代理

### 1.配置ssr

#### 1.更新用户自定义pac 规则

```
||github*.com^
```

#### 2.配置ssh config

```
Host github.com
Hostname github.com
IdentityFile ~/.ssh/id_rsa.github
User mullenlee
ProxyCommand nc -v -x 127.0.0.1:1086 %h %p
```



