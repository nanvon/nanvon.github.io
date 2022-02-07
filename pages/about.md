---
layout: page
title: About
description: 
keywords: 
comments: true
menu: 关于
permalink: /about/
---



## Introduction

Code-Read-Think



## Find Me

- 公众号：南枫的寻宝之旅

  

- 技术博客：https://www.cnblogs.com/nanvon/

  

- 知乎专栏：https://zhuanlan.zhihu.com/nanvon-tool

  

- 豆瓣：https://www.douban.com/people/nanvon/

  

- 个人网站：https://www.nanvon.cn/  



## Skill Keywords

{% for skill in site.data.skills %}
### {{ skill.name }}
<div class="btn-inline">
{% for keyword in skill.keywords %}
<button class="btn btn-outline" type="button">{{ keyword }}</button>
{% endfor %}
</div>
{% endfor %}
