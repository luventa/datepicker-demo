<template>
  <div id="app" class="is-parent" style="width: 30rem; margin:auto; margin-top: 2rem;">
    <div class="box is-child">
      <p>Selected date: {{date}}</p>
      <datepicker v-model="date" :config="{ dateFormat: 'd-m-Y' }"></datepicker>
      <button @click.prevent="setNewDate">Set date</button>
    </div>
    <div class="box is-child">
      <p>Range</p>
      <datepicker v-model="dateRange" :config="{ mode: 'range' }"></datepicker>
    </div>
    <div class="box is-child">
      <p>Min and max</p>
      <datepicker v-model="dateMaxMin" :config="{ dateFormat:'d.m.Y', minDate: '1.6.2017', maxDate: '25.6.2017' }"></datepicker>
    </div>
    <div class="box is-child">
      <p>Enable time : {{dateTime}}</p>
      <datepicker v-model="dateTime" :config="{ enableTime: true, dateFormat: 'Y-m-d h:i K' }"></datepicker>
    </div>
    <div class="box is-child">
      <p>Multiple</p>
      <datepicker v-model="dateMultiple" :config="{ dateFormat:'d.m.Y', mode: 'multiple' }"></datepicker>
    </div>
    <div class="box is-child">
      <p>Localization</p>
      <datepicker :config="{ locale: l10n }"></datepicker>
    </div>
    <div class="box is-child">
      <p>Wrap</p>
      <datepicker :alignment="'left'" :config="{ wrap: true }">
        <a class="button" data-toggle>Select</a>
        <a class="button" data-clear>Clear</a>
      </datepicker>
    </div>
  </div>
</template>

<script>
import Datepicker from 'vue-bulma-datepicker'

export default {
  name: 'app',
  data () {
    return {
      date: '01-01-2018',
      dateRange: '2017-01-01 to 2018-01-01',
      dateTime: null,
      dateMaxMin: '23.06.2017',
      dateMultiple: null,
      l10n: {
        firstDayOfWeek: 1,
        weekdays: {
          shorthand: ['周日', '周一', '周二', '周三', '周四', '周五', '周六'],
          longhand: ['星期日', '星期一', '星期二', '星期三', '星期四', '星期五', '星期六']
        },
        months: {
          shorthand: ['一月', '二月', '三月', '四月', '五月', '六月', '七月', '八月', '九月', '十月', '十一月', '十二月'],
          longhand: ['一月', '二月', '三月', '四月', '五月', '六月', '七月', '八月', '九月', '十月', '十一月', '十二月']
        }
      }
    }
  },
  methods: {
    setNewDate () {
      this.date = '12-01-2017'
    }
  },
  components: {
    Datepicker
  }
}
</script>

<style lang="scss">
@import '~bulma';

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
