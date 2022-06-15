<template>
  <div class="flex flex-col items-center">
    <h1 class="mt-10 mb-4 text-lg font-medium">Buscador de Lolzeiro</h1>
    <div class="flex flex-row gap-2 items-end">
      <div>
        <div class="mt-1">
          <input type="text" name="player" id="player" v-model="nome_do_player"
            class="h-8 shadow-sm focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm border-gray-300 rounded-md"/>
        </div>
      </div>
      <button type="button" @click="buscar_player()" class="h-8 inline-flex items-center px-3 py-2 border border-transparent text-sm leading-4 font-medium rounded-md shadow-sm text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">Encontrar</button>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: 'IndexPage',
  data() {
    return {
      nome_do_player: '',
    };
  },
  methods: {
    async buscar_player(){
      console.log(this.nome_do_player)
      const APICallString = 'https://br1.api.riotgames.com/lol/summoner/v4/summoners/by-name/' + this.nome_do_player + '?api_key='+ process.env.API_KEY;
      try {
        const data = await axios.get(APICallString);
        console.log(data)
      } catch (e) {
        console.log(e)
        alert('erro ao buscar')
      }
    }
  }
}
</script>
