# Assignment 1 - Arrays

## Task 1: Explain how to create an array of 100 elements. You can choose any data type of your choice. (requires C++ code)
**Response**
In C++ you must start by specifying the data type, the name of the array, and the number of elements in square brackets(in this case 100). Once the array is created you can access elements using their index, ranging from 0 to size-1, in this case 0 to 99. 

#include <iostream>
using namespace std;

int main(){
    //make array with 100 integers
    int myarray[100];//elements are empty to start

//if you want to fill the array say with numbers from 1 to 100
for(int i=0; i<100; i++){
    myarray[i]=i+1;
} return 0;
}

## Task 2: What will be the size of each element of an array
**Response**
The size of an element in an array depends on its data type. Int usually takes 4 bytes, a double usually 8 bytes, and a char usually 1 byte. The 'sizeof' operator can be used to determine the size of an array element in a program. 

#include <iostream>
using namespace std;

int main(){
    int numbers[100];
    double decimals[30];
    char letters[26];
cout<<"Size of each int element: "<< sizeof(numbers[0])<<"bytes"<<endl;
cout<<"Size of each double element: "<< sizeof(decimals[0])<<"bytes"<<endl;
cout<<"Size of each char element: "<< sizeof(letters[0])<<"bytes"<<endl;
}

## Task 3: For an array containing 100 elements, provide the number of steps the following operations would take: (theoretical)
**Response**
Reading: Accessing an element at a known index takes 1 step
Searching for a value not contained within the array: 100 steps, must check every element before concluding the value isnt there
Insertion at the beginning of the array:  100 steps, All the other elements must be shifted one spot to make space at the start/front
Insertion at the end of the array: 1 step, assuming space is available, no shifting is necessary
 Deletion at the beginning of the array: 100 steps, after you remove the element, all others get shifted one spot to the start
  Deletion at the end of the array: 1 step, no shifting necessary

  ## Task 4: Normally the search operation in an array looks for the first instance of a given value. But sometimes we may want to look for every instance of a given value. For example, say we want to count how many times the value “apple” is found inside an array. How many steps would it take to find all the “apples”? Give your answer in terms of N
  **Response**
  To find all of the occurrences of a value in an array, every element must be checked, meaning an array of size N would take N steps. 

  ## Task 5: Research how to find the memory address of an array
**Response** 
In C++, an array name represents the memory address of the first element in the array, so the array name itself can be used as a pointer.  You can also find the memory address of specific elements using the & operator.

#include <iostream>
using namespace std;
int main(){
    int Rigid[5]={10,20,30,40,50};
    //address of entire array(same as address of first element)
    cout<<"Address. of array(Rigid): " <<Rigid<< endl;
    //address of first element
    cout<<"Address of first element: "<< &Rigid[0]<<endl;
    //Address of 2nd element
    cout<< "Address of 2nd element: " << &Rigid[1]<<endl;
}
