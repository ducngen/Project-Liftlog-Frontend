<script setup>
import TrainingSetList from './components/TrainingSetList.vue'
</script>

<template>
  <header class="app-header">
    <h1>Liftlog</h1>
    <p>Dokumentiere dein Krafttraining und behalte deinen Fortschritt im Blick.</p>
  </header>

  <main class="content">
    <section class="intro-card">
      <h2>Willkommen bei Liftlog</h2>
      <p>
        Liftlog ist eine Webanwendung zur Erfassung und späteren Auswertung
        von Krafttrainings-Sätzen.
      </p>
    </section>

    <TrainingSetList />
  </main>
</template>

<style>
:root {
  font-family: Arial, Helvetica, sans-serif;
  color: #1f2937;
  background: #f3f4f6;
}

* {
  box-sizing: border-box;
}

body {
  margin: 0;
}

.app-header {
  padding: 3rem 1.25rem;
  text-align: center;
  color: white;
  background: #111827;
}

.app-header h1 {
  margin: 0;
  font-size: 2.5rem;
}

.app-header p {
  max-width: 620px;
  margin: 0.75rem auto 0;
  line-height: 1.5;
}

.content {
  max-width: 1100px;
  margin: 0 auto;
  padding: 2rem 1rem;
}

.intro-card {
  padding: 1.5rem;
  border-radius: 12px;
  background: white;
  box-shadow: 0 4px 12px rgb(0 0 0 / 8%);
}

.intro-card h2 {
  margin-top: 0;
}
</style>