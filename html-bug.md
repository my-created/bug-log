1. 2017-9-13 10:58:14
      问题：HTML 文件上传显示没有上传文件，最后找到原因
      原因：input 没有 name 属性造成的……。
      解决：input 添加name
2. 2017-10-11 19:40:38
      问题：window.open 在ajax 中返回null，无法打开新页面
      原因：浏览器认为 ajax不是人操作window.open 函数，不安全，所以拦截了
      解决：1. 在ajax前面 open,在ajax里write
            2. 修改ajax 同步参数为同步（而非默认的异步），在ajax里open,write
3. 2019-01-22 15:38:16
      问题：ajax提交之前展示 loading，怎么弄都展示不出来。
      原因：ajax 的 ansync 设置成 false 了，意思就是 ajax 是同步，造成 ajax 卡住了 jquery 的事件。
      解决：ansync 改成 true，异步就可以了。ajax 事件处理了，直接跳过。等待返回就行。
4. 2019-04-08 15:24:09
      问题：无法获取 iframe 的 src
      原因：iframe 只能通过 name 可以获取
      解决：
      ```javascript
      // 获取当前iframe name
      window.name
      // 获取当前iframe src
      window.parent.document.getElementById(window.name).src;
      ```
