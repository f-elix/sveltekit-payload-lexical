<script lang="ts">
	import type { SerializedEditorState } from '@payloadcms/richtext-lexical/lexical';
	import {
		convertLexicalToHTML,
		type HTMLConverters,
		type HTMLConvertersFunction
	} from '@payloadcms/richtext-lexical/html';

	const html = convertLexicalToHTML({
		data: {},
		className: `_rich-text ${typeClasses[type]}`,
		converters: ({ defaultConverters }) => {
			return {
				...defaultConverters,
				...(converters ?? {})
			};
		},
		disableTextAlign: true
	});
</script>

{@html html}
<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>
