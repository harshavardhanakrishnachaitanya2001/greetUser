<script>
	let name='';
	let displayName;
	function handleChange(e){
		e.preventDefault();
		name=e.target.value;
	}
	function handleClick(){
		 displayName=name;
		 name='';
	}
</script>

<div class='main'>
	<h1>Welcome user website</h1>
	<input type='text' on:change={handleChange} value={name} placeholder='Name of visitor' required />
	<button on:click={handleClick}>Greet</button>
	<p class='displayData'>{displayName?'Welcome ' + displayName:''}</p>
</div>

<style>
	input{
		text-align: center;
	}
	.main{
		text-align: center;
	}
	button{
		cursor:pointer;
	}
	h1 {
		font-size: 4rem;
		font-weight: bolder;
	}
	.displayData{
		font-weight: bold;
	}
</style>