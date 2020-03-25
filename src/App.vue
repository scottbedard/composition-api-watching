<template>
  <div>
    <input v-model="foo" type="number">
    <Child :obj="{ foo }"/>
  </div>
</template>

<script>
import Child from "./Child.vue";

export default {
  data() {
    return {
      foo: 1
    };
  },
  components: {
    Child
  }
};
</script>