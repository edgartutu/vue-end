<template>
    <v-toolbar>
    <v-toolbar-title>{{title}}</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar-items class="hidden-sm-and-down">
      
      <v-icon>person</v-icon>
     
      
    </v-toolbar-items>
  </v-toolbar>
    
</template>
<script>
export default {
    data(){
        return{
            title:"Admin"
        }
    },
    name:"App"
}
</script>

