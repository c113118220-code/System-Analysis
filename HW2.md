# C113118220 林余柔-個人作業2

## 一、任務基本資料

| 任務 | 任務說明 | 用時(天數) | 前置任務 |
|---|---|---:|---|
| 1 | 研擬計畫 | 1 | - |
| 2 | 任務分配 | 4 | 1 |
| 3 | 取得硬體 | 17 | 1 |
| 4 | 程式開發 | 70 | 2 |
| 5 | 安裝硬體 | 10 | 3 |
| 6 | 程式測試 | 30 | 4 |
| 7 | 撰寫使用手冊 | 25 | 5 |
| 8 | 轉換檔案 | 20 | 5 |
| 9 | 系統測試 | 25 | 6 |
| 10 | 使用者訓練 | 20 | 7、8 |
| 11 | 使用者測試 | 25 | 9、10 |

## 二、PERT/CPM 圖

```mermaid
flowchart LR

    A["1.研擬計畫<br/>(總用時1天)"]
    B["2.任務分配<br/>(總用時4天)"]
    C["3.取得硬體<br/>(總用時17天)"]
    D["4.程式開發<br/>(總用時70天)"]
    E["5.安裝硬體<br/>(總用時10天)"]
    F["6.程式測試<br/>(總用時30天)"]
    G["7.撰寫使用手冊<br/>(總用時25天)"]
    H["8.轉換檔案<br/>(總用時20天)"]
    I["9.系統測試<br/>(總用時25天)"]
    J["10.使用者訓練<br/>(總用時20天)"]
    K["11.使用者測試<br/>(總用時25天)"]

    A --> B
    A --> C
    B --> D
    C --> E
    D --> F
    E --> G
    E --> H
    F --> I
    G --> J
    H --> J
    I --> K
    J --> K

    classDef critical fill:#FFC8B4,stroke:#FF0000,stroke-width:5px,color:#000000;
    class A,B,D,F,I,K critical;

    linkStyle 0 stroke:#FF0000,stroke-width:5px;
    linkStyle 2 stroke:#FF0000,stroke-width:5px;
    linkStyle 4 stroke:#FF0000,stroke-width:5px;
    linkStyle 7 stroke:#FF0000,stroke-width:5px;
    linkStyle 10 stroke:#FF0000,stroke-width:5px;

 classDef acceed fill:#99FFFF,stroke:#0066FF,stroke-width:5px,color:#000000;
    class C,E,G,H,J acceed;

    linkStyle 1 stroke:##99FFFF,stroke-width:5px;
    linkStyle 3 stroke:##99FFFF,stroke-width:5px;
    linkStyle 5 stroke:##99FFFF,stroke-width:5px;
    linkStyle 6 stroke:##99FFFF,stroke-width:5px;
    linkStyle 8 stroke:##99FFFF,stroke-width:5px;
    linkStyle 9 stroke:##99FFFF,stroke-width:5px;
    linkStyle 11 stroke:##99FFFF,stroke-width:5px;
```

> 備註：紅色節點代表關鍵路徑，藍色節點代表非關鍵路徑。

## 三、各階段開始與結束時間

| 任務 | 任務說明 | 開始時間 | 結束時間 |
|---|---|---:|---:|
| 1 | 研擬計畫 | 第1天 | 第1天 |
| 2 | 任務分配 | 第2天 | 第5天 |
| 3 | 取得硬體 | 第2天 | 第18天 |
| 4 | 程式開發 | 第6天 | 第75天 |
| 5 | 安裝硬體 | 第19天 | 第28天 |
| 6 | 程式測試 | 第76天 | 第105天 |
| 7 | 撰寫使用手冊 | 第29天 | 第53天 |
| 8 | 轉換檔案 | 第29天 | 第48天 |
| 9 | 系統測試 | 第106天 | 第130天 |
| 10 | 使用者訓練 | 第54天 | 第73天 |
| 11 | 使用者測試 | 第131天 | 第155天 |

## 四、專案甘特圖

```mermaid
gantt
    title 專案甘特圖
    dateFormat YYYY-MM-DD
    axisFormat %m/%d

    section 專案任務
    研擬計畫       :2026-01-01, 1d
    任務分配       :2026-01-02, 4d
    取得硬體       :2026-01-02, 17d
    程式開發       :2026-01-06, 70d
    安裝硬體       :2026-01-19, 10d
    程式測試       :2026-03-17, 30d
    撰寫使用手冊   :2026-01-29, 25d
    轉換檔案       :2026-01-29, 20d
    系統測試       :2026-04-16, 25d
    使用者訓練     :2026-02-23, 20d
    使用者測試     :2026-05-11, 25d
```

## 五、關鍵路徑與最短工期

本專案關鍵路徑：

**1(研擬計畫) → 2(任務分配) → 4(程式開發) → 6(程式測試) → 9(系統測試) → 11(使用者測試)**

關鍵路徑總工期：

**1 + 4 + 70 + 30 + 25 + 25 = 155 天**

故本專案最短工期為 **155 天**。
