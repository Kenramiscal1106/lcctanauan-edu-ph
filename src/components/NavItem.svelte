<script>
  export let text;
  export let dropdown;
  export let href;
</script>

{#if dropdown}
  <button class="p-3">{text}</button>
  <div class="p-3">
    <slot />
  </div>
{:else}
  <a
    {href}
    target={href.includes("http") ? "_blank" : ""}
    class={`p-3 hover:font-medium`}>{text}</a
  >
{/if}
