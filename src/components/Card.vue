<template>
    <div class="w-full md:w-1/2 lg:w-1/3 xl:w-1/4 mt-4">
        <div class="ml-12">
            <div class="relative pb-4/5 bg-white rounded-lg overflow-hidden border">
                <img class="absolute h-full w-full object-cover shadow-md" :src='character.image' alt="Emma watson">
            </div>
            <div class="relative p-6 bg-teal-200 rounded-lg mx-3 -mt-10 shadow-lg">
                <div class="text-gray-600 uppercase mt-2 text-sm font-semibold">
                    <div class="flex items-center">
                        <span class="text-xs text-teal-700 bg-teal-300 px-3 py-1 rounded-full">{{ character.status }}</span>
                        <span class="ml-2">{{ character.species }} / {{ character.gender }}</span>
                    </div>
                </div>
                <div>
                    <h3 class='font-semibold text-xl mt-1 truncate'>
                        {{ character.name }}
                    </h3>
                </div>
                <div class="mt-2">
                    <span class="block text-sm text-gray-800 font-bold truncate">{{ character.location.name }}$</span>
                </div>
                <div class="mt-4 text-lg text-teal-400 font-bold flex items-center">
                    <span class="">{{  }}/5 stars </span><span class='text-sm text-gray-600 ml-2'> 43 reviews</span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['data'],
    data() {
        return {
            character: this.data
        }
    },
    created() {

    },
}
</script>