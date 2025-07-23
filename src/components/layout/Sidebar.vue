<template>
	<div class="sidebar-page">
		<section class="sidebar-layout">
			<o-sidebar
			  id="sidebar"
			  position="static"
			  :animate="animate"
			  :mobile="mobile"
			  :expand-on-hover="expandOnHover"
			  :reduce="reduce"
			  open>
				<router-link class="clipped-bottom-right" to="/status">
					<img src="/icons/orbital.svg" />
					<span>상태</span>
				</router-link>
				<router-link class="clipped-bottom-right" to="/pilots">
					<img src="/icons/pilot.svg" />
					<span>파일럿</span>
				</router-link>
				<router-link class="clipped-bottom-right" to="/events">
					<img src="/icons/events.svg" />
					<span>로그</span>
				</router-link>
			</o-sidebar>
		</section>
	</div>
</template>

<script>
export default {
	props: {
		animate: {
			type: Boolean,
			required: true,
		},
	},
	data() {
		return {
			expandOnHover: false,
			mobile: "reduced",
			reduce: false,
		};
	},
};
</script>

<!-- <style></style> -->
