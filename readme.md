Gax
---
项目状态树，组件通信，事件发布，消息订阅，支持后订阅消息获取

### Install
```sh
npm i gax --save
```

### Usage
```js
import gax from 'gax';


// 消息订阅
gax.on('user.login', status => console.log(status))

// 事件发布
gax.fire('user.login', true) // status === true
gax.emit('user.login', true)
gax.trigger('user.login', true)

// 后注册组件消息获取，可获得最后一次广播数据
gax.get('user.login', status => console.log(status)) // status === true
```
