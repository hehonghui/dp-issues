# Android源码设计模式解析与实战勘误

>任何一个产品在前期都不可避免会出现一些错误，本书也不例外。虽然经过了多次交稿、审核，仍然可能会发现一些细微的错误，我们将这些错误勘误在此，这些错误将在下一次印刷时得到修正。非常感谢大家的理解与帮助！

《Android源码设计模式解析与实战》

* [京东购买地址](http://item.jd.com/11793928.html) 


## 提issue规范

1. 书中错别字请注明哪一页、哪一段的什么字以及正确的字。例如 : 第89页第二段的"零活"修改为“灵活”。如果是代码错误，也请给出修改后的正确代码;
2. 如果是排版比较乱，则直接给出页数即可。例如 : 第56页代码排版混乱。

> 由于笔者写文章时使用的是mac版word，而出版社使用的则是windows版的word，导致了第一次印刷时排版出现较多的问题，在此向大家致歉。在此给出第一次印刷时的修正排版。
> 
* 第一次印刷排版勘误,[排版勘误.pdf](排版勘误.pdf) ，[从百度网盘下载](http://pan.baidu.com/s/1c00npXQ)。

## 第一次勘误列表

### 第一章
* 第2页，下7-少空格
* 第13页，上18-“无线”应为“无限”
* 第17页，下7-多空格
* 第18页，上17-“飞越”应为“飞跃”
* 第19页，下-Tenant类中的roomArea、roomPrice未初始化，也未赋值，不知道干嘛用
* 第21页，上-同上
* 第22页，上-14-“rul”应为“LRU”

### 第二章
* 第26页，下-“CheckLock”应为“Check Lock”
* 第27页，中-“调整了JVM、具体化了“，中间的、应为，
* 第28页，倒数第二行,Objectinstance应为Object instance;
* 第28页，倒数第三行,private Singleton() {} 修改为 private SingletonManager() {} ;
* 第29页，上-ObjectgetService中间应该有空格,即为Object getService;

### 第三章
* 第44页，中-“且组装顺序却是不固定的”不通顺，应为“并且组装顺序是不固定的“
* 第44页，第一行，-“组件”应为“组建”
* 第52页，上-if(mListView!=null){}的18. 括号多一个}
* 第55页，中-"meature"应为“measure”
* 第55页，下6-“但并不是只有UI线程才能更新线程”应为“但并不是因为只有UI线程才能更新UI”
* 第62页，上-真是“山重水复疑无路，柳暗花明又一村。”的句号应该放在引号外面，因为诗句是组成这句话的一部分，不能单独成句
* 64页，上-“字段私有优化”应为“字段私有化”

### 第四章
* 第82页，下5-“最好”应该为“最后”
* 第83页，上-第一段第二句话，逗号太多，建议分句；
* 第83页，下，注释中-“完成信息”应该为“完整信息”
* 第84页，“不巧的是”与“万万没想到”同义，重复
* 第85页，上第一段，“这样一来...”句子太长，难以理解，建议分句

### 第五章
* 第90页，下第二段-“但是”应为“而且”
* 第90页，下-标题应改为“工厂方法模式的简单实现”
* 第90页，下-“这里以...来说明，”应该为“这里以...来说明。”
* 第92页，下-不应该存在下划线
* 第94页，中-“...大家可以体会;”应为“...大家可以体会。”
* 第95页，上-“也曾学到一个类，在构造时...”应为“也曾学到，一个类在构造时...”
* 第95页，上-“大部分情况下...”缺少主语
* 第95页，上-“对于开发者来说常常会认为...”主语错误，这里的主语应该为“开发者”，而不是“我们的应用”
* 第96页，中-下划线不应该有
* 第101页，中-“component=new”缺少空格，修改修为为"component = new ";
* 第101页，中-“Instrumentationcall中ActivityOnCreate “应改为“Instrumentation中callActivityOnCreate”;

### 第六章
* 第106页，上-“其实现不同、展示效果也不一样”应为“其实现不同，展示效果也不一样”
* 第108页，最后一行下划线去掉；
* 第112页，下划线去掉；
* 第116页，上-“和TestPlayerStub，”应为“和TestPlayerStub。”
* 第116页，下-“一是对类文件的...”应为“一是类文件的...”

### 第十章
* 183页，下1-“解析器”应为“解释器”
* 186、187、188页，代码中“interpreter()”方法命名应为“interpret()”，应该为动词，而且与前面通用模式代码中的命名吻合。
* 189页，中-“第一个例子我们在客户类里构建由17个数字和一个数字或字母构成的语法树”，这里没有看懂是指的哪个例子。

### 第十二章
* 第226页，Test类里的方法main中 DevTechFrontierDevTechFrontier = new DevTechFrontier()； 中间没有空格，应该修改为"DevTechFrontier devTechFrontier = new DevTechFrontier()"；
* 第231页 
```java
BroadcastReceiver updateReceiver = new BroadcastReceiver(){
  @Override
  public void onReceive(Context context, Intent intent){
    Toast.makText(context, “”, 0).show();
  }   //这里少了一个大括号
};
```
* 第238页，最后一行，"或之类的组件之间的交互问题……","或之"改为“或者”;

## 第二次勘误列表
### 第三章
* 第44页，底部代码中setBoard和setDisplay方法中的core和gb变量来源不明；

应修改为 : 

```java
 // 设置主板
public  void setBoard(String board) {
  mBoard = board ;
}

// 设置显示器
public  void setDisplay(String display) {
  mDisplay = display ;
}
```

### 第四章
* 第73页，下方的代码描述不妥当，clone方法中“new Intent(this)”，这里的this究竟指代的什么应该描述清楚，建议在示例代码外部套上对应类；
* 第85页，下方最后一段代码中getLoginedUser方法内应该注释掉“return loginedUser”而非“loginedUser.clone()”；

### 第七章
* 第124页，第一段代码下方第一行末尾的“最好”应为“最后”；

### 第十二章
* 第230页，顶部第二行“AdapternotifyDataSetChanged”应为“Adapter.notifyDataSetChanged”；

### 第十三章
* 第255页，顶部第一行“最好”应为“最后”；

### 第三章 55页 

"很多读者可能对ViewRootImpl并不陌生，咋一看它的名字可能会误以为它是一个View，但实际上不是这样的，它继承自Handler，是作为native与Java层View系统通信的桥梁" 。

修改为 : 

`......它内部封装了一个Handler对象，通过这个Handler对象作为native与Java层View系统通信的桥梁。`
