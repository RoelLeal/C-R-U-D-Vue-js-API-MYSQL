<template>
   <div class="container col-lg-6 mt-4">
      <div class="card">
        <div class="card-header">
          <h4><strong>Empleados</strong></h4>      
        </div>
        <div class="card-body col-md-7 container">
          <form>
            <div class="form-group">
              <h5>Nombre</h5>
              <input type="text" class="form-control" name="nombre" id="nombre" placeholder="Nombre">
            </div>
            <br>
            <div class="form-group">            
              <h5>Correo electronico</h5>
              <input type="email" class="form-control" name="correo" id="correo" placeholder="nombre@gmail.com">          
            </div>
            <br>
            <div class="btn-group" role="group" aria-label="">
              <button type="button" class="btn btn-success">Agregar</button>
              <button type="button" class="btn btn-dark">Cancelar</button>
            </div>
            <br> 
          </form>      
        </div>
      </div>       
   </div>       
</template>