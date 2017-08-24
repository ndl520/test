<template>
  <div class="hello">
    <div class="head">
      <div class="bao">
        <div class="logo">
          <img src="../img/logo.png"><a>乐游</a>
        </div>
        <div class="input"><input><img src="../img/sousuo2.png"></div>
        <div class="login">
          <img src="../img/login.png">
        </div>
      </div>
    </div>
    <div class="swipe">
      <mt-swipe :auto="4000">
        <mt-swipe-item>
          <router-link to="/two">
            <img src="../img/lunbo1.jpg">
          </router-link>
        </mt-swipe-item>
        <mt-swipe-item>
          <router-link to="/two">
            <img src="../img/lunbo2.jpg">
          </router-link>
        </mt-swipe-item>
        <mt-swipe-item>
          <router-link to="/two">
            <img src="../img/lunbo3.jpg">
          </router-link>
        </mt-swipe-item>
      </mt-swipe>
    </div>
    <div class="jieshao">
      <router-link to="">
        <div class="d1">
          <img src="../img/chongzhi2.png">
          <p>充值</p>
        </div>
      </router-link>
      <router-link to="">
        <div class="d1">
          <img src="../img/naozhong.png">
          <p>开测</p>
        </div>
      </router-link>
      <router-link to="">
        <div class="d1">
          <img src="../img/kaifu.png">
          <p>开服</p>
        </div>
      </router-link>
      <router-link to="">
        <div class="d1">
          <img src="../img/libao.png">
          <p>礼包</p>
        </div>
      </router-link>
    </div>
    <div class="jieshao" style="border-bottom: 3px solid #ccc;padding-bottom: 10px">
      <router-link to="">
        <div class="d1">
          <img src="../img/new.png">
          <p>新游</p>
        </div>
      </router-link>
      <router-link to="">
        <div class="d1">
          <img src="../img/fenlei.png">
          <p>分类</p>
        </div>
      </router-link>
      <router-link to="">
        <div class="d1">
          <img src="../img/bt.png">
          <p>BT</p>
        </div>
      </router-link>
      <router-link to="">
        <div class="d1">
          <img src="../img/pojie.png">
          <p>破解</p>
        </div>
      </router-link>
    </div>
    <div class="content">
      <h1>--- <i class="iconfont">&#xe69b;</i>{{mulu}} ---</h1>
      <div class="content-nei" v-for="item in items">
        <div class="imgs">
          <img :src="item.imgUrl">
        </div>
        <div class="zhi">
          <h2>{{item.zhi}}</h2>
          <span>开始</span>
          <p>{{item.jie}}</p>
        </div>
      </div>
    </div>
    <div class="bigimg" v-for="gg in ggs">
      <img :src="gg.url">
    </div>
    <div class="content">
      <h1>--- <i class="iconfont">&#xe619;</i>{{mulu2}} ---</h1>
      <div class="content-nei" v-for="item2 in items2">
        <div class="imgs">
          <img :src="item2.imgUrl">
        </div>
        <div class="zhi">
          <h2>{{item2.zhi}}</h2>
          <a class="tubiao"><i class="iconfont iconfont-size">&#xe6bf;</i></a>
          <p>{{item2.jie}}</p>
        </div>
      </div>
    </div>
    <div class="foot">
      <img src="../img/logo.png">
      <p><i>用心创造快乐!</i></p>
      <p>Copyright © 2004-2017 <a>LeYouGame</a>. All Rights Reserved.</p>
      <p>乐游公司 版权所有</p>
    </div>
    <div class="tabbar">
      <mt-tabbar fixed v-model="selected">
        <mt-tab-item id="网游">
          <img slot="icon" src="../img/wangyou.png">
          网游
        </mt-tab-item>
        <mt-tab-item id="单机">
          <img slot="icon" src="../img/danji.png">
          单机
        </mt-tab-item>
        <mt-tab-item id="热门">
          <img slot="icon" src="../img/remen.png">
          热门
        </mt-tab-item>
        <mt-tab-item id="更多游戏">
          <img slot="icon" src="../img/gengduo.png">
          更多游戏
        </mt-tab-item>
      </mt-tabbar>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'hello',
    data () {
      return {
        selected: '外卖',
        mulu: '安卓推荐游戏',
        mulu2: 'IOS推荐游戏',
        ggs: [
          {url: 'http://img.d.cn/be/image/1702/gr3prizje5psf.jpg'}
        ],
        items: [
          {
            imgUrl: 'http://img.d.cn/be/image/1610/3v3peiutmm3u2.png',
            zhi: '传奇世界',
            jie: '盛大正版授权，重拾经典传奇，燃烧吧，我的青春！！！'
          },
          {
            imgUrl: 'http://img.d.cn/be/image/1701/gu3piiyd3x0n6.jpg',
            zhi: '决战沙城',
            jie: '传奇世界正版授权，全民抢boss'
          },
          {
            imgUrl: 'http://img.d.cn/be/image/1610/783pciuxgn921.png',
            zhi: '联盟与部落',
            jie: '经典魔兽题材，为了联盟，为了部落'
          },
          {
            imgUrl: 'http://img.d.cn/be/image/1702/4n3pviyzlg3t2.png',
            zhi: '大圣外传',
            jie: '会变身的手游，大圣带你72变'
          },
          {
            imgUrl: 'http://img.d.cn/be/image/1612/133pyiwfqkkbc.png',
            zhi: '绝世神功',
            jie: '老司机带你修仙带你飞'
          },
          {
            imgUrl: 'http://img.d.cn/be/image/1610/7d3priuxh2v3m.png',
            zhi: '小小地下城',
            jie: '小镇地下城中，到底有什么秘密？'
          },
          {
            imgUrl: 'http://img.d.cn/be/image/1703/pp3pvj03myerp.png',
            zhi: '超人守卫2',
            jie: '首款Q版史诗级塔防策略游戏'
          },
          {
            imgUrl: 'http://img.d.cn/be/image/1702/4x3p8iyzmmz5n.png',
            zhi: '烈焰遮天',
            jie: '高度还原老传奇的RPG挂机手游'
          },
          {
            imgUrl: 'http://img.d.cn/be/image/1611/hu3plivn7t2it.png',
            zhi: '点兵三国志',
            jie: '点千军万马，成三国霸业'
          },
          {
            imgUrl: 'http://img.d.cn/be/image/1702/503p0iyzmtq4h.png',
            zhi: '修仙外传',
            jie: '老司机带你修仙带你飞'
          }
        ],
        items2: [
          {
            imgUrl: 'http://img.d.cn/be/image/1610/hm3pwiu6q6v6m.png',
            zhi: '放开那三国',
            jie: '新派卡牌，让我先来。最精美搞笑呆萌三国卡牌手游绚丽来袭！！！'
          },
          {
            imgUrl: 'http://img.d.cn/be/image/1504/bd2d1i8zhhibv.png',
            zhi: '卧虎藏龙',
            jie: '卧虎藏龙，武者无疆'
          },
          {
            imgUrl: 'http://img.d.cn/be/image/1610/hr3pdiu6ssgzp.jpg',
            zhi: '神雕侠侣',
            jie: '相思相见知何日？此时此夜难为情！'
          },
          {
            imgUrl: 'http://img.d.cn/be/image/1610/hs3p2iu6svvgh.png',
            zhi: '魔力宝贝',
            jie: '重续经典，萌气好玩的端游移植'
          },
          {
            imgUrl: 'http://img.d.cn/be/image/1610/ht3pbiu6sza45.png',
            zhi: '天使舰队',
            jie: '火辣天使邀你共同海战'
          },
          {
            imgUrl: 'http://img.d.cn/be/image/1610/j03paiu7pltzl.png',
            zhi: '新苍穹之剑',
            jie: '全球首款真3D动作手机网游'
          },
          {
            imgUrl: 'http://img.d.cn/be/image/1610/j13phiu7ppegq.png',
            zhi: '暗黑荣耀',
            jie: '完美世界推出的暗黑风动作RPG，感受火爆战斗'
          },
          {
            imgUrl: 'http://img.d.cn/be/image/1610/k13p3iu7qp0vi.png',
            zhi: '熊猫战记',
            jie: '五大职业，多线养成，爽快动作，拳拳到肉'
          }
        ]
      }
    },
    watch: {
      selected: function (val, oldVal) {
        // 这里就可以通过 val 的值变更来确定
        console.log(val)
        if (val === '单机') {
          alert('haha')
        }
      }
    }
  }
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .content-nei {
    position: relative;
    overflow: hidden;
    padding: .2rem .4rem;
    border-bottom: .01rem solid #EBEBEB;
  }

  .bigimg {
    width: 100%;

  }

  .bigimg img {
    width: 100%;
  }

  .tubiao {
    position: absolute;
    right: 0;
    top: 0.2rem;
    color: #ff6600;
    /*margin-top: -0.5rem;*/
    font-size: 14px;
    padding: .1rem .4rem;
    font-family: 微软雅黑;
  }

  .imgs {
    display: inline;
    float: left;
    width: 1rem;
    height: 1rem;
  }

  .imgs img {
    border-radius: .1rem;
    width: 100%;
    height: 100%;
  }

  .logo {
    color: white;
    font-size: .3rem;
    font-family: 黑体;
    height: 100%;
  }

  h1 {
    font-family: 黑体;
    color: #f60;
    text-align: center;
    font-size: 16px;
  }

  .iconfont {
    font-family: "iconfont" !important;
    font-style: normal;
    -webkit-font-smoothing: antialiased;
    -webkit-text-stroke-width: 0.2px;
    -moz-osx-font-smoothing: grayscale;
  }

  .iconfont-size {
    font-size: 43px;
  }

  .bao {
    display: flex;
    justify-content: space-between;
    width: 100%;
    height: 100%;
  }

  .zhi {
    width: 79%;
    display: inline;
    float: left;
    margin-left: .3rem;
  }

  .zhi span {
    position: absolute;
    right: .4rem;
    background-color: orangered;
    color: white;
    top: .3rem;
    /*margin-top: -0.5rem;*/
    font-size: 14px;
    padding: .1rem .4rem;
    font-family: 微软雅黑;
    border-radius: 2.5rem;
  }

  h2 {
    padding: .15rem 0;
    font-size: 16px;
    color: #333;
    font-weight: normal;
    font-family: 微软雅黑;
  }

  .zhi p {
    width: 100%;
    white-space: nowrap;
    padding-right: 60px;
    text-overflow: ellipsis;
    overflow: hidden;
    clear: both;
    color: #999;
    font-size: 13px;
  }

  .logo a {
    vertical-align: .12rem;
  }

  .logo img {
    height: .5rem;
  }

  .foot {
    padding: .2rem;
    text-align: center;
    margin-bottom: 55px;
    background-color: #222222;
  }

  .foot a {
    cursor: pointer;
    color: orangered;
  }

  .foot img {
    width: 10%;

  }

  .foot p {
    padding: .1rem;
    font-family: 微软雅黑;
    font-size: 12px;
    color: #858585;
  }

  .foot p:nth-child(2) {
    padding: .1rem;
    font-family: 黑体;
    font-size: 12px;
    color: #858585;
  }

  .login {
    width: .6rem;
    height: .6rem;
  }

  .login img {
    width: 100%;
    height: 100%;
  }

  .content {
    width: 100%;
    margin-top: .5rem;
  }

  .head {
    padding: 0.1rem 0.1rem;
    background-color: darkorange;
  }

  .input input {
    display: inline-block;
    font-size: 20px;
    vertical-align: 1.12rem;
    height: 97%;
    width: 80%;
    border: none;
    outline: none;
  }

  .input {
    text-align: center;
    height: 0.6rem;
    width: 65%;
    border-radius: .3rem;
    background-color: white;
  }

  .input img {
    vertical-align: 1.02rem;
    width: .4rem;
    /*margin-top: -2rem;*/
    height: .4rem;
  }

  .swipe {
    width: 100%;
    height: 4rem;
  }

  .jieshao {
    padding: 0 .2rem;
    margin-top: .2rem;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
  }

  .jieshao p {
    font-size: 20px;
    font-family: 楷体;
    margin: 0;
    color: black;
  }

  .tabbar a {
    font-size: 20px;
    font-family: 微软雅黑;
    font-weight: 500;
  }

  .d1 {
    margin: .12rem .12rem;
    text-align: center;
    width: 1rem;
  }

  .d1 img {
    width: 80%;
    height: 80%;
  }

  .d1 a {
    color: white;
    font-family: 黑体;
    font-size: 20px;
  }

  h1, h2 {
    font-weight: normal;
  }

  .swipe img {
    width: 100%;
    height: 100%;
  }

  a {
    text-decoration: none;
  }
</style>
