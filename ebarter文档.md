# 1.引言

# 1.1 编写目的

# 1.2 项目风险

# 1.3文档约定

​		**部件编号方式**：

​		**界面编号方式**：

​		**命名规范**：

​		**命名规范**

				1、 项目名全部小写
	
				2、 包名全部小写
	
				3、 类名首字母大写，如果类名由多个单词组成，每个单词的首字母都要大写。
	
				如：
​                         `public class MyFirstClass{}`
				
​	
​			4、 变量名、方法名首字母小写，如果名称由多个单词组成，每个单词的首字母都要大写。
                  	  `int index=0; public void toString(){}`


​			5、 常量名全部大写

​			如：

  			`public static final String GAME_COLOR=”RED”;`

​		6、所有命名规则必须遵循以下规则：

​			1)、名称只能由字母、数字、下划线、$符号组成

​			2)、不能以数字开头

​			3)、名称不能使用JAVA中的关键字。

​			4)、坚决不允许出现命名。

# 2.2开发工具，中间件以及数据库接口

# 3 部件详细设计

> 这里所提及的软件部件，系指能够完成特定功能、相对独立的一些代码集合 这里特指函数和对象

###●  所属子系统

>指该部件所属的子系统；

>对于不分为多个子系统的软件来说，不必填写该栏。

###●  部件调用者

>指调用该部件的部件(或界面参数)的编号和名称。

###●  部件被调用者

>指被该部件所调用的部件的编号和名称。

###●  部件入口参数

>指该部件入口数据类名称或者数据名称，以及对这些数据的描述；

>如果部件没有入口参数，该栏为空。

###●  部件出口参数

>指该部件出口数据类名称或者数据名称，以及对这些数据的描述；

>如果部件没有出口参数，该栏为空。

###●  算法

>指该部件的算法形式表示，如果很简单、或者不存在，也可以为空。

###●  流程描述

>指该部件的处理流程的详细表示或描述。

###●  部件表示形式

# 4.词汇表

# 5.部件表

##主界面模块

### 截图

![avatar](https://github.com/daxuliu/markdown/raw/master/商城.png) 



|  部件名称   | MainActivity |
|  ----  | ----  |
| 所属子系统  | 无 |
| 部件调用者| 主界面 |
|被调用者| `Readapter` `Product` `Producttool` `MyImageView` |
|入口参数| `dataManager.getInfoMap().get("arrofpro");`登录界面返回的商品信息数组 |
|返回值| 无 |
### 部件页面代码

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/container"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    android:orientation="vertical"
    >
    <com.hjq.bar.TitleBar
        android:id="@+id/toolbar"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="0dp"
        app:title="青岛"
        app:leftIcon="@drawable/address"


        />


    <SearchView
        android:id="@+id/searchView"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:iconifiedByDefault="false"

        android:queryHint="扫地机器人" />
    <com.yalantis.phoenix.PullToRefreshView
        android:id="@+id/pull_to_refresh"
        android:layout_width="match_parent"
        android:layout_height="500dp">
    <ScrollView xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="500dp"
        android:padding="0dp">

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:orientation="vertical">

            <com.youth.banner.Banner xmlns:app="http://schemas.android.com/apk/res-auto"
                android:id="@+id/banner"
                android:layout_width="match_parent"
                android:layout_height="180dp"
                app:indicator_height="8dp"
                app:indicator_margin="4dp"
                app:indicator_width="8dp" />

            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:background="#FFffff"
                android:orientation="horizontal">

                <ImageView

                    android:id="@+id/food"
                    android:layout_width="60dp"
                    android:layout_height="60dp"
                    android:src="@drawable/class1" />

                <ImageView
                    android:id="@+id/office"
                    android:layout_width="60dp"
                    android:layout_height="60dp"
                    android:src="@drawable/class2" />

                <ImageView
                    android:id="@+id/shuma"
                    android:layout_width="60dp"
                    android:layout_height="60dp"
                    android:src="@drawable/class3" />

                <ImageView
                    android:id="@+id/ad"
                    android:layout_width="60dp"
                    android:layout_height="60dp"
                    android:src="@drawable/class4" />

                <ImageView
                    android:id="@+id/service"
                    android:layout_width="60dp"
                    android:layout_height="60dp"
                    android:src="@drawable/class5" />

                <ImageView
                    android:id="@+id/qita"
                    android:layout_width="60dp"
                    android:layout_height="60dp"
                    android:src="@drawable/class6" />


            </LinearLayout>

            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:background="#FFffff"
                android:orientation="horizontal">

                <TextView
                    android:id="@+id/tv1"
                    android:layout_width="66dp"
                    android:layout_height="wrap_content"
                    android:gravity="center"
                    android:text="餐饮" />

                <TextView
                    android:id="@+id/tv2"
                    android:layout_width="66dp"
                    android:layout_height="wrap_content"
                    android:gravity="center"
                    android:text="办公" />

                <TextView
                    android:id="@+id/tv3"
                    android:layout_width="66dp"
                    android:layout_height="wrap_content"
                    android:gravity="center"
                    android:text="数码" />

                <TextView
                    android:id="@+id/tv4"
                    android:layout_width="66dp"
                    android:layout_height="wrap_content"
                    android:gravity="center"
                    android:text="广告" />

                <TextView
                    android:id="@+id/tv5"
                    android:layout_width="66dp"
                    android:layout_height="wrap_content"
                    android:gravity="center"
                    android:text="服务" />

                <TextView
                    android:id="@+id/tv6"
                    android:layout_width="66dp"
                    android:layout_height="wrap_content"
                    android:gravity="center"
                    android:text="其他" />
            </LinearLayout>

            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:background="#FF0000"
                android:orientation="vertical">

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="match_parent"
                    android:layout_gravity="center"
                    android:gravity="center"
                    android:text="最新动态"
                    android:textColor="#ffffff" />

            </LinearLayout>

            <android.support.v7.widget.RecyclerView
                android:id="@+id/rv"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"></android.support.v7.widget.RecyclerView>


        </LinearLayout>
    </ScrollView>
    </com.yalantis.phoenix.PullToRefreshView>
    <LinearLayout
        android:id="@+id/content"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:orientation="vertical">

    </LinearLayout>
    <android.support.design.widget.BottomNavigationView

        android:id="@+id/navigation"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginEnd="0dp"
        android:layout_marginStart="0dp"
        android:background="?android:attr/windowBackground"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:menu="@menu/navigation"
        android:layout_alignParentBottom="true"/>

</LinearLayout>
```



###部件·逻辑代码

```java

package com.example.ebarter;
import android.app.Application;
import android.content.Context;
import android.content.Intent;
import android.os.Bundle;
import android.support.annotation.NonNull;
import android.support.design.widget.BottomNavigationView;
import android.support.v7.app.AppCompatActivity;
import android.support.v7.widget.GridLayoutManager;
import android.support.v7.widget.RecyclerView;
import android.util.Log;
import android.view.Menu;
import android.view.MenuInflater;
import android.view.MenuItem;
import android.view.View;
import android.view.ViewGroup;
import android.widget.AdapterView;
import android.widget.ImageView;
import android.widget.LinearLayout;
import android.widget.SearchView;
import android.widget.TextView;
import android.widget.Toast;

import com.example.ebarter.tools.GlideImageLoader;
import com.example.ebarter.tools.MyImageView;
import com.example.ebarter.tools.Product;
import com.example.ebarter.tools.Readapter;
import com.hjq.bar.OnTitleBarListener;
import com.hjq.bar.TitleBar;
import com.yalantis.phoenix.PullToRefreshView;
import com.youth.banner.Banner;
import com.youth.banner.BannerConfig;
import com.youth.banner.Transformer;

import java.util.ArrayList;

import cn.jpush.android.api.JPushInterface;

public class MainActivity extends AppCompatActivity implements  Readapter.OnItemClickListener {
    private RecyclerView rv;
    private PullToRefreshView    mPullToRefreshView;
    private  ArrayList<Product> products;
    //图片数组
   private DataManager dataManager=DataManager.getInstance();

    private Banner banner;
    private ArrayList list_path = new ArrayList<>();
    private ArrayList<String> list_title = new ArrayList<>();
     private   android.support.v7.app.ActionBar actionBar;
     private ImageView imageView_banner;
    private TitleBar mTitleBar;
    private ImageView iv1,iv2,iv3,iv4,iv5,iv6;
    private TextView tv1,tv2,tv3,tv4,tv5,tv6;
    private  LinearLayout ban1 ,ban2,ban3;
    private BottomNavigationView.OnNavigationItemSelectedListener mOnNavigationItemSelectedListener
            = new BottomNavigationView.OnNavigationItemSelectedListener() {

        @Override
        public boolean onNavigationItemSelected(@NonNull MenuItem item) {
            switch (item.getItemId()) {
                case R.id.navigation_home:
                    //mTextMessage.setText(R.string.title_home);
                    Intent intent=new Intent(MainActivity.this,chatlist.class);
                    startActivity(intent);
                    return true;
                case R.id.navigation_dashboard:
                    //mTextMessage.setText(R.string.title_dashboard);
                    Intent intent2=new Intent(MainActivity.this,Group.class);
                    startActivity(intent2);
                    return true;
                case R.id.navigation_notifications:
                    //mTextMessage.setText(R.string.title_notifications);
                    Intent intent3=new Intent(MainActivity.this,MeActivity.class);
                    startActivity(intent3);
                    return true;
                case R.id.discover:
                    return  true;
            }
            return false;
        }
    };

    /**
     * 获取屏幕宽度；
     */
    public static int getScreenWidth(Context context) {
        return context.getApplicationContext().getResources()
                .getDisplayMetrics().widthPixels;
    }
    private void initView() {
        banner = (Banner)findViewById(R.id.banner);
        //设置banner样式
        banner.setBannerStyle(BannerConfig.CIRCLE_INDICATOR_TITLE);
        //设置banner动画效果
        banner.setBannerAnimation(Transformer.DepthPage);
        banner.isAutoPlay(true);
        //设置轮播间隔时间
        banner.setDelayTime(3000);
        banner.setBannerTitles(list_title);
        Integer[] images={R.drawable.c1,R.drawable.banner,R.drawable.c2};
        //简单使用
        //list_path.
        banner.setImages(list_path)
                .setImageLoader(new GlideImageLoader())
                //.setOnBannerListener(MainActivity.this)
                .start();

    }
    private void initData() {

        list_path.add(R.drawable.banner);
        list_path.add(R.drawable.c1);
        list_path.add(R.drawable.c2);

        list_title.add("图片1");
        list_title.add("图片2");
        list_title.add("图片3");
    }





    @Override
    protected void onCreate(Bundle savedInstanceState) {
        init(this);
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        actionBar=getSupportActionBar();
        actionBar.hide();//隐藏标题栏
        mTitleBar = (TitleBar) findViewById(R.id.toolbar);




        /*轮播图*/

       // Banner banner = (Banner) findViewById(R.id.banner);
        //设置图片加载器
       // banner.setImageLoader(new GlideImageLoader());
        //设置图片集合
       // banner.setImages(images);
        //banner设置方法全部调用完毕时最后调用
       // banner.start();
          mPullToRefreshView = (PullToRefreshView) findViewById(R.id.pull_to_refresh);
        mPullToRefreshView.setOnRefreshListener(new PullToRefreshView.OnRefreshListener() {
            @Override
            public void onRefresh() {
                mPullToRefreshView.postDelayed(new Runnable() {
                    @Override
                    public void run() {
                        initreData();
                        mPullToRefreshView.setRefreshing(false);
                    }
                }, 1000);
            }
        });
        initData();
        initView();
        SearchView searchView=findViewById(R.id.searchView);
        searchView.setFocusable(false);
        dataManager.getInfoMap().get("arrofpro");
        this.products=(ArrayList<Product>)dataManager.getInfoMap().get("arrofpro");
        searchView.setOnQueryTextListener(new SearchView.OnQueryTextListener() {
            //DataManager dataManager=DataManager.getInstance();
            //Intent intent=getIntent();
            //position=intent.getIntExtra("postion",0);


            //输入完成后，点击回车或是完成键
            @Override
            public boolean onQueryTextSubmit(String query) {
                if (query.length() > 0) {
                    Log.e("onQueryTextSubmit","我是点击回车按钮");
                    for(Product p: products){
                        if (p.getName().equals(query)){
                            Intent intent=new Intent(MainActivity.this,Activity_details.class);
                            int postion;
                            postion=products.indexOf(p);
                            intent.putExtra("postion",postion);
                            startActivity(intent);
                        }
                    }

                }
                return true;
            }

            //查询文本框有变化时事件
            @Override
            public boolean onQueryTextChange(String newText) {

                Log.e("onQueryTextChange","我是内容改变");
                return false;
            }
        });
        searchView.setIconified(true);
        mTitleBar.setBackgroundColor(0xffee3333);
        //  textView=(TextView)findViewById(R.id.tv);
        int width=getScreenWidth(this);
        Log.d("TAG", "--onSuccess" + width);
        mTitleBar.setOnTitleBarListener(new OnTitleBarListener() {

            @Override
            public void onLeftClick(View v) {
                // textView.setText("left");
            }

            @Override
            public void onTitleClick(View v) {
                //textView.setText("title");
            }

            @Override
            public void onRightClick(View v) {
                //textView.setText("right");
            }

        });
        iv1=(ImageView)findViewById(R.id.food);
        iv2=(ImageView)findViewById(R.id.service);
        iv3=(ImageView)findViewById(R.id.office);
        iv4=(ImageView)findViewById(R.id.shuma);
        iv5=(ImageView)findViewById(R.id.qita);
        iv6=(ImageView)findViewById(R.id.ad);
        iv1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent=new Intent(MainActivity.this,FenleiActivity.class);
                intent.putExtra("type","餐饮娱乐");
                startActivity(intent);
            }
        });
        iv2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent=new Intent(MainActivity.this,FenleiActivity.class);
                intent.putExtra("type","商务服务");
                startActivity(intent);
            }
        });
        iv3.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent=new Intent(MainActivity.this,FenleiActivity.class);
                intent.putExtra("type","电脑办公");
                startActivity(intent);
            }
        });
        iv4.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent=new Intent(MainActivity.this,FenleiActivity.class);
                intent.putExtra("type","手机数码");
                startActivity(intent);
            }
        });iv5.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent=new Intent(MainActivity.this,FenleiActivity.class);
                intent.putExtra("type","其他");
                startActivity(intent);
            }
        });iv6.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent=new Intent(MainActivity.this,FenleiActivity.class);
                intent.putExtra("type","广告印刷");
                startActivity(intent);
            }
        });
        LinearLayout.LayoutParams params = new LinearLayout.LayoutParams(width/6, LinearLayout.LayoutParams.WRAP_CONTENT);
         iv1.setLayoutParams(params);
        iv2.setLayoutParams(params);
        iv3.setLayoutParams(params);
        iv4.setLayoutParams(params);
        iv5.setLayoutParams(params);
        iv6.setLayoutParams(params);
        tv1=(TextView)findViewById(R.id.tv1);
        tv2=(TextView)findViewById(R.id.tv2);
        tv3=(TextView)findViewById(R.id.tv3);
        tv4=(TextView)findViewById(R.id.tv4);
        tv5=(TextView)findViewById(R.id.tv5);
        tv6=(TextView)findViewById(R.id.tv6);
        tv1.setLayoutParams(params);
        tv2.setLayoutParams(params);
        tv3.setLayoutParams(params);
        tv4.setLayoutParams(params);
        tv5.setLayoutParams(params);
        tv6.setLayoutParams(params);
    /*    ban1=(LinearLayout)findViewById(R.id.ban1);
        ban2=(LinearLayout)findViewById(R.id.ban2);
        ban3=(LinearLayout)findViewById(R.id.ban3);
        LinearLayout.LayoutParams params2=new LinearLayout.LayoutParams(width/3, LinearLayout.LayoutParams.WRAP_CONTENT);
        ban3.setLayoutParams(params2);
        ban2.setLayoutParams(params2);
        ban1.setLayoutParams(params2);
*/
        BottomNavigationView navigation = (BottomNavigationView) findViewById(R.id.navigation);
        navigation.setSelectedItemId(R.id.discover);
        navigation.setOnNavigationItemSelectedListener(mOnNavigationItemSelectedListener);
      /*  imageView_banner=(ImageView)findViewById(R.id.iv_banner);
        imageView_banner.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                startActivity(new Intent(MainActivity.this,Activity_details.class));
            }
        });*/
        rv = (RecyclerView) findViewById(R.id.rv);

       // rv.setAdapter();
        initreData();


    }
    private void initreData() {
        //样式，boolean代表展示的方向
        GridLayoutManager layoutManager = new GridLayoutManager(this, 3 ,GridLayoutManager.VERTICAL,false);
        rv.setLayoutManager(layoutManager);
        Readapter readapter=new Readapter(this,"all");
        readapter.setmOnItemClickLitener(this);
        rv.setAdapter(readapter);

        //数据
      /*  rv.setAdapter(new RecyclerView.Adapter() {
            @Override
            public RecyclerView.ViewHolder onCreateViewHolder(ViewGroup parent, int viewType) {
                View view = View.inflate(parent.getContext(), R.layout.item, null);
                RecyclerView.ViewHolder viewHolder = new RvViewholder(view);
                return viewHolder;
            }

            @Override
            public void onBindViewHolder(final RecyclerView.ViewHolder holder, final int position) {
                //进行数据设置
                RvViewholder myViewholder = (RvViewholder) holder;
                //设置图片
                // myViewholder.itemIv.setImageResource(mListIcons[position]);
                //设置标题数据
                myViewholder.itemIv.setImageURL("https://pic.cnblogs.com/avatar/1142647/20170416093225.png");
                myViewholder.itemTv.setText(mListTitle[position]);
                myViewholder.price.setText(mListTitle[position]);

            }

            @Override
            public int getItemCount() {
                return mListIcons.length;
            }

            class RvViewholder extends RecyclerView.ViewHolder {

                public MyImageView itemIv;
                public TextView itemTv,price;



                 * 初始化控件

                public RvViewholder(View itemView) {
                    super(itemView);
                    itemIv = (MyImageView) itemView.findViewById(R.id.huowuimg);
                    itemTv = (TextView) itemView.findViewById(R.id.huowutype);
                    price=(TextView)itemView.findViewById(R.id.price);
                }

            }

        });*/
    }

    @Override
    public void onItemClick(View v, int postion) {
        Toast toast = Toast.makeText(this, "点击成功！"+postion, Toast.LENGTH_LONG);
        Intent intent=new Intent(this,Activity_details.class);
        intent.putExtra("postion",postion);
        startActivity(intent);
        toast.show();
    }

    @Override
    public void onItemLongClick(View v, int postion) {
        Toast toast = Toast.makeText(this, "点击成功！"+postion, Toast.LENGTH_LONG);
        toast.show();
        Intent intent=new Intent(this,Activity_details.class);
        intent.putExtra("postion",postion);
        startActivity(intent);

    }
    public void search(String  q){}

    //极光
    public static void init(Context context) {

    }

    public class ExampleApplication extends Application {
        @Override
        public void onCreate() {
            super.onCreate();
            JPushInterface.setDebugMode(true);
            JPushInterface.init(this);
        }
    }
}

```

|  部件名称   | Readapter |
|  ----  | ----  |
| 所属子系统  | 商城界面 |
| 部件调用者| 主界面 |
|被调用者| `MyImageView` |
|入口参数| ` Readapter(Context this,type "all");` |
|返回值| 无 |
###部件代码
```java
package com.example.ebarter.tools;

import android.content.Context;
import android.support.v7.widget.RecyclerView;
import android.view.View;
import android.view.ViewGroup;
import android.widget.TextView;
import android.widget.Toast;

import com.example.ebarter.DataManager;
import com.example.ebarter.R;

import java.util.ArrayList;

public class Readapter extends RecyclerView.Adapter<RecyclerView.ViewHolder> implements View.OnClickListener{
   // private RecyclerView rv;
    //图片数组
    private Context that;
    private String type;
    ArrayList<Product> list;
   public Readapter(Context context,String type) {
       this.that=context;
       this.type=type;
   }


    public void onClick(View v) {
        Toast toast = Toast.makeText(that, "点击成功！", Toast.LENGTH_LONG);
        toast.show();

    }


    @Override
        public RecyclerView.ViewHolder onCreateViewHolder(ViewGroup parent, int viewType) {
        View view = View.inflate(parent.getContext(), R.layout.item, null);
        RecyclerView.ViewHolder viewHolder = new RvViewholder(view);
      /*  if (mOnItemClickLitener != null) {
            viewHolder.itemView.setOnClickListener(new View.OnClickListener() {
                @Override
                public void onClick(View v) {
                    // int pos = realPostion;
                    mOnItemClickLitener.onItemClick( viewHolder.itemView,1);
                }
            });
            viewHolder.itemView.setOnLongClickListener(new View.OnLongClickListener()
            {
                @Override
                public boolean onLongClick(View v)
                {
                    // int pos = realPostion;
                    mOnItemClickLitener.onItemLongClick((((RvViewholder) viewHolder).itemIv),2);
                    return true;
                }
            });
        }*/
        return viewHolder;
    }

        @Override
        public void onBindViewHolder(final RecyclerView.ViewHolder holder, final int position) {
        //进行数据设置
        RvViewholder myViewholder = (RvViewholder) holder;
        //设置图片
        // myViewholder.itemIv.setImageResource(mListIcons[position]);
        //设置标题数据
            ArrayList<Product> products;//=new ArrayList();
            DataManager dataManager=DataManager.getInstance();
            products=(ArrayList<Product>) dataManager.getInfoMap().get("arrofpro");
            switch (type){
                case "all":
                    list=products;
                    break;
                case "餐饮娱乐":
                    for (Product p:products
                         ) {
                        if (p.getType().equals("餐饮娱乐")){
                            list=new ArrayList<Product>();
                            list.add(p);
                        }
                    }
                    break;
                case "电脑办公":
                    for (Product p:products
                            ) {
                        if (p.getType().equals("电脑办公")){
                            list=new ArrayList<Product>();
                            list.add(p);
                        }
                    }
                    break;
                case "手机数码":
                    for (Product p:products
                            ) {
                        if (p.getType().equals("手机数码")){
                            list=new ArrayList<Product>();
                            list.add(p);
                        }
                    }
                    break;
                case "广告印刷":
                    for (Product p:products
                            ) {
                        if (p.getType().equals("广告印刷")){
                            list=new ArrayList<Product>();
                            list.add(p);
                        }
                    }
                    break;
                case "居家生活":
                    for (Product p:products
                            ) {
                        if (p.getType().equals("居家生活")){
                            list=new ArrayList<Product>();
                            list.add(p);
                        }
                    }
                    break;

                case "其他":
                    for (Product p:products
                            ) {
                        if (p.getType().equals("其他")){
                            list=new ArrayList<Product>();
                            list.add(p);
                        }
                    }
                    break;
                    default:
                        break;
            }
            products=list;
            String price;
            price=products.get(position).getPrice();
            String name=products.get(position).getName();
            String pic=products.get(position).getPic();
            String orderid=products.get(position).getOrderid();
            orderid=orderid.replace(":","-");
            String img="https://s3.cn-north-1.amazonaws.com.cn/linda-trades-archive-1/";
        myViewholder.itemIv.setImageURL(img+orderid+".jpg");
        myViewholder.itemTv.setText(name);
        myViewholder.price.setText(price);

        if (mOnItemClickLitener != null) {
            holder.itemView.setOnClickListener(new View.OnClickListener() {
                @Override
                public void onClick(View v) {
                    // int pos = realPostion;
                    mOnItemClickLitener.onItemClick(holder.itemView,position);
                }
            });
            holder.itemView.setOnLongClickListener(new View.OnLongClickListener()
            {
                @Override
                public boolean onLongClick(View v)
                {
                    // int pos = realPostion;
                    mOnItemClickLitener.onItemLongClick((((RvViewholder) holder).itemIv),position);
                    return true;
                }
            });
        }
    }

        @Override
        public int getItemCount() {

            ArrayList<Product> products;//=new ArrayList();
            DataManager dataManager=DataManager.getInstance();
            products=(ArrayList<Product>) dataManager.getInfoMap().get("arrofpro");
            switch (type){
                case "all":
                    list=products;
                    break;
                case "餐饮娱乐":
                    for (Product p:products
                            ) {
                        if (p.getType().equals("餐饮娱乐")){
                            list=new ArrayList<Product>();
                            list.add(p);
                        }
                    }
                    break;
                case "电脑办公":
                    for (Product p:products
                            ) {
                        if (p.getType().equals("电脑办公")){
                            list=new ArrayList<Product>();
                            list.add(p);
                        }
                    }
                    break;
                case "手机数码":
                    for (Product p:products
                            ) {
                        if (p.getType().equals("手机数码")){
                            list=new ArrayList<Product>();
                            list.add(p);
                        }
                    }
                    break;
                case "广告印刷":
                    for (Product p:products
                            ) {
                        if (p.getType().equals("广告印刷")){
                            list=new ArrayList<Product>();
                            list.add(p);
                        }
                    }
                    break;
                case "居家生活":
                    for (Product p:products
                            ) {
                        if (p.getType().equals("居家生活")){
                            list=new ArrayList<Product>();
                            list.add(p);
                        }
                    }
                    break;

                case "其他":
                    for (Product p:products
                            ) {
                        if (p.getType().equals("其他")){
                            list=new ArrayList<Product>();
                            list.add(p);
                        }
                    }
                    break;
                case "商务服务":
                    for (Product p:products
                            ) {
                        if (p.getType().equals("商务服务")){
                            list=new ArrayList<Product>();
                            list.add(p);
                        }
                    }
                    break;
                default:
                    break;
            }

           dataManager.getInfoMap().put("realpro",list);
        return list.size();
    }

        class RvViewholder extends RecyclerView.ViewHolder {

            public MyImageView itemIv;
            public TextView itemTv,price;


            /**
             * 初始化控件
             */
            public RvViewholder(View itemView) {
                super(itemView);
                itemIv = (MyImageView) itemView.findViewById(R.id.huowuimg);
                itemTv = (TextView) itemView.findViewById(R.id.huowutype);
                price=(TextView)itemView.findViewById(R.id.price);
            }

        }
        public interface OnItemClickListener{
            void onItemClick(View v,int postion);
            void onItemLongClick(View v,int postion);
        }
        private OnItemClickListener mOnItemClickLitener;

        public void setmOnItemClickLitener(OnItemClickListener mOnItemClickLitener) {
        this.mOnItemClickLitener = mOnItemClickLitener;
    }
    }

```

|  部件名称   | MyImageView |
|  ----  | ----  |
| 所属子系统  | 整个程序 |
| 部件调用者| 带有网络图片的界面 |
|被调用者| 无 |
|入口参数| ` setImageURL(final String path)` |
|返回值| 无 |
###部件逻辑代码
``` java
package com.example.ebarter.tools;

import android.content.Context;
import android.graphics.Bitmap;
import android.graphics.BitmapFactory;
import android.os.Handler;
import android.os.Message;
import android.util.AttributeSet;
import android.widget.ImageView;
import android.widget.Toast;

import java.io.IOException;
import java.io.InputStream;
import java.net.HttpURLConnection;
import java.net.URL;
import android.support.v7.widget.AppCompatImageView;
public class MyImageView extends AppCompatImageView {
    public static final int GET_DATA_SUCCESS = 1;
    public static final int NETWORK_ERROR = 2;
    public static final int SERVER_ERROR = 3;
    //子线程不能操作UI，通过Handler设置图片
    private Handler handler = new Handler() {
        @Override
        public void handleMessage(Message msg) {
            switch (msg.what){
                case GET_DATA_SUCCESS:
                    Bitmap bitmap = (Bitmap) msg.obj;
                    setImageBitmap(bitmap);
                    break;
                case NETWORK_ERROR:
                    Toast.makeText(getContext(),"网络连接失败",Toast.LENGTH_SHORT).show();
                    break;
                case SERVER_ERROR:
                    Toast.makeText(getContext(),"服务器发生错误",Toast.LENGTH_SHORT).show();
                    break;
            }
        }
    };

    public MyImageView(Context context, AttributeSet attrs, int defStyleAttr) {
        super(context, attrs, defStyleAttr);
    }

    public MyImageView(Context context) {
        super(context);
    }

    public MyImageView(Context context, AttributeSet attrs) {
        super(context, attrs);
    }

    //设置网络图片
    public void setImageURL(final String path) {
        //开启一个线程用于联网
        new Thread() {
            @Override
            public void run() {
                try {
                    //把传过来的路径转成URL
                    URL url = new URL(path);
                    //获取连接
                    HttpURLConnection connection = (HttpURLConnection) url.openConnection();
                    //使用GET方法访问网络
                    connection.setRequestMethod("GET");
                    //超时时间为10秒
                    connection.setConnectTimeout(10000);
                    //获取返回码
                    int code = connection.getResponseCode();
                   if (code==200) {
                        InputStream inputStream = connection.getInputStream();
                        //使用工厂把网络的输入流生产Bitmap
                        Bitmap bitmap = BitmapFactory.decodeStream(inputStream);
                        //利用Message把图片发给Handler
                        Message msg = Message.obtain();
                        msg.obj = bitmap;
                        msg.what = GET_DATA_SUCCESS;
                        handler.sendMessage(msg);
                        inputStream.close();
                }else {
                        //服务启发生错误
                        handler.sendEmptyMessage(SERVER_ERROR);
                    }
                } catch (IOException e) {
                    e.printStackTrace();
                    //网络连接错误
                    handler.sendEmptyMessage(NETWORK_ERROR);
                }
            }
        }.start();
    }

} 
```
|  部件名称   | Activity_details |
|  ----  | ----  |
| 所属子系统  |商城|
| 部件调用者| 商城界面 |
|被调用者| 无 |
|入口参数| ` Intent intent=getIntent(); position=intent.getIntExtra("postion",0);` |
|返回值| 无 |

###部件截图
![avatar](https://github.com/daxuliu/markdown/raw/master/详情.png)
###部件页面代码：
```xml
<?xml version="1.0" encoding="utf-8"?>
<android.support.constraint.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".Activity_details"
    >


<LinearLayout
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">
    <com.hjq.bar.TitleBar
        android:id="@+id/toolbar"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="0dp"
        app:title="收藏"
        app:leftTitle="返回"
        app:rightColor="#ffffff"
        app:rightTitle="易入"
        app:titleColor="#ffffff"
        app:leftColor="#ffffff"


        /><com.example.ebarter.tools.MyImageView
    android:id="@+id/detailpic"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:src="@drawable/banner"/>
<TextView
    android:layout_gravity="center"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="崂山可乐"
    android:textSize="18sp"
    android:id="@+id/tvofhuowu"/>


    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content">
        <TextView
            android:layout_gravity="center"
            android:layout_width="132dp"
            android:layout_height="match_parent"
            android:text="1 巴特"
            android:textSize="15sp"
            android:id="@+id/price"
            android:textColor="#ff0000"/>
        <TextView
            android:layout_gravity="center"
            android:layout_width="132dp"
            android:layout_height="match_parent"
            android:text="数量: 0"
            android:id="@+id/number"
            android:textSize="15sp"
            android:textColor="#ff0000"/>
        <ImageView
            android:src="@drawable/ic2"
            android:layout_width="66dp"
            android:layout_height="66dp" />
    </LinearLayout>
<TextView
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:id="@+id/intorduce"
    android:text="详情介绍:\n1953年，青岛在国家政府的支持下组织科技人员开发了中国第一种碳酸饮料——崂山可乐。\n由于独特的配方和口感，以崂山可乐为主的崂山品牌\n饮料在此后的几十年中畅销华夏大地。"/>
</LinearLayout>




</android.support.constraint.ConstraintLayout>
```
###部件逻辑代码
```java
package com.example.ebarter;

import android.content.Intent;
import android.os.Handler;
import android.os.Message;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.TextView;
import android.widget.Toast;

import com.example.ebarter.tools.MyImageView;
import com.example.ebarter.tools.Product;
import com.hjq.bar.OnTitleBarListener;
import com.hjq.bar.TitleBar;

import org.json.JSONObject;

import java.util.ArrayList;

public class Activity_details extends AppCompatActivity {
    private TitleBar mTitleBar;
    private TextView textView;
    private int position;
    private android.support.v7.app.ActionBar actionBar;
    private ArrayList<Product> products;
    private Product orderpro;
    private Handler handler_favorite;

    {
        handler_favorite = new Handler() {
            @Override
            public void handleMessage(Message msg) {
                super.handleMessage(msg);
                switch (msg.what) {
                    case 0:
                        String re;
                        //status = response.substring((response.indexOf(":")+3) , (response.indexOf(",")-1));
                        try {
                            JSONObject jb = new JSONObject((String) msg.obj);
                            re = jb.getString("result");
                            if (re.equals("0")) {
                                //sessionId = response.substring((response.indexOf("sessionId")+13) , (response.indexOf(",",response.indexOf("sessionId"))-1));
                                Toast toast_status = Toast.makeText(Activity_details.this, "收藏成功！", Toast.LENGTH_LONG);
                                toast_status.show();
                            } else {
                                Toast toast_status = Toast.makeText(Activity_details.this, "已经收藏过该商品！", Toast.LENGTH_LONG);
                                toast_status.show();
                            }
                        } catch (Exception e) {
                        }


                        break;
                    default:
                        break;

                }
            }
        };
    }

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_details);
        actionBar = getSupportActionBar();
        actionBar.hide();//隐藏标题栏
        mTitleBar = (TitleBar) findViewById(R.id.toolbar);
        mTitleBar.setBackgroundColor(0xffee3333);
        //=new ArrayList();
        DataManager dataManager = DataManager.getInstance();
        Intent intent = getIntent();
        position = intent.getIntExtra("postion", 0);
        products = (ArrayList<Product>) dataManager.getInfoMap().get("realpro");
        orderpro = products.get(position);
        String price;
        price = products.get(position).getPrice();
        String name = products.get(position).getName();
        String pic = products.get(position).getPic();
        String orderid = products.get(position).getOrderid();
        orderid = orderid.replace(":", "-");
        String img = "https://s3.cn-north-1.amazonaws.com.cn/linda-trades-archive-1/";
        //  textView=(TextView)findViewById(R.id.tv);
        MyImageView itemIv = (MyImageView) findViewById(R.id.detailpic);
        itemIv.setImageURL(img + orderid + ".jpg");
        TextView pri = (TextView) findViewById(R.id.price);
        pri.setText(price);
        TextView tvname = (TextView) findViewById(R.id.tvofhuowu);
        tvname.setText(name);
        TextView intorduce = (TextView) findViewById(R.id.intorduce);
        intorduce.setText(products.get(position).getM_extraDescription());
        mTitleBar.setOnTitleBarListener(new OnTitleBarListener() {

            @Override
            public void onLeftClick(View v) {
                // textView.setText("left");
                startActivity(new Intent(Activity_details.this, MainActivity.class));
            }

            @Override
            public void onTitleClick(View v) {
                //textView.setText("title");
                sendRequestWithHttpClientfavorite();
            }

            @Override
            public void onRightClick(View v) {
                //textView.setText("right");
                Intent order = new Intent(Activity_details.this, OrderActivity.class);
                order.putExtra("position", position);
                startActivity(order);
            }

        });
    }

    private void sendRequestWithHttpClientfavorite() {
        new Thread(new Runnable() {
            @Override
            public void run() {
                try {
                    JSONObject jb;//= new JSONObject(responseinfo);
                    //   String token=jb.getJSONObject("user").getString("Token");
                    DataManager dataManager = DataManager.getInstance();
                    jb = (JSONObject) dataManager.getInfoMap().get("inforjb");
                    String string_uid = "" + jb.getInt("m_uId");
                    String string_fid = products.get(position).getPid();
                    //string_pwd = okhttptest.md5Decode32(string_pwd);
                    String url = "http://ebarter-env.cn-north-1.eb.amazonaws.com.cn/JSONServlet";
                    String json = "{\"userID\":" +
                            "\"" +
                            "" +
                            string_uid +
                            "\"," +
                            "\"type\":\"AddebtUserFavorite\",\"content\":\"\"," +
                            "\"favoriteID\":" +
                            "\"" +
                            string_fid +
                            "\"," +
                            "\"favoriteType\":\"p\"}";
                    Message message = new Message();
                    Okhttptest okhttptest = new Okhttptest();
                    message.what = 0;
                    message.obj = okhttptest.Favorite(url, json);
                    handler_favorite.sendMessage(message);
                } catch (Exception e) {
                    // TODO Auto-generated catch block
                    e.printStackTrace();
                }
            }
        }).start();//这个start()方法不要忘记了
    }


}
  
```

|  部件名称   | Okhttptest |
|  ----  | ----  |
| 所属子系统  | 无 |
| 部件调用者| 有网络请求的部件 |
|被调用者| 无 |
|入口参数| `String json;` |
|返回值| `String response;`|
###部件代码
```java
package com.example.ebarter;

import java.io.IOException;
import java.io.UnsupportedEncodingException;
import java.security.MessageDigest;
import java.security.NoSuchAlgorithmException;

import okhttp3.FormBody;
import okhttp3.MediaType;
import okhttp3.OkHttpClient;
import okhttp3.Request;
import okhttp3.RequestBody;
import okhttp3.Response;

public class Okhttptest {
    public static final MediaType JSON = MediaType.get("application/json; charset=utf-8");

    public static void main(String[] args) {
        // public static final MediaType JSON = MediaType.get("application/json; charset=utf-8");

        String url = "http://ebarter-env.cn-north-1.eb.amazonaws.com.cn/JSONServlet";
        String json = "{'DOB': ''," +
                " 'm_acct': 'myadmintest', " +   //username
                "'m_yearsOfBusiness': 0," +
                " 'm_phoneNum': '13062530530'," +  //tel
                " 'm_referenceCode': '26358', " +
                "'description': '', " +
                "'m_appName': 'ebartercny', " +
                "'forRcloud': True," +
                " 'topLevel': -150," +
                " 'm_storeName': '李斌43'," +
                " 'm_registered': {'m_contactPhone': '13062530530', 'm_address': '家园中路', 'm_city': '南京市', 'm_firstName': 'lb', 'm_longitude': 118.82127335896413, 'm_latitude': 31.857023885105992}, " +
                "'RoleName': 'hxgnyStudent'," +
                " 'm_lindaPoints': 0," +
                " 'm_acctType': 'SUPPLIER'," +
                " 'm_businessTypes': []," +
                " 'm_status': 'APPLY'," +
                " 'listofNewBType': [{'m_displayName': '餐饮娱乐', 'm_typeLabel': 'CateringEntertainmen'}, {'m_displayName': '电脑办公', 'm_typeLabel': 'Computeroffice'}, {'m_displayName': '手机数码', 'm_typeLabel': 'Mobiledigital'}, {'m_displayName': '广告印刷', 'm_typeLabel': 'Advertisingprinting'}], " +
                "'m_acctStatus': 'ACTIVATED'," +
                " 'm_email': '999@163.com', " +
                "'m_languageIndex': 1, " +
                "'m_platform': 'BAIDU', " +
                "'m_password': 'e10adc3949ba59abbe56e057f20f883e'}";
        Okhttptest test = new Okhttptest();
        //  System.out.println("12");
        try {
            System.out.println(test.postreg(url, json));
            //  System.out.println(json);
        } catch (IOException e) {

        }
//return  0;
    }

    //用户模块
    //注册接口
    String postreg(String url, String json) throws IOException {
        // RequestBody body = RequestBody.create(JSON, json);多余的

        RequestBody formBody;
        FormBody.Builder builder = new FormBody.Builder();
        builder.add("CTAG", "settings.LogonRegistration");
        builder.add("SCOBJ", json);
        formBody = builder.build();
        OkHttpClient client = new OkHttpClient();
        Request request = new Request.Builder()

                .url(url)
                .post(formBody)
                .build();
        try (Response response = client.newCall(request).execute()) {
            return response.body().string();
        }
    }

    //登录接口
    String Login(String url, String json) throws IOException {
        RequestBody body = RequestBody.create(JSON, json);
        RequestBody formBody;
        FormBody.Builder builder = new FormBody.Builder();
        builder.add("CTAG", "settings.LogonMsg");
        builder.add("SCOBJ", json);
        formBody = builder.build();
        OkHttpClient client = new OkHttpClient();
        Request request = new Request.Builder()

                .url(url)
                .post(formBody)
                .build();
        try (Response response = client.newCall(request).execute()) {
            return response.body().string();
        }
    }

    //忘记密码
    String Findpwd(String url, String json) throws IOException {
        RequestBody body = RequestBody.create(JSON, json);
        RequestBody formBody;
        FormBody.Builder builder = new FormBody.Builder();
        builder.add("CTAG", "settings.ResetPwd");
        builder.add("SCOBJ", json);
        formBody = builder.build();
        OkHttpClient client = new OkHttpClient();
        Request request = new Request.Builder()
                .url(url)
                .post(formBody)
                .build();
        try (Response response = client.newCall(request).execute()) {
            return response.body().string();
        }
    }

    //个人信息
    String Getinfor(String url, String json) throws IOException {
        RequestBody body = RequestBody.create(JSON, json);
        RequestBody formBody;
        FormBody.Builder builder = new FormBody.Builder();
        builder.add("CTAG", "settings.LogonRegistration");
        builder.add("SCOBJ", json);
        formBody = builder.build();
        OkHttpClient client = new OkHttpClient();
        Request request = new Request.Builder()

                .url(url)
                .post(formBody)
                .build();
        try (Response response = client.newCall(request).execute()) {
            return response.body().string();
        }
    }

    //查询好友-联系人
    String Contact(String url, String json) throws IOException {
        RequestBody body = RequestBody.create(JSON, json);
        RequestBody formBody;
        FormBody.Builder builder = new FormBody.Builder();
        builder.add("CTAG", "settings.Contact");
        builder.add("SCOBJ", json);
        formBody = builder.build();
        OkHttpClient client = new OkHttpClient();
        Request request = new Request.Builder()

                .url(url)
                .post(formBody)
                .build();
        try (Response response = client.newCall(request).execute()) {
            return response.body().string();
        }
    }

    //保存推送信息接口
    String PushRegId(String url, String json) throws IOException {
        RequestBody body = RequestBody.create(JSON, json);
        RequestBody formBody;
        FormBody.Builder builder = new FormBody.Builder();
        builder.add("CTAG", "settings.PushRegId");
        builder.add("SCOBJ", json);
        formBody = builder.build();
        OkHttpClient client = new OkHttpClient();
        Request request = new Request.Builder()

                .url(url)
                .post(formBody)
                .build();
        try (Response response = client.newCall(request).execute()) {
            return response.body().string();
        }
    }

    //根据用户名获取昵称
    String User(String url, String json) throws IOException {
        RequestBody body = RequestBody.create(JSON, json);
        RequestBody formBody;
        FormBody.Builder builder = new FormBody.Builder();
        builder.add("CTAG", "settings.User");
        builder.add("SCOBJ", json);
        formBody = builder.build();
        OkHttpClient client = new OkHttpClient();
        Request request = new Request.Builder()

                .url(url)
                .post(formBody)
                .build();
        try (Response response = client.newCall(request).execute()) {
            return response.body().string();
        }
    }

    //交易模块
    //查商品列表/需求列表
    String Productlist(String url, String json) throws IOException {
        RequestBody body = RequestBody.create(JSON, json);
        RequestBody formBody;
        FormBody.Builder builder = new FormBody.Builder();
        builder.add("CTAG", "settings.Product");
        builder.add("SCOBJ", json);
        formBody = builder.build();
        OkHttpClient client = new OkHttpClient();
        Request request = new Request.Builder()

                .url(url)
                .post(formBody)
                .build();
        try (Response response = client.newCall(request).execute()) {
            return response.body().string();
        }
    }

    //查询用户巴特币余额
    String EbarterAcct(String url, String json) throws IOException {
        RequestBody body = RequestBody.create(JSON, json);
        RequestBody formBody;
        FormBody.Builder builder = new FormBody.Builder();
        builder.add("CTAG", "settings.EbarterAcct");
        builder.add("SCOBJ", json);
        formBody = builder.build();
        OkHttpClient client = new OkHttpClient();
        Request request = new Request.Builder()

                .url(url)
                .post(formBody)
                .build();
        try (Response response = client.newCall(request).execute()) {
            return response.body().string();
        }
    }

    //查询流水
    String Root(String url, String json) throws IOException {
        RequestBody body = RequestBody.create(JSON, json);
        RequestBody formBody;
        FormBody.Builder builder = new FormBody.Builder();
        builder.add("CTAG", "settings.root");
        builder.add("SCOBJ", json);
        formBody = builder.build();
        OkHttpClient client = new OkHttpClient();
        Request request = new Request.Builder()

                .url(url)
                .post(formBody)
                .build();
        try (Response response = client.newCall(request).execute()) {
            return response.body().string();
        }
    }

    //获取店铺信息
    String Store(String url, String json) throws IOException {
        RequestBody body = RequestBody.create(JSON, json);
        RequestBody formBody;
        FormBody.Builder builder = new FormBody.Builder();
        builder.add("CTAG", "settings.User");
        builder.add("SCOBJ", json);
        formBody = builder.build();
        OkHttpClient client = new OkHttpClient();
        Request request = new Request.Builder()

                .url(url)
                .post(formBody)
                .build();
        try (Response response = client.newCall(request).execute()) {
            return response.body().string();
        }
    }

    //获取商品详情
    String Product(String url, String json) throws IOException {
        RequestBody body = RequestBody.create(JSON, json);
        RequestBody formBody;
        FormBody.Builder builder = new FormBody.Builder();
        builder.add("CTAG", "settings.Product");
        builder.add("SCOBJ", json);
        formBody = builder.build();
        OkHttpClient client = new OkHttpClient();
        Request request = new Request.Builder()

                .url(url)
                .post(formBody)
                .build();
        try (Response response = client.newCall(request).execute()) {
            return response.body().string();
        }
    }

    //查询收藏列表
    String Favoritelist(String url, String json) throws IOException {
        RequestBody body = RequestBody.create(JSON, json);
        RequestBody formBody;
        FormBody.Builder builder = new FormBody.Builder();
        builder.add("CTAG", "settings.Favorite");
        builder.add("SCOBJ", json);
        formBody = builder.build();
        OkHttpClient client = new OkHttpClient();
        Request request = new Request.Builder()

                .url(url)
                .post(formBody)
                .build();
        try (Response response = client.newCall(request).execute()) {
            return response.body().string();
        }
    }

    //收藏商品
    String Favorite(String url, String json) throws IOException {
        RequestBody body = RequestBody.create(JSON, json);
        RequestBody formBody;
        FormBody.Builder builder = new FormBody.Builder();
        builder.add("CTAG", "settings.Favorite");
        builder.add("SCOBJ", json);
        formBody = builder.build();
        OkHttpClient client = new OkHttpClient();
        Request request = new Request.Builder()

                .url(url)
                .post(formBody)
                .build();
        try (Response response = client.newCall(request).execute()) {
            return response.body().string();
        }
    }

    //获取服务器时间
    String TimeRequest(String url, String json) throws IOException {
        RequestBody body = RequestBody.create(JSON, json);
        RequestBody formBody;
        FormBody.Builder builder = new FormBody.Builder();
        builder.add("CTAG", "settings.TimeRequest");
        builder.add("SCOBJ", json);
        formBody = builder.build();
        OkHttpClient client = new OkHttpClient();
        Request request = new Request.Builder()

                .url(url)
                .post(formBody)
                .build();
        try (Response response = client.newCall(request).execute()) {
            return response.body().string();
        }
    }

    //提交订单
    String EbarterOrder(String url, String json) throws IOException {
        RequestBody body = RequestBody.create(JSON, json);
        RequestBody formBody;
        FormBody.Builder builder = new FormBody.Builder();
        builder.add("CTAG", "settings.EbarterOrder");
        builder.add("SCOBJ", json);
        formBody = builder.build();
        OkHttpClient client = new OkHttpClient();
        Request request = new Request.Builder()

                .url(url)
                .post(formBody)
                .build();
        try (Response response = client.newCall(request).execute()) {
            return response.body().string();
        }
    }

    //银联支付
    String Unionpay(String url, String json) throws IOException {
        RequestBody body = RequestBody.create(JSON, json);
        RequestBody formBody;
        FormBody.Builder builder = new FormBody.Builder();
        builder.add("CTAG", "settings.Unionpay");
        builder.add("SCOBJ", json);
        formBody = builder.build();
        OkHttpClient client = new OkHttpClient();
        Request request = new Request.Builder()

                .url(url)
                .post(formBody)
                .build();
        try (Response response = client.newCall(request).execute()) {
            return response.body().string();
        }
    }

    /**
     * 32位MD5加密
     *
     * @param content -- 待加密内容
     * @return
     */
    public String md5Decode32(String content) {
        byte[] hash;
        try {
            hash = MessageDigest.getInstance("MD5").digest(content.getBytes("UTF-8"));
        } catch (NoSuchAlgorithmException e) {
            throw new RuntimeException("NoSuchAlgorithmException", e);
        } catch (UnsupportedEncodingException e) {
            throw new RuntimeException("UnsupportedEncodingException", e);
        }
        //对生成的16字节数组进行补零操作
        StringBuilder hex = new StringBuilder(hash.length * 2);
        for (byte b : hash) {
            if ((b & 0xFF) < 0x10) {
                hex.append("0");
            }
            hex.append(Integer.toHexString(b & 0xFF));
        }
        return hex.toString();
    }


}

```



|  部件名称   |  chatlist |
|  ----  | ----  |
| 所属子系统  | 无 |
| 部件调用者| 主界面 |
|被调用者| `` |
|入口参数| `userToken` |
|返回值| 无 |
![avatar](对话列表.png) 

### 部件页面代码：

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:id="@+id/chatlist"
    tools:context=".chatlist">
    <fragment
        android:id="@+id/conversationlist"
        android:name="io.rong.imkit.fragment.ConversationListFragment"
        android:layout_width="match_parent"
        android:layout_height="400dp" />
    <LinearLayout
        android:id="@+id/content"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:orientation="vertical">

    </LinearLayout>
    <android.support.design.widget.BottomNavigationView
        android:id="@+id/navigation"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginEnd="0dp"
        android:layout_marginStart="0dp"
        android:background="?android:attr/windowBackground"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:menu="@menu/navigation"
        android:layout_alignParentBottom="true"/>




</LinearLayout>
```



### 部件逻辑代码

```java
package com.example.ebarter;

import android.content.Intent;
import android.net.Uri;
import android.support.annotation.NonNull;
import android.support.design.widget.BottomNavigationView;
import android.support.v4.app.FragmentManager;
import android.support.v4.app.FragmentTransaction;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.util.Log;
import android.view.MenuItem;

import org.json.JSONObject;

import io.rong.imkit.RongIM;
import io.rong.imkit.fragment.ConversationListFragment;
import io.rong.imlib.IRongCallback;
import io.rong.imlib.RongIMClient;
import io.rong.imlib.model.Conversation;
import io.rong.imlib.model.Message;
import io.rong.message.TextMessage;

public class chatlist extends AppCompatActivity {
    private android.support.v7.app.ActionBar actionBar;
    private BottomNavigationView.OnNavigationItemSelectedListener mOnNavigationItemSelectedListener
            = new BottomNavigationView.OnNavigationItemSelectedListener() {

        @Override
        public boolean onNavigationItemSelected(@NonNull MenuItem item) {
            switch (item.getItemId()) {
                case R.id.navigation_home:
                    //mTextMessage.setText(R.string.title_home);

                    return true;
                case R.id.navigation_dashboard:
                    //mTextMessage.setText(R.string.title_dashboard);
                    Intent intent2 = new Intent(chatlist.this, Group.class);
                    startActivity(intent2);
                    return true;
                case R.id.navigation_notifications:
                    //mTextMessage.setText(R.string.title_notifications);
                    Intent intent3 = new Intent(chatlist.this, MeActivity.class);
                    startActivity(intent3);

                    return true;
                case R.id.discover:
                    Intent intent = new Intent(chatlist.this, MainActivity.class);
                    startActivity(intent);
                    return true;
            }
            return false;
        }
    };

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_chatlist);


        actionBar = getSupportActionBar();
        actionBar.hide();//隐藏

        BottomNavigationView navigation = (BottomNavigationView) findViewById(R.id.navigation);
        navigation.setSelectedItemId(R.id.navigation_home);
        navigation.setOnNavigationItemSelectedListener(mOnNavigationItemSelectedListener);
        String token = "6uyWGOVHVRUw0QbNGv78USlrkXht8AaSYxhqbN9FijL6GK7fKByvsOpryCchGC1wRApBwpQfEEAOhmrzQoShnBFWMh4NyRMgouEFDphLdfE=";

        Intent intent = getIntent();
        //  String userToken = intent.getStringExtra("token");
        String userToken = "";
        DataManager dataManager = DataManager.getInstance();
        JSONObject jb = (JSONObject) dataManager.getInfoMap().get("inforjb");
        try {
            userToken = jb.getJSONObject("user").getString("Token");

        } catch (Exception e) {
            Intent intent2 = new Intent(chatlist.this, LoginActivity.class);
            startActivity(intent2);
        }

        // 连接 IM
        Log.d("TAG", "连接融云--onSuccess" + userToken);
        RongIM.connect(userToken, new RongIMClient.ConnectCallback() {
            @Override
            public void onTokenIncorrect() {

            }

            @Override
            public void onSuccess(String s) {
                Log.d("TAG", "连接融云--onSuccess" + s);
               /* ConversationListFragment conversationListFragment = new ConversationListFragment();
                Uri uri = Uri.parse("rong://" + getApplicationInfo().packageName).buildUpon()
                        .appendPath("conversationlist")
                        .appendQueryParameter(Conversation.ConversationType.PRIVATE.getName(), "false")
                        .appendQueryParameter(Conversation.ConversationType.GROUP.getName(), "false")
                        .appendQueryParameter(Conversation.ConversationType.PUBLIC_SERVICE.getName(), "false")
                        .appendQueryParameter(Conversation.ConversationType.APP_PUBLIC_SERVICE.getName(), "false")
                        .appendQueryParameter(Conversation.ConversationType.SYSTEM.getName(), "true")
                        .build();
                conversationListFragment.setUri(uri);

                FragmentManager fragmentManager = getSupportFragmentManager();
                FragmentTransaction transaction = fragmentManager.beginTransaction();
                transaction.add(R.id.chatlist, conversationListFragment);
                transaction.commit();*/
                FragmentManager fragmentManage = getSupportFragmentManager();
                ConversationListFragment fragement = (ConversationListFragment) fragmentManage.findFragmentById(R.id.conversationlist);
                Uri uri = Uri.parse("rong://" + getApplicationInfo().packageName).buildUpon()
                        .appendPath("conversationlist")
                        .appendQueryParameter(Conversation.ConversationType.PRIVATE.getName(), "false")
                        .appendQueryParameter(Conversation.ConversationType.GROUP.getName(), "false")
                        .appendQueryParameter(Conversation.ConversationType.PUBLIC_SERVICE.getName(), "false")
                        .appendQueryParameter(Conversation.ConversationType.APP_PUBLIC_SERVICE.getName(), "false")
                        .appendQueryParameter(Conversation.ConversationType.SYSTEM.getName(), "true")
                        .build();
                fragement.setUri(uri);


            }

            @Override
            public void onError(RongIMClient.ErrorCode errorCode) {

            }
        });
       /* RongIMClient.connect(token, new RongIMClient.ConnectCallback() {
            @Override
            public void onTokenIncorrect() {

            }


            @Override
            public void onSuccess(String userid) {
                Log.d("TAG", "连接融云--onSuccess" + userid);
                // sendandRecive=new SendandRecive();
                //receive();
                //send(sendandRecive.getSend(),sendandRecive.getTargetid());
                //send();
                // receive();
               TextMessage textMessage = TextMessage.obtain("fuck!to fucker1234");

                RongIMClient.getInstance().sendMessage(Conversation.ConversationType.PRIVATE,"26519#_chatfucker1", textMessage, null, null, new IRongCallback.ISendMessageCallback() {
                    @Override
                    public void onAttached(Message message) {
                        // 消息成功存到本地数据库的回调
                    }

                    @Override
                    public void onSuccess(Message message) {
                        // 消息发送成功的回调
                        Log.d("TAG", "发送成功--onSuccess" +message.toString());
                    }

                    @Override
                    public void onError(Message message, RongIMClient.ErrorCode errorCode) {
                        // 消息发送失败的回调
                        Log.d("TAG", "发送失败--"+errorCode.toString() );
                    }
                });


            }


            @Override
            public void onError(RongIMClient.ErrorCode errorCode) {

            }
        });*/
    }
}

```

|  部件名称   |  DataManager |
|  ----  | ----  |
| 所属子系统  | 无 |
| 部件调用者| 所有界面 |
|被调用者| 无 |
|入口参数| `String key;` |
|返回值| `Object`|
###部件代码
```java
package com.example.ebarter;

import java.util.HashMap;

public class DataManager {

    private static volatile DataManager INSTANCE;

    private HashMap<String, Object> infoMap = new HashMap<String, Object>();

    private DataManager() {
    }

    public static DataManager getInstance() {
        if (INSTANCE == null) {
            synchronized (DataManager.class) {
                if (INSTANCE == null) {
                    INSTANCE = new DataManager();
                }
            }
        }
        return INSTANCE;
    }

    public HashMap<String, Object> getInfoMap() {
        return infoMap;
    }

}

```



|  部件名称   |  S3 |
|  ----  | ----  |
| 所属子系统  | 个人信息 |
| 部件调用者| 个人信息界面 |
|被调用者| 无 |
|入口参数| `Object` |
|返回值| `无`|

###部件代码

```java
package com.example.ebarter.nets3;

import android.content.Context;
import android.graphics.Bitmap;
import android.graphics.BitmapFactory;
import android.os.AsyncTask;
import android.util.Log;

import com.amazonaws.AmazonClientException;
import com.amazonaws.AmazonServiceException;
import com.amazonaws.HttpMethod;
import com.amazonaws.auth.AWSCredentials;
import com.amazonaws.regions.Region;
import com.amazonaws.regions.Regions;
import com.amazonaws.regions.ServiceAbbreviations;
import com.amazonaws.services.s3.AmazonS3;
import com.amazonaws.services.s3.AmazonS3Client;
import com.amazonaws.services.s3.model.CannedAccessControlList;
import com.amazonaws.services.s3.model.GeneratePresignedUrlRequest;
import com.amazonaws.services.s3.model.GetObjectRequest;
import com.amazonaws.services.s3.model.PutObjectRequest;
import com.amazonaws.services.s3.model.S3Object;
import com.google.gson.JsonObject;
//import com.yuli.chexian.R;
//import com.yuli.chexian.util.FileUtil;
//import com.yuli.chexian.util.L;
//import com.yuli.chexian.util.MUtils;
//import com.yuli.chexian.util.MyApplication;
//import com.yuli.chexian.util.PictureUtil;
//import com.yuli.chexian.util.TimeUtil;

import java.io.BufferedReader;
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.InputStream;
import java.io.InputStreamReader;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.io.Writer;
import java.net.URL;
import java.util.HashMap;
import java.util.zip.GZIPInputStream;
import java.util.zip.GZIPOutputStream;

import io.rong.common.FileUtils;

import static com.example.ebarter.nets3.S3.TARGET.ZH;


/**
 * Created by tyrant on 2/3/2015.
 */
public class S3 {
    public static boolean USE_NEW_IMG = true;
    //    private static String URL_POST_US = ".s3-website-us-west-2.amazonaws.com/";
//    private static String URL_POST_CN = ".s3-website.cn-north-1.amazonaws.com.cn/";
    public static String UPLOAD_BUCKET = "linda-trades-archive-1";
    public static final String PIC_BUCKET = "linda-trades-archive-1";

    public enum TARGET {US, TW, ZH}

    ;
    private static final HashMap<TARGET, S3Info> IMG_RULS = new HashMap<TARGET, S3Info>();

    //  public enum TARGET {US, TW, ZH}
    static {
        IMG_RULS.put(ZH, new S3Info("linda-zh"));
    }

    public static final int MEGA_SIZE = 1024 * 1024;
    public static final int FILE_LMT = 3; // cannot be more than 2 mb, or we will get outofmemory error
    public static final Region REGION_US = Region.getRegion(Regions.US_EAST_1);
    public static final Region REGION_CN = Region.getRegion(Regions.CN_NORTH_1);
    public static final String SC_AD_PIC = "ad-pic";
    public static String BUCKET_NAME = "linda-trades";
    public static final String TRADE_BUCKET = "linda-trades";
    public static final String TRADE_BUCKET_ARCHIVE = "linda-trades-archive-1";
    public static final String TAG = "S3";

    private static String[] EndPoints = new String[]{"s3.amazonaws.com",
            "s3-external-1.amazonaws.com", "s3-us-west-2.amazonaws.com",
            "s3-us-west-1.amazonaws.com", "s3-eu-west-1.amazonaws.com",
            "s3-ap-southeast-1.amazonaws.com",
            "s3-ap-southeast-2.amazonaws.com",
            "s3-ap-northeast-1.amazonaws.com", "s3-sa-east-1.amazonaws.com"};

    private static S3 INSTANCE;

    private AWSCredentials m_awsCredential;

    public static S3 getINSTANCE() {
        if (INSTANCE == null) {
            INSTANCE = new S3();
        }

        return INSTANCE;
    }

    private S3() {
    }

//    public static String getImgUrl(MyApplication.TARGET target) {
//        return IMG_RULS.get(target).getHtmlUrl();
//    }

    public static String getImgBucket(TARGET target) {
        return IMG_RULS.get(target).m_bucket;
    }

    public String getBucketName() {
        // wkq LindaApplication.TARGET.TW to LindaApplication.TARGET.ZH
        return USE_NEW_IMG ? getImgBucket(TARGET.ZH) : BUCKET_NAME == null ? "linda-operation" : BUCKET_NAME;
    }

    public void setAwsData(final String accessKey, final String secretKey) {
        if (accessKey != null && secretKey != null) {
            m_awsCredential = new AWSCredentials() {
                @Override
                public String getAWSSecretKey() {
                    return secretKey;
                }

                @Override
                public String getAWSAccessKeyId() {
                    return accessKey;
                }
            };
        }
    }

    // upload a file(not image file to AWS)
    public void newUploadFile(final String fileName, final File localFile, final S3PostActionAdapter s3PostAction) {
        if (m_awsCredential == null) {
            s3PostAction.notifyError("failed upload file " + fileName);
            return;
        }

        if (localFile == null) {
            Log.i(TAG, "Uploading a new file " + fileName + " failed at compression");
            return;
        }

        // limit file size
        double megaBytes = (localFile.length() / MEGA_SIZE);
        if (megaBytes > FILE_LMT) {
            String err = "Uploading a new file " + fileName + (megaBytes == 0 ? "0 size  " : " size too big ") + megaBytes + " rejected";
            System.out.println(err);
            if (s3PostAction != null) {
                s3PostAction.notifyError(err);
            }

            return;
        }

        AsyncTask uploadTask = new AsyncTask() {
            @Override
            protected Object doInBackground(Object... arg0) {
                try {
                    AmazonS3 s3 = createS3();
                    String bucketName = UPLOAD_BUCKET;
                    // to make it public readable .withCannedAcl(CannedAccessControlList.PublicRead)
                    s3.putObject(new PutObjectRequest(bucketName, fileName, localFile).withCannedAcl(CannedAccessControlList.PublicRead));
                    if (s3PostAction != null) {
                        s3PostAction.uploadSucceed(fileName);
                    }
                } catch (Exception e) {
                    if (s3PostAction != null) {
                        s3PostAction.notifyError("failed upload file S3 AmazonServiceException " + e);
                        Log.i(TAG, "failed upload file S3 AmazonServiceException " + e);
                        //ErrorReportService.ReportErrorBackgroundThread(TAG, "failed upload file S3 AmazonServiceException " + e );
                    }
                }

                return null;
            }
        };

        uploadTask.execute();
    }

    //上传图片
    public void uploadFile(final Context context, final String fileName, final File file, final S3PostActionAdapter s3PostAction) {
        if (m_awsCredential == null) {
            s3PostAction.notifyError("failed upload file" + fileName);
            return;
        }


        final String pic_path = file.getPath();
        String targetPath = FileUtil.getDiskCacheDir(context) + "/" + ".jpg";
        //调用压缩图片的方法，返回压缩后的图片path
        final String compressImage = FileUtil.compressImage(pic_path, targetPath, 30);
        final File compressedPic = new File(compressImage);

        File usedFile = null;

        if (compressedPic.exists()) {
            usedFile = compressedPic;

            // L.e("图片压缩上传+compressImage");

        } else {//直接上传

            usedFile = file;
        }

        final File upFile = usedFile;

        if (upFile == null) {
            Log.i(TAG, "Uploading a new file " + fileName + " failed at compression");
            return;
        }
        // limit file size
        double megaBytes = (file.length() / MEGA_SIZE);

        if (megaBytes > FILE_LMT) {
            String err = "Uploading a new file " + fileName + " size too big " + megaBytes + " rejected";
            Log.d("test", "err");
//            System.out.println(err);
            if (s3PostAction != null) {
                s3PostAction.notifyError(err);
            }

            return;
        }


        AsyncTask uploadTask = new AsyncTask() {
            @Override
            protected Object doInBackground(Object... arg0) {
                try {
                    AmazonS3 s3 = createS3();
//                    String bucketName = getBucketName();
                    String bucketName = "linda-trades-archive-1";
                    // to make it public readable .withCannedAcl(CannedAccessControlList.PublicRead)
                    s3.putObject(new PutObjectRequest(bucketName, fileName, upFile).withCannedAcl(CannedAccessControlList.PublicRead));

                    if (s3PostAction != null) {
                        s3PostAction.uploadSucceed(bucketName + "/" + fileName);
                    }
                    // http://linda-tw.s3-website.cn-north-1.amazonaws.com.cn/%E5%8D%97%E4%BA%AC%E6%B5%8B%E8%AF%95:1475113284715:866926021704522.jpg
                } catch (Exception e) {
                    if (s3PostAction != null) {
                        s3PostAction.notifyError("failed upload file S3 AmazonServiceException " + e);
                        Log.i(TAG, "failed upload file S3 AmazonServiceException " + e);
                        //ErrorReportService.ReportErrorBackgroundThread(TAG, "failed upload file S3 AmazonServiceException " + e );
                    }
                }
                return null;
            }
        };
        uploadTask.execute();
    }

//   public static String getInternalAppBucket() {
//       L.e(TimeUtil.getMouthByEnglish());
//       return TimeUtil.getMouthByEnglish();
//    }

    public static String lodaDataFromS3Impl(String url) {
        try {
            BufferedReader in = new BufferedReader(new InputStreamReader((new URL(url)).openStream()));
            String line = null;

            StringBuilder sb = new StringBuilder();

            while ((line = in.readLine()) != null) {
                sb.append(line);
            }
            Log.d("sssssss", sb.toString());
            return sb.toString();
        } catch (Exception e) {
            System.out.println("Err " + e.getMessage());
        }

        return null;
    }

    public AmazonS3 createS3() {
        try {
            AmazonS3 s3 = new AmazonS3Client(m_awsCredential);
            Region usedRegion = REGION_CN;
            s3.setRegion(usedRegion);
            final String serviceEndpoint = usedRegion.getServiceEndpoint(ServiceAbbreviations.S3);
            s3.setEndpoint(serviceEndpoint);
            return s3;
        } catch (AmazonServiceException e) {
            System.out.println("S3 AmazonServiceException " + e);
            Log.d(TAG, "S3 AmazonServiceException " + e);
            //ErrorReportService.ReportErrorBackgroundThread(TAG, "S3 AmazonServiceException for " + bucketName + "\r\n" + e );
        } catch (AmazonClientException ace) {
            System.out.println("S3 AmazonServiceException " + ace);
            Log.d(TAG, "S3 AmazonServiceException " + ace);
            // ErrorReportService.ReportErrorBackgroundThread(TAG, "S3 AmazonServiceException for " + bucketName + "\r\n" + ace );
        } catch (Exception e) {
            Log.d(TAG, "S3 AmazonServiceException " + e);
        }

        return null;
    }

    public void downloadFile(final String bucketName, final String fileName, final S3PostActionAdapter postProcessor) {
        if (m_awsCredential == null) {
            postProcessor.notifyError("failed downloadFile file1 " + fileName);
            return;
        }

        AsyncTask downloadTask = new AsyncTask<Object, Void, byte[]>() {
            @Override
            protected byte[] doInBackground(Object... arg0) {
                S3Object downloadObject = null;
                try {
                    AmazonS3 s3 = createS3();
                    String bucketName = "linda-trades-archive-1";
                    downloadObject = s3.getObject(new GetObjectRequest(bucketName, fileName));
                    System.out.println("downloadFile a file " + fileName + " from " + bucketName);
                } catch (AmazonServiceException e) {
                    System.out.println("S3 AmazonServiceException " + e);
                    Log.d(TAG, "S3 AmazonServiceException " + e);
                    //ErrorReportService.ReportErrorBackgroundThread(TAG, "S3 AmazonServiceException for " + bucketName + "\r\n" + e );
                } catch (AmazonClientException ace) {
                    System.out.println("S3 AmazonServiceException " + ace);
                    Log.d(TAG, "S3 AmazonServiceException " + ace);
                    // ErrorReportService.ReportErrorBackgroundThread(TAG, "S3 AmazonServiceException for " + bucketName + "\r\n" + ace );
                } finally {
                    if (downloadObject != null) {
                        if (postProcessor != null) {

                            //   postProcessor.downloadSucceed(downloadObject.getObjectContent());
                            OutputStream outputStream = null;
                            try {
                                // FileOutputStream fos = new FileOutputStream(fileName);
                                // File file = new File(Environment.getExternalStorageDirectory(), fileName);
                                //  FileOutputStream fos = new FileOutputStream(file);
                                // file.deleteOnExit();

                                ByteArrayOutputStream out = new ByteArrayOutputStream();
                                //InputStream in = decompress(downloadObject.getObjectContent());
                                InputStream in = downloadObject.getObjectContent();
                                int bytesRead = 0;
                                byte[] buffer = new byte[1024];
                                while ((bytesRead = in.read(buffer)) > 0) {
                                    out.write(buffer, 0, bytesRead);
                                }
                                out.close();
                                return out.toByteArray();
                            } catch (IOException e) {
                                Log.d(TAG, e.toString());
                                //ErrorReportService.ReportErrorBackgroundThread(TAG, e.toString());
                            }
                        }
                        /*
                        try {
                          //  displayTextInputStream(downloadObject.getObjectContent());
                        } catch(IOException e) {
                            System.out.println("cannot display downloaded file ");
                        }
                        */
                    } else if (postProcessor != null) {
                        postProcessor.notifyError("downloadFile2 " + fileName + " failed");
                    }
                }

                return null;
            }

            @Override
            protected void onPostExecute(byte[] bytes) {


                if (bytes != null) {
                    if (postProcessor != null) {
                        try {
                            String m = new String(bytes);
                            postProcessor.downloadfilefromS3(m);
                            // System.out.println("655555"+m);
                            BitmapFactory.Options options = new BitmapFactory.Options();// Create object of bitmapfactory's option method for further option use
                            options.inPurgeable = true;
                            final Bitmap bitmap = BitmapFactory.decodeByteArray(bytes, 0, bytes.length, options);
                            //postProcessor.downloadSucceed(bitmap, fileName);
                        } catch (Exception e) {
                            Log.d(TAG, e.toString());
                            //ErrorReportService.ReportErrorBackgroundThread(TAG, e.toString());
                        }
                    }
                }
            }
        };

        downloadTask.execute();
    }

    public URL createPreAssignedURL(AmazonS3 s3, String bucketName, String fileName) {
        java.util.Date expiration = new java.util.Date();
        long msec = expiration.getTime();
        msec += 30 * 24 * 60 * 60 * 1000; // 30 days
        expiration.setTime(msec);

        GeneratePresignedUrlRequest generatePresignedUrlRequest = new GeneratePresignedUrlRequest(bucketName, fileName);
        generatePresignedUrlRequest.setMethod(HttpMethod.GET); // Default.
        generatePresignedUrlRequest.setExpiration(expiration);

        return s3.generatePresignedUrl(generatePresignedUrlRequest);
    }

    private static GZIPInputStream decompress(InputStream compressed) throws IOException {
        return new GZIPInputStream(compressed);
    }

    private File gzipFile(File sourceFile) {
        byte[] buffer = new byte[1024];
        try {
            File zip = File.createTempFile(sourceFile.getName(), ".zip");
            FileOutputStream fileOutputStream = new FileOutputStream(zip);
            GZIPOutputStream gzipOutputStream = new GZIPOutputStream(fileOutputStream);
            FileInputStream fileInput = new FileInputStream(sourceFile);
            int bytes_read;
            while ((bytes_read = fileInput.read(buffer)) > 0) {
                gzipOutputStream.write(buffer, 0, bytes_read);
            }
            fileInput.close();
            gzipOutputStream.finish();
            gzipOutputStream.close();
            System.out.println("------The file was compressed successfully!");

            return zip;
        } catch (IOException ex) {
            ex.printStackTrace();
        }

        return null;
    }

    public static File createSampleFile() throws IOException {
        File file = File.createTempFile("aws-java-sdk-", ".txt");
        file.deleteOnExit();

        Writer writer = new OutputStreamWriter(new FileOutputStream(file));
        writer.write("lindaTest\n");
        writer.close();

        return file;
    }

    //
//    /**
//     * Displays the contents of the specified input stream as text.
//     *
//     * @param input
//     *            The input stream to display as text.
//     *
//     * @throws IOException
//     */
    private static void displayTextInputStream(InputStream input) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(input));
        while (true) {
            String line = reader.readLine();
            if (line == null) break;

            System.out.println("    " + line);
        }
        System.out.println();
    }

    public static class AwsCredentialData {
        private final String m_accessKey;
        private final String m_secretKey;

        public AwsCredentialData(String accessKey, String secretKey) {
            m_accessKey = accessKey;
            m_secretKey = secretKey;
        }
    }

    public static class S3Info {
        public final String m_bucket;

        S3Info(String s) {
            m_bucket = s;
        }

//        String getHtmlUrl() {
//            return "http://" + m_bucket + (MyApplication.getInstance().useCnS3() ? URL_POST_CN : URL_POST_US);
//        }
    }
}

```

|  部件名称   |  Pay |
|  ----  | ----  |
| 所属子系统  | 支付模块 |
| 部件调用者| 订单 |
|被调用者| 无 |
|入口参数| `String tn` |
|返回值| `无`|

### 部件截图

![ava](https://github.com/daxuliu/markdown/raw/master/支付.png)

###部件逻辑代码

```java
package com.example.ebarter;

import android.content.Intent;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.LinearLayout;
import android.widget.Toast;

import com.unionpay.UPPayAssistEx;

import org.json.JSONException;
import org.json.JSONObject;

public class Pay extends AppCompatActivity {
    private LinearLayout Unionpay;
    private  String tn="";

    @Override
    protected void onActivityResult(int requestCode, int resultCode, Intent data) {
        /*************************************************
         * 步骤3：处理银联手机支付控件返回的支付结果
         ************************************************/
        if (data == null) {
            return;
        }

        String msg = "";
        /*
         * 支付控件返回字符串:success、fail、cancel 分别代表支付成功，支付失败，支付取消
         */
        String str = data.getExtras().getString("pay_result");
        if (str.equalsIgnoreCase("success")) {

            // 如果想对结果数据验签，可使用下面这段代码，但建议不验签，直接去商户后台查询交易结果
            // result_data结构见c）result_data参数说明
            if (data.hasExtra("result_data")) {
                String result = data.getExtras().getString("result_data");
                try {
                    JSONObject resultJson = null;
                    try {
                        resultJson = new JSONObject(result);
                    } catch (JSONException e) {
                        e.printStackTrace();
                    }
                    String sign = resultJson.getString("sign");
                    String dataOrg = resultJson.getString("data");
                    // 此处的verify建议送去商户后台做验签
                    // 如要放在手机端验，则代码必须支持更新证书
                    boolean ret = 1 == 1;//下面直接返回true了
                    if (ret) {
                        // 验签成功，显示支付结果
                        msg = "支付成功！";
                    } else {
                        // 验签失败
                        msg = "支付失败！";
                    }
                } catch (JSONException e) {
                }
            }
            // 结果result_data为成功时，去商户后台查询一下再展示成功
            msg = "支付成功！";
        } else if (str.equalsIgnoreCase("fail")) {
            msg = "支付失败！";
        } else if (str.equalsIgnoreCase("cancel")) {
            msg = "用户取消了支付";
        }


    }
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_liucheng);
        Unionpay=findViewById(R.id.unionpay);
        String servermode="01";
       // UPPayAssistEx.startPay( Pay.this,null,null,tn,servermode);
        Unionpay.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                if (UPPayAssistEx.checkWalletInstalled(Pay.this)) {
                    //当判断用户手机上已安装银联Apk，商户客户端可以做相应个性化处理
                    Toast toast = Toast.makeText(Pay.this, "请卸载云闪付！", Toast.LENGTH_SHORT);
                    toast.show();
                } else {
                    String servermode = "01";

                    UPPayAssistEx.startPay(Pay.this, null, null, tn, servermode);
                }
            }
        });
    }
}

```
|  部件名称   |  OrderActivity |
|  ----  | ----  |
| 所属子系统  | 支付模块 |
| 部件调用者| 订单 |
|被调用者| 无 |
|入口参数| `无` |
|返回值| `String tn`|
### 部件截图

![ava](https://github.com/daxuliu/markdown/raw/master/订单.png)



###逻辑代码

```java
package com.example.ebarter;

import android.content.DialogInterface;
import android.content.Intent;
import android.os.Bundle;
import android.os.Handler;
import android.os.Message;
import android.support.v7.app.ActionBar;
import android.support.v7.app.AlertDialog;
import android.support.v7.app.AppCompatActivity;
import android.text.SpannableString;
import android.util.Log;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;

import com.example.ebarter.tools.OrderTool;
import com.example.ebarter.tools.Product;
import com.hjq.bar.OnTitleBarListener;
import com.hjq.bar.TitleBar;

import org.json.JSONException;
import org.json.JSONObject;


import java.text.SimpleDateFormat;
import java.util.ArrayList;
import java.util.Calendar;
import java.util.Date;

import cn.smssdk.EventHandler;
import cn.smssdk.SMSSDK;

public class OrderActivity extends AppCompatActivity {

    private ActionBar actionBar;
    private TitleBar mTitleBar;

    private EditText eTxtusername;
    private EditText eTxttel;
    private EditText eTxtaddress;
    private EditText eTxtamount;
    private Product orderpro;

    private Okhttptest okhttptest;
    private ArrayList<Product> products;
    private String Orderjson;

    private Handler handler;

    {
        handler = new Handler() {
            @Override
            public void handleMessage(Message msg) {
                super.handleMessage(msg);
                switch (msg.what) {
                    case 0:
                        String response = (String) msg.obj;
                        try {
                            JSONObject order_jb = new JSONObject(response);
                            DataManager dataManager = DataManager.getInstance();
                            dataManager.getInfoMap().put("orderjb", order_jb);
                            dataManager.getInfoMap().put("orderjson", response);
                            Orderjson = response;
                            sendRequestWithHttpClientPay();
                            //Toast.makeText(OrderActivity.this, "订单提交成功！", Toast.LENGTH_LONG);
                            // Intent intent = new Intent(OrderActivity.this, Pay.class);
                            //startActivity(intent);
                            Log.d("order", response);
                        } catch (JSONException e) {
                        }
                    default:
                        break;
                }
            }
        };
    }

    private Handler handlerpay;

    {
        handlerpay = new Handler() {
            @Override
            public void handleMessage(Message msg) {
                super.handleMessage(msg);
                switch (msg.what) {
                    case 0:
                        String response = (String) msg.obj;
                        //try {
                        // JSONObject order_jb = new JSONObject(response);
                        DataManager dataManager = DataManager.getInstance();
                        // dataManager.getInfoMap().put("orderjb", order_jb);
                        // dataManager.getInfoMap().put("orderjson", response);
                        /// Toast.makeText(OrderActivity.this, "订单提交成功！", Toast.LENGTH_LONG);
                        Log.d("pay", "pay" + response);
                        Toast toast = Toast.makeText(OrderActivity.this, "response:" + response, Toast.LENGTH_SHORT);
                        toast.show();
                        Intent intent = new Intent(OrderActivity.this, Pay.class);
                        startActivity(intent);

                        //} catch (JSONException e) {
                        //}
                    default:
                        break;
                }
            }
        };
    }
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_order);
        actionBar = getSupportActionBar();
        actionBar.hide();
        mTitleBar = (TitleBar) findViewById(R.id.tb_order_title_bar);

        mTitleBar.setBackgroundColor(0xffcd3333);
        mTitleBar.setOnTitleBarListener(new OnTitleBarListener() {
            @Override
            public void onLeftClick(View v) {
                Intent i = new Intent(OrderActivity.this, MainActivity_shop.class);
                startActivity(i);
            }

            @Override
            public void onTitleClick(View v) {
                sendRequestWithHttpClient();
            }

            @Override
            public void onRightClick(View v) {

            }
        });
        okhttptest = new Okhttptest();
        eTxtusername = (EditText) findViewById(R.id.order_username);
        eTxtaddress = (EditText) findViewById(R.id.order_address);
        eTxttel = (EditText) findViewById(R.id.order_tel);
        eTxtamount = (EditText) findViewById(R.id.order_number);
        DataManager dataManager = DataManager.getInstance();
        Intent intent = getIntent();
        int position = intent.getIntExtra("postion", 0);
        products = (ArrayList<Product>) dataManager.getInfoMap().get("realpro");
        orderpro = products.get(position);
    }

    private void sendRequestWithHttpClient() {
        new Thread(new Runnable() {
            @Override
            public void run() {
                try {
                    String url = "http://ebarter-env.cn-north-1.eb.amazonaws.com.cn/JSONServlet";
                    DataManager dataManager = DataManager.getInstance();
                    JSONObject infor_jb = (JSONObject) dataManager.getInfoMap().get("inforjb");
                    JSONObject logon_jb = (JSONObject) dataManager.getInfoMap().get("log");
                    String toAcct = infor_jb.getString("m_acct") + "@";
                    ;  //买家账号
                    String amount = eTxtamount.getText().toString().replace("\n", "").replace(" ", "");  //数量
                    String m_suppid = "test:1572947018027:88EF6CAE-5670-42EB-87BA-0AD0478025E1:26509";
                    m_suppid = orderpro.getM_supplierOrderid();
                    String fromAcct = m_suppid.split(":")[0];  //卖家账号
                    String channel = "6";  //卖家 creditRate
                    String buyer_username = null;  //买家用户名
                    String seller_uid = m_suppid.split(":")[3];  //卖家uid
                    String clientip = seller_uid + "#" + fromAcct;  //卖家id 商品信息中 m_supplierOrderId 截取出来
                    String m_price = null;  // 订单价格 , 单价乘以数量
                    String m_supplierOrderId = m_suppid;  //商品信息中 m_supplierOrderId

                    String time = okhttptest.TimeRequest(url, "{}");
                    System.out.println(time);
                    JSONObject jb_EA = new JSONObject(time);
                    Object sertime = jb_EA.get("serverTime");
                    String server_time = sertime.toString();  //时间

                    String uuid = "88EF6CAE-5670-42EB-87BA-0AD0478025E1";  //uuid生成
                    String buyer_uid = infor_jb.getString("m_uId");  //买家uid
                    String address = eTxtaddress.getText().toString().replace("\n", "").replace(" ", "");  //送货地址
                    String sAcct = eTxttel.getText().toString().replace("\n", "").replace(" ", "");  //联系电话
                    String m_sessionId = null;  //登录返回session

                    String sellerUID = clientip;
                    String orderNo = toAcct + "" + ":" + server_time + ":" + uuid + ":" + buyer_uid + ":" + seller_uid;
                    //买家ID 下订单时自己根据用户名+时间 +uuid 生成 + 买家uid + 卖家uid
                    String orderId = orderNo;
                    buyer_username = toAcct;
                    m_sessionId = logon_jb.getString("sessionId");
                    String baterOrderId = buyer_username + ":" + server_time + ":" + uuid + ":" + buyer_uid;
                    //巴特币的支付ID 下单时自己根据用户名+时间 +uuid 生成 + 买家uid


                    // String code=
                    //  SMSSDK.submitVerificationCode("86", string_tel, );
                    String json = "{'type':'add','toAcct':'" +
                            toAcct +
                            "','paymentRequest':{'amount':'" +
                            amount +
                            "','deliverType':'Undeliver','courierNum':'','orderId':'" +
                            orderId +
                            "','upOrderId':'','body':'lb','m_numberOfImages':2001,'subject':'" +
                            address +
                            "','m_title':'测试','description':'hh','clientIp':'" +
                            clientip +
                            "','comment':'','baterOrderId':'" +
                            baterOrderId +
                            "','sAcct':'" +
                            sAcct +
                            "','toUID':'" +
                            seller_uid +
                            "','channel':'" +
                            channel +
                            "','logonID':'" +
                            toAcct +
                            "','ProductID':'299','liveOrderID':'','m_newBType':'居家生活','m_supplierOrderId':'" +
                            m_supplierOrderId +
                            "','RenewFlag':'','m_sessionId':'" +
                            m_sessionId +
                            "','upQueryId':'','result':'Unpaid','toAcct':'" +
                            toAcct +
                            "','m_oldOrderId':'','orderNo':'" +
                            orderNo +
                            "','m_price':1," +
                            "'upTxnTime':'','refundType':'Unrefund','m_extraDescription':'描述','fromUID':'" +
                            clientip +
                            "'},'orderId':'" +
                            orderId +
                            "'," +
                            "'fromAcct':'" +
                            fromAcct +
                            "'}";
                    Log.d("js", json);
                    String response = okhttptest.EbarterOrder(url, json);
                    Message message = new Message();
                    message.what = 0;
                    message.obj = response;
                    handler.sendMessage(message);
                } catch (Exception e) {
                    // TODO Auto-generated catch block
                    e.printStackTrace();
                }
            }
        }).start();//这个start()方法不要忘记了
    }


    private void sendRequestWithHttpClientPay() {
        new Thread(new Runnable() {
            @Override
            public void run() {
                try {
                    String url = "http://ebarter-env.cn-north-1.eb.amazonaws.com.cn/JSONServlet";
//                    DataManager dataManager = DataManager.getInstance();
//                    JSONObject infor_jb = (JSONObject) dataManager.getInfoMap().get("inforjb");
//                    JSONObject logon_jb = (JSONObject) dataManager.getInfoMap().get("log");
//                    String toAcct = infor_jb.getString("m_acct") + "@";
//                    ;  //买家账号
//                    String amount = eTxtamount.getText().toString().replace("\n", "").replace(" ", "");  //数量
//                    String m_suppid = "test:1572947018027:88EF6CAE-5670-42EB-87BA-0AD0478025E1:26509";
//                    m_suppid = orderpro.getM_supplierOrderid();
//                    String fromAcct = m_suppid.split(":")[0];  //卖家账号
//                    String channel = "6";  //卖家 creditRate
//                    String buyer_username = null;  //买家用户名
//                    String seller_uid = m_suppid.split(":")[3];  //卖家uid
//                    String clientip = seller_uid + "#" + fromAcct;  //卖家id 商品信息中 m_supplierOrderId 截取出来
//                    String m_price = null;  // 订单价格 , 单价乘以数量
//                    String m_supplierOrderId = m_suppid;  //商品信息中 m_supplierOrderId
                    SimpleDateFormat sdf = new SimpleDateFormat("yyyyMMddHHmmss");
                    Calendar calendar = Calendar.getInstance();
                    Date date = calendar.getTime();
                    String dateStr = sdf.format(date);
                    OrderTool orderTool = new OrderTool(Orderjson);
                    String toAcct = orderTool.getToAcct();
                    String orderid = orderTool.getOrderid();
                    String fromAcct = orderTool.getFromAcct();
                    String price = orderTool.getPrice();
                    String json = "{'txnTime':'" + dateStr
                            +
                            "'," +
                            "'reqReserved':'<orderId>" +
                            orderid +
                            "</orderId><fromAcct>" +
                            fromAcct +
                            "</fromAcct><toAcct>" +
                            toAcct +
                            "</toAcct>'," +
                            "'merId':'898053273991289'," +
                            "'orderId':'" +
                            orderid +
                            "'," +
                            "'txnAmt':'" +
                            price +
                            "'}";
                    String response = okhttptest.Unionpay(url, json);
                    Message message = new Message();
                    message.what = 0;
                    message.obj = response;
                    handlerpay.sendMessage(message);
                } catch (Exception e) {
                    // TODO Auto-generated catch block
                    e.printStackTrace();
                }
            }
        }).start();//这个start()方法不要忘记了
    }




}

```
###部件页面代码
```xml

<?xml version="1.0" encoding="utf-8"?>
<android.support.constraint.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    xmlns:app="http://schemas.android.com/apk/res-auto">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical">
        <com.hjq.bar.TitleBar
            android:id="@+id/tb_order_title_bar"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginTop="0dp"
            app:title="提交订单" />

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal">
            <ImageView
                android:layout_width="21dp"
                android:layout_height="26dp"
                android:layout_gravity="center"
                android:src="@drawable/username"/>
            <TextView
                android:layout_width="60dp"
                android:layout_height="wrap_content"
                android:text="姓     名"
                android:textColor="#000000"
                android:textSize="15sp"/>
            <View
                android:layout_width="1dp"
                android:layout_height="25dp"
                android:layout_gravity="center"
                android:background="#000000"/>
            <EditText
                android:id="@+id/order_username"
                android:layout_width="match_parent"
                android:layout_height="wrap_content" />
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal">
            <ImageView
                android:layout_width="21dp"
                android:layout_height="26dp"
                android:layout_gravity="center"
                android:src="@drawable/tel"/>
            <TextView
                android:layout_width="60dp"
                android:layout_height="wrap_content"
                android:text="+86"
                android:gravity="center"
                android:textColor="#000000"
                android:textSize="15sp"/>
            <View
                android:layout_width="1dp"
                android:layout_height="25dp"
                android:layout_gravity="center"
                android:background="#000000"/>
            <EditText
                android:id="@+id/order_tel"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:hint="请输入联系方式" />
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal">
            <ImageView
                android:layout_width="21dp"
                android:layout_height="26dp"
                android:layout_gravity="center"
                android:src="@drawable/username"/>
            <TextView
                android:id="@+id/TxtV_type"
                android:layout_width="60dp"
                android:layout_height="wrap_content"
                android:text="地     址"
                android:gravity="center"
                android:textColor="#000000"
                android:textSize="15sp"/>
            <View
                android:layout_width="1dp"
                android:layout_height="25dp"
                android:layout_gravity="center"
                android:background="#000000"/>
            <EditText
                android:id="@+id/order_address"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:hint="请输入地址" />
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal">
            <TextView
                android:layout_width="60dp"
                android:layout_height="wrap_content"
                android:text="数     量"
                android:textColor="#000000"
                android:textSize="15sp"/>
            <View
                android:layout_width="1dp"
                android:layout_height="25dp"
                android:layout_gravity="center"
                android:background="#000000"/>
            <EditText
                android:id="@+id/order_number"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:hint="请输入数量（仅限整数）"/>
        </LinearLayout>


    </LinearLayout>

</android.support.constraint.ConstraintLayout>
```
### "我的"模块

#### 截图

![image](https://github.com/cheng-ji-hui/picture/blob/master/bbb/me.jpg?raw=true)

 

| 部件名称   | MeActivity                                                   |
| ---------- | ------------------------------------------------------------ |
| 所属子系统 | 无                                                           |
| 部件调用者 | 我的界面                                                     |
| 被调用者   | `MyMemo` `MyStore` `Myneed` `Myshopcar`  `TradeManger` `Mycollection` `Setting` `collectionList` `UsualAddress` |
| 入口参数   | 无                                                           |
| 返回值     | 无                                                           |

## 部件页面代码：

``` xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_height="match_parent"
    android:layout_width="match_parent"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:orientation="vertical"
    android:divider="@drawable/line"
    android:showDividers="middle">
    <TextView
        android:id="@+id/wohead"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="我"
        android:textColor="#ffffff"
        android:background="#DC143C"
        android:gravity="center"
        android:textSize="20sp"
        />

    <LinearLayout
        android:id="@+id/shou_bu"
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:orientation="vertical"
        android:gravity="center"
        android:background="@mipmap/ebtarter_me_prebackground"
        >
        <com.example.ebarter.tools.MyImageView
            android:id="@+id/littlehead"
            android:layout_height="50dp"
            android:layout_width="50dp"
            android:src="@mipmap/im_default_avatar"
            android:layout_marginBottom="5dp"
            />
        <TextView
            android:id="@+id/nicheng"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text=""
            android:textColor="#ffffff"
            android:textSize="15sp"
            />
    </LinearLayout>
    <Button
        android:id="@+id/mybeiwang"
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:text="我的备忘"
        android:background="#ffffff"
        android:gravity="left"
        android:padding="10dp"
        android:minHeight="0dp"
        />


    <Button
        android:id="@+id/mystore"
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:text="我的店铺"
        android:background="#ffffff"
        android:gravity="left"
        android:padding="10dp"
        android:minHeight="0dp"

        />
    <Button
        android:id="@+id/myneed"
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:text="我的需求"
        android:background="#ffffff"
        android:gravity="left"
        android:padding="10dp"
        android:minHeight="0dp"


        />
    <Button
        android:id="@+id/myshopcar"
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:text="我的购物车"
        android:background="#ffffff"
        android:gravity="left"
        android:padding="10dp"
        android:minHeight="0dp"


        />
    <Button
        android:id="@+id/trademanger"
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:text="交易管理"
        android:background="#ffffff"
        android:gravity="left"
        android:padding="10dp"
        android:minHeight="0dp"

        />
    <Button
        android:id="@+id/mycollection"
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:text="我的收藏"
        android:background="#ffffff"
        android:gravity="left"
        android:padding="10dp"
        android:minHeight="0dp"

        />
    <Button
        android:id="@+id/set"
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:text="设置"
        android:background="#ffffff"
        android:gravity="left"
        android:padding="10dp"
        android:minHeight="0dp"

        />
    <Button
        android:id="@+id/collectionlist"
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:text="商品收藏列表"
        android:background="#ffffff"
        android:gravity="left"
        android:padding="10dp"
        android:minHeight="0dp"
        />
    <Button
        android:id="@+id/usualaddress"
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:text="常用地址"
        android:background="#ffffff"
        android:gravity="left"
        android:padding="10dp"
        android:minHeight="0dp"

        />
    <LinearLayout
        android:id="@+id/content"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:orientation="vertical">

    </LinearLayout>
    <android.support.design.widget.BottomNavigationView
        android:id="@+id/navigation"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginEnd="0dp"
        android:layout_marginStart="0dp"
        android:background="?android:attr/windowBackground"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:menu="@menu/navigation"
        android:layout_alignParentBottom="true"/>

</LinearLayout>
```

## 部件逻辑代码

``` java
package com.example.ebarter;


import android.content.Intent;
import android.graphics.Bitmap;
import android.os.Bundle;
import android.os.Handler;
import android.os.Message;
import android.support.annotation.NonNull;
import android.support.design.widget.BottomNavigationView;
import android.support.v7.app.ActionBar;
import android.support.v7.app.AppCompatActivity;
import android.support.v7.widget.RecyclerView;
import android.util.Log;
import android.view.MenuItem;
import android.view.View;
import android.widget.Button;
import android.widget.ImageButton;
import android.widget.TextView;
import android.widget.Toast;

import com.example.ebarter.nets3.S3;
import com.example.ebarter.nets3.S3Data;
import com.example.ebarter.nets3.S3PostActionAdapter;
import com.example.ebarter.nets3.XML_analyzing;
import com.example.ebarter.tools.MyImageView;
import com.example.ebarter.tools.Producttool;
import com.google.gson.Gson;

import org.json.JSONException;
import org.json.JSONObject;

import java.io.IOException;

import okhttp3.Call;
import okhttp3.Callback;
import okhttp3.OkHttpClient;
import okhttp3.Request;
import okhttp3.Response;

import static com.example.ebarter.nets3.S3.TRADE_BUCKET_ARCHIVE;

public class MeActivity extends AppCompatActivity {
    private MyImageView usrpic;
    private Handler handler_Collection;
    private  String  LogonID="";
public static String username;
    private BottomNavigationView.OnNavigationItemSelectedListener mOnNavigationItemSelectedListener
            = new BottomNavigationView.OnNavigationItemSelectedListener() {

        @Override
        public boolean onNavigationItemSelected(@NonNull MenuItem item) {
            switch (item.getItemId()) {
                case R.id.navigation_home:
                    //mTextMessage.setText(R.string.title_home);
                    Intent intent=new Intent(MeActivity.this,chatlist.class);
                    startActivity(intent);
                    return true;
                case R.id.navigation_dashboard:
                    //mTextMessage.setText(R.string.title_dashboard);
                    Intent intent2=new Intent(MeActivity.this,Group.class);
                    startActivity(intent2);
                    return true;
                case R.id.navigation_notifications:
                    //mTextMessage.setText(R.string.title_notifications);

                    return true;
                case R.id.discover:
                    Intent intent3=new Intent(MeActivity.this,MainActivity.class);
                    startActivity(intent3);
                    return  true;
            }
            return false;
        }
    };

    {
        handler_Collection = new Handler() {
            @Override
            public void handleMessage(Message msg) {
                super.handleMessage(msg);
                switch (msg.what) {
                    case 0:

                        String responseinfo = (String) msg.obj;
                        try {
                            JSONObject jb_PL = new JSONObject(responseinfo);
                            Producttool producttool = new Producttool(jb_PL);
                            producttool.getFavList();
                            DataManager dataManager = DataManager.getInstance();
                            dataManager.getInfoMap().put("listOfF", producttool.getFavList());
                            Intent intent = new Intent(MeActivity.this,CollectionList.class);
                            startActivity(intent);
                           // rv=(RecyclerView)findViewById(R.id.rv3);
                            //initreData();
                            //Toast.makeText(CollectionList.this, "init re", Toast.LENGTH_SHORT).show();

                        } catch (Exception e) {

                            //Toast.makeText(CollectionList.this, "init re  failed", Toast.LENGTH_SHORT).show();


                        }

                        //status = response.substring((response.indexOf(":")+3) , (response.indexOf(",")-1));
                        //sessionId = response.substring((response.indexOf("sessionId")+13) , (response.indexOf(",",response.indexOf("sessionId"))-1));
                        //Toast toast_status = Toast.makeText(LoginActivity.this, "这是status" + status, Toast.LENGTH_SHORT);
                        //toast_status.show();
                        break;
                    default:
                        break;

                }
            }
        };

    }




    private Handler handler = new Handler() {
        @Override
        public void handleMessage(Message msg) {
            switch (msg.what) {
                case 0:
                    XML_analyzing xml_analyzing=new XML_analyzing();
                    try {
                        Intent intent = new Intent(MeActivity.this,MyMemo.class);
                        startActivity(intent);
                        xml_analyzing.parseXMLWithPull("beiwnaglu",msg.obj.toString());

                        S3Data s3Data=S3Data.getInstance();
                        for(int j=0;j<10;j++){
                            System.out.println(s3Data.getS3Data().get("beiwnagluitem_num"));
                        }

                    } catch (Exception e) {
                        e.printStackTrace();
                    }
                    break;
                case 1:
                    break;
            }
            super.handleMessage(msg);
        }
    };







    @Override
    protected void onCreate(Bundle savedInstanceState) {

        super.onCreate(savedInstanceState);
        setContentView(R.layout.me);

       // BottomNavigationView navigation = (BottomNavigationView) findViewById(R.id.navigation);
        //navigation.setSelectedItemId(R.id.navigation_notifications);
        ActionBar actionBar = getSupportActionBar();
        if(actionBar!=null){
            actionBar.hide();
        }
        DataManager dataManager = DataManager.getInstance();
        JSONObject jb=( JSONObject)dataManager.getInfoMap().get("inforjb");
        String string_uid="";

        try {
            String user_name = jb.getString("m_acct");
           S3Data s3Data= S3Data.getInstance();
           s3Data.getS3Data().put("username",user_name);
            username=user_name;
            TextView textView =(TextView)findViewById(R.id.nicheng);
            string_uid =""+jb.getInt("m_uId");
textView.setText(user_name);
        } catch (JSONException e) {
        }
      //  DataManager dataManager = DataManager.getInstance();
        JSONObject log_jb = (JSONObject) dataManager.getInfoMap().get("log");
        try {
            LogonID = log_jb.getJSONObject("user").getString("LogonID");
        } catch (Exception e) {
        }
        String url="https://s3.cn-north-1.amazonaws.com.cn/linda-trades-archive-1/";
        usrpic=(MyImageView)findViewById(R.id.littlehead);
        usrpic.setImageURL(url+string_uid+".jpg");
        Log.d("lx",string_uid);
        //ImageButton imageButton=(ImageButton)findViewById(R.id.littlehead);

        //imageButton
        usrpic.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent = new Intent(MeActivity.this,PersonInformation.class);
                startActivity(intent);
            }
        });
        BottomNavigationView navigation = (BottomNavigationView) findViewById(R.id.navigation);
        navigation.setSelectedItemId(R.id.navigation_notifications);
        navigation.setOnNavigationItemSelectedListener(mOnNavigationItemSelectedListener);
Button button1=(Button)findViewById(R.id.mystore);
        button1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Intent intent = new Intent(MeActivity.this,MyStore.class);
                startActivity(intent);
            }
        });


        Button mybeiwang =(Button)findViewById(R.id.mybeiwang);
        mybeiwang.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                //得到数据
//                S3.getINSTANCE().setAwsData("AKIAPWGNHSKNQW2WYNNQ", "dhzG2r1JDhrknCT31Dt8AjHPYx5BfelEq/Bh47oI");
//                S3.getINSTANCE().downloadFile(TRADE_BUCKET_ARCHIVE, username+"-MyMemorandum112.plist", new S3PostActionAdapter(){
//                    public void downloadSucceed (Bitmap bitmap, String fileName){
//
//                    }
//                    public void notifyError (String message){
//
//
//                    }
//                    public void downloadfilefromS3(String plist){
//                        Message message=new Message();
//                        message.what=0;
//                        message.obj=plist;
//                        handler.sendMessage(message);
//
//                    }
//
//
//                });

                String url = "https://s3.cn-north-1.amazonaws.com.cn/linda-trades-archive-1/"+username+"-MyMemorandum112.plist";
                OkHttpClient client = new OkHttpClient();
                Request request = new Request.Builder()
                        .url(url)
                        .get()  //默认为GET请求，可以不写
                        .build();
                final Call call = client.newCall(request);
                call.enqueue(new Callback() {
                    @Override
                    public void onFailure(Call call, IOException e) {
                        //异步请求失败之后的回调
                    Toast.makeText(MeActivity.this,"网络问题，请求失败！",Toast.LENGTH_SHORT).show();                    }

                    @Override
                    public void onResponse(Call call, Response response) throws IOException {
                        //异步请求成功之后的回调
                        XML_analyzing xml_analyzing=new XML_analyzing();
                        try {
                            xml_analyzing.parseXMLWithPull("memo",response.body().string());
                            Intent intent = new Intent(MeActivity.this,MyMemo.class);
                            startActivity(intent);

                        } catch (Exception e) {
                            e.printStackTrace();
                        }

                    }
                });

            }
        });
        Button myneed =(Button)findViewById(R.id.myneed);
        myneed.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent = new Intent(MeActivity.this,Myneed.class);
                startActivity(intent);
            }
        });
        Button myshopcar =(Button)findViewById(R.id.myshopcar);
        myshopcar.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent = new Intent(MeActivity.this,Myshopcar.class);
                startActivity(intent);
            }
        });
        Button trademanager =(Button)findViewById(R.id.trademanger);
        trademanager.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent = new Intent(MeActivity.this,TradeManger.class);
                startActivity(intent);
            }
        });
        Button mycollection =(Button)findViewById(R.id.mycollection);
        mycollection.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent = new Intent(MeActivity.this,MyCollection.class);
                startActivity(intent);
            }
        });
        Button setting =(Button)findViewById(R.id.set);
        setting.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent = new Intent(MeActivity.this,Setting.class);
                startActivity(intent);
            }
        });
        Button collectionlist =(Button)findViewById(R.id.collectionlist);
        collectionlist.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                sendRequestWithHttpClientCollection();

            }
        });
        Button address =(Button)findViewById(R.id.usualaddress);
        address.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent = new Intent(MeActivity.this,UsualAddress.class);
                startActivity(intent);
            }
        });











    }
    private void sendRequestWithHttpClientCollection() {
        new Thread(new Runnable() {
            @Override
            public void run() {
                try {
                    String url = "http://ebarter-env.cn-north-1.eb.amazonaws.com.cn/JSONServlet";
                    String json = "{'favoriteType':'p','logonID':'" +
                            LogonID +
                            "','type':'GetebtUserFavoriteByLogonID'}";
                    Message message = new Message();
                    message.what = 0;
                    Okhttptest okhttptest=new Okhttptest();
                    message.obj = okhttptest.Favoritelist(url, json);
                    handler_Collection.sendMessage(message);
                } catch (Exception e) {
                    // TODO Auto-generated catch block
                    e.printStackTrace();
                }
            }
        }).start();//这个start()方法不要忘记了
    }


}

```



| 部件名称   | MyMemo                                                   |
| ---------- | -------------------------------------------------------- |
| 所属子系统 | 无                                                       |
| 部件调用者 | 我的界面                                                 |
| 被调用者   | `my_trad_memo` ``MymemoAdapter` ``  `S3` `XML_analyzing` |
| 入口参数   | s3Data.getS3Data().get  XML_analyzing 放入hashmap的数据  |
| 返回值     | 无                                                       |

## 部件逻辑代码

```java
package com.example.ebarter;

import android.app.Activity;
import android.content.Context;
import android.content.Intent;
import android.os.Bundle;
import android.os.Handler;
import android.os.Message;
import android.support.v7.app.ActionBar;
import android.support.v7.app.AppCompatActivity;
import android.support.v7.widget.LinearLayoutManager;
import android.support.v7.widget.RecyclerView;
import android.util.Log;
import android.view.MenuItem;
import android.view.View;
import android.widget.ImageButton;
import android.widget.PopupMenu;
import android.widget.TextView;
import android.widget.Toast;

import com.dd.plist.NSArray;
import com.dd.plist.NSDictionary;
import com.dd.plist.PropertyListFormatException;
import com.dd.plist.PropertyListParser;
import com.example.ebarter.nets3.Plist_create;
import com.example.ebarter.nets3.S3;
import com.example.ebarter.nets3.S3Data;
import com.example.ebarter.nets3.S3PostActionAdapter;
import com.example.ebarter.nets3.XML_analyzing;

import org.json.JSONObject;
import org.xml.sax.SAXException;

import java.io.ByteArrayInputStream;
import java.io.File;
import java.io.IOException;
import java.io.InputStream;
import java.text.ParseException;
import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;
import java.util.Map;

import javax.xml.parsers.ParserConfigurationException;

import static android.widget.Toast.LENGTH_SHORT;
import static com.mob.MobSDK.getContext;

public class MyMemo extends AppCompatActivity {
    private Handler handler = new Handler() {
        @Override
        public void handleMessage(Message msg) {
            switch (msg.what) {
                case 0:
                    Toast toast = Toast.makeText(MyMemo.this, "删除成功", LENGTH_SHORT);
                    toast.show();
                    Intent intent1 = new Intent(MyMemo.this, MeActivity.class);
                    startActivity(intent1);
                    break;
                case 1:
                    Toast toast1 = Toast.makeText(MyMemo.this, "删除失败", LENGTH_SHORT);
                    toast1.show();
                    break;
            }
            super.handleMessage(msg);
        }
    };

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_my_memo);
        ActionBar actionBar = getSupportActionBar();
        if(actionBar!=null){
            actionBar.hide();
        }
        final TextView[] textView = {(TextView) findViewById(R.id.titletext)};
        textView[0].setText("我的备忘");
        ImageButton imageButton = (ImageButton)findViewById(R.id.tile_add);
        imageButton.setVisibility(View.VISIBLE);
        imageButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Intent intent=new Intent(MyMemo.this,my_trad_memo.class);
                intent.putExtra("number","0");
                startActivity(intent);
            }
        });

        final S3Data s3Data=S3Data.getInstance();
if(s3Data.getS3Data().get("memoitem_num")==(Integer)0){
    Toast.makeText(this,"备忘录无信息",Toast.LENGTH_LONG).show();
}
else {
//            Log.d("sssssssssssssssssssssss","aaaaaaaaaaaaa");
//        Log.d("123456","262626262622");
//        //S3Data s3Data=S3Data.getInstance();
//        s3Data.getS3Data().put("aaaa",1);
//        Iterator iter = s3Data.getS3Data().entrySet().iterator();
//        while (iter.hasNext()) {
//            Map.Entry entry = (Map.Entry) iter.next();
//            Object key1 = entry.getKey();
//            Object val = entry.getValue();
//            System.out.println(key1 + "aaaa" + val);
//        }
    final Integer item_num = (int) s3Data.getS3Data().get("memoitem_num");
    final List<Integer> chatData = new ArrayList<Integer>();
    for(int i=0;i<item_num;i++){
        chatData.add(i);
    }

    RecyclerView recyclerView = (RecyclerView) findViewById(R.id.mymemo_recycleview);
    LinearLayoutManager layoutManager = new LinearLayoutManager(this);
    recyclerView.setLayoutManager(layoutManager);
    final MymemoAdapter mymemoAdapter = new MymemoAdapter(chatData);
    recyclerView.setAdapter(mymemoAdapter);
    // 设置数据后就要给RecyclerView设置点击事件
        mymemoAdapter.setOnItemClickListener(new MymemoAdapter.ItemClickListener() {
        @Override
        public void onItemClick(int position) {
            Integer a=position+1;
            //Toast.makeText(MyMemo.this , a.toString() , Toast.LENGTH_SHORT).show();
            Intent intent=new Intent(MyMemo.this,my_trad_memo.class);
            intent.putExtra("number",a.toString());
            startActivity(intent);
        }
    });
    mymemoAdapter.setOnItemClickListener(new MymemoAdapter.OnItemClickListener() {
        @Override
        public void onItemLongClick(final View view, final int pos) {
            PopupMenu popupMenu = new PopupMenu(getContext(),view);
            popupMenu.getMenuInflater().inflate(R.menu.delete,popupMenu.getMenu());

            //弹出式菜单的菜单项点击事件
            popupMenu.setOnMenuItemClickListener(new PopupMenu.OnMenuItemClickListener() {

                @Override
                public boolean onMenuItemClick(MenuItem item) {

                    if(item.getItemId()==R.id.action_delete) {
                        Integer pos1=pos+1;
                  s3Data.getS3Data().remove("memoitem"+pos1.toString()+"_"+"memorandumAmountName");
                  s3Data.getS3Data().remove("memoitem"+pos1.toString()+"_"+"memorandumDate");
                  s3Data.getS3Data().remove("memoitem"+pos1.toString()+"_"+"memorandumInsideBrokerName");
                  s3Data.getS3Data().remove("memoitem"+pos1.toString()+"_"+"memorandumInsideName");
                  s3Data.getS3Data().remove("memoitem"+pos1.toString()+"_"+"memorandumOutBrokersideName");
                  s3Data.getS3Data().remove("memoitem"+pos1.toString()+"_"+"memorandumOutsideName");
                  s3Data.getS3Data().remove("memoitem"+pos1.toString()+"_"+"memorandumProtocalContentName");


                  for(Integer i=pos1;i<item_num;i++){
                      Integer j=i+1;
                      s3Data.getS3Data().put("memoitem"+i.toString()+"_"+"memorandumAmountName",s3Data.getS3Data().get("memoitem"+j.toString()+"_"+"memorandumAmountName"));
                      s3Data.getS3Data().put("memoitem"+i.toString()+"_"+"memorandumDate",s3Data.getS3Data().get("memoitem"+j.toString()+"_"+"memorandumDate"));
                      s3Data.getS3Data().put("memoitem"+i.toString()+"_"+"memorandumInsideBrokerName",s3Data.getS3Data().get("memoitem"+j.toString()+"_"+"memorandumInsideBrokerName"));
                      s3Data.getS3Data().put("memoitem"+i.toString()+"_"+"memorandumInsideName",s3Data.getS3Data().get("memoitem"+j.toString()+"_"+"memorandumInsideName"));
                      s3Data.getS3Data().put("memoitem"+i.toString()+"_"+"memorandumOutBrokersideName",s3Data.getS3Data().get("memoitem"+j.toString()+"_"+"memorandumOutBrokersideName"));
                      s3Data.getS3Data().put("memoitem"+i.toString()+"_"+"memorandumOutsideName",s3Data.getS3Data().get("memoitem"+j.toString()+"_"+"memorandumOutsideName"));
                      s3Data.getS3Data().put("memoitem"+i.toString()+"_"+"memorandumProtocalContentName",s3Data.getS3Data().get("memoitem"+j.toString()+"_"+"memorandumProtocalContentName"));
                      s3Data.getS3Data().remove("memoitem"+j.toString()+"_"+"memorandumAmountName");
                      s3Data.getS3Data().remove("memoitem"+j.toString()+"_"+"memorandumDate");
                      s3Data.getS3Data().remove("memoitem"+j.toString()+"_"+"memorandumInsideBrokerName");
                      s3Data.getS3Data().remove("memoitem"+j.toString()+"_"+"memorandumInsideName");
                      s3Data.getS3Data().remove("memoitem"+j.toString()+"_"+"memorandumOutBrokersideName");
                      s3Data.getS3Data().remove("memoitem"+j.toString()+"_"+"memorandumOutsideName");
                      s3Data.getS3Data().remove("memoitem"+j.toString()+"_"+"memorandumProtocalContentName");
                  }
s3Data.getS3Data().remove("memoitem_num");
                        s3Data.getS3Data().put("memoitem_num",item_num-1);


                        S3.getINSTANCE().setAwsData("AKIAPWGNHSKNQW2WYNNQ", "dhzG2r1JDhrknCT31Dt8AjHPYx5BfelEq/Bh47oI");
                        Plist_create plist_create=new Plist_create();
                        String url=plist_create.creat_plist("beiwanglu");
                        File file=new File(url);
                        try {


                            S3.getINSTANCE().newUploadFile((String) s3Data.getS3Data().get("username") + "-MyMemorandum112.plist", file, new S3PostActionAdapter() {
                                public void uploadSucceed(String preSignedUrl) {
                                    Log.d("succeed", "66666666666666666666");
                                    handler.sendEmptyMessage(0);

                                }

                                public void notifyError(String msg) {
                                    Log.d("failed", "66666666666666666666");
                                    handler.sendEmptyMessage(1);

                                }
                            });
                        }catch (Exception e){

                        }

                    }

                    return false;


                }


            });
            popupMenu.show();
        }
    });

}

    }
}

```





| 部件名称   | XML_analyzing                |
| ---------- | ---------------------------- |
| 所属子系统 | 无                           |
| 部件调用者 | 整个程序                     |
| 被调用者   | 无                           |
| 入口参数   | String origin,String xmlData |
| 返回值     | 无                           |

## 部件逻辑代码

```java
package com.example.ebarter.nets3;

import android.app.Activity;
import android.util.Log;

import com.example.ebarter.App;
import com.example.ebarter.DataManager;

import org.xmlpull.v1.XmlPullParser;
import org.xmlpull.v1.XmlPullParserException;
import org.xmlpull.v1.XmlPullParserFactory;

import java.io.StringReader;
import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;

public class XML_analyzing  {

    public  void parseXMLWithPull(String origin,String xmlData) throws Exception{

        XmlPullParserFactory factory = XmlPullParserFactory.newInstance();
        XmlPullParser parser = factory.newPullParser();
        parser.setInput(new StringReader(xmlData));
        int eventType = parser.getEventType();
        String key = "";
        String string = "";
        Integer i = 0;
        while (eventType != XmlPullParser.END_DOCUMENT) {
            String nodeName = parser.getName();
            switch (eventType) {
                // 开始解析某个结点
                case XmlPullParser.START_TAG: {
                    if("dict".equals(nodeName)){
                        i++;
                    }
                    if ("key".equals(nodeName)) {
                        key = parser.nextText();
                        //i++;
                        //Log.d("key",key);
                    } else if ("string".equals(nodeName)) {
                        string = parser.nextText();
                      // Log.d("string",string);
                        S3Data s3Data=S3Data.getInstance();
                        s3Data.getS3Data().put(origin+"item"+i.toString()+"_"+key,string);
                    }
                    break;
                }
                // 完成解析某个结点
                case XmlPullParser.END_TAG: {
                    break;
                }
                default:
                    break;
            }
            eventType = parser.next();
        }
        //Log.d("aaaaaaaaaaaaaaaa",i.toString());
        S3Data s3Data=S3Data.getInstance();
        s3Data.getS3Data().put(origin+"item_num",i);
       // Log.d("aaaaaaxascdcasaxsa",App.S3data.get("item1_Name").toString());



    }
}

```




| 部件名称   | my_trad_memo |
| ---------- | ------------ |
| 所属子系统 | Mymemo       |
| 部件调用者 | Mymemo       |
| 被调用者   | 无           |
| 入口参数   | 无           |
| 返回值     | 无           |

## 部件页面代码

```java
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_height="match_parent"
    android:layout_width="match_parent"
    android:background="#F2F2F7"
    android:orientation="vertical"
    android:layout_marginLeft="10dp"

    >
    <com.example.ebarter.Title_1Layout
        android:id="@+id/aaa"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        />
    <LinearLayout
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:orientation="horizontal"
    android:background="#ffffff"
        android:layout_marginLeft="5dp"
        android:layout_marginRight="5dp"
        android:paddingTop="10dp"
        android:paddingBottom="10dp"
        android:gravity="center"
        android:focusable="true"
        android:focusableInTouchMode="true"

        >
<ImageView
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:src="@mipmap/data"
    android:layout_marginLeft="5dp"
    />
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginLeft="10dp"
            android:text="日期"
            android:textSize="15sp"

            />
        <TextView
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            />
        <TextView
            android:id="@+id/trad_data"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text=""
            android:textSize="10sp"

            />

</LinearLayout>

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="易入方"
        android:textSize="10sp"
        android:textColor="#FF0000"
        android:layout_marginLeft="10dp"
        />

    <LinearLayout
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:orientation="horizontal"
        android:background="#ffffff"
        android:layout_marginLeft="5dp"
        android:layout_marginRight="5dp"
        android:paddingTop="10dp"
        android:paddingBottom="10dp"
        android:gravity="center"
        android:focusable="true"
        android:focusableInTouchMode="true"
        >
        <ImageView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:src="@mipmap/company_person"
            android:layout_marginLeft="5dp"

            />
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginLeft="10dp"
            android:text="企业/个人"
            android:textSize="15sp"

            />
        <TextView
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            />
        <EditText
            android:id="@+id/in_person"
            android:hint="请填写易入方企业/个人名称"
            android:textSize="10sp"
            android:background="@drawable/none"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"

            />

    </LinearLayout>
    <LinearLayout
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:orientation="horizontal"
        android:background="#ffffff"
        android:layout_marginLeft="5dp"
        android:layout_marginRight="5dp"
        android:paddingTop="10dp"
        android:paddingBottom="10dp"
        android:gravity="center"
        android:focusable="true"
        android:focusableInTouchMode="true"
        >
        <ImageView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:src="@mipmap/middleman"
            android:layout_marginLeft="5dp"

            />
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginLeft="10dp"
            android:text="经纪人"
            android:textSize="15sp"

            />
        <TextView
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            />
        <EditText
            android:id="@+id/in_middleperson"
            android:hint="请填写易入方经纪人名称"
            android:background="@drawable/none"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:textSize="10sp"

            />

    </LinearLayout>
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="易出方"
        android:textSize="10sp"
        android:textColor="#FF0000"
        android:layout_marginLeft="10dp"

        />

    <LinearLayout
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:orientation="horizontal"
        android:background="#ffffff"
        android:layout_marginLeft="5dp"
        android:layout_marginRight="5dp"
        android:paddingTop="10dp"
        android:paddingBottom="10dp"
        android:gravity="center"
        android:focusable="true"
        android:focusableInTouchMode="true"
        >
        <ImageView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:src="@mipmap/company_person"
            android:layout_marginLeft="5dp"

            />
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginLeft="10dp"
            android:text="企业/个人"
            android:textSize="15sp"

            />
        <TextView
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            />
        <EditText
            android:id="@+id/out_person"
            android:hint="请填写易出方企业/个人名称"
            android:background="@drawable/none"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:textSize="10sp"

            />
    </LinearLayout>
    <LinearLayout
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:orientation="horizontal"
        android:background="#ffffff"
        android:layout_marginLeft="5dp"
        android:layout_marginRight="5dp"
        android:paddingTop="10dp"
        android:paddingBottom="10dp"
        android:gravity="center"
        android:focusable="true"
        android:focusableInTouchMode="true"
        >
        <ImageView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:src="@mipmap/middleman"
            android:layout_marginLeft="5dp"

            />
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginLeft="10dp"
            android:text="经纪人"
            android:textSize="15sp"

            />
        <TextView
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            />
        <EditText
            android:id="@+id/out_midddleperson"
            android:hint="请填写易出方经纪人名称"
            android:background="@drawable/none"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:textSize="10sp"

            />

    </LinearLayout>
    <LinearLayout
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:orientation="horizontal"
        android:background="#ffffff"
        android:layout_marginLeft="5dp"
        android:layout_marginRight="5dp"
        android:paddingTop="10dp"
        android:paddingBottom="10dp"
        android:gravity="center"
        android:focusable="true"
        android:focusableInTouchMode="true"
        >

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginLeft="10dp"
            android:text="双方就："
            />
        <EditText
            android:id="@+id/agreement_content"
            android:hint="请输入协议内容"
            android:textSize="10sp"
            android:background="@drawable/none"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            />
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="达成如上协议"
            />

    </LinearLayout>
    <LinearLayout
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:orientation="horizontal"
        android:background="#ffffff"
        android:layout_marginLeft="5dp"
        android:layout_marginRight="5dp"
        android:paddingTop="10dp"
        android:paddingBottom="10dp"
        android:gravity="center"
        android:focusable="true"
        android:focusableInTouchMode="true"
        >

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginLeft="10dp"
            android:text="交易总额："
            />
        <EditText
android:id="@+id/trad_money"
            android:hint="请输入金额"
            android:textSize="10sp"
            android:background="@drawable/none"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            />
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="巴特"
            />

    </LinearLayout>
    <TextView
        android:layout_marginTop="10dp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="提示："
        android:textSize="10sp"
        android:textColor="#CDC9C9"
        />
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="1.此表为交易双方预订单，由易出方发起填写，易入方确认后方可形成，具体交易请以实际交易单位为准。"
        android:textSize="10sp"
        android:textColor="#CDC9C9"
        />
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="2.易出方可修改内容，易入方确认后方可保存。"
        android:textSize="10sp"
        android:textColor="#CDC9C9" />
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="3.双方经纪人，易巴特客服均有查看权限。"
        android:textSize="10sp"
        android:textColor="#CDC9C9" />


    <LinearLayout
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:orientation="horizontal"
        android:background="#F2F2F7"
        android:layout_marginLeft="5dp"
        android:layout_marginRight="5dp"
        android:paddingTop="10dp"
        android:paddingBottom="10dp"
        android:gravity="center"

        >


      <TextView
          android:layout_width="0dp"
          android:layout_weight="1"
          android:layout_height="wrap_content"
          />
        <Button
            android:id="@+id/makesure"
            android:background="@drawable/buttonshape"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="确认"
            android:textColor="#ffffff"
            android:paddingBottom="10dp"
            android:paddingTop="10dp"
            android:paddingLeft="25dp"
            android:paddingRight="25dp"
            />

    </LinearLayout>
</LinearLayout>
```

## 部件逻辑代码

```java
package com.example.ebarter;

import android.content.Intent;
import android.os.Handler;
import android.os.Message;
import android.support.v7.app.ActionBar;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.util.Log;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import android.widget.Toast;

import com.example.ebarter.nets3.Plist_create;
import com.example.ebarter.nets3.S3;
import com.example.ebarter.nets3.S3Data;
import com.example.ebarter.nets3.S3PostActionAdapter;
import com.example.ebarter.nets3.XML_analyzing;

import java.io.File;
import java.sql.Time;
import java.util.Calendar;
import java.util.Iterator;
import java.util.Map;

import static android.widget.Toast.LENGTH_SHORT;

public class my_trad_memo extends AppCompatActivity {
    private Handler handler = new Handler() {
        @Override
        public void handleMessage(Message msg) {
            switch (msg.what) {
                case 0:
                    Toast toast = Toast.makeText(my_trad_memo.this, "保存成功", LENGTH_SHORT);
                    toast.show();
                    Intent intent1 = new Intent(my_trad_memo.this, MeActivity.class);
                    startActivity(intent1);
                    break;
                case 1:
                    Toast toast1 = Toast.makeText(my_trad_memo.this, "保存失败", LENGTH_SHORT);
                    toast1.show();
                    break;
            }
            super.handleMessage(msg);
        }
    };
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_my_trad_memo);
        final EditText editText = (EditText) findViewById(R.id.in_person);
        final EditText editText1 = (EditText) findViewById(R.id.in_middleperson);
        final EditText editText2 = (EditText) findViewById(R.id.out_person);
        final EditText editText3 = (EditText) findViewById(R.id.out_midddleperson);
        final EditText editText4 = (EditText) findViewById(R.id.agreement_content);
        final EditText editText5 = (EditText) findViewById(R.id.trad_money);
        final TextView textView2 = (TextView) findViewById(R.id.trad_data);
        final Button button=(Button)findViewById(R.id.makesure);
        ActionBar actionBar = getSupportActionBar();

        if(actionBar!=null){
            actionBar.hide();
        }
        final TextView textView=(TextView)findViewById(R.id.titletext);
        textView.setText("交易备忘录");


        final Intent intent=getIntent();
        final String number=intent.getStringExtra("number");


        if(number.equals("0")){
            Calendar calendar = Calendar.getInstance();
            int year = calendar.get(Calendar.YEAR);
            int month = calendar.get(Calendar.MONTH)+1;
            int day = calendar.get(Calendar.DAY_OF_MONTH);
            if(month<10&&day<10){
                textView2.setText(year+"年"+"0"+month+"月"+"0"+day+"日");

            }
            if(month<10&&day>=10) {
                textView2.setText(year+"年"+"0"+month+"月"+day+"日");
            }
            if(month>=10&&day<10) {
                textView2.setText(year+"年"+month+"月"+"0"+day+"日");
            }
            if(month>10&&day>10) {
                textView2.setText(year+"年"+month+"月"+day+"日");
            }
            button.setOnClickListener(new View.OnClickListener() {
                @Override
                public void onClick(View v) {
Log.d("aa","a"+editText.getText().toString()+"a");
if(editText.getText().toString().equals("")||editText1.getText().toString().equals("")||editText2.getText().toString().equals("")||editText3.getText().toString().equals("")||editText4.getText().toString().equals("")||editText5.getText().toString().equals("")) {
    Toast toast = Toast.makeText(my_trad_memo.this, "请填写完整", LENGTH_SHORT);
    toast.show();
}
else {

    S3Data s3Data = S3Data.getInstance();
    Integer item_num;
    if(s3Data.getS3Data().get("memoitem_num")==null) {
item_num=1;
        s3Data.getS3Data().put("memoitem_num",item_num+1);
    }
    else {
        item_num = (int) s3Data.getS3Data().get("memoitem_num") + 1;
    }
     s3Data.getS3Data().put("memoitem" + item_num.toString() + "_" + "memorandumDate",textView2.getText().toString());
   s3Data.getS3Data().put("memoitem" + item_num.toString() + "_memorandumInsideBrokerName",editText.getText().toString());
     s3Data.getS3Data().put("memoitem" + item_num.toString() + "_" + "memorandumInsideName",editText1.getText().toString());
     s3Data.getS3Data().put("memoitem" + item_num.toString() + "_" + "memorandumOutBrokersideName",editText2.getText().toString());
    s3Data.getS3Data().put("memoitem" + item_num.toString()+ "_" + "memorandumOutsideName",editText3.getText().toString());
    s3Data.getS3Data().put("memoitem" + item_num.toString()+ "_" + "memorandumProtocalContentName",editText4.getText().toString());
    s3Data.getS3Data().put("memoitem" + item_num.toString()+ "_" + "memorandumAmountName",editText5.getText().toString());
    s3Data.getS3Data().put("memoitem_num",item_num);
    S3.getINSTANCE().setAwsData("AKIAPWGNHSKNQW2WYNNQ", "dhzG2r1JDhrknCT31Dt8AjHPYx5BfelEq/Bh47oI");
    Plist_create plist_create=new Plist_create();
    String url=plist_create.creat_plist("beiwanglu");
    File file=new File(url);
try {


    S3.getINSTANCE().newUploadFile((String) s3Data.getS3Data().get("username") + "-MyMemorandum112.plist", file, new S3PostActionAdapter() {
        public void uploadSucceed(String preSignedUrl) {
            Log.d("succeed", "66666666666666666666");
            handler.sendEmptyMessage(0);

        }

        public void notifyError(String msg) {
            Log.d("failed", "66666666666666666666");
            handler.sendEmptyMessage(1);

        }
    });
}catch (Exception e){

}




}



                }
            });
        }
        else {
            S3Data s3Data = S3Data.getInstance();
            String trad_data = (String) s3Data.getS3Data().get("memoitem" + number + "_" + "memorandumDate");
            String in_person = (String) s3Data.getS3Data().get("memoitem" + number + "_memorandumInsideBrokerName");
            String in_middleperson = (String) s3Data.getS3Data().get("memoitem" + number + "_" + "memorandumInsideName");
            String out_person = (String) s3Data.getS3Data().get("memoitem" + number + "_" + "memorandumOutBrokersideName");
            String out_middleperson = (String) s3Data.getS3Data().get("memoitem" + number + "_" + "memorandumOutsideName");
            String agreement_content = (String) s3Data.getS3Data().get("memoitem" + number + "_" + "memorandumProtocalContentName");
            String trad_money = (String) s3Data.getS3Data().get("memoitem" + number + "_" + "memorandumAmountName");

            textView2.setText(trad_data);
            editText.setText(in_person);
            editText1.setText(in_middleperson);
            editText2.setText(out_person);
            editText3.setText(out_middleperson);
            editText4.setText(agreement_content);
            editText5.setText(trad_money);

        }


    }
}

```

| 部件名称   | MyStore         |
| ---------- | --------------- |
| 所属子系统 | MeActivity      |
| 部件调用者 | 整个程序        |
| 被调用者   | putproduct      |
| 入口参数   | Context context |
| 返回值     | 无              |

##  部件页面代码

```java
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_height="wrap_content"
    android:layout_width="match_parent"
    android:orientation="vertical"
    >
    <RelativeLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="#DC143C"
        >
        <ImageButton
            android:id="@+id/back"
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:src="@mipmap/back"
            android:background="#DC143C"
            android:paddingLeft="10dp"
            android:paddingTop="10dp"
            android:paddingBottom="10dp"
            android:layout_alignParentLeft="true"
            />
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="店铺详情"
            android:textColor="#ffffff"
            android:textSize="20sp"
android:layout_centerInParent="true"
            />
        <ImageButton
            android:id="@+id/add"
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_alignParentRight="true"
            android:src="@mipmap/add"
            android:background="#DC143C"
            android:paddingRight="10dp"
            android:paddingTop="10dp"
            android:paddingBottom="10dp"
            />
    </RelativeLayout>

    <RelativeLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="#ffffff"
        >
<TextView
    android:id="@+id/connectpeople"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_alignParentLeft="true"
    android:text="联系人："
    android:textColor="#000000"
    android:textSize="15sp"
    android:paddingLeft="5dp"
    android:paddingTop="20dp"
    />
        <Button
            android:id="@+id/xiugai1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_alignParentRight="true"
            android:text="修改"
            android:background="#ffffff"
            android:textColor="#FF0000"
            />
    </RelativeLayout>

    <RelativeLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="#ffffff"
        >
        <TextView
            android:id="@+id/zhuceyear"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_alignParentLeft="true"
            android:text="注册年份："
            android:textColor="#000000"
            android:textSize="15sp"
            android:paddingLeft="5dp"
            android:paddingTop="15dp"
            />
        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_alignParentRight="true"
            android:text="不可修改"
            android:textColor="#D4D4D4"
            android:background="#ffffff"
            />
    </RelativeLayout>
    <RelativeLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="#ffffff"
        >
        <TextView
            android:id="@+id/shoouji"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_alignParentLeft="true"
            android:text="手机："
            android:textColor="#000000"
            android:textSize="15sp"
            android:paddingLeft="5dp"
            android:paddingTop="15dp"
            />
        <Button
            android:id="@+id/xiugai2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_alignParentRight="true"
            android:text="修改"
            android:textColor="#FF0000"
            android:background="#ffffff"

            />
    </RelativeLayout>

    <RelativeLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="#ffffff"
        >
        <TextView
            android:id="@+id/gongsiaddress"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_alignParentLeft="true"
            android:text="公司地址："
            android:textColor="#000000"
            android:textSize="15sp"
            android:paddingLeft="5dp"
            android:paddingTop="15dp"

            />
        <Button
            android:id="@+id/xiugai3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_alignParentRight="true"
            android:text="修改"
            android:textColor="#FF0000"
            android:background="#ffffff"

            />
    </RelativeLayout>
    <RelativeLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="#ffffff"
        >
        <TextView
            android:id="@+id/gongsigerenname"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_alignParentLeft="true"
            android:text="公司/个人名称："
            android:textColor="#000000"
            android:textSize="15sp"
            android:paddingLeft="5dp"
            android:paddingTop="15dp"
            />
        <Button
            android:id="@+id/xiugai4"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_alignParentRight="true"
            android:text="修改"
            android:textColor="#FF0000"
            android:background="#ffffff"
            />
    </RelativeLayout>
    </LinearLayout>

```

部件逻辑代码

```java
package com.example.ebarter;


import android.content.Intent;
import android.os.Bundle;
import android.os.Handler;
import android.support.v7.app.ActionBar;
import android.support.v7.app.AppCompatActivity;
import android.view.View;
import android.widget.Button;
import android.widget.ImageButton;
import android.widget.TextView;

import com.hb.dialog.myDialog.MyAlertInputDialog;

import org.json.JSONException;
import org.json.JSONObject;

public class MyStore extends AppCompatActivity {
    private Handler hander1;

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_my_store);
        ActionBar actionBar = getSupportActionBar();
        if(actionBar!=null){
            actionBar.hide();
        }
        DataManager dataManager = DataManager.getInstance();
        JSONObject jb=( JSONObject)dataManager.getInfoMap().get("inforjb");



        try {
            String name= jb.getString("RoleName");
            TextView textView1 =(TextView)findViewById(R.id.gongsigerenname);
            textView1.setText("公司/个人名称："+name);
            String zhucenianfen=jb.getString("creationTime");
            TextView textView =(TextView)findViewById(R.id.zhuceyear);
            textView.setText("注册年份："+zhucenianfen);
            JSONObject jb1=jb.getJSONObject("m_registered");
            String user_phone= jb1.getString("m_contactPhone");
            TextView textView2 =(TextView)findViewById(R.id.shoouji);
            textView2.setText("手机："+user_phone);
            String gongsidizhi=jb1.getString("m_city");
            String gongsidizhi1=jb1.getString("m_address");
            TextView textView3 =(TextView)findViewById(R.id.gongsiaddress);
            textView3.setText("公司地址："+gongsidizhi+gongsidizhi1);
            String connectname=jb1.getString("m_firstName");
            String connectname1=jb1.getString("m_lastName");
            TextView textView4 =(TextView)findViewById(R.id.connectpeople);
            textView4.setText("联系人:"+connectname+connectname1);

        } catch (JSONException e) {
        }


Button button=(Button)findViewById(R.id.xiugai1);
        Button button1=(Button)findViewById(R.id.xiugai2);
        Button button2=(Button)findViewById(R.id.xiugai3);
        Button button3=(Button)findViewById(R.id.xiugai4);

        button.setOnClickListener(new View.OnClickListener() {
    @Override
    public void onClick(View view) {
        final MyAlertInputDialog myAlertInputDialog = new MyAlertInputDialog(MyStore.this).builder()
                .setTitle("请输入新的联系人")
                .setEditText("");
        myAlertInputDialog.setPositiveButton("确认", new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                TextView textView1=(TextView)findViewById(R.id.connectpeople);
                textView1.setText("联系人:"+myAlertInputDialog.getResult());
                myAlertInputDialog.dismiss();
            }
        }).setNegativeButton("取消", new View.OnClickListener() {
            @Override
            public void onClick(View v) {
//                        showMsg("取消");
                myAlertInputDialog.dismiss();
            }
        });
        myAlertInputDialog.show();
    }
});


        button1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                final MyAlertInputDialog myAlertInputDialog = new MyAlertInputDialog(MyStore.this).builder()
                        .setTitle("请输入新的手机号码")
                        .setEditText("");
                myAlertInputDialog.setPositiveButton("确认", new View.OnClickListener() {
                    @Override
                    public void onClick(View v) {
                        TextView textView1=(TextView)findViewById(R.id.shoouji);
                        textView1.setText("手机:"+myAlertInputDialog.getResult());
                        myAlertInputDialog.dismiss();
                    }
                }).setNegativeButton("取消", new View.OnClickListener() {
                    @Override
                    public void onClick(View v) {
//                        showMsg("取消");
                        myAlertInputDialog.dismiss();
                    }
                });
                myAlertInputDialog.show();
            }
        });
        button2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                final MyAlertInputDialog myAlertInputDialog = new MyAlertInputDialog(MyStore.this).builder()
                        .setTitle("请输入新的公司地址")
                        .setEditText("");
                myAlertInputDialog.setPositiveButton("确认", new View.OnClickListener() {
                    @Override
                    public void onClick(View v) {
                        TextView textView1=(TextView)findViewById(R.id.gongsiaddress);
                        textView1.setText("公司地址:"+myAlertInputDialog.getResult());
                        myAlertInputDialog.dismiss();
                    }
                }).setNegativeButton("取消", new View.OnClickListener() {
                    @Override
                    public void onClick(View v) {
//                        showMsg("取消");
                        myAlertInputDialog.dismiss();
                    }
                });
                myAlertInputDialog.show();
            }
        });
        button3.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                final MyAlertInputDialog myAlertInputDialog = new MyAlertInputDialog(MyStore.this).builder()
                        .setTitle("请输入新的公司/个人名称")
                        .setEditText("");
                myAlertInputDialog.setPositiveButton("确认", new View.OnClickListener() {
                    @Override
                    public void onClick(View v) {
                        TextView textView1=(TextView)findViewById(R.id.gongsigerenname);
                        textView1.setText("公司/个人名称:"+myAlertInputDialog.getResult());
                        myAlertInputDialog.dismiss();
                    }
                }).setNegativeButton("取消", new View.OnClickListener() {
                    @Override
                    public void onClick(View v) {
//                        showMsg("取消");
                        myAlertInputDialog.dismiss();
                    }
                });
                myAlertInputDialog.show();
            }
        });






        ImageButton imageButton1 = (ImageButton)findViewById(R.id.back);
    imageButton1.setOnClickListener(new View.OnClickListener() {
        @Override
        public void onClick(View v) {
finish();
        }
    });
        ImageButton imageButton2 =(ImageButton)findViewById(R.id.add);
        imageButton2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
Intent intent = new Intent(MyStore.this,PutProduct.class);
startActivity(intent);

            }
        });





    }
}

```

| 部件名称   | Putproduct      |
| ---------- | --------------- |
| 所属子系统 | 无              |
| 部件调用者 | Mystore         |
| 被调用者   | 无              |
| 入口参数   | Context context |
| 返回值     | 无              |

## 页面代码

```xml
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_height="wrap_content"
    android:layout_width="match_parent"
    android:orientation="vertical"
    android:divider="@drawable/line"
    android:showDividers="middle"
    >
<com.example.ebarter.Title_1Layout
    android:layout_height="wrap_content"
    android:layout_width="match_parent"
    />
    <LinearLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        >
    <ImageView
        android:layout_height="wrap_content"
        android:layout_width="wrap_content"
        android:src="@mipmap/e_product_category"
        android:layout_marginLeft="15dp"
        android:layout_marginTop="15dp"
        />
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:text="商品类别"
            android:textSize="17sp"
            android:layout_marginLeft="5dp"
            />
    <TextView
        android:layout_height="wrap_content"
        android:layout_width="wrap_content"
        android:layout_weight="1"

        />
<Button
    android:id="@+id/ImageTextButtton"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="请选择商品类别  "
    android:textSize="17sp"
    android:drawableRight="@mipmap/e_more"
    android:background="#ffffff"
    android:layout_marginRight="20dp"
    />
    </LinearLayout>
    <LinearLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_height="wrap_content"
        android:layout_width="match_parent"

        >
        <ImageView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:src="@mipmap/e_pricerange"
            android:layout_marginLeft="15dp"
            android:layout_marginTop="10dp"
            android:layout_marginBottom="10dp"
            />
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:text="商品价格"
            android:textSize="17sp"
            android:layout_marginLeft="5dp"
            android:layout_marginTop="8dp"
            />
        <TextView

            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_weight="1"
            />
        <EditText
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:hint="请输入商品价格"
            android:layout_marginRight="10dp"
            android:background="@drawable/none"
            android:layout_marginTop="10dp"

            />
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:text="巴特"
            android:textSize="15sp"
            android:textColor="#000000"
            android:layout_marginRight="15dp"
            android:layout_marginTop="10dp"
            />
    </LinearLayout>

        <TextView
            android:layout_height="wrap_content"
            android:layout_width="match_parent"
            android:text="上传商品图片（图片要求：400×400）"
            android:textSize="15sp"
            android:textStyle="bold"
            android:gravity="center"
            android:paddingTop="20dp"
            android:paddingBottom="20dp"
            />
        <ImageButton
            android:id="@+id/putonpic1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:src="@mipmap/e_upload_photo"
            android:layout_marginLeft="15dp"
            android:background="#ffffff"
            android:layout_marginBottom="20dp"
            android:layout_marginTop="20dp"
            />

    <LinearLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:orientation="horizontal"
        >
        <EditText
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:hint="商品名称"
            android:background="@drawable/none"

            android:layout_margin="15dp"
            />
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_weight="1"
        android:text=""
        />
        <com.example.ebarter.numchoose
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
android:layout_margin="15dp"
            />
    </LinearLayout>
    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="商品详细描述"
        android:layout_margin="15dp"
        android:background="@drawable/none"
        android:maxLines="2"
        />
    <TextView
    android:layout_height="wrap_content"
    android:layout_width="match_parent"
    android:text="上传商品介绍图片"
    android:textSize="15sp"
    android:textStyle="bold"
    android:gravity="center"
    android:paddingTop="20dp"
    android:paddingBottom="20dp"
    />
    <ImageButton
        android:id="@+id/putonpic2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:src="@mipmap/e_upload_photo"
        android:layout_marginLeft="15dp"
        android:background="#ffffff"
        android:layout_marginBottom="20dp"
        android:layout_marginTop="20dp"
        />
    <LinearLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:orientation="horizontal"
        >
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text=""
            />
        <Button
            android:id="@+id/lijifasong"
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:text="立即发送"
            android:textColor="#ffffff"
            android:textSize="15sp"
            android:layout_marginRight="5dp"
            android:background="@drawable/buttonshape"
            />
    </LinearLayout>
</LinearLayout>
```

| 部件名称   | Setting         |
| ---------- | --------------- |
| 所属子系统 | MeAtivity       |
| 部件调用者 | MeAtivity       |
| 被调用者   | clean_huancun   |
| 入口参数   | Context context |
| 返回值     | 无              |

## 部件逻辑代码

```java 
package com.example.ebarter;

import android.content.Intent;
import android.os.SystemClock;
import android.support.v7.app.ActionBar;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.util.Log;
import android.view.View;
import android.widget.TextView;
import android.widget.Toast;

import com.hb.dialog.dialog.LoadingDialog;

import static com.example.ebarter.Clean_huancun.clearAllCache;

public class Setting extends AppCompatActivity {
    //声明一个子线程

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_setting);
        ActionBar actionBar = getSupportActionBar();
        if(actionBar!=null){
            actionBar.hide();
        }
        TextView textView=(TextView)findViewById(R.id.titletext);
        textView.setText("设置");

        findViewById(R.id.setpassword).setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Toast.makeText(Setting.this,"设置密码",Toast.LENGTH_SHORT).show();
                Log.v("aaa","aaaaa");
                Intent intent=new Intent(Setting.this,FindpwdActivity.class);
                startActivity(intent);
            }
        });
        findViewById(R.id.clearbuffer).setOnClickListener(new View.OnClickListener() {
            private Thread newThread;

            @Override
            public void onClick(View view) {
                clearAllCache(getApplicationContext());
                LoadingDialog loadingDialog = new LoadingDialog(Setting.this);
                loadingDialog.setMessage("loading");
                loadingDialog.setCancelable(true);

                loadingDialog.show();

                Toast.makeText(Setting.this,"清除成功",Toast.LENGTH_LONG).show();
                //loadingDialog.dismiss();
                finish();


            }
        });
    }
}

```

| 部件名称   | clean_huancun   |
| ---------- | --------------- |
| 所属子系统 | Setting         |
| 部件调用者 | Setting         |
| 被调用者   | 无              |
| 入口参数   | Context context |
| 返回值     | 无              |

```java
package com.example.ebarter;

import android.content.Context;
import android.os.Environment;

import java.io.File;
import java.math.BigDecimal;

public class Clean_huancun {
    public static String getTotalCacheSize(Context context) throws Exception {
    long cacheSize = getFolderSize(context.getCacheDir());
    if (Environment.getExternalStorageState().equals(Environment.MEDIA_MOUNTED)) {
        cacheSize += getFolderSize(context.getExternalCacheDir());
    }
    return getFormatSize(cacheSize);
}

    /***
     * 清理所有缓存
     * @param context
     */
    public static void clearAllCache(Context context) {
        deleteDir(context.getCacheDir());
        if (Environment.getExternalStorageState().equals(Environment.MEDIA_MOUNTED)) {
            deleteDir(context.getExternalCacheDir());
        }
    }

    private static boolean deleteDir(File dir) {
        if (dir != null && dir.isDirectory()) {
            String[] children = dir.list();
            for (int i = 0; i < children.length; i++) {
                boolean success = deleteDir(new File(dir, children[i]));
                if (!success) {
                    return false;
                }
            }
        }
        return dir.delete();
    }

    // 获取文件
    //Context.getExternalFilesDir() --> SDCard/Android/data/你的应用的包名/files/ 目录，一般放一些长时间保存的数据
    //Context.getExternalCacheDir() --> SDCard/Android/data/你的应用包名/cache/目录，一般存放临时缓存数据
    public static long getFolderSize(File file) throws Exception {
        long size = 0;
        try {
            File[] fileList = file.listFiles();
            for (int i = 0; i < fileList.length; i++) {
                // 如果下面还有文件
                if (fileList[i].isDirectory()) {
                    size = size + getFolderSize(fileList[i]);
                } else {
                    size = size + fileList[i].length();
                }
            }
        } catch (Exception e) {
            e.printStackTrace();
        }
        return size;
    }

    /**
     * 格式化单位
     *
     * @param size
     * @return
     */
    public static String getFormatSize(double size) {
        double kiloByte = size / 1024;
        if (kiloByte < 1) {
//            return size + "Byte";
            return "0K";
        }

        double megaByte = kiloByte / 1024;
        if (megaByte < 1) {
            BigDecimal result1 = new BigDecimal(Double.toString(kiloByte));
            return result1.setScale(2, BigDecimal.ROUND_HALF_UP)
                    .toPlainString() + "KB";
        }

        double gigaByte = megaByte / 1024;
        if (gigaByte < 1) {
            BigDecimal result2 = new BigDecimal(Double.toString(megaByte));
            return result2.setScale(2, BigDecimal.ROUND_HALF_UP)
                    .toPlainString() + "MB";
        }

        double teraBytes = gigaByte / 1024;
        if (teraBytes < 1) {
            BigDecimal result3 = new BigDecimal(Double.toString(gigaByte));
            return result3.setScale(2, BigDecimal.ROUND_HALF_UP)
                    .toPlainString() + "GB";
        }
        BigDecimal result4 = new BigDecimal(teraBytes);
        return result4.setScale(2, BigDecimal.ROUND_HALF_UP).toPlainString()
                + "TB";
    }
}

```

| 部件名称   | collection_list |
| ---------- | --------------- |
| 所属子系统 | MeActivity      |
| 部件调用者 | MeActivity      |
| 被调用者   | 无              |
| 入口参数   | Context context |
| 返回值     | 无              |

## 部件逻辑代码

```java
package com.example.ebarter;

import android.content.Context;
import android.os.Environment;

import java.io.File;
import java.math.BigDecimal;

public class Clean_huancun {
    public static String getTotalCacheSize(Context context) throws Exception {
    long cacheSize = getFolderSize(context.getCacheDir());
    if (Environment.getExternalStorageState().equals(Environment.MEDIA_MOUNTED)) {
        cacheSize += getFolderSize(context.getExternalCacheDir());
    }
    return getFormatSize(cacheSize);
}

    /***
     * 清理所有缓存
     * @param context
     */
    public static void clearAllCache(Context context) {
        deleteDir(context.getCacheDir());
        if (Environment.getExternalStorageState().equals(Environment.MEDIA_MOUNTED)) {
            deleteDir(context.getExternalCacheDir());
        }
    }

    private static boolean deleteDir(File dir) {
        if (dir != null && dir.isDirectory()) {
            String[] children = dir.list();
            for (int i = 0; i < children.length; i++) {
                boolean success = deleteDir(new File(dir, children[i]));
                if (!success) {
                    return false;
                }
            }
        }
        return dir.delete();
    }

    // 获取文件
    //Context.getExternalFilesDir() --> SDCard/Android/data/你的应用的包名/files/ 目录，一般放一些长时间保存的数据
    //Context.getExternalCacheDir() --> SDCard/Android/data/你的应用包名/cache/目录，一般存放临时缓存数据
    public static long getFolderSize(File file) throws Exception {
        long size = 0;
        try {
            File[] fileList = file.listFiles();
            for (int i = 0; i < fileList.length; i++) {
                // 如果下面还有文件
                if (fileList[i].isDirectory()) {
                    size = size + getFolderSize(fileList[i]);
                } else {
                    size = size + fileList[i].length();
                }
            }
        } catch (Exception e) {
            e.printStackTrace();
        }
        return size;
    }

    /**
     * 格式化单位
     *
     * @param size
     * @return
     */
    public static String getFormatSize(double size) {
        double kiloByte = size / 1024;
        if (kiloByte < 1) {
//            return size + "Byte";
            return "0K";
        }

        double megaByte = kiloByte / 1024;
        if (megaByte < 1) {
            BigDecimal result1 = new BigDecimal(Double.toString(kiloByte));
            return result1.setScale(2, BigDecimal.ROUND_HALF_UP)
                    .toPlainString() + "KB";
        }

        double gigaByte = megaByte / 1024;
        if (gigaByte < 1) {
            BigDecimal result2 = new BigDecimal(Double.toString(megaByte));
            return result2.setScale(2, BigDecimal.ROUND_HALF_UP)
                    .toPlainString() + "MB";
        }

        double teraBytes = gigaByte / 1024;
        if (teraBytes < 1) {
            BigDecimal result3 = new BigDecimal(Double.toString(gigaByte));
            return result3.setScale(2, BigDecimal.ROUND_HALF_UP)
                    .toPlainString() + "GB";
        }
        BigDecimal result4 = new BigDecimal(teraBytes);
        return result4.setScale(2, BigDecimal.ROUND_HALF_UP).toPlainString()
                + "TB";
    }
}

```

| 部件名称   | UsualAddress    |
| ---------- | --------------- |
| 所属子系统 | MeActivity      |
| 部件调用者 | MeActivity      |
| 被调用者   | 无              |
| 入口参数   | Context context |
| 返回值     | 无              |

## 部件页面代码

```xml
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_height="match_parent"
    android:layout_width="match_parent"
    android:orientation="vertical"
    android:background="#E8E8E8"
    >
    <com.example.ebarter.Title_1Layout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        />
    <RelativeLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:background="#ffffff"
        android:id="@+id/clicksetaddress1"
        >
        <TextView
            android:id="@+id/dianjishezhichangyongdizhi1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="点击设置常用地址"
            android:padding="10dp"
            android:textColor="#3B3B3B"
            android:visibility="visible"
            />
        <TextView
            android:id="@+id/xingming1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text=""
            android:layout_below="@+id/dianjishezhichangyongdizhi1"
            android:paddingLeft="30dp"
            android:paddingRight="15dp"
            android:paddingTop="10dp"
            android:paddingBottom="10dp"

            />
        <TextView
            android:id="@+id/dianhua1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_below="@+id/xingming1"
            android:text=""
            android:paddingLeft="30dp"
            android:paddingRight="15dp"
            android:paddingTop="10dp"
            android:paddingBottom="10dp"

            />
        <TextView
            android:id="@+id/dizhi1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_below="@+id/dianhua1"
            android:text=""
            android:paddingLeft="30dp"
            android:paddingRight="15dp"
            android:paddingTop="10dp"
            android:paddingBottom="10dp"
            />



     <ImageView
         android:layout_width="wrap_content"
         android:layout_height="wrap_content"
         android:src="@mipmap/e_more"
         android:paddingTop="20dp"
         android:paddingBottom="20dp"
         android:layout_marginRight="20dp"
         android:layout_centerVertical="true"
         android:layout_alignParentRight="true"
         />
    </RelativeLayout>
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        >
        <View
            android:layout_height="0.5dp"
            android:layout_width="20dp"
            android:background="#ffffff"
            />
        <View
            android:layout_height="0.5dp"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:background="#666666"
            />
    </LinearLayout>
    <RelativeLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:background="#ffffff"
        android:id="@+id/clicksetaddress2"
        >
        <TextView
            android:id="@+id/dianjishezhichangyongdizhi2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="点击设置常用地址"
            android:padding="10dp"
            android:textColor="#3B3B3B"
            android:visibility="visible"

            />
        <TextView
            android:id="@+id/xingming2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text=""
            android:layout_below="@+id/dianjishezhichangyongdizhi2"
            android:paddingLeft="30dp"
            android:paddingRight="15dp"
            android:paddingTop="10dp"
            android:paddingBottom="10dp"

            />
        <TextView
            android:id="@+id/dianhua2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_below="@+id/xingming2"
            android:text=""
            android:paddingLeft="30dp"
            android:paddingRight="15dp"
            android:paddingTop="10dp"
            android:paddingBottom="10dp"

            />
        <TextView
            android:id="@+id/dizhi2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_below="@+id/dianhua2"
            android:text=""
            android:paddingLeft="30dp"
            android:paddingRight="15dp"
            android:paddingTop="10dp"
            android:paddingBottom="10dp"
            />



        <ImageView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:src="@mipmap/e_more"
            android:paddingTop="20dp"
            android:paddingBottom="20dp"
            android:layout_marginRight="20dp"
            android:layout_centerVertical="true"
            android:layout_alignParentRight="true"
            />
    </RelativeLayout>
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        >
        <View
            android:layout_height="0.5dp"
            android:layout_width="20dp"
            android:background="#ffffff"
            />
        <View
            android:layout_height="0.5dp"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:background="#666666"
            />
    </LinearLayout>

    <RelativeLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_height="wrap_content"
        android:layout_width="match_parent"
        android:background="#ffffff"
        android:id="@+id/clicksetaddress3"
        >
        <TextView
            android:id="@+id/dianjishezhichangyongdizhi3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="点击设置常用地址"
            android:padding="10dp"
            android:textColor="#3B3B3B"
            android:visibility="visible"

            />
        <TextView
            android:id="@+id/xingming3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text=""
            android:layout_below="@+id/dianjishezhichangyongdizhi3"
            android:paddingLeft="30dp"
            android:paddingRight="15dp"
            android:paddingTop="10dp"
            android:paddingBottom="10dp"

            />
        <TextView
            android:id="@+id/dianhua3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_below="@+id/xingming3"
            android:text=""
            android:paddingLeft="30dp"
            android:paddingRight="15dp"
            android:paddingTop="10dp"
            android:paddingBottom="10dp"

            />
        <TextView
            android:id="@+id/dizhi3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_below="@+id/dianhua3"
            android:text=""
            android:paddingLeft="30dp"
            android:paddingRight="15dp"
            android:paddingTop="10dp"
            android:paddingBottom="10dp"
            />



        <ImageView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:src="@mipmap/e_more"
            android:paddingTop="20dp"
            android:paddingBottom="20dp"
            android:layout_marginRight="20dp"
            android:layout_centerVertical="true"
            android:layout_alignParentRight="true"
            />
    </RelativeLayout>
</LinearLayout>



```

### 部件逻辑代码

``` java
package com.example.ebarter;

import android.content.Intent;
import android.support.annotation.Nullable;
import android.support.v7.app.ActionBar;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.util.Log;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;
import android.widget.Toast;

import com.hb.dialog.dialog.ConfirmDialog;

public class UsualAddress extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_usual_address);
        ActionBar actionBar = getSupportActionBar();
        if(actionBar!=null){
            actionBar.hide();
        }
        final TextView textView=(TextView)findViewById(R.id.titletext);
        textView.setText("常用地址");
        Button button=(Button)findViewById(R.id.clean);
        button.setVisibility(View.VISIBLE);
        findViewById(R.id.clean).setOnClickListener(new View.OnClickListener() {


    @Override
    public void onClick(View view) {
        ConfirmDialog confirmDialog = new ConfirmDialog(UsualAddress.this);
        confirmDialog.setLogoImg(R.mipmap.dialog_notice).setMsg("确定清空？");
        confirmDialog.setClickListener(new ConfirmDialog.OnBtnClickListener() {
            @Override
            public void ok() {
                TextView textView1=(TextView)findViewById(R.id.dianjishezhichangyongdizhi1);
                TextView textView2=(TextView)findViewById(R.id.xingming1);
                TextView textView3=(TextView)findViewById(R.id.dianhua1);
                TextView textView4=(TextView)findViewById(R.id.dizhi1);
                TextView textView11=(TextView)findViewById(R.id.dianjishezhichangyongdizhi2);
                TextView textView22=(TextView)findViewById(R.id.xingming2);
                TextView textView33=(TextView)findViewById(R.id.dianhua2);
                TextView textView44=(TextView)findViewById(R.id.dizhi2);
                TextView textView111=(TextView)findViewById(R.id.dianjishezhichangyongdizhi3);
                TextView textView222=(TextView)findViewById(R.id.xingming3);
                TextView textView333=(TextView)findViewById(R.id.dianhua3);
                TextView textView444=(TextView)findViewById(R.id.dizhi3);
                textView1.setVisibility(View.VISIBLE);
                textView11.setVisibility(View.VISIBLE);
                textView111.setVisibility(View.VISIBLE);
textView2.setText("");
textView3.setText("");
textView4.setText("");
textView22.setText("");
textView33.setText("");
textView44.setText("");
textView222.setText("");
textView333.setText("");
textView444.setText("");

            }

            @Override
            public void cancel() {

            }
        });
        confirmDialog.show();
    }
});
        findViewById(R.id.clicksetaddress1).setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Toast.makeText(UsualAddress.this,"点击设置常用地址",Toast.LENGTH_SHORT).show();
                Intent intent = new Intent(UsualAddress.this,Set_Store_information.class);
                intent.putExtra("id","1");
                 int a = 0;
                startActivityForResult(intent,a);


            }
        });
        findViewById(R.id.clicksetaddress2).setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Toast.makeText(UsualAddress.this,"点击设置常用地址",Toast.LENGTH_SHORT).show();
                Intent intent = new Intent(UsualAddress.this,Set_Store_information.class);
                intent.putExtra("id","2");
                int a = 0;
                startActivityForResult(intent,a);

            }
        });
        findViewById(R.id.clicksetaddress3).setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Toast.makeText(UsualAddress.this,"点击设置常用地址",Toast.LENGTH_SHORT).show();
                Intent intent = new Intent(UsualAddress.this,Set_Store_information.class);
                intent.putExtra("id","3");
                int a = 0;
                startActivityForResult(intent,a);
            }
        });


    }

    @Override
    protected void onActivityResult(int requestCode, int resultCode, @Nullable Intent data) {
        super.onActivityResult(requestCode, resultCode, data);
     if(resultCode==1){
         TextView textView1=(TextView)findViewById(R.id.dianjishezhichangyongdizhi1);
         TextView textView2=(TextView)findViewById(R.id.xingming1);
         TextView textView3=(TextView)findViewById(R.id.dianhua1);
         TextView textView4=(TextView)findViewById(R.id.dizhi1);
         textView1.setVisibility(View.GONE);
         String a=data.getExtras().getString("name");
         String b=data.getExtras().getString("phonenum");
         String c=data.getExtras().getString("address");
         textView2.setText("姓名： "+a);
         textView3.setText("电话： "+b);
         textView4.setText("地址： "+c);
     }
     if(resultCode==2){
         TextView textView1=(TextView)findViewById(R.id.dianjishezhichangyongdizhi2);
         TextView textView2=(TextView)findViewById(R.id.xingming2);
         TextView textView3=(TextView)findViewById(R.id.dianhua2);
         TextView textView4=(TextView)findViewById(R.id.dizhi2);
         textView1.setVisibility(View.GONE);
         String a=data.getExtras().getString("name");
         String b=data.getExtras().getString("phonenum");
         String c=data.getExtras().getString("address");
         textView2.setText("姓名： "+a);
         textView3.setText("电话： "+b);
         textView4.setText("地址： "+c);
     }
     if(resultCode==3){
         TextView textView1=(TextView)findViewById(R.id.dianjishezhichangyongdizhi3);
         TextView textView2=(TextView)findViewById(R.id.xingming3);
         TextView textView3=(TextView)findViewById(R.id.dianhua3);
         TextView textView4=(TextView)findViewById(R.id.dizhi3);
         textView1.setVisibility(View.GONE);
         String a=data.getExtras().getString("name");
         String b=data.getExtras().getString("phonenum");
         String c=data.getExtras().getString("address");
         textView2.setText("姓名： "+a);
         textView3.setText("电话： "+b);
         textView4.setText("地址： "+c);
     }

    }

}

```

| 部件名称   | LoginActivity                                                |
| ---------- | ------------------------------------------------------------ |
| 所属子系统 | 无                                                           |
| 部件调用者 | 登录界面                                                     |
| 被调用者   | `null` |
| 入口参数   | 无                                                           |
| 返回值     | 无                                                           |

### 部件截图：

![ava](https://github.com/daxuliu/markdown/raw/master/login.png)





### 部件逻辑代码

```java
package com.example.ebarter;

import android.animation.Animator;
import android.animation.AnimatorListenerAdapter;
import android.annotation.TargetApi;
import android.app.LoaderManager.LoaderCallbacks;
import android.content.CursorLoader;
import android.content.Intent;
import android.content.Loader;
import android.content.SharedPreferences;
import android.content.pm.PackageManager;
import android.database.Cursor;
import android.net.Uri;
import android.os.AsyncTask;
import android.os.Build;
import android.os.Bundle;
import android.os.Handler;
import android.os.Message;
import android.provider.ContactsContract;
import android.support.annotation.NonNull;
import android.support.design.widget.Snackbar;
import android.support.v7.app.ActionBar;
import android.support.v7.app.AppCompatActivity;
import android.text.TextUtils;
import android.view.KeyEvent;
import android.view.View;
import android.view.View.OnClickListener;
import android.view.inputmethod.EditorInfo;
import android.widget.ArrayAdapter;
import android.widget.AutoCompleteTextView;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import android.widget.Toast;

import com.example.ebarter.tools.Plisttool;
import com.example.ebarter.tools.Producttool;
import com.hjq.bar.OnTitleBarListener;
import com.hjq.bar.TitleBar;

import org.json.JSONObject;

import java.util.ArrayList;
import java.util.List;

import static android.Manifest.permission.READ_CONTACTS;

/**
 * A login screen that offers login via email/password.
 */
public class LoginActivity extends AppCompatActivity implements LoaderCallbacks<Cursor> {

    /**
     * Id to identity READ_CONTACTS permission request.
     */
    private static final int REQUEST_READ_CONTACTS = 0;

    /**
     * A dummy authentication store containing known user names and passwords.
     * TODO: remove after connecting to a real authentication system.
     */
    private static final String[] DUMMY_CREDENTIALS = new String[]{
            "foo@example.com:hello", "bar@example.com:world"
    };
    /**
     * Keep track of the login task to ensure we can cancel it if requested.
     */
    private UserLoginTask mAuthTask = null;
    private String spname;
    private String sppassword;
    private Okhttptest okhttptest;
    // UI references.
    private AutoCompleteTextView mEmailView;
    private EditText mPasswordView;
    private View mProgressView;
    private View mLoginFormView;
    private ActionBar actionBar;
    private TitleBar mTitleBar;
    private Button mEmailSignInButton;
    private String response;
    private String status;
    private String sessionId, overname, overpass;
    private Handler handler1;
    private Handler handler_info;
    private Handler handler_EbarterAcct;
    private Handler handler_Productlist;

    {
        handler_info = new Handler() {
            @Override
            public void handleMessage(Message msg) {
                super.handleMessage(msg);
                switch (msg.what) {
                    case 0:

                        String responseinfo = (String) msg.obj;
                        try {

                            JSONObject jb = new JSONObject(responseinfo);
                            String token = jb.getJSONObject("user").getString("Token");
                            DataManager dataManager = DataManager.getInstance();
                            dataManager.getInfoMap().put("inforjb", jb);
                            Intent intent = new Intent(LoginActivity.this, chatlist.class);
                            intent.putExtra("token", token);
                            startActivity(intent);
                            LoginActivity.this.finish();

                            //status = response.substring((response.indexOf(":")+3) , (response.indexOf(",")-1));
                            //sessionId = response.substring((response.indexOf("sessionId")+13) , (response.indexOf(",",response.indexOf("sessionId"))-1));
                            //Toast toast_status = Toast.makeText(LoginActivity.this, "这是status" + status, Toast.LENGTH_SHORT);
                            //toast_status.show();
                        } catch (Exception e) {
                        }
                        break;
                    default:
                        break;

                }
            }
        };

    }

    {
        handler1 = new Handler() {
            @Override
            public void handleMessage(Message msg) {
                super.handleMessage(msg);
                switch (msg.what) {
                    case 0:
                        response = (String) msg.obj;
                        try {
                            String string_name = mEmailView.getText().toString();


                            JSONObject jb = new JSONObject(response);
                            String status = jb.getString("status");
                            sessionId = jb.getString("sessionId");
                            DataManager dataManager = DataManager.getInstance();
                            dataManager.getInfoMap().put("log", jb);
                            SharedPreferences sp = getSharedPreferences("sp_file", MODE_PRIVATE);
                            String name = sp.getString("name", "shibai");
                            String password = sp.getString("password", "shibai");
                            if (status.equals("ALREADY_LOGGED_ON")) {
                                Toast toast = Toast.makeText(LoginActivity.this, "登录成功！正在加载数据！", Toast.LENGTH_SHORT);
                                toast.show();
                                sendRequestWithHttpClientinfo();  //获取个人信息
                                sendRequestWithHttpClientEbarterAcct();  //获取巴特币余额
                                sendRequestWithHttpClientProductlist();  //获取商品列表
                                Plisttool plisttool = new Plisttool();//获取备忘录信息
                                plisttool.getNewsInfo("https://s3.cn-north-1.amazonaws.com.cn/linda-trades-archive-1/" +
                                        string_name +
                                        "-MyMemorandum112.plist");
                            } else {
                                Toast toast = Toast.makeText(LoginActivity.this, "账号或者密码错误", Toast.LENGTH_SHORT);
                                toast.show();
                            }
                        } catch (Exception e) {
                        }
                        break;
                    default:
                        break;
                }
            }
        };
    }


    {
        handler_EbarterAcct = new Handler() {
            @Override
            public void handleMessage(Message msg) {
                super.handleMessage(msg);
                switch (msg.what) {
                    case 0:
                        response = (String) msg.obj;
                        try {
                            JSONObject jb_EA = new JSONObject(response);
                            DataManager dataManager = DataManager.getInstance();
                            dataManager.getInfoMap().put("EbarterAcct_jb", jb_EA);
                        } catch (Exception e) {
                        }
                        break;
                    default:
                        break;
                }
            }
        };
    }

    {
        handler_Productlist = new Handler() {
            @Override
            public void handleMessage(Message msg) {
                super.handleMessage(msg);
                switch (msg.what) {
                    case 0:
                        response = (String) msg.obj;
                        try {
                            JSONObject jb_PL = new JSONObject(response);
                            Producttool producttool = new Producttool(jb_PL);
                            producttool.getProList();
                            DataManager dataManager = DataManager.getInstance();
                            dataManager.getInfoMap().put("arrofpro", producttool.getProList());
                        } catch (Exception e) {
                        }
                        break;
                    default:
                        break;
                }
            }
        };
    }

    /*private String  getinfor(String sessionId){
        String url="";
        String json="";
        okhttptest.Getinfor(url,json);
    }*/
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_login);
        actionBar = getSupportActionBar();
        actionBar.hide();
        mTitleBar = (TitleBar) findViewById(R.id.tb_main_title_bar);
        mTitleBar.setBackgroundColor(0xffcd3333);
        mTitleBar.setOnTitleBarListener(new OnTitleBarListener() {
            @Override
            public void onLeftClick(View v) {
                Intent i = new Intent(LoginActivity.this, Login_reg.class);
                startActivity(i);
            }

            @Override
            public void onTitleClick(View v) {
            }

            @Override
            public void onRightClick(View v) {
            }
        });
        // Set up the login form.
        okhttptest = new Okhttptest();
        SharedPreferences sp = getSharedPreferences("sp_file", MODE_PRIVATE);
        spname = sp.getString("name", "");
        sppassword = sp.getString("password", "");
        if (spname.equals("") == false && sppassword.equals("") == false) {
            overname = spname;
            overpass = sppassword;
            sendRequestWithHttpClient_login();

        }
        mEmailView = (AutoCompleteTextView) findViewById(R.id.ETxt_username);
        populateAutoComplete();
        mPasswordView = (EditText) findViewById(R.id.ETxt_password);
        mPasswordView.setOnEditorActionListener(new TextView.OnEditorActionListener() {
            @Override
            public boolean onEditorAction(TextView textView, int id, KeyEvent keyEvent) {
                if (id == EditorInfo.IME_ACTION_DONE || id == EditorInfo.IME_NULL) {
                    attemptLogin();
                    return true;
                }
                return false;
            }
        });
        //   String string_name = mEmailView.
        // String string_pwd = mPasswordView.getText().toString();
        DataManager dataManager = DataManager.getInstance();
        String username = "";
        String password = "";
        username = (String) dataManager.getInfoMap().get("username");
        password = (String) dataManager.getInfoMap().get("password");
        mEmailView.setText(username);
        mPasswordView.setText(password);
        // 点击 “遇到困难？” 实现页面跳转
        Button btn1 = (Button) findViewById(R.id.btn_problem);
        btn1.setOnClickListener(new OnClickListener() {
            public void onClick(View v) {
                Intent i = new Intent(LoginActivity.this, FindpwdActivity.class);
                startActivity(i);
            }
        });

        mEmailSignInButton = (Button) findViewById(R.id.btn_login);
        mEmailSignInButton.setOnClickListener(new OnClickListener() {
            @Override
            public void onClick(View view) {
                Toast toast = Toast.makeText(LoginActivity.this, "正在登录", Toast.LENGTH_SHORT);
                toast.show();
                sendRequestWithHttpClient();

            }
        });

        mLoginFormView = findViewById(R.id.login_form);
        mProgressView = findViewById(R.id.login_progress);
    }

    private void populateAutoComplete() {
        if (!mayRequestContacts()) {
            return;
        }

        getLoaderManager().initLoader(0, null, this);
    }

    private boolean mayRequestContacts() {
        if (Build.VERSION.SDK_INT < Build.VERSION_CODES.M) {
            return true;
        }
        if (checkSelfPermission(READ_CONTACTS) == PackageManager.PERMISSION_GRANTED) {
            return true;
        }
        if (shouldShowRequestPermissionRationale(READ_CONTACTS)) {
            Snackbar.make(mEmailView, R.string.permission_rationale, Snackbar.LENGTH_INDEFINITE)
                    .setAction(android.R.string.ok, new OnClickListener() {
                        @Override
                        @TargetApi(Build.VERSION_CODES.M)
                        public void onClick(View v) {
                            requestPermissions(new String[]{READ_CONTACTS}, REQUEST_READ_CONTACTS);
                        }
                    });
        } else {
            requestPermissions(new String[]{READ_CONTACTS}, REQUEST_READ_CONTACTS);
        }
        return false;
    }


    @Override
    public void onRequestPermissionsResult(int requestCode, @NonNull String[] permissions,
                                           @NonNull int[] grantResults) {
        if (requestCode == REQUEST_READ_CONTACTS) {
            if (grantResults.length == 1 && grantResults[0] == PackageManager.PERMISSION_GRANTED) {
                populateAutoComplete();
            }
        }
    }

    private void attemptLogin() {
        if (mAuthTask != null) {
            return;
        }

        // Reset errors.
        mEmailView.setError(null);
        mPasswordView.setError(null);

        // Store values at the time of the login attempt.
        String email = mEmailView.getText().toString();
        String password = mPasswordView.getText().toString();

        boolean cancel = false;
        View focusView = null;

        // Check for a valid password, if the user entered one.
        if (!TextUtils.isEmpty(password) && !isPasswordValid(password)) {
            mPasswordView.setError(getString(R.string.error_invalid_password));
            focusView = mPasswordView;
            cancel = true;
        }

        // Check for a valid email address.
        if (TextUtils.isEmpty(email)) {
            mEmailView.setError(getString(R.string.error_field_required));
            focusView = mEmailView;
            cancel = true;
        } else if (!isEmailValid(email)) {
            mEmailView.setError(getString(R.string.error_invalid_email));
            focusView = mEmailView;
            cancel = true;
        }

        if (cancel) {
            // There was an error; don't attempt login and focus the first
            // form field with an error.
            focusView.requestFocus();
        } else {
            // Show a progress spinner, and kick off a background task to
            // perform the user login attempt.
            showProgress(true);
            mAuthTask = new UserLoginTask(email, password);
            mAuthTask.execute((Void) null);
        }
    }

    private boolean isEmailValid(String email) {
        //TODO: Replace this with your own logic
        return true;
    }

    private boolean isPasswordValid(String password) {
        //TODO: Replace this with your own logic
        return password.length() > 4;
    }

    @TargetApi(Build.VERSION_CODES.HONEYCOMB_MR2)
    private void showProgress(final boolean show) {
        // On Honeycomb MR2 we have the ViewPropertyAnimator APIs, which allow
        // for very easy animations. If available, use these APIs to fade-in
        // the progress spinner.
        if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.HONEYCOMB_MR2) {
            int shortAnimTime = getResources().getInteger(android.R.integer.config_shortAnimTime);

            mLoginFormView.setVisibility(show ? View.GONE : View.VISIBLE);
            mLoginFormView.animate().setDuration(shortAnimTime).alpha(
                    show ? 0 : 1).setListener(new AnimatorListenerAdapter() {
                @Override
                public void onAnimationEnd(Animator animation) {
                    mLoginFormView.setVisibility(show ? View.GONE : View.VISIBLE);
                }
            });

            mProgressView.setVisibility(show ? View.VISIBLE : View.GONE);
            mProgressView.animate().setDuration(shortAnimTime).alpha(
                    show ? 1 : 0).setListener(new AnimatorListenerAdapter() {
                @Override
                public void onAnimationEnd(Animator animation) {
                    mProgressView.setVisibility(show ? View.VISIBLE : View.GONE);
                }
            });
        } else {
            // The ViewPropertyAnimator APIs are not available, so simply show
            // and hide the relevant UI components.
            mProgressView.setVisibility(show ? View.VISIBLE : View.GONE);
            mLoginFormView.setVisibility(show ? View.GONE : View.VISIBLE);
        }
    }

    @Override
    public Loader<Cursor> onCreateLoader(int i, Bundle bundle) {
        return new CursorLoader(this,
                // Retrieve data rows for the device user's 'profile' contact.
                Uri.withAppendedPath(ContactsContract.Profile.CONTENT_URI,
                        ContactsContract.Contacts.Data.CONTENT_DIRECTORY), ProfileQuery.PROJECTION,

                // Select only email addresses.
                ContactsContract.Contacts.Data.MIMETYPE +
                        " = ?", new String[]{ContactsContract.CommonDataKinds.Email
                .CONTENT_ITEM_TYPE},

                // Show primary email addresses first. Note that there won't be
                // a primary email address if the user hasn't specified one.
                ContactsContract.Contacts.Data.IS_PRIMARY + " DESC");
    }

    @Override
    public void onLoadFinished(Loader<Cursor> cursorLoader, Cursor cursor) {
        List<String> emails = new ArrayList<>();
        cursor.moveToFirst();
        while (!cursor.isAfterLast()) {
            emails.add(cursor.getString(ProfileQuery.ADDRESS));
            cursor.moveToNext();
        }

        addEmailsToAutoComplete(emails);
    }

    @Override
    public void onLoaderReset(Loader<Cursor> cursorLoader) {

    }

    private void addEmailsToAutoComplete(List<String> emailAddressCollection) {
        //Create adapter to tell the AutoCompleteTextView what to show in its dropdown list.
        ArrayAdapter<String> adapter =
                new ArrayAdapter<>(LoginActivity.this,
                        android.R.layout.simple_dropdown_item_1line, emailAddressCollection);

        mEmailView.setAdapter(adapter);
    }

    private interface ProfileQuery {
        String[] PROJECTION = {
                ContactsContract.CommonDataKinds.Email.ADDRESS,
                ContactsContract.CommonDataKinds.Email.IS_PRIMARY,
        };

        int ADDRESS = 0;
        int IS_PRIMARY = 1;
    }

    public class UserLoginTask extends AsyncTask<Void, Void, Boolean> {

        private final String mEmail;
        private final String mPassword;

        UserLoginTask(String email, String password) {
            mEmail = email;
            mPassword = password;
        }

        @Override
        protected Boolean doInBackground(Void... params) {
            // TODO: attempt authentication against a network service.

            try {
                // Simulate network access.
                Thread.sleep(2000);
            } catch (InterruptedException e) {
                return false;
            }

            for (String credential : DUMMY_CREDENTIALS) {
                String[] pieces = credential.split(":");
                if (pieces[0].equals(mEmail)) {
                    // Account exists, return true if the password matches.
                    return pieces[1].equals(mPassword);
                }
            }

            // TODO: register the new account here.
            return true;
        }

        @Override
        protected void onPostExecute(final Boolean success) {
            mAuthTask = null;
            showProgress(false);

            if (success) {
                finish();
            } else {
                mPasswordView.setError(getString(R.string.error_incorrect_password));
                mPasswordView.requestFocus();
            }
        }

        @Override
        protected void onCancelled() {
            mAuthTask = null;
            showProgress(false);
        }
    }

    //获取个人信息请求
    private void sendRequestWithHttpClientinfo() {
        new Thread(new Runnable() {
            @Override
            public void run() {
                try {
//                    String string_name = mEmailView.getText().toString();
//                    String string_pwd = mPasswordView.getText().toString();
//                    string_pwd = okhttptest.md5Decode32(string_pwd);
                    String url = "http://ebarter-env.cn-north-1.eb.amazonaws.com.cn/JSONServlet";
                    String json = "{'m_status':'QUERY','m_appName':'ebartercny','m_acct':'" +
                            overname +
                            "','" +
                            sessionId +
                            "':'" +
                            "test-1572946090976-5-1289891401" +
                            "','hasToken':false,'forRcloud':false}";
                    Message message = new Message();
                    message.what = 0;
                    message.obj = okhttptest.Getinfor(url, json);
                    handler_info.sendMessage(message);
                } catch (Exception e) {
                    // TODO Auto-generated catch block
                    e.printStackTrace();
                }
            }
        }).start();//这个start()方法不要忘记了
    }

    //用户登录请求
    private void sendRequestWithHttpClient() {
        new Thread(new Runnable() {
            @Override
            public void run() {
                try {
                    SharedPreferences password_name_preferences = getSharedPreferences("sp_file", MODE_PRIVATE);
                    SharedPreferences.Editor editor = password_name_preferences.edit();
//                    用户名和密码持久化

                    String string_name = mEmailView.getText().toString();
                    String string_pwd = mPasswordView.getText().toString();
                    string_pwd = okhttptest.md5Decode32(string_pwd);
                    editor.putString("name", string_name);
                    editor.putString("password", string_pwd);
                    editor.commit();
                    overname = string_name;
                    overpass = string_pwd;
                    String url = "http://ebarter-env.cn-north-1.eb.amazonaws.com.cn/JSONServlet";
                    String json = "{'appName': 'ebartercny'," +
                            " 'm_ScConfig': {'m_deviceId': '88EF6CAE-5670-42EB-87BA-0AD0478025E1', 'm_appDate': 1572160704, 'm_appName': 'ebartercny'}," +
                            " 'm_platform': 'BAIDU'," +
                            " 'm_deviceId': '88EF6CAE-5670-42EB-87BA-0AD0478025E1'," +
                            " 'm_surveySex': False," +
                            " 'm_languageIndex': 1," +
                            " 'm_surveyName': 'shenyang'," +
                            " 'ecryptPwd': '" +
                            string_pwd +
                            "'," +
                            " 'scAcct': '" +
                            string_name +
                            "'}";
                    String response = okhttptest.Login(url, json);
                    Message message = new Message();
                    message.what = 0;
                    message.obj = response;
                    handler1.sendMessage(message);
                } catch (Exception e) {
                    // TODO Auto-generated catch block
                    e.printStackTrace();
                }
            }
        }).start();//这个start()方法不要忘记了
    }

    private void sendRequestWithHttpClient_login() {
        new Thread(new Runnable() {
            @Override
            public void run() {
                try {


                    String url = "http://ebarter-env.cn-north-1.eb.amazonaws.com.cn/JSONServlet";
                    String json = "{'appName': 'ebartercny'," +
                            " 'm_ScConfig': {'m_deviceId': '88EF6CAE-5670-42EB-87BA-0AD0478025E1', 'm_appDate': 1572160704, 'm_appName': 'ebartercny'}," +
                            " 'm_platform': 'BAIDU'," +
                            " 'm_deviceId': '88EF6CAE-5670-42EB-87BA-0AD0478025E1'," +
                            " 'm_surveySex': False," +
                            " 'm_languageIndex': 1," +
                            " 'm_surveyName': 'shenyang'," +
                            " 'ecryptPwd': '" +
                            sppassword +
                            "'," +
                            " 'scAcct': '" +
                            spname +
                            "'}";
                    String response = okhttptest.Login(url, json);
                    Message message = new Message();
                    message.what = 0;
                    message.obj = response;
                    handler1.sendMessage(message);
                } catch (Exception e) {
                    // TODO Auto-generated catch block
                    e.printStackTrace();
                }
            }
        }).start();//这个start()方法不要忘记了
    }

    //查询巴特币余额请求
    private void sendRequestWithHttpClientEbarterAcct() {
        new Thread(new Runnable() {
            @Override
            public void run() {
                try {
//                    String string_name = mEmailView.getText().toString();
                    String url = "http://ebarter-env.cn-north-1.eb.amazonaws.com.cn/JSONServlet";
                    String json = "{'Acct':'" +
                            overname +
                            "'}";
                    Message message = new Message();
                    message.what = 0;
                    message.obj = okhttptest.EbarterAcct(url, json);
                    handler_EbarterAcct.sendMessage(message);
                } catch (Exception e) {
                    // TODO Auto-generated catch block
                    e.printStackTrace();
                }
            }
        }).start();//这个start()方法不要忘记了
    }

    //查询商品列表
    private void sendRequestWithHttpClientProductlist() {
        new Thread(new Runnable() {
            @Override
            public void run() {
                try {
                    String url = "http://ebarter-env.cn-north-1.eb.amazonaws.com.cn/JSONServlet";
                    String json = "{'acct':'test','contant':'','type':'product'}";
                    Message message = new Message();
                    message.what = 0;
                    message.obj = okhttptest.Productlist(url, json);
                    handler_Productlist.sendMessage(message);
                } catch (Exception e) {
                    // TODO Auto-generated catch block
                    e.printStackTrace();
                }
            }
        }).start();//这个start()方法不要忘记了
    }
}


```

### 部件页面代码

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:gravity="center_horizontal"
    android:orientation="vertical"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    tools:context=".LoginActivity">

    <!-- Login progress -->
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:orientation="vertical">
        <com.hjq.bar.TitleBar
            android:id="@+id/tb_main_title_bar"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginTop="0dp"


            app:rightTitle="微信登录"
            app:title="登录" />
        <ProgressBar
        android:id="@+id/login_progress"
        style="?android:attr/progressBarStyleLarge"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="8dp"
        android:visibility="gone" />

    <ScrollView
        android:id="@+id/login_form"
        android:layout_width="match_parent"
        android:layout_height="match_parent">

        <LinearLayout
            android:id="@+id/email_login_form"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="vertical">

            <android.support.design.widget.TextInputLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content">
                <LinearLayout
                    android:id="@+id/username"
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content">

                    <ImageView
                        android:layout_width="21dp"
                        android:layout_height="26dp"
                        android:layout_gravity="center"
                        android:src="@drawable/username" />
                    <TextView
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:text="账户 "
                        android:textColor="#000000"
                        android:textSize="20sp"/>
                    <View
                        android:layout_width="1dp"
                        android:layout_height="25dp"
                        android:layout_gravity="center"
                        android:background="#000000"/>

                    <AutoCompleteTextView
                        android:id="@+id/ETxt_username"
                        android:layout_width="match_parent"
                        android:layout_height="wrap_content"
                        android:hint="请输入用户名"
                        android:inputType="textEmailAddress"
                        android:maxLines="1"
                        android:singleLine="true" />
                </LinearLayout>
            </android.support.design.widget.TextInputLayout>

            <android.support.design.widget.TextInputLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content">
                <LinearLayout
                    android:id="@+id/pwd"
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal">
                    <ImageView
                        android:layout_width="21dp"
                        android:layout_height="26dp"
                        android:layout_gravity="center"
                        android:src="@drawable/pwd"/>
                    <TextView
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:text="密码 "
                        android:textColor="#000000"
                        android:textSize="20sp"/>
                    <View
                        android:layout_width="1dp"
                        android:layout_height="25dp"
                        android:layout_gravity="center"
                        android:background="#000000"  />

                    <EditText
                        android:id="@+id/ETxt_password"
                        android:layout_width="match_parent"
                        android:layout_height="wrap_content"
                        android:hint="请输入密码"
                        android:imeActionId="6"
                        android:imeActionLabel="@string/action_sign_in_short"
                        android:imeOptions="actionUnspecified"
                        android:inputType="textPassword"
                        android:maxLines="1"
                        android:singleLine="true" />
                </LinearLayout>
            </android.support.design.widget.TextInputLayout>

            <Button
                android:id="@+id/btn_login"
                style="?android:textAppearanceSmall"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_marginTop="16dp"
                android:text="登录"
                android:textColor="#FFFFFF"
                android:background="#CD0000"
                android:textStyle="bold" />
            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:gravity="right">

                <Button
                    android:id="@+id/btn_problem"
                    android:layout_width="wrap_content"
                    android:layout_height="wrap_content"
                    android:text="遇到困难？"
                    android:textColor="#EE0000"
                    android:background="#FFFFFF"/>
            </LinearLayout>


        </LinearLayout>
    </ScrollView>
    </LinearLayout>

```

| 部件名称   | RegisterActivity |
| ---------- | ---------------- |
| 所属子系统 | 无               |
| 部件调用者 | 注册界面         |
| 被调用者   | `null`           |
| 入口参数   | 无               |
| 返回值     | 无               |
![](https://github.com/daxuliu/markdown/raw/master/reg.png)
### 逻辑代码

```java
package com.example.ebarter;

import android.content.DialogInterface;
import android.content.Intent;
import android.os.Bundle;
import android.os.Handler;
import android.os.Message;
import android.support.v7.app.ActionBar;
import android.support.v7.app.AlertDialog;
import android.support.v7.app.AppCompatActivity;
import android.text.SpannableString;
import android.util.Log;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;

import com.hjq.bar.OnTitleBarListener;
import com.hjq.bar.TitleBar;

import org.json.JSONObject;


import cn.smssdk.EventHandler;
import cn.smssdk.SMSSDK;

public class RegisterActivity extends AppCompatActivity {
    private AlertDialog alertDialog1;

    private Button button1;
    private  Button getcode;

    private ActionBar actionBar;
    private TitleBar mTitleBar;

    private Okhttptest okhttptest;

    private EditText username,code;
    private EditText password;
    private EditText tel;

    private Button Btnreg;

    private Handler handler;
    {
        handler = new Handler() {
            @Override
            public void handleMessage(Message msg) {
                super.handleMessage(msg);
                switch (msg.what) {
                    case 0:
                        String response = (String) msg.obj;
                        try {
                            JSONObject jb = new JSONObject(response);
                            String status=jb.getString("m_status");
                            DataManager dataManager=DataManager.getInstance();
                            dataManager.getInfoMap().put("regjb",jb);
                            username = (EditText)findViewById(R.id.register_username);
                            password = (EditText)findViewById(R.id.register_pwd);
                            dataManager.getInfoMap().put("username",username.getText().toString());
                            dataManager.getInfoMap().put("password",password.getText().toString());
                            if(status.equals("APPROVED")){
                            Toast toast = Toast.makeText(RegisterActivity.this, "注册成功！请登录！", Toast.LENGTH_SHORT);
                            toast.show();

                            Intent intent=new Intent(RegisterActivity.this,LoginActivity.class);
                            startActivity(intent);
                            }
                            else {
                                Toast toast = Toast.makeText(RegisterActivity.this, "注册失败！账户重复！", Toast.LENGTH_SHORT);
                                toast.show();

                            }
                        } catch (Exception e) {
                        }
                        break;
                    default:
                        break;
                }
            }
        };
    }

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_register);
        actionBar=getSupportActionBar();
        actionBar.hide();
        mTitleBar = (TitleBar) findViewById(R.id.tb_register_title_bar);

        mTitleBar.setBackgroundColor(0xffcd3333);
        mTitleBar.setOnTitleBarListener(new OnTitleBarListener() {
            @Override
            public void onLeftClick(View v) {
                Intent i = new Intent(RegisterActivity.this, MainActivity.class);
                startActivity(i);
            }

            @Override
            public void onTitleClick(View v) {

            }

            @Override
            public void onRightClick(View v) {

            }
        });
        getcode=(Button)findViewById(R.id.getcode);

        EventHandler eh=new EventHandler(){

            @Override
            public void afterEvent(int event, int result, Object data) {

                if (result == SMSSDK.RESULT_COMPLETE) {
                    //回调完成
                    if (event == SMSSDK.EVENT_SUBMIT_VERIFICATION_CODE) {
                        //提交验证码成功
                      //  Toast toast = Toast.makeText(RegisterActivity.this, "success", Toast.LENGTH_SHORT);

                        //  toast.show();
                        //sendRequestWithHttpClient();
                    }else if (event == SMSSDK.EVENT_GET_VERIFICATION_CODE){
                        //获取验证码成功
                        Log.d("CODE", "--onSuccess__app1" + "获取验证码成功");
                    }else if (event ==SMSSDK.EVENT_GET_SUPPORTED_COUNTRIES){
                        //返回支持发送验证码的国家列表
                    }
                }else{
                    ((Throwable)data).printStackTrace();
                    //code.setText("验证码错误！");
                }
            }
        };
        SMSSDK.registerEventHandler(eh);
        code=(EditText)findViewById(R.id.code);

        getcode.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String iphonenumber=tel.getText().toString();
                 Toast toast = Toast.makeText(RegisterActivity.this, iphonenumber, Toast.LENGTH_SHORT);

                  toast.show();
               // sendRequestWithHttpClient();
                SMSSDK.getVerificationCode("86", iphonenumber);
            }
        });
        //注册短信回调
        okhttptest = new Okhttptest();
        username = (EditText)findViewById(R.id.register_username);
        password = (EditText)findViewById(R.id.register_pwd);
        tel = (EditText)findViewById(R.id.register_tel);
        Btnreg = (Button)findViewById(R.id.register_Btnreg);
        Btnreg.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
               // Toast toast = Toast.makeText(RegisterActivity.this, "onclick", Toast.LENGTH_SHORT);

             //   toast.show();
               // SMSSDK.getVerificationCode("86", "17691256118");
  //             sendRequestWithHttpClient();
//
                sendRequestWithHttpClient();
               // SMSSDK.submitVerificationCode("86", tel.getText().toString(), code.getText().toString());
            }
        });
    }
    public void init(){
        button1 = (Button)findViewById(R.id.btnregister);
    }


    public void showList(View view){
        final String[] items = {"公司", "个人"};
        AlertDialog.Builder alertBuilder = new AlertDialog.Builder(this);
        alertBuilder.setTitle("这是列表框");
        alertBuilder.setItems(items, new DialogInterface.OnClickListener() {
            @Override
            public void onClick(DialogInterface dialogInterface, int i) {
                Toast.makeText(RegisterActivity.this, items[i], Toast.LENGTH_SHORT).show();
                alertDialog1.dismiss();
            }
        });
        alertDialog1 = alertBuilder.create();
        alertDialog1.show();
        EditText name = (EditText) findViewById(R.id.register_typename);
        SpannableString s = new SpannableString("请输入全称");
        name.setHint(s);
    }
    private void sendRequestWithHttpClient() {
        new Thread(new Runnable() {
            @Override
            public void run() {
                try {
                    String string_name = username.getText().toString();
                    String string_pwd = password.getText().toString();
                    string_pwd = okhttptest.md5Decode32(string_pwd);
                    String string_tel = tel.getText().toString();
                    SMSSDK.getVerificationCode("86", string_tel);
                   // String code=
                  //  SMSSDK.submitVerificationCode("86", string_tel, );
                    String url="http://ebarter-env.cn-north-1.eb.amazonaws.com.cn/JSONServlet";
                    String json="{'DOB': '','m_acct': '" +
                            string_name +  //username
                            "', 'm_yearsOfBusiness': 0," +
                            " 'm_phoneNum': '" +
                            string_tel +  //tel
                            "'," +
                            " 'm_referenceCode': '26358', " +
                            "'description': '', " +
                            "'m_appName': 'ebartercny', " +
                            "'forRcloud': True," +
                            " 'topLevel': -150," +
                            " 'm_storeName': '李斌43'," +
                            " 'm_registered': {'m_contactPhone': '13062530530', 'm_address': '家园中路', 'm_city': '南京市', 'm_firstName': 'lb', 'm_longitude': 118.82127335896413, 'm_latitude': 31.857023885105992}, " +
                            "'RoleName': 'hxgnyStudent'," +
                            " 'm_lindaPoints': 0," +
                            " 'm_acctType': 'SUPPLIER'," +
                            " 'm_businessTypes': []," +
                            " 'm_status': 'APPLY'," +
                            " 'listofNewBType': [{'m_displayName': '餐饮娱乐', 'm_typeLabel': 'CateringEntertainmen'}, {'m_displayName': '电脑办公', 'm_typeLabel': 'Computeroffice'}, {'m_displayName': '手机数码', 'm_typeLabel': 'Mobiledigital'}, {'m_displayName': '广告印刷', 'm_typeLabel': 'Advertisingprinting'}], " +
                            "'m_acctStatus': 'ACTIVATED'," +
                            " 'm_email': '999@163.com', " +
                            "'m_languageIndex': 1, " +
                            "'m_platform': 'BAIDU', " +
                            "'m_password': '" +
                            string_pwd +  //password
                            "'}";
                    String sellname=string_name+"@";

                  String response= okhttptest.postreg(url, json);
                  json="{'DOB': '','m_acct': '" +
                          sellname +  //username
                          "', 'm_yearsOfBusiness': 0," +
                          " 'm_phoneNum': '" +
                          string_tel +  //tel
                          "'," +
                          " 'm_referenceCode': '26358', " +
                          "'description': '', " +
                          "'m_appName': 'ebartercny', " +
                          "'forRcloud': True," +
                          " 'topLevel': -150," +
                          " 'm_storeName': '李斌43'," +
                          " 'm_registered': {'m_contactPhone': '13062530530', 'm_address': '家园中路', 'm_city': '南京市', 'm_firstName': 'lb', 'm_longitude': 118.82127335896413, 'm_latitude': 31.857023885105992}, " +
                          "'RoleName': 'hxgnyStudent'," +
                          " 'm_lindaPoints': 0," +
                          " 'm_acctType': 'SUPPLIER'," +
                          " 'm_businessTypes': []," +
                          " 'm_status': 'APPLY'," +
                          " 'listofNewBType': [{'m_displayName': '餐饮娱乐', 'm_typeLabel': 'CateringEntertainmen'}, {'m_displayName': '电脑办公', 'm_typeLabel': 'Computeroffice'}, {'m_displayName': '手机数码', 'm_typeLabel': 'Mobiledigital'}, {'m_displayName': '广告印刷', 'm_typeLabel': 'Advertisingprinting'}], " +
                          "'m_acctStatus': 'ACTIVATED'," +
                          " 'm_email': '999@163.com', " +
                          "'m_languageIndex': 1, " +
                          "'m_platform': 'BAIDU', " +
                          "'m_password': '" +
                          string_pwd +  //password
                          "'}";
                    okhttptest.postreg(url, json);
                    Message message = new Message();
                    message.what =0;
                    message.obj =response;
                    handler.sendMessage(message);
                } catch (Exception e) {
                    // TODO Auto-generated catch block
                    e.printStackTrace();
                }
            }
        }).start();//这个start()方法不要忘记了
    }
}

```

### 页面代码



```xml
<?xml version="1.0" encoding="utf-8"?>
<android.support.constraint.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android" android:layout_width="match_parent"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_height="match_parent">
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical">
        <com.hjq.bar.TitleBar
            android:id="@+id/tb_register_title_bar"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginTop="0dp"

            app:title="注册" />
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal">
            <ImageView
                android:layout_width="21dp"
                android:layout_height="26dp"
                android:layout_gravity="center"
                android:src="@drawable/username"/>
            <TextView
                android:layout_width="60dp"
                android:layout_height="wrap_content"
                android:text="会 员 名 "
                android:textColor="#000000"
                android:textSize="15sp"/>
            <View
                android:layout_width="1dp"
                android:layout_height="25dp"
                android:layout_gravity="center"
                android:background="#000000"/>
            <EditText
                android:id="@+id/register_username"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:hint="6～12位字符串（非必填）"/>
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal">
            <ImageView
                android:layout_width="21dp"
                android:layout_height="26dp"
                android:layout_gravity="center"
                android:src="@drawable/pwd"/>
            <TextView
                android:layout_width="60dp"
                android:layout_height="wrap_content"
                android:text="密      码 "
                android:gravity="center"
                android:textColor="#000000"
                android:textSize="15sp"/>
            <View
                android:layout_width="1dp"
                android:layout_height="25dp"
                android:layout_gravity="center"
                android:background="#000000"/>
            <EditText
                android:id="@+id/register_pwd"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:hint="请输入密码" />
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="30dp"
            android:orientation="horizontal">
            <TextView
                android:layout_width="wrap_content"
                android:layout_height="match_parent"
                android:text="国家/地区"
                android:textColor="#000000"
                android:textSize="15sp"/>
            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:gravity="right">
                <TextView
                    android:layout_width="wrap_content"
                    android:layout_height="match_parent"
                    android:text="中国"
                    android:textColor="#000000"
                    android:textSize="15sp"/>
            </LinearLayout>
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal">
            <ImageView
                android:layout_width="21dp"
                android:layout_height="26dp"
                android:layout_gravity="center"
                android:src="@drawable/tel"/>
            <TextView
                android:layout_width="60dp"
                android:layout_height="wrap_content"
                android:text="+86"
                android:gravity="center"
                android:textColor="#000000"
                android:textSize="15sp"/>
            <View
                android:layout_width="1dp"
                android:layout_height="25dp"
                android:layout_gravity="center"
                android:background="#000000"/>
            <EditText
                android:id="@+id/register_tel"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:hint="请输入联系方式" />
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="30dp"
            android:orientation="horizontal">
            <TextView
                android:layout_width="wrap_content"
                android:layout_height="match_parent"
                android:text="类型        "
                android:gravity="center"
                android:textColor="#000000"
                android:textSize="15sp"/>

            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:gravity="right">

                <Button
                    android:id="@+id/btnregister"
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:background="#01000000"
                    android:text="                                                          请选择类型"
                    android:onClick="showList"
                    android:gravity="center"
                    android:textColor="#000000"
                    android:textSize="15sp" />
            </LinearLayout>
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal">
            <ImageView
                android:layout_width="21dp"
                android:layout_height="26dp"
                android:layout_gravity="center"
                android:src="@drawable/username"/>
            <TextView
                android:id="@+id/TxtV_type"
                android:layout_width="60dp"
                android:layout_height="wrap_content"
                android:text="公      司"
                android:gravity="center"
                android:textColor="#000000"
                android:textSize="15sp"/>
            <View
                android:layout_width="1dp"
                android:layout_height="25dp"
                android:layout_gravity="center"
                android:background="#000000"/>
            <EditText
                android:id="@+id/register_typename"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:hint="请输入公司全称" />
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="30dp"
            android:orientation="horizontal">
            <TextView
                android:layout_width="wrap_content"
                android:layout_height="match_parent"
                android:text="商品类别"
                android:gravity="center"
                android:textColor="#000000"
                android:textSize="15sp"/>

            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:gravity="right">

                <Button
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:background="#01000000"
                    android:text="                                                  请选择商品类别"
                    android:gravity="center"
                    android:textColor="#000000"
                    android:textSize="15sp" />
            </LinearLayout>
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal">
            <EditText
                android:id="@+id/code"
                android:layout_width="200dp"
                android:layout_height="wrap_content"
                android:hint="验证码" />

            <Button
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="获取验证码"
                android:id="@+id/getcode"
                android:background="#01000000"
                android:textColor="#D3D3D3"/>
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content">
            <EditText
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:hint="经纪人邀请码（非必填）" />
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content">
            <CheckBox
                android:layout_width="wrap_content"
                android:layout_height="wrap_content" />
            <TextView
                android:layout_width="wrap_content"
                android:layout_height="match_parent"
                android:text="同意《易巴特服务协议》"
                android:textSize="10dp"
                android:gravity="center"/>
        </LinearLayout>
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content">
            <Button
                style="?android:textAppearanceSmall"
                android:id="@+id/register_Btnreg"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_marginTop="16dp"
                android:text="注册"
                android:textColor="#FFFFFF"
                android:background="#CD0000"
                android:textStyle="bold" />
        </LinearLayout>

    </LinearLayout>
</android.support.constraint.ConstraintLayout>
```

