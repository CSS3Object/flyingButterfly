# 飞舞的蝴蝶flyingButterfly

效果如下

![](images/img.gif)

HTML代码:fdfdfdsfdsf

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>CSS3逼真的蝴蝶飞舞动画 -A5源码</title>
  <link rel="stylesheet" href="css/style.css"/>
</head>
<body>
<div id="container">
  <div id="butterfly">
    <div class="left wing"></div>
    <div class="right wing"></div>
  </div>
</div>
</body>
</html>
```

CSS代码：
```
body{
	background-color: lightblue;
}
#container {
	perspective: 600px;
	perspective-origin: -20% 20%;
	width: 850px;
	height: 566px;
	left: 300px;
	top: 0px;
	color: gray;
	margin: 0px auto;
}

#butterfly {
	transform: rotateZ(-30deg) rotate3d(0, 1, 0, 0deg) scale3d(0.5, 0.5, 0.5);
	transform-origin: 51% 50%;
	left: 0px;
	top: 0px;
	width: 400px;
	height: 238px;
	transform-style: preserve-3d;
	/*Fly in a loop below*/
	/*animation-name: butterflyani;
      animation-duration: 5s;
      animation-iteration-count: infinite;
      animation-timing-function: linear;*/
}
.wing {
	transform: rotateX(30deg)  translate3d(-200px, 0px, 0px) rotate3d(0, 1, 0, 160deg);
	transform-origin: top right;
	position: absolute;
	left: 200px;
	top: 0px;
	width: 200px;
	height: 238px;
	background: url(../images/butterfly.png) no-repeat;
	animation-name: rightwingani;
	animation-duration: 0.6s;
	animation-delay: 2s;
	animation-iteration-count: 4;
	animation-timing-function: ease-out;
}

#butterfly .left{
	transform: rotateX(30deg) rotate3d(0, 1, 0, 0deg);
	animation-name: leftwingani;
	left: 0px;
	top: 0px;
}

@keyframes rightwingani {
	from {
		transform:rotateX(30deg) translate3d(-200px, 0px, 0px) rotate3d(0, 1, 0, 160deg);
	}
	50% {
		transform:rotateX(30deg) translate3d(-200px, 0px, 0px) rotate3d(0, 1, 0, 100deg);
	}
	to{
		transform:rotateX(30deg) translate3d(-200px, 0px, 0px) rotate3d(0, 1, 0, 160deg);
	}
}

@keyframes leftwingani {
	from {
		transform:rotateX(30deg) rotate3d(0, 1, 0, 0deg);
	}
	50% {
		transform:rotateX(30deg) rotate3d(0, 1, 0, 80deg);
	}
	to{
		transform:rotateX(30deg) rotate3d(0, 1, 0, 00deg);
	}
}
a {
	font-size: 5.5em;
	font-family: Arial;
	text-decoration: none;
	text-align: right;
	color: teal;
	letter-spacing: -2px;
	position: relative;
	top: -70%;
	left: -9%;
	width: 67%;
	display: block;
	line-height: 1.1em;
}
```
