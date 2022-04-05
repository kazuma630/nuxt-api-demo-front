<template>
  <div>
    <v-card-title
      class="pb-8 text-subtitle-2 justify-center"
    >
      テスト
    </v-card-title>
    <v-card-title
      class="text-subtitle-2 justify-center"
    >
      Rails6とNuxtで作るSPAアプリケーション
    </v-card-title>
    <v-card-text
      class="text-center"
    >
      <a
        :href="siteUrl"
        rel="nofollow"
        target="_blank"
        class="text-decoration-none"
      >
        {{ siteUrl }}
      </a>
    </v-card-text>
    <v-card-title
      class="text-subtitle-2 justify-center"
    >
      技術
    </v-card-title>
    <v-container
      fluid
      :style="{ maxWidth: '960px' }"
    >
      <v-row
        justify="space-around"
      >
        <v-col
          v-for="(tec, i) in technologies"
          :key="`tec-${i}`"
          class="text-center pa-2"
        >
          <v-avatar
            :color="tec.color"
            size="80"
          >
            <span
              class="white--text"
            >
              {{ tec.name }}
            </span>
          </v-avatar>
          <div
            class="pt-2 text-body-2 my-grey"
          >
            {{ tec.use }}
          </div>
          <div
            class="pt-2 text-body-2 my-grey"
          >
            {{ tec.v }}
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data () {
    return {
      siteUrl: 'https://github.com/kazuma630',
      technologies: [
        { name: 'Docker', v: 'v19.03+', use: '開発環境', color: '#2496ED' },
        { name: 'Rails', v: 'v6.0+', use: '・サーバーサイド', color: '#CC0000' },
        { name: 'Nuxt.js', v: 'v2.13+', use: 'フロントエンド', color: '#00C48D' },
        { name: 'Docker', v: 'v19.03+', use: '開発環境', color: '#2496ED' },
        { name: 'Rails', v: 'v6.0+', use: '・サーバーサイド', color: '#CC0000' },
        { name: 'Nuxt.js', v: 'v2.13+', use: 'フロントエンド', color: '#00C48D' }
      ]
    }
  }
}
</script>
