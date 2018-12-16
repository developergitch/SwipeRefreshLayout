### SwipeRefresh supports pull-down refresh and pull-up loading for a single View
### SwipeNest scroll view (supports various common View recycleView scrollView listView and other mixed arrangements) Handling scrolling conflicts With pull-down refresh and pull-up loading
### MultipleListAdapter<T> Simple and fast implementation of ListView multiple types of display
### MultipleRecycleAdapter<T> Simple and fast implementation RecycleView multiple types of display

Add Gradle dependency:
```gradle
dependencies {
      compile 'com.github.powyin:scroll:3.2.5'
      compile 'com.android.support:recyclerview-v7:24.0.0'
}
```

### SwipeRefresh UI

|Refresh (customizable)|Launch load to get new data (customizable)|Upload and load data are all available (customizable)|
|---|---|----
|![github](https://github.com/powyin/nest-scroll/blob/master/app/src/main/res/raw/refresh_pre.gif)|![github](https://github.com/powyin/nest-scroll/blob/master/app/src/main/res/raw/refresh_load_2.gif)|![github](https://github.com/powyin/nest-scroll/blob/master/app/src/main/res/raw/refresh_load_1.gif)|


### SwipeNest UI

|Refresh (customizable)|Smooth scrolling conflicts between various Views|Custom refresh example|
|---|---|----
|![github](https://github.com/powyin/nest-scroll/blob/master/app/src/main/res/raw/nest_pre.gif)|![github](https://github.com/powyin/nest-scroll/blob/master/app/src/main/res/raw/nest_pre_1.gif)|![github](https://github.com/powyin/nest-scroll/blob/master/app/src/main/res/raw/nest_pre_2.gif)|

### how to use  SwipeRefresh

```
    <com.powyin.scroll.widget.SwipeRefresh>
        <!--ListView-->
        <android.support.v7.widget.RecyclerView/>
    </com.powyin.scroll.widget.SwipeRefresh>
```
    
### how to use  SwipeNest 

```
    <com.powyin.scroll.widget.SwipeNest>
        <FrameLayout>
            <ImageView />
        </FrameLayout>
        <android.support.v7.widget.RecyclerView/>
        <ImageView />
    </com.powyin.scroll.widget.SwipeNest>
```

### Set refresh listener and refresh result processing

ISwipe

        ISwipe.setOnRefreshListener(new SwipeRefresh.OnRefreshListener() {
            @Override
            public void onRefresh() {
                // Start pull-down refresh
            }

            @Override
            public void onLoading(boolen isLoadViewShow) {
                // Start loading more
            }
        });
        
        ISwipe.setFreshStatue(ISwip.RreshStatus.SUCCESS);             //Pulldown refresh complete
        ISwipe.setFreshStatue(ISwipe.RreshStatus.ERROR);              //Pulldown refresh failed
 
        
        
### SwipeRefresh set refresh mode

```
ISwipe.setSwipeModel(SwipeControl.SwipeModel model)
(BOTH = SwipeModel.SWIPE_BOTH)                    Support for pull-down refresh and pull-up loading 
(ONLY_REFRESH == SwipeModel.SWIPE_ONLY_REFRESH))  Only pull-down refresh
(ONLY_REFRESH == SwipeModel.SWIPE_ONLY_LOADINN)   Only pull-up loading is supported 
(SWIPE_NONE == SwipeModel.SWIPE_NONE）           Not supported
```


### MultipleRecycleAdapter&MultipleListAdapter&MultipleViewPageAdapter
```     
PowViewHolder<T> This class abstracts the necessary conditions for getting ListAdapter.Item and Recycle.Adapter.Item and PagerAdapter.Item;
The generic type must be determined when using it;
AdapterDelegate<T> This interface defines the ListAdapter and RecycleView.Adatper and PagerAdapter public data operations;
```        
        
