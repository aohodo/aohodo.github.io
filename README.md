# aohodo.github.io<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0"
          name="viewport">
    <meta content="ie=edge" http-equiv="X-UA-Compatible">
    <title>Document</title>

    <style>
        * {
            margin: 3.3px;
            padding:3.3px;
        }

        html, body {
            width: 90%;
            height: 90vh;
            background:rgb(58, 58, 158);
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .btn-box {
            width: 805px;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-wrap: wrap;
        }

        .box {
            position: relative;
            width: 256px;
            height: 125px;
            border-radius: 15px;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            text-align: center;
            user-select: none;
            margin: 5px;
            box-shadow: 10px 10px 10px blue;
        }

        .box:nth-of-type(1) {
            background: linear-gradient(
                    150deg,
                    rgb(251, 182, 5),
                    rgb(36, 122, 28)
            );
        }

        .box:nth-of-type(2) {
            background: linear-gradient(
                    150deg,
                    rgb(241, 43, 84),
                    rgb(237, 11, 125)
            );
        }

        .box:nth-of-type(3) {
            background: linear-gradient(
                    150deg,
                    rgb(65, 182, 73),
                    rgb(125, 195, 65)
            );
        }

        .box:nth-of-type(4) {
            background: linear-gradient(
                    150deg,
                    rgb(5, 239, 63),
                    rgb(85, 34, 89)
            );
        }

        .box:nth-of-type(5) {
            background: linear-gradient(
                    150deg,
                    rgb(134, 0, 255),
                    rgb(103, 0, 255)
            );
        }

        .box:nth-of-type(6) {
            background: linear-gradient(
                    150deg,
                    rgb(79, 11, 148),
                    rgb(183, 52, 178)
            );
        }

        .ripple {
            display: block;
            position: absolute;
            border-radius: 100%;
            background: rgba(25, 25, 255, 0.5);
            transform: scale(0);
        }


        .animation {
            animation: ripple 0.6s ease-in;
        }

        @keyframes ripple {
            100% {
                transform: scale(9);
                opacity: 0;
            }
        }


    </style>


</head>
<body>

<div class="btn-box">
    <div class="box">
        <span class="ripple"></span>
        <p><a href="https://www.xmu.edu.cn/" target="_blank">南国海风吹拂钟塔百年沧桑</a></p>
        <p>囊萤映雪同集南洋国光</p>
    </div>
    <div class="box">
        <span class="ripple"></span>
        <p><a href="https://qzone.qq.com/" target="_blank">胡晨煜~aohodo</a></p>
    </div>
    <div class="box">
        <span class="ripple"></span>
        <p>22920202202777</p>
    </div>
    <div class="box">
        <span class="ripple"></span>
        <p><a href="https://www.xmu.edu.cn/" target="_blank">信息学院·示范性软件学院</a></p>
        <p>大学人，博学笃行，南方之强</p>
    </div>
    <div class="box">
        <span class="ripple"></span>
        <p>大一计算机，大二通信人</p>
    </div>
    <div class="box">
        <span class="ripple"></span>
        <p><a href="http://www.fjpnyz.com/" target="_blank">我的青春记忆</a></p>
        <p>自强不息，止于至善，人生不茫茫</p>
    </div>
</div>

<script>
    let box = document.querySelectorAll(".box");
    for (let i = 0; i < box.length; i++) {
        box[i].onmouseenter = function (event) {
            let ripple = box[i].querySelector(".ripple");
            ripple.classList.add("animation");
            ripple.style.width = this.offsetWidth + "px";
            ripple.style.height = this.offsetWidth + "px";
            ripple.style.top = -(this.offsetHeight - event.offsetY) + "px";
            ripple.style.left = -(this.offsetWidth / 2 - event.offsetX) + "px";
            setTimeout(function () {
                ripple.classList.remove("animation");
            }, 500)

        }
    }


</script>


</body>
</html>
