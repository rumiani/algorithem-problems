# 60 Algorithem-Problems sloved by `TypeScript`
Source: [codesignal.com](https://codesignal.com)

# 1- Add
Write a function that returns the sum of two numbers.
Example
For `param1 = 1` and `param2 = 2`, the output should be `solution(param1, param2) = 3`.

## Solution:
```typescript
function solution (param1: number, param2: number): number {
    return param1 + param2 ;
}
```
Link to the problem number 1 for testing: [Test out the solution here](https://app.codesignal.com/arcade/intro/level-1/jwr339Kq6e3LQTsfa)

# 2- Century From Year
Given a year, return the century it is in. The first century spans from the year 1 up to and including the year 100, the second - from the year 101 up to and including the year 200, etc.

Example

   * For `year = 1905`, the output should be
    `solution(year) = 20`;
   * For `year = 1700`, the output should be
    `solution(year) = 17`.


## Solution:
```typescript
function solution(year: number): number {
    return Math.floor((year - 1) / 100) + 1 ;
}
```
Link to the problem number 2 for testing: [Test out the solution here](https://app.codesignal.com/arcade/intro/level-1/egbueTZRRL5Mm4TXN)

# 3- Check Palindrome 
Given the string, check if it is a palindrome.

Example

   For `inputString = "aabaa"`, the output should be
   `solution(inputString) = true`;
   For `inputString = "abac"`, the output should be
   `solution(inputString) = false`;
   For `inputString = "a"`, the output should be
   `solution(inputString) = true`.


## Solution:
```typescript
function solution(inputString: string): boolean {
    return inputString.split("").reverse().join("") == inputString ;
}
```
Link to the problem number 3 for testing: [Test out the solution here](https://app.codesignal.com/arcade/intro/level-1/s5PbmwxfECC52PWyQ)

# 4- Adjecent Elements Product
Given an array of integers, find the pair of adjacent elements that has the largest product and return that product.

Example

For `inputArray = [3, 6, -2, -5, 7, 3]`, the output should be
`solution(inputArray) = 21`.

`7` and `3` produce the largest product.


## Solution:
```typescript
function solution(inputArray: number[]): number {
let num:number = inputArray[0] * inputArray[1] ;
for (let i in inputArray){
  let a = inputArray[+i] * inputArray[+i+1] ;
  if(a > num ) num = a ;
}
return num
}
```
Link to the problem number 4 for testing: [Test out the solution here](https://app.codesignal.com/arcade/intro/level-2/xzKiBHjhoinnpdh6m)

# 5- Shape Area
Below we will define an n-interesting polygon. Your task is to find the area of a polygon for a given n.

A 1-interesting polygon is just a square with a side of length 1. An n-interesting polygon is obtained by taking the n - 1-interesting polygon and appending 1-interesting polygons to its rim, side by side. You can see the 1-, 2-, 3- and 4-interesting polygons in the picture below:

![ Polygon Picture](https://codesignal.s3.amazonaws.com/uploads/1664318501/area.png "Polygon Picture from Codesignal website")

Example

   * For `n = 2`, the output should be
    `solution(n) = 5`;
   * For `n = 3`, the output should be
    `solution(n) = 13`.

## Solution:
```typescript
function solution(n: number): number {
return (n**2 + (n-1)**2);
}
```
Link to the problem number 5 for testing: [Test out the solution here](https://app.codesignal.com/arcade/intro/level-2/yuGuHvcCaFCKk56rJ)

# 6- Make Array Consecutive 2
Ratiorg got statues of different sizes as a present from CodeMaster for his birthday, each statue having an non-negative integer size. Since he likes to make things perfect, he wants to arrange them from smallest to largest so that each statue will be bigger than the previous one exactly by 1. He may need some additional statues to be able to accomplish that. Help him figure out the minimum number of additional statues needed.

Example

For `statues = [6, 2, 3, 8]`, the output should be
`solution(statues) = 3`.

Ratiorg needs statues of sizes `4`, `5` and `7`.
## Solution:
```typescript
function solution(statues: number[]): number {
statues.sort((a,b) => a-b) ;
return statues[statues.length -1 ] - statues[0] +1 - statues.length ;
}

```
Link to the problem number 6 for testing: [Test out the solution here](https://app.codesignal.com/arcade/intro/level-2/bq2XnSr5kbHqpHGJC)
