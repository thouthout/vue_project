<template>
  <div id="example">
    <p>Original message: "{{ msg }}"</p>
    <p>"{{ now }}"</p>
    <el-button type="info" plain @click="changeMsg">确认</el-button>
    <!-- <p>Computed reversed message: "{{ reversedMessage }}"</p> -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      msg: 'some msg is here'
    }
  },
  computed: {
    now: function () {
      return Date.now()
    }
  },
  watch:{
    msg: function(newMsg, oldMsg){
      alert(newMsg);
    }
  },
  created() {
      
  },
  methods: {
    changeMsg: function(){
      this.msg = 'hello vue'
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
