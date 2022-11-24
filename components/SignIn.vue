<template>
  <div id="form-div" class="mt-[20px] p-[20px]">
    <div class="flex flex-col items-center max-w-[360px] mr-auto ml-auto">
      <p
        class="text-[21px] w-[100%] leading-[28px] font-bold text-black h-[28px]"
      >
        Sign In to WisdomCircle
      </p>
      <p class="text-[#606880] w-[100%] text-[14px] leading-[22px]">
        Don't have an account?
        <nuxt-link
          class="text-[14px] leading-[22px] text-[#2558E5] font-semibold"
          to="/signup"
          >Sign up</nuxt-link
        >
      </p>
    </div>
    <div>
      <form
        class="flex flex-col items-center max-w-[360px] mr-auto ml-auto"
        @submit.prevent="onSubmit"
      >
        <div
          class="w-[100%] h-10 px-[16px] py-[9px] rounded border border-[#DCDEE5] mt-[15px] border-style"
        >
          <input
            type="email"
            name="email"
            id="email"
            placeholder="Email Id or Mobile Number"
            class="text-[14px] w-[100%] placeholder:w-[100%] placeholder:h-auto placeholder:text-[14px] placeholder:leading-[22px] placeholder:text-[#606880] outline-none"
          />
        </div>
        <div
          class="w-[100%] rounded border border-[#DCDEE5] mt-[15px] text-sm h-10 justify-start items-center flex border-style"
        >
          <input
            :type="type"
            name="password"
            id="password"
            placeholder="Password"
            class="px-[16px] w-[90%] py-[9px] text-[14px] placeholder:w-[100%] placeholder:h-auto placeholder:text-[14px] placeholder:leading-[22px] placeholder:text-[#606880] outline-none"
          />
          <span @click="togglePassword"><Eye /></span>
        </div>
        <nuxt-link
          class="text-[12px] leading-[18px] font-semibold text-[#2558E5] w-[100] self-end"
          to="/reset"
          >Forgot password</nuxt-link
        >
        <input
          type="submit"
          value="Sign In"
          class="w-[100%] bg-[#F1C12B] h-auto font-semibold leading-[24px] rounded-[4px] mt-[260px] py-[8px]"
        />
      </form>
    </div>
  </div>
</template>

<script>
import Eye from './svgs/Eye.vue'
// import { Form, Field } from 'vee-validate';

export default {
  name: 'SignIn',
  data() {
    return {
      type: 'password',
    }
  },
  components: {
    Eye,
    // Form,
    // Field,
  },
  methods: {
    togglePassword() {
      if(this.type === 'password'){
        this.type = 'text';
      }
      else{
        this.type = 'password';
      }
    },
    onSubmit(){
       console.log('Submitting :(');
    }
  },
}
</script>

<style scoped>

</style>
