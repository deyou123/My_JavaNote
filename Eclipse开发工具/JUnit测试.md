#选中要测试的代码Math：
new——>Java——>JUnit——>JUnit Test Case.
选中要测试的add 方法即可

----------
编写Math类
	package cn.mldn.demo;

	public class Math {
	private Math(){}
	
		public static  int add (int a, int b){
			int result = 0;//为了方便观察定义此变量
			result =  a + b; //加法计算
			return result; //返回计算结果
		} 
	}

----------

## 编写JUnit测试程序

    package cn.mldn.demo;

	import static org.junit.Assert.*;
	import junit.framework.TestCase;

	import org.junit.Test;

	public class MathTest {

		@Test
		public void testAdd() {
			TestCase.assertEquals(Math.add(10, 20), 30);//测试是否相等
			System.out.println("测试add 方法成功");
		}

	}

run as ——> JUnit Test 成功显示Green bar ,失败显示Red bar.