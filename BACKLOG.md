# 共創待辦與里程碑

以下是原創起始規劃，**全部待認領／未開始**。沒有指定負責人、完成百分比或承諾日期。開始前查 [Issues](https://github.com/FreeTWAI-AI/freedom-skill-projection-mapping/issues)／[PR](https://github.com/FreeTWAI-AI/freedom-skill-projection-mapping/pulls)；把認領範圍與相依工作連回來，最新討論优先。

## M1：可複用的入門流程（planned）

完成條件：新增合成案例、模板欄位及其結構檢查；由維護者審查後才標完成。

### LIGHT-01 · 加入多表面素材命名與校對規則

- 狀態：proposed／未認領
- 範圍：擴充 surface-map 模板，定義兩個以上投影表面的素材對應。
- 驗收：提供雙表面合成案例；每個表面有唯一 id 與尺寸；既有單表面範例仍可驗證。
- 驗證：`python3 scripts/validate.py examples/projection-plan.json`；`python3 -m unittest discover -s tests -v`；人工核對模板文字。
- PR 附：task id、改動檔案、範例、執行結果與未驗證事項。

### LIGHT-02 · 設計中斷後的 cue 復原流程

- 狀態：proposed／未認領
- 範圍：新增停止、重播、跳下一段與切黑場的操作紀錄模板。
- 驗收：不直接操作硬體；分開記錄預期與實測結果；列出操作者與恢復時点。
- 驗證：`python3 scripts/validate.py examples/projection-plan.json`；`python3 -m unittest discover -s tests -v`；人工核對模板文字。
- PR 附：task id、改動檔案、範例、執行結果與未驗證事項。

### LIGHT-03 · 補充輸出規格交接範例

- 狀態：proposed／未認領
- 範圍：加入解析度、幀率、長度、編碼格式與聲音交付欄位。
- 驗收：只使用原創合成素材清單；不同播放端規格標成待實測；提供至少兩種交付情境。
- 驗證：`python3 scripts/validate.py examples/projection-plan.json`；`python3 -m unittest discover -s tests -v`；人工核對模板文字。
- PR 附：task id、改動檔案、範例、執行結果與未驗證事項。

## M2：由真實使用回饋改善（planned）

M1 後，由自願使用者提供可公開、已去識別的回饋。僅把實際收到的回饋列入 Issue；不預填活動成果、人數、成效或測試成功。跨公會協作可連結原 Issue，不重複複製責任。
