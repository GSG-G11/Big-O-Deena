```js
// 1.
==> O(n) ==>time
==> O(1) ==> space
function logUpTo(n) {
  for (let i = 1; i <= n; i++) {
    console.log(i);
  }
}

// 2.
==> O(1) ==>time
==> O(1) ==> space
function logAtMost10(n) {
  for (let i = 1; i <= Math.min(n, 10); i++) {
    console.log(i);
  }
}

// 3.
==> O(n) ==>time
==> O(1) ==> space
function logAtLeast10(n) {
  for (let i = 1; i <= Math.max(n, 10); i++) {
    console.log(i);
  }
}

// 4.
==> O(n) ==>time
==> O(n) ==> space
function onlyElementsAtEvenIndex(array) {
  let newArray = Array(Math.ceil(array.length / 2));
  for (let i = 0; i < array.length; i++) {
    if (i % 2 === 0) {
      newArray[i / 2] = array[i];
    }
  }
  return newArray;
}

// 5.
==> O(n^2) ==>time
==> O(n) ==> space
function subtotals(array) {
  let subtotalArray = Array(array.length);
  for (let i = 0; i < array.length; i++) {
    let subtotal = 0;
    for (let j = 0; j <= i; j++) {
      subtotal += array[j];
    }
    subtotalArray[i] = subtotal;
  }
  return subtotalArray;
}
```
