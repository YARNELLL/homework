## homework
#### Computer Professional English Assignment
[B站](https://www.bilibili.com/)  
[超星](http://i.mooc.chaoxing.com/)

[另一个markdown文本链接](https://github.com/YARNELLL/homework/blob/master/homework.md)
***
网络不好图片可能展示不出来  
![1 图片](./1.png)

![RUNOOB](http://static.runoob.com/images/runoob-logo.png)
***
**一个实现互斥的代码**
```Java
package study15d;
public class Ticket {
	public static void main(String[] args){
     sold t1=new sold("1");
     sold t2=new sold("2");
     sold t3=new sold("3");
     sold t4=new sold("4");
     sold t5=new sold("5");
     t1.start();
     t2.start();
     t3.start();
     t4.start();
     t5.start();
	}
}
class sold extends Thread
{
	private String name;
	public sold(String name) {
		super(name);
		this.name = name;
	}
	public static int total=100;
	//该object对象是静态的
	public static Object obj=new Object();
	
	public void run()
	{  
		while(true)
	  {
		synchronized(obj)
		{
			if(total>0)
			{
				System.out.println(name+"_______"+(total--));
			}
			else
			{
				break; 
			}
		}
		try {
			Thread.sleep(200);
		} catch (InterruptedException e) {
			e.printStackTrace();
		}
	  }
	}
}
```
***
>第一层
>>1.第二层第一列  
>>2.第二层第二列
>>>+ 第三层第一列  
>>>+ 第三层第二列
***
| 第一列 | 第二列 |
| :---:  | :---: |
| 第一项 | 第二项 |
| 第三项 | 第四项 |
***
**粗体字**  
*斜体字*
***
~~删除线~~  
~~111111~~
