# CSS
css样式库

- 单行省略

```
.row-ellipsis {
  overflow: hidden;
  text-overflow:ellipsis;
  white-space: nowrap;
}
```

- 多行省略 （3行）

> 使用了WebKit扩展属性，该方法适用于WebKit浏览器及移动端

```
.rows-ellipsis {
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 3;
  overflow: hidden;
}
```

- 图片置灰
> 下面是css3的代码实现,兼容Ie9以下，谷歌，火狐，浏览器，不兼容ie10+

```
.gray {
  -webkit-filter: grayscale(100%);
  -moz-filter: grayscale(100%);
  -ms-filter: grayscale(100%);
  -o-filter: grayscale(100%);
  filter: grayscale(100%);
  //上面代码是兼容火狐与谷歌的样式
  //下面代码是兼容ie9以下浏览器的样式，包括ie9
  filter: gray;
}
```

- 解决苹果手机滚动卡顿

```
.containBox{
    width: 100%;
    position: absolute;
    top: 50px;
    left: 0;
    right: 0;
    bottom: 50px;
    overflow-x: hidden;
    /*overflow-y:auto;//不能写,会和下面的产生冲突*/
    -webkit-overflow-scrolling: touch; // 解决苹果手机滚动卡顿
}
```
