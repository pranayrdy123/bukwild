<template>
  <div id="app">
    <div class="bg-light py-5">
      
      <header class="container">
        <ul
          class="nav float-right"
        >
          <li>
            <a
              class="btn btn-primary btn-sm"
              href="https://pranayrdy123.wordpress.com/ "
              target="_blank"
            >
              ContactUs
            </a>
          </li>
        </ul>
        <h1>abc</h1>
            <div id="app">
    
    <square
      v-for="data in myJson"
      v-bind:key="data.text"
      v-bind:text="data.text"
      v-bind:size="data.size"
      v-bind:color="data.color"
      
    />

  </div>
  <div :style="{'background-image':'url(/Users/pranayreddy/kaki/src/slide_one.jpg)'}">
  </div>
  
        <p class="lead">
          [<a
            href="https://pranayrdy123.wordpress.com/ "
            target="_blank"
          >About US</a>]
          
        </p>
   
      </header>
    </div>
    <main
      class="container"
      role="main"
    >
      <section class="my-4">
        <h1 class="mb-3">
          Lorem ipsum  
        
        </h1>
        <h1 class="mb-3">
          
        dolor sit amet 
        </h1>




        

        
      </section>
      <section class="my-4">
        <h3 class="mb-3">
           <small>press to stop flow</small>
          <button
            :class="{ 'active': isPaused }"
            class="btn btn-sm btn-outline-primary ml-2"
            type="button"
            @click="isPaused = !isPaused"
          >
            Pause/start
          </button>
        </h3>
       
        <marquee-text
          :duration="20"
          :paused="isPaused"
          reverse
          class="py-2 mt-2 bg-light"
        >
          Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.
        </marquee-text>
      </section>
      
    </main>
  </div>
  
</template>

<script>
  import MarqueeText from './components/MarqueeText.vue'

  import square from './components/square.vue'
import json from './json/data.json'

  export default {
    name: 'App',
    components: {
      MarqueeText,
      square
    },
    data() {
      return {
        isPaused: false,
        myJson: json
      }
    }
  }
  

</script>

<style>
  @import'~bootstrap/dist/css/bootstrap.css';

  table code {
    white-space: nowrap;
  }
  
</style>
