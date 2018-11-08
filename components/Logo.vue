<template>
  <div class="logo">
    <el-tag type="success">{{ userList }}</el-tag>
    <el-table :data="userList">
      <el-table-column
        type="index"
        width="50"/>
      <el-table-column
        label="姓名"
        width="150">
        <template slot-scope="scope">{{ scope.row.name }}</template>
      </el-table-column>
      <el-table-column
        prop="age"
        label="年龄"
        width="150"/>
    </el-table>
  </div>
</template>
<script>
export default {
  props: {
    userList: {
      type: Array,
      default: () => []
    }
  }
}
</script>

<style>
</style>
