# Quản lý mã nguồn với GitHub

## 1. Giới thiệu về GitHub
### GitHub là gì?

GitHub là một nền tảng lưu trữ mã nguồn và quản lý phiên bản dựa trên Git. Nó cung cấp các công cụ để lập trình viên có thể hợp tác, theo dõi thay đổi, và quản lý các dự án phần mềm một cách hiệu quả.  GitHub cũng hỗ trợ các tính năng như pull request, issue tracking, và continuous integration.

![GitHub Logo](https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png)


### Lịch sử phát triển của GitHub.

GitHub được thành lập vào năm 2008 bởi Tom Preston-Werner, Chris Wanstrath, PJ Hyett, và Scott Chacon. Ban đầu, GitHub được phát triển như một nền tảng để lưu trữ và quản lý mã nguồn dựa trên Git, một hệ thống quản lý phiên bản phân tán do Linus Torvalds tạo ra.

- **2008**: GitHub chính thức ra mắt.
- **2012**: GitHub đạt mốc 1 triệu repository.
- **2014**: GitHub đạt mốc 10 triệu repository.
- **2018**: Microsoft mua lại GitHub với giá 7.5 tỷ USD. Thương vụ này giúp Microsoft củng cố vị thế trong cộng đồng mã nguồn mở và cung cấp thêm nguồn lực để phát triển GitHub.
- **2020**: GitHub giới thiệu GitHub Copilot, một công cụ AI hỗ trợ lập trình viên viết mã nhanh hơn và hiệu quả hơn, được phát triển dựa trên mô hình ngôn ngữ của OpenAI. 

GitHub đã phát triển từ một nền tảng lưu trữ mã nguồn đơn giản thành một hệ sinh thái toàn diện cho các lập trình viên và các dự án phần mềm trên toàn thế giới.

- Các tính năng chính:
  - Lưu trữ mã nguồn.
  - Cộng tác nhóm.
  - Tích hợp với các công cụ CI/CD.

## 2. Bắt đầu với GitHub
### 2.1. Tạo tài khoản GitHub

1. Truy cập trang chủ GitHub: [https://github.com](https://github.com).
2. Nhấp vào nút **Sign up** ở góc trên bên phải.
3. Nhập địa chỉ email của bạn và nhấp vào **Continue**.
4. Tạo mật khẩu và nhấp vào **Continue**.
5. Chọn tên người dùng và nhấp vào **Continue**.
6. Xác nhận bạn không phải là robot và nhấp vào **Create account**.
7. Kiểm tra email để xác nhận tài khoản của bạn.

### Thiết lập thông tin người dùng

1. Đăng nhập vào tài khoản GitHub của bạn.
2. Nhấp vào ảnh đại diện của bạn ở góc trên bên phải và chọn **Settings**.
3. Trong mục **Profile**, bạn có thể cập nhật tên, bio, ảnh đại diện, và các thông tin khác.
4. Nhấp vào **Update profile** để lưu các thay đổi.

### 2.2. Thiết lập GitHub trên máy cục bộ

1. **Cài đặt Git:**
  - Truy cập trang [Git Downloads](https://git-scm.com/downloads) và tải phiên bản Git phù hợp với hệ điều hành của bạn.
  - Thực hiện cài đặt Git theo hướng dẫn trên trang web.

2. **Cấu hình Git:**
  - Mở terminal (Command Prompt, PowerShell, hoặc Git Bash).
  - Thiết lập tên người dùng và email của bạn:
    ```sh
    git config --global user.name "Tên của bạn"
    git config --global user.email "email@example.com"
    ```
    ### Đăng nhập GitHub trên Windows

    1. **Sử dụng Git Credential Manager:**
      - Git Credential Manager (GCM) là một công cụ giúp bạn quản lý thông tin đăng nhập GitHub trên Windows một cách an toàn và tiện lợi.
      - Khi cài đặt Git trên Windows, GCM thường được cài đặt kèm theo. Nếu chưa có, bạn có thể tải và cài đặt từ [Git Credential Manager](https://github.com/GitCredentialManager/git-credential-manager).

    2. **Cấu hình Git Credential Manager:**
      - Mở terminal (Command Prompt, PowerShell, hoặc Git Bash).
      - Thiết lập GCM làm trình quản lý thông tin đăng nhập mặc định:
        ```sh
        git config --global credential.helper manager-core
        ```

    3. **Đăng nhập GitHub:**
      - Khi bạn thực hiện các lệnh Git yêu cầu xác thực (như `git push` hoặc `git pull`), GCM sẽ tự động mở một cửa sổ đăng nhập GitHub.
      - Nhập thông tin tài khoản GitHub của bạn và xác nhận đăng nhập.
      - GCM sẽ lưu trữ thông tin đăng nhập của bạn một cách an toàn để sử dụng cho các lần sau.

    4. **Sử dụng Personal Access Token (PAT):**
      - Nếu bạn không muốn sử dụng GCM, bạn có thể tạo một Personal Access Token trên GitHub và sử dụng nó như mật khẩu.
      - Truy cập [GitHub Settings](https://github.com/settings/tokens) và tạo một token mới với các quyền cần thiết.
      - Khi Git yêu cầu mật khẩu, nhập token này thay vì mật khẩu GitHub của bạn.


## 3. Quản lý repository trên GitHub
### 3.1. Tạo repository mới
#### Tạo repository trên giao diện web.
1. Đăng nhập vào tài khoản GitHub của bạn.
2. Nhấp vào biểu tượng **+** ở góc trên bên phải và chọn **New repository**.

![alt text](image.png)


3. Điền thông tin cho repository mới:
  - **Repository name**: Tên của repository.
  - **Description**: Mô tả ngắn gọn về repository (không bắt buộc).
  - **Public/Private**: Chọn chế độ công khai hoặc riêng tư cho repository.
  - **Initialize this repository with a README**: Chọn tùy chọn này nếu bạn muốn tạo một tệp README.md mặc định.

4. Nhấp vào **Create repository** để hoàn tất việc tạo repository mới.

#### Tạo repository bằng dòng lệnh.

1. Mở terminal (Command Prompt, PowerShell, hoặc Git Bash).
2. Điều hướng đến thư mục bạn muốn tạo repository mới:
  ```sh
  cd đường/dẫn/đến/thư/mục
  ```
3. Khởi tạo repository Git mới:
  ```sh
  git init
  ```
4. Thêm các tệp vào repository:
  ```sh
  git add .
  ```
5. Tạo commit đầu tiên:
  ```sh
  git commit -m "Initial commit"
  ```
6. Thêm remote repository trên GitHub:
  ```sh
  git remote add origin https://github.com/tên-người-dùng/tên-repository.git
  ```
7. Đẩy thay đổi lên GitHub:
  ```sh
  git push -u origin master
  ```


### 3.2. Kết nối repository cục bộ với GitHub

#### Kết nối repository cục bộ với GitHub

1. Mở terminal (Command Prompt, PowerShell, hoặc Git Bash).
2. Điều hướng đến thư mục chứa repository cục bộ của bạn:
  ```sh
  cd đường/dẫn/đến/thư/mục
  ```
3. Thêm remote repository trên GitHub:
  ```sh
  git remote add origin https://github.com/tên-người-dùng/tên-repository.git
  ```
4. Xác nhận remote repository đã được thêm:
  ```sh
  git remote -v
  ```


### 3.3. Đẩy thay đổi lên GitHub

1. Mở terminal (Command Prompt, PowerShell, hoặc Git Bash).
2. Điều hướng đến thư mục chứa repository cục bộ của bạn:
  ```sh
  cd đường/dẫn/đến/thư/mục
  ```
3. Thêm các thay đổi vào staging area:
  ```sh
  git add .
  ```
4. Tạo commit với thông điệp mô tả thay đổi:
  ```sh
  git commit -m "Mô tả thay đổi của bạn"
  ```
5. Đẩy thay đổi lên remote repository trên GitHub:
  ```sh
  git push origin master
  ```

### 3.4. Sao chép (clone) repository từ GitHub về máy cục bộ.

1. Mở terminal (Command Prompt, PowerShell, hoặc Git Bash).
2. Điều hướng đến thư mục bạn muốn sao chép repository về:
  ```sh
  cd đường/dẫn/đến/thư/mục
  ```
3. Sử dụng lệnh `git clone` để sao chép repository:
  ```sh
  git clone https://github.com/tên-người-dùng/tên-repository.git
  ```
4. Sau khi sao chép xong, điều hướng vào thư mục repository vừa được sao chép:
  ```sh
  cd tên-repository
  ```


## 4. Làm việc nhóm với GitHub
### 4.1. Thêm cộng tác viên vào repository

1. Đăng nhập vào tài khoản GitHub của bạn.
2. Điều hướng đến repository mà bạn muốn thêm cộng tác viên.
3. Nhấp vào tab **Settings** ở phía trên của trang repository.
4. Trong menu bên trái, chọn **Collaborators**.
![
GitHub Repository Settings](https://docs.github.com/assets/cb-28260/mw-1440/images/help/repository/repo-actions-settings.webp)
5. Nhập tên người dùng GitHub hoặc email của người bạn muốn thêm làm cộng tác viên.
6. Nhấp vào **Add collaborator**.
7. Người được mời sẽ nhận được một email thông báo và cần chấp nhận lời mời để trở thành cộng tác viên.


#### Quản lý quyền truy cập

1. Đăng nhập vào tài khoản GitHub của bạn.
2. Điều hướng đến repository mà bạn muốn quản lý quyền truy cập.
3. Nhấp vào tab **Settings** ở phía trên của trang repository.
4. Trong menu bên trái, chọn **Manage access**.
5. Tại đây, bạn có thể xem danh sách các cộng tác viên và quyền truy cập của họ.
6. Để thay đổi quyền truy cập, nhấp vào biểu tượng bút chì bên cạnh tên của cộng tác viên và chọn quyền truy cập mới (Read, Write, hoặc Admin).
7. Nhấp vào **Save** để lưu các thay đổi.


### 4.2. Pull Request
- Pull Request là gì?

Pull Request (PR) là một tính năng của GitHub cho phép bạn thông báo cho người khác về những thay đổi mà bạn đã đẩy lên một branch trong repository. Khi bạn mở một Pull Request, bạn đang yêu cầu người khác xem xét và hợp nhất (merge) những thay đổi của bạn vào branch chính (thường là `main` hoặc `master`).

### Tầm quan trọng của Pull Request trong các dự án phần mềm

- **Kiểm tra và đánh giá mã nguồn:** Pull Request cho phép các thành viên trong nhóm xem xét và đánh giá mã nguồn trước khi hợp nhất vào branch chính. Điều này giúp phát hiện và sửa lỗi sớm, đảm bảo chất lượng mã nguồn.
- **Cộng tác và giao tiếp:** Pull Request là một công cụ quan trọng để giao tiếp giữa các thành viên trong nhóm. Nó cho phép thảo luận về các thay đổi, đề xuất cải tiến và giải quyết các vấn đề kỹ thuật.
- **Lịch sử thay đổi:** Pull Request cung cấp một lịch sử chi tiết về các thay đổi được thực hiện, bao gồm các commit, bình luận và quyết định liên quan. Điều này giúp theo dõi và quản lý các thay đổi dễ dàng hơn.
- **Quy trình làm việc chuẩn hóa:** Pull Request giúp chuẩn hóa quy trình làm việc trong các dự án phần mềm, đặc biệt là các dự án nguồn mở. Nó đảm bảo rằng mọi thay đổi đều được xem xét kỹ lưỡng trước khi được hợp nhất vào branch chính.

### Tầm quan trọng của Pull Request trong phần mềm nguồn mở

- **Đóng góp từ cộng đồng:** Pull Request là cách chính để các nhà phát triển bên ngoài đóng góp vào các dự án nguồn mở. Nó cho phép các nhà phát triển gửi các bản vá lỗi, tính năng mới và cải tiến cho dự án.
- **Quản lý đóng góp:** Pull Request giúp các maintainer của dự án nguồn mở quản lý và xem xét các đóng góp từ cộng đồng một cách hiệu quả. Nó cung cấp một quy trình rõ ràng để xem xét, thảo luận và hợp nhất các thay đổi.
- **Minh bạch và công khai:** Pull Request là công khai và minh bạch, cho phép mọi người trong cộng đồng theo dõi và tham gia vào quá trình phát triển của dự án. Điều này thúc đẩy sự hợp tác và chia sẻ kiến thức trong cộng đồng nguồn mở.

### Quy trình tạo và review Pull Request


#### Khi nào thì tạo Pull Request

- **Khi hoàn thành một tính năng mới hoặc sửa lỗi:** Sau khi bạn đã hoàn thành việc phát triển một tính năng mới hoặc sửa lỗi trên một branch riêng, bạn nên tạo Pull Request để yêu cầu xem xét và hợp nhất các thay đổi vào branch chính.
- **Khi cần sự xem xét từ người khác:** Nếu bạn muốn nhận phản hồi hoặc sự xem xét từ các thành viên khác trong nhóm về các thay đổi của mình, bạn có thể tạo Pull Request để bắt đầu quá trình thảo luận và đánh giá.
- **Khi làm việc theo quy trình chuẩn hóa:** Trong nhiều dự án, đặc biệt là các dự án nguồn mở, việc tạo Pull Request là một phần của quy trình làm việc chuẩn hóa để đảm bảo mọi thay đổi đều được xem xét kỹ lưỡng trước khi hợp nhất vào branch chính.

#### Ai có quyền chấp nhận hoặc từ chối Pull Request

- **Maintainer hoặc người quản lý dự án:** Trong các dự án nguồn mở, maintainer hoặc người quản lý dự án thường có quyền chấp nhận hoặc từ chối Pull Request. Họ chịu trách nhiệm xem xét các thay đổi và quyết định xem chúng có nên được hợp nhất vào branch chính hay không.
- **Thành viên nhóm có quyền truy cập:** Trong các dự án nội bộ hoặc nhóm, các thành viên có quyền truy cập phù hợp (thường là quyền Write hoặc Admin) có thể chấp nhận hoặc từ chối Pull Request. Quyền này thường được thiết lập bởi người quản lý dự án hoặc chủ sở hữu repository.
- **Người được chỉ định:** Trong một số trường hợp, một hoặc nhiều thành viên cụ thể có thể được chỉ định để xem xét và chấp nhận Pull Request. Điều này giúp đảm bảo rằng các thay đổi được xem xét bởi những người có kiến thức chuyên môn phù hợp.

Quyền chấp nhận hoặc từ chối Pull Request thường được thiết lập dựa trên vai trò và trách nhiệm của các thành viên trong dự án, đảm bảo rằng mọi thay đổi đều được xem xét kỹ lưỡng trước khi được hợp nhất vào branch chính.

#### Tạo Pull Request

1. **Tạo một branch mới:**
  - Mở terminal (Command Prompt, PowerShell, hoặc Git Bash).
  - Điều hướng đến thư mục chứa repository cục bộ của bạn:
    ```sh
    cd đường/dẫn/đến/thư/mục
    ```
  - Tạo một branch mới và chuyển sang branch đó:
    ```sh
    git checkout -b tên-branch
    ```

2. **Thực hiện các thay đổi:**
  - Thực hiện các thay đổi cần thiết trong mã nguồn của bạn.

3. **Commit các thay đổi:**
  - Thêm các thay đổi vào staging area:
    ```sh
    git add .
    ```
  - Tạo commit với thông điệp mô tả thay đổi:
    ```sh
    git commit -m "Mô tả thay đổi của bạn"
    ```

4. **Đẩy branch lên GitHub:**
  - Đẩy branch mới lên remote repository trên GitHub:
    ```sh
    git push origin tên-branch
    ```

5. **Tạo Pull Request:**
  - Truy cập repository của bạn trên GitHub.
  - Nhấp vào tab **Pull requests** và sau đó nhấp vào nút **New pull request**.
  - Chọn branch mà bạn vừa đẩy lên và branch mà bạn muốn hợp nhất vào (thường là `main` hoặc `master`).
  - Nhập tiêu đề và mô tả cho Pull Request của bạn.
  - Nhấp vào **Create pull request** để tạo Pull Request.

#### Review Pull Request

1. **Xem xét Pull Request:**
  - Truy cập tab **Pull requests** trong repository của bạn trên GitHub.
  - Chọn Pull Request mà bạn muốn xem xét.
  - Xem xét các thay đổi được đề xuất trong Pull Request.

2. **Thảo luận và phản hồi:**
  - Sử dụng phần bình luận để thảo luận về các thay đổi với tác giả của Pull Request.
  - Đưa ra phản hồi, đề xuất cải tiến hoặc yêu cầu thay đổi nếu cần thiết.

3. **Chấp nhận hoặc từ chối Pull Request:**
  - Nếu Pull Request đáp ứng các yêu cầu và không có vấn đề gì, nhấp vào nút **Merge pull request** để hợp nhất các thay đổi vào branch chính.
  - Nếu Pull Request cần thêm thay đổi, yêu cầu tác giả cập nhật và gửi lại.

4. **Xóa branch sau khi hợp nhất:**
  - Sau khi Pull Request được hợp nhất, bạn có thể xóa branch đã sử dụng để tạo Pull Request để giữ cho repository của bạn gọn gàng.
    ```sh
    git branch -d tên-branch
    git push origin --delete tên-branch
    ```

Quy trình này giúp đảm bảo rằng mọi thay đổi đều được xem xét kỹ lưỡng trước khi được hợp nhất vào branch chính, giúp duy trì chất lượng mã nguồn và sự ổn định của dự án.

### 4.3. Issues và Quản lý công việc

#### Issues trong GitHub là gì?

Issues là một công cụ quản lý công việc và theo dõi lỗi tích hợp sẵn trong GitHub. Nó cho phép các thành viên trong dự án tạo, thảo luận và theo dõi các vấn đề, lỗi, hoặc yêu cầu tính năng mới. Mỗi issue có thể được gắn nhãn, phân công cho các thành viên cụ thể, và liên kết với các Pull Request để theo dõi tiến độ giải quyết.

#### Tạo và quản lý Issues

1. **Tạo Issue mới:**
  - Truy cập repository của bạn trên GitHub.
  - Nhấp vào tab **Issues** và sau đó nhấp vào nút **New issue**.
  - Nhập tiêu đề và mô tả cho issue của bạn.
  - Nhấp vào **Submit new issue** để tạo issue.

2. **Quản lý Issues:**
  - Sử dụng các nhãn (labels) để phân loại issues theo loại (bug, enhancement, question, v.v.).
  - Phân công issues cho các thành viên trong nhóm để theo dõi trách nhiệm.
  - Sử dụng milestones để nhóm các issues liên quan đến một mục tiêu hoặc phiên bản cụ thể.

#### Gắn nhãn và phân công nhiệm vụ

1. **Gắn nhãn cho Issue:**
  - Mở issue mà bạn muốn gắn nhãn.
  - Nhấp vào biểu tượng nhãn (label) và chọn các nhãn phù hợp từ danh sách.

2. **Phân công Issue:**
  - Mở issue mà bạn muốn phân công.
  - Nhấp vào biểu tượng người dùng (assignee) và chọn thành viên mà bạn muốn phân công issue.

Issues giúp tổ chức và quản lý công việc trong dự án một cách hiệu quả, đảm bảo rằng mọi vấn đề và yêu cầu đều được theo dõi và giải quyết kịp thời.

- Tạo và quản lý Issues.
- Gắn nhãn và phân công nhiệm vụ.

## 5. Các tính năng nâng cao
### 5.1. Actions: Tích hợp CI/CD
Continuous Integration (CI) và Continuous Deployment (CD) là hai khái niệm quan trọng trong phát triển phần mềm hiện đại.

- **Continuous Integration (CI):** CI là một thực hành trong phát triển phần mềm, nơi các nhà phát triển thường xuyên tích hợp mã nguồn của họ vào một nhánh chính của repository. Mỗi lần tích hợp được xác minh bằng cách xây dựng tự động và kiểm thử (automated build and test). Mục tiêu của CI là phát hiện lỗi sớm, cải thiện chất lượng phần mềm và giảm thời gian kiểm thử.

- **Continuous Deployment (CD):** CD là một phần mở rộng của CI, nơi các thay đổi mã nguồn được tự động triển khai vào môi trường sản xuất sau khi vượt qua các kiểm thử tự động. Điều này giúp đảm bảo rằng phần mềm luôn ở trạng thái có thể triển khai và các tính năng mới được phát hành nhanh chóng và liên tục.

CI/CD giúp tăng cường sự hợp tác giữa các thành viên trong nhóm, cải thiện chất lượng mã nguồn và giảm thiểu rủi ro khi triển khai phần mềm.

- Thiết lập GitHub Actions.

### Thiết lập GitHub Actions

GitHub Actions là một dịch vụ CI/CD tích hợp sẵn trong GitHub, cho phép bạn tự động hóa các quy trình phát triển phần mềm như xây dựng, kiểm thử và triển khai. Dưới đây là các bước cơ bản để thiết lập GitHub Actions cho dự án của bạn:

1. **Tạo tệp workflow:**
  - Trong repository của bạn, tạo một thư mục `.github/workflows`.
  - Trong thư mục này, tạo một tệp YAML (ví dụ: `ci.yml`) để định nghĩa workflow của bạn.

2. **Định nghĩa workflow:**
  - Mở tệp YAML và thêm cấu hình cho workflow của bạn. Dưới đây là một ví dụ về workflow cơ bản để xây dựng và kiểm thử mã nguồn Node.js:
    ```yaml
    name: CI

    on:
     push:
      branches:
        - main
     pull_request:
      branches:
        - main

    jobs:
     build:
      runs-on: ubuntu-latest

      steps:
        - name: Checkout code
         uses: actions/checkout@v2

        - name: Set up Node.js
         uses: actions/setup-node@v2
         with:
          node-version: '14'

        - name: Install dependencies
         run: npm install

        - name: Run tests
         run: npm test
    ```

3. **Commit và đẩy thay đổi:**
  - Commit tệp workflow và đẩy thay đổi lên repository của bạn:
    ```sh
    git add .github/workflows/ci.yml
    git commit -m "Add GitHub Actions workflow"
    git push origin main
    ```

4. **Kiểm tra kết quả:**
  - Truy cập tab **Actions** trong repository của bạn trên GitHub để xem trạng thái của workflow. Bạn sẽ thấy các workflow chạy tự động khi có các sự kiện như push hoặc pull request.

GitHub Actions cung cấp nhiều tính năng mạnh mẽ và linh hoạt để tự động hóa quy trình phát triển phần mềm của bạn. Bạn có thể tùy chỉnh workflow theo nhu cầu cụ thể của dự án và sử dụng các action có sẵn từ GitHub Marketplace để mở rộng chức năng.


### 5.2. Bảo mật repository

Khi tạo một repository mới trên GitHub, bạn có thể chọn giữa hai tùy chọn: công khai (public) và riêng tư (private).

- **Repository công khai (Public):**
  - Mọi người trên internet đều có thể xem repository của bạn.
  - Thích hợp cho các dự án mã nguồn mở hoặc khi bạn muốn chia sẻ mã nguồn với cộng đồng.
  - Các thành viên trong cộng đồng có thể đóng góp vào dự án của bạn thông qua Pull Request.

- **Repository riêng tư (Private):**
  - Chỉ những người được bạn mời mới có thể xem và truy cập repository.
  - Thích hợp cho các dự án cá nhân, dự án nội bộ của công ty, hoặc khi bạn không muốn công khai mã nguồn.
  - Bạn có thể kiểm soát quyền truy cập và phân công nhiệm vụ cho các thành viên trong nhóm.

Bạn có thể thay đổi tùy chọn này bất kỳ lúc nào trong phần cài đặt của repository.

### Sử dụng GitHub Secrets

GitHub Secrets là một tính năng bảo mật cho phép bạn lưu trữ và quản lý các thông tin nhạy cảm như token, mật khẩu, và khóa API một cách an toàn. Secrets có thể được sử dụng trong các workflow của GitHub Actions để bảo vệ thông tin nhạy cảm khỏi bị lộ.

#### Tạo GitHub Secrets

1. Truy cập repository của bạn trên GitHub.
2. Nhấp vào tab "Settings" ở phía trên của trang repository.
3. Trong menu bên trái, chọn "Secrets and variables" và sau đó chọn "Actions".
4. Nhấp vào nút "New repository secret".
5. Nhập tên và giá trị cho secret của bạn.
  - **Name:** Tên của secret (ví dụ: `API_KEY`).
  - **Value:** Giá trị của secret (ví dụ: `your-api-key-value`).
6. Nhấp vào "Add secret" để lưu secret.

#### Sử dụng GitHub Secrets trong Workflow

Sau khi tạo secret, bạn có thể sử dụng nó trong các workflow của GitHub Actions bằng cách tham chiếu đến tên của secret. Dưới đây là một ví dụ về cách sử dụng secret trong một workflow:

```yaml
name: CI

on:
  push:
   branches:
    - main
  pull_request:
   branches:
    - main

jobs:
  build:
   runs-on: ubuntu-latest

   steps:
    - name: Checkout code
      uses: actions/checkout@v2

    - name: Set up Node.js
      uses: actions/setup-node@v2
      with:
       node-version: '14'

    - name: Install dependencies
      run: npm install

    - name: Run tests
      run: npm test

    - name: Use API key
      run: echo ${{ secrets.API_KEY }}
```

Trong ví dụ trên, `secrets.API_KEY` sẽ được thay thế bằng giá trị của secret `API_KEY` mà bạn đã tạo. Secrets giúp bảo vệ thông tin nhạy cảm và đảm bảo rằng chúng không bị lộ trong quá trình thực thi workflow.


### 5.3. Release


#### Tạo release và quản lý phiên bản

Releases là một tính năng của GitHub cho phép bạn đóng gói và phân phối các phiên bản cụ thể của phần mềm. Mỗi release thường đi kèm với một tag, mô tả, và các tệp nhị phân hoặc tài liệu liên quan. Releases giúp người dùng dễ dàng truy cập và tải xuống các phiên bản ổn định của phần mềm.

##### Tạo release mới

1. Truy cập repository của bạn trên GitHub.
2. Nhấp vào tab **Releases**.
3. Nhấp vào nút **Draft a new release**.
4. Điền thông tin cho release:
  - **Tag version:** Nhập tên tag cho phiên bản (ví dụ: `v1.0.0`).
  - **Release title:** Nhập tiêu đề cho release.
  - **Description:** Nhập mô tả chi tiết về các thay đổi, tính năng mới, hoặc sửa lỗi trong phiên bản này.
5. Đính kèm tệp nhị phân hoặc tài liệu (nếu có):
  - Kéo và thả các tệp vào khu vực đính kèm hoặc nhấp để chọn tệp từ máy tính của bạn.
6. Nhấp vào **Publish release** để tạo release mới.

##### Quản lý phiên bản

- **Tag:** Mỗi release đi kèm với một tag, giúp bạn dễ dàng tham chiếu đến các phiên bản cụ thể trong lịch sử mã nguồn.


![GitHub Release](https://user-images.githubusercontent.com/2387015/38778095-fc3b7fa6-40e5-11e8-9a9c-6d1061fb7ac6.png)

- **Changelog:** Sử dụng changelog để ghi lại các thay đổi, tính năng mới, và sửa lỗi trong mỗi phiên bản. Điều này giúp người dùng và các thành viên trong nhóm dễ dàng theo dõi tiến trình phát triển.
- **Semantic Versioning:** Sử dụng quy ước Semantic Versioning (ví dụ: `v1.0.0`, `v1.1.0`, `v2.0.0`) để đặt tên cho các phiên bản, giúp người dùng hiểu rõ mức độ thay đổi giữa các phiên bản.

Releases giúp tổ chức và phân phối các phiên bản phần mềm một cách hiệu quả, đảm bảo rằng người dùng luôn có thể truy cập các phiên bản ổn định và cập nhật nhất của phần mềm.

- Phân phối tài nguyên qua release.

#### Phân phối tài nguyên qua release

Releases trên GitHub không chỉ giúp bạn quản lý các phiên bản phần mềm mà còn cho phép bạn phân phối tài nguyên liên quan một cách dễ dàng. Bạn có thể đính kèm các tệp nhị phân, tài liệu, hoặc bất kỳ tài nguyên nào khác mà người dùng cần để sử dụng phiên bản phần mềm của bạn.

#### Đính kèm tài nguyên vào release

1. **Tạo release mới hoặc chỉnh sửa release hiện có:**
  - Truy cập repository của bạn trên GitHub.
  - Nhấp vào tab **Releases**.
  - Nhấp vào **Draft a new release** hoặc chọn một release hiện có để chỉnh sửa.

2. **Đính kèm tài nguyên:**
  - Kéo và thả các tệp vào khu vực đính kèm hoặc nhấp để chọn tệp từ máy tính của bạn.
  - Bạn có thể đính kèm nhiều tệp, bao gồm các tệp nhị phân, tài liệu hướng dẫn, hoặc bất kỳ tài nguyên nào khác mà người dùng cần.

3. **Hoàn tất và xuất bản release:**
  - Điền thông tin chi tiết cho release như tag version, tiêu đề, và mô tả.
  - Nhấp vào **Publish release** để xuất bản release mới hoặc lưu các thay đổi.

###### Lợi ích của việc phân phối tài nguyên qua release

- **Dễ dàng truy cập:** Người dùng có thể dễ dàng tìm và tải xuống các tệp cần thiết từ trang release của repository.
- **Quản lý phiên bản:** Mỗi release đi kèm với một tag, giúp người dùng biết chính xác phiên bản nào họ đang tải xuống và sử dụng.
- **Tổ chức tốt hơn:** Tất cả các tài nguyên liên quan đến một phiên bản cụ thể được tổ chức và lưu trữ cùng nhau, giúp dễ dàng quản lý và phân phối.

Phân phối tài nguyên qua release giúp đảm bảo rằng người dùng luôn có thể truy cập các tệp cần thiết để sử dụng phần mềm của bạn một cách hiệu quả và thuận tiện.


## 6. Công cụ GitHub CLI


GitHub CLI (Command Line Interface) là một công cụ mạnh mẽ cho phép bạn tương tác với GitHub trực tiếp từ dòng lệnh. Với GitHub CLI, bạn có thể thực hiện nhiều tác vụ khác nhau mà không cần phải truy cập giao diện web của GitHub, giúp tăng cường hiệu quả và tốc độ làm việc của bạn.

#### Các tính năng cơ bản của GitHub CLI

1. **Quản lý repository:**
  - Tạo, sao chép (clone), và xóa repository.
  - Xem thông tin chi tiết về repository.

2. **Quản lý Issues và Pull Requests:**
  - Tạo, xem, và bình luận trên Issues và Pull Requests.
  - Gắn nhãn, phân công, và đóng Issues và Pull Requests.

3. **Quản lý nhánh (branch):**
  - Tạo, liệt kê, và xóa nhánh.
  - Chuyển đổi giữa các nhánh.

4. **Tích hợp với Git:**
  - Thực hiện các lệnh Git cơ bản như `commit`, `push`, `pull`, và `merge`.
  - Xem lịch sử commit và trạng thái của repository.

5. **Tự động hóa quy trình làm việc:**
  - Tạo và quản lý workflow của GitHub Actions.
  - Kiểm tra trạng thái và nhật ký của các workflow.

#### Cài đặt GitHub CLI

1. **Trên macOS:**
  ```sh
  brew install gh
  ```

2. **Trên Windows:**
  - Tải và cài đặt từ [GitHub CLI releases](https://github.com/cli/cli/releases).

3. **Trên Linux:**
  - Sử dụng trình quản lý gói của hệ điều hành hoặc tải từ [GitHub CLI releases](https://github.com/cli/cli/releases).

#### Sử dụng GitHub CLI

1. **Đăng nhập vào GitHub:**
  ```sh
  gh auth login
  ```

2. **Tạo repository mới:**
  ```sh
  gh repo create tên-repository
  ```

3. **Tạo Issue mới:**
  ```sh
  gh issue create --title "Tiêu đề của Issue" --body "Mô tả chi tiết của Issue"
  ```

4. **Tạo Pull Request mới:**
  ```sh
  gh pr create --title "Tiêu đề của Pull Request" --body "Mô tả chi tiết của Pull Request"
  ```

5. **Xem danh sách Issues:**
  ```sh
  gh issue list
  ```

GitHub CLI giúp bạn quản lý và tương tác với các dự án trên GitHub một cách nhanh chóng và hiệu quả, đặc biệt hữu ích cho các nhà phát triển yêu thích làm việc với dòng lệnh.

## 7. Tổng kết

GitHub đóng vai trò quan trọng trong việc quản lý mã nguồn và phát triển phần mềm nhờ các tính năng sau:

- **Lưu trữ mã nguồn:** GitHub cung cấp một nền tảng lưu trữ mã nguồn an toàn và đáng tin cậy, giúp các lập trình viên dễ dàng truy cập và quản lý mã nguồn của họ.
- **Quản lý phiên bản:** Với GitHub, bạn có thể theo dõi lịch sử thay đổi của mã nguồn, giúp dễ dàng quay lại các phiên bản trước đó khi cần thiết.
- **Cộng tác nhóm:** GitHub cho phép nhiều lập trình viên làm việc cùng nhau trên cùng một dự án, hỗ trợ các tính năng như pull request và issue tracking để quản lý công việc và giao tiếp hiệu quả.
- **Tích hợp CI/CD:** GitHub Actions giúp tự động hóa quy trình xây dựng, kiểm thử và triển khai phần mềm, đảm bảo chất lượng và giảm thiểu rủi ro khi phát hành.
- **Bảo mật:** GitHub cung cấp các công cụ bảo mật như GitHub Secrets để quản lý thông tin nhạy cảm và bảo vệ mã nguồn khỏi các mối đe dọa.


Để nâng cao kỹ năng sử dụng GitHub, bạn có thể thực hiện các bước sau:

1. **Học các lệnh Git cơ bản:** Nắm vững các lệnh Git như `clone`, `commit`, `push`, `pull`, và `merge` để quản lý mã nguồn hiệu quả.
2. **Sử dụng GitHub Actions:** Tìm hiểu cách thiết lập và sử dụng GitHub Actions để tự động hóa quy trình CI/CD.
3. **Tham gia các dự án mã nguồn mở:** Đóng góp vào các dự án mã nguồn mở trên GitHub để rèn luyện kỹ năng và học hỏi từ cộng đồng.
4. **Quản lý Issues và Pull Requests:** Sử dụng các tính năng quản lý công việc của GitHub để theo dõi và giải quyết các vấn đề trong dự án.
5. **Tìm hiểu về bảo mật:** Sử dụng GitHub Secrets và các công cụ bảo mật khác để bảo vệ mã nguồn và thông tin nhạy cảm.
6. **Sử dụng GitHub CLI:** Tìm hiểu cách sử dụng GitHub CLI để tương tác với GitHub từ dòng lệnh, giúp tăng cường hiệu quả làm việc.

Bằng cách thực hiện các bước trên, bạn sẽ nâng cao kỹ năng sử dụng GitHub và trở thành một lập trình viên chuyên nghiệp hơn.
