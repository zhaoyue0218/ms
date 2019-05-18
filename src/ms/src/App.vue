<template>
  <div id="app">
    <!-- <HelloWorld/> -->
    <header>
      <ul>
        <li><i class="icon iconfont icon-zuojiantou-01"></i></li>
        <li>面试列表</li>
        <li>
        <span><i class="icon iconfont icon-gengduo"></i></span>
        <span><i class="icon iconfont icon-gengduo"></i></span>
        </li>
      </ul>
      <ol>
        <li v-for="(item,index) in data" :key="index" :class="{active:index==ind}" v-on:click="activ(index)">{{item.lis}}</li>
      </ol>
    </header>
    <mysection :data="data[ind].inners" :ind="ind" >
    </mysection>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Mysection from './components/mysection'
import './fonts/iconfont.css'
import data from './mock/data.json'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Mysection
  },
    data(){
        return {
            data:data,
            ind:0
        }
    },
    methods:{
      activ(index){
        console.log(index)
        this.ind=index
      }
    }
}
</script>

<style>
*{
  list-style: none;
  margin:0;
  padding:0;
}
body,html{
  width: 100%;
  height: 100%;
}
#app {
  width: 100%;
  height: 100%;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: flex;
  flex-direction: column;
}
.active{
  color: skyblue;
  border-bottom: 1px solid skyblue;
}
header{
  width: 100%;
  height:80px;

  display: flex;
  justify-content: space-between;
  flex-direction: column;
}
header ul{
 width: 100%;
  height: 40px;
  box-sizing: border-box;
  padding: 0 10px;
 display: flex;
  align-items: center;
  justify-content: space-between;
  border-bottom: 1px solid #ccc;
}
header ol{
  width: 100%;
  height: 40px;
  box-sizing: border-box;
  padding: 0 10px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
header ol li{
  height: 100%;
  display: flex;
  align-items: center;
  border-bottom: 1px solid #fff;
}
</style>
