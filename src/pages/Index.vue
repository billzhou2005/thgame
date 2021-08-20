<template>
  <q-div class="q-gutter-y-md column" style="max-width: 300px">
      <br>
      <br>
      <q-input v-model="email" filled type="email" hint="Email" />
      <q-input filled square v-model="username" hint="Please input user name" :dense="dense" />
      <q-input v-model="password" filled :type="isPwd ? 'password' : 'text'" hint="Please input your password">
        <template v-slot:append>
          <q-icon
            :name="isPwd ? 'visibility_off' : 'visibility'"
            class="cursor-pointer"
            @click="isPwd = !isPwd"
          />
        </template>
      </q-input>
      <br>
      <br>
      <q-btn color="secondary" icon-right="done" label="Register" />

  </q-div>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'PageIndex',
  setup () {
    return {
      email: ref(''),
      password: ref(''),
      isPwd: ref(true),
      username: ref(''),
      ph: ref(''),
      dense: ref(false)
    }
  }
})
</script>
