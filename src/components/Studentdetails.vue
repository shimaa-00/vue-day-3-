<template>
  <div class="text-center bg-info p-3 fw-bold mb-3" style="font-size: 30px">
    student details
  </div>
  <template>{{ loadStudentData($route.params.id) }}</template>
  <div class="text-center bg-light p-3 fw-bold">
    <p>ID: {{ stdid }}</p>
    <p>Name: {{ stdname }}</p>
    <p>City: {{ stdcity }}</p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      stdid: "",
      stdname: "",
      stdcity: "",
    };
  },
  methods: {
    async loadStudentData(_id) {
      const resp = await fetch(`http://localhost:5000/students/${_id}`);
      let obj = await resp.json;
      this.stdid = obj.id;
      this.stdname = obj.name;
      this.stdcity = obj.city;
    },
  },
};
</script>
