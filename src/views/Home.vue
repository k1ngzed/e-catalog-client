<template>
  <main class="content">
    <!-- <section class="products">
      <div class="container">
        <ProductList
          v-for="(filter, index) in productsFilter"
          class="product-list"
          :key="index"
          :id="filter.id"
          :title="filter.title"
          :products="filter.products"
          :sellers="sellers"
          :itemComponent="'minimal'"
        />
      </div>
    </section> -->
    <!-- <section class="articles">
      <ArticleList :items="posts" :container="'container'" />
    </section>
    <section class="brands">
      <Brands :items="brands" :container="'container'" />
    </section> -->
    <section class="novelty">
      <NoveltyList :container="'container'" />
    </section>
  </main>
</template>

<script>
// import { mapGetters } from "vuex";

// components
// import ProductList from "../components/Content/Products/ProductList";
// import ArticleList from "../components/Content/Articles/ArticleList";
// import Brands from "../components/Content/Brands";
import NoveltyList from "../components/Content/Novelty/NoveltyList"

export default {
  name: "home",
  components: {
    // ProductList,
    // ArticleList,
    // Brands,
    NoveltyList
  },
  data() {
    return {
      isModalVisible: false
    }
  },
  computed: {
    // ...mapGetters(["products", "sellers", "brands", "posts", "users"]),
    productsFilter() {
      // let arr = this.products,
      //   // eslint-disable-next-line no-unused-vars
      //   temp;

      // for (var i = 0, j = arr.lenght - 1; i < j; i++, j--) {
      //   temp = arr[j];
      //   arr[j] = arr[i];
      //   arr[i] = temp;
      // }

      let filter = [
        {
          id: 0,
          title: "Рекомендуемые товары",
          products: this.products
        },
        {
          id: 1,
          title: "Популярные товары",
          products: this.products
        }
      ]

      return filter
    }
    // recommendedProducts() {
    //   return this.products;
    // },
    // popularProducts() {
    //   return this.products;
    // }
  },
  created() {
    // this.$store.dispatch("loadBrands");
    // console.log(this.$apollo);
    // console.log(this.$apolloProvider);
    // console.log(this.$data);
  },
  methods: {
    showModal() {
      this.isModalVisible = true
    },
    closeModal() {
      this.isModalVisible = false
    }
  }
}
</script>
