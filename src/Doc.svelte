<div class="doc-box">
    <h1 class="doc-title"><slot name="title" /></h1>
    <br />
    <p class="doc-content"><slot name="content" /></p>
</div>

<style lang="scss">
    .doc-box {
        padding: 12px;
        border: 1px solid;
        border-image: linear-gradient(666deg, #a255ff, #5a9cff) 1;
        border-radius: 12px;
        margin: 12px;
        max-width: 500px;

        .doc-content {
            color: #b6b7d4;
        }

        .doc-title {
            font-size: 24px;
            font-weight: bold;
            margin-bottom: -20px;
            color: #ececec;
        }
    }
</style>
