# 国内免拔卡使用Tiktok记录
此处仅为自用流程，包含APP文件已绑定个人AppleID

### Shadowrocket配置记录

    [URL Rewrite]
    (?<=_region=)CN(?=&) JP 307
    (?<=&mcc_mnc=)4 2 307
    ^(https?:\/\/(tnc|dm)[\w-]+\.\w+\.com\/.+)(\?)(.+) $1$3 302
    (^https?:\/\/*\.\w{4}okv.com\/.+&.+)(\d{2}\.3\.\d)(.+) $118.0$3 302

    [MITM]
    hostname = *.tiktokv.com,*.byteoversea.com,*.tik-tokapi.com,-*snssdk.com, -*amemv.com

默认是日本区，更改代码JP (?<=_region=)CN(?=&) JP 307<br>
美国示例： (?<=_region=)CN(?=&) US 307<br>
英文简写 JP（日本）｜KR（韩国）｜UK（英国）｜US（美国）｜TW（台湾）<br>
