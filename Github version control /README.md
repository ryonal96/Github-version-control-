1. Git và Hệ thống Kiểm soát Phiên bản (VCS)
    Git: Git là một hệ thống kiểm soát phiên bản phân tán (Distributed Version Control System). Điều này có nghĩa là mỗi nhà phát triển sẽ có một bản sao đầy đủ của toàn bộ lịch sử mã nguồn trên máy tính của mình.
    VCS: Hệ thống kiểm soát phiên bản giúp theo dõi các thay đổi trong mã nguồn, cho phép nhiều người cùng làm việc trên cùng một dự án một cách hiệu quả mà không lo lắng về việc ghi đè lẫn nhau.
2. Các Khái niệm Cơ Bản trong GitHub
    Repository (Repo): Là nơi lưu trữ mã nguồn của dự án. Mỗi repo có thể chứa nhiều tệp và thư mục khác nhau.
    Commit: Một commit ghi lại sự thay đổi trong mã nguồn. Mỗi commit có một thông điệp đi kèm để mô tả thay đổi đó.
    Branch: Nhánh giúp bạn phân tách công việc ra từ nhánh chính (thường gọi là main hoặc master). Bạn có thể làm việc trên các tính năng mới hoặc sửa lỗi mà không ảnh hưởng đến nhánh chính.
    Merge: Kết hợp các thay đổi từ nhánh này vào nhánh khác. Quá trình merge có thể xảy ra xung đột, cần giải quyết thủ công.
    Pull Request (PR): Là một yêu cầu để merge các thay đổi từ nhánh của bạn vào nhánh chính. PR giúp nhóm làm việc có thể xem xét và thảo luận về thay đổi trước khi hợp nhất.

3. Các Lệnh Git Cơ Bản
    git init: Khởi tạo một repo mới.
        git init

    git clone [URL]: Sao chép một repo từ GitHub về máy tính cá nhân.
        git clone [URL]

    git add [file]: Thêm tệp vào khu vực tạm để chuẩn bị commit.
        git add [file] hoặc git add . để thêm cả thư mục.

    git commit -m "message": Tạo một commit với thông điệp mô tả thay đổi.
        git commit -a -m "message" để đẩy nhanh các thay đổi lên github ( chỉ đối với các file đã có sẵn, nếu tạo file mới phải dũng git add để update)

    git push: Đẩy các commit từ máy tính cá nhân lên GitHub.
        git push [remote] [branch]
        Khi bạn sử dụng tùy chọn -u, Git sẽ nhớ rằng nhánh main trên máy tính được theo dõi bởi nhánh main trên origin

    git pull: Kéo các thay đổi từ repo trên GitHub về máy tính cá nhân.
        git pull [remote]

    git branch: Liệt kê các nhánh hiện có hoặc tạo nhánh mới.
        git branch hoặc git branch [branch-name]

    git fetch: Tải về các thay đổi từ remote nhưng không merge vào nhánh hiện tại.
        git fetch [remote]

    git rebase: Tái tổ chức lịch sử commit của nhánh
        git rebase [branch-name]

    git cherry-pick: Áp dụng một commit cụ thể từ nhánh khác vào nhánh hiện tại. 
        git cherry-pick [commit]

    git checkout [branch]: Chuyển đổi giữa các nhánh.
        git checkout [branch-name] hoặc git checkout -b [new-branch] để tạo mới và chuyển sang nhánh mới

    git merge [branch]: Hợp nhất nhánh chỉ định vào nhánh hiện tại.

    Để custom việc upfile lên hệ thống thì sẽ thêm tệp vào .gitignore thì lúc sử dụng git status, git add và git commit sẽ tự động bỏ qua ( nếu đã upfile từ những lần trước thì cần phải gỡ các tệp đấy bằng cách xóa khỏi git tracking. Ví dụ : git rm --cached [file]
)


4. Quy trình Làm việc Thông thường trên GitHub
    Fork Repository: Tạo một bản sao của repo gốc về tài khoản GitHub cá nhân.
    Clone Repository: Sao chép repo từ GitHub về máy tính cá nhân.
    Create a Branch: Tạo một nhánh mới để phát triển tính năng hoặc sửa lỗi.
    Make Changes and Commit: Thực hiện thay đổi và tạo commit.
    Push Changes: Đẩy các commit lên nhánh tương ứng trên GitHub.
    Create Pull Request: Tạo một PR để yêu cầu merge các thay đổi từ nhánh của bạn vào nhánh chính của repo gốc.
    Code Review and Merge: Thảo luận, xem xét và cuối cùng là merge các thay đổi sau khi các thành viên khác chấp nhận.
