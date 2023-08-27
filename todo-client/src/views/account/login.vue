<template>
  <svg class="login__image-animate blob1" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
    <path fill="#FF0066" d="M66.1,-23.3C70.3,-8.7,47.6,12.8,23.4,29.9C-0.9,47,-26.7,59.7,-38,51.7C-49.3,43.6,-46,14.9,-37.2,-6C-28.4,-26.9,-14.2,-40,8.4,-42.7C31,-45.4,62,-37.8,66.1,-23.3Z" transform="translate(100 100)" />
  </svg>
  <svg class="login__image-animate blob2" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
    <path fill="#FF0066" d="M26.9,-14.3C38.3,4.3,53.4,21.9,49.5,36.2C45.7,50.5,22.8,61.5,0.7,61.1C-21.4,60.7,-42.8,48.9,-47.4,34.2C-52,19.4,-39.8,1.7,-29.1,-16.4C-18.4,-34.6,-9.2,-53.3,-0.7,-52.9C7.7,-52.5,15.5,-32.9,26.9,-14.3Z" transform="translate(100 100)" />
  </svg>
  <div class="login">
    <div class="login__left"></div>
    <div class="login__right">
      <div class="login__right__logo">
        <img class="login__right__logo--img" src="../../assets/logo.svg">
      </div>
      <div class="login__right__header">
        <p class="login__right__header--title">
          Hello Again !
        </p>
        <p class="login__right__header--description">
          login please
        </p>
      </div>
      <div class="login__right__form">
        <form class="login__right__form--input">
          <input class="login__right__form--input__email" type="text" placeholder="email">
          <input class="login__right__form--input__password" type="password" placeholder="password">
          <div class="login__right__form--input--rememberMe">
            <input class="login__right__form--input--rememberMe__input" id="rememberMe" type="checkbox">
            <label class="login__right__form--input--rememberMe__label" for="rememberMe">Remember Me</label>
            <div class="login__right__form--input--rememberMe__recovery">
              <RouterLink class="login__right__form--input--rememberMe__recovery--tag" to="#">Recovery Password</RouterLink>
            </div>
          </div>

          <div class="login__right__form--input__submit">
            <button class="login__right__form--input__submit__loginBox">login</button>
            <button class="login__right__form--input__submit__signInBox">
              <img class="login__right__form--input__submit__signInBox--img" src="../../assets/images/download%20(1).jfif">
              <p>sign in with google</p>
            </button>
          </div>
        </form>
      </div>
      <div class="login__right__fotter">
        <p class="login__right__fotter--question">Dont have an account yet ?</p>
        <RouterLink class="login__right__fotter--answer" to="#">sign up</RouterLink>
      </div>
    </div>

  </div>
</template>

<script setup>
</script>

<style scoped>
.login {
  display: flex;
  justify-content: center;
  margin: 20px auto;
  width: 80vw;
  height: 80vh;
  border-radius: 16px;
  box-shadow: 0px 5px 15px rgba(0, 0, 0, 0.25);
  overflow: hidden;
}

.login__image-animate {
  position: absolute;
  max-width: 50px;
  animation-name: rotation;
  animation-direction: alternate;
  animation-duration: 5s;
  animation-iteration-count: infinite;
}

.blob1 {
  left: 100px;
}

bolob2 {
  right: 100px;
}

.login__left {
  background-color: cornflowerblue;
  flex-basis: 50%;
}

.login__right {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  flex-basis: 50%;
}

.login__right__logo {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 60px;
  height: 60px;
  border: 0px solid black;
  background-color: #282828;
  border-radius: 50%;

}

.login__right__logo--img {
  width: 40px;
}

.login__right__header {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.login__right__header--title {
  font-size: 30px;
}

.login__right__form {
  display: flex;
  flex-direction: column;
  padding: 30px;
}

.login__right__form--input {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: start;
}

.login__right__form--input__email {
  margin-bottom: 20px;
  width: 250px;
  height: 30px;

}

.login__right__form--input__password {
  height: 30px;
  width: 250px;

}

.login__right__form--input--rememberMe {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 15px;
}

.login__right__form--input--rememberMe__label {
  font-size: 10px;
  margin-right: 80px;
}
.login__right__form--input--rememberMe__recovery--tag{
  font-size: 11px;
  color: blue;
}

.login__right__form--input__submit {
  display: flex;
  flex-direction: column;
  width: 250px;
  margin-top: 30px;

  margin-bottom: 60px;

}

.login__right__form--input__submit__loginBox {
  margin: 3px;
  border-radius: 5px;
  background-color: dodgerblue;
  height: 30px;
  color: white;

}

.login__right__form--input__submit__signInBox {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 3px;
  border-radius: 5px;
  height: 30px;
  background-color: white;
}
.login__right__form--input__submit__signInBox--img{
  width: 20px;
}
.login__right__fotter{
  display: flex;
  align-items: center;
  justify-content: space-between;

}
.login__right__fotter--question{
  font-size: 10px;
  margin-right: 10px;

}
.login__right__fotter--answer{
  font-size: 15px;
  color: blue;
}

@keyframes rotation {
  0% {
    transform: rotate(0) scale(1);
  }
  50% {
    transform: rotate(180deg) scale(1.5);
  }
  100% {
    transform: rotate(360deg) scale(2);
  }
}
</style>