<template>
  <div class="chat">
    <div class="chat-content">
      <div class="chat-head">
        {{user}}
      </div>
      <div class="chat-body">
        <message type="asker"></message>
        <message type="answer" message="反弹全部反弹！！！！！！！！！！！！！！！！！！！你骂我的，说我的，全部反弹！！！！！！！！"></message>

      </div>
      <div class="chat-foot"></div>
    </div>
  </div>
</template>

<script>
  import message from '../components/message.vue'
  export default {
    name: 'chat',
    components: {
      message
    },
    data () {
      return {
        user: '岁月如同马匹',
        nowTime: '21:36',
        asker: {

        },
        answer: {

        },
        askList: [],
        answerList: []
      }
    }
  }
</script>

<style scoped lang="scss">
  .chat{
    height: 100%;
    max-width: 800px;
    min-width: 600px;
    margin: 0 auto;
    .chat-content{
      position: relative;
      background-color: #EEEEEE;
      max-height: 800px;
      height: 100%;
      border-radius: 4px;
      .chat-head{
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        padding: 10px 0;
        height: 40px;
        line-height: 40px;
        border-bottom: 1px solid #d6d6d6;
        text-align: center;
      }
      .chat-body{
        position: absolute;
        top: 60px;
        bottom: 200px;
        left: 0;
        right: 0;
        padding: 10px 20px;
      }
      .chat-foot{
        position: absolute;
        bottom: 0;
        left: 0;
        right: 0;
        padding: 10px 0;
        height: 180px;
        line-height: 40px;
        border-top: 1px solid #d6d6d6;
      }
    }
  }
</style>
