<template>
    <div>
        <div class="p-6 sm:px-20 bg-white border-b border-gray-200">
            <div>
                <jet-application-logo class="block h-12 w-auto" />
            </div>

            <div class="mt-8 text-2xl">
                Welcome to stalkee!
            </div>

            <div class="mt-6 text-gray-500">
                Stalkee is a platform that helps people to stalk each other... You might just want to know what your ex is doing...
                It helps you to achieve that.
            </div>
            <div class="mt-6">
                <inertia-link  href = "/stalk" class="bg-green-500 hover:bg-green-700 text-white py-4 px-5 rounded font-bold">Start stalking 😄😄😄</inertia-link>
            </div>
        </div>

    </div>
</template>

<script>
    import JetApplicationLogo from './../Jetstream/ApplicationLogo'

    export default {
        components: {
            JetApplicationLogo,
        },
    }
</script>
