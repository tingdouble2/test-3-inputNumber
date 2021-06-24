<template>
  <v-container>
    <div class="box">
      <v-row>
        <v-col cols="12" md="6">
          <v-btn
            class="btn-cal"
            color="red"
            @click="$emit('Oncalculate')"
          >
            CALCULATE
          </v-btn>
        </v-col>
        <v-col md="12">
          <v-text-field
            v-model="listJson"
            class="answer"
            label="ผลลัพธ์"
            outlined
            dense
          />
        </v-col>
      </v-row>
    </div>
  </v-container>
</template>

<script>
export default {
  name: 'Calculate',
  props: {
    answer: {
      type: Number,
      default: Number
    }
  },
  computed: {
    listJson () {
      return JSON.parse(this.answer)
    }
  }
}
</script>

<style>
.box{
  padding-bottom: 10px;
}

.btn-cal {
  position: relative;
  top: -10px
}

.answer {
  position: absolute;
  left: 50px;
}
</style>
