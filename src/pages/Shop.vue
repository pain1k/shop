<template>
  <div class="wrapper-content wrapper-content--fixed">
    <section>
      <div class="container">
        <h1>Shop page</h1>
        <div class="item-wrapper">
          <shopItem
              v-for="product in shopList"
              :key="product.id"
              :product="product"
          >

          </shopItem>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import shopItem from '@/components/ShopItem'
export default{
  components:{
    shopItem
  },
  data(){
    return {
      shopList:null
    }
  },
  created () {
    this.shopList = this.$store.getters.getShopList
    console.log(this.shopList)
  }
}

</script>

<style scoped>

</style>