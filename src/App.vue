<script setup lang="ts">
import { Check, Delete, Edit, Message, Search, Star, Sunny, Moon } from '@element-plus/icons-vue'

import { useDark } from "@vueuse/core"

const value2 = useDark()

const tableData = [
  {
    date: '2016-05-03',
    name: 'Tom',
    address: 'No. 189, Grove St, Los Angeles',
  },
  {
    date: '2016-05-02',
    name: 'Tom',
    address: 'No. 189, Grove St, Los Angeles',
  },
  {
    date: '2016-05-04',
    name: 'Tom',
    address: 'No. 189, Grove St, Los Angeles',
  },
  {
    date: '2016-05-01',
    name: 'Tom',
    address: 'No. 189, Grove St, Los Angeles',
  },
]

</script>

<template>
  <div class="common-layout">
    <el-container class="h-screen">
      <el-header class="flex items-center justify-between bg-cyan">
        <div>Logo</div>
        <div>
          <el-switch size="large" v-model="value2" class="mt-2" style="margin-left: 24px" inline-prompt
            :active-action-icon="Moon" :inactive-action-icon="Sunny" />
        </div>
      </el-header>
      <el-container>
        <el-aside width="200px" class="bg-pink">Aside</el-aside>
        <el-container>
          <el-main>
            <div class="p-4">
              <h1 class="mb-6">Button按钮</h1>
              <div class="mb-4">
                <el-button>Default</el-button>
                <el-button type="primary">Primary</el-button>
                <el-button type="success">Success</el-button>
                <el-button type="info">Info</el-button>
                <el-button type="warning">Warning</el-button>
                <el-button type="danger">Danger</el-button>
              </div>

              <div class="mb-4">
                <el-button plain>Plain</el-button>
                <el-button type="primary" plain>Primary</el-button>
                <el-button type="success" plain>Success</el-button>
                <el-button type="info" plain>Info</el-button>
                <el-button type="warning" plain>Warning</el-button>
                <el-button type="danger" plain>Danger</el-button>
              </div>

              <div class="mb-4">
                <el-button round>Round</el-button>
                <el-button type="primary" round>Primary</el-button>
                <el-button type="success" round>Success</el-button>
                <el-button type="info" round>Info</el-button>
                <el-button type="warning" round>Warning</el-button>
                <el-button type="danger" round>Danger</el-button>
              </div>

              <div>
                <el-button :icon="Search" circle />
                <el-button type="primary" :icon="Edit" circle />
                <el-button type="success" :icon="Check" circle />
                <el-button type="info" :icon="Message" circle />
                <el-button type="warning" :icon="Star" circle />
                <el-button type="danger" :icon="Delete" circle />
              </div>
            </div>
            <div class="p-4">
              <h2 class="mb-6">基础表格</h2>
              <el-table :data="tableData" style="width: 100%">
                <el-table-column prop="date" label="Date" width="180" />
                <el-table-column prop="name" label="Name" width="180" />
                <el-table-column prop="address" label="Address" />
              </el-table>
            </div>
          </el-main>
          <el-footer>Footer</el-footer>
        </el-container>
      </el-container>
    </el-container>
  </div>
</template>

<style scoped></style>
