<template>
  <div class="appeal-detail">
    <header class="page-header">
      <span class="btn-left" @click="$router.go(-1)">
        <svg-icon icon-class="white-btn"></svg-icon>
      </span>
      <div class="header-content">申诉详情</div>
      <router-link class="appeal-record" to="/order/appealRecord" tag="span">申诉记录</router-link>
    </header>
    <section class="order-card">
      <ul class="order-list">
        <li class="order-item">
          <div class="store-info">
            <img src="../../assets/image/product/store-headerM.png" class="header-img" />
            <span>店铺名称</span>
          </div>
        </li>
        <li class="order-info">
          <img src alt />
          <div class="order-detail">
            <p class="info-one">
              <span>娜扎新装LOOK</span>
              <i>￥222</i>
            </p>
            <p class="info-two">
              <span>型号;规格;颜色;</span>
              <span>×2</span>
            </p>
          </div>
        </li>
        <li class="order-count">
          <span>共2件商品,小计:</span>
          <i>￥444</i>
        </li>
      </ul>
    </section>
    <section class="info-form">
      <van-cell-group>
        <van-field v-model="username" disabled label="用户名" />
        <van-field v-model="phone" disabled label="手机号" />
        <van-field v-model="time" disabled label="申诉时间" />
        <van-field
          v-model="content"
          :autosize="{ minHeight: 150 }"
          type="textarea"
          label="申诉内容"
          disabled
        />
      </van-cell-group>
      <ul class="imgs-list">
        <li class="img-item">
          <img src="../../assets/image/home/test1.png" class="header-img" />
        </li>
        <li class="img-item">
          <img src="../../assets/image/home/test1.png" class="header-img" />
        </li>
        <li class="img-item">
          <img src="../../assets/image/home/test1.png" class="header-img" />
        </li>
      </ul>
    </section>
    <div class="pay-btn">
      <van-button type="danger" @click="handlePay" size="large">补充申诉信息</van-button>
    </div>
  </div>
</template>

<script>
export default {
  name: "",
  data() {
    return {
      username: "某某人",
      phone: "13548669666",
      time: "2019-06-06 16:24:30",
      content: `今天下午，放了学，哥哥今天没上班，我们一起去逛鞋店，我喜欢上了一个帆布鞋，黑色的，89元，哥哥非常疼我，给我买下了这双鞋子。哥哥也要买鞋，他买了一个白鞋，74元，比我的便宜。因为爸爸妈妈今天加班，所以我们只能吃泡面，不过泡面也很好吃。`
    };
  },
  created() {},
  methods: {}
};
</script>

<style scoped lang="scss">
.appeal-detail {
  padding: 0 16px;
  .page-header {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    padding: 10px;
    .header-content {
      text-align: center;
      font-size: 18px;
      font-weight: 600;
      color: #3a3a3a;
      flex: 1;
    }
    .appeal-record {
      color: #d8182d;
      font-size: 13px;
    }
  }
  .order-card {
    background-color: #fff;
    border-radius: 5px;
    padding: 10px 20px;
    margin-top: 20px;
    .order-list {
      .order-item {
        display: flex;
        justify-content: space-between;
        & > span {
          color: #d8182d;
          font-size: 11px;
        }
        .store-info {
          display: flex;
          justify-content: flex-start;
          align-items: center;
          font-size: 10px;
          .header-img {
            width: 24px;
            height: 24px;
          }
          span {
            color: #3a3a3a;
            padding-left: 3px;
            font-size: 11px;
          }
        }
      }
      .order-info {
        padding-top: 10px;
        display: flex;
        justify-content: space-between;
        img {
          width: 80px;
          height: 80px;
          display: inline-block;
          background-color: #d8182d;
          border-radius: 4px;
        }
        .order-detail {
          flex: 1;
          padding-left: 16px;
          padding-bottom: 4px;
          .info-one,
          .info-two {
            display: flex;
            justify-content: space-between;
            font-size: 11px;
          }
          .info-one {
            color: #3a3a3a;
            padding-bottom: 5px;
            i {
              font-weight: 700;
            }
          }
          .info-two {
            color: #949497;
          }
        }
      }
      .order-count {
        display: flex;
        justify-content: flex-end;
        font-size: 13px;
        i {
          color: #d8182d;
          padding-left: 5px;
          font-weight: 700;
        }
        span {
          color: #3a3a3a;
        }
      }
    }
  }
  .info-form {
    padding: 20px;
    margin-top: 20px;
    border-radius: 5px;
    background-color: #fff;
    ::v-deep .van-cell {
      padding-left: 0;
      padding-right: 0;
    }
    ::v-deep .van-field__control:disabled {
      color: #3a3a3a;
      font-size: 13px;
    }
    ::v-deep .van-image img {
      border-radius: 8px;
    }
  }
  .pay-btn {
    width: 100%;
    padding: 0 16px;
    padding-top: 50px;
    padding-bottom: 10px;
    ::v-deep .van-button--danger {
      background-color: #d8182d;
      line-height: 44px;
      font-size: 18px;
    }
  }
  .imgs-list {
    display: flex;
    .img-item {
      img {
        display: inline-block;
        width: 94px;
        height: 94px;
        border-radius: 5px;
        padding-right: 10px;
      }
    }
  }
}
</style>
