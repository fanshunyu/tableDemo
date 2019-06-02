<template>
  <div class="index">
    <el-data-table v-bind="tableConfig" ></el-data-table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tableConfig: {
        url: '/mock/11/components',
        columns: [
          { type: 'selection'},
          {
            prop: 'name',
            label: '组件名称'
          },
          {
            prop: 'category',
            label: '分类'
          },
          {
            prop: 'version',
            label: '版本'
          },
          {
            prop: 'lang',
            label: '开发语言'
          },
          {
            prop: 'last_up_time',
            label: '最后更新时间'
          },
          {
            prop: 'state',
            label: '状态',
            formatter: row => (row.state === 'normal' ? '上架' : '下架')
          }
        ],
        searchForm: [
          {
            $type: 'input',
            $id: 'name',
            label: '组件名称',
            $el: {
              placeholder: '请输入'
            }
          },
          {
            $type: 'select',
            $id: 'category',
            label: '分类',
            $el: {
              placeholder: '请输入'
            }
          },
          {
            $type: 'select',
            $id: 'state',
            label: '状态',
            $el: {
              placeholder: '请输入'
            }
          }
        ],
        form: [
          {
            $type: 'input',
            $id: 'name',
            label: '组件名',
            $el: {
              placeholder: '请输入'
            },
            rules: [
              {
                required: true,
                message: '请输入用户名',
                trigger: 'blur'
              }
            ]
          }
        ],
        extraButtons: [
          {
            type: 'danger',
            text: '删除'
          }
        ]
      }
    }
  },
  methods: {}
}
</script>
<style lang="less">
.index {
  .home-img {
    width: 100%;
  }
}
</style>
