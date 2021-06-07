<template>
  <form>
    <input type="text"
           class="form-control my-2"
           placeholder="Ingrese Nombre"
           v-model="tarea.nombre"> 
  </form>
  <!--Boton de JavaScript-->
  <div class="form-check form-check-inline">
    <input class="form-check-input" type="checkbox" id="check-1" v-model="tarea.categorias" value="JavaScript">
    <label class="form-check-label" for="check-1">JavaScript</label>
  </div>

  <!--Boton de NodeJS-->
  <div class="form-check form-check-inline">
    <input class="form-check-input" type="checkbox" id="check-1" v-model="tarea.categorias" value="NodeJS">
    <label class="form-check-label" for="check-1">NodeJS</label>
  </div>

  <!--RADIO BUTTON-->
  <div class="mt-2">

  <!--Boton 1 clase No.81-->
  <div class="form-check form-check-inline">
    <input class="form-check-input" type="radio" id="radio-1" value="urgente" v-model="tarea.estado"> <!--Con ayuda del v-model podemos crear un modelo de datos bidireccional-->
    <label  class="form-check-label" for="radio-1">Urgente</label>
  </div>
  <!--Boton 2 -->
  <div class="form-check form-check-inline">
    <input class="form-check-input" type="radio" id="radio-2" value="relax" v-model="tarea.estado">
    <label  class="form-check-label" for="radio-2">Normal</label>
  </div>
  
  </div> 

  <!--Number clase No.82-->
  <div>
  <input class="form-control" type="number" v-model.number="tarea.numero"> <!--Con ayuda del v-model.number podemos forzar a que nuestro dato sea de tipo number-->

  </div>

  <p>{{tarea}}</p>
</template>

<script>



export default {
  name: 'Home',
  components: {
    
  }, 
  data(){ 
    return{ 
      tarea:{ 
        nombre:'', 
        categorias: [], 
        estado: '', 
        numero: 0
      }
    }
  }
}
</script>
