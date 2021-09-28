<template>
  <v-app>
    <v-app-bar app color="grey" dense dark>Search Demo</v-app-bar>
    <v-main>
      <v-row>
        <v-spacer></v-spacer>
        <v-col md="3">
          <v-text-field
            v-model="search"
            label="Search"
            append-icon="mdi-magnify"
          ></v-text-field>
        </v-col>
      </v-row>
      <v-card :elevation="4" class="ml-4 mr-4">
        <v-data-table
          id="data-table"
          :headers="columnDef"
          :items="datarecon"
          :search="search"
        >
        </v-data-table>
      </v-card>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    search: "",
    columnDef: [
      { text: "ID", value: "ID" },
      { text: "COUNT", value: "COUNT" },
      { text: "HITS", value: "HITS" },
    ],
    datarecon: [
      { ID: "ZX-925", COUNT: "857", HITS: "25" },
      { ID: "MS-526", COUNT: "956", HITS: "58" },
      { ID: "MA-723", COUNT: "796", HITS: "545" },
      { ID: "SP-563", COUNT: "676", HITS: "165" },
      { ID: "DF-243", COUNT: "566", HITS: "8765" },
      { ID: "FZ-123", COUNT: "906", HITS: "345" },
    ],
  }),
};
</script>
