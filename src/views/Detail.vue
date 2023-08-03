<template>
        <!-- <div v-if="filteredProduk.length == 0">
        <h1>Produk Tidak Tersedia</h1>
    </div>
    <div v-else>
        <h1>Daftar Produk {{ categoryName }}</h1>
    </div> -->

    <h1>Detail {{ detail.nama }}</h1>
    <h4>Harga: {{ detail.harga }}</h4>
    <img :src="getImgSrc(detail.img)" alt="Category Image" style="width: 300px;"/>
    <h4>Keterangan: {{ detail.keterangan }}</h4>
  </template>

<script>
import { produk } from '@/assets/produk.js'

export default {
    props: [
        "id_produk"
    ],
    setup(props)
    {
        const getImgSrc = (imgFileName) => {
        return '../src/assets/img/' + imgFileName + '';
        };
        const detail = produk["produk"].find(function(item) {
            return item.id == props.id_produk;
        });

        return{
            detail,
            getImgSrc
        }
    }
}
</script>

