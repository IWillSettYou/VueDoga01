<script>
export default{
    props: ['name', 'ingredients', 'time', 'desc'],
    setup(props){
        console.log(props.title)
    },
       methods: {
        set(){
            this.name = name,
            this.ingredients = ingredients,
            this.time = time,
            this.desc = desc
        }
    }
    
}

</script>
<template>
    <div>
        <div class="flex flex-col gap-1 float right">

            <span>Name: {{ name }} </span>
            <span>Ingredients: {{ ingredients }} </span>
            <span>Required time: {{ time }}</span>
            <span>Description: {{ desc }}</span>
        </div>
    </div>
</template>