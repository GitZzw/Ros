### some ros concepts


#### 1.spin rate sleep区别
[参考](https://www.cnblogs.com/liu-fa/p/5925381.html)
>
 ros::spin() 一直循环执行消息回调，不执行之后的语句
 ros::spinOnce() 执行一次消息回调，然后继续执行之后的语句，与ros::Rate 和 rate.sleep()结合使用
 ros::Rate rate(50)  规定循环的频率50Hz
 rate.sleep()  如果运行到rate.sleep()后未达到0.02s（1/50Hz） 进行休眠，与spinOnce结合使用


#### 2.roslaunch 的写法(填坑)
[参考](https://www.one-tab.com/page/P6bgTvrWRHS8LNmPqqJStA)
>
  对于python文件
  <node pkg="initialpos" name="initial_pos" type="initial_pos.py" output="screen">
  </node>

> 对于cpp文件
  在Cmamkelist里修改add_excutable


#### 3.ros info throttle 控制输出流频率(埋坑) (如果输出频率太快输出太多，cpu性能不好的话可能直接崩掉)


#### 4.px4切offboard短时间内会上锁，所以在起飞前不能做太多其他延时逻辑


#### 5.命令行操作文件.sh的参考写法见sh.md


#### 6.windows下文件批量重命名的方法(linux下直接用系统的rename工具即可)
> [参考](https://www.cnblogs.com/dirgo/p/11167968.html)

> 在excel中生成一列A1原文件的名字(注意加引号)  
  在第二列B1生成要更改文件的名字(注意加引号)
  在第三列C1中用excel函数="ren "&A1&" "&B1
  复制第三列到txt文件中，改名为rename.bat
  然后执行批处理文件.bat即可
