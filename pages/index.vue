<template>
  <div id="main" class="">
    <div class="h-[42px] mt-[40px]">
      <AppHead class=" " />
    </div>
    <div>
      <SignIn class="" />
    </div>
  </div>
</template>

<script>
import SignIn from '../components/SignIn.vue'
import AppHead from '../components/svgs/AppHead.vue'
export default {
  components: { SignIn, AppHead },
  name: 'IndexPage',
}
</script>

<style>
* {
  font-family: 'Poppins', sans-serif;
}
</style>
