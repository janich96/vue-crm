<template>
  <form class="" action="" method="post">
    <label for="surname">Фамилия</label>
    <input v-model="surname" id="surname" placeholder="Фамилия">
    <label for="name">Имя</label>
    <input v-model="name" id="name" placeholder="Имя">
    <label for="fatherName"></label>
    <input v-model="fatherName" id="fatherName" placeholder="Отчество">
    <label for="birthday">Дата рождения</label>
    <input type="date" v-model="birthday" id="birthday">
    <label for="phone">Телефон</label>
    <input type="number" v-model="phone" id="phone">
  </form>
</template>

<script>

export default {
  name: 'SignUp'
}
</script>
