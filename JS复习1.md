### JS中的字符串概述
> 在JS中使用单引号，双引号的都是字符串
### 常用方法
> - charAt charCodeAt>  -  substr substring slice>  -  toUpperCase toLowerCase>  -  indexOf lastIndexOf>  -  split>  -  replace>  -  match






### JS中的number类型
> 除了常规数字外，JS中增加了一个number的数据类型：NaN>  typeof NaN ->"string">


**`NaN`**
> not a number:不是一个数，但是属于number类型> NaN == NaN:false,NaN和任何值都不相等


** ` Isnan ` **
> 用来检测当前值是否是有效是数字，如果为有效数字则为false，反之则为true
``` javascript
isNaN(0)->flaseisNaN(NaN)-trueisNaN('12')->false
//当我们是哟你isNaN检测的时候，如果监测值不是number类型，浏览器会默认把值转换为number类型，然后再检测```

** `数字` **
> 把其他类型的数据值转换为number类型的值
``` javascript
Number('12') ->12
Number('12px') ->NaN
//在使用Number转换的时候只要字符串中出现任何一个非数字字符，结果都为NaN
Number(true) ->1
Number(false) ->0
NUmber(null) ->0
Number(undefined) ->NaN

Number([]) ->0
//把引用数据类型转换为number，首先要把引用数据类型转换为字符串(toString),在把字符串转换为number
Number('12') ->12
Number([12,23]) ->NaN
Number({name:'ji'}) ->NaN
```

**`parseInt`**
> 把其他数据类型转换为number，与Number方法在处理字符串是存在区别
 ```javascript
Number('12px')->12
parseInt('12px13')->12
//parseInt 提取规则，从左到右依次查找有效数字字符，遇到非有效数字字符停止，且只能提取整数
parseFloat('12.5px') ->12.5
//parseFloat,可提取小数
```

### null和undefined的区别
> null：空，没有
> undefined：未定义，没有
> '' 空串，没有
> 0 ：理解为无

`空字符串和null的区别`
> 例如：两个小和尚去打水，一个拿了水桶，没有装水，一个是连桶都没有拿
> 
> 空串相比于null来说，开辟了空间，，消耗了内存
>
`null和undefined的区别`
>null 表示暂时没有，预期中会有，但是未必达到预期
>
>undefined 完全没有在意料之内
>比如一个男孩现阶段没有女朋友(null)，但在预期中会有，但是不可能有男朋友(undefined)
  
### 对象数据类型object
> var obj = {name:'ji',age:21};
> 每一个对象都是由到多组'属性名(key键):属性值(value值)'组成，或是说有多组键值对组成
> 属性：描述对象的特点特征
> 对象的属性名是数字或字符串，存储的属性值可以是任何数据类型
```javascript
var obj = {name:'ji',age:21}; 
//获取某个属性名对应的属性值
obj.name
obj['name']

var test = {0:100};
//不支持test.0
test['0']/test[0]

//设置或修改属性
obj.sex = '男'；
//设置属性名和属性值
obj.age = 22;
//修改属性值

//删除
obj.sex = null;
//假删除，将属性值赋值为null，但属性名还在

delete obj.sex
//真删除，将对象中的属性移除

```



<!--stackedit_data:
eyJoaXN0b3J5IjpbLTU0MTUyMDkwM119
-->