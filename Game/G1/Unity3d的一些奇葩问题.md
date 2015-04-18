## 打包单独一个label，AssetBundle莫名奇妙达到600KB以上
* 排查结果，是因为在PlayerSettings中，使用了 Api Compatibility level中的.net 2.0，而不是subset
