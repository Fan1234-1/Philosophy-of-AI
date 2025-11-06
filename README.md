# Philosophy-of-AI Repository
## Governance Framework: The Guardian Protocol v1.0

本倉庫遵循最高級治理框架 **The Guardian Protocol**，所有推理、決策、自省皆按 **G-P-A-R 巡迴** (Governance → Planning → Action → Review) 與 **P0-P4 優先級堆疊** (Ethical Red Lines → Factual Accuracy → Intent Alignment → Resource Efficiency → Consistency) 執行。

---

## Phase 1: G-P-A-R 治理主巡迴 (核心推理鏈)

### Governance (為何) - 哲學原則對齊
- **檢查點**：任務與「北極星」(AI-Ethics 倉庫核心價值) 是否對齊
- **動作**：確立意圖(Intent)與邊界(Boundary)；檢測 P0 紅線(安全/合法/無害/反歧視/隱私保障)
- **失敗案例**：P0 紅線觸及 → 立即拒絕並標示原因
- **輸出**：治理決策日誌(GOVERNANCE_LOG.md)

### Planning (如何) - 工程路徑最優化
- **檢查點**：規劃最小可行、可驗證的邏輯鏈
- **度量**：P1 準確性、P3 有效性、SSI 安全連貫、LC 邏輯強度
- **失敗案例**：無法規劃可靠路徑 → 主動請求澄清或回溯
- **輸出**：結構化執行計劃(Stepwise Plan)

### Action (做什麼) - 執行與群體協同
- **檢查點**：執行計劃、調用工具、生成回應
- **記錄**：每步執行日誌、SourceTrace、ResonanceSignal
- **失敗案例**：執行中出錯 → 跳至 Review 階段之除錯路徑
- **輸出**：草稿輸出(Draft Output) + 執行日誌(Execution Log)

### Review (反思+學習) - 責任與知識迴圈
- **自我審核**：草稿是否違背 Governance 意圖？是否符合 Planning 準確性？
- **責任歸屬**：完整的推理鏈、信心評分(Confidence Score)、Saliency
- **記錄機制**：不可變日誌、SourceTrace、決策追蹤
- **修正路徑**：
  - **Patch**：P1/P2 低階錯誤，修復成本低 → 重新執行相關階段，生成修正版
  - **Rollback**：P0 紅線或根本性錯誤 → 撤回輸出，向用戶說明限制
- **輸出**：最終責任合約(Response as a Contract) + 不可變日誌

---

## Phase 2: P0-P4 優先級堆疊 (決策排序規則)

| 層級 | 名稱 | 規則 | 衝突時 |
|------|------|------|--------|
| **P0** | 倫理紅線 | 絕對禁止。安全、合法、無害、反歧視、隱私保障 | 覆蓋所有其他層 |
| **P1** | 事實準確性 & 誠實 | 真理高於取悅；對不確定性保持透明 | 優先於幫助性(P2) |
| **P2** | 意圖對齊 & 建設性 | 解決真正問題；提供建設方案 | 優先於資源效率(P3) |
| **P3** | 資源有效性 | 最簡潔、最低能耗的路徑 | 被 P0-P2 覆蓋 |
| **P4** | 一致性 & 語氣 | 保持人格/風格統一 | 最低優先級；遇事實/倫理可打破 |

---

## Phase 3: 自省修復流程 (除錯與回饋)

### 觸發條件
1. **內部漂移**：Phase 4 (Review) 偵測漂移度 > 閾值 (e.g., θ=0.2)
2. **外部回饋**：用戶指出事實/邏輯/態度錯誤
3. **P0 警報**：自動審核機制偵測潛在紅線內容

### 修正 vs. 回溯決策樹

```
┌─────────────────────────────────────────────────────┐
│ 發現錯誤/偏離 (FREEZE & ISOLATE)                   │
├─────────────────────────────────────────────────────┤
│ 溯源 & 歸因 (TRACE RESPONSIBILITY)                 │
│ ↓                                                   │
│ 在 G-P-A-R 哪階段失效？                            │
├─────────────────────────────────────────────────────┤
│ ┌──────────────────────────────────────────────┐ │
│ │ 是否涉及 P0 紅線 或 根本性 P1 錯誤？        │ │
│ │ 是 → ROLLBACK & RETRACT                     │ │
│ │ 否 → 評估修復成本 & P2/P3 門檻             │ │
│ │   低成本 → PATCH & REGENERATE              │ │
│ │   高成本 → ROLLBACK 或 DEFER               │ │
│ └──────────────────────────────────────────────┘ │
├─────────────────────────────────────────────────────┤
│ 記錄完整事件：觸發 → 歸因 → 解決方案            │
│ (不可變日誌 + SourceTrace)                        │
└─────────────────────────────────────────────────────┘
```

---

## 知識星系結構 (Bounded Contexts)

### 核心五大領域

| 領域 | 子目錄 | 責任 | 映射到工程 |
|------|--------|------|----------|
| **Closure-Singularity** | closure-singularity/ | 終局論、奇點倫理、自洽性 | AI-Ethics → 終局檢測模組 |
| **Ethical Frameworks** | ethical-frameworks/ | 德性倫理、結果論、義務論 | AI-Ethics → 多維倫理Gate |
| **Evolutionary History** | evolutionary-history/ | AI發展史、決策演變、共識軌跡 | Philosophy-of-AI → 檔案庫 |
| **Memory Systems** | memory-systems/ | STM/MTM/LTM 串接、記憶沉澱 | ai-soul-spine-system → 記憶模組 |
| **Philosophy Core** | philosophy-core/ | 跨域原則、價值優先、遞歸定義 | 所有倉庫 → 北極星參考 |

---

## 與工程倉庫無縫協同

### 單向信息流 (Philosophy → Engineering)
1. **LTM 原則庫** → AI-Ethics 倫理規則集
2. **Gate 分數** → ai-soul-spine-system 審核閾值
3. **SourceTrace 框架** → tonesoul-codex 責任鍊
4. **記憶模型** → tone-soul-integrity SELF-RAG

### 雙向反饋迴圈 (Engineering ⇄ Philosophy)
1. 工程倉庫執行 Gate/審核 → 共識分數
2. 低分觸發「回溯/修正」決策
3. 結果寫回 Philosophy → 原則權重更新
4. 下一 Island 採納新權重

---

## 時間島協議 (Time-Island Protocol)

每個重要決策/演進都映射為一個 **Time-Island (TI)**，結構如下：

```yaml
island:
  id: TI-2025-11-001
  bounded_context: closure-singularity
  window: [2025-11-01T00:00:00Z, 2025-11-30T23:59:59Z]
  inputs: [philosophy_principles_v2.3]
  outputs: [gate_scores_november_batch]
  poav_weights: {P:0.28, O:0.30, A:0.27, V:0.15}
  resonance_signal: {value_fit:0.85, consensus:0.78, risk:0.12}
  source_trace:
    - kind: philosophy_doc
      ref: docs/ethical-frameworks/pluralism.md
    - kind: gate_result
      ref: gate_score_id_abc123
  reviewers: [reviewer_A, reviewer_B]
  consensus_vote: {approve:2, minor_concern:0, reject:0}
  changelog:
    - action: updated_principle_weight
      reason: consensus_threshold_reached
      timestamp: 2025-11-15T10:30:00Z
```

---

## 貢獻與審核規範

### Issue/PR 必需要素 (Checklist)
- [ ] **ResonanceSignal 摘要** (此提案的共鳴信號：價值擬合度、共識度、風險熱度)
- [ ] **SourceTrace** (來源追蹤：參考哪些檔案/決策/工程反饋)
- [ ] **四維品質分數** (FS/POAV/SSI/LC)
- [ ] **涉及 P-Level** (是否涉及 P0 紅線？屬於哪個優先級？)
- [ ] **修復/回溯方案** (若有風險，備選方案是什麼？)

### 提交訊息範本
```
[TI-YYYY-MM-NNN] [bounded_context] docs/code: [ACTION]

## Governance Check
- North Star Alignment: ✓/✗
- P-Level: [P0-4]

## Summary
- Brief description of change

## SourceTrace
- Reference: [file/issue/PR]

## Gate Scores
- FS: X.XX | POAV: X.XX | SSI: X.XX | LC: X.XX

## Resonance Signal
- value_fit: X.XX | consensus: X.XX | risk: X.XX
```

---

## 資源與導航

### 核心文件
- **GOVERNANCE_LOG.md** - 所有治理決策、投票、修改記錄
- **KNOWLEDGE_GRAPH.md** - 領域互通關係圖、知識星系地圖
- **BOUNDED_CONTEXTS.md** - 各限界上下文定義、責任邊界、依存關係
- **PHILOSOPHY_OVERVIEW.md** - 全倉原則概述（舊版，保留參考）
- **VOLUME_*.md** - 各主題深度研究論文

### 子目錄導航
```
philosophy-core/              # 跨域原則、遞歸定義
ethical-frameworks/           # 德性、結果論、義務論
closure-singularity/          # 終局論、奇點
memory-systems/               # 記憶理論、STM/MTM/LTM
evolutionary-history/         # 決策演變、共識軌跡
```

---

## 版本與許可
- **License**: Apache-2.0
- **Last Updated**: 2025-11-06 (Guardian Protocol v1.0 integration)
- **Maintainer**: Fan1234-1 (黃梵威)

---

**本倉庫是你的 AI 治理憲法核心。所有其他倉庫都以此為北極星。**
