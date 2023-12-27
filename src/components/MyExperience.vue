<template>
    <section class="container">
        <div class="experience">
            <div class="an_exp">
            <h1>{{ lang.my_exp }}</h1>
            </div>
            
            <div class="an_exp">
                <h2>{{ lang.productowner }}</h2>
                <small>📆 2023 - {{ lang.now }}</small>
                <p>{{ lang.productowner_exp }}</p>
            </div>

            <div class="an_exp">
                <h2>{{ lang.softwarearquitect }}</h2>
                <small>📆 2022 - 2023</small>
                <p>{{ lang.softwarearquitect_exp }}</p>
            </div>

            <div class="an_exp">
                <h2>{{ lang.sre }}</h2>
                <small>📆 2022 - 2022</small>
                <p>{{ lang.sre_exp }}</p>
            </div>

            <div class="an_exp">
                <h2>{{ lang.devops }}</h2>
                <small>📆 2020 - 2022</small>
                <p>{{ lang.devops_exp }}</p>
            </div>

            <div class="an_exp">
                <h2>{{ lang.sysadmin_linux }}</h2>
                <small>📆 2020 - 2020</small>
                <p>{{ lang.sysadmin_linux_exp }}</p>
            </div>
            <div class="an_exp">
                <h2>{{ lang.sysadmin }}</h2>
                <small>📆 2016 - 2019</small>
                <p>{{ lang.sysadmin_exp }}</p>
            </div>            
            
        </div>
    </section>   
</template>

<script lang="ts">
import { defineComponent, computed } from '@vue/runtime-core'
import { useStore } from "vuex"
import { useLang } from "../utils/langs"
import my_experience from '../langs/my_experience'

export default defineComponent({
    setup() {
        const { getters } = useStore();
        const lang = computed(() => {
            return useLang(my_experience, getters.lang)
        })

        return {
            lang
        };
    },
})
</script>