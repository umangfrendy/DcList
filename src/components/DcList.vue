<template>
  <div>
    <v-app-bar color="deep-purple accent-4" dense dark>
      <v-app-bar-nav-icon>
        <!-- <v-list-item-title></v-list-item-title> -->
      </v-app-bar-nav-icon>
      <v-btn icon>
        <v-icon>mdi-chevron-left</v-icon>
      </v-btn>

      <v-toolbar-title>DC List</v-toolbar-title>

      <v-spacer></v-spacer>
    </v-app-bar>

    <div class="font-weight-bold subtitle pa-2">Delivery Chalan Details</div>

    <div align="center">
      <h3>Delivery Otp:XXXX</h3>
      <div>
        <v-tabs center-active>
          <v-tab class="font-weight-bold"> Upcoming</v-tab>
          <v-tab class="font-weight-bold"> Delivered</v-tab>
        </v-tabs>
        <div>
          <template>
            <div>
              <v-col v-for="(item, i) in items" :key="i" cols="12">
                <v-expansion-panels class="mb-6">
                  <v-expansion-panel>
                    <v-expansion-panel-header expand-icon="mdi-chevron-down">
                      DC Number: {{ item.DC_Number }}
                    </v-expansion-panel-header>
                    <v-expansion-panel-content>
                      <v-row>
                        <v-col cols="6"
                          ><p>
                            Total items: <b>{{ item.total_items }}</b>
                          </p></v-col
                        >
                        <v-col cols="6"
                          ><p>
                            Total Amount: <b>{{ item.total_amount }}</b>
                          </p></v-col
                        >
                      </v-row>

                      <div>
                        <v-tabs center-active>
                          <v-tab @click="order" class="font-weight-bold">
                            ORDER</v-tab
                          >
                          <v-tab @click="product" class="font-weight-bold">
                            PRODUCT</v-tab
                          >
                        </v-tabs>
                        <!-- <v-dialog v-model="order"> -->
                          <v-row class="pt-6">
                            <p class="body-2">
                              Name: <b>{{ item.name }}</b>
                            </p>
                          </v-row>
                          <v-row>
                            <p class="body-2">
                              Number: <b>{{ item.number }}</b>
                            </p>
                          </v-row>
                          <v-row>
                            <p class="body-2">
                              Email: <b>{{ item.email }}</b>
                            </p>
                          </v-row>
                        <!-- </v-dialog> -->

                        <!-- <v-dialog v-model="product"> -->
                          <v-img
                            :src="item.src"
                            class="white--text align-end"
                            gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                            height="200px"
                            width="200px"
                          >
                            <v-card-title v-text="item.name"></v-card-title>
                          </v-img>
                        <!-- </v-dialog> -->
                        
                      </div>
                    </v-expansion-panel-content>
                  </v-expansion-panel>
                </v-expansion-panels>
              </v-col>
            </div>
          </template>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        DC_Number: "42122DC-75175",
        total_items: 2,
        total_amount: 243,
        name: "umang",
        number: 1212121212,
        email: "umang@g.c",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
      },
      {
        DC_Number: "42122DC-75345",
        total_items: 9,
        total_amount: 1113,
        name: "umang122",
        number: 1478521212,
        email: "umang2@g.c",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
      },
      {
        DC_Number: "42122DC-75225",
        total_items: 4,
        total_amount: 2343,
        name: "umang",
        number: 1212258963,
        email: "umang3@g.c",
        src: "https://cdn.vuetifyjs.com/images/cards/house.jpg   ",
      },
    ],
  }),
};
</script>
