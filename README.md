# 9.17.1
矩阵的转置（引用数组的使用）
// 9.17.1.cpp : 定义控制台应用程序的入口点。
//矩阵转置函数

#include "stdafx.h"
#include<iostream>

using namespace std;
void Swap(int &a, int &b) {
	int temp=a;
	a = b;
	b = temp;
}

int main()
{
	int a[3][3];
	cout << "请输入一个3*3的矩阵" << endl;
	for (int i = 0; i < 3; i++) {
		for (int j = 0; j < 3; j++) {
			cin >> a[i][j];
		}
	}
	cout << endl << "初始矩阵为：" << endl;
	for (int i = 0; i < 3; i++) {
		for (int j = 0; j < 3; j++) {
			cout << a[i][j]<<" ";
		}
		cout << endl;
	}
	for (int i = 0; i < 3; i++) {
		for (int j = 0; j < i; j++) { //j<i保证了只进行一半的元素的转换
			swap(a[i][j],a[j][i]);
		}
	}
	cout << "转置后的矩阵为：" << endl;
	for (int i = 0; i < 3; i++) {
		for (int j = 0; j < 3; j++) {
			cout << a[i][j]<<" ";
		}
		cout << endl;
	}
    return 0;
}

