<template>
	<section>
		<base-card>
			<template #headerSlot>
				<!-- v-slot:headerSlot  ======  #headerSlot -->
				<h3>{{ fullName }}</h3>
				<base-badge :type="role" :caption="role.toUpperCase()"></base-badge>
			</template>
			<template #default>
				<p>{{ infoText }}</p>
			</template>
		</base-card>
	</section>
</template>

<script>
export default {
	props: ["fullName", "infoText", "role"],
};
</script>