<template>
  <h1 @click="increase">
    {{ count }}
  </h1>

  <div v-if="count > 4">
    4보다 큽니다!
  </div>

  <ul>
    <Fruit
      v-for="fruit in fruits"
      :key="fruit"
      :name="fruit">
      {{ fruit }}
    </Fruit>
  </ul>
</template>

<script>
import Fruit from '~/components/Fruit'

export default {
  components: {
    Fruit // Fruit: Fruit - 속성의 이름과 데이터의 이름이 같은 경우 생략 가능
  },
  data() { // data를 갱신하면 화면도 바뀌는 것 : 반응성(Reactivity)
    return {
      count: 0, // count 0으로 초기화
      fruits: ['Apple', 'Banana', 'Cherry']
    }
  },
  methods: {
    increase() {
      this.count += 1 //this를 이용해서 count를 참조해서 가져올수 있도록 함
    }
  }
}
</script>

<style lang="scss">
  h1 {
    font-size: 50px;
    color: royalblue;
  }
  ul {
    li {
      font-size: 40px;
    }
  }
</style>