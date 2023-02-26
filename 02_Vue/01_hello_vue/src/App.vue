<script>
import MyButton from "./components/MyButton.vue";

export default {
  data() {
    return {
      message: "你好Vue",
    };
  },
  components: {
    MyButton,
  },
};
</script>

<template>
  <div>{{ message }}</div>
  <MyButton></MyButton>
</template>
