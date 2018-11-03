## Properties of &lt;checksum&gt; Layer
The **&lt;checksum&gt;** layer has all the [common](layers.md) properties as
well as ones listed below. Refer to [&lt;checksum&gt; Layer](../frames/checksum.md) chapter
for detailed description. 

|Property Name|Allowed type / value|DSL Version|Required|Default Value|Description|
|:-----------:|:------------------:|:---------:|:------:|:-----------:|-----------|
|**alg**|"sum", "crc-ccitt", "crc-16", "crc-32", "custom"|1|yes||Checksum calculation algorithm.|
|**algName**|[name](../intro/names.md) string|1|no||Name of the custom algorithm. Applicable only if **alg="custom"**.|
|**from**|[name](../intro/names.md) string|1|yes (only if **until** is not specified)||Name of the frame layer, from which the checksum calculation starts.|
|**until**|[name](../intro/names.md) string|1|yes (only if **from** is not specified)||Name of the frame layer, until (and including) which the checksum calculation is executed.|
|**verifyBeforeRead**|[bool](../intro/boolean.md)|1|no|false|Perform checksum verification without reading values of other layers.|
