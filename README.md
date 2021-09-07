### JavaScript语法

> 表达式与语句

+ 表达式一般有值，语句可能有也可能没有

+ 语句一般会改变语境(声明，赋值)

  ```javascript
  console.log(3)
  //undefined
  
  function(){
      retuen 4; //return后不可加回车，否则返回undefined
  }
  ```

> 标识符规则

+ 首字符可以是字母、$、_、中文
+ 其余字符可以是数字、字母、下划线、中文、$

> if else

```javascript
if(表达式){
    语句1
}else{
    语句2
}

a = 1
if(a === 2)
    console.log('a')
    console.log('a等于2')
//花括号省略时，if只作用于下面1句

function fn(){
    if(表达式){
        return 表达式
    }
    if(表达式){
        return 表达式
    }
    return 表达式
}
//return时，else可省略
```

> 三目运算符

```javascript
a > b ? a : b;

//短路运算
if(a){
    a = a
}else{
    a = 100   //保底值
}
```

> while循环

```javascript
while(表达式){
    语句
}

var a = 0.1
while(a !== 1){
    console.log(i)
    a+=0.1
}
//死循环，浮点数：存在精度误差
```

> for循环

```javascript
for(语句1，表达式1，表达式2){
    循环体
}
//如果为真，先执行循环体，再执行语句3
    
    
for(var i = 0; i<5; i++){
    setTimeout(()=>{
        console.log(i + '随机数' + Math.random())
    },0)
}
//5 5 5 5 5
```

> break continue

```javascript
for(var i = 0; i<5; i++){
    if(i%2 === 1){
        break;
    }
}
//i = 1 break退出

for(var i = 0; i<5; i++){
    if(i%2 === 1){
        continue;
    }else{
        console.log(i)
    }
}
//continue next
```

> label

```javascript
{a : 1}

foo:{
    console.log(1);
    break foo;
    console.log('本行不会输出');
}
console.log(2)
```

