# How to get your token discord using browser console !
1. Open developer tools (F12 or Ctrl+Shift+)
2. Switch current tab to Console
3. Write this code and press enter
```js
let token;
window.webpackChunkdiscord_app.push([[Symbol()], {}, o => {
  for (let e of Object.values(o.c)) {
    try {
      if (!e.exports || e.exports === window) continue;
      if (e.exports?.getToken) {
        token = e.exports.getToken();
        console.log("Token:", token); // Print the token
      }
      for (let o in e.exports) {
        if (e.exports?.[o]?.getToken && "IntlMessagesProxy" !== e.exports[o][Symbol.toStringTag]) {
          token = e.exports[o].getToken();
          console.log("Token:", token); // Print the token
        }
      }
    } catch {}
  }
}]);
window.webpackChunkdiscord_app.pop();
```
It will give your token !
