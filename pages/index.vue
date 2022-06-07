<template>
  <div class="flex flex-col items-center">
    <h1 class="mt-10">Buscador de Lolzeiro</h1>
    <div class="flex align-middle">
      <div>
        <label for="email" class="block text-sm font-medium text-gray-700">Email</label>
        <div class="mt-1">
          <input type="email" name="email" id="email"
            class="shadow-sm focus:ring-indigo-500 focus:border-indigo-500 block w-full sm:text-sm border-gray-300 rounded-md"
            placeholder="you@example.com" />
        </div>
      </div>
      <button type="button" class="h-min inline-flex items-center px-3 py-2 border border-transparent text-sm leading-4 font-medium rounded-md shadow-sm text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">Button text</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
