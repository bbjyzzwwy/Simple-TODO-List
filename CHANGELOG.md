# Changelog

All notable changes to Tiny TODO List are documented in this file.

## [0.1.2] - 2026-06-20

### Added

- Manual **Sync now** button (🔄) in the toolbar, with syncing / success / failure feedback.
- Setting `tinyTodoList.autoSync`: automatically push your changes after you finish editing, and pull others' changes when the window regains focus.
- Setting `tinyTodoList.periodicPullSeconds`: optional periodic pull for when the window stays focused for long stretches (off by default).

### Changed

- Sync is now event-driven: your changes are pushed shortly after you finish editing (debounced) instead of polling on a fixed interval — lighter on Settings Sync and avoids rate-limiting.
- Incoming changes are pulled automatically when the VS Code window regains focus (throttled).

### Fixed

- Syncing no longer interrupts a TODO item you are currently editing; remote updates are deferred and applied after you finish.

## [0.1.1] - 2026-06-18

### Added

- Cross-device TODO sync via VS Code Settings Sync, with automatic refresh.

## [0.1.0] - 2026-06-14

### Added

- Initial VS Code Marketplace-ready release.
- Sidebar TODO list powered by a WebviewView.
- Grouped TODO management with collapsible groups.
- TODO and Finished tabs with completion tracking.
- Inline editing, keyboard navigation, multi-select, and delete shortcuts.
- Theme-aware webview UI.
- Marketplace icon and Activity Bar icon.

---

# 更新日志

Tiny TODO List 的重要变更都会记录在此文件中。

## [0.1.2] - 2026-06-20

### 新增

- 工具栏新增手动「立即同步」按钮（🔄），带同步中 / 成功 / 失败反馈。
- 新增设置 `tinyTodoList.autoSync`：编辑完成后自动推送你的改动，并在窗口重新获得焦点时拉取他人的改动。
- 新增设置 `tinyTodoList.periodicPullSeconds`：可选的周期性拉取，适合长时间停留在同一窗口的情况（默认关闭）。

### 变更

- 同步改为事件驱动：编辑完成后短暂防抖即推送，不再按固定间隔轮询——更省 Settings Sync 资源，并避免被限流。
- 窗口重新获得焦点时自动拉取远端变更（带节流）。

### 修复

- 同步不再打断正在编辑的 TODO 项；远端更新会被暂存，待你编辑完成后再应用。

## [0.1.1] - 2026-06-18

### 新增

- 通过 VS Code Settings Sync 支持跨设备 TODO 同步，并自动刷新。

## [0.1.0] - 2026-06-14

### 新增

- 初始 VS Code 市场发布版本。
- 基于 WebviewView 的侧边栏 TODO 列表。
- 支持可折叠分组的 TODO 管理。
- TODO 和 Finished 标签页，以及完成状态跟踪。
- 支持内联编辑、键盘导航、多选和删除快捷键。
- 适配 VS Code 主题的 Webview UI。
- Marketplace 图标和 Activity Bar 图标。
