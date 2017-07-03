# 使用步骤
1.添加Jcenter仓库 Gradle依赖:</br>
```
compile 'com.lyf.slidebarlibrary:slidebarlibrary:0.0.1' 
```

2.在Xml中添加控件</br>
```
        <FrameLayout
          
                android:layout_width="match_parent"
                android:layout_height="match_parent">
                <android.support.v7.widget.RecyclerView

                    android:layout_height="match_parent"
                    android:layout_width="match_parent">

                </android.support.v7.widget.RecyclerView>


                <com.lyf.slidebarlibrary.SlideBar
                   
                    android:layout_width="match_parent"
                    android:layout_height="match_parent"/>


            </FrameLayout> 
```
3.在Activit添加如下代码:</br>
```
 mSlideBar.setSize(100);//recycleview的容器大小
 mSlideBar.setOnTouchingChangedListener(this);
     /**
     * SlideBar的回调
     * @param position
     */
    @Override
    public void onTouchingChanged(int position) {
        //将recycleview滑动到指定位置
        mRvDirectory.smoothScrollToPosition(position);
    }
```
#大功告成~
