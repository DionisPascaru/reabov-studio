<template>
  <div class="dropdown">
      <span class="dropdown-text">what you get</span>
      <ul class="dropdown-list" :class="{ active: this.isActive }" :style="[this.isActive ? {'height': height + 'px' } : {'height': '0'}]" >
        <li v-for="(item, index) in items" :key="index" >{{item}}</li>
      </ul>
      <span class="el-dropdown-link" @click="toggle">
        <i class="el-icon-arrow-down" :class="{ active: this.isActive }"></i>
      </span>
    </div>
</template>

<script>
export default {
  name: 'DropdownComponent',
  props: ['items', 'height'],
  data() {
    return {
      isActive: false,
    }
  },
  methods: {
    toggle() {
      this.isActive = !this.isActive
    }
  }
}
</script>