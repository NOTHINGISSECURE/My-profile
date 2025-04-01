# My-profile
About myself 
<!DOCTYPE html>
<html lang="en">

<head>
     <title>MR_NOTHINGx</title>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <meta http-equiv="X-UA-Compatible" content="ie=edge">
     <!-- <link rel="stylesheet" href="css/style.css"> -->
     <link rel="shortcut icon" href="x.ico" type="image/x-icon">
<style>
@import url('https://fonts.googleapis.com/css2?family=Titillium+Web:ital@1&display=swap');
@import url('https://fonts.googleapis.com/icon?family=Material+Icons');
@import url('https://fonts.googleapis.com/css2?family=Space+Mono&display=swap');

* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

:root {
    -webkit-tap-highlight-color: #0000;
    -webkit-user-select: none; 
    -ms-user-select: none; 
    user-select: none;
}

body {
    background-position: center;
    background-repeat: no-repeat;
    background-size: 100%;
    -webkit-background-size: 100%;
    -moz-background-size: 100%;
    -o-background-size: 100%;
    overflow: hidden;
}

h1:hover {
    cursor: pointer;
    background-color: #e8e1ef;
    color: #100b16;
    border-radius: .25em;
    padding: 1rem 2rem;
    transition: all 300ms linear;
}

#check {
    display: none;
}

#particles-js {
    position: absolute;
    width: 100%;
    height: 100%;
    background-color: #100b16;
    background-repeat: no-repeat;
    background-size: 100%;
    background-position: 50% 50%;
    transition: all .3s;
}

/* .loader {
    position: fixed;
    z-index: 99999;
    background-color: #100b16;
    width: 100vw;
    height: 100vh;
    color: #e8e1ef;
    display: flex;
    opacity: 1;
    justify-content: center;
    align-items: center;
    font-family: 'Space Mono', monospace;
    font-size: 1.25rem;
    transition: all 300ms linear;
} */

.modal{
    position: fixed;
    width: 100%;
    height: 100vh;
    background-color: #000000cc;
    z-index: -1;
    opacity: 0;
    transition: .5s;
    backdrop-filter: blur(5px);
}

.modal img{
    position: absolute;
    top: 25%;
    left: 50%;
    transform: translate(-50%, -50%) scale(.3);
    max-width: 100%;
    max-height: 100%;
    transition: .5s;
    border-radius: 5px;
}

.modal.show{
    opacity: 1;
    z-index: 99;
}

.modal.show img{
    top: 50%;
    transform: translate(-50%, -50%) scale(1);
}

.container {
    font-family: 'Poppins', sans-serif;
    padding: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    transition: .3s;
}

.card {
    position: relative;
    width: 400px;
    border-radius: 10px;
    overflow: hidden;
    transition: .3s;
    --anim: none;
}

.card:before {
    content: '';
    position: absolute;
    width: 100%;
    height: 270px;
    top: 0;
    left: 0;
    clip-path: circle(400px at 50% -48.5%);
    transition: .3s;
    animation: var(--anim);
}

.header{
    position: relative;
    height: 265px;
    transition: .3s;
}

.mail {
    position: absolute;
    top: 1rem;
    right: 2rem;
    font-size: 1.5rem;
    opacity: .8;
    transition: .3s;
    z-index: 3;
    text-decoration: none;
}

.mail:hover {
    opacity: 1;
    transform: scale(1.07);
}

.hamburger-menu{
    position: relative;
    width: 21px;
    height: 16px;
    top: 1.4rem;
    left: 1.9rem;
    z-index: 3;
    cursor: pointer;
    transition: .3s;
    opacity: .8;
}

.hamburger-menu:hover{
    opacity: 1;
    position: relative;
    width: 25px;
}

.hamburger-menu .center{
    position: relative;
    height: 2px;
    width: 70%;
    top: 50%;
    transform: translateY(-50%);
    border-radius: 1px;
    transition: .3s;
}

.hamburger-menu:before, .hamburger-menu:after{
    content: '';
    position: absolute;
    width: 100%;
    height: 2px;
    border-radius: 1px;
    transition: .3s;
}

.hamburger-menu:before{
    top: 0;
}

.hamburger-menu:after{
    bottom: 0;
}

.main{
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    transition: .3s;
}

.main .image{
    position: relative;
    width: 110px;
    height: 110px;
    border-radius: 50%;
    background: url('1.jpg') no-repeat center / cover;
    margin-bottom: 2px;
    overflow: hidden;
    cursor: pointer;
    transition: border .3s;
}

.image .hover{
    color: #fff;
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: .5s;
    opacity: 0;
}

.image:hover .hover {
    opacity: 1;
}

.hover.active {
    opacity: 1;
}

.name {
    color: #fff;
    font-size: 1.2rem;
    font-weight: 500;
    line-height: 1;
    margin: 5px 0;
    transition: .3s;
}

.sub-name {
    color: #fff;
    font-family: 'Titillium Web', sans-serif;
    font-size: 1.2rem;
    opacity: .8;
    transition: .3s;
}

.content {
    display: flex;
    padding: 1.7rem 2.5rem 2.6rem 2.5rem;
    transition: .3s;
}

.right {
    padding-top: 1.5rem;
    display: flex;
    flex-direction: column;
    text-align: right;
    align-items: flex-end;
    justify-content: space-between;
    margin-left: 2.1rem;
    transition: .3s;
}

.number {
    color: #333;
    font-size: 2.1rem;
    font-weight: 200;
    line-height: 1.2;
    transition: .3s;
}

.number-title {
    color: #666;
    font-size: .55rem;
    font-weight: 400;
    line-height: 1;
    letter-spacing: 1px;
    text-transform: uppercase;
    transition: .3s;
}

.title {
    position: relative;
    font-weight: 500;
    font-size: 1.1rem;
    padding: 0 0 3px 0;
    margin-bottom: .9rem;
    display: inline-block;
    transition: .3s;
}

.title:after {
    content: '';
    position: absolute;
    height: 3px;
    width: 50%;
    border-radius: 1.5px;
    bottom: 0;
    left: 0;
}

.text {
    font-weight: 300;
    line-height: 1.7;
    transition: .3s;
}

.icons-container {
    padding: 1rem 0;
    transition: .3s;
}

.icon {
    font-size: 1.3rem;
    text-decoration: none;
    margin-right: 8px;
    transition: .3s;
}

.buttons-wrap {
    display: flex;
    margin-top: 5px;
    transition: .3s;
}

.follow-wrap, .share-wrap {
    flex: 4;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: .3s;
}

.follow-wrap:hover, .share-wrap:hover {
    flex: 5;
}

.follow {
    padding: 9.6px 0;
    width: 100%;
    text-align: center;
    text-decoration: none;
    font-size: .7rem;
    letter-spacing: 1px;
    text-transform: uppercase;
    border-radius: 18.1px;
    margin-right: 3px;
    transition: .3s;
    animation: none;
}

.share {
    padding: 7.6px 0;
    width: 100%;
    text-decoration: none;
    text-align: center;
    font-size: .7rem;
    letter-spacing: 1px;
    text-transform: uppercase;
    margin-left: 3px;
    border-radius: 18.1px;
    transition: .3s;
}

.close {
    position: absolute;
    top: 1rem;
    right: 1rem;
    width: 30px;
    height: 30px;
    cursor: pointer;
    transition: .3s;
}

.close:before, .close:after {
    background-color: #fff;
    content: '';
    position: absolute;
    width: 100%;
    height: 3px;
    border-radius: 1.5px;
    top: 50%;
    left: 50%;
}

.close:before {
    transform: translate(-50%, -50%) rotate(45deg);
}

.close:after {
    transform: translate(-50%, -50%) rotate(135deg);
}

.close:hover {
    opacity: .5;
}

.sidebar {
    position: absolute;
    top: 50px;
    left: 15px;
    width: 45%;
    z-index: 1000;
    display: none;
    backdrop-filter: blur(12.5px);
    border-radius: 10px;
    border: 1px solid #00000025;
    transition: .3s;
}

.sidebar a {
    padding: 10px 15px;
    text-decoration: none;
    justify-content: center;
    display: flex;
    font-family: 'Poppins', sans-serif;
    transition: .3s;
}

.sidebar a:hover {
    transform: scale(1.2);
}

.dark .card {
    background-color: #00000060;
    box-shadow: 0 5px 15px 1px #0001;
    backdrop-filter: blur(10px);
}

.dark .card:before {
    background: #734f96;
}

.dark .mail {
    color: #1b262c;
}

.dark .hamburger-menu .center {
    background-color: #000;
}

.dark .hamburger-menu:before, .dark .hamburger-menu:after {
    background-color: #000;
}

.dark .main .image {
    border: 4px solid #24192f;
}

.dark .image .hover {
    background-color: #734f96a9;
}

.dark .title {
    color: #fff;
}

.dark .title:after {
    background-color: #fff;
}

.dark .text {
    color: #fff;
}

.dark .icon {
    color: #fff;
}

.dark .icon:hover {
    color: #734f96;
}

.dark .follow {
    background: #734f96;
    color: #000;
}

.dark .share {
    border: 2px solid #734f96;
    color: #734f96;
}

.dark .sidebar {
    background-color: #0005;
}

.dark .sidebar a {
    color: #fff;
}

.light .card{
    background-color: #ffffff60;
    box-shadow: 0 5px 15px 1px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(7.5px);
}

.light .card:before {
    background: linear-gradient(to top, #7F00FF, #E100FF);
}

.light .mail {
    color: #fff;
}

.light .hamburger-menu .center {
    background-color: #fff;
}

.light .hamburger-menu:before, .light .hamburger-menu:after {
    background-color: #fff;
}

.light .main .image {
    border: 4px solid #c300ff;
}

.light .image .hover {
    background: #9c00cc69;
}


.light .title {
    color: #555;
}

.light .title:after {
    background-color: #555;
}

.light .text {
    color: #666;
}

.light .icon {
    color: #c4c4c4;
}

.light .icon:hover {
    color: #9D4EDD;
}

.light .follow {
    background: linear-gradient(to right, #7F00FF, #E100FF);
    color: #fff;
}

.light .share {
    border: 2px solid #6200ffc0;
    color: #7F00FF;
}

.light .close:before, .light .close:after {
    background-color: #fff;
}

.light .sidebar a {
   color: #510080;
}

@media (max-width: 410px) {
    .content{
        flex-direction: column;
    }

    .right{
        flex-direction: row;
        text-align: center;
        justify-content: space-around;
        align-items: center;
        margin: 0;
    }
}

@media (max-width: 370px){
    .header{
        height: 230px;
    }

    .card:before{
        clip-path: circle(400px at 50% -74.5%);
        height: 230px;
    }

    .hamburger-menu{
        width: 16px;
        height: 12px;
        top: 1.1rem;
        left: 1.5rem;
    }

    .mail{
        font-size: 1.1rem;
        top: .75rem;
        right: 1.5rem;
    }

    .main .image{
        width: 90px;
        height: 90px;
        border-width: 3px;
    }

    .name, .sub-name{
        font-size: 1rem;
    }

    .content{
        padding: 1.2rem 1.8rem 1.8rem 1.8rem;
    }

    .number{
        font-size: 1.8rem;
    }

    .number-title{
        font-size: .4rem;
    }

    .right{
        padding-top: 1rem;
    }

    .title{
        font-size: .9rem;
        margin-bottom: .5rem;
    }

    .text{
        font-size: .8rem;
    }

    .icons-container{
        padding: .5rem 0;
    }

    .icon{
        font-size: 1.1rem;
    }

    .follow{
        padding: 7.6px 0;
        border-radius: 14.6px;
        font-size: .6rem;
    }

    .share{
        padding: 5.6px 0;
        border-radius: 14.6px;
        font-size: .6rem;
    }
}


.wrapper {
    position: absolute;
    left: 0;
    top: 20px;
    transform: scale(.8);
    margin-left: -75px;
}
.toggle {
    position: relative;
    display: inline-block;
    width: 100px;
    margin-left: 100px;
    padding: 5px;
    border-radius: 40px;
}
.toggle:before, .toggle:after {
    content: '';
    display: block;
}
.toggle:after {
    clear: both;
}
.toggle-bg {
    position: absolute;
    top: -5px;
    left: -5px;
    width: 100%;
    height: 100%;
    background-color: #e7bdffa1;
    border-radius: 40px;
    border: 5px solid #e0aaff;
    transition: all 300ms cubic-bezier(0.25, 0.46, 0.45, 0.94);
    backdrop-filter: blur(2.5px);
    transition: .3s;
}
.toggle-input {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 1px solid red;
    border-radius: 40px;
    z-index: 2;
    opacity: 0;
    transition: .3s;
}
.toggle-switch {
    position: relative;
    width: 40px;
    height: 40px;
    margin-left: 50px;
    background-color: #f5eb42;
    border: 5px solid #e4c74d;
    border-radius: 50%;
    transition: all 300ms cubic-bezier(0.25, 0.46, 0.45, 0.94);
    transform: translate(-4px,-4px);
}
.toggle-switch-figure {
    position: absolute;
    bottom: -15px;
    left: -50px;
    display: block;
    width: 80px;
    height: 30px;
    border: 8px solid #d4d4d2;
    border-radius: 20px;
    background-color: #fff;
    transform: scale(0.4);
    transition: all 300ms cubic-bezier(0.25, 0.46, 0.45, 0.94);
}
.toggle-switch-figure:after {
    content: '';
    display: block;
    position: relative;
    top: -65px;
    right: -40px;
    width: 15px;
    height: 15px;
    border: 8px solid #d4d4d2;
    border-radius: 100%;
    border-right-color: transparent;
    border-bottom-color: transparent;
    transform: rotateZ(70deg);
    background-color: #fff;
}
.toggle-switch-figure:before {
    content: '';
    display: block;
    position: relative;
    top: -25px;
    right: -15px;
    width: 30px;
    height: 30px;
    border: 8px solid #d4d4d2;
    border-radius: 100%;
    border-right-color: transparent;
    border-bottom-color: transparent;
    transform: rotateZ(30deg);
    background-color: #fff;
}
.toggle-switch-figureAlt {
    content: '';
    position: absolute;
    top: 5px;
    left: 5px;
    width: 2px;
    height: 2px;
    background-color: #efeeda;
    border-radius: 100%;
    border: 4px solid #dee1c5;
    box-shadow: 42px -7px 0 -3px #fcfcfc, 65px -10px 0 -3px #fcfcfc, 54px 4px 0 -2px #fcfcfc, 70px 7px 0 -2px #fcfcfc, 55px 30px 0 -4px #fcfcfc, 44px 20px 0 -2px #fcfcfc, 65px 20px 0 -3px #fcfcfc;
    transition: all 0.12s cubic-bezier(0.25, 0.46, 0.45, 0.94);
    transform: scale(0);
}
.toggle-switch-figureAlt:before {
    content: '';
    position: absolute;
    top: -5px;
    left: 5px;
    width: 10px;
    height: 10px;
    background-color: #efeeda;
    border-radius: 100%;
    border: 2.5px solid #dee1c5;
}
.toggle-switch-figureAlt:after {
    content: '';
    position: absolute;
    top: 10px;
    width: 1.5px;
    height: 1,5px;
    background-color: #efeeda;
    border-radius: 100%;
    border: 2.5px solid #dee1c5;
}
.toggle-input:checked ~ .toggle-switch {
    margin-left: 0;
    border-color: #dee1c5;
    background-color: #fffdf2;
}
.toggle-input:checked ~ .toggle-bg {
    background-color: #2d1f3da1;
    border-color: #231830;
}
.toggle-input:checked ~ .toggle-switch .toggle-switch-figure {
    margin-left: 40px;
    opacity: 0;
    transform: scale(0.1);
}
.toggle-input:checked ~ .toggle-switch .toggle-switch-figureAlt {
    transform: scale(1);
}

@keyframes fadeIn {
    0% {
        opacity: 0; 
        display: none;
    }
    100% {
        opacity: 1;
        display: block;
        z-index: 1000;
    }
  }

@keyframes fadeOut {
    0% { 
        opacity: 1; 
        display: block;
    }
    100% { 
        opacity: 0; 
        display: none;
        z-index: 0;
    }
  }

@keyframes cardDarkGradient {
    0% {
        background-image: linear-gradient(to top, #7F00FF, #E100FF);
    }
    100% {
        background: #734f96;
    }
}

@keyframes cardLightGradient {
    0% {
        background: #734f96;
    }
    100% {
        background-image: linear-gradient(to top, #7F00FF, #E100FF);
    }
}

@keyframes followDarkGradient {
    0% {
        background-image: linear-gradient(to right, #7F00FF, #E100FF);
    }
    100% {
        background: #734f96;
    }
}

@keyframes followLightGradient {
    0% {
        background: #734f96;
    }
    100% {
        background-image: linear-gradient(to right, #7F00FF, #E100FF);
    }
  }
</style>
</head>

<body id="body" class="dark" oncontextmenu="return false">
     <!-- <div class="loader" id="loader">
          <h1 data-value="OreO" id="loader-text">Created by OreO</h1>
     </div> -->
     <div id="particles-js"></div>
<script>
  function hexToRgb(e) {
  var a = /^#?([a-f\d])([a-f\d])([a-f\d])$/i;
  e = e.replace(a, function (e, a, t, i) {
    return a + a + t + t + i + i;
  });
  var t = /^#?([a-f\d]{2})([a-f\d]{2})([a-f\d]{2})$/i.exec(e);
  return t
    ? { r: parseInt(t[1], 16), g: parseInt(t[2], 16), b: parseInt(t[3], 16) }
    : null;
}
function clamp(e, a, t) {
  return Math.min(Math.max(e, a), t);
}
function isInArray(e, a) {
  return a.indexOf(e) > -1;
}
var pJS = function (e, a) {
  var t = document.querySelector("#" + e + " > .particles-js-canvas-el");
  this.pJS = {
    canvas: { el: t, w: t.offsetWidth, h: t.offsetHeight },
    particles: {
      number: { value: 400, density: { enable: !0, value_area: 800 } },
      color: { value: "#fff" },
      shape: {
        type: "circle",
        stroke: { width: 0, color: "#ff0000" },
        polygon: { nb_sides: 5 },
        image: { src: "", width: 100, height: 100 }
      },
      opacity: {
        value: 1,
        random: !1,
        anim: { enable: !1, speed: 2, opacity_min: 0, sync: !1 }
      },
      size: {
        value: 20,
        random: !1,
        anim: { enable: !1, speed: 20, size_min: 0, sync: !1 }
      },
      line_linked: {
        enable: !0,
        distance: 100,
        color: "#fff",
        opacity: 1,
        width: 1
      },
      move: {
        enable: !0,
        speed: 2,
        direction: "none",
        random: !1,
        straight: !1,
        out_mode: "out",
        bounce: !1,
        attract: { enable: !1, rotateX: 3e3, rotateY: 3e3 }
      },
      array: []
    },
    interactivity: {
      detect_on: "canvas",
      events: {
        onhover: { enable: !0, mode: "grab" },
        onclick: { enable: !0, mode: "push" },
        resize: !0
      },
      modes: {
        grab: { distance: 100, line_linked: { opacity: 1 } },
        bubble: { distance: 200, size: 80, duration: 0.4 },
        repulse: { distance: 200, duration: 0.4 },
        push: { particles_nb: 4 },
        remove: { particles_nb: 2 }
      },
      mouse: {}
    },
    retina_detect: !1,
    fn: { interact: {}, modes: {}, vendors: {} },
    tmp: {}
  };
  var i = this.pJS;
  a && Object.deepExtend(i, a),
    (i.tmp.obj = {
      size_value: i.particles.size.value,
      size_anim_speed: i.particles.size.anim.speed,
      move_speed: i.particles.move.speed,
      line_linked_distance: i.particles.line_linked.distance,
      line_linked_width: i.particles.line_linked.width,
      mode_grab_distance: i.interactivity.modes.grab.distance,
      mode_bubble_distance: i.interactivity.modes.bubble.distance,
      mode_bubble_size: i.interactivity.modes.bubble.size,
      mode_repulse_distance: i.interactivity.modes.repulse.distance
    }),
    (i.fn.retinaInit = function () {
      i.retina_detect && window.devicePixelRatio > 1
        ? ((i.canvas.pxratio = window.devicePixelRatio), (i.tmp.retina = !0))
        : ((i.canvas.pxratio = 1), (i.tmp.retina = !1)),
        (i.canvas.w = i.canvas.el.offsetWidth * i.canvas.pxratio),
        (i.canvas.h = i.canvas.el.offsetHeight * i.canvas.pxratio),
        (i.particles.size.value = i.tmp.obj.size_value * i.canvas.pxratio),
        (i.particles.size.anim.speed =
          i.tmp.obj.size_anim_speed * i.canvas.pxratio),
        (i.particles.move.speed = i.tmp.obj.move_speed * i.canvas.pxratio),
        (i.particles.line_linked.distance =
          i.tmp.obj.line_linked_distance * i.canvas.pxratio),
        (i.interactivity.modes.grab.distance =
          i.tmp.obj.mode_grab_distance * i.canvas.pxratio),
        (i.interactivity.modes.bubble.distance =
          i.tmp.obj.mode_bubble_distance * i.canvas.pxratio),
        (i.particles.line_linked.width =
          i.tmp.obj.line_linked_width * i.canvas.pxratio),
        (i.interactivity.modes.bubble.size =
          i.tmp.obj.mode_bubble_size * i.canvas.pxratio),
        (i.interactivity.modes.repulse.distance =
          i.tmp.obj.mode_repulse_distance * i.canvas.pxratio);
    