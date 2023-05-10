<template>
  <a v-if="isExternalLink"
    :href="link.to">{{ link.name }}</a>
</template>

<script>
export default {
    props: {
        link: {
            type: Object,
            required: true
        }
    },

    computed: {
        isExternalLink() {
            return this.link.to.startsWith('http')
        }
    }
}
</script>

<style>

</style>