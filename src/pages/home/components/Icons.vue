<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.img"/>
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [{
        id: '0001',
        img: 'https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=2494659386,2426237724&fm=58',
        desc: '景点门票'
      }, {
        id: '0002',
        img: 'https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=2494659386,2426237724&fm=58',
        desc: '滑雪季节'
      }, {
        id: '0003',
        img: 'https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=2494659386,2426237724&fm=58',
        desc: '泡温泉'
      }, {
        id: '0004',
        img: 'https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=2494659386,2426237724&fm=58',
        desc: '动物园'
      }, {
        id: '0005',
        img: 'https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=2494659386,2426237724&fm=58',
        desc: '植物园'
      }, {
        id: '0006',
        img: 'https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=2494659386,2426237724&fm=58',
        desc: '水族馆'
      }, {
        id: '0007',
        img: 'https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=2494659386,2426237724&fm=58',
        desc: '宾馆'
      }, {
        id: '0008',
        img: 'https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=2494659386,2426237724&fm=58',
        desc: '酒店'
      }, {
        id: '0009',
        img: 'https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=2494659386,2426237724&fm=58',
        desc: '民宿'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/variables.styl'
@import '~styles/mixins.styl'
.icons >>> .swiper-container
  height: 0;
  padding-bottom: 50%;
.icons
  margin-top: .1rem;
  .icon
    position: relative;
    float: left;
    height: 0;
    width: 25%;
    padding-bottom: 25%;
    .icon-img
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: .44rem;
      box-sizing: border-box;
      padding: .1rem;
      .icon-img-content
        display: block;
        margin: 0 auto;
        height: 100%;
    .icon-desc
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      line-height: .44rem;
      height: .44rem;
      text-align: center;
      color: $darkTextColor;
      ellipsis();
</style>
