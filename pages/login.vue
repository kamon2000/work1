<template>
  <v-app>
    <br>
    <center>
      <v-card width="420">
        <v-card-title>
          <h1>Login</h1>
        </v-card-title>
        <v-card-text>
          <v-form>
            <v-text-field label="Username"
                          prepend-icon="mdi-account-circle"
            />
          </v-form>

          <v-form>
            <v-text-field
              :type="showPassword ? 'text' : 'password'"
              label="Password"
              prepend-icon="mdi-lock"
              :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
              @click:append="showPassword = !showPassword"
            />
          </v-form>

          <v-card-actions>
            <nuxt-link to="register">
              <v-btn depressed large color="success">
                Ragister
              </v-btn>
            </nuxt-link>
            <v-spacer />
            <nuxt-link to="">
              <v-btn depressed large color="primary">
                Login
              </v-btn>
            </nuxt-link>
          </v-card-actions>
        </v-card-text>
      </v-card>
    </center>
  </v-app>
</template>
<script>
export default {
  name: 'App',
  data () {
    return {
      showPassword: false,
    }
  },
}
</script>
