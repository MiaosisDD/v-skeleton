<template>
  <div v-show="visible" class="skeleton-box">
    <div class='__row' v-for="(row, rindex) in COLUMNS" :key="rindex">
      <div class='__col' v-for="(col, cindex) in row" :key="cindex" :style='{width: col + "%"}'>
        <div class="__item"></div>
      </div>
    </div>
  </div>
</template>

<script>
const COLUMNS = [[83], [33, 62.5], [25, 75], [54, 37.5], [16.6, 12.5, 66.6]]

export default {
  data() {
    return {
      visible: false,
      COLUMNS
    }
  }
}
</script>

<style scoped>
@keyframes card-loading {
  0%,
  to {
    background-position: 0 50%;
  }

  50% {
    background-position: 100% 50%;
  }
}

.skeleton-none {
  display: none !important;
}

.skeleton-box {
  z-index: 5000;
  width: 100%;
  height: 140px;
  background: #fff;
  overflow: hidden;
}

.__item {
  height: 16px;
  background:
    linear-gradient(
      90deg,
      rgba(207, 216, 220, 0.2),
      rgba(207, 216, 220, 0.4),
      rgba(207, 216, 220, 0.2)
    );
  background-size: 600% 600%;
  border-radius: 2px;
  animation: card-loading 1.4s ease infinite;
  margin: 3px 0;
}

.__col {
  display: inline-block;
  padding: 0 5px;
  box-sizing: border-box;
}
</style>
