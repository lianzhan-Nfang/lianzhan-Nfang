<template>
  <div>
    <el-row>
      <!-- 按钮 -->
      <el-button>默认按钮</el-button>
      <el-button type="primary">主要按钮</el-button>
      <el-button type="success">成功按钮</el-button>
      <el-button type="info">信息按钮</el-button>
      <el-button type="warning">警告按钮</el-button>
      <el-button type="danger">危险按钮</el-button>
    </el-row>
    <div>
      <!-- link文字链接 -->
      <el-link href="https://element.eleme.io" target="_blank"
        >默认链接</el-link
      >
      <el-link type="primary">主要链接</el-link>
      <el-link type="success">成功链接</el-link>
      <el-link type="warning">警告链接</el-link>
      <el-link type="danger">危险链接</el-link>
      <el-link type="info">信息链接</el-link>
    </div>
    <div>
      <!-- 单选框 -->
      <el-radio v-model="radio" label="1">备选项</el-radio>
      <el-radio v-model="radio" label="2">备选项</el-radio>
    </div>
    <div>
      <!-- 多选框 -->
      <!-- `checked` 为 true 或 false -->
      <el-checkbox v-model="checked">备选项</el-checkbox>
    </div>

    <div>
      <!-- 输入框 -->
      <el-input v-model="input" placeholder="请输入内容"></el-input>
    </div>

    <template>
      <!-- 计数器 -->
      <el-input-number
        v-model="num"
        @change="handleChange"
        :min="1"
        :max="10"
        label="描述文字"
      ></el-input-number>
    </template>

    <template>
      <!-- 选择器 -->
      <el-select v-model="value" placeholder="请选择">
        <el-option
          v-for="item in options"
          :key="item.value"
          :label="item.label"
          :value="item.value"
        >
        </el-option>
      </el-select>
    </template>


  </div>
</template>

  </div>
</template>

<script>
export default {
  data() {
    return {
      radio: "1",
      checked: true,
      input: "",
      num: 1,
      options: [{
          value: '选项1',
          label: '黄金糕'
        }, {
          value: '选项2',
          label: '双皮奶'
        }, {
          value: '选项3',
          label: '蚵仔煎'
        }, {
          value: '选项4',
          label: '龙须面'
        }, {
          value: '选项5',
          label: '北京烤鸭'
        }],
        value: ''
    };
  },
  methods: {
    handleChange(value) {
      console.log(value);
    },
  },
};
</script>

<style lang="scss" scoped>
</style>