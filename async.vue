<script>
export default {
    mounted () {
        this.run();
        console.log('step2')
    },
    methods: {
        fun_1() {
            return new Promise((resolve, reject) => {
                setTimeout(() => {
                    resolve('111')
                }, 2000)
            })
        },
        fun_2() {
            return new Promise((resolve, reject) => {
                setTimeout(() => {
                    resolve('222')
                }, 1000)
            })
        },
        fun_3() {
            return new Promise((resolve, reject) => {
                setTimeout(() => {
                    resolve('333')
                }, 2000)
            })
        },
        async run () {
            const data_1 = await this.fun_1();
            console.log(data_1) 
            const data_2 = await this.fun_2();
            console.log(data_2)
            const data_3 = await this.fun_3();
            console.log(data_3)
        }
    }
}
</script>