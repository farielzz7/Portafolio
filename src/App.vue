<template>
  <!-- component -->
  <!-- This is an example component -->
  <div class="max-w-7xl mx-auto flex flex-col relative">

    <nav class="max-w-7xl px-5 md:fixed top-0 z-[98] w-screen backdrop-blur-md bg-[#121212] bg-opacity-80">
      <div class="container mx-auto flex flex-wrap items-center justify-between">
        <button @click="redirectToHome" class="flex">
          <span class="self-center text-lg text-[#0361e5] font-semibold whitespace-nowrap fadein-bot hover:text-blue-500">Farielpzz();</span>
        </button>
        <div class="flex md:order-2 fadein-bot space-x-4">
          <a href="https://github.com/farielzz7" target="_blank" rel="noopener noreferrer" class="flex items-center">
            <img class="w-9 h-9 rounded-full" src="https://seeklogo.com/images/G/github-logo-2E3852456C-seeklogo.com.png" alt="github">
          </a>
          <a href="https://www.instagram.com/tu_usuario" target="_blank" rel="noopener noreferrer" class="flex items-center">
            <img class="w-9 h-9 rounded-full" src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Instagram_icon.png" alt="instagram">
          </a>
          <a href="mailto:tu_email@gmail.com" target="_blank" rel="noopener noreferrer" class="flex items-center">
            <i class="fab fa-google w-9 h-9 rounded-full text-white flex items-center justify-center"></i>
          </a>
          <a href="https://www.youtube.com/channel/tu_canal" target="_blank" rel="noopener noreferrer" class="flex items-center">
            <img class="w-9 h-9 rounded-full" src="https://upload.wikimedia.org/wikipedia/commons/0/09/YouTube_full-color_icon_%282017%29.svg" alt="youtube">
          </a>
        </div>
        <div class="hidden md:flex justify-between items-center w-full md:w-auto md:order-1" id="mobile-menu-3">
          <ul class="flex-col md:flex-row flex md:space-x-8 mt-4 md:mt-0 md:text-sm md:font-medium">
            <li>
              <router-link to="/"
                class="fadein-bot text-white hover:bg-gray-50 border-b border-gray-100 md:hover:bg-transparent md:border-0 block pl-3 pr-4 py-2 md:hover:text-gray-500 md:p-0"
                aria-current="page">Home</router-link>
            </li>
            <li>
              <router-link to="/about"
                class="fadein-bot fadein-1 text-white hover:bg-gray-50 border-b border-gray-100 md:hover:bg-transparent md:border-0 block pl-3 pr-4 py-2 md:hover:text-gray-500 md:p-0">About</router-link>
            </li>
            <li>
              <router-link to="/portfolio"
                class="fadein-bot fadein-2 text-white hover:bg-gray-50 border-b border-gray-100 md:hover:bg-transparent md:border-0 block pl-3 pr-4 py-2 md:hover:text-gray-500 md:p-0">Portfolio</router-link>
            </li>
            <li>
              <router-link to="/blog"
                class="fadein-bot fadein-3 text-white hover:bg-gray-50 border-b border-gray-100 md:hover:bg-transparent md:border-0 block pl-3 pr-4 py-2 md:hover:text-gray-500 md:p-0 blog">Blog</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <div class="md:mt-[100px]">
      <router-view />
    </div>
  </div>
  <footer class="block md:hidden fixed bottom-0 left-0 right-0 rounded-t-3xl border border-[#383838] bg-[#121212] bg-opacity-80 backdrop-blur-md backdrop-opacity-90">
    <nav class="flex justify-around py-4 text-xs">
      <router-link to="/" class="text-white hover:text-blue-500">Home</router-link>
      <router-link to="/about" class="text-white hover:text-blue-500">About</router-link>
      <router-link to="/portfolio" class="text-white hover:text-blue-500">Portfolio</router-link>
      <router-link to="/blog" class="text-white hover:text-blue-500">Blog</router-link>
    </nav>
  </footer>
</template>

<script>
export default {
  methods: {
    redirectToHome() {
      this.$router.push('/')
    }
  },
}
</script>

<style>
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

::-webkit-scrollbar {
  width: 5px; /* for vertical scrollbar */
  height: 5px; /* for horizontal scrollbar */
}

::-webkit-scrollbar-track {
  background: hsl(240, 1%, 17%);
  border-radius: 5px;
}

::-webkit-scrollbar-thumb {
  background:rgb(3, 180, 229);
  border-radius: 5px;
}

::-webkit-scrollbar-button { width: 20px; }

body {
  font-family: 'Poppins', sans-serif;
  background: hsl(0, 0%, 7%);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100vh;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: white;
  transition: color 0.3s;
}

nav a.router-link-exact-active {
  display: inline-flex;
  flex-direction: column;
  color: white;
  transition: color 0.3s;
}

nav a.router-link-exact-active::after {
  display: inline-block;
  content: "";
  margin-top: 0.08em;
  width: 100%;
  height: 4px;
  border-radius: 2px;
  background-color: #0361e5;
}

nav a.router-link-exact-active:hover {
  color: white;
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(-100%);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.flex.items-center .fab {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 36px; /* 9 * 4 */
  height: 36px; /* 9 * 4 */
  font-size: 1.5rem; /* Adjust the size as needed */
}
</style>
