<template>
    <v-container class="register">
        <v-row>
        <v-col cols="12">
            <v-card>
            <v-card-title>
                <span class="headline">Registrera för att spela</span>
            </v-card-title>
            <v-card-text>
                <v-form @submit.prevent="register">
                <v-text-field
                    v-model="form.email"
                    label="Email"
                    required
                ></v-text-field>
                <v-text-field
                    v-model="form.password"
                    label="Password"
                    required
                    type="password"
                ></v-text-field>
                <v-text-field
                    v-model="form.confirmPassword"
                    label="Confirm Password"
                    required
                    type="password"
                ></v-text-field>
                <v-btn type="submit">Registrera</v-btn>
                </v-form>
            </v-card-text>
            </v-card>
        </v-col>
        </v-row>
    </v-container>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { useRouter } from 'vue-router'

const form = ref({
    email: '',
    password: '',
    confirmPassword: ''
})

const router = useRouter()

const register = () => {
    console.log(form.value)
    router.push('/')
}


</script>

<style scoped>
    .register {
        margin-top: 20px;
        align-items: center;
        text-align: center;
    }

    .v-card {
        margin-top: 20px;
    }

    .v-btn {
        margin-top: 20px;
    }

    .v-text-field {
        margin-top: 20px;
    }

    .v-container {
        margin-top: 20px;
    }

</style>