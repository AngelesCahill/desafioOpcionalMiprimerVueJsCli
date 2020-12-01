<template>
<div class="main">
  <div class="container">
   <div class="row">
     <div class="col-12 col-sm-12 col-md-12 col-lg-12 col-xl-12">
         <table class="table table-hover">
            <thead>
              <tr>
                <th>#</th>
                <th>Nombre</th>
                <th>Apellido</th>
                <th>Rut</th>
                <th>Fecha de Nacimiento</th>
                <th>Edad</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="(item, index) in usuarios" :key="index">
                <th>{{item.id}}</th>
                <td>{{item.nombre}}</td>
                <td>{{item.apellido}}</td>
                <td>{{item.rut}}</td>
                <td>{{item.fechanacimiento}}</td>
                <td>{{item.edad}}</td>
              </tr>
            </tbody>
          </table>
     </div>
   </div>
 </div>
   
  <div class="container">
    <div class="row">
      <div class="col-12 col-sm-12 col-md-12 col-lg-12 col-xl-12">
          <form @submit="nuevoUsuario">
              <div class="form-group">
                <label for="nombre">Nombre</label>
                <input type="text" class="form-control" v-model="datosUsuario.nombre">
              </div>

              <div class="form-group">
                <label for="apellido">Apellido</label>
                <input type="text" class="form-control" v-model="datosUsuario.apellido">
              </div>

              <div class="form-group">
                <label for="rut">Rut</label>
                <input type="text" class="form-control" v-model="datosUsuario.rut">
              </div>

              <div class="form-group">
                <label for="fechanacimiento">fechanacimiento</label>
                <input type="text" class="form-control" v-model="datosUsuario.fechanacimiento">
              </div>

              <div class="form-group">
                <label for="edad">edad</label>
                <input type="number" class="form-control" v-model="datosUsuario.edad">
              </div>
              
              <button type="submit" class="btn btn-primary">Registrar</button>
            </form>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'Main',
  data(){
    return {
      datosUsuario: {
        id: '',
        nombre: '',
        apellido: '',
        rut: '',
        fechanacimiento: '',
        edad:''
      },
      
      usuarios: [
        {
          id: '1',
          nombre: 'Tremaine',
          apellido: 'Reynolds',
          rut: '12.098.345-0',
          fechanacimiento: '10-11-2010',
          edad:'10'
        },
        {
          id: '2',
          nombre: 'Erling',
          apellido: 'Durgan',
          rut: '10.900.321-k',
          fechanacimiento: '10-01-2000',
          edad:'20'
        },
        {
          id: '3',
          nombre: 'Gennaro',
          apellido: 'Runolfsson',
          rut: '5.890.123-1',
          fechanacimiento: '10-09-2006',
          edad:'14'
        }
      ]
    }
  },
  methods: {
    nuevoUsuario(){
      this.datosUsuario
    }
  },
  beforeMount: {
    
  }
  
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
