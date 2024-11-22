---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Giới thiệu về Quản trị Mã Nguồn

## 1. Khái niệm

Quản trị mã nguồn (Source Control Management - SCM) là quá trình quản lý các thay đổi đối với mã nguồn của phần mềm. SCM giúp theo dõi lịch sử thay đổi, quản lý các phiên bản khác nhau của mã nguồn và hỗ trợ làm việc nhóm hiệu quả. 

## 2. Lợi ích của Quản trị Mã Nguồn

### 2.1. Theo dõi lịch sử thay đổi
SCM cho phép theo dõi mọi thay đổi được thực hiện trên mã nguồn, từ đó giúp dễ dàng xác định nguyên nhân gây ra lỗi và khôi phục lại phiên bản trước đó nếu cần thiết.

### Ví dụ
Giả sử một lập trình viên phát hiện ra một lỗi trong mã nguồn của dự án. Nhờ có SCM, họ có thể:

- Xem lại lịch sử thay đổi để xác định ai đã thực hiện thay đổi gần đây nhất.
- Kiểm tra chi tiết các thay đổi để tìm ra nguyên nhân gây ra lỗi.
- Khôi phục lại phiên bản trước đó của mã nguồn để tạm thời giải quyết vấn đề trong khi tìm cách sửa lỗi.

Ví dụ, trong Git, bạn có thể sử dụng các lệnh sau để theo dõi lịch sử thay đổi và khôi phục lại phiên bản trước đó:

```bash
# Xem lịch sử thay đổi
git log

# Xem chi tiết thay đổi của một commit cụ thể
git show <commit-id>

# Khôi phục lại phiên bản trước đó
git checkout <commit-id>
```

### 2.2. Làm việc nhóm hiệu quả
SCM cho phép nhiều lập trình viên làm việc trên cùng một dự án mà không lo lắng về việc ghi đè lên mã nguồn của nhau. Mỗi lập trình viên có thể làm việc trên nhánh riêng của mình và sau đó hợp nhất các thay đổi lại với nhau một cách dễ dàng.

### Ví dụ
Giả sử một nhóm phát triển phần mềm gồm ba lập trình viên: A, B và C. Mỗi người làm việc trên một tính năng khác nhau của dự án. Nhờ có SCM, họ có thể:

- A tạo một nhánh mới từ nhánh chính để phát triển tính năng X.
- B tạo một nhánh mới từ nhánh chính để phát triển tính năng Y.
- C tạo một nhánh mới từ nhánh chính để phát triển tính năng Z.

Sau khi hoàn thành, họ có thể hợp nhất các nhánh của mình vào nhánh chính mà không lo lắng về việc ghi đè lên mã nguồn của nhau. Nếu có xung đột, SCM sẽ thông báo và giúp họ giải quyết xung đột đó.

![Git branch](../_static/figures/fig1-gitworkflow.webp)

### 2.3. Quản lý phiên bản
SCM cho phép tạo và quản lý các phiên bản khác nhau của mã nguồn, giúp dễ dàng triển khai các bản phát hành (release) và duy trì các phiên bản cũ.

### 2.4. Tăng cường bảo mật
SCM cung cấp các cơ chế kiểm soát truy cập, giúp bảo vệ mã nguồn khỏi các truy cập trái phép và đảm bảo tính toàn vẹn của mã nguồn.

## 3. Các công cụ phổ biến trong Quản trị Mã Nguồn

### 3.1. Git
Git là một hệ thống quản trị mã nguồn phân tán, được sử dụng rộng rãi trong cộng đồng phát triển phần mềm. Git cho phép lập trình viên làm việc offline và đồng bộ hóa mã nguồn khi có kết nối mạng.


### 3.2. Subversion (SVN)
Subversion là một hệ thống quản trị mã nguồn tập trung, cho phép quản lý mã nguồn trên một máy chủ duy nhất. SVN phù hợp với các dự án có quy mô nhỏ và trung bình.

### 3.3. Mercurial
Mercurial là một hệ thống quản trị mã nguồn phân tán, tương tự như Git. Mercurial được thiết kế để dễ sử dụng và có hiệu suất cao.

### 3.4. Perforce
Perforce là một hệ thống quản trị mã nguồn tập trung, được sử dụng chủ yếu trong các dự án lớn và phức tạp. Perforce cung cấp các tính năng mạnh mẽ và linh hoạt.

## 4. Sơ đồ minh họa

Dưới đây là sơ đồ minh họa quá trình quản trị mã nguồn với Git:


![Git Workflow](../_static/figures/fig2-gitflow.png)


### 4.1. Working Directory
Working Directory là thư mục chứa mã nguồn mà bạn đang làm việc. Đây là nơi bạn thực hiện các thay đổi đối với mã nguồn của dự án.

### 4.2. Staging Area
Staging Area (hay còn gọi là Index) là khu vực tạm thời lưu trữ các thay đổi mà bạn muốn commit. Bạn có thể chọn những thay đổi cụ thể để thêm vào Staging Area trước khi thực hiện commit.

### 4.3. Remote Repository
Remote Repository là kho mã nguồn trên máy chủ từ xa, nơi bạn có thể đẩy (push) các thay đổi từ local repository lên và kéo (pull) các thay đổi từ remote repository về.

### Quản trị mã nguồn với Git
Quản trị mã nguồn với Git bao gồm các bước cơ bản sau: 

1. **Khởi tạo Git Repository**
    ```bash
    git init
    ```

2. **Thêm tệp vào Staging Area**
    ```bash
    git add <file>
    ```

3. **Commit các thay đổi**
    ```bash
    git commit -m "Mô tả thay đổi"
    ```

4. **Kết nối với Remote Repository**
    ```bash
    git remote add origin <remote-url>
    ```

5. **Đẩy các thay đổi lên Remote Repository**
    ```bash
    git push origin main
    ```

6. **Kéo các thay đổi từ Remote Repository về**
    ```bash
    git pull origin main
    ```
Ảnh bên dưới là cách thức các lập trình viên cùng làm việc trong một dự án thông qua Git.

![Git Workflow](../_static/figures/fig3-gitcolab.png)


## 5. Kết luận

Quản trị mã nguồn là một phần quan trọng trong quá trình phát triển phần mềm. Việc sử dụng các công cụ SCM giúp tăng cường hiệu quả làm việc nhóm, quản lý phiên bản và bảo mật mã nguồn. Các công cụ phổ biến như Git, SVN, Mercurial và Perforce đều có những ưu điểm riêng, phù hợp với các nhu cầu khác nhau của dự án.
