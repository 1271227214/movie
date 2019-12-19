<template>
    <div style="width:900px;">
        <el-row style="text-align: left;margin-top: 30px;line-height: 35px;">
            <el-col :span="16" :offset="3">
                <span style=" font-size: 25px;">豆瓣电影排行榜</span>
            </el-col>
            <el-col :span="16" :offset="3">
                <span style="color:green;" >豆瓣新片榜······</span>
            </el-col>
        </el-row>
        <div v-for="movie in movieList">
        <div style="padding-top:10px;padding-left:110px;">
            <hr STYLE="BORDER:0.5px dashed;color:rgba(203,203,203,0.75)"></hr>
        <el-row type="flex"justify="center" :gutter="20">
            <el-col :span="5" >
                <img v-bind:src="movie.src"style="width: 85px;height:120px">
            </el-col>
            <el-col :span="16"style="text-align: left;padding-top:5px;" >
            <div style="color:#37a;">{{movie.title}}</div>
                <div style="padding-top:10px;">{{movie.describe}}</div>
            </el-col>
            <el-col :span="5" style="text-align: left">
                <div>
                    <div style="display: inline-block;float: left;padding-top:35px;">
                        <el-rate disabled v-model="movie.scoring.star"></el-rate>
                        <div style="display: inline-block">{{movie.scoring.score}}</div>
                        <div style="font-size:12px;padding-left: 3px">({{movie.scoring.amount}}人评价)</div>
                    </div>
                </div>
            </el-col>
        </el-row>
        </div>
        </div>
    </div>
</template>
<script>
    import ElProgress from "../../node_modules/element-ui/packages/progress/src/progress";
    export default {
        components: {ElProgress},
        data () {
            return {
                    movieList:[
                        {
                            src:require( "../assets/11.jpg"),
                            title: "爱尔兰人/爱尔兰杀手（港）/听说你刷房子了",
                            describe: "2019-09-27(纽约电影节) / 2019-11-01(美国点映) / 2019-11-27(美国网络) / 罗伯特·德尼罗 / 阿尔·帕西诺 / 乔·佩西 / 安娜·帕奎因 / 杰西·普莱蒙 / 哈威·凯特尔 / 斯蒂芬·格拉汉姆 / 鲍比·坎纳瓦尔 / 杰克·休斯顿 / 阿莱卡萨·帕拉迪诺 / 凯瑟琳·纳杜奇...",
                            scoring: {
                                score: 9.1,
                                amount: 48085,
                                star: 4.5
                            }
                        },
                        {
                            src:require( "../assets/12.jpg"),
                            title: "小丑/小丑起源电影：罗密欧 / Romeo  ",
                            describe: "2019-09-27(纽约电影节) / 2019-11-01(美国点映) / 2019-11-27(美国网络) / 罗伯特·德尼罗 / 阿尔·帕西诺 / 乔·佩西 / 安娜·帕奎因 / 杰西·普莱蒙 / 哈威·凯特尔 / 斯蒂芬·格拉汉姆 / 鲍比·坎纳瓦尔 / 杰克·休斯顿 / 阿莱卡萨·帕拉迪诺 / 凯瑟琳·纳杜奇...",
                            scoring: {
                                score: 8.8,
                                amount: 380752,
                                star: 4.5
                            }
                        },
                        {
                            src:require( "../assets/13.jpg"),
                            title: "82年生的金智英/82年生金智英/Kim Ji-young,Borm 1982 ",
                            describe: "2019-10-23(韩国) / 2019-11-07(中国香港) / 郑有美 / 孔侑 / 金美京 / 孔敏晶 / 朴成妍 / 李凤莲 / 金圣喆 / 李乌 / 李海云 / 孙成灿 / 金正英 / 李娜云 / 禹志贤 / 韩国 / 金度英 / 118分钟 / 82年生的金智英 / 剧情 / 刘英雅 Yeong-ah Yoo / 赵南珠 Nam-joo...",
                            scoring: {
                                score: 8.7,
                                amount: 390752,
                                star: 4.5
                            }
                        },
                        {
                            src:require( "../assets/14.jpg"),
                            title: "好莱坞往事/从前，有个荷里活（港）/从前有个好莱坞...（台） ",
                            describe: "2019-05-21(戛纳电影节) / 2019-07-26(美国) / 2019(中国大陆) / 莱昂纳多·迪卡普里奥 / 布拉德·皮特 / 玛格特·罗比 / 埃米尔·赫斯基 / 玛格丽特·库里 / 蒂莫西·奥利芬特 / 茱莉亚·巴特斯 / 奥斯汀·巴特勒 / 达科塔·范宁 / 布鲁斯·邓恩 /...",
                            scoring: {
                                score: 7.3,
                                amount: 345672,
                                star: 3.5
                            }
                        },
                        {
                            src:require( "../assets/15.jpg"),
                            title: "婚姻故事 ",
                        describe: "2019-08-29(威尼斯电影节) / 2019-12-06(美国) / 斯嘉丽·约翰逊 / 亚当·德赖弗 / 梅里特·韦弗 / 劳拉·邓恩 / 雷·利奥塔 / 朱丽·哈基提 / 马克·奥布莱恩 / 华莱士·肖恩 / 阿伦·阿尔达 / 凯尔·柏海莫 / 米奇·萨姆纳 / 艾奇·罗伯逊 / 马修·马希尔...",
                        scoring: {
                            score: 8.8,
                            amount: 245652,
                            star: 4.5
                        }
                        },
                        {
                            src:require( "../assets/16.jpg"),
                            title: "准备好了没/弑婚游戏(台) / 爆血新婚夜(港) ",
                            describe: "2019-08-21(美国) / 萨玛拉·维文 / 安迪·麦克道威尔 / 马克·奥布莱恩 / 亚当·布罗迪 / 亨利·科泽尼 / 妮基·瓜达尼 / 梅兰妮·斯科洛凡诺 / 克里斯蒂安·布鲁恩 / 伊利斯 莱韦斯克 / 约翰·拉尔斯顿 / 达妮埃拉·巴博萨 / 伊拉娜·盖尔 /...",
                            scoring: {
                                score: 6.7,
                                amount: 290752,
                                star: 3.5
                            }
                        },
                        {
                            src:require( "../assets/17.jpg"),
                            title: "克劳斯：圣诞节的秘密/圣诞老人 ",
                            describe: "2019-11-08(西班牙) / 2019-11-08(英国) / J·K·西蒙斯 / 詹森·舒瓦兹曼 / 拉什达·琼斯 / 琼·库萨克 / 诺曼·麦克唐纳徳 / 威尔·萨索 / 塞尔希奥·巴勃罗斯 / 米拉·布雷纳 / 内达·玛格丽特·拉巴 / 悉尼·布朗 / 泰迪·布鲁姆 / 艾玛·香农 / 肯德尔·卓依...",
                            scoring: {
                                score: 8.6,
                                amount: 9752,
                                star: 4.5
                            }
                        },
                        {
                            src:require( "../assets/18.jpg"),
                            title: "第一滴血5：最后的血/第一滴血：终极血战(港) / 蓝波：最后一滴血(台)",
                            describe: "2019-09-18(印度尼西亚) / 2019-09-20(美国) / 2019-09-27(西班牙) / 西尔维斯特·史泰龙 / 帕斯·贝加 / 塞尔吉奥·佩里斯-门切塔 / 艾德里安娜·巴拉扎 / 维特·蒙雷尔 / 吉妮·金 / 华金·科西奥 / 帕斯卡西奥·洛佩斯 / 奥斯卡·贾恩那达 / 亚历山大·迪米特罗夫...",
                            scoring: {
                                score: 7.5,
                                amount: 18566,
                                star: 4
                            }
                        },
                        {
                            src:require( "../assets/19.jpg"),
                            title: "行骗天下JP：浪漫篇/信用欺诈师JP:香港浪漫篇(港) / 行骗天下 电影版  ",
                            describe: "2019-05-17(日本) / 长泽雅美 / 东出昌大 / 小日向文世 / 竹内结子 / 三浦春马 / 江口洋介 / 小手伸也 / 织田梨沙 / 前田敦子 / 小栗旬 / 佐津川爱美 / 冈田义德 / 生濑胜久 / 日本 / confidenceman-movie.com / 田中亮 / 116分钟 / 行骗天下JP：浪漫篇...",
                            scoring: {
                                score: 8.2,
                                amount: 13516,
                                star: 4
                            }
                        },
                        {
                            src:require( "../assets/20.jpg"),
                            title: "纽约的一个雨天/情迷纽约下雨天(港) / 纽约有雨 ",
                            describe: "2019-07-26(波兰) / 蒂莫西·柴勒梅德 / 艾丽·范宁 / 赛琳娜·戈麦斯 / 裘德·洛 / 迭戈·卢纳 / 列维·施瑞博尔 / 苏琪·沃特豪斯 / 凯莉·罗尔巴赫 / 丽贝卡·豪尔 / 安娜莱吉·阿什福特 / 切莉·琼斯 / 葛瑞芬·纽曼 / 凯瑟琳·利·斯科特 /...",
                            scoring: {
                                score: 7.5,
                                amount: 12552,
                                star: 4.
                            }
                        },
                        ]
                }
            }

    }
</script>