<script setup>
import { ref } from 'vue'
 let number=ref(5);

 function add(){
    number.value++;
    
 }
 function remove(){
    
    if(number.value > 0){
        number.value--
    }

 }
</script>
 <template>
    <div class="max-w-96 bg-blue-200 rounded-lg py-3 px-6 mx-auto">
        <div class="max-w-5 bg-red-400 rounded-full py-3 px-6 mx-auto flex items-center justify-center " v-if="number > 0">
        {{ number }}
        
        </div>
        <div v-else> 
            nadie te escribe :/
        </div>
        

      <div class="flex ">
        <div class="max-w-5 bg-blue-400 rounded-full py-3 px-6 mx-auto flex items-center justify-center hover:cursor-pointer" @click="add()">
            +
        </div>
        <div class="max-w-10 bg-blue-400 rounded-full py-3 px-6 mx-auto  flex items-center justify-center hover:cursor-pointer " @click="remove()">
            -
        </div>
      </div>

    </div>
 </template>