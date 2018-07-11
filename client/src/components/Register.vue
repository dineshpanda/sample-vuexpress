<template>
  <div id="app">
    <v-app>
      <v-form ref="form">
        <v-text-field
          v-model="email"
          label="E-mail"
          required
        ></v-text-field>
        <v-text-field
            v-model="password"
            :type="show1 ? 'text' : 'password'"
            label="Password"
            hint="At least 8 characters"
            counter
          ></v-text-field>
        <v-btn @click.prevent="submit">submit</v-btn>
    </v-form>
  </v-app>
</div>
</template>

<script>
import AuthenticationService from '@/services/AuthenticationService'

export default {
  data () {
    return {
      email: '',
      password: '',
      show1: false
    }
  },
  methods: {
    async submit () {
      const res = await AuthenticationService.register({
        email: this.email,
        password: this.password
      })
      console.log(res.data);
    }
  }
}
</script>
