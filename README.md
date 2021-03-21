# 3D-Text-marquee-effect
.....html.....
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <link href="style.css" rel="stylesheet" type="text/css" />
  </head>
  <body>
    <div class="box">
  <div class="inner">
    <span>CSS Love</span>
  </div>
  <div class="inner">
    <span>YOU GO GIRL!</span>
  </div>
</div>
  </body>
</html>
.....css.....
html,
body {
	height: 100%;
	display: flex;
	align-items: center;
	justify-content: center;
	background-color: black;
}

.box {
	display: flex;
}

.box .inner {
	width: 600px;
	height: 200px;
	line-height: 200px;
	font-size: 3em;
	font-family: sans-serif;
	font-weight: bold;
	white-space: nowrap;
	overflow: hidden;
}

.box .inner:first-child {
	background-color: lightpink;
	color: springgreen;
	transform-origin: left;
	transform: perspective(100px) rotateY(-15deg);
}

.box .inner:last-child {
	background-color: tomato;
	color: antiquewhite;
	transform-origin: left;
	transform: perspective(100px) rotateY(15deg);
}

.box .inner span {
	position: absolute;
	animation: marquee 3s linear infinite;
}

.box .inner:first-child span {
	animation-delay: 2.5s;
	left: -100%;
}

@keyframes marquee {
	from {
		left: 100%;
	}

	to {
		left: -100%;
	}
}
