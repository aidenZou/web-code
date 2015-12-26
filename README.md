# web-demo

## web 兼容性 测试

### CSS

- calc():

  http://codepen.io/aidenzou/full/mVrxVv/
  
  兼容性传送门：http://caniuse.com/#search=calc

### Javascript

- Zepto事件委托的小坑

  http://codepen.io/aidenzou/full/WrGzxQ/
  
  Find:https://github.com/riskers/blog/issues/14
  
  Zepto 的事件委托是：
  
  > 在代码解析的时候，所有document的所有 click 委托事件都依次放入一个队列里，click 的时候先看当前元素是不是.a，符合就执行，然后查看是不是.b，符合就执行。
  这样的话，就导致如果 .a 的事件在前面，会先执行 .a 事件，然后 class 更改成 b，Zepto再查看当前元素是不是 .b，以此类推。
  
  jQuery 的事件委托：
  
  > document上委托了2个 click 事件，click 后判断是否当前符合条件（选择符），然后把事件拿出来执行。



