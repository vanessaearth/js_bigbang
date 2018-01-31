# js大杂烩
获取地址栏参数值用字符串的split方法

split将字符串以传入的关键字，将原先的字符串风格中2个字符串

~~~
例如当前网址为如下：
https://www.baidu.com/s?wd=%E5%A8%83%E5%93%88%E5%93%88&rsv_spt=1&rsv_iqid=0xb1ebebd30001a5ad&issp=1&f=8&rsv_bp=1&rsv_idx=2&ie=utf-8&rqlang=cn&tn=baiduhome_pg&rsv_enter=1&oq=%25E7%2588%25B1%25E5%25A5%2587%25E8%2589%25BA&inputT=2748&rsv_t=60124RBX%2B45ze439k5oi27MoTpaJBeiKYHvb4Nuzi7DbiK4yMnEMgCW4oKkeiJH6H3zh&rsv_pq=84fb005f00020ac5&rsv_sug3=9&rsv_sug1=6&rsv_sug7=100&bs=%E7%88%B1%E5%A5%87%E8%89%BA

var str=location.href.split('?');
//运行上面的split分割后str变为
str=['https://www.baidu.com/s','wd=%E5%A8%83%E5%93%88%E5%93%88&rsv_spt=1&rsv_iqid=0xb1ebebd30001a5ad&issp=1&f=8&rsv_bp=1&rsv_idx=2&ie=utf-8&rqlang=cn&tn=baiduhome_pg&rsv_enter=1&oq=%25E7%2588%25B1%25E5%25A5%2587%25E8%2589%25BA&inputT=2748&rsv_t=60124RBX%2B45ze439k5oi27MoTpaJBeiKYHvb4Nuzi7DbiK4yMnEMgCW4oKkeiJH6H3zh&rsv_pq=84fb005f00020ac5&rsv_sug3=9&rsv_sug1=6&rsv_sug7=100&bs=%E7%88%B1%E5%A5%87%E8%89%BA']
str2 = str[1].split("&");
//str2=["wd=%E5%A8%83%E5%93%88%E5%93%88", "rsv_spt=1", "rsv_iqid=0xb1ebebd30001a5ad", "issp=1", "f=8", "rsv_bp=1", "rsv_idx=2", "ie=utf-8", "rqlang=cn", "tn=baiduhome_pg", "rsv_enter=1", "oq=%25E7%2588%25B1%25E5%25A5%2587%25E8%2589%25BA", "inputT=2748", "rsv_t=60124RBX%2B45ze439k5oi27MoTpaJBeiKYHvb4Nuzi7DbiK4yMnEMgCW4oKkeiJH6H3zh", "rsv_pq=84fb005f00020ac5", "rsv_sug3=9", "rsv_sug1=6", "rsv_sug7=100", "bs=%E7%88%B1%E5%A5%87%E8%89%BA"]
var str3={};
for(var i=0;i<str2.length;i++){
	var q=str2[i].split('=');
	str3[q[0]]=q[1];
}
str3={wd: "%E5%A8%83%E5%93%88%E5%93%88", rsv_spt: "1", rsv_iqid: "0xb1ebebd30001a5ad", issp: "1", f: "8", …}
~~~