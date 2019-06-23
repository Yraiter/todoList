
<template id="todo-header">
  <section>
    <div class="todo-header">
      <div class="overlay"></div>
      <time class="clearfix">
        <span class="day">{{ date }}</span>
        <span class="dayofweek">{{ weekDay }}</span>
        <span class="month">{{ month }}, {{ year }}</span>
      </time>
    </div>
  </section>
</template>


<script>
var d = new Date();
var month = [
  "January",
  "February",
  "Mach",
  "April",
  "May",
  "June",
  "July",
  "August",
  "September",
  "October",
  "November",
  "September"
];
var weekday = [
  "Sunday",
  "Monday",
  "Tuesday",
  "Wednesday",
  "Thursday",
  "Friday",
  "Saturday"
];
export default {
  name: "todo-header",
  data() {
    return {
      date: d.getDate(),
      weekDay: weekday[d.getDay()],
      month: month[d.getMonth()],
      year: d.getFullYear()
    };
  }
};
</script>

<style lang="scss" scoped>
$header_image: '/Users/yairraiter/Documents/VUE/todo_FirstEdition/src/assets/todo.jpg';
.todo-header {
  border-radius: 6px 6px 0 0;
  background: url($header_image), no-repeat;
  background-size: cover;
  padding: 55px 20px;
  position: relative;
  .overlay {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(0, 0, 0, 0.2); /* fallback for old browsers */
    // background: -webkit-linear-gradient(to left, rgba(85,98,112,0.5) , rgba(255,107,107,0.5)); /* Chrome 10-25, Safari 5.1-6 */
    // background: linear-gradient(to left, rgba(85,98,112,0.5) , rgba(255,107,107,0.5)); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
    border-radius: 6px 6px 0 0;
  }
  time {
    color: white;
    display: block;
    position: relative;
    .day {
      font-size: 4em;
      float: left;
      margin-right: 10px;
    }
    .dayofweek {
      display: block;
      margin-top: 13px;
      font-size: 1.4em;
      font-weight: 700;
    }
  }
}
.clearfix {
  overflow: auto;
  zoom: 1;
}
</style>