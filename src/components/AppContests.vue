<template>
  <v-container
    id="contests"
    class="text-center"
  >
    <v-row>
      <v-col cols="12">
        <h1 class="display-2 font-weight-bold my-3">
          <v-icon class="display-2 pb-3">mdi-medal-outline</v-icon>
          Contests
        </h1>

      </v-col>
        <v-col
          cols="12"
          v-for="content in contents"
          :key="content.name"
          class="mb-3 "
        >
          <p
            class="text-subtitle-1 text-md-h6 text-lg-h6 text-xl-h4"
            style="margin: 0;"
          >
            {{ content.name }}
          </p>
          <p
            v-if="content.result"
            class="text-caption text-md-subtitle-1 text-lg-subtitle-1 text-xl-h6"
            style="margin-bottom: 0.5rem;"
          >
            {{ content.result }}
          </p>
          <p>
            <a target="_blank" :href="content.link">
              {{ content.link }}
            </a>
          </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "AppContests",

  data() {
    return {
      contents: [
        {
          name: "第30回 高専プロコン (2019)",
          result: "サブメンバーとして参加",
          link: "https://www.procon.gr.jp/?cat=1661"
        },
        {
          name: "中高生国際Rubyプログラミングコンテスト 2020",
          result: "ゲーム部門 最優秀賞",
          link: "https://www.ruby-procon.net/"
        },
        {
          name: "第32回 高専プロコン (2020)",
          result: "特別賞 / サブメンバーとして参加",
          link: "https://www.procon.gr.jp/?cat=1680"
        },
        {
          name: "技育展2021 登壇",
          link: "https://talent.supporterz.jp/geekten/2021/"
        },
      ]
    }
  },
}
</script>
