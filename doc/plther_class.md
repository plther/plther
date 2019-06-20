1. Item：时间安排的父类

   1. 目的：

      为了提供时间安排上的最小单位的描述

   2. 设计：

      1. 属性：
         1. date：描述年月日，节次
         2. activity:在这个时间段的安排
         3. flag:有没有被占用
      2. 特殊方法：
         1. 对比时间


2. classItem extend Item

      1. 目的：记录一个课程的某一节
      2. 设计：
         1. 属性
            1. 课程 id
            2. 课程名
            3. 所有者
            4. 重要程度 <del>可以翘课吗</del>
         2. 特殊方法
3. activatyItem extend Item

   1. 目的：安排自定义活动
   2. 设计：

      1. 属性：

         1. group:参与者群组
      2. 方法：

         1. getGroup：获取本次事件群组
         
4. Day
   1. 目的：以天为单位管理Item
   2. 设计
      1. 属性：dayOfWeak：是本周的第几天
      2. 方法
         1. getItem: 获取一天中指定的节
5. 一周课表类

      1. 容纳这一周的Item
      2. 设计

         1. 属性

            1. 一周的item安排
            2. weekOfSemester：本周是这个学期的第几周
            3. Single: 标志单双周
         2. 方法：

            1. getDay:获取指定的天
6. 一学期课表类

   1. 目的：容纳这一学期的周
   2. 设计

      1. 属性

         1. 一学期的周安排
         2. semesterOfSchoolYear:本学期是这一年中的第几个人学期
      2. 方法

         1. getWeek 获取指定的周