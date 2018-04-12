# vue-luck-draw

> �����ֻ��˵Ĵ�ת�̳齱

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```
> ����
```
������ķ�ʽ���롣
����ָ����Ʒͨ����̨����,����������OnRotate()
�ӷ�������ȡ�û���ʵ�Ļ���Ϣ����Ӧ�Ļ���ţ�
<template>
  <div id="app">
    <v-luck-draw :rewardNames="rewardNames" @OnClick="OnLuck" ref="luckDraw"></v-luck-draw>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      rewardNames: ["mp3", "iphone8", "лл����", "iphoneX", "ipad mini4"]
    };
  },
  mounted() {},
  methods: {
    //�����ת��ť��,��������صĳ��еĽ�Ʒ����
    OnLuck(data) {
      alert(data);
    }
  },
  components: {
    //���Լ�������Ҳ���Բ����첽����
    //�첽�������
    "v-luck-draw": () => import("./components/luck-draw/luck-draw.vue")
  }
};
</script>

<style>

</style>
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
