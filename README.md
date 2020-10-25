实验3-选课模拟
一、实验目的
（1）初步了解分析系统需求，从学生选课角度了解系统中的实体及其关系，学会定义类中的属性以及方法；
（2）掌握面向对象的类设计方法（属性、方法）；
（3）掌握类的继承用法，通过构造方法实例化对象；
（4）学会使用super()，用于实例化子类；
（5）掌握使用Object根类的toString（）方法,应用在相关对象的信息输出中。
二、（1）业务要求
说明：学校有“人员”，分为“教师”和“学生”，教师教授“课程”，学生选择“课程”。从简化系统考虑，每名教师仅教授一门课程，每门课程的授课教师也仅有一位，每名学生选仅选一门课程。
对象：
人员（编号、姓名、性别）
教师（编号、姓名、性别、所授课程）
学生（编号、姓名、性别、所选课程）
课程（编号、课程名称、上课地点、时间、授课教师）
三、（2）实验要求
1.编写上述实体类以及测试主类（注意类之间继承关系的适用）
2.在测试主类中，实例化多个类实体，模拟学生选课操作、打印课程信息（信息包括：编号、课程名称、上课地点、时间、授课教师 等）；模拟学生退课操作，再打印课程信息。
四、流程图
五、核心代码
package test3.java;
public class Test {
    public static void main(String[] args) {
        Student me = new Student(2019311146, "史亦文", "MAN");
        System.out.println("学生信息");
        System.out.println(me);
        Teacher b = new Teacher(01, "游煦", "MAN", "线代");
        System.out.println("教师信息");
        System.out.println(b);
        Course c = new Course("线代", 01, "202", 90f);
        System.out.println("课程信息");
        System.out.println(c); 
        me.tuike();
        me.delete();
   
}
}  
六、实验过程
1.Teacher和Student为子类， 用extends继承person的属性和方法
2.利用super函数调用父类的构造方法，实例化子类
3.在Course类创建课程信息并将所选课覆盖即退课
4 在test里输入选课信息之后退课
七、实验结果
![Image text](https://github.com/SYW-github/-/blob/main/1603607232(1).png)
八、实验感想
对super访问父类属性和extends继承父类构造方法有一些了解
