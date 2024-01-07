<script>
	import ProfilePic from '$lib/assets/profile_pic.png';
	import LinkedinIcon from '$lib/assets/linkedin.svg';
	import GithubIcon from '$lib/assets/github-mark-white.svg';
</script>

<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Open+Sans" />

<div id="parent">
	<div id="main-content">
		<div id="upper-content">
			<img id="profic-img" src={ProfilePic} alt="Avatar" />
			<div id="intro-paragraph">
				<p id="sentence-01">Hi, I am</p>
				<p id="sentence-02">Ting Wei Jing</p>
				<p id="sentence-03">Full Stack Software Engineer at MoneyLion</p>
			</div>
		</div>
		<div id="lower-content">
			<a
				href="https://www.linkedin.com/in/ting-wei-jing/"
				target="_blank"
				rel="noopener noreferrer"
			>
				<img id="linkedin-icon" src={LinkedinIcon} alt="LinkedIn Icon" />
			</a>
			<a href="https://github.com/TINGWEIJING" target="_blank" rel="noopener noreferrer">
				<img id="github-icon" src={GithubIcon} alt="GitHub Icon" />
			</a>
		</div>
	</div>
</div>

<style>
	p {
		margin: 0;
		text-align: left;
		color: whitesmoke;

		font-family: 'Open Sans', Arial, Helvetica, sans-serif;
		font-size: 48px;
	}
	#parent {
		padding: 0;
		margin: 0;
		width: 98vw;
		height: 98vh;
		position: relative;
	}

	#main-content {
		text-align: center;

		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);

		margin: 0 auto;
		min-height: 100px;
		height: 80vh;
		min-width: 100px;
		width: 80vw;

		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: stretch;
	}
	#upper-content {
		padding: 8px;
		display: flex;
		height: auto;
		flex-direction: row;
		justify-content: center;
		align-items: center;
	}
	#intro-paragraph {
		padding: 8px;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;
	}
	#sentence-01 {
		font-size: 2.4vw;
		text-shadow: 3px 3px 5px #000000;
	}
	#sentence-02 {
		font-size: 6vw;
		font-weight: bold;
		text-shadow: 3px 3px 5px #000000;
		line-height: 1.2;
	}
	#sentence-03 {
		font-size: 2vw;
		text-shadow: 3px 3px 5px #000000;
	}
	#lower-content {
		padding: 8px;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		gap: 0px 10vw;
	}
	#linkedin-icon,
	#github-icon {
		margin: 16px;
		height: 3vw;
		min-width: 10px;
		min-height: 10px;
		object-fit: contain;
	}
	#profic-img {
		margin: 16px;
		clip-path: circle();
		height: 11vw;
		min-width: 64px;
		min-height: 64px;
		object-fit: contain;
	}
	:global(body) {
		background-color: rgb(47, 47, 47);
	}
</style>
