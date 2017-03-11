
> /**
 * 冒泡算法（升序）：两个值比较，较大的值往后移
 */
function bubbleSorting(arr){
    var i= arr.length, j, gtVal;

    while(i > 0){
        for(j=0;j<i-1;j++){
            if(arr[j] > arr[j+1]){
                gtVal = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = gtVal;
            }
        }

        i--;
    }

    return arr;
}
