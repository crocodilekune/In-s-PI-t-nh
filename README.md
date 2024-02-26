# In-s-PI-t-nh
Lập trình tính số PI với sai số eps cho trước nhập từ bàn phím. Biết rằng số PI tính theo công thức: PI = 4 - 4/3 + 4/5 - 4/7 +... tính tổng các số hạng có giá trị không nhỏ hơn eps. In ra số PI tính được và số PI của Turbo C++ với 10 chữ số thập phân để so sánh.
#include <stdio.h>
#include <conio.h>
#include <math.h>;//chua hang so pi la M_PI

void main()
{
	float pi, t, n, eps, dau;
	clrscr();
	printf("Nhap sai so eps=");
	scanf("%f", &eps);

	pi = 0;
	t = 4;
	n = dau = 1;

	do
	{
		pi += dau * t;
		n = n + 2;
		dau = -dau;
		t = 4 / n;
	} while (t >= eps);
	printf("\nSo PI tinh duoc voi sai so %12.10f, PI=%12.10f\n", eps, pi);
	printf("\nSo PI cua Turbo C++, PI=%12.10f\n", M_PI);
	getch();
}
