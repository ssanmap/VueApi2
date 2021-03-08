<template>
    <px-table  :assets="assets" />
</template>

<script>
import PxTable from "@/components/PxTable";
import api from "@/api";

export default {
    name: "Home",
    components: {
        PxTable
    },
    data(){
        return {
            assets: []
        }
    },
    created(){
        api.getAssets().then(assets => (this.assets = assets))
    }
    
}
</script>