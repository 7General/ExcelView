# ExcelView
IOS表格自定义视图，支持XIB布局，支持代码布局，支持锁双向表头。<br>

##效果展示

![image](https://github.com/RmondJone/ExcelView/blob/master/ExcelViewDemo/GIF.gif)

##更新日志

* 更新时间2017年02月11日09:48:27  -----ExcelView V1.0.0

##API使用说明

```objective-c 
    self.leftTableDataArray=(NSMutableArray *)@[@"塔城",@"哈密",@"和田",@"阿勒泰",@"克州"];
    self.rightTableHeadArray=(NSMutableArray *)@[@"当日收入（万）",@"同比",@"环比",@"当月收入（万）",@"同比",@"环比",@"当年收入（万）",@"同比",@"环比"];
    self.excelDataArray=(NSMutableArray *)@[@[@"2.9",@"2%",@"3%",@"3.0",@"4%",@"5%",@"18",@"4.5%",@"6.8%"],@[@"2.9",@"2%",@"3%",@"3.0",@"4%",@"5%",@"18",@"4.5%",@"6.8%"],@[@"2.9",@"2%",@"3%",@"3.0",@"4%",@"5%",@"18",@"4.5%",@"6.8%"],@[@"2.9",@"2%",@"3%",@"3.0",@"4%",@"5%",@"18",@"4.5%",@"6.8%"],@[@"2.9",@"2%",@"3%",@"3.0",@"4%",@"5%",@"18",@"4.5%",@"6.8%"]];
    
    //代码方式添加
    ExcelView *excelView=[[ExcelView alloc]initWithFrame:CGRectMake(0, 280, UIScreenWidth, 270)];
    excelView.topTableHeadDatas=self.rightTableHeadArray;
    excelView.leftTabHeadDatas=self.leftTableDataArray;
    excelView.tableDatas=self.excelDataArray;
    excelView.isLockFristColumn=YES;
    excelView.isLockFristRow=YES;
    excelView.isColumnTitlte=YES;
    excelView.columnTitlte=@"地区";
    [excelView show];
    [self.view addSubview:excelView];
    
    
    //xib布局添加方式
    self.mExcelView.topTableHeadDatas=self.rightTableHeadArray;
    self.mExcelView.leftTabHeadDatas=self.leftTableDataArray;
    self.mExcelView.tableDatas=self.excelDataArray;
    self.mExcelView.isLockFristColumn=YES;
    self.mExcelView.isLockFristRow=YES;
    self.mExcelView.isColumnTitlte=YES;
    self.mExcelView.columnTitlte=@"地区";
    [self.mExcelView show];

```
##目前支持可自定义属性

```objective-c 
/**
 是否锁定第一列
 */
@property BOOL isLockFristColumn;
/**
 是否锁定第一行
 */
@property BOOL isLockFristRow;
/**
 是否存在第一列列标题
 */
@property BOOL isColumnTitlte;
/**
 列标题名称（表格左上角数据）
 */
@property(nonatomic,copy) NSString *columnTitlte;
/**
 第一行表头数据（不包括表格左上角数据，只接收字符串）
 */
@property(nonatomic,retain) NSMutableArray *topTableHeadDatas;
/**
 第一列表头数据（不包括表格左上角数据，只接收字符串）

 */
@property(nonatomic,retain) NSMutableArray *leftTabHeadDatas;
/**
 表格数据（2维数组，不包括第一列和第一行数据，只接收字符串，例：@[@[],@[],....]）
 */
@property(nonatomic,retain) NSMutableArray *tableDatas;

/**
 显示，必须调用该方法，视图才会展现
 */
-(void)show;

```

##问题反馈
* 联系方式：QQ(2318560278）
* 技术交流群：QQ(264587303)
* Demo作者：郭翰林
    
    
    
