vue-pagination ������
����ʹ�ã�
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
total: 100,     // ��¼������   Ĭ�Ͽգ����С��pageNum���������ʾ   ����Number
pageNum: 10,    // ÿҳ��ʾ����,Ĭ��10                              ����Number
current: 2,     // ��ǰҳ����   Ĭ��Ϊ1                             ����Number
pagegroup:5,     // ��ҳ����     Ĭ��Ϊ5���贫������                  ����Number
}
},
computed:{
},
methods: {
pagechange:function(current){     // ҳ��ı䴫���µ�ҳ�룬�˴����ص�
console.log(current);
},
},
mounted: function () {
},

}
</script>