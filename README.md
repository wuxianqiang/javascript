# javascript
前端

## 目录

* 从一个地址栏输入一个网址到页面呈现都经历了什么？

### 数据类型转换

两个等号之间的数据类型转规则如下

|两边的数据类型|转换规则|
|-|-|
|数字==字符串|字符串调用`Number()`方法转换为数字就可以比较了|
|数字==对象|对象调用`toString()`再`Number()`转为数字就可以比较了|
|数字==NaN|NaN和任何数据类型的都不相等的|
|数字==布尔|布尔值调用`Number()`转为数字就可以比较了|
|数字==null|null和任何数据类型的都不相等的|
|数字==undefined|undefined和任何数据类型的都不相等的|
|对象==对象|两个对象之间也是不相等的|
|对象==字符串|对象调用`toString()`就可以比较了|

有三个方法可以把非数值转换为数值，那就是`parseInt()`,`parseFloat()`,`Number()`,如果传入的对象，默认会调用toString()转换，时间对象有一点区别。

|方法名称|空字符串|null|undefined|NaN|true|false|数组里只有一项|普通对象|
|-|-|-|-|-|-|-|-|-|
|Number()|0|0|NaN|NaN|1|0|数组的那项一项|NaN|
|parseInt()|NaN|NaN|NaN|NaN|NaN|NaN|数组的那项一项|NaN|
|parseFloat()|NaN|NaN|NaN|NaN|NaN|NaN|数组的那项一项|NaN|
