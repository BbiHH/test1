#include <bits/stdc++.h>

using namespace std;

typedef long long ll;
const int MAXN = 1e5 + 5;
const int INF = 0x3f3f3f3f;
bool vis[MAXN];
int prime[MAXN],x;

int kkk(int n)
{
    int ans = 0;
    if(n%2 == 0)
    {
        ans ++;
        while(n%2 == 0)
        {
            n/=2;
        }
    }
    for(int i=1; prime[i]*prime[i]<=n; i++)
    {

        while(n%prime[i]==0)
        {
            n=n/prime[i];
            ans ++;
        }

    }
    if(n>1)
        ans++;
    return ans;
}


void oulasai(int n)  //欧拉筛
{
    for(int i=2; i<=n; i++)
    {
        if(!vis[i]) prime[x++]=i;
        for(int j=0; j<x; j++)
        {
            if(i*prime[j]>n) break;
            vis[i*prime[j]]=true;
            if(i%prime[j]==0) break;
        }
    }
}

int main()
{
    ios::sync_with_stdio(false);
    int t;
    cin>>t;
    oulasai(MAXN);
    while(t --)
    {
        int n;
        cin>>n;
        //cout<<kkk(n)<<endl;

        int num = 0;
        int ans=0;
        int z = 0;
        for(int i = 0; i < n; i ++)
        {
            int t;
            cin>>t;
            int k = kkk(t);
            ans=ans^k;
        }
        if(ans)
            cout<<"W"<<endl;
        else
            cout<<"L"<<endl;
    }
    return 0;
}
