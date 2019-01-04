<template>
    <img v-bind:src="imageSrc" alt="image" />
</template>

<script>
export default {
    name : 'v-bind',
    data() {
        return  {
            imageSrc: '',
            imaages : [
                'path/to/image/1.jpg',
                'path/to/image/2.jpg',
                'path/to/image/3.jpg',
            ]
        }
    },
    mounted() {
        let vm = this
        let count = 0

        setInterval(function() {
            vm.imageSrc = vm.images[count++]
            if(count == vm.images.length)
                count = 0
        }, 1500)
    }
}
</script>
