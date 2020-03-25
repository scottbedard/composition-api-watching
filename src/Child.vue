<template>
  <div>
    <pre>{{ $props }}</pre>
  </div>
</template>

<script>
import { watch } from "@vue/composition-api";

const useThing = obj => {
  watch(
    () => obj.foo,
    () => {
      console.log("useThing");
    }
  );
};

export default {
  setup(props) {
    useThing(props.obj);

    watch(
      () => props.obj.foo,
      () => {
        console.log("setup");
      }
    );
  },
  props: ["obj"]
};
</script>