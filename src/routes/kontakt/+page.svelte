<script>
	const CONTACT = {
		name: 'Lauras Digitalaufklärung',
		tel: {
			href: 'tel:0049812140595',
			text: '08121 405 95'
		},
		email: 'laura@digauf.de',
		address: 'Lange Str. 6, 9420 Dahoam',
		googleMapsUrl: 'https://www.google.com/maps/search/?api=1@query=Lauras+Digitalaufklärung+Dahoam'
	};
	const { name, tel, email, address, googleMapsUrl } = CONTACT;
</script>

<svelte:head>
	<title>Kontakt</title>
	<meta name="description" content="{tel.text} // {email} // {address}" />
</svelte:head>

<h2>Kontakt</h2>
<p>{name}</p>
<div class="address">
	<p>{address}</p>
	<a href={googleMapsUrl} class="google-maps" title={`${name} auf Google Maps`} target="_blank"
		>Google Maps</a
	>
</div>
<table>
	<tbody>
		<tr>
			<td>Tel.</td>
			<td>
				<a href={tel.href} title="Telefonnummer"> {tel.text}</a>
			</td>
		</tr>
		<tr>
			<td>E-Mail</td>
			<td>
				<a href={`mailto:${email}`} title="Email-Adresse">{email}</a>
			</td>
		</tr>
	</tbody>
</table>
