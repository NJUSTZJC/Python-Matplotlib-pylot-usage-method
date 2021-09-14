绘制所有图的共同考虑顺序：



- 为了能够显示中文字体，所以必须添加以下两行。
  from pylab import *
  plt.rcParams['font.sans-serif'] = ['SimHei']






- plt.figure(num,figsize)
  #设置打开画布大小,长10，宽6
  plt.figure(figsize=(10,6))



- 设置图标的标题名称
  plt.title("")

- ​    ax = plt.gca()   
  ​     设置X轴和Y轴的归属
  ​     设置X轴和Y轴的名称
  ​     plt.xlabel("")
  ​     plt.ylabel("")
  ​     ax.spines



- plt.xlim()或者plt.ylim()限制图标展示的X和Y的范围

​     

- plt.xticks()和plt.yticks()设置X轴Y轴上取得值及其对应的名字
  ​     plt.xticks([0,1],["男","女"])
  ​     plt.yticks([-4000,-2000,0,2000,4000],["really bad","bad","zero","good","really good"])



- plt.bar(X值, Y值,  color = "",  width = 0.35,   label(图例) = "y1")



- plt.annotate()添加注释
  #为单独描出的一个点添加注释：
  x0 = 35
  y1_0 = 100*x0+1
  plt.scatter(x0,y1_0 ,color ="red",s = 20)
  plt.annotate(xy=(x0,y1_0) , s = (x0,y1_0),textcoords = "offset points",xytext = (+20,-10),weight="heavy",
                   color = "green", fontsize = 10,arrowprops = dict(arrowstyle = "->",color = "red"))

  

- 为所有marker的点添加注释：
  for (a,b) in zip(x, y1):
      顺序为xy(给哪个点添加注释)/s(添加的注释内容)/添加的注释的位置/.........      S后不仅可以填入字符串，还可以填入整形数据。
      plt.annotate(xy=(a,b), s=(a,b), textcoords="offset points", xytext=(+30, -10), weight="heavy",
                   color="red", fontsize=5, arrowprops=dict(arrowstyle="->", color="green"))

- plt.legend(loc = "best")，画出图例，并设置图例在图中的位置，这里我们默认为best。

- plt.show()#画出图像