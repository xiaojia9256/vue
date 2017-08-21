# 2017-08-16 （内部指令） 
#### v-if 、v-else  & v-show <br>
   v-if： 判断是否加载，可以减轻服务器的压力，在需要时加载。<br>
   v-show：调整css dispaly属性，DOM 已经加载，只是CSS控制没有显示出来。这样可以使客户端操作更加流畅。<br>

#### v-for 循坏 <br>
 v-for 是循环渲染一组data中的数组，v-for 需要以item in items 形式的特殊语法，items 是源数据数组并且item是数组元素迭代的别名。<br>

#### v-text  和  v-html<br>
v-text ：html中输出data中的值，用的是{{xxx}},这种情况是有弊端，当网速很慢或者javascript出错时，会暴露{{xxx}}。Vue提供的v-text,解决这个问题。<br>
v-html :当javascript中写有html标签，用v-text是输出不出来的，这时我们需要用v-html标签。<p v-html=“xx”></p>    <br>
在生产环境中动态渲染HTML是非常危险的，因为容易导致XSS攻击。所以只能在可信的内容上使用v-html，永远不要在用户提交和可操作的网页上使用。<br>

#### v-on 绑定事件监听器  v-model（绑定数据源）<br>
v-on:click 的简写  @click  v-on:click ==== @click<br>

#### v-model（绑定数据源）模型 双向数据绑定 <br>
  v-model.lazy :  取代 imput 监听 change 事件<br>
  v-model.number : 输入字符串转为数字<br>
  v-model.trim : 输入去掉首尾空格 <br>
#### vue其他内部指令
v-pre:原样输出<br>
v-cloak：等DOM树全部加载完才渲染<br>
v-once：只渲染第一次的，之后的不渲染<br>
