# Android Studio Localization-ja, ko, zh

Android Studio 中日韩语言包 (同样也适用其它基于 IntelliJ 平台的 IDE)。

Android Studio 向け 中国語・日本語・韓国語 言語パック (その他の IntelliJ プラットフォームを基盤とする IDE にも同様に適用されます)。

Android Studio 용 중국어/일본어/한국어 언어 팩 (다른 IntelliJ 플랫폼 기반 IDE에도 마찬가지로 적용됩니다).

## 前言 / はじめに / 서문

语言包能够为基于 IntelliJ 平台的 IDE 带来完全本地化的界面。语言包在 2024.1 或更低版本的 IDE 中需手动安装。但从 2024.2 版开始，该语言包已捆绑，无需手动安装。因此某些基于 IntelliJ 平台的 IDE 将无法获取新版语言包。

言語パックは、IntelliJ プラットフォームを基盤とする IDE に完全にローカライズされたユーザーインターフェースを提供します。2024.1 以前のバージョンの IDE では、言語パックは手動でインストールする必要があります。しかしながら、2024.2 バージョン以降では、当該言語パックは製品にバンドル（同梱）されており、手動インストールは不要となりました。そのため、一部の IntelliJ プラットフォーム基盤の IDE では、新バージョンの言語パックを入手できなくなります。

언어 팩은 IntelliJ 플랫폼 기반 IDE에 완전히 현지화된 사용자 인터페이스를 제공합니다. 2024.1 이하 버전의 IDE에서는 언어 팩을 수동으로 설치해야 합니다. 그러나 2024.2 버전부터 해당 언어 팩이 번들로 제공되어 수동 설치가 필요 없습니다. 따라서 일부 IntelliJ 플랫폼 기반 IDE에서는 새 버전의 언어 팩을 이용할 수 없게 됩니다.

## 操作 / 手順 / 조작 방법

你可以按照下述步骤制作最新的语言包插件，也可以前往 [Releases] 页面下载已处理好的插件。

1. 下载 [IntelliJ IDEA] 最新版本的压缩包。
2. 解压压缩包并从 plugins/localization-ja/ko/zh 中找到语言包插件。
3. 对 localization-ja/ko/zh.jar 插件执行下面的命令。

最新の言語パックプラグインを作成するには、以下の手順に従ってください。または、[Releases] ページから処理済みのプラグインをダウンロードすることもできます。

1. [IntelliJ IDEA] の最新バージョンのアーカイブ（圧縮ファイル）をダウンロードします。
2. アーカイブを解凍し、plugins/localization-ja/ko/zh ディレクトリ内にある言語パックプラグインを見つけます。
3. localization-ja/ko/zh.jar プラグインファイルに対して、以下のコマンドを実行します。

최신 언어 팩 플러그인을 제작하려면 다음 단계를 따르십시오. 또는 [Releases] 페이지에서 처리된 플러그인을 다운로드할 수도 있습니다.

1. [IntelliJ IDEA] 최신 버전의 압축 파일을 다운로드합니다.
2. 압축 파일을 해제하고 plugins/localization-ja/ko/zh 디렉터리에서 언어 팩 플러그인 파일을 찾습니다.
3. localization-ja/ko/zh.jar 플러그인 파일에 대해 다음 명령어를 실행합니다.

```Bash
jar xf localization-ja/ko/zh.jar META-INF/plugin.xml
ver=$(grep '^  <version' META-INF/plugin.xml | cut -d'>' -f2 | cut -d'<' -f1)
sed -i "/^  <idea-version/{s/$ver/201.7223.36/; s/$ver/999.999.999/1}" META-INF/plugin.xml
jar uf localization-ja/ko/zh.jar META-INF/plugin.xml
```

[Releases]: https://github.com/kitty-panics/android-studio-ja-ko-zh/releases
[IntelliJ IDEA]: https://www.jetbrains.com/idea/download/other.html

## Others

- https://plugins.jetbrains.com/plugin/13710-chinese-simplified-language-pack----/versions/stable/85840
- https://plugins.jetbrains.com/plugin/13964-japanese-language-pack------/versions/stable/85841
- https://plugins.jetbrains.com/plugin/13711-korean-language-pack------/versions/stable/106484
