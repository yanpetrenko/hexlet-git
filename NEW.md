const flatten = (arr) => {
const result = [];
for (const item of arr) {
  if (Array.isArray(item)) {
    const copy = [...item];
    for (const i of copy) {
      result.push(i);
    }
    continue;
  }
  result.push(item);
}
return result;
};
console.log(flatten([1, [3, 2], 9]))
const flatten = (coll) => { //более правильное решение
  let result = [];
  for (const item of coll) {
    if (Array.isArray(item)) {
      result = [...result, ...item];
    } else {
      result = [...result, item];
    }
  }

  return result;
};