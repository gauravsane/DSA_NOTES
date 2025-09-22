# DSA_NOTES
DSA From August


## --------------------10/08/2025----------------------------------------------
1] Data Types In C++
= int,long, long long, float, double, string, getline and char

3] Array are stored in consicutive memory location

3] Time Complexity (Big O) for worst case Senario
 = Theta for average Case
 = Omega for Best Case

calculating time complexity avoid constants and lower values


4]Space Complexity = Memory Space (Big O)
= Auxilary Space(space that takes to store the problem) + Input space(space to store inputs)



## -----------------------11/08/2025------------------------------------------
5] Pattern Logic
Rule1: "Outor For Loop count No of Rows"
Rule2: "Inner For Loop used for columns and connect somehows to the rows"
Rule3: "Print what pattern on the inner loop like "*, # $ "..etc;

#include <bits/stdc++.h>
using namespace std;



void printFirstCase(int n){
  for(int i=0;i<n;i++){
    for(int j=0;j<n;j++){
      cout << "* ";
    }
    cout << endl;
  }
}



void print2(int n){
    for(int i=0; i<n; i++){
        for(int j=0; j<=i; j++){
            cout << "* ";
        }
        cout << endl;
    }
}

void print3(int n){
    for(int i=1;i<=n;i++){
        for(int j=1;j<=i;j++){
            cout << j << " ";
        }
        cout << endl;
    }
}

void print4(int n){
    for(int i=1;i<=n;i++){
        for (int j=1;j<=i;j++){
            cout << i << " ";
        }
        cout << endl;
    }
}

void print5(int n){
    for(int i=1; i<=n ;i++){
       for(int j = 1; j<n-i+1;j++){
           cout << j << " ";
       }
    cout << endl;
    }
}

void print6(int n){
    for(int i=1;i<=n;i++){
        for(int j=1;j<n-i+1;j++){
            cout << j << " ";
        }
        cout << endl;
    }
}



int main()
{
  int n;
  cin >> n;
  print6(n);

}


## -----------------------------12/08/25-----------------------------------

#include <bits/stdc++.h>
using namespace std;


void print7(int n){
  for(int i=0;i<=n;i++){
      //space
      for(int j=0;j<=n-i-1;j++){
          cout << " ";
      }

      //Star
      for(int j=0;j<2*i+1;j++){
          cout << "*";
      }

      //space
      for(int j=0;j<n-i-1;j++){
          cout << " ";
      }
      cout << endl;
  }
}

void print8(int n){
   for(int i=0;i<=n;i++){
       //Space
       for(int j=0;j<=i;j++){
           cout << " ";
       }
       //star
       for(int j=0; j<2*n-(2*i+1);j++){
           cout<< "*";
       }
       //space
       for(int j=0;j<=i;j++){
           cout << " ";
       }
       cout << endl;
   }
}



int main()
{
   print8(9);
}




## -------------------------------13/08/2025------------------------------
void print10(int n){
    for(int i=1;i<=2*n-1;i++){
        int star = i;
        if(i> n) star = 2*n-i;
        for(int j=1;j<=star;j++){
            cout << "*";
        }
        cout << endl;
    }
}

int main()
{
    print10(9);
}


#include <bits/stdc++.h>
using namespace std;


void print10(int n){
    for(int i=1;i<=2*n-1;i++){
        int star = i;
        if(i> n) star = 2*n-i;
        for(int j=1;j<=star;j++){
            cout << "*";
        }
        cout << endl;
    }
}

void print11(int n){
        int start = 1;
    for(int i=0;i<=n;i++){
        if(i % 2 == 0) start = 1;
        else start = 0;
        for(int j=0;j<=i;j++){
            cout << start;
            cout << 1 - start;
        }
        cout << endl;
    }
}

int main()
{
    print11(5);
}



## ---------------------------------------14/08/2025-------------------------------------------------
#include <bits/stdc++.h>
using namespace std;


void print11(int n){
        int space = 2*(n-1);
    for(int i=1;i<=n;i++){
        for(int j=1;j<=i;j++){
            cout << j;
        }
        for(int j=1;j<=space;j++){
            cout << " ";
        }
        for(int j=i;j>=1;j--){
            cout << j;
        }
        cout << endl;
        space -= 2;
    }
}


void print12(int n){
    int num = 1;
    for(int i=1;i<=n;i++){
        for(int j=1; j<=i; j++){
            cout << num << " ";
            num += 1;
        }
        cout << endl;
    }
}


void print13(int n){
    for(int i=0;i<=n;i++){
       for(char ch='A'; ch <= 'A' + i; ch++){
           cout << ch << " ";
       }
        cout << endl;
    }
}


void print14(int n){
    for(int i=0;i<=n;i++){
        for(char ch = 'A'; ch<='A'+(n-i-1);ch++){
            cout << ch << " ";
        }
        cout << endl;
    }
}

void print15(int n){
    for(int i=0;i<=n;i++){
    char ch ='A'+ i;
        for(int j=0;j<=i;j++){
            cout << ch << " ";
        }
        cout << endl;
    }
}

void print16(int n){
    for(int i=0;i<=n;i++){
        for(int j=0;j<=n-i-1;j++){
            cout << " ";
        }

        char ch = 'A';
        int breakpoint = (2*i+1) / 2;
        for(int j=1;j<=2*i+1;j++){
            cout << ch;
            if(j <= breakpoint) ch++;
            else ch--;
        }

        for(int j=0;j<=n-i-1;j++){
            cout << " ";
        }
        cout << endl;
    }
}

int main()
{
    print16(5);
}



## ------------------------------------15/08/2025-------------------------------------------------
#include <bits/stdc++.h>
using namespace std;


void print18(int n){
    for (int i=0;i<=n;i++){
        for(char ch = 'E' - i;ch <= 'E';ch++){
            cout << ch << " ";
        }
        cout << endl;
    }
}

void print19(int n){
    int insS = 0;
    for(int i=1;i<=n;i++){
        for(int j=1;j<=n-i;j++){
            cout << "*";
        }
         for(int j=1;j<insS;j++){
            cout << " ";
        }
         for(int j=1;j<=n-i;j++){
            cout << "*";
        }
        insS += 2;
        cout << endl;
    }
    int inS1 = 2*n - 2;
     for(int i=0;i<=n;i++){
        for(int j=0;j<=i;j++){
            cout << "*";
        }
         for(int j=1;j<inS1;j++){
            cout << " ";
        }
         for(int j=1;j<=i;j++){
            cout << "*";
        }
        inS1 -= 2;
        cout << endl;
    }
}

void print20(int n){
    for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
            if(i == 0 || i == n-1 || j == 0 || j== n-1){
                cout << "*";
            }
            else cout << " ";
        }
        cout << endl;
    }
}

int main(){
    print20(6);
}

## -STL (Standard Template Library)-

# 1] Pairs = Present in Utility function, it is used to stored paired values,
# 2] Vectors = Its a Container stored values like array but we can modified also that values;
# 3] dataStructure<dataType>::iterator it = v.begin() || v.end() || v.rend() || v.rbegin(); -----syntax of iterator is basically used to access the vector values stored in memories;


## ------------------17/08/2025---------------------------------

1] Stack = Works in Lifo principle last in first out
2] Queue = Works in Fifo principle first in first out
3] Priority Queue = Large value comes first

push = log n
pop = O(1)
top = log n

4] Set = Unique + Sorted values

5] MultiSet = Only Sorted Values

6] Unordered Set = only Unique Time Complexity O(n) most of the time O(n) some times its goes O(n);

7] Map = Stored data in key and value pair and stored it Unique keys + sorted order Sorted keys

8] MultiMap = Sorted log N

9] Unordered Map = Unique keys


## ---------------------------18/08/2025------------------------------
1] If your code any operation perform by division then time complexity is always logn(N)


## ------------------------19/08/2025---------------------------------
1] Find Factors of Number Using Sqrt method
#include <bits/stdc++.h>
using namespace std;
 bool factors(int n) {
        vector<int> ls;
        for(int i = 1; i <= sqrt(n);i++){
          if (n % i == 0) {
              ls.push_back(i);
              if((n/i) != i) ls.push_back(n/i);
          }
        }
        sort(ls.begin(),ls.end());
        for(auto it: ls) cout << it << " ";
        return 0;
    }

int main() {
    factors(36);
}


2] Check For Prime
#include <bits/stdc++.h>
using namespace std;


 int checkPrime(int n) {
       int cp = 0;
       for(int i = 1; i < sqrt(n); i++){
           if(n % i == 0) cp++;
           if(n/i) cp++;
       }
           if(cp == 2) cout << "Prime No";
           else cout << "Not Prime No";
       return 0;
    }

int main() {
    checkPrime(8);
}

3] Euclidean_algorithm
#include <bits/stdc++.h>
using namespace std;

    //Euclidean_algorithm
    int checkGCF(int n1,int n2) {
     while (n1 > 0 && n2 > 0){
         if(n1 > n2) n1 = n1 % n2;
         else n2 = n2 % n1;
     }
     if (n1 == 0) cout <<  n2 << endl;
     else cout << n1 << endl;
     return 0;
    }

int main() {
    checkGCF(20,34);
}


## ------------------------------20/8/2025-------------------------
1] Recursion = Its a function call itself until specific condition is met;

#include <bits/stdc++.h>
using namespace std;

void printInt(int i,int n){
    if (i > n) return;
    cout << i << " ";
    i += 1;
    printInt(i,n);
}

int main()
{
  printInt(1,4);
}


## ------------------------------------21/08/2025-----------------------------
#include <bits/stdc++.h>
using namespace std;


int functionalRecursion(int n){
    if(n == 0) return 1;
    return n * functionalRecursion(n-1);
}

int parameterRecursion(int i, int sum){
    if(i == 0) return sum;

    return parameterRecursion(i-1,sum * i);
}

int main()
{
    int d = functionalRecursion(6);
    int c = parameterRecursion(3,1);
    cout << c;
}
## ----------------------------------------25/08/2025---------------------------
1] Check Given String in Palindrome or not
#include <bits/stdc++.h>
using namespace std;

bool checkPalindrome(int i,const string &s,int n){
        if(n <=1) return true;
        if (i >= n / 2)
            return true;
        if (s[i] != s[n - i - 1])
            return false;

        return checkPalindrome(i + 1, s, n);
    }

int main(){
    string s = "A.";
     for (char &c : s) {
        c = tolower(c);
    }
    regex re("[^a-zA-Z0-9]+");
    string replString = regex_replace(s,re,"");
    int n = replString.length();checkPalindrome(0,replString,n);
}

2] Fibonacci Series
#include <bits/stdc++.h>
using namespace std;

 int printFibonacci(int n){
        if (n <= 1) return n;
        int flast = printFibonacci(n - 1);
        int slast = printFibonacci(n - 2);
        cout << flast + slast;
        return flast + slast;
    }

int main()
{
   int n = 2;
   return printFibonacci(n);
}
                          

## ------------------29/08/2025---------------------
1] Hashing
-In hashing using array you can only go 10^6 in main and 10^7 in globally

## ---------------------31/08/2025------------------
1] Hashing Methods:
- Division Method
- Folding Method
- Mid Square Method


## ------------------07-09-2025-------------------------
1] Selection-Sort = Get the minimum value and swap it.
#include <bits/stdc++.h>
using namespace std;


void selection_sort(int arr[],int n){
    for(int i=0;i<=n-2;i++){
        int miniV = i;
        for(int j = i; j<=n-1; j++){
            if(arr[j] < arr[miniV]){
            miniV = j;
            }
        }
        int temp = arr[miniV];
        arr[miniV] = arr[i];
        arr[i] = temp;
    }
}   

int main(){
    int nums[] = {12,2,4,5,6,1,0};
    selection_sort(nums,7);
     cout << "Sorted array: ";
    for (int i = 0; i < 7; i++) {
        cout << nums[i] << " ";
    }
}
Time complexity = O(n^2) worst best and average;

2] Bubble-Sort = Push the maximum values to the last by adjacent swaping
void bubble_sort(int arr[],int n){
    for(int i = n-1; i>=0; i--){
        for(int j=0; j<=i-1; j++){
            if(arr[j] > arr[j+1]){
                int temp = arr[j+1];
                arr[j+1] = arr[j];
                arr[j] = temp;
            }
        }
    }
}
Time Complexity = Best = O(N) is already sorted and worst is O(n^2);


3] Insertion Sort = Take an element and place it in correct order
void insertion_sort(int arr[],int n){
    for(int i=0; i<=n-1; i++){
        int j=i;
        while(j > 0 && arr[j-1] > arr[j]){
            int temp = arr[j-1];
            arr[j-1] = arr[j];
            arr[j] = temp;
            j--;
        }
    }
    Time Complexity = Best = O(N) is already sorted and worst is O(n^2);


 ## -------------------------22-09-2025-------------------------------
1] Find smalles and largest value with its index position
#include <bits/stdc++.h>
using namespace std;

int main() {
        int nums[] = {32,5,78,-4,7,1};
        int size = 5;

        int smallestValue = INT_MAX;
        int largestValue = INT_MIN;
        int smallestIndex = 0;
        int largestIndex = 0;
        for (int i=0; i<=size; i++) {
                if(nums[i] < smallestValue) {
                        smallestValue = nums[i];
                        smallestIndex = i;
                }
                else if(nums[i] > largestValue){
                    largestValue = nums[i];
                    largestIndex = i;
                }
        }
        cout << "Smallest-Value: " << smallestValue << endl;
        cout << "Smallest-Index: " << smallestIndex << endl;
        cout << "Largest-Value: " << largestValue << endl;
        cout << "Largest-Index: " << largestIndex << endl;
        return 0;
}

2] Pass by refrence in C++ change in original array;

3] Linear Search
#include <bits/stdc++.h>
using namespace std;

int linearSearch(int arr[],int sz,int target){
    for (int i = 0; i<sz; i++){
        if (arr[i] == target){
            return i;
        }
    }
    return -1;
}

int main() {
        int arr[] = {32,5,78,-4,7,1};
        int size = 5;
        int target = -40;
        int lSearch = linearSearch(arr,size,target);
        cout << lSearch;
        return 0;
}
Time Complexity = O(n);


4] Reverse an Array
#include <bits/stdc++.h>
using namespace std;


void reverseArray(int arr[],int size){
    int start = 0;
    int end = size -1;
    while (start < end){
        swap(arr[start],arr[end]);
        start++;
        end--;
    }
}
int main() {
        int arr[] = {32,5,78,-4,7,1};
        int size = 6;
        reverseArray(arr,size);
        for (int i=0;i<size;i++){
            cout << arr[i] << " ";
        }
        return 0;

5]Calculate sum and product of all numbers present in Array
#include <bits/stdc++.h>
using namespace std;


void sumAndProductOfArray(int arr[],int sz){
    int sum = 0;
    int product = 1;
   for(int i = 0;i<sz; i++){
       sum += arr[i];
       product *= arr[i];
   } 
   cout << sum << endl;
   cout << product;
}

int main() {
	int arr[] = {1,2,4,2};
	int size = 4;
	sumAndProductOfArray(arr,size);
	return 0;
}
