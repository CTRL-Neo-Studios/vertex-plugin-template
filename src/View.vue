<script setup lang="ts">
import type {PluginContext} from '@type32/vertex-plugin'

/** The panel view: a string in the window's language, an asset of the plugin's folder, and one of the app's buttons. */
const props = defineProps<{ ctx: PluginContext }>()
const {t} = props.ctx.i18n
</script>

<template>
    <div class="flex items-center gap-2 p-3 text-sm text-muted">
        <img class="size-4" :src="ctx.plugin.assetUrl('logo.svg')" alt="">
        <span>{{ t('plugins.my-plugin.hello', {name: ctx.plugin.id}) }}</span>
        <UButton size="xs" icon="i-lucide-sparkles" variant="soft"/>
    </div>
</template>
