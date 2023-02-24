<template>
    <div class="entry-title d-flex justify-content-between p-2">

        <div>
            <span class="text-success fs-3 fw-bold">15</span>
            <span class="mx-1 fs-3">Julio</span>
            <span class="mx-2 fs-4 fw-light">2020, jueves</span>
        </div>

        <div>
            <button class="btn btn-danger mx-2">
                Borrar
                <i class="fa fa-trash-alt"></i>
            </button>

            <button class="btn btn-primary ">
                Subir Foto
                <i class="fa fa-upload"></i>

            </button>

        </div>

    </div>
    <hr>
    <div class="d-flex flex-column px-3 h-75">
        <textarea placeholder="¿Qué sucedió hoy?"></textarea>
    </div>

    <Fab :icon='fa-save' />

    <img 
    src="https://occ-0-2773-1555.1.nflxso.net/dnm/api/v6/E8vDc_W8CLv7-yMQu8KMEC7Rrr8/AAAABYxJFBDckfZw1YUEIPwyuIg43Kw_HUBLvnCcgdOlvvf5Nc90SF3HSAi5L8uLyBqjziKBY-kGD2wu2JAqVsdHVR0frb6qG26I_U5v.jpg?r=77f" 
    alt="entry-picture"
    class="img-thumbnail">
</template>

<script>
import { defineAsyncComponent } from 'vue'
export default {

    components:{
        Fab: defineAsyncComponent(() => import('@/modules/daybook/components/Fab.vue'))
    }
}
</script>

<style lang="scss" scoped>

    textarea{

        font-size: 20px;
        border: none;
        height: 100%;
        
        &:focus {
            outline: none;
        }
    }

    img{
        width: 200px;
        position: fixed;
        bottom: 150px;
        right: 20px;
        box-shadow: 0px 5px 10px rgba($color: #000000, $alpha: 0.2);
    }

    

</style>

