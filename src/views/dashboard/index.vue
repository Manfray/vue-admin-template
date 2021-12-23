<template>
  <div class="dashboard-container">
    <!-- <div class="dashboard-text">name: {{ name }}</div> -->
    <!-- <div class="dashboard-text">引导页</div> -->
    <el-form
      ref="formRef"
      :model="form"
      size="small"
      label-width="80px"
      :rules="formRules"
    >
      <el-form-item label="操作值a" prop="a">
        <el-input v-model="form.a" placeholder="请输入操作值" clearable />
      </el-form-item>
      <el-form-item label="操作值b" prop="b">
        <el-input v-model="form.b" placeholder="请输入操作值" clearable />
      </el-form-item>
      <el-form-item label="操作值c" prop="c">
        <el-input v-model="form.c" placeholder="请输入操作值" clearable />
      </el-form-item>
      <el-form-item label="操作值d" prop="d">
        <el-input v-model="form.d" placeholder="请输入操作值" clearable />
      </el-form-item>
    </el-form>
    <el-button @click="volidate">验证</el-button>
    <el-button @click="test">修改验证</el-button>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
console.log('加载dashboard组件')
export default {
  name: 'Dashboard',
  data() {
    return {
      form: {
        a: '',
        b: '',
        c: '',
        d: ''
      },
      formRules: {
        a: [{ required: true, message: '请选择操作符', trigger: 'change' }],
        b: [{ required: true, message: '请选择操作符', trigger: 'change' }],
        c: [{ required: true, message: '请选择操作符', trigger: 'change' }],
        d: [{ required: true, message: '请选择操作符', trigger: 'change' }]
      }
    }
  },
  computed: {
    ...mapGetters([
      'name'
    ])
  },
  created() {
    console.log('dashboard created')
  },
  methods: {
    volidate() {
      this.$refs['formRef'].validate((valid) => {
        if (valid) {
          console.log('验证ok')
        } else {
          console.log('验证error')
        }
      })
    },
    test() {
      this.formRules['b'][0].required = !this.formRules['b'][0].required
    }
  }
}
</script>

<style lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}
</style>
