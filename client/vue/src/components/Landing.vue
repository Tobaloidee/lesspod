<template>
	<section class="section">

		<div class="hero-body">
			<div class="container has-text-centered">
				<div class="columns is-vcentered">
					<div class="column is-5">
						<figure class="image is-4by3">
							<img src="./../assets/images/serverless.png" alt="Description">
						</figure><br>
						<h6 class="title is-6" style="font-weight: 300;">Image credits: Hackernoon</h6>
					</div>
					<div class="column is-6 is-offset-1">
						<h1 class="title is-2">
							Serverless Blogging Engine
						</h1>
						<h2 class="subtitle is-4"><br>
							Lesspod lets build and deploy personal website+blog to Firebase. Key benefits are listed below.
						</h2>
						<!-- <div class="content"> -->
							<ul style="font-size: 1.3rem;">
								<li>No fixed recurring hosting fees.</li>
								<li>Infinite scalability of the cloud.</li>
								<li>Free hosting till you're very popular!</li>
							</ul>
						<!-- </div> -->
						<br>
						<p class="has-text-centered">
							<a href="https://github.com/Rajan/lesspod" target="_blank" class="button is-medium is-success is-outlined">
								Lesspod on Github
							</a>
						</p>
					</div>
				</div>
			</div>
		</div>

		<div class="hero-foot">
			<div class="container">
				<div class="is-centered">
					<div class="column has-text-centered" style="font-size:1.5rem;">
						<a href="/login">Login</a> Or <a href="/register">Create Account</a>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>
<script type="text/javascript">
module.exports = {
	data(){
		return {}
	},
	beforeMount: function(){

		// auto login if credentials are present

		if(Cookies.get('token').length > 0){
			this.$router.push('/home');
		}
	}
};
</script>