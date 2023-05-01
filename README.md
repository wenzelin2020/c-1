# c-1
这是我的c++学习记录
···#include <bits/stdc++.h>
using namespace std;
long long n, q, a[200001],  total = 1, b[200001], c[200001];
char pp[200001];

signed main() {
	ios::sync_with_stdio(0);
	cin.tie(0);
	cout.tie(0);
	cin >> n >> q;
	for (int i = 1; i <= q; i++) {
		cin >> pp[i];
		if (pp[i] == '+')
			cin >> b[i] >> c[i];
		if (pp[i] == '*')
			cin >> b[i];
	}
	for (int i = q; i >= 1; i--) {
		if (pp[i] == '*')
			total *= b[i], total %= 1000000007;
		if (pp[i] == '+')
			a[b[i]] += total * c[i];
		a[b[i]] %= 1000000007;
	}
	for (int i = 1; i <= n; i++)
		printf("%lld ", a[i]);
	return 0;
}···
//这是解决单点修改，全部乘法的c++代码
格式没做好，请见谅
