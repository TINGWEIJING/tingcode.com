<script>
	import '../styles/app.css';

	import ProfilePic from '$lib/assets/profile_pic.png';
	import LinkedinIcon from '$lib/assets/linkedin.svg';
	import GithubIcon from '$lib/assets/github-mark-white.svg';
	import MoneyLionIcon from '$lib/assets/moneylion.png';
</script>

<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Open+Sans" />

<div class="sized-name-card">
	<div class="sized-profile-img">
		<img class="profic-img" src={ProfilePic} alt="Avatar" />
	</div>
	<div class="sized-intro-paragraph">
		<p class="sentence-01">Hi, I am</p>
		<p class="sentence-02">Ting Wei Jing</p>
		<p class="sentence-03">Software Engineer at MoneyLion</p>
	</div>
	<div class="sized-links">
		<a href="https://www.linkedin.com/in/ting-wei-jing" target="_blank" rel="noopener noreferrer">
			<img class="link-icon" src={LinkedinIcon} alt="LinkedIn Icon" />
		</a>
		<a href="https://github.com/TINGWEIJING" target="_blank" rel="noopener noreferrer">
			<img class="link-icon" src={GithubIcon} alt="GitHub Icon" />
		</a>
	</div>
</div>
<div class="sized-project-gallery">
	<div class="project-box">
		<a
			class="project-link"
			href="https://tingweijing.github.io/MoneyLion-Tech-Talk-15-slide"
			target="_blank"
			rel="noopener noreferrer"
		>
			<div class="project-card">
				<img class="project-icon" src={MoneyLionIcon} alt="MoneyLion Icon" />
				<div class="project-description">
					<p class="project-title">
						<strong>MoneyLion Tech Talk #15</strong><br /><i
							>Optimizing Performance: Tackling Thread Pool Exhaustion to Reduce Backend Latency</i
						>
					</p>
				</div>
			</div>
		</a>
	</div>
	<div class="project-box">
		<a
			class="project-link"
			href="https://marketplace.visualstudio.com/items?itemName=tingcode.bread-jam"
			target="_blank"
			rel="noopener noreferrer"
		>
			<div class="project-card">
				<img
					class="project-icon"
					src="https://tingcode.gallerycdn.vsassets.io/extensions/tingcode/bread-jam/0.0.2/1717336190922/Microsoft.VisualStudio.Services.Icons.Default"
					alt="MoneyLion Icon"
				/>
				<div class="project-description">
					<p class="project-title">
						<strong>VS Code Bread Jam</strong><br /><i>A Visual Studio Code extension</i>
					</p>
				</div>
			</div>
		</a>
	</div>
</div>

<style>
	.sized-name-card {
		display: grid;
		grid-template-columns: repeat(12, 1fr);
		grid-template-rows: repeat(12, 1fr);

		aspect-ratio: 100 / 46;
		width: 100%;
		max-width: 1000px;
	}
	.sized-profile-img {
		grid-area: 1 / 1 / 10 / 5;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.sized-intro-paragraph {
		grid-area: 1 / 5 / 10 / 13;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;
		text-align: left;
		text-shadow: 3px 3px 5px #000000;
	}
	.sized-links {
		grid-area: 10 / 1 / 13 / 13;

		display: flex;
		flex-direction: row;
		justify-content: space-evenly;
		align-items: center;
	}
	.sized-project-gallery {
		display: flex;
		flex-direction: row;
		justify-content: space-evenly;
		align-items: stretch;
		padding-top: 20px;

		aspect-ratio: 600 / 100;
		width: 100%;
		max-width: 1000px;
	}

	.project-box {
		width: 46%;
		box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
		border-radius: 8px;
		background-color: rgb(56, 54, 54);
	}
	.project-link {
		display: block;
		height: 100%;
		width: 100%;
		text-decoration: none;
	}
	.project-card {
		display: grid;
		height: 100%;
		width: 100%;
		grid-template-columns: repeat(6, 1fr);
		grid-template-rows: repeat(1, 1fr);
	}
	.project-card > img {
		grid-column: 1/3;
	}
	.project-icon {
		object-fit: contain;
		aspect-ratio: 1/1;
		width: 80%;
		height: auto;
		margin: auto;
	}
	.project-description {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: start;
		height: 100%;
		grid-column: 3/7;
		color: aliceblue;
		padding-right: 20px;
	}
	.project-title {
		font-size: var(--size-20);
	}

	.profic-img {
		clip-path: circle();
		object-fit: contain;
		aspect-ratio: 1/1;
		width: var(--size-250);
		height: auto;
	}
	.sentence-01 {
		/* font-size: 2.8em; */
		font-size: var(--size-40);
	}
	.sentence-02 {
		/* font-size: 6.4em; */
		font-size: var(--size-100);
		font-weight: bold;
	}
	.sentence-03 {
		/* font-size: 2.5em; */
		font-size: var(--size-40);
	}
	.sized-links > a {
		height: 100%;
		width: auto;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.link-icon {
		object-fit: contain;
		aspect-ratio: 1/1;
		width: var(--size-100);
		height: auto;
	}

	@media only screen and (max-width: 499px) {
		.sized-name-card {
			aspect-ratio: 90 / 100;
		}
		.sized-profile-img {
			grid-area: 1 / 1 / 5 / 13;
		}
		.sized-intro-paragraph {
			grid-area: 5 / 1 / 10 / 13;
			align-items: center;
		}
		.sized-project-gallery {
			flex-direction: column;
			justify-content: center;
			align-items: center;
			aspect-ratio: unset;
			gap: 20px;
		}
		.project-box {
			width: 90%;
		}
		.project-description {
			padding: 10px;
			height: fit-content;
		}
		.project-title {
			font-size: var(--size-40);
		}
		.sentence-01 {
			font-size: var(--size-50);
		}
		.sentence-02 {
			font-size: var(--size-112);
		}
		.sentence-03 {
			font-size: var(--size-60);
		}
		.profic-img {
			width: 34%;
		}
		.link-icon {
			width: var(--size-150);
		}
	}

	@media only screen and (min-width: 1000px) {
		.project-title {
			font-size: 0.4em;
		}
		.profic-img {
			width: 84%;
		}
		.sentence-01 {
			font-size: 2.8em;
		}
		.sentence-02 {
			font-size: 6.4em;
		}
		.sentence-03 {
			font-size: 2.5em;
		}
		.link-icon {
			width: auto;
			height: 84%;
		}
	}
</style>
