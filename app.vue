<template>
  <div>
    <transition name="fade" appear>
      <div class="notification" v-show="showalert" :class="classesObj">
        <div class="notification__close" @click="showalert = !showalert">&times;</div>
        <div class="notification__head">{{head}}</div>
        <div class="notification__meta">{{meta}}</div>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: "noti",
  props: {
    showalert: Boolean,
    type: String,
    fixed: Boolean,
    duration: Number,
    heading: String,
    msg: String
  },
  data() {
    return {
      types: ["success", "info", "warning", "danger"],
      head: this.heading ? this.heading : "Success",
      meta: this.msg ? this.msg : "Yay! You made it.",
      sticky: this.fixed ? this.fixed : false
    };
  },
  computed: {
    classesObj: function() {
      return {
        fixed: this.sticky,
        info: this.type === "info",
        warning: this.type === "warning",
        danger: this.type === "danger",
        success : this.type === undefined || this.type === "success"
      };
    }
  }
};
</script>

<style>
.notification {
  display: grid;
  grid-template-rows: 1fr 1fr;
  grid-gap: 5px;
  background-color: #f1f1f1;
  min-width: 300px;
  width: 300px;
  max-width: auto;
  height: auto;
  color: #555;
  padding: 10px 15px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
  border-radius: 2px;
  margin: 6px;
  position: relative;
}

.notification__close {
  position: absolute;
  top: 0;
  right: 10px;
  cursor: pointer;
  font-size: 25px;
  color: #fff;
}

.fixed {
  position: fixed;
  bottom: 0;
  left: 50%;
  transform: translate(-50%, -50%);
}

.notification__head {
  padding: 5px 0;
  font-weight: 500;
  text-transform: capitalize;
  letter-spacing: 0.5px;
  font-size: 20px;
}

.notification__meta {
  padding: 0 0 5px;
  font-weight: 400;
  font-size: 17px;
}

.success {
  background-color: #28a745;
  color: #fff;
}

.danger {
  background-color: #dc3545;
  color: #fff;
}

.warning {
  background-color: #ffc107;
  color: brown;
}

.info {
  background-color: #007bff;
  color: #fff;
}

.fade-enter {
  opacity: 0;
}

.fade-enter-active {
  transition: all 0.5s ease-in;
}

.fade-leave-active {
  transition: all 0.5s ease-out;
  opacity: 0;
}
</style>

