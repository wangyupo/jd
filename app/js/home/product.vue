<template lang="html">
    <Panel title="新品推荐" :class="$style.panel">
        <section :class="$style.content">
            <div class="arrow">更多尖货></div>
            <Slider :options="options" :items="items" cname="product-slider"/>
        </section>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
import Slider from "../core/slider.vue"
export default {
    components: {
        Panel,
        Slider,
    },
    data() {
        return {
            items: [
                {
                    href: "home",
                    src: "//img12.360buyimg.com/jrpmobile/jfs/t14641/180/1638965003/42812/2f4a85a1/5a54aadbN5269a1f1.jpg?width=335&height=421",
                },
                {
                    href: "home",
                    src: "//img12.360buyimg.com/jrpmobile/jfs/t14584/14/1620812582/49401/2a98f763/5a54aaeeNde89f852.jpg?width=335&height=421",
                },
                {
                    href: "home",
                    src: "//img12.360buyimg.com/jrpmobile/jfs/t15670/84/1493061629/40102/9f58843d/5a54aaecNecedcefd.jpg?width=335&height=421",
                },
                {
                    href: "home",
                    src: "//img12.360buyimg.com/jrpmobile/jfs/t15175/239/1652258993/41684/2827c8e3/5a54ab0fN0c596f31.jpg?width=335&height=421",
                },
            ],
            options: {
                slidesPerView: 2.3,
                spaceBetween: 30,
                freeMode: true,
            },
        }
    },
}
</script>

<style lang="scss">
.product-slider{
    .swiper-container{
        box-sizing: border-box;
        padding: 0 24px;
        .swiper-slide{
            a{
                display: inline-block;
                width: 100%;
                img{
                    width: 100%;
                    display: block;
                    height: 314px;
                    border: 1px solid #fafafa;
                }
            }
        }
    }
}
</style>

<style lang="scss" module>
    @import "../../css/element.scss";
    .panel{
        @include panel;
        .content{
            padding-bottom: 40px;
            position: relative;
            &>div{
                position: absolute;
                font-size: 28px;
                color: #999;
                right: 20px;
                top: -70px;
            }
        }
    }
</style>
