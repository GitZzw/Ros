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
