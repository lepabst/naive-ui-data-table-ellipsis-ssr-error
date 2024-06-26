<template>
  <div>
    <n-data-table :columns="columns" :data="data"></n-data-table>
  </div>
</template>

<script setup lang="ts">
import { NDataTable } from 'naive-ui';
import type { DataTableColumn } from 'naive-ui'

const columns: Array<DataTableColumn> = [
  {
    key: 'no',
    title: 'No',
  },
  {
    key: 'title',
    title: 'Title column ellipsis problem',
    width: 350,
    ellipsis: true
  },
  {
    key: 'length',
    title: 'Length',
  }
]

const data = [
  { no: 3, title: 'Wonderwall', length: '4:18' },
  { no: 4, title: "Don't Look Back in Anger", length: '4:48' },
  { no: 12, title: 'Champagne Supernova', length: '7:27' },
  { no: 47, title: 'Hitman', length: '3:33' },
  { no: 33, title: 'Way too long title to be displayed in a column just like that so we need to set ellipsis: true in the column', length: '3:33' }
]
</script>
