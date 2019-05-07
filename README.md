# 实验2 《Windows Form实现MIDI音乐文件的播放APP》实验报告
学院：软件学院  班级：软工四班   学号：3017218159   姓名：李琛
日期：2019年5月4日
# 一、功能概述：
1.点击open，选择音乐进行播放。  
2.可使用按钮进行开始/暂停/继续操作，也可使用进度条改变播放进度。  
3.实现单曲循环功能。  
# 二、项目特色
GUI界面中的控件大小、位置能够随APP界面大小自动调整。  
添加背景图片，并适应窗口大小。  
实现是否开启单曲循环功能。  
# 三、代码总量
100行左右
# 四、工作时间
不详
# 五、知识点总结
1.保存原始窗口比例大小，用以实时改变控件大小  
2.用事件实现radio button选中以及取消选择  
3.用委托实现跨线程调用按钮点击事件  
# 六、结论
## 实现过程
### 1.实现控件大小自适应
（1）首先为每个控件设置一个标签  
（2）标签记录每个控件的大小  
（3）在事件Form1_Resize（窗口大小变化事件）中，遍历所有控件，将其大小、位置、字体按比例变化。  
### 2.用一个RadioButton实现是否单曲循环
（1）添加radioButton1_Click事件，点击选中，再点取消选中。  
（2）选中radioButton1时，将标签置为true。  
（3）播放结束时，判断标签，若为true则执行Replay。  
（4）定义一个委托，使用委托事件模拟点击开始按钮，实现单曲循环自动播放。  
# 实现结果
1.打开窗口：  
![image](https://github.com/3017218159/Sanford.Multimedia.Midi-master/blob/master/Demo/SequencerDemo/1.png)  
2.调整大小：  
![image](https://github.com/3017218159/Sanford.Multimedia.Midi-master/blob/master/Demo/SequencerDemo/2.png)  
3.播放音乐时：  
![image](https://github.com/3017218159/Sanford.Multimedia.Midi-master/blob/master/Demo/SequencerDemo/3.png)  
4.选中单曲循环时，播放完会重新播放。
