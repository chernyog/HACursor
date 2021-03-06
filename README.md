# HACursor

## Introduction:
**HACursor**，是一个对横向ScrollView中的视图进行管理的UI控件。只要几行代码就可以集成类似于网易新闻对主题页面进行排序，删除操作的功能。
## Presentation:
#### 滚动效果
![(下拉刷新02-动画图片)](http://ww2.sinaimg.cn/bmiddle/96a577c4gw1eubkkqtxoeg20ad0j1n9b.gif)
#### 排序效果
![(下拉刷新02-动画图片)](http://ww4.sinaimg.cn/bmiddle/96a577c4gw1eubkkz6pz2g20ad0j1az2.gif)
#### 删除效果
![(下拉刷新02-动画图片)](http://ww2.sinaimg.cn/bmiddle/96a577c4gw1eubkl6e1akg20ad0j1e82.gif)

## Usage:
#### 代码例子:其中（必选）为必须设置的属性，其余可根据需要来设置

    HACursor *cursor = [[HACursor alloc]init];
    cursor.frame = CGRectMake(0, 20, self.view.width, 45);
    
    //显示的标题栏的标题（必选！！）
    cursor.titles = self.titles; 
    //需要管理的子页面（必选！！）
    cursor.pageViews = self.pageViews;
    //设置rootScrollView的高度（必选！！）
    cursor.rootScrollViewHeight = self.view.frame.size.height - 65;
    
    //设置标题普通状态下的颜色
    cursor.titleNormalColor = [UIColor whiteColor];
    //设置标题选中状态下的颜色
    cursor.titleSelectedColor = [UIColor redColor];
    //是否需要显示排序的按钮
    cursor.showSortbutton = YES;
    //设置背景颜色
    cursor.backgroundColor = [UIColor yellowColor];
    //设置最小化的字体
    cursor.minFontSize = 10.0;
    //设置最大化的字体
    cursor.maxFontSize = 30.0;
    //设置是否需要渐变字体的大小
    cursor.isGraduallyChangFont = NO;
    //设置是否需要渐变字体的颜色
    cursor.isGraduallyChangColor = NO;
    [self.view addSubview:cursor];
## Requirement:
* iOS7.0以上
* Xcode 6
