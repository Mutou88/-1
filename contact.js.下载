/*
 * @Descripttion:
 * @version:
 * @Author: sueRimn
 * @Date: 2021-05-21 22:21:50
 * @LastEditors: Please set LastEditors
 * @LastEditTime: 2022-04-04 20:15:45
 */
// 联系方式在线沟通
// 判断电脑端 、 手机端
let web_type = false; // 默认电脑端
if (navigator.userAgent.match(/(iPhone|iPod|Android|ios|iPad)/i)) {
    // 手机端
    web_type = true;
}

function go_fn(type, id) {
    $("#content").attr("value", id);
    var text = $("#content");
    text.select();
    document.execCommand("copy");

    switch (type) {
        case "qq":
            if (web_type) {
                window.location.href = `mqqwpa://im/chat?chat_type=wpa&uin=${id}&version=1&src_type=web`;
            } else {
                window.location.href = `tencent://message/?uin=${id}&Menu=yes`;
            }
            break;

        case "app":
            if (web_type) {
                window.location.href = `https://35fe.oub109.com:9042/entry/register/?i_code=4801344`;
            } else {
                window.location.href = `https://a1e1.obao88.com:25010/register/?i_code=4801344`;
            }
            break;

        case "wx":
            let html = `<div class="contactBox" id="contactBox">
          <div class="inner-box">
            <div class="wx">
              <img src="./images/ewm.jpg" alt="" />
            </div>

            <div class="s_close" id="s_close">
              <div class="line"></div>
              <div class="line"></div>
            </div>
          </div>
        </div>
        <style>
          .contactBox {
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            position: fixed;
            top: 0;
            left: 0;
            z-index: 999;
            display: flex;
            justify-content: center;
            align-items: center;
          }
          .inner-box {
            width: 300px;
            height: 400px;
          }
          .inner-box .wx img {
            width: 100%;
          }
          .inner-box .s_close {
            margin: 10px auto;
            width: 80px;
            height: 80px;
            background-color: rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            cursor: pointer;
            transition: all 0.3s;
          }
          .inner-box .s_close:hover {
            opacity: 0.6;
          }
          .inner-box .s_close .line {
            position: relative;
            top: 40px;
            left: 10px;
            width: 60px;
            height: 1px;
            background-color: #000;
          }
          .inner-box .s_close .line:nth-of-type(1) {
            transform: rotate(45deg);
          }
          .inner-box .s_close .line:nth-of-type(2) {
            transform: rotate(-45deg);
          }
        </style>`;

            $("body").append(html);

            break;

        case "sk":
            window.location.href = `skype:${id}?call`;
            break;

        case "te":
            window.location.href = `https://t.me/${id}`;
            break;

        case "em":
            window.location.href = `mailto:${id}`;
            break;

        case "fly":
            window.location.href = `https://www.flygram3.com`;
            break;

        case "cc":
            window.location.href = `https://www.cloudchat.com/`;
            break;

        case "bf":
            window.location.href = `https://web.batchat.com/#/login`;
            break;

        case "ft":
            window.location.href = `https://www.potato.im/`;
            break;
    }
}

$("body").on("click", "#s_close", function() {
    $("#contactBox").remove();
});