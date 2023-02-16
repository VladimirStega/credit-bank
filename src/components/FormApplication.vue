<template>
    <form action="">

        <input class="intut-style"
        v-model="name"
        id="name"
        type="name"
        placeholder="ФИО"
        required
        pattern="[A-Za-z]{3}"
        >

        <input class="intut-style"
        v-model="email"
        id="email"
        type="email"
        placeholder="Электронный адрес"
        required
        pattern=".+@globex\.com" size="30"
        >

        <input class="intut-style"
        v-model="phone"
        id="phone"
        type="tel"
        placeholder="Номер телефона"
        required
        pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}"
        >  
        <select class="intut-style">
            <option value="Российская федерация">Российская федерация</option>
            <option value="Белорусь">Белорусь</option>
            <option value="Украина">Украина</option>
            <option value="Казахстан">Казахстан</option>
        </select>

        <div class="checkbox">
            <input class="checkbox-input"
            id="checkbox"
            type="checkbox"
            v-model="checked">
            <label for="checkbox" class="checkbox-label">
                Я соглашаюсь на <span>обработку</span>  моих персональных данных
            </label>
        </div>
        
    </form>
    <button class="btn">Заказать сейчас</button>
</template>

<script>
export default {
 name: 'FormApplication',
  data() {
    return{
        name: '',
        email: '',
        phone: '',
        selelcted: 'Российская федерация',
        checked: false,
        }
    },
     methods: {
        showFormApplication() {
            this.formApplication = !this.formApplication
    }
  }
}

</script>

<style>

.intut-style {
    width: 100%;
    height: 80px;
    margin-bottom: 20px;
    padding-left: 30px;
    border-radius: 10px;
    border: none;
    background-color: #191919;
}

.intut-style:focus {
    outline: none;
    background-color: #333333;
}

.intut-style::placeholder {
    font-size: 20px;
}

.intut-style {
    font-size: 20px;
    color: #fff;
}

.checkbox {
    margin: 20px 0;
}

.checkbox-label {
    padding-left: 50px;
    font-size: 16px;
    color: #6C6C6C;
 }

.checkbox-label span{
    color: #fff;
 }

.btn{
    padding: 26px 45px;
    border-radius: 10px;
    font-size: 24px;
    font-weight: 700;
    color: #fff;
    background-color: #C0965C;
    cursor: pointer;
  }

</style>