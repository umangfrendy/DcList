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

      <!-- <v-menu
        left
        bottom
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            icon
            v-bind="attrs"
            v-on="on"
          >
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item
            v-for="n in 5"
            :key="n"
            @click="() => {}"
          >
            <v-list-item-title>Option {{ n }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu> -->
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
              <v-expansion-panels class="mb-6">
                <v-expansion-panel v-for="(item, i) in 5" :key="i">
                  <v-expansion-panel-header expand-icon="mdi-chevron-down">
                    Item
                  </v-expansion-panel-header>
                  <v-expansion-panel-content
                    >Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                    sed do eiusmod tempor incididunt ut labore et dolore magna
                    aliqua. Ut enim ad minim veniam, quis nostrud exercitation
                    ullamco laboris nisi ut aliquip ex ea commodo
                    consequat.</v-expansion-panel-content
                  >
                </v-expansion-panel>
              </v-expansion-panels>

            </div>
          </template>
        </div>
      </div>
    </div>
  </div>
</template>
