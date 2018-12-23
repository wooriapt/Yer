# The Minimal theme

[![Build Status](https://travis-ci.org/pages-themes/minimal.svg?branch=master)](https://travis-ci.org/pages-themes/minimal) [![Gem Version](https://badge.fury.io/rb/jekyll-theme-minimal.svg)](https://badge.fury.io/rb/jekyll-theme-minimal)

*Minimal is a Jekyll theme for GitHub Pages. You can [preview the theme to see what it looks like](http://pages-themes.github.io/minimal), or even [use it today](#usage).*

본 기술 백서는 블록체인에서 자체적으로 발행되는 네이티브 암호화폐가 없는 퍼블릭 블록체인 기술에 대해 소개한다.
법정화폐에 가치가 고정된 코인(예, dUSD , USD에 가치가 고정된 신용 토큰)이 블록체인 상에 발행되어 블록체인
시스템의 기본 통화로 사용되며, 금융 회사나 정부와 같은 신뢰기관들이 블록체인 사용자들로부터 수신한 법정화폐를
지급준비금으로 안전하게 보관하고, 그와 동일한 양만큼의 코인만이 투명하고 안전하게 블록체인 상에서 발행되고
유통된다. YOSEMITE 블록체인은 신뢰기관(Depository)들을 통해 발행되는 법정화폐 가치 고정 안정화 토큰,
비트코인과 같은 암호화폐에 가치가 고정된 토큰, 부동산 등의 실물 자산에 가치가 고정된 토큰들이 블록체인 상에서
거래될 수 있는 탈중앙화 분산 거래소 기능을 기본적으로 제공한다. Transaction-as-a-Vote(TaaV) 메커니즘을 통해,
블록체인 트랜잭션을 많이 발생시켜 블록체인 생태계에 직접적으로 공헌하는 서비스 제공자들에게 인센티브를
부여하는 방식으로, 기존의 PoW, PoS 합의 방식보다 공정하고 합리적인 새로운 방식의 Proof-of-Transaction (PoT)
블록체인 합의 메커니즘을 본 기술 백서를 통해 소개한다. Optimistic-Block-Production 방식과 최적화된 블록 유효성
투표 프로토콜을 통해 짧은 블록 타임과 빠른 블록 확정성을 구현하는 PoT 기반 BFT 합의 알고리즘은 기 개발된
YOSEMITE on/off-chain 하이브리드 거래소 기술과 함께 높은 수준의 블록체인 성능 확장성을 제공한다. 블록체인
상에 신뢰 네트워크를 구축하여 블록체인 계정 복구를 실현할 수 있는 네임드 멀티시그너처 블록체인 계정 시스템과
블록체인에 통합되어 제공되는 KYC/AML 규제준수 지원과 같은 특징들은 안정적이고 견고한 YOSEMITE 블록체인
생태계를 가능케 한다.

![Thumbnail of minimal](thumbnail.png)

## Usage

To use the Minimal theme:

1. Add the following to your site's `_config.yml`:

    ```yml
    theme: jekyll-theme-minimal
    ```

2. Optionally, if you'd like to preview your site on your computer, add the following to your site's `Gemfile`:

    ```ruby
    gem "github-pages", group: :jekyll_plugins
    ```



## Customizing

### Configuration variables

Minimal will respect the following variables, if set in your site's `_config.yml`:

```yml
title: [The title of your site]
description: [A short description of your site's purpose]
```

Additionally, you may choose to set the following optional variables:

```yml
logo: [Location of the logo]
show_downloads: ["true" or "false" to indicate whether to provide a download URL]
google_analytics: [Your Google Analytics tracking ID]
```

### Stylesheet

If you'd like to add your own custom styles:

1. Create a file called `/assets/css/style.scss` in your site
2. Add the following content to the top of the file, exactly as shown:
    ```scss
    ---
    ---

    @import "{{ site.theme }}";
    ```
3. Add any custom CSS (or Sass, including imports) you'd like immediately after the `@import` line

### Layouts

If you'd like to change the theme's HTML layout:

1. [Copy the original template](https://github.com/pages-themes/minimal/blob/master/_layouts/default.html) from the theme's repository<br />(*Pro-tip: click "raw" to make copying easier*)
2. Create a file called `/_layouts/default.html` in your site
3. Paste the default layout content copied in the first step
4. Customize the layout as you'd like

## Roadmap

See the [open issues](https://github.com/pages-themes/minimal/issues) for a list of proposed features (and known issues).

## Project philosophy

The Minimal theme is intended to make it quick and easy for GitHub Pages users to create their first (or 100th) website. The theme should meet the vast majority of users' needs out of the box, erring on the side of simplicity rather than flexibility, and provide users the opportunity to opt-in to additional complexity if they have specific needs or wish to further customize their experience (such as adding custom CSS or modifying the default layout). It should also look great, but that goes without saying.

## Contributing

Interested in contributing to Minimal? We'd love your help. Minimal is an open source project, built one contribution at a time by users like you. See [the CONTRIBUTING file](docs/CONTRIBUTING.md) for instructions on how to contribute.

### Previewing the theme locally

If you'd like to preview the theme locally (for example, in the process of proposing a change):

1. Clone down the theme's repository (`git clone https://github.com/pages-themes/minimal`)
2. `cd` into the theme's directory
3. Run `script/bootstrap` to install the necessary dependencies
4. Run `bundle exec jekyll serve` to start the preview server
5. Visit [`localhost:4000`](http://localhost:4000) in your browser to preview the theme

### Running tests

The theme contains a minimal test suite, to ensure a site with the theme would build successfully. To run the tests, simply run `script/cibuild`. You'll need to run `script/bootstrap` one before the test script will work.
