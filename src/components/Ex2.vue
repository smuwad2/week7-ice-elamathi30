<script>

    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter']
            }
        },
        
            newitem:'', 
            
        methods:{
            addItem(){
                this.items.push(this.newitem)
       }
        }
        
       
    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
   <ul>
        <li v-for="(item,idx) in items">
            <!-- need to know the index to remove the element -->
        {{ item }}
        <button @click="items.splice(idx,1)">Delete!</button>
        </li>

   </ul>
   <input type="text" v-model="newitem"> 
   <!-- not id use v-model -->
   </input>
   <button @click="addItem">Add!</button>
</template>
