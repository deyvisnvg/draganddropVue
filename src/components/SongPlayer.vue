<script>
import { useDragAndDrop } from "@formkit/drag-and-drop/vue";
import { animations } from "@formkit/drag-and-drop";

export default {
    name: 'SongPlayer',
    props: {
        dataSong: Array
    },
    setup(props) {
        const [parent, tapes] = useDragAndDrop(props.dataSong, {
            plugins: [
                animations()]
        });
        return {
            parent,
            tapes
        }
    }
}
</script>

<template>
    <div class="grid gap-3 grid-cols-3 items-center p-10" ref="parent">
        <article v-for="song in tapes" :key="song"
            class="bg-black p-5 text-white border-4 rounded-lg border-yellow-500">
                <p> {{ song.name }} </p>
                <p> {{ song.artist }} </p>
                <p> {{ song.year }} </p>
        </article>
    </div>
</template>