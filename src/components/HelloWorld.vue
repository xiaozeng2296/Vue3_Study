<template>
  <h1>一个人的信息</h1>
  姓<input type="text" v-model="person.firstName" />
  <br />
  <br />
  名<input type="text" v-model="person.lastName" />
  <br />
  hobby: <input type="text" v-model="person.hobby.test1.test2.test3">
  全名：<span>{{ fullName }}</span>
</template>

<script setup>
import { ref, computed } from "vue";
const person = ref({
  firstName: "曾",
  lastName: "佳辉",
  hobby: {
    test1: {
      test2: {
        test3: "jfalskd",
      },
    },
  },
});
const fullName = computed(
  () =>
    person.value.firstName +
    person.value.lastName +
    person.value.hobby.test1.test2.test3
);
</script>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
