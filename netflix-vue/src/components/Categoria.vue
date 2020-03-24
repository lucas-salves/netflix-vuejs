<template>
    <div class="slider">
      <h3> {{titulo}} </h3>
      <span @mouseover="scrollToLeft" @mouseout="clearScroll" class="handle handlePrev active">
        <i class="fa fa-caret-left" aria-hidden="true"></i>
      </span>

      <div ref="scroller" class="row">
        <div class="row__inner">
          <filme titulo="Doctor Who" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"/>
          <filme titulo="Doctor Who" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"/>
          <filme titulo="Doctor Who" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"/>
          <filme titulo="Doctor Who" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"/>
          <filme titulo="Doctor Who" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"/>
          <filme titulo="Doctor Who" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"/>
          <filme titulo="Doctor Who" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"/>

        </div> 
      </div>

      <span @mouseover="scrollToRight"  @mouseout="clearScroll" class="handle handleNext active">
        <i class="fa fa-caret-right" aria-hidden="true"></i>
      </span>

    </div>
</template>

<script>
import Filme from './Filme.vue';

export default {
    components:{
      Filme
    },
    props: ['titulo'],
    methods:{
    scrollToRight(){
      this.intervalo = setInterval(() => {
        this.$refs.scroller.scrollLeft += 1
      }, 5);
    },
    scrollToLeft(){
      this.intervalo = setInterval(() => {
        this.$refs.scroller.scrollLeft -= 1
      }, 5);
    },
    clearScroll(){
      clearInterval(this.intervalo);
    }
  }
}
</script>

<style >

</style>