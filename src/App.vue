<template>
  <v-app>
    <v-navigation-drawer v-model="isDrawerOpen">
      <v-list>
        <v-list-subheader>Menu</v-list-subheader>
        <v-list-item prepend-icon="mdi-home">Home</v-list-item>
        <v-list-item prepend-icon="mdi-account">Usuários</v-list-item>

        <v-list-group value="Clientes">
          <template #activator="{ props }">
            <v-list-item v-bind="props" prepend-icon="mdi-account-circle">
              Clientes
            </v-list-item>
          </template>
          <v-list-item prepend-icon="mdi-chart-pie">Relatório</v-list-item>
          <v-list-item prepend-icon="mdi-file-chart">Atendimentos</v-list-item>
        </v-list-group>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar flat class="border-b">
      <v-app-bar-nav-icon @click="isDrawerOpen = !isDrawerOpen">
      </v-app-bar-nav-icon>
      <v-app-bar-title>Curso de Vuetify</v-app-bar-title>

      <template #append>
        <v-menu>
          <template #activator="{ props }">
            <v-btn icon class="mr-2" v-bind="props">
              <v-badge dot color="info">
                <v-icon icon="mdi-bell-outline"></v-icon>
              </v-badge>
            </v-btn>
          </template>
          <v-card min-width="300px" min-height="200px" max-height="400px">
            <v-card-title>Notificações</v-card-title>
            <v-list>
              <v-list-item>
                <v-card flat class="border">
                  <v-card-subtitle class="pt-3">Them de bordo</v-card-subtitle>
                  <v-card-text>
                    <div>Whitehaven Beach</div>
                    <div>Whitsunday Island, Whitsunday Islands</div>
                  </v-card-text>
                  <v-card-actions>
                    <v-btn variant="outlined" color="primary">Ver mais</v-btn>
                  </v-card-actions>
                </v-card>
              </v-list-item>

              <v-list-item>
                <v-card flat class="border">
                  <v-card-subtitle class="pt-3">Them de bordo</v-card-subtitle>
                  <v-card-text>
                    <div>Whitehaven Beach</div>
                    <div>Whitsunday Island, Whitsunday Islands</div>
                  </v-card-text>
                  <v-card-actions>
                    <v-btn variant="outlined" color="primary">Ver mais</v-btn>
                  </v-card-actions>
                </v-card>
              </v-list-item>
            </v-list>
          </v-card>
        </v-menu>

        <v-menu>
          <template #activator="{ props }">
            <v-avatar v-bind="props">
              <v-img
                cover
                src="https://images.pexels.com/photos/2194261/pexels-photo-2194261.jpeg"
              >
              </v-img>
            </v-avatar>
          </template>
          <v-card min-width="200px">
            <v-list :lines="false" density="compact" nav>
              <v-list-item prepend-icon="mdi-account-outline">
                <v-list-item-title>Perfil</v-list-item-title>
              </v-list-item>

              <v-list-item prepend-icon="mdi-heart-outline">
                <v-list-item-title>Favoritos</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-card>
        </v-menu>
      </template>
    </v-app-bar>

    <v-main>
      <v-container>
        <h1>Dashboard</h1>

        <v-card flat class="border mb-4">
          <v-card-title>Últimos Usuários</v-card-title>
          <v-table>
            <thead>
              <tr>
                <th>Nome</th>
                <th>E-mail</th>
                <th>Cargo</th>
                <th></th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>Fulano</td>
                <td>Fulano@gmail.com</td>
                <td>Adm</td>
                <td>
                  <v-btn variant="tonal" color="primary" >Editar</v-btn>
                </td>
              </tr>
              <tr>
                <td>Cicrano</td>
                <td>Cicrano@gmail.com</td>
                <td>Vendedor</td>
                <td>
                  <v-btn variant="tonal" color="primary" >Editar</v-btn>
                </td>
              </tr>
            </tbody>
          </v-table>
        </v-card>

        <v-row>
          <v-col cols="12" sm="6" md="4" lg="3">
            <v-card flat class="border">
              <v-img
                class="align-end text-white"
                src="https://images.pexels.com/photos/533630/pexels-photo-533630.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
              >
                <v-card-title>Top 10 lugares para visita</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">Them de bordo</v-card-subtitle>
              <v-card-text>
                <div>Whitehaven Beach</div>
                <div>Whitsunday Island, Whitsunday Islands</div>
              </v-card-text>
              <v-card-actions>
                <v-btn variant="outlined" color="primary">Ver mais</v-btn>
                <v-btn prepend-icon="mdi-cart" variant="tonal" color="blue">
                  Comprar
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-col>

          <v-col cols="12" sm="6" md="4" lg="3">
            <v-card flat class="border">
              <v-img
                class="align-end text-white"
                src="https://images.pexels.com/photos/533630/pexels-photo-533630.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
              >
                <v-card-title>Top 10 lugares para visita</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">Them de bordo</v-card-subtitle>
              <v-card-text>
                <div>Whitehaven Beach</div>

                <div>Whitsunday Island, Whitsunday Islands</div>
              </v-card-text>
              <v-card-actions>
                <v-btn variant="outlined" color="primary">Ver mais</v-btn>
                <v-btn prepend-icon="mdi-cart" variant="tonal" color="blue">
                  Comprar
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-col>

          <v-col cols="12" sm="6" md="4" lg="3">
            <v-card flat class="border">
              <v-img
                class="align-end text-white"
                src="https://images.pexels.com/photos/533630/pexels-photo-533630.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
              >
                <v-card-title>Top 10 lugares para visita</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">Them de bordo</v-card-subtitle>
              <v-card-text>
                <div>Whitehaven Beach</div>

                <div>Whitsunday Island, Whitsunday Islands</div>
              </v-card-text>
              <v-card-actions>
                <v-btn variant="outlined" color="primary">Ver mais</v-btn>
                <v-btn prepend-icon="mdi-cart" variant="tonal" color="blue">
                  Comprar
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-col>

          <v-col cols="12" sm="6" md="4" lg="3">
            <v-card flat class="border">
              <v-img
                class="align-end text-white"
                src="https://images.pexels.com/photos/533630/pexels-photo-533630.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
              >
                <v-card-title>Top 10 lugares para visita</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">Them de bordo</v-card-subtitle>
              <v-card-text>
                <div>Whitehaven Beach</div>

                <div>Whitsunday Island, Whitsunday Islands</div>
              </v-card-text>
              <v-card-actions>
                <v-btn variant="outlined" color="primary">Ver mais</v-btn>
                <v-btn prepend-icon="mdi-cart" variant="tonal" color="blue">
                  Comprar
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script setup>
import { ref } from "vue";

const isDrawerOpen = ref(false);
</script>
