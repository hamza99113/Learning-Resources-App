<template>
  <!-- <ul>
    <LearningResource
      v-for="resource in storedResources"
      :key="resource.id"
      :title="resource.title"
      :description="resource.description"
      :link="resource.link"
    />
  </ul> -->
  <div>
    <TheHeader title="Remember Me"/>
    <StoredResources :resources="storedResources"/>
  </div>
  
</template>

<script>
// import LearningResource from './components/learning-resources/LearningResource.vue';
import TheHeader from './components/layouts/TheHeader.vue';
import StoredResources from './components/learning-resources/StoredResources.vue';
export default {
  components: {
    // LearningResource,
    TheHeader,
    StoredResources
  },
  data() {
    return {
      storedResources: [
        {
          id: 'official-guide',
          title: 'Official Guide',
          description: 'The official Vue.js documentation.',
          link: 'https://vuejs.org/',
        },
        {
          id: 'google',
          title: 'Google',
          description: 'Learn more about google.',
          link: 'https://google.org/',
        },
      ],
    };
  },
};
</script>


<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
  box-sizing: border-box;
}

html {
  font-family: 'Roboto', sans-serif;
}

body {
  margin: 0;
}
</style>