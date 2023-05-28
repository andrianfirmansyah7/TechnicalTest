<template>
<h1>Soal Nomer 3</h1>
  <div class="wrapper">
    <div>
    <div class="form">
      <a href="#" @click="add" class="btn btn-primary" style="margin-bottom:10px"><i class="fa fa-plus"></i> Tambah</a>
      <!-- Melakukan proses perulangan berdasarkan angka pada variabel jumlah -->
      <div v-for="key in jumlah" :key="key">
      <div class="row" style="margin-bottom:10px">
      <div class="col-5">
      <select v-model="values['dynamic-field-'+key]" :id="key" class="form-control">
       <option default>Age</option>
       <option>Education</option>
       <option>Interest</option>
       <option>Language</option>
       <option>Marital Status</option>
       <option>Skill</option>
      </select>
      </div>
      <div class="col-5">
        <input type="text" :id="key" class="form-control" placeholder="Isian">
      </div>
      <div class="col-2">
        <a href="#" @click="remove" class="btn btn-danger"><i class="fa fa-plus"></i> X</a>
      </div>
      </div>
      </div>
    </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data: function () {
    return {
      jumlah: 1,
     values: {}

    }
  },
   methods: {
   // Fungsi penambahan jumlah
    add: function(){
      this.jumlah++;
    },
    // Fungsi pengurangan jumlah
    remove: function () {
     this.jumlah--;

    }
    }
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


body {
  background-color: #f0f5ff;
  color: #fff;
}

.form {
  width: 450px;
  margin: 15px auto;
}

h1 {
  text-align: center;
  font-size: 48px;
  color: #232c3d;
}
</style>
