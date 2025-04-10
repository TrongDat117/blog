---
Source: 
cssclasses: 
tags: 
aliases: 
topics: "[[git]]"
---
thứ hai-07-04-2025  21:07:20

---
### 🛠️ **1. Khởi tạo Git repo trong thư mục Obsidian**
```bash
git init
```
### 📦 **2. Thêm file và commit**
```bash
git add .                  # Thêm tất cả file
git commit -m "Nội dung commit"
```
### 🔗 **3. Thêm remote**
```bash
git remote add origin git@git.trongdat117.xyz:USERNAME/REPO.git
```
🔁 Nếu cần đổi lại:
```bash
git remote set-url origin git@git.trongdat117.xyz:USERNAME/REPO.git
```
### 🚀 **4. Push lần đầu**
```bash
git push -u origin main
```
### 🔄 **5. Pull về để cập nhật thay đổi**
```bash
git pull origin main
```
### 👀 **6. Kiểm tra trạng thái**
```bash
git status
```
### 📝 **7. Sửa commit gần nhất (nếu quên .gitignore chẳng hạn)**
```bash
git commit --amend
```
### 💥 **9. Xóa remote repo (cần admin quyền)**
```bash
# Từ Gitea UI: Repository → Settings → Danger Zone → Delete this repository
```
### 💻 **10. Kiểm tra SSH hoạt động**
```bash
ssh -T git@git.trongdat117.xyz -p 2222
```
### 📝 **11. Kiểm tra file có đang tracked ko (dc theo dõi)**
```bash
git check-ignore -v .obsidian/workspace.json
```
*ví dụ cho file workspace.json*
### 📝 **12. Xóa file khỏi Git (ko xóa khỏi máy)**
```bash
git rm --cached .obsidian/workspace.json
```
`--cached` nghĩa là **xóa khỏi Git, không xóa khỏi ổ cứng**
**Commit thay đổi**
```bash
git commit -m "Stop tracking workspace.json"
git push
```
### 🔁 **Làm sạch toàn repo để áp dụng `.gitignore` lại từ đầu:**
```bash
git rm -r --cached .
git add .
git commit -m "Reapply .gitignore rules"
```
**Cẩn thận:** lệnh này sẽ bỏ theo dõi toàn bộ file trong repo, rồi thêm lại những file **không bị ignore**.