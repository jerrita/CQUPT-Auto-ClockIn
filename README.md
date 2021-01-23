# 某高校自动打卡脚本

## 事先声明
1. 本脚本仅供学习交流使用，请勿过分依赖。时刻注意每天是否打卡成功，如若失败，请手动打卡。
2. 本脚本仅限低风险地区学生使用，并且不要前往中高风险地区。如果身体出现新冠肺炎相关症状，请立即报告辅导员。
3. 本脚本需要自行抓包才能正常使用，为了避免脚本被滥用，在此我不会提供抓包相关教程。
4. 开发者对使用或不使用本脚本造成的问题不负任何责任，不对脚本执行效果做出任何担保，原则上不提供任何形式的技术支持。



你需要创建一个priv.py，自行填入以下信息
```python
conf = {
    'xh': xxx,
    'name': 'xxx',
    'xb': 'x',
    'lxdh': xxx,  # 联系电话
    'xxdz': 'xxx',  # 详细地址
    'openid': 'xxx'  # openId
}

# http://api.map.baidu.com/lbsapi/getpoint/index.html
loc = (x, x)  # 在以上链接获取您的经纬度信息，直接复制

modify = {
    "ywjcqzbl": "低风险", "ywjchblj": "无", "xjzdywqzbl": "无", "twsfzc": "是",
    "ywytdzz": "无", "beizhu": "无"
}   
# 此为默认值，如有修改需求，请自己导入并修改
# ad = AutoDk(config=conf, location=loc, modify=modify)
```



之后，在你的服务器上执行

```bash
docker build -t mrdk:v1 .
docker run --name mrdk -d mrdk:v1
```

记得关注日志。