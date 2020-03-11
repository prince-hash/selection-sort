# selection-sort


#include <iostream>

void swap(int *a, int *b) {
    int tmp = *a;
    *a = *b;
    *b = tmp;
    
}

int main() {
   int n;
   std::cin >> n;
   int a[n];
   for (int i = 0; i < n; i++) {
       std::cin >> a[i];
   }
   for (int i = 0; i < n; i++) {
       for (int j = i; j < n; j++) {
           if (a[i] > a[j]) {
               swap(&a[i], &a[j]);
           }
       }
   }
   
   for (int i = 0; i < n; i++) {
       std::cout << a[i] << ' ';
   }
    return 0;
}
