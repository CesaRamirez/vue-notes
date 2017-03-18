<template lang="html">
    <div class="sidebar">
        <div v-if="notes.length">
            <note v-for="note in notes" v-bind:note="note" :key="note.id"></note>
        </div>
        <div class="sidebar__content" v-else>
            Boo, no notes. Get writing!
        </div>
    </div>
</template>

<script>
import Note from './Note'
import { mapGetters } from 'vuex'

export default {
  computed: {
    ...mapGetters([
      'notes'
    ])
  },
  components: {
    Note
  }
}
</script>

<style lang="scss" scoped>
    .sidebar {
        background-color: #f9f9f9;
        flex: 1;
        height: 100%;
        min-width: 28%;
        border-right: 2px solid #eee;
        overflow-y: scroll;

        &__content {
            padding: 30px;

            a {
                text-decoration: none;
                color: inherit;
            }
        }
    }
</style>
