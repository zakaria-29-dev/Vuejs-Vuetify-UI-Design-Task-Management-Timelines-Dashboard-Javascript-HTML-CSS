<template>
<v-app :style="{background: $vuetify.theme.themes.dark.background}">
  <SideBar />
  <RightSideBar />
  <v-container>
     <v-toolbar color="rgba(0,0,0,0)" flat>
       <v-toolbar-title class="mt-n4 white--text">Task Management</v-toolbar-title>

       </v-toolbar>
       <v-toolbar color="rgba(0,0,0,0)" flat dark class="mt-n6">
      <div>
         <v-icon color="#7C7C7F" class="mr-2">
           far fa-calendar-alt
         </v-icon>
          <v-badge
          color="red"
          content="1"
        >    
          <span class="caption grey--text mt-2">
           DIM 9, 2022
          </span>
            </v-badge>
      </div>
      <v-spacer></v-spacer>
        <div  color="rgba(0,0,0,0)">
           <v-tabs
            color="#A9DDD8"
            right
            background-color="#171721"
            >
    <v-tab>Day</v-tab>
    <v-tab>Week</v-tab>
    <v-tab>Month</v-tab>
    <v-tab>Year</v-tab>
  </v-tabs>
        </div>
           
           
       </v-toolbar>
       <v-divider color="#7C7C7F"></v-divider>
       <v-row>
         <v-col cols="12" sm="3">
           <v-list rounded
           flat
           color="rgba(0,0,0,0)"
           class="mt-3"
           >
      
      <v-list-item-group
        v-model="selectedItem"
        color="#A9DDD8"
      >
        <v-list-item active-class="border">
          <v-list-item-content>
            <v-list-item-title class="grey--text">Design</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item active-class="border" class="mt-11">
          <v-list-item-content >
            <v-list-item-title class="grey--text">Mobile Apps</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item active-class="border" class="mt-8">
          <v-list-item-content >
            <v-list-item-title class="grey--text">Infography</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item active-class="border" class="mt-8">
          <v-list-item-content >
            <v-list-item-title class="grey--text">Protoyping</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
         </v-col>
         <v-col cols="12" sm="9">
           <v-timeline
    align-top
    :dense="$vuetify.breakpoint.smAndDown"
    class="mt-2 mr-3"
  >
    <v-timeline-item 
      color="red" 
      fill-dot
      small
    >
      <v-card
        color="#22222C"
        dark
      >
        <v-card-title class="text-subtitle-2 red--text">
          About 2 hours
           <v-spacer></v-spacer>
          <v-avatar size="30">
              <img
               src="https://cdn.vuetifyjs.com/images/lists/1.jpg"
                alt="John"
              >
            </v-avatar>
             <v-avatar class="ml-n3" size="30">
              <img
                src="https://cdn.vuetifyjs.com/images/lists/5.jpg"
                alt="John"
              >
            </v-avatar>
        </v-card-title>
                
      </v-card>
    </v-timeline-item>
    <v-timeline-item 
      color="cyan" 
      fill-dot
      small
    >
      <v-card
        color="#22222C"
        dark
      >
        <v-card-title class="text-subtitle-2 cyan--text">
          About 5 hours
           <v-spacer></v-spacer>
          <v-avatar size="30">
              <img
               src="https://cdn.vuetifyjs.com/images/lists/3.jpg"
                alt="John"
              >
            </v-avatar>
            
        </v-card-title>
                
      </v-card>
    </v-timeline-item>
     <v-timeline-item 
      color="pink" 
      fill-dot
      small
    >
      <v-card
        color="#22222C"
        dark
      >
        <v-card-title class="text-subtitle-2 pink--text">
          About 5 hours
           <v-spacer></v-spacer>
          <v-avatar size="30">
              <img
               src="https://cdn.vuetifyjs.com/images/lists/4.jpg"
                alt="John"
              >
            </v-avatar>
             <v-avatar class="ml-n3" size="30">
              <img
                src="https://cdn.vuetifyjs.com/images/lists/2.jpg"
                alt="John"
              >
            </v-avatar>
        </v-card-title>
                
      </v-card>
    </v-timeline-item>
    <v-timeline-item 
      color="yellow" 
      fill-dot
      small
    >
      <v-card
        color="#22222C"
        dark
      >
        <v-card-title class="text-subtitle-2 yellow--text">
          About 3 hours
           <v-spacer></v-spacer>
          <v-avatar size="30">
              <img
               src="https://cdn.vuetifyjs.com/images/lists/1.jpg"
                alt="John"
              >
            </v-avatar>
             <v-avatar class="ml-n3" size="30">
              <img
                src="https://cdn.vuetifyjs.com/images/lists/3.jpg"
                alt="John"
              >
            </v-avatar>
            <v-avatar class="ml-n3" size="30">
              <img
                src="https://cdn.vuetifyjs.com/images/lists/5.jpg"
                alt="John"
              >
            </v-avatar>
        </v-card-title>
                
      </v-card>
    </v-timeline-item>
    
  </v-timeline>
         </v-col>
       </v-row>
       <v-row>
         <v-col cols="12" sm="4">
           <v-card  color="#22222C" class="rounded-lg" elevation="10">
          <v-app-bar
            flat
            color="rgba(0, 0, 0, 0)"
          >
             
            <v-toolbar-title class="text-subtitle-2 white--text pl-0 ">
              UX UI Design <br>
              <span class="caption grey--text">Deans and Creative</span>
            </v-toolbar-title>

            <v-spacer></v-spacer>
            <v-btn
              color="#7C7C7F"
              icon
              small
            >
              <v-icon>mdi-dots-vertical</v-icon>
            </v-btn>
          </v-app-bar>
           <v-app-bar
            flat
            color="rgba(0, 0, 0, 0)"
            class="mt-n7"
          >
            <v-avatar size="30">
              <img
                src="https://cdn.vuetifyjs.com/images/lists/4.jpg"
                alt="John"
              >
            </v-avatar>
             <v-avatar class="ml-n3" size="30">
              <img
                src="https://cdn.vuetifyjs.com/images/lists/1.jpg"
                alt="John"
              >
            </v-avatar>
            <v-avatar class="ml-n3" size="30">
              <img
                src="https://cdn.vuetifyjs.com/images/lists/3.jpg"
                alt="John"
              >
            </v-avatar>
          

            
          </v-app-bar>
           <v-app-bar
            flat
            color="rgba(0, 0, 0, 0)"
            class="mt-n6"
          >
            <span
             class="grey--text"
              small
            >
              Progress
            </span>
            <v-spacer></v-spacer> 
             <span
             class="caption grey--text"
            >
              45%
            </span>
          </v-app-bar>
      
          <v-app-bar
            flat
            color="rgba(0, 0, 0, 0)"
            class="mt-n10"
          >
          <v-progress-linear
      color="green"
      height="6"
      value="45"
     
    ></v-progress-linear>
           
          </v-app-bar>
<v-card-text class="pt-0">
  <v-row>
    <v-col cols="12" sm="8">
<v-icon
      class="mr-2"
        small
        color="#7C7C7F"
      >
        fas fa-share-alt
      </v-icon>
      <span class="text-caption grey--text font-weight-light">5</span>
      <v-icon
      class="ml-2 mr-2"
        small
        color="#7C7C7F"
      >
       far fa-comment-dots
      </v-icon>
      <span class="text-caption grey--text font-weight-light">3</span>
    </v-col>
    <v-col cols="12" sm="4">
       <v-chip
        dark
        color="#7C7C7F"
        class=""
        small
      >
        <v-icon left small>
          mdi-alarm-check
        </v-icon>
        3 Week left
      </v-chip>
    </v-col>
  </v-row>
      
     
     
    </v-card-text>
      </v-card>
         </v-col>
         <v-col cols="12" sm="4">
            <v-card  color="#22222C" class="rounded-lg" elevation="10">
          <v-app-bar
            flat
            color="rgba(0, 0, 0, 0)"
          >
             
            <v-toolbar-title class="text-subtitle-2 white--text pl-0 ">
              Backend Team <br>
              <span class="caption grey--text">Vuejs Vuetify</span>
            </v-toolbar-title>

            <v-spacer></v-spacer>
            <v-btn
              color="#7C7C7F"
              icon
              small
            >
              <v-icon>mdi-dots-vertical</v-icon>
            </v-btn>
          </v-app-bar>
           <v-app-bar
            flat
            color="rgba(0, 0, 0, 0)"
            class="mt-n7"
          >
            <v-avatar size="30">
              <img
                src="https://cdn.vuetifyjs.com/images/lists/4.jpg"
                alt="John"
              >
            </v-avatar>
             <v-avatar class="ml-n3" size="30">
              <img
                src="https://cdn.vuetifyjs.com/images/lists/1.jpg"
                alt="John"
              >
            </v-avatar>
            <v-avatar class="ml-n3" size="30">
              <img
                src="https://cdn.vuetifyjs.com/images/lists/3.jpg"
                alt="John"
              >
            </v-avatar>
            <v-avatar class="ml-n3" size="30">
              <img
                src="https://cdn.vuetifyjs.com/images/lists/5.jpg"
                alt="John"
              >
            </v-avatar>
          

            
          </v-app-bar>
           <v-app-bar
            flat
            color="rgba(0, 0, 0, 0)"
            class="mt-n6"
          >
            <span
             class="grey--text"
              small
            >
              Progress
            </span>
            <v-spacer></v-spacer> 
             <span
             class="caption grey--text"
            >
              95%
            </span>
          </v-app-bar>
      
          <v-app-bar
            flat
            color="rgba(0, 0, 0, 0)"
            class="mt-n10"
          >
          <v-progress-linear
      color="green"
      height="6"
      value="95"
     
    ></v-progress-linear>
           
          </v-app-bar>
<v-card-text class="pt-0">
  <v-row>
    <v-col cols="12" sm="8">
<v-icon
      class="mr-2"
        small
        color="#7C7C7F"
      >
        fas fa-share-alt
      </v-icon>
      <span class="text-caption grey--text font-weight-light">5</span>
      <v-icon
      class="ml-2 mr-2"
        small
        color="#7C7C7F"
      >
       far fa-comment-dots
      </v-icon>
      <span class="text-caption grey--text font-weight-light">3</span>
    </v-col>
    <v-col cols="12" sm="4">
       <v-chip
        dark
        color="#7C7C7F"
        class=""
        small
      >
        <v-icon left small>
          mdi-alarm-check
        </v-icon>
        2 Week left
      </v-chip>
    </v-col>
  </v-row>
      
     
     
    </v-card-text>
      </v-card>
         </v-col>
         <v-col cols="12" sm="4">
            <v-card  color="#22222C" class="rounded-lg" elevation="10">
          <v-app-bar
            flat
            color="rgba(0, 0, 0, 0)"
          >
             
            <v-toolbar-title class="text-subtitle-2 white--text pl-0 ">
              Software Testing <br>
              <span class="caption grey--text">Developement</span>
            </v-toolbar-title>

            <v-spacer></v-spacer>
            <v-btn
              color="#7C7C7F"
              icon
              small
            >
              <v-icon>mdi-dots-vertical</v-icon>
            </v-btn>
          </v-app-bar>
           <v-app-bar
            flat
            color="rgba(0, 0, 0, 0)"
            class="mt-n7"
          >
            <v-avatar size="30">
              <img
                src="https://cdn.vuetifyjs.com/images/lists/4.jpg"
                alt="John"
              >
            </v-avatar>
             <v-avatar class="ml-n3" size="30">
              <img
                src="https://cdn.vuetifyjs.com/images/lists/1.jpg"
                alt="John"
              >
            </v-avatar>
            <v-avatar class="ml-n3" size="30">
              <img
                src="https://cdn.vuetifyjs.com/images/lists/3.jpg"
                alt="John"
              >
            </v-avatar>
          

            
          </v-app-bar>
           <v-app-bar
            flat
            color="rgba(0, 0, 0, 0)"
            class="mt-n6"
          >
            <span
             class="grey--text"
              small
            >
              Progress
            </span>
            <v-spacer></v-spacer> 
             <span
             class="caption grey--text"
            >
              75%
            </span>
          </v-app-bar>
      
          <v-app-bar
            flat
            color="rgba(0, 0, 0, 0)"
            class="mt-n10"
          >
          <v-progress-linear
      color="green"
      height="6"
      value="75"
     
    ></v-progress-linear>
           
          </v-app-bar>
<v-card-text class="pt-0">
  <v-row>
    <v-col cols="12" sm="8">
<v-icon
      class="mr-2"
        small
        color="#7C7C7F"
      >
        fas fa-share-alt
      </v-icon>
      <span class="text-caption grey--text font-weight-light">5</span>
      <v-icon
      class="ml-2 mr-2"
        small
        color="#7C7C7F"
      >
       far fa-comment-dots
      </v-icon>
      <span class="text-caption grey--text font-weight-light">3</span>
    </v-col>
    <v-col cols="12" sm="4">
       <v-chip
        dark
        color="#7C7C7F"
        class=""
        small
      >
        <v-icon left small>
          mdi-alarm-check
        </v-icon>
        2 Week left
      </v-chip>
    </v-col>
  </v-row>
      
     
     
    </v-card-text>
      </v-card>
         </v-col>
       </v-row>
  </v-container>
 </v-app>
</template>

<script>
  import SideBar from '../components/SideBar'
  import RightSideBar from '../components/RightSideBar'

  export default {
    name: 'Home',
    data: () => ({
selectedItem: 2,
      items: [
        { text: 'Real-Time'},
        { text: 'Audience' },
        { text: 'Conversions' },
      ],
    }),

    components: {
      SideBar,
      RightSideBar
    },
  }
</script>
<style scoped>
.theme--light.v-timeline::before {
    background: #7C7C7F !important;
}
.border  {
  
    background: #22222C ;
    border-radius: 50%;
    
    
}
</style>
