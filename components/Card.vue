<template>
<div>
    <h1>𨳒你老母</h1>
    <h2>Diu nei lo mo</h2>
    <div>
        <b-button @click="playSound">play</b-button>
    </div>
</div>
</template>

<script>
import {
    Howl,
    Howler
} from 'howler';




export default {
    data(){
        return {
            audio: null
        }
    },
    methods: {
        pronounce() {
            console.log("pronouncing...")
        },

        playSound() {

            this.audio = new Howl({
                src: [require('~/assets/sounds/01.mp3')],
                rate: 1.0,
                onend: function() {
                    this.playing = false
                }
            });

            // Play the sound.
            this.audio.play();
            console.log('done')

            

        }
    }
}
</script>
