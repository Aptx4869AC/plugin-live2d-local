# plugin-live2d-local
专属看板娘

我本质要求：

①人物模型能全部显示，因此我只需要调整

```
"layout":{
"width":2.0,
"center_x":0,
"center_y":0
}
```



即可

②调整条件①后，我的

```
#live2d {
cursor: grab;
height: 600px;  /* 你想要的高度 */
width: 320px;   /* 你想要的宽度 */
position: relative;
/* 初始状态透明 */
transform: translateX(100%);
/* 初始位置在右侧（屏幕外） */
transform-origin: center center;
/* 添加以下属性 */
overflow: hidden;
display: flex;
align-items: center;
justify-content: center;
}
```



太小导致显示效果不好

③如果条件②非正方形，后导致拉伸问题

④如果条件②是正方形，会导致其他界面遮挡。

因此我本质是想解决①②③

