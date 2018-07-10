<template>
  <v-container fluid>
    <v-layout column>
      <v-flex xs12>
        <v-form>
          <v-text-field
            v-model="email"
            label="E-mail"
            required>
            </v-text-field>
        </v-form>
        </v-form>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      email: ''
    }
  }
}
</script>

<style>
  @import '~vuetify/src/stylus/main'
</style>

