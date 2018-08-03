# img缝隙问题

## 问题

img与div（block元素）下方有空隙

> HTML代码
```
<div>
  <img src="https://pic.qyer.com/public/zworld/ad/2018/08/01/15331133527670">
</div>
```
> CSS代码
```
div {
  position: relative;
  background:#ccc;
}

img {
  width: 100%
}
```
>效果
![img](../pic/D18D045D-E635-4A1D-ADAF-0754A9359FB1.png)

## 解决方案

1. 给图片img标签加display: block
2. 给图片img标签加vertical-align: bottom
3. 将div的字体大小设为0 font-size: 0

## 原因

图片文字等inline元素默认是和父级元素的baseline对齐的，而baseline又和父级底边有一定距离（这个距离和 font-size，font-family 相关），所以设置 vertical-align:top/bottom/text-top/text-bottom 都可以避免这种情况出现。
