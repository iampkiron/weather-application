<template>
  <header class="header">
    <h2>날씨봐라</h2>
    <p>{{ username }}님 반갑습니다.</p>
  </header>
</template>

<script>
export default {
  name: "headerDisplay",
  data() {
    return {
      username: "박 순철",
    };
  },
};
</script>

<style scoped>
.header {
  background-image: linear-gradient(135deg, #fdfcfb 0%, #e2d1c3 100%);
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1em;
}

.header h2 {
  color: #ff7f50;
}

.header p {
  font-size: 12px;
}
</style>
