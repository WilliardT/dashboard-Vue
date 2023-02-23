<template>
  <table>
    <thead>
        <img src="../assets/icons/sort.png" alt="sort" @click="clickOnDate()" >
      <tr>
        <th>Data</th>
        <th>Summary1</th>
        <th>Summary2</th>
        <th>Summary3</th>
        <th>Summary4</th>
        <th>Summary5</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(line, index) of sorting" :key="index" @sorting="setSort">
        <td class="tableName">{{ line.name }}</td>
        <td class="tableOther">{{ line.sum1 }}</td>
        <td class="tableOther">{{ line.sum2 }}</td>
        <td class="tableOther">{{ line.sum3 }}</td>
        <td class="tableOther">{{ line.sum4 }}</td>
        <td class="tableOther">{{ line.sum5 }}</td>
      </tr>
    </tbody>
  </table>
</template>

<script setup>
import { ref, computed } from "vue";

const sort = ref("name");
const sortAsc = ref("asc"); //

const sorting = computed(() => {
  return dataTable.value.sort((a, b) => {
    let modifier = 1;
    if (sortAsc.value === "desc") modifier = -1;
    if (a[sort.value] < b[sort.value]) return -1 * modifier;
    if (a[sort.value] > b[sort.value]) return 1 * modifier;
    
    return 0;
  });
});

const dataTable = ref([
  { name: "Data1", sum1: 186, sum2: 186, sum3: 92, sum4: 8, sum5: 1 },
  { name: "Data2", sum1: 95, sum2: 95, sum3: 31, sum4: 11, sum5: 0 },
  { name: "Data3", sum1: 329, sum2: 329, sum3: 256, sum4: 32, sum5: 4 },
  { name: "Data4", sum1: 804, sum2: 804, sum3: 697, sum4: 40, sum5: 22 },
]);


const clickOnDate = () => {
  if(sortAsc.value === 'asc') {
    sortAsc.value = 'desc'
  } else {
    sortAsc.value = 'asc'
  }
    
};

</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Racing+Sans+One&family=Roboto&display=swap");

th {
  font-family: "Quicksand";
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  letter-spacing: 0.44px;
  color: #919699;
}

thead > img {
  position: absolute;
  left: 427px;
  top: 171px;
  cursor: pointer;
}

.tableName {
  font-family: "Roboto";
  font-style: normal;
  font-weight: 500;
  font-size: 20px;
  line-height: 28px;
  letter-spacing: 0.15px;
  color: rgba(0, 0, 0, 0.87);
}

.tableOther {
  font-family: "Roboto";
  font-style: normal;
  font-weight: 500;
  font-size: 20px;
  line-height: 28px;
  text-align: right;
  letter-spacing: 0.15px;
  color: #5e6366;
}
</style>
