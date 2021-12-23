<template>
    <el-row justify="center">
        <el-col :span="16">
            <md-editor @onGetCatalog="onGetCatalog" v-model="content" :previewOnly="true" />
        </el-col>
        <el-col :span="8">
            <catalog class="catalog" :heads="catalogList"></catalog>
        </el-col>
    </el-row>
</template>

<script setup>
import MdEditor from "md-editor-v3";
import "md-editor-v3/lib/style.css";
import Catalog from './Catalog.vue';
import { ref } from "@vue/reactivity"
import Catalog from "./Catalog.vue";
const content = ref("文章内容")
const catalogList = ref([])
const onGetCatalog = (list) => {
    this.catalogList = list
},
</script>