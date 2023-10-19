<template>
  <div>Câu 1:</div>
  <div>Output: {{ newArr }}</div>
  <div>Câu 2: </div>
  <div>Fibonacci: {{ fibonacciRecursion(6) }}</div>
</template>

<script>
// @ is an alias to /src

import { ref } from "vue";
export default {
  name: "App",
  setup() {
    const arr = ref(["a", "b", 1, 2, "c", 8, 9]);
    const newArr = ref();
    function convertArray(arr) {
      var start = 0;
      var end = arr.length - 1;
      const lengthArray = arr.length;
      for (start; start < (lengthArray - 1) / 2; start++) {
        if (!Number.isFinite(arr[start])) {
          for (let j = end; j > (lengthArray - 1) / 2; j--) {
            if (!Number.isFinite(arr[j])) {
              var temp = arr[start];
              arr[start] = arr[j];
              arr[j] = temp;
              end = j;
              start++;
            }
          }
        }
      }

      return arr;
    }

    function fibonacciRecursion(num) {
      if (num < 2) {
        return num;
      }
      return fibonacciRecursion(num - 1) + fibonacciRecursion(num - 2);
    }

    newArr.value = convertArray(arr.value);
 
    return {
      newArr,
      fibonacciRecursion
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
