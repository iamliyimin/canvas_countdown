# canvas_countdown
a project about canvas
canvas 绘图与动画基础
1. 在body中添加<canvas></canvas>标签，设置样式及其大小
2. canvas的大小设置有两种方法，一种是直接在canvas标签内设置width和height的值，而且是不带px单位的。一种是在js里获取canvas对象后直接使用'canvas对象.width'和'canvas对象.height'来设置大小。不建议使用css的方式设置画布大小，因为这里的大小不单是指画布的显示大小还有画布显示分辨率，如果使用css方法设置就只是设置了画布的显示大小而已，没有设置分辨率，这样会造成分辨率不适合该画布的结果。
3. 先设置绘制状态，再使用绘制方法进行具体绘制，stroke()方法绘制线条，fill()方法给多边形实心着色
4. 使用context.moveTo()和context.lineTo()定义一个路径。若想要定义多个路径并且让其分开，则使用context.beginPath()和context.closePath()来将多个图形的首位分隔开。当绘制的状态的路径不是封闭状态时，使用了closePath()，closePath()会自动使用一条线段将这个不封闭的路径的首尾连接起来形成一个封闭的路径，常见于画非圆的弧时，若是不想要封闭，可以去掉closePath()的使用。
5. 使用context.arc(centerX, centerY, radius, startingAngle, endingAngle, anticlockwise=false)方法绘制弧线，参数包括原点x坐标，原点y坐标， 起始角度，结束角度，是否逆时针（false为顺时针，true为逆时针）；特别说明的是无论是顺时针还是逆时针，无论开始和结束弧度是多少，弧度值的位置是不变的，依然是按照顺时针从0pi、0.5pi、1pi、1.5pi、2pi(跟0pi重叠)这样两两之间相隔90度来排布。

