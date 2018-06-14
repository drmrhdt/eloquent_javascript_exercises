## 1. The sum of a range.

```function range(start, end, step = 1) {
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
