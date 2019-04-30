# yearCalender-monthCalender
about choose year and choose month
# 年份选择器
![images](https://github.com/krifyFan/image-folder/blob/master/yearCalender.png)<br>
用到的环境是vue2.0+iview2.0<br>
## 思路
1、首先拿到今年的年份，放在初始页面的最后一个位置，一页放9个，只需要再循环出8个年份就可以了<br>
2、获取上一页的年份，拿到当前页的第一个年份，即yearList[0]，然后向上拿到9个就可以了<br>
3、获取下一页的年份，同理，拿到当前页的最后一个年份，即yearList[8]，然后向下拿到9个年份就可以了
# 月份选择器
![images](https://github.com/krifyFan/image-folder/blob/master/monthCalender.png)<br>
用到的环境是vue2.0+iview2.0<br>
## 思路
1、拿到当前的年份，每一年都是12个月，上一年或下一年只需要在当前年份的基础上减加就可以了
#  日历，对年月日的选择（包含了间隔选择、星期选择、自由选择三种模式）
## 间隔选择
![images](https://github.com/krifyFan/image-folder/blob/master/jiange.png)
## 星期选择模式
![images](https://github.com/krifyFan/image-folder/blob/master/week.png)
## 自由选择模式
![images](https://github.com/krifyFan/image-folder/blob/master/free.png)<br>
代码地址：https://github.com/krifyFan/calender.git
