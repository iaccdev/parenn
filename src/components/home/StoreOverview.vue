<template>
  <section class="sec-product bg0 p-b-80">
    <div class="container">
      <div class="p-b-32">
        <h3 class="ltext-105 cl5 txt-center respon1">
          Nos produits
        </h3>
      </div>
      <!-- Store overview tab -->
      <div class="store-overview-tab">
        <b-tabs content-class="p-t-43">
          <b-tab
            v-for="(item, index) in tabListData"
            v-bind:title="item.tabName"
            v-bind:key="index"
            v-bind:class="{ active: currentActiveTab == item.tabName }"
            @click="setCurrentTab(item.tabName)"
          >
            <StoreOverviewCarousel
              style="i"
              v-if="currentActiveTab == item.tabName"
              v-bind:current-tab-data="item"
            />
          </b-tab>
        </b-tabs>
      </div>
    </div>
  </section>
</template>
<script>
import StoreOverviewCarousel from "@/components/home/StoreOverviewCarousel.vue";
export default {
  name: "StoreOverview",
  components: {
    StoreOverviewCarousel
  },
  data() {
    return {
      tabListData: [
        {
          tabName: "Eau en bouteille",
          product: [
            {
              productImg: "img4.jpg",
              productName: "Herschel supply",
              productCost: "$35.31"
            }
          ]
        },
        {
          tabName: "Parfum",
          product: [
            {
              productImg: "img3.jpg",
              productName: "Esprit Ruffle Shirt",
              productCost: "$16.64"
            }
          ]
        },

        {
          tabName: "Sac a poubelle",
          product: [
            {
              productImg: "img6.jpg",
              productName: "Esprit Ruffle Shirt",
              productCost: "$16.64"
            }
          ]
        },
        {
          tabName: "Ciment",
          product: [
            {
              productImg: "img5.jpg",
              productName: "CIMENT PARENN",
              productCost: "$35.31"
            }
          ]
        },
        {
          tabName: "Bracelet",
          product: [
            {
              productImg: "img7.jpg",
              productName: "BRACELET PARENN",
              productCost: "$35.31"
            }
          ]
        },
        {
          tabName: "Camion décharge",
          product: [
            {
              productImg: "img8.jpg",
              productName: "CAMION DÉCHARGE PARENN",
              productCost: "$35.31"
            }
          ]
        }
        // {
        //   tabName: "Top Rate",
        //   product: [
        //     {
        //       productImg: "product-11.jpg",
        //       productName: "Herschel supply",
        //       productCost: "$63.16"
        //     },
        //     {
        //       productImg: "product-13.jpg",
        //       productName: "T-Shirt with Sleeve",
        //       productCost: "$18.49"
        //     },
        //     {
        //       productImg: "product-03.jpg",
        //       productName: "Only Check Trouser",
        //       productCost: "$25.50"
        //     },
        //     {
        //       productImg: "product-04.jpg",
        //       productName: "Classic Trench Coat",
        //       productCost: "$75.00"
        //     },
        //     {
        //       productImg: "product-05.jpg",
        //       productName: "Front Pocket Jumper",
        //       productCost: "$34.75"
        //     },
        //     {
        //       productImg: "product-06.jpg",
        //       productName: "Vintage Inspired Classic",
        //       productCost: "$93.20"
        //     },
        //     {
        //       productImg: "product-07.jpg",
        //       productName: "Shirt in Stretch Cotton",
        //       productCost: "$52.66"
        //     },
        //     {
        //       productImg: "product-08.jpg",
        //       productName: "Pieces Metallic Printed",
        //       productCost: "$18.96"
        //     }
        //   ]
        // }
      ],
      currentActiveTab: "Best Seller"
    };
  },
  methods: {
    setCurrentTab(tabName) {
      this.currentActiveTab = tabName;
    }
  }
};
</script>
