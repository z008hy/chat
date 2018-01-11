<template>
  <div class="message-content">
    <div class="asker" v-if="type==='asker'">
      <img src="../assets/asker.jpeg" alt="">
      <div class="message">
        {{message}}
      </div>
    </div>
    <div class="answer" v-else>
      <img src="../assets/answer.jpeg" alt="">
      <div class="message">{{message}}</div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'message',
    props: {
      type: {
        type: String,
        default: 'asker'
      },
      message: {
        type: String,
        default: 'hello! 你好，我是岁月如同马匹！'
      }
    }
  }
</script>

<style scoped lang="scss">
  .message-content{
    display: block;
    overflow: auto;
    margin: 20px 0;
    img{
      width: 40px;
      height: 40px;
    }
    .message{
      max-width: 60%;
      min-height: 20px;
      line-height: 20px;
      position: relative;
      word-wrap: break-word;
      word-break: break-all;
      padding: 9px 13px;
      font-size: 14px;
      border-radius: 2px;
    }
    .asker{
      overflow: auto;
      float: right;
      .message{
        float: right;
        background-color: #BCDF8C;
        margin-right: 10px;
        &:after{
          position: absolute;
          content: "";
          right: -8px;
          top: 10px;
          width: 0;
          height: 0;
          border-style: solid;
          border-width: 5px 0 5px 8px;
          border-color: transparent transparent transparent #BCDF8C;
        }
      }
      img{
        float: right;
      }
    }
    .answer{
      overflow: auto;
      float: left;
      .message{
        float: left;
        background-color: #FFFFFF;
        margin-left: 10px;
        &:after{
          position: absolute;
          content: "";
          left: -8px;
          top: 10px;
          width: 0;
          height: 0;
          border-style: solid;
          border-width: 5px 8px 5px 0;
          border-color: transparent #FFFFFF transparent transparent;
        }
      }
      img{
        float: left;
      }
    }
  }
</style>
