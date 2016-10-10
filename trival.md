### position:fixed height 100% 失效
查了一下主要是transform 的value不为none，就会发生这个问题transform(stackoverflow)[http://stackoverflow.com/questions/15194313/webkit-css-transform3d-position-fixed-issue]
有记载

### ios 双击 页面上移
http://www.cnblogs.com/Ivangel/p/4377972.html

### 点击按钮会出现选中文字 然后复制之类的命令行出现。
其实就是屏蔽选中，用css
```css
.row-of-icons {
  -webkit-user-select: none;  /* Chrome all / Safari all */
  -moz-user-select: none;     /* Firefox all */
  -ms-user-select: none;      /* IE 10+ */
  user-select: none;          /* Likely future */      
}
.force-select {  
  -webkit-user-select: all;  /* Chrome 49+ */
  -moz-user-select: all;     /* Firefox 43+ */
  -ms-user-select: all;      /* No support yet */
  user-select: all;          /* Likely future */   
}
```