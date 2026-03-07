# OpenList 繁體中文本地化專案

## 前言

[OpenList](https://github.com/OpenListTeam/OpenList) 是一款強大且開源的檔案列表程式，支援多種儲存空間，是 [Alist](https://github.com/AlistGo/alist) 的一個社群驅動替代品。 

目前 OpenList 的多國語言支援（i18n）仍在開發中。<br>
雖然官方已將其納入未來規劃，但我們相信社群的力量可以加速實現完整的繁體中文介面。

本專案使用 OpenCC 搭配 GitHub Actions Workflow 進行自動化翻譯，<br>
旨在為繁體中文使用者提供更友善、無障礙的使用體驗。

---

## 如何使用？

前往本專案的 [Releases 頁面](https://github.com/HongyiHank/OpenList_zh-TW_L10n/releases/latest)下載符合您作業系統的可執行檔<br>
解壓縮後替換您電腦中原有的執行檔（請記得重新命名）。

目前本專案僅提供以下兩種系統架構的可執行檔：

* Linux amd64 (musl)
* Windows amd64

若您需要其他系統或架構的版本，歡迎 Fork 本專案，並修改 `.github/workflows/build.yml` 中的 `target` 設定。

結構如下：

```
jobs:
  build:
    strategy:
      matrix:
        └── target: [linux-amd64-musl, windows-amd64]
              │
              └── 💡 在此新增或修改您的目標平台（例如：linux-arm64-musl）
```

修改完成後，可前往 Actions 頁面重新編譯。

<details>
  <summary>支援的系統架構如下：</summary>
  
### 1. Linux(glibc)

- `linux-386`
- `linux-amd64`
- `linux-arm-5`
- `linux-arm-6`
- `linux-arm-7`
- `linux-arm64`
- `linux-mips`
- `linux-mipsle`
- `linux-mips64`
- `linux-mips64le`
- `linux-ppc64le`
- `linux-riscv64`
- `linux-loong64`
- `linux-loong64-abi1.0`
- `linux-s390x`

### 2. Linux(musl)

- `linux-amd64-musl`
- `linux-arm64-musl`
- `linux-arm-musleabi`
- `linux-arm-musleabihf`
- `linux-armel-musleabi`
- `linux-armel-musleabihf`
- `linux-armv5l-musleabi`
- `linux-armv5l-musleabihf`
- `linux-armv6-musleabi`
- `linux-armv6-musleabihf`
- `linux-armv7l-musleabihf`
- `linux-armv7m-musleabi`
- `linux-armv7r-musleabihf`
- `linux-mips-musl`
- `linux-mips64-musl`
- `linux-mips64le-musl`
- `linux-mipsle-musl`
- `linux-ppc64le-musl`
- `linux-riscv64-musl`
- `linux-s390x-musl`
- `linux-loong64-musl`

### 3. macOS(Darwin)

- `darwin-amd64`
- `darwin-arm64`

### 4. Windows

- `windows-386`
- `windows-amd64`
- `windows-arm64`
- `windows7-386`
- `windows7-amd64`

### 5. Android

- `android-386`
- `android-amd64`
- `android-arm`
- `android-arm64`

### 6. FreeBSD

- `freebsd-386`
- `freebsd-amd64`
- `freebsd-arm64`

</details>

---

## 如何協助我們？

儘管本專案使用了強大的 OpenCC，但作為機器轉換工具，仍可能出現部分翻譯不自然或不準確的情況。<br>
若您發現翻譯問題，歡迎提交 Pull Request 協助修正。

此外，如果您發現 GitHub Actions Workflow 有可優化之處，也歡迎提出 Pull Request。

---

## 使用到的專案

- [OpenList](https://github.com/OpenListTeam/OpenList)
- [OpenList-Frontend](https://github.com/OpenListTeam/OpenList-Frontend)
- [OpenCC](https://github.com/BYVoid/OpenCC)