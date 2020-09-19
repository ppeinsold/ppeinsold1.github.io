<template>
  <div>
    <img src="@/assets/profile.jpg">
    <vue-particles color="#dedede" :particlesNumber="120"></vue-particles>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  props: {
  },
  methods: {
  }
})
export default class Header extends Vue {
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  img{
    position: absolute;
    object-fit: cover;
    border-radius:50%;
    width: 200px;
    height: 200px;
    top: 10px;
    left: calc(50% - 100px);
  }
</style>
