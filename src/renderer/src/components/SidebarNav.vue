<template>
  <nav class="sidebar-nav" :aria-label="$t('app.title')">
    <!-- 默认清单是唯一入口，其余分类与工具入口已隐藏 -->
    <div class="nav-main-content">
      <div class="nav-section">
        <ListSidebar />
      </div>
    </div>

    <!-- 底部按钮区 -->
    <div class="nav-section-bottom nav-icon-buttons">
      <IconButton class="nav-icon-btn h-10 w-10" :label="$t('settings.title')" @click="openSettings">
        <Settings class="h-icon-lg w-icon-lg" />
      </IconButton>
    </div>
  </nav>
</template>

<script setup>
import { Settings } from '@lucide/vue'
import ListSidebar from './ListSidebar.vue'
import IconButton from './ui/button/IconButton.vue'

const emit = defineEmits(['open-settings'])

const openSettings = () => {
  emit('open-settings')
}
</script>

<style scoped>
@import '@/assets/styles/components/sidebar-nav.css';
</style>
