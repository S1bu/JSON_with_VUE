<template>
  <div>
    <h1>Welcome to the server</h1>
  </div>

  <div id="show">
    
  </div>
</template>

<script>
async function getData() {
    let data = await fetch("https://s1bu.github.io/JSON.SERVER_SIBU/people.json")
    let peopleData = await data.json()
    let extractedData = peopleData.students
    let display = document.querySelector("#show")
    extractedData.forEach(person => {
        display.innerHTML +=`
  
        <div class="card-body">
            <h4 class="card-title">${person.first_name}</h4>
            <h6 class="card-title">${person.last_name}</h6>
            <h6 class="card-title">${person.email}</h6>
        </div>
 
        `
    })
}
getData()
</script>

<style scoped>
.card-body{
  width: 40%;
  border: 1px solid black;
  background-color: blue;
  padding: 40px;
}
</style>
 