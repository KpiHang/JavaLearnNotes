# Java Learn Notes

## 第一章 基础知识

### Code

```java
import java.util.Arrays;

public class Main {
    // ??: 这里的类变量为何自动分配空间了？
    static boolean bool;
    static byte by;
    static char ch;
    static double d;
    static float f;
    static int i;
    static long l;
    static short sh;
    static String str;

    public static void main(String[] args) {
        // 一、变量声明与赋值
        double a_double; // 仅声明变量，还未分配内存空间；
        a_double = Math.PI; // 分配空间并赋值；
        System.out.printf("a_double: %.2f \n", a_double);

        double b_double = Math.PI;  // 声明变量并分配空间赋值；
        System.out.printf("b_double: %.15f \n", b_double);

        // 二、基本数据类型及其默认值
        // 1. byte：8位补码表示的有符号整数；[-128, 127]
        // 2. short: 16位补码表示的有符号整数；
        // 3. int: 32位补码表示的有符号整数；
        // 4. long: 64位补码表示的有符号整数；

        // float: 数据类型是单精度、32位、符合IEEE 754标准的浮点数；默认值：0.0f；
        // double: 数据类型是双精度、64 位、符合 IEEE 754 标准的浮点数；默认值是 0.0d；

        // boolean: true and false
        // char: 类型是一个单一的 16 位 Unicode 字符；C语言ASCII码是8位的；

        // byte
        System.out.println("基本类型：byte 二进制位数：" + Byte.SIZE);
        System.out.println("包装类：java.lang.Byte");
        System.out.println("最小值：Byte.MIN_VALUE=" + Byte.MIN_VALUE);
        System.out.println("最大值：Byte.MAX_VALUE=" + Byte.MAX_VALUE);
        System.out.println();

        // short
        System.out.println("基本类型：short 二进制位数：" + Short.SIZE);
        System.out.println("包装类：java.lang.Short");
        System.out.println("最小值：Short.MIN_VALUE=" + Short.MIN_VALUE);
        System.out.println("最大值：Short.MAX_VALUE=" + Short.MAX_VALUE);
        System.out.println();

        // int
        System.out.println("基本类型：int 二进制位数：" + Integer.SIZE);
        System.out.println("包装类：java.lang.Integer");
        System.out.println("最小值：Integer.MIN_VALUE=" + Integer.MIN_VALUE);
        System.out.println("最大值：Integer.MAX_VALUE=" + Integer.MAX_VALUE);
        System.out.println();

        // long
        System.out.println("基本类型：long 二进制位数：" + Long.SIZE);
        System.out.println("包装类：java.lang.Long");
        System.out.println("最小值：Long.MIN_VALUE=" + Long.MIN_VALUE);
        System.out.println("最大值：Long.MAX_VALUE=" + Long.MAX_VALUE);
        System.out.println();

        // float
        System.out.println("基本类型：float 二进制位数：" + Float.SIZE);
        System.out.println("包装类：java.lang.Float");
        System.out.println("最小值：Float.MIN_VALUE=" + Float.MIN_VALUE);
        System.out.println("最大值：Float.MAX_VALUE=" + Float.MAX_VALUE);
        System.out.println();

        // double
        System.out.println("基本类型：double 二进制位数：" + Double.SIZE);
        System.out.println("包装类：java.lang.Double");
        System.out.println("最小值：Double.MIN_VALUE=" + Double.MIN_VALUE);
        System.out.println("最大值：Double.MAX_VALUE=" + Double.MAX_VALUE);
        System.out.println();

        // char
        System.out.println("基本类型：char 二进制位数：" + Character.SIZE);
        System.out.println("包装类：java.lang.Character");
        // 以数值形式而不是字符形式将Character.MIN_VALUE输出到控制台
        System.out.println("最小值：Character.MIN_VALUE="
                + (int) Character.MIN_VALUE);
        // 以数值形式而不是字符形式将Character.MAX_VALUE输出到控制台
        System.out.println("最大值：Character.MAX_VALUE="
                + (int) Character.MAX_VALUE);
        System.out.println();

        // 默认值
        System.out.println("Bool default value:" + bool);
        System.out.println("Byte default value:" + by);
        System.out.println("Character default value:" + ch);
        System.out.println("Double default value:" + d);
        System.out.println("Float  default value:" + f);
        System.out.println("Integer default value:" + i);
        System.out.println("Long default value:" + l);
        System.out.println("Short default value:" + sh);
        System.out.println("String default value:" + str);

        // 三、变量类型

        // 1 常量
        // 常量在程序运行时是不能被修改的；在 Java 中使用 final 关键字来修饰常量；
        final double PI = 3.1415927;
        System.out.println();

        // 四、条件语句
        int x = 10;
        if (x < 0)
            System.out.println("x < 0");
        else
            System.out.println("x > 0");
        System.out.println();

        // 五、循环语句（while + for）
        // 1 while
        int N = 10;
        int v = 1;
        while(v <= N) {
            System.out.print(" " + v + " ");
            v = v * 2;
        }
        System.out.println();
        System.out.println();

        // 2.1 for遍历数组1；
        double[] a = {1,1,2,3,5,8};
        // 数值倒置；
        N = a.length;
        for (int i=0; i < N/2; i++){
            double temp = a[i];
            a[i] = a[N-1-i];
            a[N-1-i] = temp;
        }
        System.out.println(Arrays.toString(a));

        // 2.2 for遍历数组2；
        for (double y: a)
            System.out.print(" " + y);
        System.out.println();
    }
    // 参考目录：
    // https://www.runoob.com/java/java-basic-datatypes.html
}
```



### Output

```shell
a_double: 3.14 
b_double: 3.141592653589793 
基本类型：byte 二进制位数：8
包装类：java.lang.Byte
最小值：Byte.MIN_VALUE=-128
最大值：Byte.MAX_VALUE=127

基本类型：short 二进制位数：16
包装类：java.lang.Short
最小值：Short.MIN_VALUE=-32768
最大值：Short.MAX_VALUE=32767

基本类型：int 二进制位数：32
包装类：java.lang.Integer
最小值：Integer.MIN_VALUE=-2147483648
最大值：Integer.MAX_VALUE=2147483647

基本类型：long 二进制位数：64
包装类：java.lang.Long
最小值：Long.MIN_VALUE=-9223372036854775808
最大值：Long.MAX_VALUE=9223372036854775807

基本类型：float 二进制位数：32
包装类：java.lang.Float
最小值：Float.MIN_VALUE=1.4E-45
最大值：Float.MAX_VALUE=3.4028235E38

基本类型：double 二进制位数：64
包装类：java.lang.Double
最小值：Double.MIN_VALUE=4.9E-324
最大值：Double.MAX_VALUE=1.7976931348623157E308

基本类型：char 二进制位数：16
包装类：java.lang.Character
最小值：Character.MIN_VALUE=0
最大值：Character.MAX_VALUE=65535

Bool default value:false
Byte default value:0
Character default value:
Double default value:0.0
Float  default value:0.0
Integer default value:0
Long default value:0
Short default value:0
String default value:null

x > 0

 1  2  4  8 

[8.0, 5.0, 3.0, 2.0, 1.0, 1.0]
 8.0 5.0 3.0 2.0 1.0 1.0
```

