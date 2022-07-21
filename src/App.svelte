<script>
  import {onMount} from "svelte";
  import {isLoading, _} from "svelte-i18n"
  import "./i18n"
</script>

<main>
  <h1>Vite + Svelte</h1>

  {#if !$isLoading}
    <div class="card">
      <p>
        Working:
        {$_("common.workingMessage", {values: {name: "John"}})}
      </p>

      <p>
        Not working:
        {$_("common.notWorkingMessage", {values: {name: "John"}})}
      </p>
    </div>
  {/if}
</main>
