# qqlinux-week3

「Linux 實務與應用」WEEK3：Docker 系統的備份、還原與主機安全——學生下載檔（v2.1）。

| 檔案 | 用途 |
|---|---|
| `backup.sh` | 備份 WordPress 資料庫、`wp-data` Volume、設定檔與憑證，並產生檢查碼與比對清單 |
| `restore.sh` | 在 Volume 已不存在時，從 `backup.sh` 的備份還原，並自動比對檔案與文章 |
| `compose.yml` | WEEK3 版：固定 Image 版本、資料庫健康檢查、固定 Volume 名稱 |

## 下載方式（在 VM 的 `~/webstack` 執行）

```bash
cd ~/webstack
BASE=https://raw.githubusercontent.com/qqnice/qqlinux-week3/main
curl -fsSLO "$BASE/backup.sh"
curl -fsSLO "$BASE/restore.sh"
chmod +x backup.sh restore.sh
```

`compose.yml` 請依手冊 STEP 4 下載成 `compose.yml.new`，檢查通過後再替換，不要直接覆蓋。

## 注意

- 下載的腳本執行前，請先用 `less` 閱讀一遍。
- 備份檔含有資料庫密碼與憑證私鑰，**不要**上傳到 GitHub 或任何公開位置。
- 操作步驟請依課程的學生實作手冊進行。
