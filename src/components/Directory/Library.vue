<template>
<nav class="ma-0 pa-0">
  <v-navigation-drawer depressed class="ma-0 pa-0" width="auto">

<v-container depressed
  class="ma-0 pa-0">
  <v-text-field
  solo
  label="Search Projects"
  prepend-inner-icon="mdi-magnify"
  class="ma-0 pa-0 ">
  </v-text-field>

      <v-list-group
        prepend-icon="mdi-folder-outline"
        value="true"
      >
        <template v-slot:activator>
          <v-list-item-title>All Projects</v-list-item-title>
        </template>

        <v-list-group
          no-action
          sub-group
          value="true"
        >
          <template v-slot:activator>
            <v-list-item-content>
              <v-list-item-title>Plask1</v-list-item-title>
            </v-list-item-content>
          </template>

          <v-list-item
            v-for="(admin, i) in admins"
            :key="i"
            link
          >
            <v-list-item-title v-text="admin[0]"></v-list-item-title>
            <v-list-item-icon>
              <v-icon v-text="admin[1]"></v-icon>
            </v-list-item-icon>
          </v-list-item>
        </v-list-group>

        <v-list-group
          sub-group
          no-action
        >
          <template v-slot:activator>
            <v-list-item-content>
              <v-list-item-title>My Plask</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item
            v-for="(crud, i) in cruds"
            :key="i"
            @click="i"
          >
            <v-list-item-title v-text="crud[0]"></v-list-item-title>
            <v-list-item-action>
              <v-icon v-text="crud[1]"></v-icon>
            </v-list-item-action>
          </v-list-item>
        </v-list-group>
      </v-list-group>

  </v-container>
    </v-navigation-drawer>
</nav>

</template>

<style>
.Listbox {
  /* overflow: hidden; */
  background: #f5f5f5;
}
</style>

<script>
export default {
  data: () => ({
    admins: [
      ['Plask1'],
      ['My Plask']
    ],
    cruds: [
      ['Folder'],
      ['Scene 1'],
      ['Character 1']
    ]
  })
}
</script>
