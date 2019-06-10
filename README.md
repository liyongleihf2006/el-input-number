# el-input-number
对element input number做了简单扩展,使其支持input所支持的前缀,后缀,前置和后置元素

使用方式:
```js
//单独引入的时候
import ElInputNumber from './el-input-number';
export default {
  components:{ElInputNumber}
}

//全局引入element-ui的时候,可以覆盖element-ui原装的el-input-number
import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css';
import ElInputNumber from "./el-input-number.vue";
Vue.use(ElementUI);
Vue.component(ElInputNumber.name,ElInputNumber);
```

模板中使用
```html
<el-input-number prefix-icon="el-icon-search" suffix-icon="el-icon-date" v-model="num" :controls="false" :min="1" :max="10" label="描述文字">
    <template slot="prepend">Http://</template>
    <template slot="append">.com</template>
    <!-- <i slot="prefix" class="el-input__icon el-icon-search"></i> -->
    <!-- <i slot="suffix" class="el-input__icon el-icon-date"></i> -->
</el-input-number>
```
