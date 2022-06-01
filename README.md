# JavaScript

https://opentutorials.org/module/4047

## Prototype

Prototype을 통해서 객체가 생성될때마다 호출되거나, 메모리를 잡아먹지 않고,
모든 Person객체가 서로 prototype하나의 함수만 공유함.
또한 kim.sum을 통해서 함수를 재정의 가능함.

```
function Person(name, first, second, third){
    this.name=name;
    this.first=first;
    this.second=second;   
}
 
Person.prototype.sum = function(){
    return 'prototype : '+(this.first+this.second);
}
 
var kim = new Person('kim', 10, 20);
kim.sum = function(){
    return 'this : '+(this.first+this.second);
}
var lee = new Person('lee', 10, 10);
console.log("kim.sum()", kim.sum());
console.log("lee.sum()", lee.sum());
```

