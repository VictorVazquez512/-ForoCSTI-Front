<template>
  <v-container fluid class="contenido">
    <v-app>
      <h1 class="title d-inline">Listado de Usuarios</h1>
      <template>
        <v-card>
          <v-tabs>
            <v-tab> Usuarios </v-tab>
            <v-tab> Publicaciones </v-tab>
            <v-tab-item>
              <v-card flat>
                <v-card-text>
                  <v-divider class="mb-2"></v-divider>
                  <template>
                    <v-data-table
                      :headers="headers"
                      :items="primeraLista"
                      :search="search"
                      class="elevation-1"
                    >
                      <template v-slot:top>
                        <v-toolbar flat>
                          <v-toolbar-title>Listado de usuarios</v-toolbar-title>
                          <v-divider class="mx-4" inset vertical></v-divider>
                          <v-spacer></v-spacer>
                          <v-spacer></v-spacer>
                          <v-text-field
                            v-model="search"
                            append-icon="mdi-magnify"
                            label="Buscar"
                            single-line
                            hide-details
                          ></v-text-field>
                        </v-toolbar>
                        <v-divider></v-divider>
                      </template>
                      <template v-slot:[`item.botonAdmin`]="{ item }" >
                        <div>
                          <v-btn
                            small
                            color="blue"
                            v-model="item.botonAdmin"
                            :disabled="item.admin"
                            :dark="!item.admin"
                          >Administrador<v-icon class="pl-1">mdi-account-tie</v-icon></v-btn>
                        </div>
                      </template>
                      <template v-slot:no-data>
                        <v-btn color="primary" @click="lista()">
                          Reintentar
                        </v-btn>
                      </template>
                    </v-data-table>
                  </template>
                  <!-- Fin empresas modal -->
                </v-card-text>
              </v-card>
            </v-tab-item>
            <v-tab-item>
              <v-card flat>
                <v-card-text>
                  <v-divider class="mb-2"></v-divider>
                  <template>
                    <v-data-table
                      :headers="headersSecond"
                      :items="segundaLista"
                      :search="search"
                      class="elevation-1"
                    >
                      <template v-slot:top>
                        <v-toolbar flat>
                          <v-toolbar-title>Listado de publicaciones</v-toolbar-title>
                          <v-divider class="mx-4" inset vertical></v-divider>
                          <v-spacer></v-spacer>
                          <v-spacer></v-spacer>
                          <v-text-field
                            v-model="search"
                            append-icon="mdi-magnify"
                            label="Buscar"
                            single-line
                            hide-details
                          ></v-text-field>
                        </v-toolbar>
                        <v-divider></v-divider>
                      </template>
                      <template v-slot:[`item.eliminar`]="{ item }" >
                        <div>
                          <v-btn
                            small
                            color="red"
                            v-model="item.eliminar"
                            dark
                          >Eliminar<v-icon>mdi-book-off-outline</v-icon></v-btn>
                        </div>
                      </template>
                      <template v-slot:no-data>
                        <v-btn color="primary" @click="lista()">
                          Reintentar
                        </v-btn>
                      </template>
                    </v-data-table>
                  </template>
                  <!-- Fin empresas modal -->
                </v-card-text>
              </v-card>
            </v-tab-item>
          </v-tabs>
        </v-card>
      </template>
    </v-app>
  </v-container>
</template>
  
  <script>
export default {
  data: () => ({
    search: '',
    headers: [
      {
        text: "Usuarios",
        align: "start",
        sortable: false,
        value: "name",
      },
      { text: "Tipo de usuario", value: "tipo" },
      { text: "Hacer administrador", value: "botonAdmin",  sortable: false, },
    ],
    headersSecond: [
      {
        text: "Usuario",
        align: "start",
        sortable: false,
        value: "user",
      },
      { text: "Fecha de publicacion", value: "fechaPublicacion" },
      { text: "Publicacion", value: "eliminar",  sortable: false, },
    ],
    primeraLista: [
      {
        name: "Jose Manuel",
        tipo: "Usuario",
        admin: false,
        botonAdmin:false
      },
      {
        name: "Manuel Ramirez",
        tipo: "Administrador",
        admin: true,
        botonAdmin:false
      },
    ],
    segundaLista: [
      {
        user: "Jose Manuel",
        fechaPublicacion: "01/12/22",
        eliminar:true
      },
      {
        user: "Jose Manuel",
        fechaPublicacion: "01/12/22",
        eliminar:true
      },
    ],
  }),
};
</script>