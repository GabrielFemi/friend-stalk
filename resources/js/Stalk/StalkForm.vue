<template>
    <div>
        <div class="p-6 sm:px-20 bg-white border-b border-gray-200">
            <div class="bg-blue-100 border-t border-b border-blue-500 text-blue-700 px-4 py-3" role="alert">
                <p class="font-bold">Brief Information</p>
                <p class="text-sm">It is fun to stalk, ain't it?</p>
            </div>

            <div class="mt-8 text-2xl">
                Provide <code class = "">stalkee</code> details
            </div>

            <div class="mt-6 text-gray-500">
                <form @submit.prevent="submit" action = "/search" method="post">
                    <input v-model="form.stalkee_name" class="py-5 bg-white focus:outline-none focus:shadow-outline border border-gray-300 rounded-lg py-2 px-4 block w-full appearance-none leading-normal" type="text" placeholder="TolulopeFaleye" id = "github-username">
                    <div class="text-red-700" v-if="$page.errors.stalkee_name">{{ $page.errors.stalkee_name[0] }}</div>
                    <input type = "submit"  class = "transition ease-in-out duration-500 transform hover:-translate-y-1 hover:scale-110 w-full cursor-pointer bg-blue-500 hover:bg-blue-700 text-white pt-2 mt-3 cursor-auto font-bold py-2 px-4 rounded" value = "Stalk">
                </form>

            </div>

        </div>

    </div>
</template>

<script>
export default {
name: "StalkForm",
    data() {
        return {
            form: {
                stalkee_name:null,
            }
        }
    },
    methods: {
    submit() {
        this.$inertia.post('/stalk', this.form)
    }
    }

}
</script>

<style scoped>

</style>
