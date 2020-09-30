# No-of-set-bits
This is the code to find the number of set bits in a number
#include <bits/stdc++.h>
#define ull unsigned ll
#define ll long long int
#define ld long double
#define pb push_back
#define mp make_pair
#define mt make_tuple
#define ff first
#define ss second
#define pi acos(-1)
#define nu 100
#define INF 100000000000
#pragma GCC optimize("Ofast")
#pragma GCC target("avx,avx2,fma")
#pragma GCC optimization ("unroll-loops")
#define F(i,a,n) for(ll i=a;i<n;i++)
#define B(i,a,n) for(ll i=n-1;i>=a;i--)

#define tc int t;cin>>t;while(t--)
#define tcf ll t;cin>>t;for(int w=1;w<=t;w++)

const int mod = 1000000007;


using namespace std;

/*
Time Complexity O(set bits)
*/

ll countsetbits(ll n)
{
    ll ct = 0;
    while (n > 0)
    {
        n &= (n - 1);
        ct++;
    }
    return ct;
}

int main()
{

#ifndef ONLINE_JUDGE
    freopen("input.txt", "r", stdin);
    freopen("output.txt", "w", stdout);
#endif

    ios_base::sync_with_stdio(0); cin.tie(0); cout.tie(0);


    ll n;
    cin >> n;
    cout << countsetbits(n) << "\n";
}

