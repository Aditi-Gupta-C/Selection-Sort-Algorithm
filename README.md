# Selection Sort Algorithm

* It is a simple and efficient sorting algorithm
* Divides the array in sorted and unsorted part, then in each iteration finds the minimum or 
  maximum element in unsorted part.
* for minimum element->swaps the minimum element with the first element in the unsorted 
  region or for maximum element->swaps the maximum element with the last element in the unsorted 
  region
* In each step expanding the sorted region by one step

  ## Function for selection sort

  ## Code

First Approach
     
      

     void selectionSort(int a[] ,int n){
     
      for (int i=0;i<n;i++){  
     int mi=a[i];
    // i -> position of current beginning element
    // suppose mi be the minimum element, let's compare it with the remaining array
    int swapindex=-1;// initialize it with -1 at now, we don't have any element which is less than mi
    for (int j=i+1;j<n;j++){
        if(a[j]<mi){
        mi=a[j];       // update mi
        swapindex=j;  // update swapindex with index j --> shows we have an element at position j which is less than the current end position element
        }
    }
    if(swapindex!=-1)
     swap(a[i],a[swapindex]); } }// if we get a minimum element less than the current beginning element -> swap them

## We can applied the same logic in opposite way to find the maximum element and placed it at the end of an unsorted array, let see in code


  ## Code

Another approach
     
      

     void selectionSort(int a[] ,int n){
     
      for (int i=n-1;i>-1;i--){  
     int ma=a[i];
    // i -> position of current end element
    // suppose ma is be the maximum element, let's compare it in the remaining array
    int swapindex=-1;// initialize it with -1 at now we don't have any element which is greater than ma
    for (int j=i-1;j>-1;j--){
        if(a[j]>ma){
        ma=a[j];       // update ma
        swapindex=j;  // update swapindex with index j --> shows we have an element at position j which is greater than the current end position element
        }
    }
    if(swapindex!=-1)
     swap(a[i],a[swapindex]); } }// if we get a maximum element greater than the current end element -> swap them

#### Noted 
* Unstable algorithm
*  number of sort is less than the Bubble sort
* take less space than bubble sort
* time complexity - o(n2)
* space complexity - o(1) constant
* maximum swaps -o(n)
