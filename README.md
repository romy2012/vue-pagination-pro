vue-pagination 改良版
父级使用：
<template>
<div>

<pagination
:total="total"
:myCurrentPage="current"
:skin="skin"
:pagenum="pageNum"
:pagegroup="pagegroup"
@change="pagechange"
></pagination>

</div>
</template>

<script>
import pagination from '../components/public/PublicPage.vue'
export default {
components: {
pagination
},
props: {
},
data (){
return{
total: 100,     // 记录总条数   默认空，如果小于pageNum则组件不显示   类型Number
pageNum: 10,    // 每页显示条数,默认10                              类型Number
current: 2,     // 当前页数，   默认为1                             类型Number
pagegroup:5,     // 分页条数     默认为5，需传入奇数                  类型Number
}
},
computed:{
},
methods: {
pagechange:function(current){     // 页码改变传入新的页码，此处做回调
console.log(current);
},
},
mounted: function () {
},

}
</script>