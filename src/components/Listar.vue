<template>
   <div class="card col-md-10 ms-auto me-auto mt-3">
    <div class="card-header">
      <h3>Empleados</h3>
    </div>
    <div class="card-body">
      <table class="table table-bordered border-dark">
                <thead class="table-dark">
                    <tr>
                        <th>Id</th>
                        <th>Nombre</th>
                        <th>Correo</th>
                        <th>Acciones</th>
                    </tr>
                </thead>
                <tbody class="border-dark">
                    <tr v-for="varvue in empleados" :key="varvue.id">
                       <td scope="row">{{ varvue.id }}</td>
                       <td>{{ varvue.nombre }}</td>
                       <td>{{ varvue.correo }}</td>
                       <td><button class="btn btn-primary">Editar</button> |
                       <button class="btn btn-danger">Borrar</button></td>
                    </tr>
                </tbody>
      </table>
    </div>
  </div>       

 
</template>

<script>
export default {

   data(){
     return {
          empleados:[]     
     }
   },        

   created:function(){
          this.consultarDatos();
   },
   methods: {
        consultarDatos(){
                  fetch('http://localhost:8080/vue/')
                  .then(respuesta=>respuesta.json())
                  .then((datosDeRespuesta)=>{
                            console.log(datosDeRespuesta)
                            this.empleados=[]
                            if(typeof datosDeRespuesta[0].success === 'undefined'){
                              this.empleados = datosDeRespuesta;      
                            }
                  } ).catch(console.log)
        }     
   }    
}
</script>