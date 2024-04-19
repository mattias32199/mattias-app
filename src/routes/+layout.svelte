<script>
    import Navbar from '$lib/components/NavBar.svelte';
</script>

<!-- <svelte:body use:cssVariables={{ background: '#0a0908' }} /> -->

<!-- Navbar component, passing the current page's pathname as a prop. -->
<Navbar/>

<!-- Where the child components go e.g. +page.svelte -->
<slot />

<style>
    * {
	    box-sizing: border-box;
    }

    @font-face {
        font-family: 'Fira Code', monospace;
        font-display: optional; /* Allows the browser to use a fallback font until 'Fira Code' is downloaded */
        src: url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;600;700&display=swap');
    }

    :global(#svelte) {
		width: 100vw;
		height: 100%;
		max-width: 900px;

		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}

    :global(html),

    /* layout and font styling */
	:global(body) {
		transition: background-color 0.2s ease 0s;
		position: relative;
		width: 100%;
		height: 100%;
		overflow: auto;
		font-family: 'Fira Code', monospace;
		background-color: #0a0908;
	}

    /* color, margin, additional layout properties */
    :global(body) {
		background-color: var(--background);
		background-size: 200% 200%;
		color: white;
		margin: 0;
		box-sizing: border-box;
		display: grid;
		line-height: 1.75;
		place-items: center;
		height: 100%;
		overflow-x: hidden;
	}

    :global(h1) {
		border: 0;
	}

    :global(::selection) {
		color: white;
		background: #ca3c25;
	}

    :global(::-webkit-scrollbar) {
		width: 8px;
		height: 8px;
		border-radius: 1px;
	}

    :global(::-webkit-scrollbar-thumb) {
		background-color: #fafffd;
		border-radius: 3px;
	}

    :global(::-webkit-scrollbar-track) {
		background-color: transparent;
		border-radius: 1px;
	}

    @media (min-width: 900px) {
		:global(body) {
			padding: 0 100px;
		}
	}

    :global(a) {
		text-decoration: none;
	}

    /* Styles for anchor tags, setting color and removing text-decoration */
    a {
        color: rgb(0, 100, 200);
        text-decoration: none;
    }

    /* Adds underline to anchor tags on hover */
    a:hover {
	    text-decoration: underline;
    }

    /* Styles for visited anchor tags, changing the color */
    a:visited {
	    color: rgb(0, 80, 160);
    }

    /* Styles for the footer, setting font properties, layout, and alignment */
    footer {
        font-size: 16px;
        font-weight: 400;
        padding: 30px 0;
        max-width: 900px;
        text-align: center;
        width: 100%;
    }

    /* Styles for anchor tags inside the footer, setting color and removing text-decoration */
    footer a {
	    text-decoration: none;
	    color: #4158d0;
    }

    /* Styles for elements with the .svelte class inside the footer, changing the color */
    footer .svelte {
	    olor: #ff3e00;
    }

    /* Styles for elements with the .me class inside the footer, changing the color */
    footer .me {
	    color: #ff3e00;
    }

    /* Media query that makes .tooltip elements visible on wider screens */
    @media (min-width: 900px) {
        :global(.tooltip) {
            visibility: visible;
        }
    }

</style>