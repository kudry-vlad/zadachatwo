#include "stdafx.h"
#include <iostream>
#include <locale.h>
using namespace std; 

int main(void) {
	setlocale(LC_ALL, "Russia");
	int h1, m1, h2, m2;
	cout << "Введите время отправления (hh mm): ";
	cin >> h1 >> m1;
	cout << "Введите время в пути (hh mm): ";
	cin >> h2 >> m2;
	int d3, h3, m3;
	m3 = (m1 + m2) % 60;
	int hext = (m1 + m2) / 60;
	h3 = (h1 + h2 + hext) % 24;
	d3 = 1 + (h1 + h2 + hext) / 24;
	cout << "Время прибытия: день " << d3 << ", " << h3 << ":" << m3 << endl;
	return 0;
