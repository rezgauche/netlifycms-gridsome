<template>
	<div class="author">
		
		<h1>
		Welcome to
    		<strong class="bg-clip-text text-transparent bg-gradient-to-r from-blue-500 to-purple-500">
      		{{$static.metadata.siteName}}
    		</strong>
  		</h1>

		<h1 v-if="showTitle" class="author__site-title">
			{{ $static.metadata.siteName }}
		</h1>

		<p class="author__intro">
			rezgauche.be is responsive to a need for an immediate representation of artists, balancing responsibility with decentralised organisation.
		</p>

		<p class="author__links">
			<a href="https://www.3xr.space/store/rezgauche.mintbase1.near">gallery</a>
			<a href="https://www.instagram.com/rezgauche/">insta</a>
			<a href="https://reverent-noether-6cff94.netlify.app/item-01">01</a>
		</p>

	</div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
	props: ['showTitle']
}
</script>

<style lang="scss">
.author {
	margin: 0 auto;
	max-width: 500px;
	text-align: center;
	padding-bottom: calc(var(--space) / 2);
	bg-clip-text text-transparent bg-gradient-to-r from-blue-500 to-purple-500;

	&__image {
		border-radius: 100%;
		width: 90px;
		height: 90px;
		margin-bottom: 1em;
	}

	&__intro {
		opacity: .8;
	}

	&__site-title {
		margin: 0 auto;
		font-size: 1.5em;
		max-width: 400px;
	}

	&__links {
		margin-top: -.5em;
		a {
			margin: 0 .5em;
		}
	}
}
</style>
