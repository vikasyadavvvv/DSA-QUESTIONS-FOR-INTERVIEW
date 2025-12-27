## 1.Find the largest and smallest element in an array
```javascript
function findLargestandSmallestElment(arr){
    let min=arr[0]
    let max=arr[0]
    for(let i=1;i<arr.length;i++){
        if(arr[i]>max) max=arr[i]
        if(arr[i]<min) min=arr[i]
    }
    return {max,min}
}
console.log(findLargestandSmallestElment([1,2,3,4,5,6,78]))
```

## 2.Reverse an array
```javascript
function reverseArray(arr){
    let left=0
    let right=arr.length-1
    while(left<right){
        let temp=arr[left]
        arr[left]=arr[right]
        arr[right]=temp
        left++
        right--
    }
    return arr
}
console.log(reverseArray([1,2,3,4,5,6,7]))
```
## 3.Check if an array is sorted
```javascript
function isArraySorted(arr){
    for(let i=0;i<arr.length;i++){
        if(arr[i]>arr[i+1]) return false
    }
    return true
}
console.log(isArraySorted([1,2,3,4,4,4]))
```

## 4.Find the second largest element
```javascript
function secondLargest(arr) {
  let largest = -Infinity
  let seocnd = -Infinity
  for (let num of arr) {
    if (num > largest) {
      second = largest
      largest = num
    }
    else if (num < largest && num > second) {
      second = num
    }
  }
  return second === -Infinity ? -1 : second
}
console.log(secondLargest([1, 2, 3, 4, 5, 6]))
```
## 3.Count even and odd numbers
```javascript
function countEvenOdd(arr){
    let even=0
    let odd=0
    for(let num of arr){
        if(num % 2===0) even ++
        else{
            odd++
        }
    }
    return {even,odd}
}
console.log(countEvenOdd([1,2,3,4,5]))

```

## 4.Remove duplicates from a sorted array
```javascript
function uniqueElement(arr){
    let k=1
    for(let i=1;i<arr.length;i++){
        if(arr[i]!==arr[i-1]){
            arr[k]=arr[i]
            k++
        }
    }
    return k
}
console.log(uniqueElement([1,2,2,2,3,4,5]))
```

## 5.Rotate array by K positions
```javascript
function rotateArray(arr,k){
    const n=arr.length;
    if(n === 0) return arr;
    k = k % n;
    reverse(arr,0,n-1)
    reverse(arr,0,k-1)
    reverse(arr,k,n-1)
    
   return arr
}

function reverse(arr,left,right){
    while(left<right){
        let temp=arr[left]
        arr[left]=arr[right]
        arr[right]=temp
        left++
        right--
    }
}
console.log(rotateArray([1,2,3,4,5,6],3))
```
## 6.Move all zeros to the end
```javascript
function moveZero(arr){
    let k=0;
    for(let i=0;i<arr.length;i++){
        if(arr[i]!==0){
            arr[k]=arr[i]
            k++
        }
    }
    while(k<arr.length){
        arr[k]=0
        k++
    }
    return arr
}
console.log(moveZero([1,2,3,4,5,0,6,6,6,0,8]))
```
## Find the sum of array elements
```javascript
function sumofElement(arr){
    let sum=0;
    for(let i=0;i<arr.length;i++){
        sum+=arr[i]
    }
    return sum
}
console.log(sumofElement([1,2,3,4,5]))
```
