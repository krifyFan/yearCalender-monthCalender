<template>
    <div>
        <!-- 年份选择器 -->
        <section>
            <Input v-model="calenderData.choosedYear"></Input>
            <year-calender ref="getYearChild" v-on:getYearChild="getActiveYearText"></year-calender>
        </section>  
        <!-- 月份选择器 -->
        <section>
            <Input v-model="calenderData.chooseMonth"></Input>
            <month-calender ref="getMonthChild" v-on:getMonthChild="getActiveMonthText"></month-calender>
        </section>
    </div>

</template>
<script>
import yearCalender from '@/components/yearCalender'
import monthCalender from '@/components/monthCalender'
export default {
    comments: {
        yearCalender,
        monthCalender
    },
    data() {
        return {
            calenderData: {
                choosedYear: [],
                chooseMonth: []
            }
        }
    },
    methods: {
        getActiveYearText(childValue){
            this.calenderData.choosedYear = childValue
        },
        getActiveMonthText(childValue){
            childValue.forEach(element => {
               //这里的format方法是自己封装的方法，可根据自己的需要封装自己的format方法 
				this.calenderData.chooseMonth.push(new Date(element).format('yyyy-MM'))
            });
        }   
    },
}
</script>
<style scoped>

</style>
