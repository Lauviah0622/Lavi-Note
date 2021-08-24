## Tagged Template Literal
ES6 中新的 call function 方式，直接看這個範例可能比較清楚

```js
console.log`string1${'attr1'}string2${'attr2'}`

// ["string1", "string2", "", raw: Array(3)] 0
//  "string1" 1 
//  "string2" 2
```

可以利用 template string 的方式來帶入參數，就直接在 function 後面加上 template string 就好了
```js
function sum () {

}

sum`${10}${20}`
```

那 template string　中的 
- string 部分作為第一個參數  
  以 template string 裡面有出現的變數作為 `split` 分割，被集合成一個 `array`，。
- 變數部分依序帶入之後的參數

### 用法
可以用 rest parameter 的方式來蒐集變數，function 看起來比較乾淨

```js
function (strings, ...variables) {

}
```
  