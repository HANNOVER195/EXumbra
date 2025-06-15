<template>
  <div class="min-h-screen flex items-center justify-center bg-gray-100">
    <div class="w-full max-w-md p-8 bg-white shadow-md rounded-xl">
      <h2 class="text-2xl font-bold text-center text-gray-800 mb-6">Iniciar Sesión</h2>
      <form @submit.prevent="handleLogin">
        <div class="mb-4">
          <label class="block text-gray-700 mb-2" for="email">Correo electrónico</label>
          <input
            v-model="email"
            id="email"
            type="email"
            placeholder="tucorreo@example.com"
            class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-400"
            required
          />
        </div>
        <div class="mb-6">
          <label class="block text-gray-700 mb-2" for="password">Contraseña</label>
          <input
            v-model="password"
            id="password"
            type="password"
            placeholder="••••••••"
            class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-400"
            required
          />
        </div>
        <button
          type="submit"
          class="w-full bg-blue-600 text-white py-2 px-4 rounded-lg hover:bg-blue-700 transition duration-200"
        >
          Ingresar
        </button>
      </form>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const email = ref('')
const password = ref('')

function handleLogin() {
  console.log('Email:', email.value)
  console.log('Password:', password.value)
  alert('Login enviado (ver consola). Aquí podrías conectar con tu backend.')
}
</script>
