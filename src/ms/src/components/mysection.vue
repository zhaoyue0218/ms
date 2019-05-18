<template>
    <div class="section">
<!-- {{ind}} -->
<ul  v-for="(item,index) in data" :key="index" >
    <li><h4>{{item.nav}}</h4><span>{{item.fangqi}}</span></li>
    <li>{{item.dizhi}}</li>
    <li>{{item.shijian}}<span >{{item.tixing}}</span></li>
    <li >{{item.nul}}</li>
</ul>
    </div>
</template>
<script>
export default {
    props:["data","ind"],
    components:{

    },
    data(){
        return {
           col:'#skyblue'
        }
    },
    computed:{

    },
    methods:{

    },
    created(){

    },
    mounted(){

    }
}
</script>
<style scoped lang="">
.section{
    width: 100%;
    flex-grow:1;
}
.section ul{
 width: 100%;
  /* height: 40px; */
  box-sizing: border-box;
  padding: 10px 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  border-top:10px solid #eee;
}
.section ul li{
 width: 100%;
 display: flex;
 align-items: center;
 justify-content: space-between;
 margin: 3px;
}
.section ul li:nth-child(1) h4{
    font-size: 20px;
}
.section ul li:nth-child(1) span{
    font-size: 14px;
    background: rgb(253, 227, 227);
    color: rgb(236, 113, 113);
    padding: 5px 5px;
}
.section ul li:nth-child(2){
    font-size: 17px;
    color: #ccc;
}
.section ul li:nth-child(3){
    /* font-size: 17px; */
    color: rgb(122, 120, 120);
}
.section ul li:nth-child(3) span{
    font-size: 14px;
    background: rgb(238, 237, 237);
    color: rgb(189, 184, 184);
    padding: 5px 5px;
}
</style>