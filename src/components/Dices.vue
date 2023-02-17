<template>
    <div class="custom-container">
        <button class="button is-link" v-on:click="throwDice">
            Tirar
        </button>
    </div>
    <div class="columns ">
        <div class="column is-flex is-justify-content-center">
            <figure class="image custom-background">
                <img v-bind:src="leftDice" alt="Left Dice">
            </figure>
        </div>
        <div class="column is-flex is-justify-content-center">
            <figure class="image custom-background">
                <img v-bind:src="rigthDice" alt="Rigth Dice">
            </figure>
        </div>
    </div>

    <article v-if="leftDice === rigthDice" class="message is-success is-small">
        <div class="message-header">
            <p>Congrats</p>
        </div>
        <div class="message-body">
            You Win!!!!. Wanna play again?😏
        </div>
    </article>
</template>

<script>
export default {
    data() {
        return {
            leftDice: 'assets/img/dice1.png',
            rigthDice: 'assets/img/dice6.png',
        }
    },
    methods: {
        throwDice() {
            this.leftDice = `assets/img/dice${this.getRandomNumber()}.png`
            this.rigthDice = `assets/img/dice${this.getRandomNumber()}.png`
        },
        getRandomNumber(min = 1, max = 6) {
            min = Math.ceil(min);
            max = Math.floor(max);
            return Math.floor(Math.random() * (max - min) + min);
        }
    },
}
</script>

<style scoped>
.custom-background {
    background: grey;
    border-radius: 20px;
}

.custom-container {
    display: flex;
    justify-content: center;
}
</style>