# HQCardFlowView
效果：
![](https://img-blog.csdn.net/20180724141023415?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTA5NjAyNjU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)


###  参考UITableView的UITableViewDataSource和UITableViewDelegate两个方法实现；支持五险轮播，可以加载本地图片，也可以加载网络图片，可以根据自己的需求自定义

##  UITableViewDelegate
```
/**
*  当前显示cell的Size(中间页显示大小)
*
*  @param flowView 
*
*  @return CGSize
*/
- (CGSize)sizeForPageInFlowView:(HQFlowView *)flowView;

/**
*  滚动到了某一列
*
*  @param pageNumber 
*  @param flowView   
*/
- (void)didScrollToPage:(NSInteger)pageNumber inFlowView:(HQFlowView *)flowView;

/**
*  点击了第几个cell
*
*  @param subView 点击的控件
*  @param subIndex    点击控件的index
*
*  @return 
*/
- (void)didSelectCell:(HQIndexBannerSubview *)subView withSubViewIndex:(NSInteger)subIndex;
```

##  UITableViewDataSource
```
/**
*  返回显示View的个数
*
*  @param flowView 
*
*  @return 
*/
- (NSInteger)numberOfPagesInFlowView:(HQFlowView *)flowView;

/**
*  给某一列设置属性
*
*  @param flowView 
*  @param index    
*
*  @return 
*/
- (HQIndexBannerSubview *)flowView:(HQFlowView *)flowView cellForPageAtIndex:(NSInteger)index;
```
