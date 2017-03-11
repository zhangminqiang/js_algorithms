#### 快速排序
什么是快速排序？选一个基准值（一般选第一个或最后一个）将数组分为两边，大于这个值的放一边，小于这个值得放另一边。然后对两边重复同意操作，直到只剩一项。
function quicksort(arr){
    var left = [], 
        right = [], 
        i = 1,
        len = arr.length,
        current = arr[0];

    if(arr.length < 2){
        return arr;
    }

    for(;i<len;i++){
        if(arr[i] < current){
            left.push(arr[i]);
        }else{
            right.push(arr[i]);
        }
    }

    left = quicksort(left);
    right = quicksort(right);

    return left.concat(current).concat(right);
}
