- 👋 Hi, I’m @mostafanada
- 👀 I’m interested in program
- 🌱 I’m currently learning backend
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me https://www.facebook.com/mostafamahmoud.nada/

<!---
mostafanada/mostafanada is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
#include <bits/stdc++.h>
#define ll long long
using namespace std;

int main()
{
    ll t;cin>>t;
    while(t--)
    {
        ll n,k;cin>>n>>k;
        ll maxi=-1e16;
        ll arr[n+5];
        for(ll i=1;i<=n;i++)cin>>arr[i];
        for(ll i=n;i>=1;i--)
        {
            for(ll j=i-1;j>=1;j--)
            {
                if(i*j<maxi)break;
                ll s=i*j-k*(arr[i]|arr[j]);
                maxi=max(s,maxi);
            }
        }
        cout<<maxi<<"\n";
    }
    return 0;
}
