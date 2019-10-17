# ICPC

1:===================================================================================

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
