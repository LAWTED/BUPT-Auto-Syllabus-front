<template>
  <div class="container">
    <n-card size="small">
      <n-space>
        <n-input v-model="user" type="text" placeholder="学号" />
        <n-input v-model="password" type="password" show-password-on="mousedown" placeholder="密码" :maxlength="8" round />
        <n-button @click="handleClick">submit</n-button>
      </n-space>
    </n-card>
  </div>
</template>

<script setup lang="ts">
import { NInput, NButton, NCard, NSpace} from "naive-ui";
import { ref } from "vue";
import axios from "axios";
const user = ref(null);
const password = ref(null);
const handleClick = () => {
  const api = "www.baidu.com";
  axios.get(api).then((res: any) => {
    console.log(res);
  });
};
</script>



<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.container {
  width: 200px;
  height: 400px;
  margin: auto;
}
</style>
