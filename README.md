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
        temp=arr[right]
        left++
        right--
    }
    return arr
}
console.log(reverseArray([1,2,3,4,5,6,7]))
```
