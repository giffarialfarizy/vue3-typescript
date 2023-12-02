<template>
  <div class="app">
    <!-- <p>{{ jobs[0].title }}</p> -->
    <pre>{{ jobs }}</pre>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from "vue";
import Job from "@/types/Job";

export default defineComponent({
  name: "App",
  components: {},
  setup() {
    // --- using reactive ---
    // const state = reactive({
    //   name: "Link",
    //   age: 25 as string | number,
    // });

    // return { ...toRefs(state) };

    // --- using ref ---
    // const name = ref<string>("Link");
    // const age = ref<number | string>(25);

    // return { name, age };

    const jobs = ref<Job[]>([
      {
        title: "Farm worker",
        location: "Bandung",
        salary: 1000,
        id: "2",
      },
      {
        title: "Fisherman",
        location: "Pangandaran",
        salary: 1050,
        id: "1",
      },
    ]);

    return { jobs };
  },
  // data() {
  //   return {
  //     name: "Link",
  //     age: 25 as number | string,
  //   };
  // },
  // methods: {
  //   changeName(name: string) {
  //     this.name = name;
  //     return name;
  //   },
  //   changeAge(age: number) {
  //     this.age = age;
  //     return age;
  //   },
  // },
});
</script>
