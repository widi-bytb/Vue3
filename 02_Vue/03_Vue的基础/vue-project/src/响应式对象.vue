<script setup>
import { reactive, ref } from "vue";
const stu = reactive({
  name: "孙悟空",
});
// ref在生成响应式代理时，它是将值包装成了一个对象 0 --> {value:0}
// 访问ref对象时，必须通过 对象.value 来访问其中的值
// 在模板中，ref对象会被自动解包
let count = ref(0); //该变量只会影响到变量自己，在js中，无法实现对一个变量的代理

function func() {
  count.value++;
}
console.log(stu.name);
console.log(count);
</script>
<template>
  <div>
    <h1>组合式API</h1>
    <h2 @click="func">{{ count }}</h2>
  </div>
</template>
