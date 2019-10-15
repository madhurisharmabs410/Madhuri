#include<bits/stdc++.h>
using namespace std;

int partition(int arr[], int low, int high)
{
int pivot=low, i=low+1, j=high;

while(1)
{
 while(arr[i]<=arr[pivot] && i<=high)
  i++;
 while(arr[j]>arr[pivot] && j>=low)
  j--;
 
 if(i<j)
 {
  swap(arr[i], arr[j]);
 }
 else
{
swap(arr[j], arr[pivot]);
return j;
}
}
}

int kthsmallest(int a[], int l, int h, int k)
{
int pos=partition(a, l, h);

if(pos-l == k-1)
 return a[pos];
else if(pos-l > k-1)
 return kthsmallest(a, l, pos-1, k);

return kthsmallest(a, pos+1, h, k-pos+l-1);
}


int main()
{
int n, i, q;
cout<<"Enter length of array: ";
cin>>n;
int a[n];
cout<<"Enter array elemnts: ";
for(i=0; i<n; i++)
cin>>a[i];
cout<<"Enter number of queries: ";
cin>>q;

while(q--)
{
int start, end, k;
cout<<"Enter values of start, end and k: ";
cin>>start>>end>>k;
cout<<"The "<<k<<"th smallest element between the given range is: ";
int ans=kthsmallest(a, start-1, end-1, k);
cout<<ans<<endl;
}
}
