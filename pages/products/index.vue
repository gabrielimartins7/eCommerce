<template>
  <div>
    <Nav />
    <v-container>
      <v-row dense>
        <v-col md="3">
          <div>
            <v-text-field
              prepend-inner-icon="mdi-magnify"
              outlined
              clearable
              placeholder="Search"
            />
            <v-list subheader color="transparent" v-if="$vuetify.breakpoint.mdAndUp">
              <v-subheader>Categories</v-subheader>
              <v-list-item v-for="(c,i) in categories" :key="`categiry${i}`" link>
                <v-list-item-avatar>
                  <v-img :src="c.image"></v-img>
                </v-list-item-avatar>
                <v-list-item-content>
                  <v-list-item-title>
                    {{ c.name }}
                  </v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  async created(){
    this.categories = await this.$content('category').fetch();
    this.products = await this.$content('products').fetch();
  },
  data(){
    return {
      products: null,
      categories: null,
    }
  },
}
</script>

<style>

</style>
