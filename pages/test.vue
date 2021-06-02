<template>
  <v-card hover rounded>
    <v-container class="pa-0" fluid fill-height>
      <v-row>
        <v-col cols="6">
          <v-text-field label="URL" v-model="url" />
          <iframe class="mini" width="600" height="400" :src="url"></iframe>
        </v-col>
        <v-col cols="6">
          <v-card>
            <iframe width="1000" height="800" :src="url"></iframe>
          </v-card>
          <!-- <v-dialog v-model="dialog" fullscreen>
            <template v-slot:activator="{ on, attrs }">
              <v-btn color="red lighten-2" dark v-bind="attrs" v-on="on">
                Click Me
              </v-btn>
            </template>

            <v-card>
              <iframe
                width="1000"
                height="800"
                src="https://character-sheets.appspot.com/shinobigami/edit.html?key=ahVzfmNoYXJhY3Rlci1zaGVldHMtbXByFwsSDUNoYXJhY3RlckRhdGEY7Kz-wAMM"
              ></iframe>

              <v-divider></v-divider>

              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn color="primary" text @click="dialog = false">
                  I accept
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-dialog> -->
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>

<style>
.mini {
  transform: scale(0.8);
  transform-origin: 0 0;
}
</style>
<script>
export default {
  data() {
    return {
      dialog: false,
      url: 'https://character-sheets.appspot.com/shinobigami/edit.html?key=ahVzfmNoYXJhY3Rlci1zaGVldHMtbXByFwsSDUNoYXJhY3RlckRhdGEY7Kz-wAMM',
    }
  },
}
</script>
