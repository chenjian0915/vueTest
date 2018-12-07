<template>
	<div>
		<h3>{{ itemData.title }}</h3>
	    <ul>
	      <li v-for="itemBtn in itemData.buttons"><a :href="itemBtn.url" target="_blank" rel="noopener">{{itemBtn.text}}</a></li>
	    </ul>
	</div>
</template>

<script>
	export default {
		name: 'ListItem',
		props: {
			itemData: Object
		}
	}
</script>

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