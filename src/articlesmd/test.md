### 一、== 和 === 的区别
1. == 在比较类型不同的变量时，会进行数据类型转化，将二者转换成数据类型相同的变量，再进行比较。  
    + NaN和任何数都不相等，包括NaN本身。  
        ```javascript
        NaN == NaN
        false
        ```  
    + 引用数据类型比较的是地址。  
        ```javascript
        [] == []
        false 
        {} == {}
        false
        ```  
    + 对象 == 字符串 将对象转换成字符串。  

    + 剩下的其他情况如果两边数据类型不一样，都需要转换成数字类型。  
        （1）对象转数字：先转换为字符串，再转换为数字  
        （2）字符串转换为数字：只要出现非数字字符，结果就是NaN  
        （3）布尔转数字：true=>1 false=>0  
        （4）null转数字：0  
        （5）undefined转数字：NaN  
2. === 比较的二者数据类型不一样时，直接返回false。  

    + 数据类型不一样  
        ```javascript
        undefined == null
        true
        undefined === null
        false
        ```  
### 二、null 和 undefined区别  
1. 两者之间 == 返回true，=== 返回false  
2. undefined 表示一个变量自然的、最原始的状态值，而 null 则表示一个变量被人为的设置为空对象，而不是原始状态  

### 三、typeof 和 instanceof 区别  
1. typeof用于判断参数是什么数据类型，返回值有number，boolean，string，function，object，undefined。  
2. 若参数为引用类型，typeof对于丰富的对象实例，只能返回"object"字符串。  
3. instanceof用来判断一个对象在其原型链中是否存在一个构造函数的prototype属性，代码形式为obj1 instanceof obj2（obj1是否是obj2的实例），obj2必须为对象，否则会报错！其返回值为布尔值。  