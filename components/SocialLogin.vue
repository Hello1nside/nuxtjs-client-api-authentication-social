<template>
  <div class="social-login">
    <button @click="socialLogin('google')" class="social-login-btn google">
      <i class="fab fa-google"></i>
    </button>
    <button @click="socialLogin('facebook')" class="social-login-btn facebook">
      <i class="fab fa-facebook"></i>
    </button>
  </div>
</template>


<script>
    export default {
        methods: {
            socialLogin(service) {
                window.location.href = `${process.env.baseUrl}auth/login/${service}`;
            }
        }
    }
</script>

<style lang="scss" scoped>
  .social-login {
    display: flex;
    justify-content: center;
  }
  .social-login-btn {
    color: white;
    border-radius: 5px;
    background: #333;
    margin-bottom: 10px;
    border: none;
    margin-left: 5px;
    margin-right: 5px;
    width: 50px;
    height: 50px;
    font-size: 23px;
    cursor: pointer;

    &.google {
      background: #dd4b39;
    }

    &.facebook {
      background: #3B5998;
    }
  }
</style>
