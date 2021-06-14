<template>
  <v-main>
    <v-card width="500" class="mx-auto mt-9">
      <v-card-title>Login</v-card-title>
      <v-card-text>
        <v-text-field
          v-model="username"
          :rules="nameRules"
          label="Username"
          prepend-icon="mdi-account-circle"
          required
        ></v-text-field>

        <v-text-field
          v-model="password"
          :rules="passwordRules"
          label="Password"
          :type="showPassword ? 'text' : 'password'"
          prepend-icon="mdi-lock"
          :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
          @click:append="showPassword = !showPassword"
          required
        ></v-text-field>
      </v-card-text>
      <v-divider />
        <v-card-actions justify="center">
          <v-btn color="success" @click="login"> Login </v-btn>
        </v-card-actions>
    </v-card>
  </v-main>
</template>
<script>
export default {
  data: () => ({
    valid: false,
    username: "",
    password: "",
    nameRules: [(v) => !!v || "username is required"],
    passwordRules: [(v) => !!v || "Password is required"],
    showPassword: false
  }),
  props: {
  },
  methods: {
    login(){
      if(this.username.toLowerCase() === "bebeto" && this.password === "tfeb18g3") alert("Logging in")
      else alert("Invalid credentials" + this.username.toLowerCase() + this.password)
    }
  }
};
</script>