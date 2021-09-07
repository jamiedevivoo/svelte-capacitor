<script lang="typescript">
	import { Router } from "@roxi/routify";
	import { routes } from "../.routify/routes";
	import TailwindCss from "./tailwindCSS.svelte";

	import { Haptics, ImpactStyle } from '@capacitor/haptics';

const hapticsImpactMedium = async () => {
  await Haptics.impact({ style: ImpactStyle.Medium });
};

const hapticsImpactLight = async () => {
  await Haptics.impact({ style: ImpactStyle.Light });
};

const hapticsVibrate = async () => {
  await Haptics.vibrate();
};

const hapticsSelectionStart = async () => {
  await Haptics.selectionStart();
};

const hapticsSelectionChanged = async () => {
  await Haptics.selectionChanged();
};

const hapticsSelectionEnd = async () => {
  await Haptics.selectionEnd();
};
</script>

<TailwindCss />

<Router {routes} />
<p>Hey</p>
<style @global>

</style>
