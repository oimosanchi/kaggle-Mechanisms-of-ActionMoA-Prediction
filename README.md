# kaggle-Mechanisms-of-ActionMoA-Prediction
Mechanisms of Action (MoA) Predictionコンペのリポジトリ

#### 20201103  
**参考にしたNotebooks**  
https://www.kaggle.com/mannsingh/simple-xgboost-model-for-beginners  
Public Score:0.02098  

**特徴**  
*sig_id               サンプルのユニークなID  
*g-接頭辞を持つ特徴量   遺伝子発現特徴量 772個（g-0からg-771まで）  
*c-接頭辞を持つ特徴量   細胞生存率の特徴量 100個（c-0からg-99まで）  
*cp_time               治療期間（24時間，48時間，72時間）を示す分類的特徴量である．  
*cp_dose               投与量が低いか高いかを示す2値のカテゴリ特徴量である(D1またはD2)  
*cp_type               サンプルが化合物で処理されたか，対照摂動（rt_cpまたはctl_vehicle）で処理されたかを示す2値のカテゴリ特徴量です  

Encoding  
cp_time   trt_cp:0, ctl_vehicle:1  
cp_dose   D1:0, D21  
cp_time   24, 48, 72のまま  

XGBRegressor


#### 20201126  
**参考にしたNotebooks**  
https://www.kaggle.com/oimosanchi/moa-with-keras-for-beginner-s/edit  
Encoding  
cp_time   trt_cp:0, ctl_vehicle:1  
cp_dose   D1:0, D21  
cp_time   24:0, 48:1, 72:2  

4つのモデルを作成し、各モデルは5つのkfold分割
最後に予測値を平均化してcsvに保存

create model, train model について　詳しく知りたいこと
