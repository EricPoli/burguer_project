<template>
    <div>
        <div>
            <form id="burguer-form" >
                <div class="input-container" >
                    <label for="name">Nome do cliente:</label>
                    <input type="text" id="name" name="name" v-model="name" placeholder="Digite o seu nome">
                </div>
                <div class="input-container" >
                    <label for="bread">Escolha o pão:</label>
                    <select id="bread" name="bread" v-model="bread">
                        <option value="">Selecione o seu pão</option>
                        <option value="integral">Integral</option>
                    </select>
                </div>
                <div class="input-container" >
                    <label for="meat">Escolha a carne do seu Burguer:</label>
                    <select id="meat" name="meat" v-model="meat">
                        <option value="">Selecione a sua carne</option>
                        <option value="maminha">Maminha</option>
                    </select>
                </div>
                <div class="input-container" id="options-container">
                    <label id="options-title" for="options">Selecio e os opcionais:</label>
                    <div class="checkbox-container">
                        <input type="checkbox" name="options" id="options" v-model="options" value="salame">
                        <span>Salame</span>
                    </div>
                    <div class="checkbox-container">
                        <input type="checkbox" name="options" id="options" v-model="options" value="salame">
                        <span>Salame</span>
                    </div>
                    <div class="checkbox-container">
                        <input type="checkbox" name="options" id="options" v-model="options" value="salame">
                        <span>Salame</span>
                    </div>
                </div>
                <div class="input-container">
                    <input type="submit" class="submit-btn" value="Criar meu Burguer">
                </div>
            </form>
        </div>
    </div>
</template>

<script>
    export default {
        name: "BurguerForm"
    }
</script>

<style scoped>
    #burguer-form {
        max-width: 400px;
        margin: 0 auto;
    }

    .input-container {
        display: flex;
        flex-direction: column;
        margin-bottom: 20px;
    }

    label {
        font-weight: bold;
        margin-bottom: 15px;
        color: #222;
        padding: 5px 10px;
        border-left: 4px solid #fcba03;
    }

    input, select {
        padding: 5px 10px;
        width: 300px;
    }

    #options-container {
        flex-direction: row;
        flex-wrap: wrap;
    }

    #options-title {
        width: 100%;
    }

    .checkbox-container {
        display: flex;
        align-items: flex-start;
        width: 50%;
        margin-bottom: 20px;
    }

    .checkbox-container span, 
    .checkbox-container input {
        width: auto;
    }

    .checkbox-container span {
        margin-left: 6px;
        font-weight: bold;
    }

    .submit-btn {
        background-color: #222;
        color: #fcba03;
        font-weight: bold;
        border: 2px solid #222;
        padding: 10px;
        font-size: 16px;
        margin: 0 auto;
        cursor: pointer;
        transition: .5s;
    }

    .submit-btn:hover {
        background-color: transparent;
        color: #222;
    }
</style>