<template>
    <section class="h-[100svh] overflow-x-hidden bg-dra-background text-slate-200">
        <div class="mx-auto flex h-full max-w-md flex-col">
            <div @click="openPlayer" :class="[playlistOpen ? 'flex-row pl-4' : 'grow flex-col justify-center']" class="flex h-16 items-center gap-y-4 gap-x-4 overflow-hidden delay-100 duration-300 ease-in-out">
                <img class="duration-150 ease-in-out" :width="[playlistOpen ? '40' : '300']" src="https://images.template.net/wp-content/uploads/2016/05/17050744/DJ-Album-Cover-Template-Sample.jpg" alt="" />
                <div class="">
                    <ul :class="[playlistOpen ? 'gap-x-px' : 'gap-x-4']" class="flex items-center">
                        <li>
                            <button @click=""><Icon icon="mdi:skip-previous" :class="[playlistOpen ? 'h-6' : 'h-12']" width="50" /></button>
                        </li>
                        <li>
                            <button @click=""><Icon icon="mdi:play" :class="[playlistOpen ? 'h-6' : 'h-12']" width="50" /></button>
                        </li>
                        <li>
                            <button @click=""><Icon icon="mdi:skip-next" :class="[playlistOpen ? 'h-6' : 'h-12']" width="50" /></button>
                        </li>
                    </ul>
                </div>
            </div>
            <div @click="openPlaylist" :class="[playlistOpen ? 'grow' : '']" class="h-12 delay-100 duration-300 ease-in-out">playlist</div>
        </div>
    </section>
</template>

<script>
    import { Icon } from "@iconify/vue";
    export default {
        components: { Icon },
        data() {
            return {
                playlistOpen: false,
            };
        },
        methods: {
            openPlaylist() {
                this.playlistOpen = true;
            },
            openPlayer() {
                this.playlistOpen = false;
            },
        },
    };
</script>

<!-- <div class="grid justify-items-center gap-y-10">
            <img class="rounded-lg" width="300" src="https://images.template.net/wp-content/uploads/2016/05/17050744/DJ-Album-Cover-Template-Sample.jpg" alt="" />

            <div class="flex flex-col">
                <text>judul</text>
                <text>artis</text>
            </div>
            <input type="range" name="" id="" />
            <ul class="flex items-center gap-x-6">
                <li>
                    <button @click=""><Icon icon="mdi:skip-previous" width="40" /></button>
                </li>
                <li>
                    <button @click=""><Icon icon="mdi:play" width="60" /></button>
                </li>
                <li>
                    <button @click=""><Icon icon="mdi:skip-next" width="40" /></button>
                </li>
            </ul>
        </div> -->
<!-- <div class="">
        </div>
        <div class="">
            <ul class="flex gap-x-6">
                <li>
                    <button @click=""><Icon icon="mdi:skip-previous" width="70" /></button>
                </li>
                <li>
                    <button @click=""><Icon icon="mdi:play" width="70" /></button>
                </li>
                <li>
                    <button @click=""><Icon icon="mdi:skip-next" width="70" /></button>
                </li>
            </ul>
        </div> -->
