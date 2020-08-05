#### implement binary search

```
const arr = [1, 3, 5, 7, 9, 10, 11, 12, 14, 15, 19, 20];
function binarySearch(arr, val) {
  var low = 0,
    high = arr.length - 1;
  while (low <= high) {
    var mid = parseInt((low + high) / 2);
    if (val == arr[mid]) {
      return mid;
    } else if (val > arr[mid]) {
      low = mid + 1;
    } else if (val < arr[mid]) {
      high = mid - 1;
    }
  }
  return -1;
}
console.log(binarySearch(arr, 10));
```
