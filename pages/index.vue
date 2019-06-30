<template>
  <section class="section">
    <div class="container">
      <div class="columns is-multiline">
        <div
          class="column is-one-quarter"
          v-for="(article, index) in articles"
          :key="index">
          <a :href="article.url" target="_blank">
            <div class="card">
              <div class="card-image">
                <figure class="image is-3by2">
                  <img :src="article.urlToImage" :alt="article.title">
                </figure>
              </div>
              <div class="card-content">
                <div class="content">{{ article.title }}</div>
              </div>
            </div>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
<<<<<<< HEAD
console.log("teeeeeeeeest")
=======
console.log("this will be merged with master i guess")
>>>>>>> 5b043d10f137bb7100067c57c8148529fbb86c45
export default {
  async asyncData({ app }) {
    const { articles } = await app.$axios.$get(
      `https://newsapi.org/v2/top-headlines?sources=cnn&apiKey=${
        process.env.API_KEY
      }`
    );

    return { articles };
  },
};
</script>
