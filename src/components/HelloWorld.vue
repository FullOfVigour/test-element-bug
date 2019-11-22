<template>
  <div class="hello">
    <el-transfer
      v-model="value4"
      :titles="['未分配人员', '已分配人员']"
      :props="{
        key: 'id',
        label: 'name'
      }"
      :data="data3"
    >
    </el-transfer>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data() {
    const generateData3 = () => {
      const data = [];
      for (let i = 1; i <= 15; i++) {
        data.push({
          id: i,
          name: `${i}sadsadasda`,
          disabled: i % 4 === 0
        });
      }
      return data;
    };
    return {
      data3: generateData3(),
      value4: []
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
