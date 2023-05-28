<script>
const employees = [
    { "nik":"1", "name":"ABIYYU" },
    { "nik":"2", "name":"ADHIKA" },
    { "nik":"3", "name":"AFRIE" },
    { "nik":"4", "name":"ALAM"}
    ];

const selected_employees = [
    { "nik": "1", "name": "ABIYYU" },
    { "nik": "2","name":"ADHIKA"}
    ];

const unselected_employees = [];

  export default {
  el: '#',
  data() {
    this.employees = employees;
    this.selected_employees = selected_employees;
    this.unselected_employees = unselected_employees;
  },
  method : {
    show : function(){
      for (let i = 0; i < this.employees.length; i++){
        // Melakukan perbandingan
        if(this.employees[i]["nik"] != this.selected_employees){
          //Proses input data karyawan tidak terpilih ke dalam array
          this.unselected.employees.push(this.employees[i]);
        }
      }
      return this.unselected_employee;
    }
  }
}
</script>

<template>
  <h1 id="data">{{ show() }}</h1>
</template>
