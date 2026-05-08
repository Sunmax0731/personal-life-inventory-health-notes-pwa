# 仕様

        ## 対象レコード

        - `inventoryItem`
- `healthNote`
- `lifeMemo`
- `nextAction`

        ## 必須項目

        `title`, `category`, `nextAction`

        ## 警告項目

        `sensitivityNote`, `reviewDate`

        ## フロー

        1. 入力レコードを受け取る。
        2. `src/core/scenarioEngine.js` が必須項目と警告項目を評価する。
        3. `src/report/reportBuilder.js` が検証結果を集計する。
        4. `dist/validation-result.json` を release evidence の前提証跡にする。

        ## 保存方針

        健康メモは医療判断ではなく個人記録として扱い、外部送信しない
