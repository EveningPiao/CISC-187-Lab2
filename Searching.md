1. 4 steps  
2. 1 step  
3. 17 steps  
4. ```  
#include <iostream>  
using namespace std;  
const int SIZE = 100000;  

//if we search for 95555  
// Linear Search
int linearSearch(int arr[], int size, int &steps) {  
    steps = 0;  
    for (int i = 0; i < size; i++) {  
        steps++;  
        if (arr[i] == 95555) {  
            return i;  
        }  
    }  
    // no target  
    return -1;  
}  

// Binary Search  
int binarySearch(int arr[], int size, int &steps) {  
    int left = 0;  
    int right = size - 1;  
    steps = 0;  

    while (left <= right) {  
        steps++;  

        int mid = (right + left) / 2;  

        if (arr[mid] == 95555) {  
            return mid;
        }
        // target on the right
        else if (arr[mid] < 95555) {
            left = mid + 1;
        }
        // target on the left
        else {
            right = mid - 1;
        }
    }

    // no target
    return -1;  
}

int main() {  
    int arr[SIZE];  

    for (int i = 0; i < SIZE; i++) {
        arr[i] = i;
    }

    int stepsLinear = 0;
    int stepsBinary = 0;

    int index1 = linearSearch(arr, SIZE, stepsLinear);
    int index2 = binarySearch(arr, SIZE, stepsBinary);

    cout << "Linear Search index: " << index1 << endl;
    cout << "Linear Search steps: " << stepsLinear << endl << endl;

    cout << "Binary Search index: " << index2 << endl;
    cout << "Binary Search steps: " << stepsBinary << endl;

    return 0;  
}
```

// Linear Search — O(N)  
// Binary Search — O(log N)    after k steps N/2^k=1  
  
5. 
//Pseudocode  
RandomSearch(vector, target)  
    a list of [0, 1, ..., n-1]  
    Shuffle the list of indices randomly  
    
    FOR each index IN shuffled_indices:  
        IF vector[index] == target:  
            RETURN index (Success)  
            
    RETURN -1 (Not Found)  

Best-Case: O(1) Average-Case: O(n) Worst-Case: O(n)  

```  
#include <iostream>  
#include <vector>  
#include <random>  
int main() {  
    const int SIZE = 100000;  
    std::vector<int> data(SIZE);  
    
}  
```  