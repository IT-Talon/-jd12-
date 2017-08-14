# 这是一张jd12期免息卷引发的血案

- 点击领息券后出来下图界面

![领券图](http://i2.bvimg.com/605658/7ac4f7051f377099.png)
点击‘我知道了’没有反应，就很气。然后谢了一段js代码，把它搞掉了...(这货model拼错了?)

```js
var btn = document.getElementById('m-modal').lastChild.firstChild;
btn.onclick => document.getElementById('m-mask').style.display ='none';
```

进去后滑动鼠标滑轮没反应，鼠标可以拖动界面，认定这肯定是给手机看的，又想起来这个button之前绑定的事件是tap，更加印证了我的想法。url发到手机上打开后点击果然可以，妈个鸡，300ms延迟的click操作无法触发100ms的tap操作，看来还是手速不够快啊。
