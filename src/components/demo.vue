<template>
  <div>
    <div>
      <input v-validate="'required|email'" name="email" type="text">
    </div>
    <div>
      <span>{{ errors.first('email') }}</span>
    </div>
  </div>
</template>

<script>
import Vue from 'vue';
import VeeValidate, { Validator } from 'vee-validate';
import zh_TW from 'vee-validate/dist/locale/zh_TW';

Vue.use(VeeValidate);

Validator.localize('zh_TW', zh_TW);

export default {
  name: 'demo',
};
</script>
