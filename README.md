# canvasStar
自己写的一个少女心满满的canvasStar特效

## 使用 canvasstar.js
### 在 HTML 中创建 canvas 元素
使用需要在 html 中加入 id 为 canvas 的 canvas，并且需要自己写好 canvas的样式

### 引用 `canvasstar.js` 文件
引用的 `canvasstar.js` 必须在 canvas 元素之后 

### 创建对象并调用
创建一个新的`CanvasStar`对象，并且使用`CanvasStar.init()`调用即可

```
<script>
    var CanvasStar = new CanvasStar;
    CanvasStar.init();
</script>
```
### 修改默认参数
如果有需要，可以更改默认参数
默认参数如下：
```
    /*
     * @para star_r：star半径系数，系数越大，半径越大
     * @para star_alpha：生成star的透明度，star_alpha越大，透明度越低
     * @para initStarsPopulation：初始化stars的个数
     * @para move_distance：star位移的距离，数值越大，位移越大
     * @para dot_r : dot半径系数，系数越大，半径越大
     * @para dot_speeds : dots运动的速度
     * @para dot_alpha : dots的透明度
     * @para aReduction：dot消失条件，透明度小于aReduction时消失
     * @para dotsMinDist：dot最小距离
     * @para maxDistFromCursor：dot最大距离
     *
     * */
    var config = {
        star_r : 3,
        star_alpha : 5,
        initStarsPopulation : 150,
        move_distance : 0.25,
        dot_r : 5,
        dot_speeds : 0.5,
        dot_alpha : 0.5,
        dot_aReduction : 0.01,
        dotsMinDist : 5,
        maxDistFromCursor : 50,
    };
```

如需修改，在`CanvasStar.init()`时传入对象的参数
```
<script>
    var CanvasStar = new CanvasStar;
    var conf = {
        star_r : 10,
        star_alpha : 50,
        initStarsPopulation : 10,
        move_distance : 0.65,
        dot_r : 7,
        dot_speeds : 5,
        dot_alpha : 0.5,
    };
    CanvasStar.init(conf);
</script>
```
