<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>一键六学 v1.1</title>
<script type="text/javascript" src="//bog.ac/template/js/jquery.min.js"></script>
<style>
@font-face {
	font-family: 'wbficonregular';
    src: url("//img.t.sinajs.cn/t6/style/images/common/font/wbficon.eot?id=201811011533") ;
    src: url("//img.t.sinajs.cn/t6/style/images/common/font/wbficon.eot?id=201811011533#iefix")  format('embedded-opentype'),         url("//img.t.sinajs.cn/t6/style/images/common/font/wbficon.svg?id=201811011533")  format('svg'),         url("//img.t.sinajs.cn/t6/style/images/common/font/wbficon.woff?id=201811011533")  format('woff'),         url("//img.t.sinajs.cn/t6/style/images/common/font/wbficon.ttf?id=201811011533")  format('truetype');
	src: url("//img.t.sinajs.cn/t6/style/images/common/font/wbficon.eot?id=201811011533") \9;    font-weight: normal;
    font-style: normal;
}
body {
	width: 600px;
	min-height: 500px;
	margin: 0 auto;
	padding: 16px 0 0 0;
    background-color: #b4daf0;
    font: 12px/1.3 Arial,"PingFang SC","Hiragino Sans GB","Microsoft YaHei","WenQuanYi Micro Hei",sans-serif;
    overflow-x: hidden;
    color: #333;
    -webkit-font-smoothing: antialiased;
}
.f {
    font-size: 15px;
    color: #124969;
}
input {
    background: #b4daf0;
    border-bottom: 1px solid #000;
    width: 150px;
    height: 24px;
    padding: 0 8px;
    border-top: none;
    border-left: none;
    border-right: none;
	outline:none;
}
input::-webkit-input-placeholder{
    color:#75accc
}

textarea {
    height: 100px;
    border-radius: 2px;
    -webkit-appearance: none;
    box-sizing: border-box;
    overflow: auto;
    color: #555;
    width: 100%;
    padding: 5px 10px;
    outline: none;
    border: none;
    resize: none;
    background-color: #fff;
    box-shadow: 0 0 2px rgba(0,0,0,0.2);
}

.button {
margin: 10px 0;
    padding: 0px;
    height: 36px;
    line-height: 36px;
    color: #fff;
    font-size: 16px;
    box-sizing: border-box;
    overflow: auto;
    width: 100%!important;
    transition: 0s;
    background: #ff8140 none repeat scroll 0 0;
    box-shadow: 0 1px 2px rgba(0, 0, 0, 0.25);
    white-space: nowrap;
    display: inline-block;
    border-radius: 2px;
    text-decoration: none;
    text-align: center;
    outline: none;
}
.button:hover {
    background: #f7671d none repeat scroll 0 0;
    color: #fff;
}
.button:active {
    background: #de6f36 none repeat scroll 0 0;
    color: #fff;
}
.weibo_main {
    background-color: #fff;
    margin: 0 0 10px 0;
    box-shadow: 0 0 2px rgba(0,0,0,0.2);
    border-radius: 2px;
}
.weibo_c {
    background-image: url(//img.t.sinajs.cn/t6/skin/public/feed_cover/star_057_pc_x2.png?version=41c059f3d4d6eda9);
    padding: 20px 20px 4px;
    background-repeat: no-repeat;
    background-position: right top;
    background-size: 600px;
}
.weibo_face {
    position: relative;
    width: 50px;
    float: left;
}
.weibo_face_radius {
    border-radius: 50%;
}
.weibo_detail {
    margin-left: 60px;
}
.weibo_info {
    margin-bottom: 7px;
    padding: 5px 0 0;
}
.weibo_info_name {
    color: #333;
    text-decoration: none;
    font-size: 14px;
    font-weight: 700;
}
.weibo_approve {
    background-image: url(//img.t.sinajs.cn/t6/style/images/common/steps_gold.png);
    background-size: 475px 14px;
    background-position: left;
    background-repeat: no-repeat;
    margin-left: 3px;
    vertical-align: -2px;
    width: 15px;
    height: 14px;
    display: inline-block;
}
.vip {
    display: inline-block;
    background-image: url(//img.t.sinajs.cn/t6/style/images/common/icon.png);
    background-repeat: no-repeat;
    background-position: -25px -125px;
    width: 16px;
    height: 14px;
    vertical-align: -2px;
    margin-left: 3px;
}
a{
    color: #808080;
    text-decoration: none;
}
a:hover{
    color: #eb7350;
}
.weibo_from {
    margin-bottom: 2px;
    color: #808080;
    text-decoration: none;
    letter-spacing: normal;
    word-spacing: normal;
    vertical-align: top;
    font-size: 12px;
    display: inline-block;
}
.weibo_text {
    margin-bottom: 2px;
    padding-bottom: 0;
    padding: 1px 0 3px;
    overflow: hidden;
    line-height: 23px;
    word-wrap: break-word;
    letter-spacing: normal;
    word-spacing: normal;
    font-size: 14px;
}
.weibo_b_handle {
    overflow: hidden;
}
ul {
    border-top-width: 1px;
    border-top-style: solid;
    border-color: #f2f2f5;
    margin: 0 0 0 -1px;
    zoom: 1;
    padding: 0;
}
ul:after {
    content: ".";
    display: block;
    height: 0;
    clear: both;
    visibility: hidden;
}
li {
    width: 25%;
    float: left;
    height: 38px;
    list-style: none;
}
.pos {
    margin: 0 0 0 1px;
    padding: 1px 0;
    color: #808080;
    text-decoration: none;
    display: block;
    margin-left: -1px;
    text-align: center;
}
.line {
    display: block;
    height: 22px;
    margin: 7px 0;
    border-left-width: 1px;
    border-left-style: solid;
    line-height: 22px;
    border-color: #d9d9d9;
}
.S_ficon {
    font-family: "wbficonregular" !important;
    display: inline-block;
    -webkit-font-smoothing: antialiased;
    font-size: 15px;
    vertical-align: top;
    margin-left: 2px;
    margin-right: 3px;
    color: #696e78;
}
em{
    font-style: normal;
    font-weight: normal;
}
.weibo_url{
    color: #eb7350;
}
.weibo_s_l {
    float: left;
    padding-bottom: 5px;
}
.weibo_s_r {
    float: right;
    color: #124969;
    font-size: 14px;
    padding-top: 2px;
}
.share_btn_inner {
    background: url(//img.t.sinajs.cn/t4/appstyle/widget/images/shareButton/share_btn.png?id=1375775002754) no-repeat;
    display: inline-block;
    width: 62px;
    height: 22px;
}
.ico_share_btn {
    float: left;
    width: 16px;
    height: 16px;
    margin: 3px 0 0 3px;
    background: url(//img.t.sinajs.cn/t4/appstyle/widget/images/shareButton/share_icon.png?id=1375775002754) 0 0 no-repeat;
}
.share_text {
    float: left;
    width: 40px;
    height: 16px;
    padding: 4px 0 3px 3px;
    color: #fff;
    text-align: center;
    cursor: pointer;
    font-style: normal!important;
}
</style>
</head>
<body>
<div class="f">
惊闻<input class="input1" placeholder="ATM毕业论文又被打回">，深感<input class="input2" placeholder="同情(笑)">。
虽然我们未曾有过交集，但<input class="input3" placeholder="ATM屡败屡战的精神">，跟孙悟空<input class="input4" value="一身正气" placeholder="一身正气">是一样的。<br>
今年下半年，中美合拍的西游记即将正式开机，我继续扮演美猴王孙悟空，我会用美猴王艺术形象努力创造一个正能量的形象，文体两开花，弘扬中华文化，希望大家能多多关注。
<br>
<a href="#" class="button" >给我六！</a>
</div>
<div class="weibo">
	<div class="weibo_main">
		<div class="weibo_c">
			<div class="weibo_face">
				<div class="face">
					<a class="weibo_face_radius" href="#" title="六小龄童">
						<img src="//tvax3.sinaimg.cn/crop.0.0.1242.1242.180/483521dbly8fwpwlwhwzgj20yi0yiach.jpg" width="50" height="50" alt="六小龄童" class="weibo_face_radius">
					</a>
				</div>
			</div>
			<div class="weibo_detail">
				<div class="weibo_info">
					<a href="#" class="weibo_info_name">六小龄童</a>
					<a href="#"><i title="微博个人认证 " class="weibo_approve"></i></a>
					<a title="微博会员" href="#"><em class="vip"></em></a>
				</div>
				<div class="weibo_from">
					<a href="#" class="S_txt2 time" > 11月1日 08:13</a>
					来自 
					<a class="S_txt2" href="#">iPhone 7 Plus</a>
				</div>
				<div class="weibo_text">
					戏说不是胡说，改编不是乱编！<br>
					该工具为在线微博文本模拟器，仅供娱乐学习使用。<br>
					该工具所使用的用户数据为新浪微博提供，仅为模拟微博显示样式，内容为用户自定义，和工具开发者无关。<br>
					若要弘扬玄奘精神，传承西游文化，请关注大闹天宫首席文化大使<a href="//[图片]weibo.com/liuxiaolingtong" target="_blank" class="weibo_url">@六小龄童</a>老师的微博，一起做一名<a href="//s.weibo.com/weibo/%23%E5%85%AD%E5%AD%A6%E5%AE%B6%23" target="_blank" class="weibo_url">#六学家#</a>！
				</div>
			</div>
		</div>
		<div class="weibo_b">
			<div class="weibo_b_handle">
				<ul>
					<li><span class="pos"><span class="line"><span><em class="S_ficon">û</em><em>收藏</em></span></span></span></li>
					<li><span class="pos"><span class="line"><span><em class="S_ficon"></em><em>1599</em></span></span></span></li>
					<li><span class="pos"><span class="line"><span><em class="S_ficon"></em><em>评论</em></span></span></span></li>
					<li><span class="pos"><span class="line"><span><em class="S_ficon">ñ</em><em>128044</em></span></span></span></li>
				</ul>
			</div>
		</div>
	</div>
</div>
<div class="weibo_s_l">
<cite class="share_btn_inner"><u class="ico_share_btn"></u><cite class="share_text">分享</cite></cite>
</div>
<div class="weibo_s_r">
由于接口限制，分享窗口无法抓取完整文本，请手动复制粘贴。
</div>
<textarea class="666"></textarea>
<script>
$(".button").click(function(){
	if($(".input1").val()==''||$(".input2").val()==''||$(".input3").val()==''||$(".input4").val()==''){//判断有任意一项未填
		if($(".input1").val()==''&&$(".input2").val()==''&&$(".input3").val()==''){//若全部未填，则使用默认值
		var str_1 = '京城权限调戏玩家被ban';
		var str_2 = '同情(笑)';
		var str_3 = '京城的调皮';
		var str_4 = '随性由心';
		}else{//否则跳出
		$(".666").val("没填完怎么六？");
		return;
		}
	}else{//填完的情况下，使用用户输入值
		var str_1 = $(".input1").val();
		var str_2 = $(".input2").val();
		var str_3 = $(".input3").val();
		var str_4 = $(".input4").val();
	};
	$(".time").html(getFormatDate());
	var temp = "惊闻"+ str_1 +"，深感"+ str_2 +"。虽然我们未曾有过交集，但"+ str_3 +"，跟孙悟空"+ str_4 +"是一样的。今年下半年，中美合拍的西游记即将正式开机，我继续扮演美猴王孙悟空，我会用美猴王艺术形象努力创造一个正能量的形象，文体两开花，弘扬中华文化，希望大家能多多关注。​";
	$(".weibo_text").html(temp);
	$(".weibo_text").val('惊闻'+ str_1 +'，深感'+ str_2 +'。虽然我们未曾有过交集，但'+ str_3 +'，跟孙悟空'+ str_4 +'是一样的。今年下半年，中美合拍的西游记即将正式开机，我继续扮演美猴王孙悟空，我会用美猴王艺术形象努力创造一个正能量的形象...');
	$(".666").val(temp);
});
function getFormatDate(){//获取时间
    var nowDate = new Date();
    var month = nowDate.getMonth() + 1 < 10 ? "0" + (nowDate.getMonth() + 1) : nowDate.getMonth() + 1;
    var date = nowDate.getDate() < 10 ? "0" + nowDate.getDate() : nowDate.getDate();
    var hour = nowDate.getHours()< 10 ? "0" + nowDate.getHours() : nowDate.getHours();
    var minute = nowDate.getMinutes()< 10 ? "0" + nowDate.getMinutes() : nowDate.getMinutes();
    return month + "月" + date+"日 "+hour+":"+minute;
};
$(".share_btn_inner").click(function() {//分享
	var title = $(".weibo_text").val();
		if(title == ''){//未生成时，默认分享
		var title = '一键六学'
		};
	var openUrl = "http://service.weibo.com/share/share.php?url=https%3A%2F%2Fbognmb.com%2Ftool%2F6%2F&type=button&language=zh_cn&appkey=1716545151&title=%23%E5%85%AD%E5%AD%A6%E5%AE%B6%23" + title + "&pic=https%3A%2F%2Fww1.sinaimg.cn%2Flarge%2F005GvIo1gy1fxzstwun51j303c03cq2s.jpg&style=number"; //弹出窗口的url
	var iWidth = 630; //弹出窗口的宽度;
	var iHeight = 580; //弹出窗口的高度;
	var iTop = (window.screen.availHeight - 30 - iHeight) / 2; //获得窗口的垂直位置;
	var iLeft = (window.screen.availWidth - 10 - iWidth) / 2; //获得窗口的水平位置;
	window.open(openUrl, "", "height=" + iHeight + ", width=" + iWidth + ", top=" + iTop + ", left=" + iLeft + "" + ",toolbar=no, menubar=no, scrollbars=no, resizable=no, location=no, status=no");
});
</script>
</body>
</html>

