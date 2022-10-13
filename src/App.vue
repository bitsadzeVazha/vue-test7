<template>
  <h2>My Course Goal</h2>
  <!-- Task 1: Output your main course goal with help of the composition API -->
  <!-- Don't hardcode it into the template, instead hardcode it into the JS code -->
  <h3 v-if="visible" >{{ goal }}</h3>
  <!-- Task 2: Toggle (show/ hide) the goal with help of the button  -->
  <button @click="visibility">Toggle Goal</button>
  <!-- Task 3: Manage data in three ways -->
  <!-- => Separate refs -->
  <!-- => Ref Object -->
  <!-- => Reactive Object -->
  <!-- Task 4: Also solve the assignment with the Options API -->
</template>

<script>
import {ref} from 'vue';
export default {
  setup(){
    // 1. Separete refs
    const goal = ref('Learn Vue.js');
    const visible = ref("true");

    function visibility(){
      visible.value = !visible.value;
    }
  
   return {goal, visible, visibility}
    
    // 2. Ref object
    //   const data = ref({
    //   goal: 'Vue.js',
    //   visible: true
    // })

    // function objVisibility(){
    //   data.value.visible = !data.value.visible;
    // }

    // return{goal: data.value.goal, data, objvisibility }

    // 3. Reactive Object
    // const data = reactive({
    //   goal: 'Learn Vue.js');
    //   visible: true;
    // })

    // function objVisibility(){
    //   data.visible = !data.visible
    // }

    // return{goal: data.goal, data, objvisibility }

    // 4. Options API
    // data(){
    //   return{
    //     goal: 'Vue.js',
    //     visible: true
    //   }
    // },

    // methods: {
    //   isVisible(){
    //     this.visible = !this.visible
    //   }
    // }

  }
}
</script>

<style>
html {
  font-family: sans-serif;
}
body {
  margin: 3rem;
  text-align: center;
}
</style>