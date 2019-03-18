<template>
  <section class="container posts-page">
    <el-card>
      <div slot="header" class="clearfix">
        <span>新着投稿</span>
      </div>
      <el-table :data="showPosts" style="width: 100%;" class="table">
        <el-table-column prop="title" label="タイトル"></el-table-column>
        <el-table-column prop="user.id" label="投稿者" width="180"></el-table-column>
        <el-table-column prop="creted_at" label="投稿日時" width="240"></el-table-column>
      </el-table>
    </el-card>
  </section>
</template>

<script>
export default {
  computed: {
    showPosts() {
      return [
        {
          id: '001',
          title: 'How to develop Nuxt.js App',
          body: 'Loef feinm apanm ei utub elalsm dsdii',
          created_at: '2019/03/17 12:00:00',
          user: {
            id: 'canisterism'
          }
        },
        {
          id: '002',
          title: 'Deploy iiiiiiiiiiiiiiittttttttttt',
          body: 'Loef feinm apanm ei utub elalsm dsdii',
          created_at: '2019/03/18 00:00:00',
          user: {
            id: 'canisterism'
          }
        }
      ]
    }
  }
}
</script>
<style>
.posts-page .el-table__row {
  cursor: pointer;
}
</style>
