<template>
	<div>
		<the-header></the-header>
		<!-- <TheHeader /> -->
		<badge-list></badge-list>
		<user-info
			:full-name="activeUser.name"
			:info-text="activeUser.description"
			:role="activeUser.role"
		></user-info>
		<course-goals #default="slotProps">
			<!-- here we don't need template because we have only default slot -->
			<!-- slotProps contains all the props we passed from CourseGoals -->
			<h2>{{ slotProps.item }}</h2>
			<p>{{ slotProps["another-prop"] }}</p>
		</course-goals>
	</div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
import BadgeList from "./components/BadgeList.vue";
import UserInfo from "./components/UserInfo.vue";
import CourseGoals from "./components/CourseGoals.vue";

export default {
	components: {
		// 'the-header': TheHeader, =====>
		// TheHeader: TheHeader, ====>
		TheHeader,
		BadgeList,
		UserInfo,
		CourseGoals,
	},
	data() {
		return {
			activeUser: {
				name: "Nikola Bogicevic",
				description: "Site owner and admin",
				role: "admin",
			},
		};
	},
};
</script>

<style>
html {
	font-family: sans-serif;
}

body {
	margin: 0;
}
</style>