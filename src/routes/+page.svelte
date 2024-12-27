<script>
    import { fade } from 'svelte/transition';
    let currentWord = 0;
    let words = ['Simple', 'Flexible', 'Fast', 'Secure'];
 
    setInterval(() => {
        currentWord = (currentWord + 1) % words.length;

    }, 2000);
</script>

<div class="min-h-screen bg-gradient-to-br from-gray-900 via-black to-gray-900 text-gray-200">
  <header class="w-full py-6 bg-transparent">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 flex justify-between items-center">
      <h1 class="text-3xl font-bold text-gray-200 flex items-center gap-2">
        <svg class="w-8 h-8" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M13 4L7 20M17 4L11 20" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M5 8H19" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
          <path d="M5 16H19" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
        </svg>
        exec
      </h1>
      <nav>
        <ul class="flex space-x-6 text-gray-300 text-xl">
          <li><a href="https://github.com/ItzCyzmiX/Exec" class="hover:border-b hover:border-gray-200 hover:text-gray-200 flex items-center gap-2" target="_blank"><svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z" clip-rule="evenodd" /></svg>Github</a></li>
          <li><a href="/docs" class="hover:border-b hover:border-gray-200 hover:text-gray-200">Docs</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main class="flex-grow">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-20">
      <div class="text-center mb-20">
        <h2 class="text-7xl font-extrabold tracking-tight mb-8 bg-gradient-to-r from-blue-400 via-purple-500 to-pink-500 text-transparent bg-clip-text animate-gradient">

        
          Code Execution Made 
        
            <span class=" transition-all duration-300 " in:fade out:fade>{words[currentWord]}</span>
     
           
        </h2>
        <p class="text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
          Transform strings into executable code across multiple programming languages with our powerful API.
        </p>
        <div class="flex justify-center gap-6">
          <a href="/docs" class="text-black bg-white font-bold rounded-lg px-8 py-4 hover:scale-105 transition-all duration-300 hover:shadow-lg hover:shadow-purple-500/50">
            Get Started
          </a>
          <a href="https://github.com/ItzCyzmiX/Exec" class="text-white border-2 border-white font-bold rounded-lg px-8 py-4 hover:scale-105 transition-all duration-300 hover:shadow-lg hover:shadow-pink-500/50">
            View on GitHub
          </a>
        </div>
      </div>

      <div class="grid md:grid-cols-3 gap-8 mt-20">
        <div class="bg-gray-800/50 p-8 rounded-xl border border-gray-700 hover:border-purple-500 transition-colors duration-300">
          <div class="text-purple-400 mb-4">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
            </svg>
          </div>
          <h3 class="text-xl font-bold mb-4">Lightning Fast</h3>
          <p class="text-gray-400">Execute code instantly with our optimized runtime environment.</p>
        </div>

        <div class="bg-gray-800/50 p-8 rounded-xl border border-gray-700 hover:border-blue-500 transition-colors duration-300">
          <div class="text-blue-400 mb-4">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
            </svg>
          </div>
          <h3 class="text-xl font-bold mb-4">Secure Sandbox</h3>
          <p class="text-gray-400">Run code in isolated environments with robust security measures.</p>
        </div>

        <div class="bg-gray-800/50 p-8 rounded-xl border border-gray-700 hover:border-pink-500 transition-colors duration-300">
          <div class="text-pink-400 mb-4">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
            </svg>
          </div>
          <h3 class="text-xl font-bold mb-4">Multiple Languages</h3>
          <p class="text-gray-400">Support for various programming languages in a single unified API.</p>
        </div>
      </div>
    </div>
  </main>
  <section class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
    <h2 class="text-3xl font-bold text-center mb-12">See It in Action</h2>
    
    <div class="grid md:grid-cols-2 gap-12">
      <div class="bg-gray-800/50 rounded-xl border border-gray-700 p-8">
        <h3 class="text-xl font-bold mb-4">Simple Python Example</h3>
        <pre class="bg-black p-4 rounded mb-4 border border-gray-700 text-sm">{`
import requests

response = requests.post('https://exec-urmk.onrender.com/exec', 
    json={
        'code': 'print("Hello, World!")',
        'language': 'python'
    },
    headers={'Content-Type': 'application/json'}
)`}</pre>
        <div class="bg-black p-4 rounded border border-gray-700">
          <p class="text-green-400 text-sm font-mono">Output: Hello, World!</p>
        </div>
      </div>

      <div class="bg-gray-800/50 rounded-xl border border-gray-700 p-8">
        <h3 class="text-xl font-bold mb-4">JavaScript Calculator</h3>
        <pre class="bg-black p-4 rounded mb-4 border border-gray-700 text-sm">{`
fetch('https://exec-urmk.onrender.com/exec', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    code: 'console.log(5 + 10 * 2)',
    language: 'javascript'
  })
})`}</pre>
        <div class="bg-black p-4 rounded border border-gray-700">
          <p class="text-green-400 text-sm font-mono">Output: 25</p>
        </div>
      </div>
    </div>
  </section>
  <section class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
    <h2 class="text-3xl font-bold text-center mb-12">Performance Metrics</h2>
    
    <div class="grid md:grid-cols-3 gap-8">
      <div class="bg-gray-800/50 rounded-xl border border-gray-700 p-8 text-center hover:bg-gray-700/50 hover:border-gray-600 transition-all duration-300 hover:scale-105 hover:shadow-lg hover:shadow-green-500/20">
        <h3 class="text-xl font-bold mb-2">Average Response Time</h3>
        <p class="text-4xl font-bold text-green-400">150ms</p>
        <p class="text-gray-400 mt-2">For simple code execution</p>
      </div>

      <div class="bg-gray-800/50 rounded-xl border border-gray-700 p-8 text-center hover:bg-gray-700/50 hover:border-gray-600 transition-all duration-300 hover:scale-105 hover:shadow-lg hover:shadow-green-500/20">
        <h3 class="text-xl font-bold mb-2">99th Percentile</h3>
        <p class="text-4xl font-bold text-green-400">450ms</p>
        <p class="text-gray-400 mt-2">Response time</p>
      </div>

      <div class="bg-gray-800/50 rounded-xl border border-gray-700 p-8 text-center hover:bg-gray-700/50 hover:border-gray-600 transition-all duration-300 hover:scale-105 hover:shadow-lg hover:shadow-green-500/20">
        <h3 class="text-xl font-bold mb-2">Uptime</h3>
        <p class="text-4xl font-bold text-green-400">99.9%</p>
        <p class="text-gray-400 mt-2">Service availability</p>
      </div>
    </div>
  </section>
  <section class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-16 text-center">
    <h2 class="text-4xl font-bold mb-6">What Are You Waiting For?</h2>
    <p class="text-xl text-gray-300 mb-8">Start building amazing applications with our powerful code execution API today.</p>
    
    <div class="flex flex-col sm:flex-row justify-center items-center gap-6">
        <a href="/docs" class="text-black bg-white font-bold rounded-lg px-8 py-4 hover:scale-105 transition-all duration-300 hover:shadow-lg hover:shadow-purple-500/50">
            Get Started
          </a>
          <a href="https://github.com/ItzCyzmiX/Exec" class="text-white border-2 border-white font-bold rounded-lg px-8 py-4 hover:scale-105 transition-all duration-300 hover:shadow-lg hover:shadow-pink-500/50">
            View on GitHub
          </a>
    </div>
  </section>
  <footer class="w-full py-6 bg-transparent shadow-md">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 text-center text-gray-300">
      &copy; 2024 exec. All rights reserved.
    </div>
  </footer>
</div>
