<template><!--只能有一个根节点-->
    <div>
        <table>
            <tr>
                <td>编号</td>
                <td>图书名称</td>
                <td>作者</td>
            </tr>
            <tr>
                <td>{{books[0].id}}</td>
                <td>{{books[0].name}}</td>
                <td>{{books[0].author}}</td>
            </tr>
            <tr v-for="item in books">
                <td>{{item.id}}</td>
                <td>{{item.name}}</td>
                <td>{{item.author}}</td>
            </tr>
        </table>
        {{msg}}
    </div>
</template>

<script>
    export default{//所有的js都要写到这个花括号里
        name: "Book",
        data(){//20200312k将data写成date导致页面不显示
            return {
                books:[
                    {
                        id:1,
                        name:'MySQL从删库到跑路',
                        author:'赵日天'
                    },
                    {
                        id:2,
                        name:'MySQL从删库到跑路',
                        author:'赵日地'
                    },
                    {
                        id:3,
                        name:'MySQL从删库到跑路',
                        author:'赵日东'
                    }
                ]
            }
        }
    }
</script>
    <style scoped/>

