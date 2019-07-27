<template>
  <div>
    <a-button @click="doSomeThing" type="primary">Primary</a-button>
    <a-button>Default{{ msg }}</a-button>
    <a-button type="dashed">Dashed"{{ test }}"</a-button>
    <a-button type="danger">Danger</a-button>
  </div>
</template>
<script>
import Vue from 'vue';
import { Button } from 'ant-design-vue';
Vue.use(Button);
// doSomething = () => {
//   console.log(11111);
// }
export default {
  name: 'HelloWorld',
  data() {
    return {
      test: 'test',
    }
  },
  methods: {
    doSomeThing() {
      console.log(this.propFunc);
      this.$data.test = this.propFunc.name;
    }
  },
  props: {
    msg: String,
    propFunc: {
      type: Object,
      default: function () {
        return { propFunc }
      }
    },
  }
}
</script>
