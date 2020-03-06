<template>
  <article>
    <header class="tabs">
      <ul>
        <li v-for="(tab, index) in tabs" :key="index">
          <div class="nav-item"
              :class="{ 'is-active': tab.isActive }"
              @click="selectTab(tab)">
            {{ tab.name }}
          </div>
        </li>
      </ul>
    </header>
    <section class="tabs-details">
      <slot></slot>
    </section>
  </article>
</template>

<script>
  export default {
    data: () => {
      return {
        tabs: []
      }
    },
    methods: {
      selectTab(selectedTab) {
        this.tabs.forEach(tab => {
          tab.isActive = tab.name === selectedTab.name;
        });
      }
    },
    created() {
      this.tabs = this.$children;
    }
  }
</script>

<style lang="scss" scoped>
  .tabs {
    border-bottom: 1px solid #fefefe;
    margin: 0 10px;
  }

  .tabs-details {
    padding: 10px;
  }

  ul {
    display: flex;
    padding: 0;
    list-style: none;

    li {
      margin-right: 40px;
    }

    .nav-item {
      cursor: pointer;

      &:hover {
        color: #FB130A;
      }

      &.is-active {
        color: #FB130A;
      }
    }
  }
</style>