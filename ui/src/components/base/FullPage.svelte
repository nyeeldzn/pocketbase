<script>
    import PageWrapper from "@/components/base/PageWrapper.svelte";

    export let nobranding = false;
</script>

<PageWrapper class="full-page" center>
    <div class="wrapper wrapper-sm m-b-xl panel-wrapper">
        {#if !nobranding}
            <div class="block txt-center m-b-lg">
                <figure class="logo">
                    <img
                        src="{import.meta.env.BASE_URL}images/logo.png"
                        alt="Greenbase logo"
                        width="60"
                        height="45"
                    />
                    <span class="txt">Green<strong>Base</strong></span>
                </figure>
            </div>
            <div class="clearfix" />
        {/if}

        <slot />
    </div>
</PageWrapper>

<style>
    .panel-wrapper {
        animation: slideIn 200ms;
    }
</style>
