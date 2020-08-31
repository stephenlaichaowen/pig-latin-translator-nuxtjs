<template>
  <div>
    <PageLoader />
    <nuxt />
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: sans-serif;
}

body {
  max-width: 1920px;
  margin: auto;
  padding: 2rem;
  min-height: 100vh;
  background: #aaa;
  color: rgba(255, 255, 255, 0.7);
  background-color: #6760aa;
}

.container {
  max-width: 650px;
  margin: 0 auto;
  /* padding: 0 25px; */
}

.header {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 50px;
  margin-bottom: 25px;
}

.header__title {
  font-size: 3rem;
}

.header__icon {
  max-height: 100px;
  margin-right: 20px;
}

.text-input__input {
  width: 100%;
  resize: none;
  padding: 15px;
  border-radius: 2px;
  border: none;
  box-shadow: 1px 1px 2px #7f9fd0;
  font-size: 14px;
  color: #6760aa;
}

.text-input__input:focus {
  outline: #7f9fd0 auto 2px;
}

.text-output {
  background-color: rgba(255, 255, 255, 0.7);
  color: #6760aa;
  padding: 15px;
}

@media (max-width: 470px) {
  .header {
    width: 100%;
  }
  .header__icon {
    width: 80px;
    height: 80px;
  }
  .header__title {
    font-size: 2rem;
  }
}
</style>
