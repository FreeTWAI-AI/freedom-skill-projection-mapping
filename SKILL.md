---
name: freedom-projection-mapping
description: 把投影光雕構想整理成場勘、畫面分區、素材規格與播放 cue。
---

# 光影與光雕製作手冊

## 適用範圍

先做提案、素材與播放排程；不包含硬體控制、實際投影校正或現場技術認證。

## 輸入

- 投影表面、觀看距離、環境光與場地可用時段
- 可用投影機與播放設備的已確認规格或待查項目
- 原創或獲授權的素材及輸出尺寸、幀率、長度

## 執行步驟

1. 複製 templates/site-survey.md，記錄表面尺寸、環境光、觀眾位置與設備限制。
2. 用 templates/surface-map.md 為每個投影區域命名，附原創線框示意與對應尺寸。
3. 在 templates/cue-sheet.csv 列出 cue、素材檔名、觸發時點、操作角色與黑場備援。
4. 填 templates/projection-plan.json，執行驗證，排除重複 cue 與未列入清單的素材。
5. 現場試播另留紀錄；只有實際量測與播放才標完成，提案測試不算現場驗收。

## 輸出與驗收

一份可交接的光雕製作提案：場勘紀錄、畫面配置與播放 cue 表。

```sh
python3 scripts/validate.py examples/projection-plan.json
python3 -m unittest discover -s tests -v
```

驗證結果只描述結構檢查；實地確認、內容授權、參與者同意及實際成效必須另由當事人提供，未知保持未知。不要把模板範例當成已發生事實。

## 協作交接

1. 查 [BACKLOG.md](BACKLOG.md)、[Issues](https://github.com/FreeTWAI-AI/freedom-skill-projection-mapping/issues) 與 [PR](https://github.com/FreeTWAI-AI/freedom-skill-projection-mapping/pulls) 的最新狀態，避免重複工作。
2. 在已授權範圍內選一個待辦，用自己的 Fork／分支製作最小可審查變更。尚未派工時先在 Issue 協調；當前使用者已明確派工則直接沿用。
3. PR 目標 `https://github.com/FreeTWAI-AI/freedom-skill-projection-mapping:main`。列 task id、變更用途、實跑命令、結果、未驗證項目及相依 PR。
4. 保留作者、來源與審查結果。Agent 可讀此技能，不因此取得帳號、發送訊息、付款、現場設備或平台資料的操作權。

## 邊界

- 公開範例不含未授權的音樂、影像或客戶場勘照片；只提供原創文字模板。
- 本包不操作雷射、電力、吊掛、舞台或投影設備；實際作業由現場負責人確認。
- 不以模擬輸出宣稱真實亮度、對位、色彩或設備相容性已驗證。
