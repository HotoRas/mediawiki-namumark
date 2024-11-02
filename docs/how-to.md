------------------------
mediawiki-namumark를 어떻게 사용하는지 설명합니다
------------------------

# 사용 방법
1. 미디어위키 extensions 폴더에서 다음을 실행합니다. (git이 없는 경우 수동 다운받아 넣어도 됨)
```sh
git clone https://github.com/dodawiki/mediawiki-namumark.git NamuMark
```

2. LocalSettings.php 파일에서 다음을 설정합니다.
```php
wfLoadExtension( 'NamuMark' );

$wgRawHtml = true;
$wgAllowExternalImages = true;
$wgNamespacesWithSubpages[NS_MAIN] = true;
$wgNamespacesWithSubpages[NS_TEMPLATE] = true;
$wgAllowDisplayTitle = true;
$wgRestrictDisplayTitle = false;
$wgDefaultUserOptions['numberheadings'] = 1;
$wgAllowSlowParserFunctions = true; # [pagecount(이름공간)] 문법을 사용하기 위해서는 켜야 합니다.
```
