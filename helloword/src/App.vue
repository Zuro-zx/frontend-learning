<script setup>
// 删掉切换逻辑，全部内容直接展示
</script>

<template>
  <div class="page">
    <div class="card">
      <!-- 代码生成头像，内置文字“张” -->
      <div class="avatar">
        <span class="avatar-text">张</span>
      </div>

      <h2 class="name">张世杰</h2>
      <p class="job">前端开发 / Vue 爱好者</p>
      <p class="intro">热爱编程，专注于简洁优雅的页面实现。</p>

      <!-- 导航文字（仅展示，不可点击） -->
      <div class="nav">
        <span class="nav-item active">关于我</span>
        <span class="nav-item">技能</span>
        <span class="nav-item">项目</span>
        <span class="nav-item">联系</span>
      </div>

      <!-- 全部板块直接显示在一页 -->
      <div class="section">
        <h3 class="section-title">关于我</h3>
        <p class="section-text">
          一名 Web 开发学习者，熟悉 Vue、JavaScript、HTML、CSS 和前端基础开发流程。喜欢简洁的界面设计，也在持续学习新技术。
        </p>
      </div>

      <div class="section">
        <h3 class="section-title">技能清单</h3>
        <div class="skill-list">
          <span class="skill-tag">Vue3</span>
          <span class="skill-tag">JavaScript</span>
          <span class="skill-tag">HTML / CSS</span>
          <span class="skill-tag">TypeScript</span>
          <span class="skill-tag">Element Plus</span>
          <span class="skill-tag">Git</span>
        </div>
      </div>

      <div class="section">
        <h3 class="section-title">项目作品</h3>
        <div class="project-card">
          <h4>图书管理系统</h4>
          <p>基于 Vue3 + Element Plus 开发的后台管理平台。</p>
        </div>
      </div>

      <div class="section">
        <h3 class="section-title">联系方式</h3>
        <p class="section-text">邮箱：zhangshijie@example.com</p>
        <p class="section-text">欢迎交流学习。</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.page {
  min-height: 100vh;
  background: radial-gradient(circle at top left, rgba(30, 58, 138, 0.45), transparent 35%), linear-gradient(180deg, #0a0f1a 0%, #05070a 100%);
  display: flex;
  justify-content: center;
  align-items: flex-start;
  padding: 18px;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
}

.card {
  width: 100%;
  max-width: 390px;
  background: rgba(18, 24, 42, 0.88);
  border: 1px solid rgba(255, 255, 255, 0.06);
  border-radius: 22px;
  padding: 30px 24px 24px;
  box-shadow: 0 0 18px rgba(0, 0, 0, 0.35), inset 0 0 0 1px rgba(255, 255, 255, 0.02);
  backdrop-filter: blur(10px);
}

/* 代码绘制圆形头像，带文字 */
.avatar {
  width: 84px;
  height: 84px;
  margin: 0 auto 18px;
  border-radius: 50%;
  background: linear-gradient(135deg, #4facfe 0%, #00f2fe 50%, #2563eb 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 0 0 3px rgba(255, 255, 255, 0.08), 0 8px 20px rgba(0, 0, 0, 0.45);
}
.avatar-text {
  width: 72px;
  height: 72px;
  border-radius: 50%;
  background-color: #0f172a;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #38bdf8;
  font-size: 34px;
  font-weight: bold;
}

.name {
  margin: 0 0 4px;
  color: #ffffff;
  font-size: 21px;
  font-weight: 600;
  text-align: center;
  letter-spacing: 0.5px;
}

.job {
  margin: 0 0 8px;
  color: #7dd3fc;
  font-size: 13px;
  text-align: center;
  letter-spacing: 1px;
}

.intro {
  margin: 0 0 26px;
  color: #94a3b8;
  font-size: 13px;
  text-align: center;
  line-height: 1.5;
}

.nav {
  display: flex;
  justify-content: center;
  gap: 18px;
  margin-bottom: 28px;
  padding-bottom: 12px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.06);
}
.nav-item {
  font-size: 13px;
  color: #64748b;
}
.nav-item.active {
  color: #ffffff;
}

.section {
  margin-bottom: 28px;
}

.section-title {
  margin: 0 0 12px;
  color: #e2e8f0;
  font-size: 16px;
  font-weight: 600;
  display: flex;
  align-items: center;
  gap: 8px;
}
.section-title::before {
  content: "";
  width: 3px;
  height: 16px;
  border-radius: 2px;
  background: linear-gradient(180deg, #38bdf8, #2563eb);
}

.section-text {
  margin: 0;
  color: #94a3b8;
  font-size: 14px;
  line-height: 1.7;
}

.skill-list {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}
.skill-tag {
  background: rgba(255, 255, 255, 0.04);
  border: 1px solid rgba(255, 255, 255, 0.08);
  color: #38bdf8;
  font-size: 13px;
  padding: 6px 12px;
  border-radius: 999px;
}

.project-card {
  background: rgba(255, 255, 255, 0.04);
  border: 1px solid rgba(255, 255, 255, 0.06);
  border-radius: 14px;
  padding: 16px;
}
.project-card h4 {
  margin: 0 0 6px;
  color: #e2e8f0;
  font-size: 15px;
  font-weight: 600;
}
.project-card p {
  margin: 0;
  color: #94a3b8;
  font-size: 13px;
  line-height: 1.6;
}
</style>