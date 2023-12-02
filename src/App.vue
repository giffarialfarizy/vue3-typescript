<template>
  <div class="app">
    <p>{{ name }} - {{ age }}</p>
    <button @click="changeName('Squirtle')">Change name!</button>
    <button @click="changeAge(30)">Change age!</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from "vue";

export default defineComponent({
  name: "App",
  components: {},
  setup() {
    // const state = reactive({
    //   name: "Link",
    //   age: 25 as string | number,
    // });

    // return { ...toRefs(state) };

    const name = ref<string>("Link");
    const age = ref<number | string>(25);

    return { name, age };
  },
  // data() {
  //   return {
  //     name: "Link",
  //     age: 25 as number | string,
  //   };
  // },
  methods: {
    changeName(name: string) {
      this.name = name;
      return name;
    },
    changeAge(age: number) {
      this.age = age;
      return age;
    },
  },
});
</script>
