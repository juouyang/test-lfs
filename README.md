當建立好新專案後，以下是上傳第一個 Git LFS 檔案 的步驟指令整理：

---

## 上傳第一個 Git LFS 檔案的流程

### 🧰 前提準備（只需一次）

```
# 安裝 git-lfs
brew install git-lfs
```

```
# 初始化 git-lfs
git lfs install
```

---

### 🚀 建立或進入專案資料夾

```
git clone https://github.com/juouyang/test-lfs.git
cd test-lfs
```

---

### 📝 建立 .gitattributes 並追蹤檔案類型（例如 .zip）

```
git lfs track "*.zip"
git add .gitattributes
git commit -m "track .zip files via Git LFS"
```

---

### 📁 建立一個測試檔案

```
dd if=/dev/urandom of=testfile.zip bs=1M count=5
git add testfile.zip
git commit -m "add testfile.zip using Git LFS"
```

---

### ☁️ 推送到 GitHub

```
git push origin main
```

✅ 驗證是否成功

執行：
  
```
git lfs ls-files
```
    
應該會看到類似：
      
```
abc123def456 * testfile.zip
```

