<template>
  <v-container>
    <v-layout>
      <v-flex>
        <v-card>
          <v-card-text>
            <v-form @submit.prevent="add">
              <v-text-field label="Name" v-model="name"></v-text-field>
            </v-form>
            <v-list>
              <v-list-tile v-for="(item, index) in items" :key="index">
                <v-list-tile-content>
                  <v-list-tile-text v-text="item"></v-list-tile-text>
                </v-list-tile-content>
                <v-list-tile-action>
                  <v-btn icon @click="remove(index)"><v-icon color="red">delete</v-icon></v-btn>
                </v-list-tile-action>
              </v-list-tile>
            </v-list>
          </v-card-text>
        </v-card>
      </v-flex>

      <v-btn fab fixed bottom right @click="add" icon ripple color="light-green"><v-icon color="white">add</v-icon></v-btn>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      items: []
    }
  },
  methods: {
    add() {
      if (this.name) {
        this.items.push(this.name)
        this.name = ''
      }
    },
    remove(index) {
      this.items.splice(index, 1)
    }
  }
}
</script>
