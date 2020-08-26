
# DeepRacer

## Train
### 计分学习模式 使用网格系统计分

每个网格的计分系统不同，通过中间黄线的车道的网格计分为2，黄线两侧的计分为0.2，赛道外记为失败，通过学习反馈让小车能够增加在黄线的准确性。 

### Parameter

1. position on track
   - x 赛车当前的x轴
   - y 赛车当前的y轴
2. Heading
   - heading 赛车头部和x轴的偏移角度
3. Waypoints
   - waypoints
     - [x,y] 赛道黄线都被分割为若干个点，这些点都有各自的x和y值来标识坐标
4. Track width
    - track_width 赛道的宽度
5. Distance from center line
   - distance_from_center 距离中心线的长度
   - is_left_of_center [boolean] 返回一个布尔值，标识赛车是否在黄线的左侧
6. All wheels on track
   - all_wheels_on_track [boolean] 表明是否所有的轮子都在赛道之内
7. Speed
   - speed 测量当前的速度
8. Steering angle
   - steering_angle 用于测量当前车头方向和轮胎便宜方向的角度并返回这个角度，如果车辆右转，此值为负值，如果车辆左转，此值为正值