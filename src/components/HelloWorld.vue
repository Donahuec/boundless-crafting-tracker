<template>
    <v-content>
      <v-container>
        <v-expansion-panels>
          <v-expansion-panel
            v-for="(item,i) in recipes"
            :key="i"
          >
            <v-expansion-panel-header>{{item.name}}</v-expansion-panel-header>
            <v-expansion-panel-content>
              <v-simple-table>
                <tbody>
                  <tr>
                    <td>Id:</td>
                    <td>{{item.id}}</td>
                  </tr>
                  <tr>
                    <td>Description:</td>
                    <td>{{item.description}}</td>
                  </tr>
                  <tr>
                    <td>Machine:</td>
                    <td>{{item.machine}}</td>
                  </tr>
                </tbody>
              </v-simple-table>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-container>
    </v-content>

</template>

<script>
  export default {
    props: ['recipes'],
    data: () => ({

    }),
  }
</script>