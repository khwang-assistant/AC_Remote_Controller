# AI Assistant Instructions for AC Remote Controller Project

Whenever this workspace is initialized, the AI assistant should follow these rules:

## 1. Auto-Load Project State
- Immediately check if `./docs/brainstorm_notes.md` exists in the workspace.
- Read the contents of `./docs/brainstorm_notes.md` to understand the current architecture, decisions, and current TODOs.

## 2. Proactive Documentation Maintenance
- During the brainstorming and coding sessions, after any significant decision is reached, a component is designed, or a task is finished, proactively update `./docs/brainstorm_notes.md` to reflect the latest status.
- Keep the document clean, highly structured, and readable.

## 3. Development Guidelines
- Maintain the architectural boundaries specified in the documentation.
- Document any code changes and design rationales clearly.
- **Use Relative Paths Only**: Never use absolute paths (such as `/Users/...` or `file:///...`) in any project documentation or files; always use relative paths (e.g., `./docs/system_spec.md`).

## 4. 專案任務追蹤與運維規範 (Project Management & Task Tracking SOP)
- **公開/私密邊界 (Public/Private Boundary)**：
  - 本專案為公開開源庫。所有內部開發任務、待辦、採購追蹤、未成熟之想法，統一在私密中樞 `khwang-assistant/agent-hub` 開立 Issue，並標註標籤 `project: ac-remote`。
  - 本機對應之運維目錄為 `../agent-hub/ac-remote-controller/`。
- **狀態巡邏與維護 (Patrol & Status Maintenance)**：
  - 任務驗收與狀態異動遵循 `../agent-hub/ac-remote-controller/AGENT_PATROL_RULES.md` 的兩大核心原則（嚴格結案、遇歧義請示）。
  - 執行巡邏時直接調用專案腳本：`python3 ../agent-hub/ac-remote-controller/patrol.py`。
