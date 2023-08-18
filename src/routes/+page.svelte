<script>
	import P5 from 'p5-svelte';
	let windowWidth = window.innerWidth;
	let windowHeight = window.innerHeight;
	// @ts-ignore
	const sketch = (p5) => {
		// @ts-ignore
		let img = p5.loadImage(
			'https://images.unsplash.com/photo-1633837018163-3d3f09dec30d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxjb2xsZWN0aW9uLXBhZ2V8MXw0NTU5MTI3M3x8ZW58MHx8fHx8&w=1000&q=80'
		);

		p5.setup = () => {
			p5.createCanvas(windowWidth, windowHeight);
			p5.noStroke();
			p5.max_distance = p5.dist(0, 0, p5.width, p5.height);
		};

		p5.draw = () => {
			p5.background(img);
			p5.fill(0, 0, 255);
			for (let i = 0; i <= p5.width; i += 20) {
				for (let j = 0; j <= p5.height; j += 20) {
					let size = p5.dist(p5.mouseX, p5.mouseY, i, j);
					size = (size / p5.max_distance) * 66;
					p5.ellipse(i, j, size, size);
				}
			}
		};
	};
</script>

	<P5 {sketch} />


<style>
	.wrap {
		width: 100vw;
		height: 100vh;
		display: flex;
		justify-content: center;
		align-items: center;
	}
</style>
