# Count of positives / sum of negatives

## Problem 

Create a function that takes an array of integers as an argument and returns an array, where the first element is the count of positive numbers and the second element is sum of negative numbers.

---
## Example

Input: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15].

Output: [10, -65].

onst countOfPositives_SumOfNegatives = function(Array){
   const result=[0,0];
    for(let i=0;i<Array.length;i++){
    if(Array[i]<=0){
        result[1]=result[1]+Array[i];
    }else result[0]=result[0]+1;
}
return result;
}
const Input=[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15];
countOfPositives_SumOfNegatives(Input);

//another sloustion.....................

//  Declare the function with an array as an arguement
const countPosSumNeg = function(numsArr) {
  // Declare the output array variable
  const outArr = [0, 0];
  // For loop that will iterate through the input array
  for (let i = 0; i < numsArr.length; i++) {
    // Get the current array element, in a seperate variable
    const element = numsArr[i];
    // Check if the element positive, then count it and add it to output array
    if (element > 0) {
      // Counting the positive numbers
      outArr[0] = outArr[0] + 1;
    } // Else some other
    else {
      // Sum the negative and zero numbers
      outArr[1] = outArr[1] + element;
    }
  }
  // Return the output array
  return outArr;
};
---
## Bonus
If the input array is empty or null, return an empty array.
const
