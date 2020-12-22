# plusbutton
‣example

----index.html----
````
<div id="AppPlus">
      <mycomp
      :width = 500
      :height = 300
      @plusclick="plus"></mycomp> //@plusclick: ボタンが押されたら発火
  </div>
  ````
  
  ----index.js----
  ````
import Vue from 'vue';
import AppMinus from 'plusbutton';

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
````
