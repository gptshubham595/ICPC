# ICPC

1:
===================================================================================

#include <bits/stdc++.h>
using namespace std;

int main() {

int t;
cin>>t;
for(int T=0;T<t;T++)
	{
	    string s;
	    cin>>s;
	    int c=0,r=0,n=s.size();
	    for(int i=0;i<n;i++)if(s[i]=='.')c++;
	    r=n-c;

	    int us=0;

	    if(r==0 || r==1)cout<<"safe"<<endl;

	    else{
	    for(int i=0;i<n;i++)if(s[i]!='.'){
	        //cout<<"RF";
	        int dig=(int)(s[i]-'0');
	     //   cout<<"DIG="<<dig<<endl;
	       // cout<<"i+1="<<i+1<<endl;
	        int rs=i+1-dig; if(rs<0)rs=0;
	        int re=i+1+dig; if(re>n)re=n;

	        //cout<<"RS="<<rs<<endl;
	        //cout<<"Re="<<re<<endl;


	        for(int j=rs;j<re;j++)
                {if(s[j]!='.' && i!=j )
                {us++;}else if(i!=j){s[j]=s[i];}
            }
	    }
	    }

        if(us>0)cout<<"unsafe"<<endl;
	}

	return 0;
}
===================================================================================
2:
#include<bits/stdc++.h>
 
// Competetive Template:
typedef long long int lli;
typedef unsigned long long int ulli;
typedef long double ldb;
 
#define pb push_back
#define pf push_front
#define popb pop_back
#define popf pop_front
#define ba  back
#define si size()
#define be begin()
#define en end()
#define le length()
#define mp make_pair
#define mt make_tuple
#define fi first
#define se second
 
#define forz(i,n) for(long long int i=0;i<n;i++)
#define rep(i,k,n) for (lli i = k; i <= n; i++)
#define deci(n)  fixed<<setprecision(n)
#define high(n) __builtin_popcount(n)
#define parity(n) __builtin_parity(n)
#define ctz(n)  __builtin_ctz(n)
#define mod 1000000007
#define mod2 998244353
#define kira ios::sync_with_stdio(0), cin.tie(0),cout.tie(0)
 
using namespace std;
typedef pair <lli,lli> pll;
