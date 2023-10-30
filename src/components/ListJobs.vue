<template>
     <!-- <ul v-for="(item, index) in herramientas" :key="index"></ul> -->
    <div>
        <article v-for="(listjob, index) in listjobs" :key="index" class="container card d-flex flex-row px-3 py-3 my-3 custom">
        <div class="d-flex align-items-center">
            <img class="rounded" :src="listjob.img" alt="Logo de la empresa">
        </div>
        <div class="ps-3 d-flex flex-column flex-grow-1 justify-content-center">
            <div class="d-flex align-items-center mb-2">
                <a class="text-dark text-decoration-none pointer d-md-inline-flex">
                    <h2 class="card-title fs-5 bold">{{ listjob.title }}</h2>
                    <ul class="d-flex align-items-center">
                        <li v-for="(skill, index) in listjob.skill" :key="index" class="border border-dark rounded-pill px-2 me-2">{{ skill }}</li>
                    </ul>
                </a>
            </div>
            <div class="flex-row justify-content-between align-items-center d-none d-md-flex">
                <div class="d-flex flex-row align-items-center">
                    <img class="icono" src="../assets/building.svg" alt="icono empresa">
                    <span class="text-capitalize">{{ listjob.organization }}</span>
                </div>
                <div class="d-flex flex-row align-items-center">
                    <img class="icono" src="../assets/ubicacion.svg" alt="icono ubicacion">
                    <p>{{ listjob.location }}</p>
                </div>
                <div class="d-flex flex-row align-items-center">
                    <img class="icono" src="../assets/money.svg" alt="icono salario">
                    <p>{{ listjob.salary }}</p>
                </div>
                <div class="d-flex flex-row align-items-center">
                    <img class="icono" src="../assets/vacante.svg" alt="icono vacante">
                    <p>{{ listjob.numberVacants }} Vacante</p>
                </div>
                <div class="d-flex flex-row align-items-center">
                    <img class="icono" src="../assets/fecha.svg" alt="icono fecha">
                    <p>{{ listjob.datePosted }} days ago</p>
                </div>
                <ul class="d-flex flex-row align-items-center">
                    <li v-for="(benefit, index) in listjob.benefits" :key="index" class="me-1 border border-dark rounded-pill px-2">
                        <img class="benefit" :src="benefit.icono" :title="benefit.title" :alt="benefit.icono">
                    </li>
                 
                </ul>
            </div>
        </div>
    </article>
    </div>
</template>
 
<script>
import {jobs} from '../js/data.js'
    export default {
        props: {

        },
        data() {
            const listjobs = { ...jobs} 
            return {
                
                listjobs
            }
        },
        methods: {

        }
    }

</script>
<style scoped>
    h2 {
        margin: 0;
    }
    img {
        width: 75px;
        height: auto;
    }
    .icono {
        width: 14px;
        height: 14px;
        margin-right: 4px;
    }
    .benefit {
        width: 14px;
        height: 14px;
    }
    ul {
        list-style: none;
        margin: 0;
        }
    p {
        margin: 0;
    }
    .custom:hover{
        box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    }
    a {
        cursor: pointer;
    }
</style>
