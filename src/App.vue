<template>
  <div id="app">
    <sidebar></sidebar>
    <pad></pad>
  </div>
</template>

<script>
import Pad from './components/Pad'
import Sidebar from './components/Sidebar'

export default {
  name: 'app',
  components: {
    Pad,
    Sidebar
  }
}
</script>

<style>
    body, html {
        margin: 0;
        padding: 0;
        height: 100%;
    }

    body {
        color: #2c3e50;
    }

    #app {
      font-family: 'Raleway', Helvetica, Arial, sans-serif;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      display: flex;
      height: 100%;
    }

    /* Let's get this party started */
    ::-webkit-scrollbar {
        width: 3px;
    }

    /* Track */
    ::-webkit-scrollbar-track {
        -webkit-box-shadow: inset 0 0 6px rgba(0,0,0,0.3);
        -webkit-border-radius: 10px;
        border-radius: 10px;
    }

    /* Handle */
    ::-webkit-scrollbar-thumb {
        -webkit-border-radius: 5px;
        border-radius: 10px;
        background: grey;
        -webkit-box-shadow: inset 0 0 6px grey;
    }
    ::-webkit-scrollbar-thumb:window-inactive {
    	background: grey;
    }
</style>
