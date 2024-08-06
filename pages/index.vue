<template>
  <div class="flex items-center pa-2 justify-center min-h-screen">
    <v-card
      flat
      color="transparent"
      class="pa-6 w-100 bg-red-400 mx-auto shadow-lg text-center"
    >
      <v-img
        src="https://media.giphy.com/media/vR1dPIYzQmkRzLZk2w/giphy.gif?cid=790b7611s8x3vd5mrxh5civ3lxha2dq0lijo3degsml44lhj&ep=v1_gifs_search&rid=giphy.gif&ct=g"
        height="200px"
        class="mb-4"
        contain
      ></v-img>
      <v-card-title class="justify-center text-3xl font-bold mb-4">
        <span class="text-3xl"> Coming Soon </span>
      </v-card-title>
      <v-card-text class="text-gray-700 mb -6">
        Meanwhile, you can visit our other sites:
      </v-card-text>
      <div class="mb-6">
        <v-btn
          v-for="link in links"
          :key="link.url"
          :href="link.url"
          target="_blank"
          class="mb-2 mx-2"
          outlined
          color="primary"
        >
          <v-icon left>mdi-link</v-icon>{{ link.name }}
        </v-btn>
      </div>
    </v-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      links: [
        { name: 'Anime Site', url: 'https://anime.dheep.site' },
        {
          name: '1945 Uncolonized Game',
          url: 'https://dhitgt.github.io/1945/',
        },
        { name: 'Portfolio', url: 'https://dhitgt.github.io/' },
        // Add more links as needed
      ],
    }
  },
}
</script>

<style scoped>
/* Add any custom styles here */
</style>
