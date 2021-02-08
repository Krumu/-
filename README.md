### Q1

```html
<!DOCTYPE html>
<html>
  <head>
    <title> Document</title>
    <script src = "async/callback.js" defer></script>
  </head>
  <body>
      <h1>JavaScript</h1>
      <h2>비동기, Promise, async/await</h2>

      <div id="log box">
        <div id='log-box-title'>log</div><hr>
        <div id='log-box-body'>로그가 여기에 나타납니다.</div>
      </div>

      <script src="./script.js"></script>
  </body>
</html>
```

```javascript
function setLog(log){
var logBody = document.getElementById('log-box-body');
var logDiv = document.createElement('div');
logDiv.append(log);
logBody.append(logDiv);
}


var pr = new Promise(function(resolve,reject){
// 정의{
setTimeout(function(){
  console.log('값');
  //resolve('보임?');
},3000);
});

pr.then(function(value){// promise가 수행되고 나서 수행된다.
//promise수
console.log("after");
//console.log(value); 삽입시 after출력
});
```
