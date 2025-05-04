# M5 需要予測 - Kaggle 
このプロジェクトでは、Kaggle コンペティション「[M5 Forecasting - Accuracy](https://www.kaggle.com/competitions/m5-forecasting-accuracy)」のデータを用いて、小売商品の日次需要を予測するモデルを構築しています。

Notebook は Kaggle 上で開発・実行されたもので、GitHub でのポートフォリオ公開を目的にエクスポートしたものです。

---

## 📌 プロジェクトの目的

- 時系列データに対する需要予測モデルの構築
- 特徴量エンジニアリングおよび高速なブースティングモデル（LightGBM）の活用
- M5コンペ特有の複雑なデータ構造の取り扱いに対応

---

## 📂 使用データ

- データソース：[M5 Forecasting - Accuracy | Kaggle](https://www.kaggle.com/competitions/m5-forecasting-accuracy/data)
- 主なデータセット：
  - `sales_train_validation.csv`：販売実績
  - `calendar.csv`：日付とイベント情報
  - `sell_prices.csv`：価格データ

---

## 🧪 使用ライブラリ

| ライブラリ名 | 用途 |
|--------------|------|
| pandas | データフレーム操作 |
| numpy | 数値計算 |
| matplotlib / seaborn | 可視化 |
| scikit-learn | モデル評価や前処理 |
| lightgbm | 時系列回帰モデルの構築 |

---

## 🔍 分析の流れ（Notebook 構成）

1. **データの読み込みと整形**
   - 各CSVファイルのマージと変換（long形式への変換など）
2. **特徴量エンジニアリング**
   - カレンダー情報、ラグ特徴量、移動平均などの導入
3. **モデル構築**
   - LightGBMによる回帰モデル
   - 予測対象：日次需要（validation対象期間）
4. **評価**
   - 評価指標：RMSE
   - クロスバリデーションでの性能確認
5. **予測結果の出力**
   - 提出用フォーマット（sample_submission.csvに準拠）

---
