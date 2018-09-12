<template>
    <div class="panel">
        <p>
            CoinTool-ETH 是一个开源工具，使用浏览器自动生成自定义靓号ETH地址<br>
            在下面输入您选择的简短前缀，然后点击“生成”开始。
        </p>

        <h2>什么是靓号地址？</h2>
        <p>
            靓号地址是一个ETH地址，其中一部分由您自己选择，使其看起来不那么随机。<br>
            例如: <span class="monospace">0x1111ee254729296a45a3885639AC7E10F9d54979</span>, 或
            <span class="monospace">0x999999cf1046e68e36E1aA2E0E07105eDDD1f08E</span>
        </p>

        <h2>怎么运行的</h2>
        <p>
            在下面输入您选择的前缀，然后单击“生成”开始。 您的浏览器将生成大量随机ETH地址，直到一个以你输入的前缀开头的地址。<br>找到地址后，您可以显示私钥，或单击“保存”按钮进行下载keystore文件。<br>您可以增加工作线程的数量以达到更快的速度，或者在计算机时空闲时运行它。<br>
        </p>
        <h2>安全</h2>
        <p>
            如上所述，所有内容仅在您的浏览器中计算。什么都没有离开你的电脑，甚至您的浏览器标签。 没有数据库，没有服务器端代码。 当你关闭标签时，一切都消失了<br><br>
            <b>CoinTool-ETH不能也不会存储您的私钥</b>，如果您不信任它，您有3种方法可以确保你的钥匙仍然是私人的<br>
            &nbsp;-&nbsp;加载网页后，您可以断网并继续使用CoinTool-ETH，它将继续工作<br>
            &nbsp;-&nbsp;您还可使用Chrome的Network功能来监视网页的网络活动<br>
            &nbsp;-&nbsp;代码开源。您可以无限制的审查网页代码<br>
            <br>CoinTool-ETH使用加密安全伪随机数生成器（CSPRNG）来生成以太坊地址。<br>keystore 文件使用AES-128-CTR密码加密，使用BKDF2-SHA256派生函数和65536个hash随机数。
        </p>
        <h2>性能</h2>
        <p>
            出于某种原因，CoinTool-ETH的性能在浏览器之间可能有很大差异。目前，推荐使用Chrome，因为效果最佳。<br>
            在手机或平板电脑上CoinTool也可以正常工作，但不要期望达到好电脑的速度.
        </p>
    </div>
</template>

<script>
    export default {};
</script>

<style lang="sass" scoped>
    @import "../css/variables"
    p
        margin: 15px 0 20px
        color: $text-alt
        overflow-x: hidden
        text-overflow: ellipsis
        .monospace
            font-family: $monospace-font
            font-size: 0.85em
</style>
