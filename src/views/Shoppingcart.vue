<template>
  <div style="background-color: white;">
    <van-nav-bar title="购物车" left-arrow />
    <!-- 购物车逻辑部分 -->
    <van-row type="flex" align="center" class="shopShowSet">
      <van-col span="2">
        <van-checkbox v-model="shopChecked"></van-checkbox>
      </van-col>
      <van-col span="22">
        <van-card num="2" price="2.00" desc="描述信息" title="商品标题" thumb="https://img.yzcdn.cn/vant/ipad.jpeg">
          <template #tags>
            <van-tag plain type="danger">标签</van-tag>
            <van-tag plain type="danger">标签</van-tag>
          </template>
          <template #footer>
            <van-stepper v-model="value" input-width="40px" button-size="32px" integer />
          </template>
        </van-card>
      </van-col>
    </van-row>
    <van-row type="flex" align="center" class="shopShowSet">
      <van-col span="2">
        <van-checkbox v-model="shopChecked"></van-checkbox>
      </van-col>
      <van-col span="22">
        <van-card num="2" price="2.00" desc="描述信息" title="商品标题" thumb="https://img.yzcdn.cn/vant/ipad.jpeg">
          <template #tags>
            <van-tag plain type="danger">标签</van-tag>
            <van-tag plain type="danger">标签</van-tag>
          </template>
          <template #footer>
            <van-stepper v-model="value" input-width="40px" button-size="32px" integer />
          </template>
        </van-card>
      </van-col>
    </van-row>
    <!-- 提交数据 -->
    <van-submit-bar class="submitArea" :price="3050" button-text="提交订单" @submit="onSubmit">
      <van-checkbox v-model="shopChecked">全选</van-checkbox>
      <template #tip> 你的收货地址不支持同城送, <span @click="onClickEditAddress">修改地址</span> </template>
    </van-submit-bar>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      value: 1,
      shopChecked: false
    };
  },
  methods: {
    onSubmit() {},
    onClickEditAddress() {}
  }
};
</script>
<style lang="less" scoped>
.submitArea {
  margin-bottom: 1.4rem;
}
.shopShowSet {
  background-color: #fafafa;
}
</style>
