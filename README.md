# Code
Study code
/*结构体
	结构体的声明
	结构：结构是一些值的集合，这些值称为成员变量，结构的每个成员可以是不同类型的变量。
	结构的声明：
	struct tag
	{
		member-list;
	}variable-list;
	结构成员的类型：结构的成员可以是标量，叔祖，指针，甚至是结构体。
	结构体变量的定义和初始化.
	结构体成员的访问：
		结构体变量访问成员 结构体变量的成员是通过点操作符(.)访问的。点操作符接受两个操作数。
*/
#include<stdio.h>
//描述一个学生--一些数据
//struct--结构体关键字  stu--结构体标签 struct stu--结构体类型
//struct stu
//{
//	char name[20];//姓名
//	short age;    //年龄
//	char tele[12];//电话
//	char sex[5];  //性别
//}s1,s2,s3;//s1,s2,s3是3个全局的结构体变量
//typedef struct stu//typedef--重新命名结构体类型
//{
//	char name[20];//姓名
//	short age;    //年龄
//	char tele[12];//电话
//	char sex[5];  //性别
//}stu;//stu是类型。
//
//void print1(stu s)
//{
//	printf("name: %s\n",s.name);
//	printf("age : %d\n",s.age);
//	printf("tele: %s\n",s.tele);
//	printf("sex : %s\n",s.sex);
//}
//void print2(stu* p)
//{
//	printf("name: %s\n",p->name);
//	printf("age : %d\n", p->age);
//	printf("tele: %s\n", p->tele);
//	printf("sex : %s\n", p->sex);
//}
////print1和print2函数哪个好些？
////首选print2函数,原因：
////函数传参的时候，参数是需要压栈的。
////如果传递一个结构体对象的时候，结构体过大，参数压栈时的系统开销比较大，所以会导致性能的下降
////结论：结构体传参的时候要传结构体的地址
//int main()
//{
//	struct stu s1 = {"张三",20,"15249287076","男"};//局部变量
//	//stu s2;
//	print1(s1);
//	print2(&s1);
//	return 0;
//}
#include<string.h>
#define _CRT_SECURE_NO_WARNINGS 1
//void my_strcpy(char* dest,char* src)
//{
//	while (* src != '\0')
//	{
//		*dest = *src;
//		src++;
//		dest++;
//	}
//	*dest = *src;//'\0'
//}
// 6分
//void my_strcpy(char* dest, char* src)
//{
//	while (*dest++=*src++)
//	{
//		;
//	}
//	
//}
//7分
//void my_strcpy(char* dest, char* src)
//{
//	if (dest != NULL && src != NULL) {
//		while (*dest++ = *src++)
//		{
//			;
//		}
//	}
//}
#include<assert.h>
//void my_strcpy(char* dest, char* src)
//{
//	assert(dest!=NULL);//断言
//	assert(src!=NULL);//断言
//		while (*dest++ = *src++)
//		{
//			;
//		}
//	
//}
//8分
//void my_strcpy(char* dest,const char* src)
//{
//	assert(dest!=NULL);//断言
//	assert(src!=NULL);//断言
//		while (*dest++ = *src++)
//		{
//			;
//		}
//	
//}
//9分
//char* my_strcpy(char* dest,const char* src)
//{
//	char* ret = dest;
//	assert(dest!=NULL);//断言
//	assert(src!=NULL);//断言
//	//把src指向的字符串拷贝到dest指向的空间，包含'\0'字符
//		while (*dest++ = *src++)
//		{
//			;
//		}
//		return dest;
//}
//10分
//int main()
//{
//	char arr1[] = "####################";
//	char arr2[] = "bit";
//	//strcpy
//	//字符串拷贝
//	my_strcpy(arr1,arr2);
//	printf("%s\n",arr2);
//	return 0;
//}
//int main()
//{
//	int a = 10;
//	int b = 20;
//	//const 放在指针变量的*左边时，修饰的是*p,也就是说：不能通过p来改变*p(num)的值
//	//const int* p = &a;
//	//*p = 20;//err
//	//const 放在指针变量的*右边时，修饰的是指针变量p本身，p不能被改变
//	//int* const p = &a;
//	//p = &b;//err
//	//*p = 20;
//	printf("%d\n",a);
//	return 0;
//}
//求字符串长度
//int my_strlen(const char *arr)
//{
//	int count = 0;
//	assert(arr!=NULL);//保证指针的有效性
//
//	while (*arr != '\0')
//	{
//		count++;
//		arr++;
//	}
//	return count;
//}
//int main()
//{
//	char arr[] = "abcdef";
//	int len=my_strlen(arr);
//	printf("%d\n",len);
//	return 0;
//}
