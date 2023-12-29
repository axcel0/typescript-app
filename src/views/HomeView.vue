<template>
  <div class="home">
    <img 
      src="https://media.licdn.com/dms/image/C5603AQF10D_OwmIxKg/profile-displayphoto-shrink_800_800/0/1629314160569?e=1709164800&v=beta&t=CCEgWZsuSByglMgtQBHFHiY8tzTay0hXPFAG8FPz3Yo" 
      alt="Profile Picture" 
      class="profile-picture"
    >
    <h2>Your Name</h2>
    <p>This is a web to show my profile. Here you can learn more about me, my skills, and my work.</p>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  components: {
  },
})
export default class HomeView extends Vue {}
</script>

<style scoped>
.profile-picture {
  width: 200px;
  height: 200px;
  border-radius: 50%;
}
</style>