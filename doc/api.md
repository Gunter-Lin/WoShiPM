# 人人都是产品经理 - API接口（使用Fiddler抓包）

## Host : api.woshipm.com

## 1、获取所有的资讯类型：
  > url：config/menuV3.html

  > method：get

  > response：
  ```
        {
        "RESULT":
        {
        "menus":[
            {"cName":"首页","eName":"home","icon":"http://api.woshipm.com/images/icon/home.png","bType":0,"bUrl":"","bColor":""},
            {"cName":"业界动态","eName":"it","icon":"http://api.woshipm.com/images/icon/it.png","bType":0,"bUrl":"","bColor":""},
            {"cName":"交互视觉","eName":"ucd","icon":"http://api.woshipm.com/images/icon/ucd.png","bType":0,"bUrl":"","bColor":""},
            {"cName":"产品经理","eName":"pmd","icon":"http://api.woshipm.com/images/icon/pmd.png","bType":0,"bUrl":"","bColor":""},
            {"cName":"分析评测","eName":"evaluating","icon":"http://api.woshipm.com/images/icon/rp.png","bType":0,"bUrl":"","bColor":""},
            {"cName":"产品设计","eName":"pd","icon":"http://api.woshipm.com/images/icon/pd.png","bType":0,"bUrl":"","bColor":""},
            {"cName":"产品运营","eName":"operate","icon":"http://api.woshipm.com/images/icon/operate.png","bType":0,"bUrl":"","bColor":""},
            {"cName":"人人专栏","eName":"discuss","icon":"http://api.woshipm.com/images/icon/discuss.png","bType":0,"bUrl":"","bColor":""},
            {"cName":"原型设计","eName":"rp","icon":"http://api.woshipm.com/images/icon/yxsj.png","bType":0,"bUrl":"","bColor":""},
            {"cName":"职场攻略","eName":"zhichang","icon":"http://api.woshipm.com/images/icon/zhichang.png","bType":0,"bUrl":"","bColor":""},
            {"cName":"创业学院","eName":"chuangye","icon":"http://api.woshipm.com/images/icon/it.png","bType":0,"bUrl":"","bColor":""}
        ]
        },
        "CODE":200
        }
        ```


## 2、获取首页资讯列表
> url：news/listV3.html?type=[eName]&PS=xxx&LTime=xxx

> params：
 - type：指明获取哪类资讯信息，传入接口1中获取到的eName
 - PS：获取多少条
 - LTime：毫秒时间戳，可以用来获取下拉加载更多的数据

> response：
```
    {
    "RESULT":
    {
    "news":
    [
    {
    "id":644634,
    "uid":39251,
    "type":"ucd",
    "title":"如何运用预置的内容和默认设置，创造更好的用户体验",
    "image":"http://image.woshipm.com/wp-files/2017/04/LKfqg3IrjVwTjZhNRRuG-202x150.png, http://image.woshipm.com/wp-files/2017/04/IM7LbQeIbulsZ40OX2hX-202x150.png, http://image.woshipm.com/wp-files/2017/04/knhRqsM5xvJuIgeTJvLk-202x150.png",
    "creator":"可乐橙",
    "tag":"交互体验 用户体验 表单输入框 默认项",
    "link":"http://api.woshipm.com/ucd/644634.html?sf=mobile",
    "description":"首先出现的数值和设置内容就是默认项。它们的作用似乎微乎其微，但默认项（和它们的设计者）掌握着强大的力量——替",
    "publishTime":1492948664000,
    "clickCount":"584",
    "praiseCount":3,
    "tClickCount":121,
    "UID":39251,
    "imageList":["http://image.woshipm.com/wp-files/2017/04/LKfqg3IrjVwTjZhNRRuG.png","http://image.woshipm.com/wp-files/2017/04/IM7LbQeIbulsZ40OX2hX.png","http://image.woshipm.com/wp-files/2017/04/knhRqsM5xvJuIgeTJvLk.png"],
    "publishTimeStr":"2小时前",
    "URole":"专栏作家",
    "clickCountStr":"584"
    },{...},{...}
    ]
    },"CODE":200}
```