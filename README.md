# plusbutton

‣example
----index.html----
  <div id="AppNum">
      <mycomp
      :width = 500
      :height = 300
      :number = 10　//表示する数字
      @numclick="num"></mycomp>　@numclick: 押されたときに発火
  </div>
  <div id="AppPlus">
      <mycomp
      style="border: solid 1px;"
      style="width: 100px;"
      style="height: 100px;"
      :width = 500
      :height = 300
      @plusclick="plus"></mycomp>　@plusclick: 押されたときに発火
  </div>
  <div id="AppMinus">
      <mycomp
      :width = 500
      :height = 300
      @minusclick="minus"></mycomp> @minusclick: 押されたときに発火
  </div>
  
  
  import Vue from 'vue';
import AppPlus from 'plusbutton';
import AppMinus from 'minusbutton';
import AppNum from 'numbutton';


----index.js----
new Vue({
    el: '#AppPlus',
    components: {
        'mycomp': AppPlus
    },
    methods: {
        plus(){
            console.log("plus")
        }
    }
}) 
new Vue({
    el: '#AppMinus',
    components: {
        'mycomp': AppMinus
    },
    methods: {
        minus(){
            console.log("minus")
        }
    }
}) 
new Vue({
    el: '#AppNum',
    components: {
        'mycomp': AppNum
    },
    methods: {
        num(){
            console.log("num")
        }
    }
}) 
