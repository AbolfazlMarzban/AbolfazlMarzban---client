<template>
    <div>
        <AdminHeader :insert="true" :delet="true" @insert="insert" />
        <v-data-table :headers="headers"></v-data-table>
    </div>
</template>
  
<script>
export default {
    layout: "admin",
    data() {
        return {
            headers: [
                {
                    text: 'image',
                    value: 'image',
                    sort: false,
                    align: 'center'
                },
                {
                    text: 'name',
                    value: 'name',
                    sort: false,
                    align: 'center'
                },
                {
                    text: 'link',
                    value: 'link',
                    sort: false,
                    align: 'center'
                }
            ]
        }
    },
    methods: {
        insert() {
            this.$router.push('/admin/courses/insert')
        }
    }
}
</script>
  
<style></style>