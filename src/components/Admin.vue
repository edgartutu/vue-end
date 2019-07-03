<template>


    
    <v-card height="700px"  class="grey" >
      
    <v-navigation-drawer 
      v-model="drawer"
      permanent
      absolute
    >
   
      <v-toolbar flat class="md-list-item" color="success">
            
            <h1>Admin</h1>
            
       </v-toolbar>
       

      <v-list class="md-list-item" >
        <v-divider></v-divider>

        <v-list-tile v-for="item in items" :key="item.title" router :to = "item.route">
          <v-list-tile-action class="md-list-item-content md-ripple" >
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>

          <v-list-tile-content color="success">
            <v-list-tile-title>{{ item.title }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
     
    
    </v-navigation-drawer>
    
  </v-card>
  
  
    
</template>

<script>

export default {
    
    data () {
      return {
        pending: 'pending proposals',
        drawer: true,
        items: [
          { title: 'Pending Proposal', icon: 'dashboard' ,route:'/admin'},
          { title: 'Approved Proposal', icon: 'question_answer' ,route: '/approvedproposals'},
          { title: 'Upload Projects', icon: 'dashboard',route: '/upload' },
          { title: 'View projects', icon: 'dashboard', route: '/viewprojects' },
          { title: 'Messages', icon: 'dashboard', route: '/messages' },
          { title: 'Logout', icon: 'dashboard', route: '/' }
        ],
        right: null
      }
    
  
  }
};
   

</script>
