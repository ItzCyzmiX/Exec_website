<script>
  let js_example = `fetch('https://exec-urmk.onrender.com/exec', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    code: 'print("Hello, World!")',
    language: 'python'
  })
})  `

  let python_example = `import requests

response = requests.post('https://exec-urmk.onrender.com/exec', json={
  'code': 'print("Hello, World!")', 
  'language': 'python'
})

print(response.json())`

  let activeTab = 'python';
</script>

<div class="min-h-screen bg-gradient-to-br from-gray-900 via-black to-gray-900 text-gray-200">
  <header class="w-full py-12 bg-transparent">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
      <h1 class="text-5xl font-bold bg-gradient-to-r from-blue-400 via-purple-500 to-pink-500 text-transparent bg-clip-text mb-4">API Documentation</h1>
      <p class="text-xl text-gray-400">Everything you need to integrate Exec into your applications</p>
    </div>
  </header>

  <main class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
    <section class="mb-16">
      <div class="flex items-center gap-4 mb-8">
        <h2 class="text-3xl font-bold">Endpoints</h2>
        <div class="h-1 flex-grow bg-gradient-to-r from-blue-500 to-purple-500 rounded"></div>
      </div>
      
      <div class="bg-gray-800/30 backdrop-blur-sm rounded-xl p-8 mb-8 border border-gray-700 hover:border-purple-500/50 transition-all duration-300 shadow-lg">
        <div class="flex items-center gap-3 mb-4">
          <span class="px-3 py-1 bg-green-500/20 text-green-400 rounded-full text-sm font-mono">POST</span>
          <h3 class="text-2xl font-bold">/exec</h3>
        </div>
        <p class="mb-6 text-gray-300">Execute code in a specified programming language with full output capture and error handling.</p>
        
        <div class="space-y-6">
          <div>
            <h4 class="font-bold mb-3 text-purple-400">Request Body:</h4>
            <pre class="bg-black/50 p-6 rounded-lg border border-gray-700 font-mono">{`{
  "code": "string",    // The code to execute
  "language": "string" // The programming language
}`}</pre>
          </div>

          <div>
            <h4 class="font-bold mb-3 text-purple-400">Response:</h4>
            <pre class="bg-black/50 p-6 rounded-lg border border-gray-700 font-mono">{`{
  "success": boolean,  // Whether the execution was successful
  "stdout": "string",  // The program output
  "error": "string"    // Error message if execution failed
}`}</pre>
          </div>
        </div>
      </div>

      <div class="bg-gray-800/30 backdrop-blur-sm rounded-xl p-8 border border-gray-700 hover:border-blue-500/50 transition-all duration-300 shadow-lg">
        <div class="flex items-center gap-3 mb-4">
          <span class="px-3 py-1 bg-blue-500/20 text-blue-400 rounded-full text-sm font-mono">GET</span>
          <h3 class="text-2xl font-bold">/getlangs</h3>
        </div>
        <p class="mb-6 text-gray-300">Retrieve a list of all supported programming languages.</p>

        <div>
          <h4 class="font-bold mb-3 text-blue-400">Response:</h4>
          <pre class="bg-black/50 p-6 rounded-lg border border-gray-700 font-mono">{`{
  "languages": ["python", "javascript", "java", "cpp"]  // Array of supported languages
}`}</pre>
        </div>
      </div>
    </section>

    <section>
      <div class="flex items-center gap-4 mb-8">
        <h2 class="text-3xl font-bold">Example Usage</h2>
        <div class="h-1 flex-grow bg-gradient-to-r from-pink-500 to-purple-500 rounded"></div>
      </div>

      <div class="bg-gray-800/30 backdrop-blur-sm rounded-xl p-8 border border-gray-700 hover:border-pink-500/50 transition-all duration-300 shadow-lg">
        <div class="flex gap-4 mb-6">
          <button 
            class={`px-4 py-2 rounded-lg font-mono text-sm ${activeTab === 'python' ? 'bg-purple-500/20 text-purple-400 border border-purple-500/50' : 'text-gray-400 hover:text-gray-200'}`}
            on:click={() => activeTab = 'python'}
          >
            Python
          </button>
          <button 
            class={`px-4 py-2 rounded-lg font-mono text-sm ${activeTab === 'javascript' ? 'bg-purple-500/20 text-purple-400 border border-purple-500/50' : 'text-gray-400 hover:text-gray-200'}`}
            on:click={() => activeTab = 'javascript'}
          >
            JavaScript
          </button>
        </div>
        <pre class="bg-black/50 p-6 rounded-lg border border-gray-700 font-mono">{activeTab === 'python' ? python_example : js_example}</pre>
      </div>
    </section>
  </main>

  <footer class="w-full py-8 bg-transparent mt-16 border-t border-gray-800">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 text-center text-gray-400">
      <p>&copy; 2024 exec. All rights reserved.</p>
      <p class="mt-2 text-sm">Built with ❤️ for developers</p>
    </div>
  </footer>
</div>
