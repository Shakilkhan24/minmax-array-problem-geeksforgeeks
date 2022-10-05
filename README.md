/*minmax-array-problem-geeksforgeeks
geeksforgeeks minium and maximum element in an array
*/


#include <bits/stdc++.h>
using namespace std;
#define ll long long

pair<long long, long long> getMinMax(long long a[], int n) {
    
    long long min=a[0],max=a[0];
    
    for(int i=0;i<n;i++){
        if(a[i]>max){
           max=a[i];
       }
     }
      for(int i=0;i<n;i++){
        if(a[i]<min){
           min=a[i];
       }
     }
     
    pair<long long ,long long> pp(min,max);
    return pp;
};

int main() {
    int t;
    cin >> t;
    while (t--) {
        int n;
        cin >> n;
        ll a[n];
        for (int i = 0; i < n; i++) cin >> a[i];

        pair<ll, ll> pp = getMinMax(a, n);

        cout << pp.first << " " << pp.second << endl;
    }
    return 0;
}


