# 分享组件
一个东凑西凑魔改出来的分享组件, 加上平时遇到客户的需求会顺便加上，效果貌似还行~<br><br>
Demo：http://demo.gfwboom.com/myshare<br>
博客：https://gfwboom.com/archives/code/javascript/2017/02/08/271.html<br>
```
var config = {
            url: window.location.href,
            title: document.title,
            desc: _desc,
            img: document.getElementsByTagName('img').length > 0 && document.getElementsByTagName('img')[0].src,
            img_title: document.title,
            from: window.location.host,
			
			// 如果使用UC、QQ浏览器会调用其分享接口
			// 1：底部(有微信)、有右上角
			// 2: 底部(有微信)、无右上角
			// 3: 底部(无微信)、有右上角
			// 4: 底部(无微信)、无右上角
			// 5: 底部(有微信、但点击后提示复制下方链接)、有右上角
			// 6: 底部(有微信、但点击后提示复制下方链接)、无右上角
			// 7: 底部(有微信、但点击后提示复制下方链接)、点击微信、朋友圈才显示右上角提示
            // 8: 无底部、仅右上角
			// 9: 底部(无QQ、无QQ空间、无微信)、无右上角
			// 10: 底部(无QQ、无QQ空间、无微信)、有右上角
			// 11: 底部(无QQ、无QQ空间、有微信但点击后提示复制下方链接)、点击微信或朋友圈才显示右上角
			// 12: 底部(无QQ、无QQ空间、有微信但点击后提示复制下方链接)、无右上角
			// 13: 底部(无微博、无QQ、无QQ空间、无微信)、无右上角
			// 14: 底部(无微博、无QQ、无QQ空间、无微信)、有右上角
			// 15: 底部(无微博、无QQ、无QQ空间、有微信但点击后提示复制下方链接)、点击微信或朋友圈才显示右上角
			// 16: 底部(无微博、无QQ、无QQ空间、有微信但点击后提示复制下方链接)、无右上角
			
			//指定app弹出某个类型的分享组件,通过浏览器ua来判断
            //(UC浏览器、QQ浏览器、手机QQ内置浏览器、微信(可覆盖,默认7)已在js文件里判断,如需改动需要到js里改,此处无需再填)，
            appShowType: {//格式： '【UA(全小写)】':【类型1~7】
                'weibo': 3,
				'weixin': 7  //js里已默认7,也可覆盖，仅微信('weixin')
            },
            defaultShowType: 6 //默认显示类型6
        };
```
#感谢
https://github.com/caixiaojia/wxshare<br>
https://github.com/AngusFu/uc-qq-share-to-wechat<br>
https://github.com/ZouStrong/Project-Wap-Share<br>
