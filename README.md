# Million news text dataset
一个从2018年11月到2023年7月的百万网络财经新闻文本数据集
<br>
----------------------------------------------------------
链接：https://pan.baidu.com/s/1taZicVuNnsSseV3igEHORg 
提取码：1234
<br>
读取合并文件的代码示例：
```python
# python
import pandas as pd

src="dir_name"
data=0
begin=0
for year in range(2018,2024):
    if year==2018:
        for month in range(11,13):
            if month<10:
                month="0"+str(month)
            else:
                month=str(month)
            filename="./"+src+"/"+str(year)+"-"+month+".csv"
            temp_data=pd.DataFrame(pd.read_csv(filename))
            if begin==0:
                data=temp_data
                begin=1
            else:
                data=pd.concat([data,temp_data],axis=0)
    elif year==2023:
        for month in range(1, 8):
            if month<10:
                month="0"+str(month)
            else:
                month=str(month)
            filename="./"+src+"/"+str(year)+"-"+month+".csv"
            temp_data=pd.DataFrame(pd.read_csv(filename))
            data = pd.concat([data, temp_data], axis=0)
    else:
        for month in range(1,13):
            if month<10:
                month="0"+str(month)
            else:
                month=str(month)
            filename="./"+src+"/"+str(year)+"-"+month+".csv"
            temp_data=pd.DataFrame(pd.read_csv(filename))
            data = pd.concat([data, temp_data], axis=0)
data=data.iloc[:,:-1]
data.to_csv('./new_dir_name/'+src+'.csv')
```
----------------------------------------------------------
<br>
由于数据集用于本人辅修毕设，并未发表，请使用者在正文引用该github库链接或点击star。
<br>
仅用于学术研究，禁止贩卖、二次分享数据集，文件有解压密码，目前需要联系我简要说明身份、用途获得。
<br>
如有需要联系jiechengzhang.alex@qq.com
<br>
更新于2023/04/05 
