## 1. The sum of a range.

```
function range(start, end, step = 1) {
	let array = [];
	
	if (step > 0) {
		for(let i = start; i < end; i += step) {
			if(i == start) array.push(i); 
			array.push(i + step);
    	}
    } 
    else if (step < 0) {
		for(let i = start; i > end; i += step) {
			if(i == start) array.push(i); 
			array.push(i + step);
    	}
    }

	return array; 
}

function sum(array) {
	let sum = 0;
	
	for (let i = 0; i < array.length; i++) {
		sum += array[i];
    }
    
	return sum;
}

alert(sum(range(1, 10)));
```

## 2. Reversing an array

ReverseArray takes an array as argument and produces a new array that has the same elements in the inverse order.

```
function reverseArray(oldArr) {
	let newArr = [];
	for (let i = oldArr.length - 1; i >= 0; i--) {
		newArr.push(oldArr[i]);
    }
	return newArr;
}

let oldArr = [1, 2, 3];
alert(reverseArray(oldArr)); // 3, 2, 1
alert(oldArr) // 1, 2, 3
```

The second, reverseArrayInPlace, does what the reverse method does: it modifies the array given as argument by reversing its elements.
```
function reverseArrayInPlace(arr) {
	for(let i = 0; i < (arr.length) / 2; i++) {
		let tmp = arr[i];
		arr[i] = arr[arr.length - i - 1];
		arr[arr.length - i - 1] = tmp;
    }
	return arr;
}
let arr = [1, 2, 3];
alert(reverseArrayInPlace(arr)); // 3, 2 ,1
alert(arr); // // 3, 2 ,1
```
