<script setup>
import { ref } from 'vue';

const fortunes = [
  "You will have a great day!",
  "Success is coming your way.",
  "A pleasant surprise awaits you.",
  "Expect good news soon.",
  "Happiness is just around the corner.",
  "An exciting opportunity is on its way.",
  "You will make a new friend soon.",
  "Your hard work will pay off.",
  "Good things take time, be patient.",
  "Adventure awaits you!"
];

const fortune = ref("");

const getFortune = () => {
  const randomIndex = Math.floor(Math.random() * fortunes.length);
  fortune.value = fortunes[randomIndex];
};
</script>

<template>
  <div id="app">
    <h1>Fortune Teller</h1>
    <button @click="getFortune">Get Your Fortune</button>
    <p id="fortuneDisplay" v-if="fortune">{{ fortune }}</p>
  </div>
</template>

<style scoped>
#fortuneDisplay {
  font-size: 20px;
  font-weight: bold;
  color: #333;
  margin-top: 15px;
  padding: 10px;
  border: 2px solid #4CAF50;
  border-radius: 5px;
  display: inline-block;
  background-color: #f9f9f9;
}
</style>
