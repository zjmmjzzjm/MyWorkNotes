# 受击动作

``` java
IF 在地面

   IF 受击类型为击退
       
      播放普通击退动作      HitBack

   ELSE IF 受击类型为击飞

	转入上升第一阶段   HitFloat1
   
   ELSE IF 受击类型为挑空
	
        转入上升第一阶段 HitFloat1

   END

ELSE IF 上升第一阶段  

   IF 受击类型为击退
	
        转入上升第二阶段       HitFloat2
    
   ELSE IF 受击类型为击飞
 
	转入上升第三阶段    HitFloat3
   
   ELSE IF 受击类型为挑空

	转入上升第二阶段   HitFloat1
   END

ELSE IF 上升第二阶段（上升阶段）

   IF 受击类型为击退

        转入上升第二阶段        HitFloat2
    
   ELSE IF 受击类型为击飞
    
        击飞参数重置
        重新进入上升第三阶段   HitFloat3
   
   ELSE IF 受击类型为挑空
	
        挑空参数重置
        重新进入上升第二阶段  HitFloat1

   END

ELSE IF 下降阶段

   IF 受击类型为击退

        转入上升第二阶段  HitFloat2
    
   ELSE IF 受击类型为击飞

	击飞参数重置
        重新进入上升第三阶段   HitFloat3
   
   ELSE IF 受击类型为挑空
	
	挑空参数重置
        重新进入上升第二阶段  HitFloat1

   END

   循环检测落地事件，落地后进入起身状态

END


```
