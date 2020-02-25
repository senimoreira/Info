<template>
<div>
     <form >
        <h1>Dados Pessoais:</h1>

      <div class="form-inline"> 
        <label for="name" >Nomes próprios</label>
        <input type="text" id="name" v-model="firstName">
      </div>

      <div class="form-inline"> 
        <label for="lastName">Apelidos</label>
        <input type="text" id="lastName" v-model="lastName">
      </div>

      <div class="form-inline"> 
        <label for="gender">Sexo</label>
        <select id="gender" v-model="gender">
        <option value="Feminino">Feminino</option>
        <option value="Masculino">Masculino</option>
        </select>
      </div>

      <div class="form-inline"> 
        <label for="birth">Data de nascimento</label>
        <input type="date" id="birth" v-model="birth" placeholder="dd/MM/yyyy">
      </div>

      <div class="form-inline"> 
        <label  for="id">Numero de Identificação</label>
        <input type="number" id="id" v-model="id">
      </div>

      <div class="form-inline"> 
        <label for="type">Tipo</label>
            <select id="type" v-model="type">
            <option value="Passaporte">Passaporte</option>
            <option value="CC">Cartão de Cidadão</option>
        </select>

      </div>

      <div class="form-inline"> 
        <label for="validity">Validade</label>
        <input type="date" id="validity" v-model="validity" placeholder="dd/MM/yyyy">
      </div>

      <div class="form-inline"> 
        <label for="nationality">Nacionalidade</label>
        <Nationality/>
      </div>

      <div class="form-inline"> 
        <label for="NIF">Nº de Contribuinte</label>
        <input type="text" id="NIF" v-model="NIF">
      </div>

      <div class="form-inline"> 
        <label for="residency">País de residência</label>
        <Residency/>
      </div>

      <div class="form-inline"> 
        <label for="address">Morada</label>
        <input type="text" id="address" v-model="address">
      </div>

      <div class="form-inline"> 
        <label for="postal">Código Postal</label>
        <input type="text" id="postal" v-model="postal">
      </div>

      <div class="form-inline"> 
        <label for="locality">Localidade</label>
        <input type="text" id="locality" v-model="locality">
      </div>

      <div class="form-inline"> 
        <label for="phone">Telemóvel</label>
        <input type="tel" id="phone" v-model="phone">
      </div>

    <input type="submit" value="Enviar">
  </form>

  <p> The final is: </p>
  <p> firstName: {{firstName}}</p>
  <p> lastName: {{lastName}}</p>
  <p> gender: {{gender}}</p>
  <p> birth: {{birth}}</p>
  <p> id: {{id}}</p>
  <p> type: {{type}}</p>
  <p> validity: {{validity}}</p>
  <p> nationality: {{nationality}}</p>
  <p> NIF: {{NIF}}</p>
  <p> residency: {{residency}}</p>
  <p> address: {{address}}</p>
  <p> postal: {{postal}}</p>
  <p> locality: {{locality}} </p>
  <p> phone: {{phone}}</p>


</div>
</template>

<script>

import Residency from '../Residency'
import Nationality from '../Nationality'

export default {
    name: 'Information',

    components: {
        Residency,
        Nationality
        },

    props: {
        firstName: String,
        lastName: String,
        gender: String,
        birth: Number,
        id: Number,
        type: String,
        validity: Number,
        nationality: String,
        NIF: Number,
        residency:String,
        address: String,
        postal: Number,
        locality: String,
        phone: Number, 
    }
}
</script>

<style >

.form-inline {
  display: flex;
  align-items: center;
}


label{
  width: 15%;
  text-align: right;
  margin-right: 20px;
}

input, select {
  width: 85%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}


input[type=submit] {
  width: 100%;
  background-color: rgb(40, 146, 179);
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}



</style>