## DecisionTreeBktUtil 使用教程
### step 1: 导包
* pip install DecisionTreeBktUtil -i –trusted-host https://pypi.python.org/simple

### step 2: 引用实例

        # 导包
        from DecisionTreeBktUtil import getColBktFromDF
        import pandas as pd
        # 读取csv数据
        df_train = pd.read_csv("./hh.csv",header=0,sep='	')
        # 指定要分桶的列名
        featureCols = ['price']
        # 遍历列名，自动分桶
        for col in featureCols:
            # 在这个地方使用分桶工具
            getColBktFromDF.getFeatureBkt_DT(df_train, col, 'click_label')

### step 3: 拷贝输出的结果
        'price': [0.0, 933.0, 943.0]