<template>
  <div class="black-bg">
    <div class="white-bg">
      <h4>상세페이지임</h4>
      <p>상세페이지 내용임</p>
    </div>
  </div>

  <div class="menu">
    <a v-for="(a,i) in 메뉴들" :key="i">{{a}}</a>
  </div>



  <div>
    <img src="./assets/room0.jpg" class="room-img">
    <h4>{{products[0]}}</h4>
    <p>50만원</p>
    <button @click="신고수[0]++">허위매물신고</button><span>신고수:{{신고수[0]}}</span>
  </div>
  <div>
    <img src="./assets/room1.jpg" class="room-img">
    <h4>{{products[1]}}</h4>
    <p>80만원</p>
    <button @click="신고수[1]++">허위매물신고</button><span>신고수:{{신고수[1]}}</span>
  </div>
  <div>
    <img src="./assets/room2.jpg" class="room-img">
    <h4>{{products[2]}}</h4>
    <p>100만원</p>
    <button @click="신고수[2]++">허위매물신고</button><span>신고수:{{신고수[2]}}</span>
  </div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return{
      모달창열렸니:true,
      신고수:[0,0,0],
      메뉴들:['Home','Shop','About'],
      products:['역삼동원룸','천호동원룸','마포구원룸'],
      price:['50만원','100만원','80만원'],
    }
  },
  methods:{
    increase(){
      this.신고수[0]+=1;
      console.log(this)
    }
  },
  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu{
  background: darkslateblue;
  padding:15px;
  border-radius:5px;
  display:flex;
  flex-direction: row;
}

.menu a{
  color:white;
  padding:10px;
}

.room-img{
  width:100%;
  margin-top: 40px;
}

body{
  margin:0;
}
div{
  box-sizing: border-box;
}
.black-bg{
  width:100%;height:100%;
  background:rgba(0,0,0,0.5);
  position:fixed;padding:20px
}
.white-bg{
  width:100%;background:white;
  border-radius: 8px;
  padding:20px;
}
</style>
