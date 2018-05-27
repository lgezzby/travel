<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li
        class="item"
        v-for="item of recommendList"
        :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" />
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=2494659386,2426237724&fm=58',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      }, {
        id: '0002',
        imgUrl: 'https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=2494659386,2426237724&fm=58',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      }, {
        id: '0003',
        imgUrl: 'https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=2494659386,2426237724&fm=58',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      }, {
        id: '0004',
        imgUrl: 'https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=2494659386,2426237724&fm=58',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    line-height: .8rem;
    background: #EEE;
    text-indent: .2rem;
    margin-top: .2rem;
  .item-img-wrapper
    overflow: hidden;
    height: 0;
    padding-bottom: 33.9%;
    .item-img
      width: 100%;
  .item-info
    padding: .1rem;
    .item-title
      line-height: .54rem;
      font-size: .32rem;
      ellipsis()
    .item-desc
      line-height: .4rem;
      color:#999;
      ellipsis()
</style>
