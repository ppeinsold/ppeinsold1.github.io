<template>
  <div class="resume">
    <div class="top-container">
      <Header/>
    </div>
    <div class="bottom-container">
      <div class="left-container">
        <Personal-Profile/>
        <Contact/>
      </div>
      <div class="right-container">
        <Skills/>
        <Work-Experience/>
        <Education/>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Header from '@/components/Header.vue';
import PersonalProfile from '@/components/PersonalProfile.vue';
import Skills from '@/components/Skills.vue';
import Contact from '@/components/Contact.vue';
import WorkExperience from '@/components/WorkExperience.vue';
import Education from '@/components/Education.vue';

@Options({
  components: {
    Header, PersonalProfile, Skills, Contact, WorkExperience, Education
  },
})
export default class Home extends Vue {}
</script>


<style scoped lang="scss">
  .resume{
    display: flex;
    flex-direction: column;

    .top-container{
      background-color: #181e30;
      max-height: 220px;
      overflow: hidden;
    }

    .bottom-container{
      display: flex;
      flex-direction: row;
      color: #f2f2f2;

      .left-container{
        display: flex;
        flex-direction: column;
        flex-grow: 1;
        min-height: 100vh;
        padding: 20px;

        background-color: rgba(29,37,59,.95);
      }

      .right-container{
        display: flex;
        flex-direction: column;
        flex-grow: 2;
        min-height: 100vh;
        padding: 20px;

        background-color: #1d253b;
      }
    }
  }
</style>