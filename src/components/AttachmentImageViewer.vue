<template>
	<Modal
		:size="isMobile ? 'full' : 'large'"
		@close="$emit('close')">
		<img
			:src="url"
			class="modal__attachment">
	</Modal>
</template>

<script>
import Modal from '@nextcloud/vue/dist/Components/Modal'
import isMobile from '@nextcloud/vue/dist/Mixins/isMobile'
export default {
	name: 'AttachmentImageViewer',
	components: {
		Modal,
	},

	mixins: [isMobile],

	props: {
		url: {
			type: String,
			required: true,
		},
	},
}
</script>
<style scoped />
