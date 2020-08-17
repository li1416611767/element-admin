<!--
 * @Author: your name
 * @Date: 2020-08-17 10:09:46
 * @LastEditTime: 2020-08-17 10:55:53
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \sk007-web-uid:\vue-element-admin-master\src\views\dashboard\index.vue
-->
<template>
  <div class="dashboard-container">
    1111
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
import adminDashboard from './admin'
import editorDashboard from './editor'

export default {
  name: 'Dashboard',
  components: { adminDashboard, editorDashboard },
  data() {
    return {
      currentRole: 'adminDashboard'
    }
  },
  computed: {
    ...mapGetters([
      'roles'
    ])
  },
  created() {
    if (!this.roles.includes('admin')) {
      this.currentRole = 'editorDashboard'
    }
  }
}
</script>
