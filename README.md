#### lacssanimation
#####1
######CSS transform basics
```
transform: translate(100px, 50px) skew(20deg) scale(2) rotate(53deg)
```

######simple 3D
in wrapper:
```
perspective: 1000px;
```
inner:
```
transform:rotateY(45deg)
```
######CSS animation
```
transition: background .5s ease-in, transform .25s .25s(delay) ease-in;
```
hover:
```
transform:scale(1.2);
background:
```
#####2Understanding CSS Animations
######Use animation-delay and animation-fill-mode
fill-mode:forwards  //stop at the end state  
[full example] (http://codepen.io/SitePoint/pen/emjxYg)  
summary:  
none(default): stop at start,color will change after delaying period.  
forwards: (applies stypes from the last executed keyframe after animation ends)stop at final,color will change after delaying period.  
backwards:(applies stypes from the last executed keyframe b4 animation starts) stop at start,color will change when starts.  
both:stop at final,color will change when starts.  
######animation-direction
```
normal/reverse/alternate/alternate-reverse
```
#####3 CSS Animation Buliding Blocks
create animation property respectively in keyframes
```
section{animation: a 1s linear;}
@keyframes a{0%{transform:translateY(100px);animation-timing-function:ease-out;}50%{transform:translateY(100px);animation-timing-function:ease-in;}}
```
if two keyframes(animations) applys on same object, it will take effect simultaneously  
```
section{animation: a 1s linear,b 2s ease-in-out;}
```
######pause and play with animation-play-state
using turn
```
100%{transform: rotate(1turn);}
```

how to use
```
x{
  animation: a 10s linear;
  animation-play-state:paused
}
x:hover{
  animaton-play-state:running;
}
@keyframes a{...}
```
######animate aprite images with steps
image:
```
.image{
  display:block;
  background:transparent url(image.png) 0 0 no-repeat;
  animation-timing-function:steps(4);  //Or: animation: a 2s steps(4) infinite;
}
```
move sprite image
```
@keyframes a{
  0%{background-position 0 0;}
  0%{background-position 0 -10000px;}
}
```

#####5
######most performant properties
opacity,scale, rotation, position with transform  
[css triggers](http://csstriggers.com)  
css will-change property (opera dev)


#####6 Tools
######Helpful online tools
svgomg  
svg_optimizer peter  
sara soueidan (understanding svg coordinate)  
