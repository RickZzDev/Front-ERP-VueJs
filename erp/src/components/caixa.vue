<template>
  <div class="container col-xl-5 py-4">
      <div class="row px-5">
          <h5>Nome</h5>
          <input type="text" id="nome"   class="form-control"  aria-describedby="emailHelp" placeholder="Nome">
      </div>
      <div class="row px-5 mt-3">
          <h5>CNPJ</h5>
          <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Cnpj">
      </div>
      <div class="row px-5 mt-3">
          <h5>Senha</h5>
          <input type="email" class="form-control" id="senha" aria-describedby="emailHelp" placeholder="Senha">
      </div>
      <div class="row px-5">
          <button type="button" v-on:click='getEmpresas()' class="btn btn-primary mt-3 ml-auto">Primary</button>
      </div>
   </div>
</template>

<script>



export default {
    name:'caixa',
    methods:{

         getEmpresas(){
             let nome = document.getElementById('nome').value;
             let senha =  document.getElementById('senha').value
             const dadosRegistro = {
                nome: nome,
                senha:senha                
             }


            let url = ('http://127.0.0.1:8000/empresas/')

            fetch(url, {
                method: 'POST',
                headers: {
                    'Accept': 'application/json',
                    'Content-Type': 'application/json'
                },
                body: JSON.stringify({
                    nome: nome,
                    senha:senha  
                })
            }).then(resposta=>resposta.json()).then(data=>console.log(data));

            
            console.log(dadosRegistro)
            
        }

        
    }
}

 
</script>

<style scoped>
   

    .container{
        background-color: rgb(221, 218, 218);
        border-radius: 10px;
    }
</style>