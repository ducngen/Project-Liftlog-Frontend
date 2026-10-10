<script setup>
const trainingSets = [
  {
    id: 1,
    exercise: 'Bankdrücken',
    muscleGroup: 'CHEST',
    weightKg: 60,
    reps: 8,
    performedOn: '2026-10-01',
    volume: 480
  },
  {
    id: 2,
    exercise: 'Kniebeuge',
    muscleGroup: 'LEGS',
    weightKg: 80,
    reps: 5,
    performedOn: '2026-10-02',
    volume: 400
  },
  {
    id: 3,
    exercise: 'Klimmzüge',
    muscleGroup: 'BACK',
    weightKg: 0,
    reps: 10,
    performedOn: '2026-10-03',
    volume: 0
  },
  {
    id: 4,
    exercise: 'Schulterdrücken',
    muscleGroup: 'SHOULDERS',
    weightKg: 30,
    reps: 10,
    performedOn: '2026-10-03',
    volume: 300
  }
]
</script>

<template>
  <section class="training-set-list">
    <h2>Meine Trainingssätze</h2>
    <p class="subtitle">
      Beispielhafte Einträge für das Liftlog-Frontend.
    </p>

    <div class="table-wrapper">
      <table>
        <thead>
          <tr>
            <th>Übung</th>
            <th>Muskelgruppe</th>
            <th>Gewicht</th>
            <th>Wiederholungen</th>
            <th>Datum</th>
            <th>Volumen</th>
          </tr>
        </thead>

        <tbody>
          <tr v-for="trainingSet in trainingSets" :key="trainingSet.id">
            <td>{{ trainingSet.exercise }}</td>
            <td>{{ trainingSet.muscleGroup }}</td>
            <td>{{ trainingSet.weightKg }} kg</td>
            <td>{{ trainingSet.reps }}</td>
            <td>{{ trainingSet.performedOn }}</td>
            <td>{{ trainingSet.volume }} kg</td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>
</template>

<style scoped>
.training-set-list {
  margin-top: 2rem;
  padding: 1.5rem;
  border-radius: 12px;
  background: white;
  box-shadow: 0 4px 12px rgb(0 0 0 / 8%);
}

.training-set-list h2 {
  margin-top: 0;
}

.subtitle {
  color: #4b5563;
}

.table-wrapper {
  overflow-x: auto;
}

table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 1rem;
}

th,
td {
  padding: 0.8rem;
  border-bottom: 1px solid #e5e7eb;
  text-align: left;
}

th {
  color: white;
  background: #1f2937;
}

tbody tr:hover {
  background: #f9fafb;
}
</style>