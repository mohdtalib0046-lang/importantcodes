# importantcodes
all codes
// #include <iostream>
// using namespace std;
// int factorial(int a){
//     int fact = 1;
//     for(int i=1;i<=a;i++){
//         fact*=i;
//     }
//     return fact;
// }

// int main() {
//     cout<<factorial(6);

//     return 0;
// }



// #include <iostream>
// using namespace std;
// int binarynumber(int a){
//     int ans=0;
//     int pow=1; 
//     while( a > 0) {
//         int rem = a%2;
//         a = a/2;
//         ans = ans + (pow*rem);
//         pow = pow*10;

//     }
//     return ans;
// }
    

// int main() {
//     cout<<binarynumber(8);
    

//     return 0;
// }



// #include <iostream>
// using namespace std;
// int bintodec(int n){
//     int ans=0;
//     int pow= 1;
//     while (n > 0){
//         int rem = n%10;
//         ans = (rem*pow)+ans;
//         n = n/10;
//         pow = pow*2;
        

    
//     }
//     return ans;
// }
// int main (){
//     cout<<bintodec(1001);
//     return 0;
// }


// LINIAR SERCH ALGORITHME

// # include<iostream>
// using namespace std;
// int linsech(int arr[],int size,int target){
//     for(int i=0;i<size;i++){
//        if(arr[i]==target){
//         return i;
//        }
//     }
//     return -1;
       
// }
// int main (){
//     int arr[]={1,3,4,5,7,9,43,56,23,54};
//     int size=10;
//     int target=9;
//     cout<<linsech(arr,size,target)<<endl;
//     return 0;
// }



//ARRAY REVERSE


// #include<iostream>
// using namespace std;

// int main (){
//     int arr[7] = {4,3,5,6,7,89,32};

//     for(int i = 6; i >= 0; i--){
//         cout << arr[i] << endl;
//     }

//     return 0;
// }


// caluculate sum and product of all numbers of arr



// #include<iostream>
// using namespace std;
// int sumandproductarr(int arr[], int size){
//     int sum = 0;
//     int pro = 1;
//     for(int i=0;i<size;i++){
//         sum = sum + arr[i];
//         pro = pro*arr[i];

        

//     }
//     cout<<"the sum of arr is "<<sum<<" "<<endl<<"the product of arr is "<<pro;
    
    
// }
// int main (){
//     int arr[] = {4,6,7,5,3,2,9,1};
//     int size = 8;
//     cout<<"the sum of arr is "<<sumandproductarr(arr,8);
//     return 0;






// BOILERPLATE CODE





// #include<iostream>
// using namespace std;
// int main (){

//     return 0;
// }



// VECTOR



// #include<iostream>
// #include<vector>
// using namespace std;
// int main (){
//     int ans = 0;
//     vector<int> vec = {1,1,2,2,3,3,4,4,5};
//     for(int val : vec){
//          ans = ans ^ val;

//     }
//     cout<<ans<<endl
//     return 0;
// }









    
// #include<iostream>
// #include<vector>
// using namespace std;

// int main(){
//     vector<int> arr = {1,2,3,4,5,6,7,8,9};
//     int target = 7;

//     int n = arr.size();

//     for(int i = 0; i < n; i++){                                                       // PAIR SUM FIND                      
//         for(int j = i + 1; j < n; j++){
//             if(arr[i] + arr[j] == target){
//                 cout << "(" << arr[i] << ", " << arr[j] << ")" << endl;
//             }
//         }
//     }

//     return 0;
// }













                                                                                   // optimize technique
// #include <iostream>
// #include <vector>
// #include <algorithm>
// using namespace std;

// int main (){
    
//     vector<int> arr = {1,1,2,3,7,7,7,7,8,8,8,9,9,9,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4};
//     int n = arr.size();

//     sort(arr.begin(), arr.end());

//     int freq = 1;

//     for(int i = 1; i < n; i++){
//         if(arr[i] == arr[i-1]){
//             freq++;
//         }
//         else{
//             freq = 1;
//         }

//         if(freq > n/2){
//             cout << "Majority element = " << arr[i];
//             return 0;
//         }
//     }

//     cout << "No majority element";

//     return 0;
// }
















// #include<iostream>
// using namespace std;

// int powert(int val, int pow){
//     int ans = 1;
//     for(int i = 1; i <= pow; i++){                                                             // find pow with no
//         ans = ans * val;
//     }
//     return ans;
// }

// int main (){
//     int result = powert(3,9);
//     cout << result;
//     return 0;
// }























    












// #include<iostream>                                                                        // maxwater problem
// #include<vector>
// #include<algorithm>
// using namespace std;

// int maxArea(vector<int>& height) {
//     int ans = 0;
//     for(int i = 0; i < height.size(); i++) {
//         for(int j = i + 1; j < height.size(); j++) {
//             int wt = j - i;
//             int ht = min(height[i], height[j]);
//             int area = wt * ht;
//             ans = max(ans, area);
//         }
//     }
//     return ans;
// }

// int main() {
//     vector<int> height = {1,8,6,2,5,4,8,3,7};
//     cout << "Max Area: " << maxArea(height);
//     return 0;
// }



// int maxArea(vector<int>& height) {
//         int lp = 0;
//         int rp = height.size()-1;
//         int ans = 0;
//         while(lp<rp){                                                             //water conteiner with pointer
//             int wt = rp-lp;                                                       // leetcode = 11
//             int ht = min(height[lp],height[rp]);
//             int maxwater = wt*ht;
//             ans = max(ans,maxwater);
//             height[lp]<height[rp]?lp++:rp--;
//         }
//         return ans;







end 