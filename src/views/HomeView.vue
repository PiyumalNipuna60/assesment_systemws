<template>
  <div class="navigation-panel">
    <ul>
      <li v-for="item in navigationItems" :key="item.text">
        <router-link :to="item.route">{{ item.text }}</router-link>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue'
import TheWelcome from '../components/TheWelcome.vue'
const navigationItems = [
  { text: 'Home', route: '/' },
  { text: 'About', route: '/about' },
  { text: 'Contact', route: '/contact' }
]
const items = ref([])

onMounted(() => {
  items.value = [
    {
      title: 'Home',
      icon: ''
    },
    {
      title: 'Home',
      icon: ''
    }
  ]
})
</script>
