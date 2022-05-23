---
layout: post
title: ElementPlus日期组件设置一周起始日
categories:  [编程,前端]
description: ElementPlus日期组件设置一周起始日
keywords: 前端、编程、组件
---

> 周起始日涉及到国际化配置  

#### 配置国际化
ElementUI日期组件提供了 `firstDayOfWeek`属性，可以设置周起始日，但是ElementPlus未提供该属性，文档里只提到[“日期相关的文字（月份，每一周的第一天等等）也都是通过国际化来配置的。”](https://element-plus.org/zh-CN/component/date-picker.html#%E5%9B%BD%E9%99%85%E5%8C%96)<br />在项目中main.js文件内配置国际化，再配置dayjs国际化。（第7、8、10行）<br />再使用日期组件，一周起始日就是周一了。
```javascript
import { createApp } from 'vue';
import App from './App.vue';

import ElementPlus from 'element-plus';
import 'element-plus/dist/index.css';

import zhCn from 'element-plus/es/locale/lang/zh-cn';
import 'dayjs/locale/zh-cn';

createApp(App).use(ElementPlus, { locale: zhCn }).use(ElementPlus).mount('#app');

```
<a name="pMO9F"></a>

#### 配置前后效果
配置前：<br />![](https://img.nanvon.cn/2022-0523-17:31:49:605.png#crop=0&crop=0&crop=1&crop=1&id=TNMdY&originHeight=440&originWidth=384&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)<br />![](https://img.nanvon.cn/2022-0523-17:33:33:885.png#crop=0&crop=0&crop=1&crop=1&id=te1xD&originHeight=469&originWidth=368&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)<br />配置后：<br />![](https://img.nanvon.cn/2022-0523-17:34:01:265.png#crop=0&crop=0&crop=1&crop=1&id=SN8X5&originHeight=451&originWidth=406&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)
#### 更多
这是中文环境下的配置，我们国家周一是周起始日，如果要按其他国家的习惯来，就配置对应国际化。
#### 文档资料
[日期组件国际化](https://element-plus.org/zh-CN/component/date-picker.html#%E5%9B%BD%E9%99%85%E5%8C%96)<br />[国际化配置](https://element-plus.org/zh-CN/guide/i18n.html)
