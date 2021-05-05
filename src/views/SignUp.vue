<template>
  <form class="registerForm" action="" method="post" enctype="multipart/form-data">
    <div>
      <label for="surname">Фамилия*</label>
      <input v-model="surname" id="surname" placeholder="Фамилия" required>
      <label for="name">Имя*</label>
      <input v-model="name" id="name" placeholder="Имя" required>
      <label for="fatherName">Отчество</label>
      <input v-model="fatherName" id="fatherName" placeholder="Отчество">
    </div>
    <div>
      <label for="birthday">Дата рождения*</label>
      <input type="date" v-model="birthday" id="birthday" required>
      <label for="phone">Номер телефона*</label>
      <input type="tel" v-model="phone" id="phone" pattern="8[0-9]{10}" placeholder="79991234567" required>
    </div>
    <div>
      <span>Пол</span>
      <input type="radio" v-model="male" name="sex" value="male">
      <label for="male">Мужской</label>
      <input type="radio" v-model="female" name="sex" value="female">
      <label for="female">Женский</label>
    </div>
    <div>
      <label for="clientType">Группа клиентов*</label>
      <select class="clientType" v-model="clientType" name="clientType" multiple required>
        <option value="vip">VIP</option>
        <option value="problem">Проблемный</option>
        <option value="oms">ОМС</option>
      </select>
    </div>
    <div>
      <label for="doctor">Лечащий врач</label>
      <select class="doctor" v-model="doctor" name="doctor">
        <option value="ivanov">Иванов</option>
        <option value="zakharov">Захаров</option>
        <option value="chernyshova">Чернышева</option>
      </select>
    </div>
    <div>
      <label for="sms">Не отправлять СМС</label>
      <input type="checkbox" v-model="sms" name="sms">
    </div>
    <p class="adress">Адрес</p>
    <div>
      <label for="index">Индекс</label>
      <input type="tel" v-model="index" name="index" pattern="[0-9]{6}" placeholder="123456">
      <label for="country">Страна</label>
      <input type="text" v-model="country" name="country" placeholder="Страна">
      <label for="region">Область</label>
      <input type="text" v-model="region" name="region" placeholder="Область">
    </div>
    <div>
      <label for="city">Город*</label>
      <input type="text" v-model="city" name="city" placeholder="Город" required>
      <label for="street">Улица</label>
      <input type="text" v-model="street" name="street" placeholder="Улица">
      <label for="house">Дом</label>
      <input type="tel" v-model="house" name="house" placeholder="Дом">
    </div>
    <p class="docs">Паспорт</p>
    <div>
      <label for="docType">Тип документа*</label>
      <select class="docType" v-model="docType" name="docType" required>
        <option value="passport">Паспорт</option>
        <option value="birthCertificate">Свидетельство о рождении</option>
        <option value="driverLicence">Вод. удостоверение</option>
      </select>
    </div>
    <div>
      <label for="serialNumber">Серия</label>
      <input type="tel" v-model="serialNumber" name="serialNumber" placeholder="1234" pattern="[0-9]{4}">
      <label for="docNumber">Номер</label>
      <input type="tel" v-model="docNumber" name="docNumber" placeholder="123456" pattern="[0-9]{6}">
    </div>
    <div>
      <label for="issuedBy">Кем выдан</label>
      <input type="text" v-model="issuedBy" name="issuedBy" placeholder="Кем выдан">
      <label for="issueDate">Дата выдачи*</label>
      <input type="date" v-model="issueDate" name="issueDate" required>
    </div>
    <p class="required">*Поле обязательное для заполнения</p>
    <button type="submit" name="submit">Отправить</button>
  </form>
</template>

<script>

export default {
  name: 'SignUp'
}
</script>
