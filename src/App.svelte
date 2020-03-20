<script>
	import Router from 'svelte-spa-router'
	import Home from './pages/home.svelte'
	import About from './pages/about.svelte'
	import Booking from './pages/booking.svelte'
	import Faq from './pages/faq.svelte'
	import NotFound from './pages/notFound.svelte'
	import Nav from './comps/nav.svelte'	
	import Footer from './comps/footer.svelte'	

	const routes = {
		'/': Home,
		'/home': Home,
		'/about': About,
		'/booking': Booking,
		'/faq': Faq,
		'*': NotFound
	}

</script>

<Nav />
<Router {routes} />
<Footer />