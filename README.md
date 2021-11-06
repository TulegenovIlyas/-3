#<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <link rel="stylesheet" href="style.css">
  <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
  <title>To-do app</title>
</head>
<body>
  <div id="app">
    <div class="stats">
      <h3 class="stats__title">{{"Текущих задач: "+ tasks.length}}</h3>
    </div>
    <task @task_done="delete_task(index)" :key="index" v-for="(data,index) in tasks" :data="data" ></task>
    <div class="add_task">
      <div class="add_task__input ">
          <input placeholder="Новая задача..." type="text" v-model="new_task.title">
          <textarea placeholder="Описание" type="text" v-model="new_task.desc"></textarea>
      </div>
      <button class="add_task__btn" @click="add_task">➕</button>
    </div>
  </div>
</body>
<script src="script.js"></script>
</html>
