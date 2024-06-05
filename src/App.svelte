<!-- 这是一个文档搜索项目 -->

<script>
    import Doc from "./Doc.svelte";
    import docs from "./data.json";


    let itext = "";

    $: targets = docs.filter(
        (doc) =>
            doc.title.toLowerCase().includes(itext.toLowerCase()) ||
            doc.content.toLowerCase().includes(itext.toLowerCase()),
    );
</script>

<input type="text" bind:value={itext} />
<ul>
    {#each targets as target}
        <Doc>
            <span slot="title">{target.title}</span>
            <span slot="content">{target.content.substring(0, 120)} ...</span>
        </Doc>
    {/each}
</ul>
