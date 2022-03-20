# My-repo-pub
# My-repo-pub
//bt2
#include <iostream>

using namespace std;
void test(int *a){
    cout<<sizeof(a)/sizeof(int)<<endl;
}
int main()
{
    int a[6]={1,2,5,5,5};
    cout<<sizeof(a)/sizeof(int)<<endl;
    test(a);

    return 0;
}
//bt3
#include <iostream>

using namespace std;
void count_even(int*a,int n){
        int cnt=0;
    for (int i=0; i<n; i++){
        if (*(a+i) %2==0) cnt++;
    }
        cout<<cnt;
}
int main()
{
    int n=6;
    int a[n]={1,2,5,5,5,6};
     count_even(a,n);
    return 0;
}

//bt4
#include <iostream>
#include <algorithm>

using namespace std;
void find(int*a,int n,int x){
    int flag=1;
    int i=0, j=n;
    while (i<=j){
        int mid=i+(j-i)/2;
        if (*(a+mid)==x) {
            cout<<"yes"; flag=0;
            break;
        }
        if (*(a+mid)>x) j=mid-1;
        else i=mid+1;
    }
    if (flag) cout<<"no";
}
int main()
{
    int n=6,x=6;
    int a[n]={1,2,5,5,5,6};
    sort(a,a+n);
    find(a,n,x);
    return 0;
}
