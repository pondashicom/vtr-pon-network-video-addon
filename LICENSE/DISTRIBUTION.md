# 配布条件・第三者通知 — 0.3.0

## 自作コード

Copyright (c) 2026 Tetsu Suzuki. 自作コードは[MIT License](MIT.txt)です。原文の著作権・許諾通知を保持してください。無保証・責任制限は原文によります。利用者の制作目的に非商用限定の条件を追加しません。

## インストール時の同意

パッケージのMIT原文とNDI-TERMS.mdを本体が同意対象として表示します。通知は別に閲覧できます。拒否・取り消しではそのパッケージを適用しません。更新版では文書と同意を改めて確認します。これによってMITやLGPLで認められた権利を減らすものではありません。

## 外部ソフト

NDI Runtime 6 x64を[NDI公式サイト](https://ndi.video/for-developers/ndi-sdk/)から別途導入してください。使用版は6.3.2.0で、`NDIlib_v6_load` を提供するRuntimeが必要です。NDI Toolsを使う場合も[公式配布](https://ndi.video/tools/)から取得します。

ATEM Software、NDI Runtime／Tools、Desktop Video、利用者のVST3プラグインはこのパッケージに含まれません。外部ソフトを導入するときはその提供元の契約を確認・承諾してください。アドオンの同意操作は外部インストーラーの同意を代行しません。SDKは生成する開発者だけが別途取得して契約を確認します。

## 生成元と境界

使用するSDKは NDI 6 SDK 6.3.2.0。配置は `network-video-addons/vtr-pon-network-video-addon.dll`、実行契約は `network-video-abi-v2`、Runtime Status v1です。DeckLinkの追加Output ABIはv1です。

SDK本体、生成ヘッダー、IDL、サンプル、テストDLL、デバッグ情報、ベンダーRuntime、他者のプラグインは配布しません。SDK由来の必要なコード・通知と、次項の同梱依存の条件を自作MITと区別します。

## NDI 6 SDK 6.3.2.0

[ヘッダー通知原文](third-party/NDI-HEADER-NOTICE.txt)のMITは対象ヘッダーだけに適用され、SDK全体やRuntimeには適用されません。Runtimeは動的に読み込みます。同梱しないRuntime／SDK／NDI製品・プロトコルに適用する[NDI利用条件](NDI-TERMS.md)と、[SDKの公式ライセンス案内](https://docs.ndi.video/all/developing-with-ndi/sdk/licensing)を確認してください。

NDI® is a registered trademark of Vizrt NDI AB. Copyright (C) 2023-2026 Vizrt NDI AB. All rights reserved. NDI契約が指定する権利者表記: NDI, Inc. 本ソフトへの提供元による推薦・保証・認証を示しません。[NDI公式サイト](https://ndi.video/)。
