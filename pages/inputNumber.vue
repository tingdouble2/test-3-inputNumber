<template>
  <v-container class="content">
    <v-row>
      <v-col cols="12" sm="6" md="6">
        <v-text-field
          v-model="input"
          label="ข้อมูล"
          outlined
          dense
        />
      </v-col>
      <v-col>
        <Calculate :answer="result" @Oncalculate="calculate" />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>

export default {
  data () {
    return {
      input: '',
      result: null
    }
  },
  methods: {
    calculate () {
      const changeinput = Number(this.input)
      this.result = changeinput / 100
    }
  }
}
</script>
<style>
.content {
  position: relative;
  background-color: #ffffff;
  box-shadow: 0 0.125rem 0.25rem rgba(0, 0, 0, 0.075);
  border-radius: 3px;
  padding: 50px;
}
</style>
