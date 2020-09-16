<template>
  <div class="box">
    <h1 class="title skeleton"></h1>
    <p class="text skeleton"></p>
    <p class="text skeleton"></p>
  </div>
</template>

<style scoped>
.skeleton {
  position: relative;
  overflow: hidden;
  background: #d9d9d9;
}
.skeleton::after {
  content: '';
  display: block;
  height: 100%;
  width: 100%;
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255, 255, 255, 0.5),
    transparent
  );
  position: absolute;
  top: 0;
  left: 0;
  animation: skeleton-animation 1.2s linear infinite;
}
.title {
  width: 90%;
  height: 40px;
  margin-bottom: 10px;
}
.text {
  height: 16px;
  margin-bottom: 5px;
}
@keyframes skeleton-animation {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(100%);
  }
}

.box {
  position: relative;
  top: 50px;
  left: 50px;
  width: 300px;
  min-height: 100px;
  padding: 10px;
  box-shadow: 0 2px 20px 0 rgba(0, 0, 0, 0.1);
  border-radius: 8px;
}
</style>
