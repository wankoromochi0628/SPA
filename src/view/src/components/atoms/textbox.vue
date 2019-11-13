<template>
    <div class="field">
        <div class="control">
            {{postSentence}}
            <textarea v-model="sentence" class="textarea is-primary" placeholder=""></textarea>
        </div>
    </div>
</template>

<script>
    export default {
        name: "TextForm",
        props: {
            postSentence: {
                type: String,
                description: "入力項目"
            }
        },
        computed: {
            sentence: {
                get() {
                    return this.postSentence;
                },
                set(newSentence) {
                    this.$emit('writtenSentence', newSentence);
                }
            }
        }
    };
</script>