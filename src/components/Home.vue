<template>
    <div>
        <!--轮播图区域-->
        <mt-swipe :auto="4000">
            <mt-swipe-item v-for="(item, key) in lunbotuList" :key="key">
                <img :src="item.img" :alt="item.title">
            </mt-swipe-item>
        </mt-swipe>
        <!-- 九宫格 到 6宫格 的改造工程 -->

        <ul class="mui-table-view mui-grid-view mui-grid-9">
            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3"><a href="#">
                <img src="../../images/menu1.png" alt="">
                <div class="mui-media-body">新闻资讯</div></a></li>
            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3"><a href="#">
                <img src="../../images/menu2.png" alt="">
                <div class="mui-media-body">图片分享</div></a></li>
            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3"><a href="#">
                <img src="../../images/menu3.png" alt="">
                <div class="mui-media-body">商品购买</div></a></li>
            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3"><a href="#">
                <img src="../../images/menu4.png" alt="">
                <div class="mui-media-body">留言反馈</div></a></li>
            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3"><a href="#">
                <img src="../../images/menu5.png" alt="">
                <div class="mui-media-body">视频专区</div></a></li>
            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3"><a href="#">
                <img src="../../images/menu6.png" alt="">
                <div class="mui-media-body">联系我们</div></a></li>
        </ul>



    </div>
</template>

<script>
export default {
    name: "Home",
    data() {
        return {
            lunbotuList:[ // 保存轮播图的数组
                {id:1,title:'联想电脑',img:'//img20.360buyimg.com/pop/s1180x940_jfs/t1/112194/40/8858/75328/5ed4cfdaEa2809655/86f4d6868be9b371.jpg.webp'},
                {id:2,title:'年终大促',img:'//img13.360buyimg.com/pop/s1180x940_jfs/t1/122022/29/2140/72437/5ec33779Ead8c24e5/b8ef831ac7a94d08.jpg.webp'},
                {id:3,title:'影像生活',img:'//img10.360buyimg.com/pop/s1180x940_jfs/t1/134162/6/1851/80384/5edf3b24E70cd4092/7d42931ca5ece9d3.jpg.webp'},
                {id:4,title:'电脑整机',img:'//img14.360buyimg.com/pop/s1180x940_jfs/t1/115293/37/8433/101063/5ecdb806E3e785d2b/b28d5bca26383697.jpg.webp'},
            ],
        }
    },
    created() {
    },

    methods: {

    }

}
</script>

<style scoped lang="scss">
.mint-swipe {
    height: 200px;

    .mint-swipe-item {

        &:nth-child(1) {
            background-color: red;
        }

        &:nth-child(2) {
            background-color: blue;
        }

        &:nth-child(3) {
            background-color: cyan;
        }

        img {
            width: 100%;
            height: 100%;

        }
    }
}



.mui-grid-view.mui-grid-9 {
    background-color: #fff;
    border: none;
    img {
        width: 60px;
        height: 60px;
    }

    .mui-media-body{
        font-size: 13px;
    }
}

.mui-grid-view.mui-grid-9 .mui-table-view-cell {
    border: 0;
}
</style>