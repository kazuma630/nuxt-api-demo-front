<template>
  <v-app>
    <home-app-bar />
    <v-sheet>
      <v-container
        fluid
        :style="{ maxWidth: '1280px' }"
      >
        <v-row
          v-for="(menu, i) in menus"
          :key="`menu-${i}`"
        >
          <v-col cols="12">
            <div :is="`home-${menu.title}`"></div>
          </v-col>
        </v-row>
      </v-container>
    </v-sheet>
    <app-footer />
  </v-app>
</template>

<script>
import HomeAbout from '~/components/Home/HomeAbout'
import HomeProducts from '~/components/Home/HomeProducts'
import HomePrice from '~/components/Home/HomePrice'
import HomeContact from '~/components/Home/HomeContact'
import HomeCompany from '~/components/Home/HomeCompany'

export default {
  components: {
    HomeAbout,
    HomeProducts,
    HomePrice,
    HomeContact,
    HomeCompany
  },
  data () {
    return {
      menus: [
        { title: 'about', subtitle: 'デモアプリです。' },
        { title: 'products', subtitle: '数々の機能' },
        { title: 'price', subtitle: '企業成長に合わせた3つのプラン' },
        { title: 'contact', subtitle: 'ご連絡くださいまし' },
        { title: 'company', subtitle: '会社' }
      ]
    }
  }
}
</script>
