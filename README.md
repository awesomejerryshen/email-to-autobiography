# Email to Autobiography 📧✨📖

> Turn your emails into your life story. Write naturally, let AI weave the narrative.

[English](#english) | [繁體中文](#繁體中文)

---

<a name="english"></a>
## English

### The Concept

**Email to Autobiography** is a creative exploration of combining three powerful elements:
1. **Email** - A natural, frictionless way to capture thoughts and memories
2. **LLM (Large Language Model)** - Intelligent organization, theme detection, and narrative synthesis
3. **Autobiography** - Structured, meaningful output that tells your life story

### Core Idea

People already write emails daily - to friends, family, colleagues, or even to themselves as notes. What if we could turn those emails into a coherent autobiography without asking anyone to adopt new habits?

### How It Works

```
┌─────────────────────────────────────────────────────────────┐
│                    1. WRITE EMAILS                          │
│  ────────────────────────────────────────────────────────  │
│  Natural capture through email:                              │
│  • Email yourself about life events                          │
│  • Use a dedicated address                                   │
│  • Forward existing emails                                  │
└─────────────────────────────────────────────────────────────┘
                            ↓
┌─────────────────────────────────────────────────────────────┐
│                    2. AI PROCESSING                         │
│  ────────────────────────────────────────────────────────  │
│  LLM-powered analysis:                                       │
│  • Theme extraction (career, relationships, growth, etc.)   │
│  • Emotional arc detection                                  │
│  • Chronological organization                               │
│  • Key milestone identification                            │
│  • Chapter generation                                       │
└─────────────────────────────────────────────────────────────┘
                            ↓
┌─────────────────────────────────────────────────────────────┐
│                 3. EXPLORE & SHARE                           │
│  ────────────────────────────────────────────────────────  │
│  Multiple viewing modes:                                      │
│  • Read by chapters (narrative flow)                         │
│  • Browse by themes (categorical view)                       │
│  • Interactive timeline (chronological)                     │
│  • Export: PDF, EPUB, Markdown                              │
└─────────────────────────────────────────────────────────────┘
```

### Features

#### Zero Friction
- No new app to install
- No new habit to form
- Use email clients you already love
- Works with Gmail, Outlook, Apple Mail, etc.

#### AI-Powered Organization
- **Theme Detection**: Automatically categorize emails by topics (career, relationships, travel, learning, health, etc.)
- **Emotional Arcs**: Track emotional journeys and personal growth
- **Smart Grouping**: Related emails clustered into meaningful chapters
- **Title Generation**: AI suggests chapter titles based on content
- **Summary Creation**: Generate chapter summaries for quick navigation

#### Multiple Views
- **Chapter View**: Read like a book with AI-generated titles
- **Theme View**: Explore by topics and categories
- **Timeline View**: Browse through life's moments chronologically
- **Search**: Find any memory instantly

#### Export Options
- PDF (print-ready)
- EPUB (e-reader friendly)
- Markdown (portable, version-controllable)

#### Privacy First
- All data stored locally or in your chosen encrypted vault
- You own your data, always
- Optional: Self-hosted option for complete control

### Technical Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                      Frontend                               │
│  ────────────────────────────────────────────────────────  │
│  • React / Next.js                                          │
│  • TypeScript                                               │
│  • Tailwind CSS                                             │
│  • i18n (English + Traditional Chinese)                     │
└─────────────────────────────────────────────────────────────┘
                            ↑↓
┌─────────────────────────────────────────────────────────────┐
│                      Backend API                            │
│  ────────────────────────────────────────────────────────  │
│  • Node.js / Express                                         │
│  • RESTful + GraphQL endpoints                              │
│  • Email webhook handling                                    │
│  • LLM integration (OpenAI / Anthropic / local)            │
└─────────────────────────────────────────────────────────────┘
                            ↑↓
┌─────────────────────────────────────────────────────────────┐
│                      Data Layer                             │
│  ────────────────────────────────────────────────────────  │
│  • PostgreSQL / SQLite (emails metadata)                   │
│  • Vector DB (semantic search)                             │
│  • Object Storage (attachments, exports)                   │
└─────────────────────────────────────────────────────────────┘
                            ↑↓
┌─────────────────────────────────────────────────────────────┐
│                   Email Integration                         │
│  ────────────────────────────────────────────────────────  │
│  • Gmail API                                                │
│  • Microsoft Graph (Outlook)                                │
│  • IMAP/SMTP for generic providers                         │
│  • Custom email address (optional)                         │
└─────────────────────────────────────────────────────────────┘
```

### LLM-Powered Features

#### Content Analysis
```typescript
interface EmailAnalysis {
  themes: string[];           // ["career", "growth", "learning"]
  emotions: string[];         // ["hopeful", "determined", "anxious"]
  entities: Entity[];         // people, places, organizations
  keyMilestones: Milestone[]; // significant life events
  suggestedChapter?: string;  // AI-generated chapter assignment
}

interface Milestone {
  date: Date;
  title: string;
  description: string;
  impact: "high" | "medium" | "low";
}
```

#### Chapter Generation
- Group related emails into cohesive chapters
- Generate chapter titles
- Create chapter summaries
- Identify narrative arcs
- Suggest chapter ordering

#### Timeline Detection
- Identify key life events (graduation, marriage, job changes, etc.)
- Create visual timeline with milestones
- Link emails to timeline events

### Development Roadmap

#### Phase 1: MVP (Minimum Viable Product)
- [ ] Backend API with email ingestion
- [ ] Basic LLM integration for theme detection
- [ ] Simple chapter generation
- [ ] Frontend with chapter view
- [ ] Support for one email provider (Gmail)

#### Phase 2: Enhanced Features
- [ ] Multiple email providers (Outlook, generic IMAP)
- [ ] Theme view and timeline view
- [ ] Export to PDF
- [ ] Advanced LLM features (emotional arcs, milestones)
- [ ] Search functionality

#### Phase 3: Polish & Deploy
- [ ] Export to EPUB and Markdown
- [ ] Self-hosted option
- [ ] Mobile-responsive design
- [ ] User authentication
- [ ] Privacy controls

#### Phase 4: Advanced Features (Exploratory)
- [ ] AI narrative enhancement (rewrite for better storytelling)
- [ ] Voice support ( dictate emails)
- [ ] Photo attachment integration
- [ ] Collaboration (invite family to contribute)
- [ ] AI-powered insights and patterns

### Installation & Setup (Development)

```bash
# Clone the repository
git clone https://github.com/awesomejerry/email-to-autobiography.git
cd email-to-autobiography

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Edit .env with your API keys

# Run development server
npm run dev
```

### Environment Variables

```env
# Email Integration
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
MICROSOFT_CLIENT_ID=your_microsoft_client_id
MICROSOFT_CLIENT_SECRET=your_microsoft_client_secret

# LLM Integration
OPENAI_API_KEY=your_openai_api_key
# or ANTHROPIC_API_KEY for Claude

# Database
DATABASE_URL=postgresql://user:password@localhost:5432/autobiography
VECTOR_DB_URL=your_vector_db_url

# App
NEXT_PUBLIC_APP_URL=http://localhost:3000
```

### Contributing

This is a creative exploration project. Ideas, suggestions, and contributions are welcome!

### License

MIT License - feel free to explore and build upon this idea.

---

<a name="繁體中文"></a>
## 繁體中文

### 核心概念

**Email 轉自傳**是一個創新專案，結合三大元素：
1. **Email（電子郵件）** - 自然、零摩擦的紀錄方式
2. **LLM（大型語言模型）** - 智慧整理、主題偵測、敘事合成
3. **Autobiography（自傳）** - 結構化、有意義的人生故事輸出

### 運作理念

人們每天都在寫 Email - 寄給朋友、家人、同事，甚至自己作為筆記。如果我們能將這些 Email 轉化為連貫的自傳，而無需要求任何人養成新習慣呢？

### 運作方式

```
┌─────────────────────────────────────────────────────────────┐
│                    1. 撰寫 Email                            │
│  ────────────────────────────────────────────────────────  │
│  透過 Email 自然紀錄：                                       │
│  • 寄信給自己記錄人生事件                                   │
│  • 使用專用地址                                             │
│  • 轉發現有 Email                                          │
└─────────────────────────────────────────────────────────────┘
                            ↓
┌─────────────────────────────────────────────────────────────┐
│                    2. AI 處理                              │
│  ────────────────────────────────────────────────────────  │
│  LLM 驅動的分析：                                            │
│  • 主題提取（事業、感情、成長等）                           │
│  • 情感弧線偵測                                            │
│  • 時序組織                                                │
│  • 關鍵里程碑識別                                          │
│  • 章節生成                                                │
└─────────────────────────────────────────────────────────────┘
                            ↓
┌─────────────────────────────────────────────────────────────┐
│                 3. 探索與分享                               │
│  ────────────────────────────────────────────────────────  │
│  多種瀏覽模式：                                              │
│  • 依章節閱讀（敘事流暢）                                    │
│  • 依主題瀏覽（分類視圖）                                    │
│  • 互動時間軸（時間順序）                                   │
│  • 匯出：PDF、EPUB、Markdown                               │
└─────────────────────────────────────────────────────────────┘
```

### 特色功能

#### 零摩擦力
- 無需安裝新 App
- 無需養成新習慣
- 使用您已熟悉的 Email 客戶端
- 支援 Gmail、Outlook、Apple Mail 等

#### AI 驅動整理
- **主題偵測**：自動將 Email 依主題分類（事業、感情、旅行、學習、健康等）
- **情感弧線**：追蹤情感旅程與個人成長
- **智慧分組**：相關 Email 聚集成有意義的章節
- **標題生成**：AI 根據內容建議章節標題
- **摘要創建**：生成章節摘要以便快速導航

#### 多元視角
- **章節視圖**：像閱讀書籍一樣，有 AI 生成的標題
- **主題視圖**：依主題和類別探索
- **時間軸視圖**：按時間順序瀏覽人生時刻
- **搜尋**：即時找到任何回憶

#### 匯出選項
- PDF（列印就緒）
- EPUB（電子書友善）
- Markdown（可攜、可版本控制）

#### 隱私優先
- 所有資料儲存在本地或您選擇的加密保險庫
- 資料永遠屬於您
- 選項：自架版本以獲得完全控制權

### 技術架構

（參見上方英文版本的技術架構圖）

### 開發計畫

#### 階段 1：MVP（最小可行產品）
- [ ] 後端 API 與 Email 輸入
- [ ] 基礎 LLM 整合用於主題偵測
- [ ] 簡單章節生成
- [ ] 前端與章節視圖
- [ ] 支援一個 Email 提供者（Gmail）

#### 階段 2：增強功能
- [ ] 多個 Email 提供者（Outlook、一般 IMAP）
- [ ] 主題視圖與時間軸視圖
- [ ] 匯出至 PDF
- [ ] 進階 LLM 功能（情感弧線、里程碑）
- [ ] 搜尋功能

#### 階段 3：優化與部署
- [ ] 匯出至 EPUB 與 Markdown
- [ ] 自架選項
- [ ] 響應式設計
- [ ] 使用者驗證
- [ ] 隱私控制

#### 階段 4：進階功能（探索性）
- [ ] AI 敘事增強（為更好的故事重寫）
- [ ] 語音支援（口述 Email）
- [ ] 照片附件整合
- [ ] 協作（邀請家人貢獻）
- [ ] AI 驅動的洞察與模式

### 安裝與設定（開發）

```bash
# 複製儲存庫
git clone https://github.com/awesomejerry/email-to-autobiography.git
cd email-to-autobiography

# 安裝依賴
npm install

# 設定環境變數
cp .env.example .env
# 編輯 .env 填入您的 API 金鑰

# 執行開發伺服器
npm run dev
```

### 貢獻

這是一個創意探索專案。歡迎提出想法、建議和貢獻！

### 授權

MIT License - 歡迎探索並在此想法上建構。

---

## 快速連結

- **Landing Page**: [Live Demo](https://awesomejerry.github.io/email-to-autobiography/)
- **GitHub Repository**: [github.com/awesomejerry/email-to-autobiography](https://github.com/awesomejerry/email-to-autobiography)

---

## Acknowledgements 致謝

Built by [AwesomeJerry](https://github.com/awesomejerry) as an exploration of memory, storytelling, and AI.

由 [AwesomeJerry](https://github.com/awesomejerry) 打造，探索記憶、敘事與 AI 的交匯點。
