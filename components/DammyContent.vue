<template>
  <div>
    <SkeletonScreen v-if="loading" />
    <div v-else class="box">
      <h1>タイトル</h1>
      <p>テキストテキストテキストテキストテキスト</p>
    </div>
  </div>
</template>

<script>
import SkeletonScreen from '@/components/SkeletonScreen'
export default {
  components: {
    SkeletonScreen,
  },
  data() {
    return {
      loading: true,
    }
  },
  created() {
    setTimeout(() => {
      this.loading = false
    }, 3000)
  },
}
</script>

<style scoped>
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
