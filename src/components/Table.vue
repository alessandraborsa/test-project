<script setup>
import {data} from '../../public/dataTable.json'

</script>

<template>
  
  <table class="table">
    <thead>
      <tr>
        <th>Immagine</th>
        <th>Id</th>
        <th>Azienda</th>
        <th>CO2 (kg)</th>
        <th>Progetto</th>
        <th>Tipo</th>
        <th>Origine</th>
        <th>Data</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="element in data" :key="element.id">
        <td><img class="table-image-row" :src=element.image></td>
        <td>{{ element.internal_id }}</td>
        <td>{{ element.details.entity_name }}</td>
        <td>{{ element.formatted_quantity_kg }}</td>
        <td>{{ element.details.project_name }}</td>
        <td>{{ element.details.project_type }}</td>
        <td>{{ element.details.country_name }}</td>
        <td>{{ element.details.transaction_datetime }}</td>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  data() {
    return {
      data
    };
  }
};
</script>

<style scoped>
  .table {
    color: black;
    padding: 80px;
    width: 100%;
  }
  .table-image-row {
    height: 70px;
    width: 70px;
  }
</style>
