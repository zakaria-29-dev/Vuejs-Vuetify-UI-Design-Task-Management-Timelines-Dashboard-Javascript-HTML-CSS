<template>
  <v-navigation-drawer
  v-model="drawer"
  app dark color="#171721" mini-variant mini-variant-width="90"
  >
        <div class="text-center mt-2">
            <v-icon small color="red">mdi-circle</v-icon>
            <v-icon small color="yellow">mdi-circle</v-icon>
            <v-icon small color="green">mdi-circle</v-icon>
        </div>
        <v-avatar class="d-block text-center mx-auto mt-4" size="30">
            <v-icon color="#7C7C7F">fas fa-align-left</v-icon>
        </v-avatar>
        <v-list flat class="mt-5">
            <v-list-item-group v-model="selectItem">
                <v-list-item v-for="(item,i) in items" :key="i" active-class="border" v-slot="{active}" :ripple="false">
                    <v-list-item-icon>
                        <v-icon v-text="item.icon" :color="active ? 'black' : '#7C7C7F'"></v-icon>
                    </v-list-item-icon>
                </v-list-item>
            </v-list-item-group>
        </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
data: () => ({
    selectItem: 3,
    drawer: null,
    items: [
        {icon: 'fas fa-tv'},
        {icon: 'far fa-building'},
        {icon: 'far fa-compass'},
        {icon: 'far fa-folder-open'},
        {icon: 'far fa-clock'},
        {icon: 'far fa-bell'},
        {icon: 'far fa-address-book'},
    ],
})
}
</script>

<style>
    .border {
        margin-left: 15px;
        margin-right: 15px;
        background: #A9DDD8;
        border-radius: 50%;
        text-decoration: none;
    }
    .v-list-item-group .v-list-item--active {
        color: white !important;
    }
    .theme--light.v-list-item--active .v-list-item__subtitle, .theme--light.v-list-item
 .v-list-item__action-text {
    color: white !important; 
}
</style>