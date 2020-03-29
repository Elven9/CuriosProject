# 黃能富的 AR Test

基本上，這個方法會成功完全仰賴教授的智商程度，把邏輯驗證全部寫在前端導致 Security 錯誤百出，厲害了教授，虧你還院長😉

## 操作流程

網址：[AR test](http://188.166.191.153:3456/test)

![](./Screen&#32;Shot&#32;2020-03-29&#32;at&#32;9.07.40&#32;PM.png)

打開 Chrome Dev Tool 或是其他各家瀏覽器的 Dev Tool，點最後一個 Script Tag 並滑倒 `sendAnswer` 這個 Function(直接 Command + F 比較快），就可以看到答案了，Happy Test~⭐️

![](./Screen&#32;Shot&#32;2020-03-29&#32;at&#32;9.13.15&#32;PM.png)

p.s 順便說，這個 APP 充滿了一堆 Bug 看右上角 18 個 error 就知道了

如果你更懶的話，可以打開 dev tool 中的 `Console`，把下面這個 code 修改成你的學號跟姓名版本，按 Enter 就可以了 = =

```js
$.ajax({
  url: './testDataPush',
  data: {
    student_Name: "你的名字",
    student_id: "你的學號",
    student_answer: "B;B&D;A&C&F;B;E;D;D;D;A;B;C;X"
  },
  type: 'POST',
  success: function (data) {
    console.log(data);

  },
  error: function(e) {
    console.log(e);
  }
})
```