# KHBD_latex

Đây là mẫu kế hoạch bài dạy bằng $\LaTeX$, dựa trên mẫu kế hoạch bìa dạy đính kèm Công văn số 5512/BGDĐT-GDTrH ngày 18 tháng 12 năm 2020 của Bộ GDĐT.

## Hướng dẫn sử dụng chung

### Thông tin chung

- Thầy cô chỉnh sửa các thông tin chung ở trước ```\begin{document}```:

    ```latex
    \def\truong{<Tên trường>}
    \def\tobomon{<Tên tổ bộ môn>}
    \def\giaovien{<Tên giáo viên>}
    \def\monhoc{<Tên môn học>}
    \def\lophoc{<Tên lớp>}
    ```

### Các lệnh gõ tiêu đề

- Thầy cô lưu ý Template sẽ tự động in hoa, thầy cô không cần gõ thủ công. 

- Khi thầy cô muốn xuống dòng ở giữa tiêu đề cho đẹp thì thầy cô dùng lệnh `\xuongdong` để chèn vào giữa.

- Thầy cô dùng lệnh sau để gõ tiêu đề chương:

    ```latex
    \setcounter{chapter}{<số chương - 1>}
    \section{<Tên chương>}
    ``` 

- Thầy cô dùng lệnh sau để tạo khung tên bài dạy:

    ```latex
    \section{<Tên bài>}
    ```

- Thầy cô dùng ```\subsection``` cho tiêu đề lớn đánh số La Mã in hoa:
    - I. MỤC TIÊU
    - II. THIẾT BỊ DẠY HỌC VÀ HỌC LIỆU
    - III. TIẾN TRÌNH DẠY HỌC
    - IV. PHỤ LỤC
    - ...

- Thầy cô dùng ```\subsubsection``` cho tiêu đề của tiết học (Tiết 1, Tiết 2,...)

- Thầy cô dùng ```\paragraph``` cho tiêu đề nhỏ đánh số Ả rập (1, 2, 3,...):
    - Về kiến thức
    - Về năng lực
    - Về phẩm chất
    - Hoạt động khởi động
    - Hoạt động hình thành kiến thức
    - Hoạt động luyện tập
    - Hoạt động vận dụng
    - ...

- Thầy cô dùng ```\subparagraph``` cho tiêu đề nhỏ đánh số bằng chữ cái (a, b, c,...):
    - Mục tiêu
    - Nội dung
    - Sản phẩm
    - Tổ chức thực hiện
    - ...

## Chi tiết

### Phần Mục tiêu và Thiết bị dạy học và học liệu

- Mẫu soạn như sau:

    ```latex
    \subsection{Mục tiêu}

    \paragraph{Về kiến thức}

    \begin{itemize}
        \item ...
        \item ...
    \end{itemize}

    \paragraph{Về năng lực}

    \begin{itemize}
        \item ...
        \item ...
    \end{itemize}

    \paragraph{Về phẩm chất}

    \begin{itemize}
        \item ...
        \item ...
    \end{itemize}

    \subsection{Thiết bị dạy học và học liệu}

    \paragraph{Giáo viên}

    \begin{itemize}
        \item ...
    \end{itemize}

    \paragraph{Học sinh}

    \begin{itemize}
        \item ...
    \end{itemize}
    ```

### Phần Tiến trình dạy học

- Ở đây thầy cô ghi rõ là chia thành mấy tiết.

    ```latex
    \subsection{Tiến trình dạy học}

    \danhsachtiet

    \subsubsection{<Tên tiết dạy 1>}

    \subsubsection{<Tên tiết dạy 2>}
    ```

    Nội dung sẽ hiện như sau:

    ```
    III. Tiến trình dạy học

    Bài học này dạy trong 02 tiết:
    - Tiết 1: <Tên tiết dạy 1>.
    - Tiết 2: <Tên tiết dạy 2>.
    ```

- Thầy cô vui lòng soạn các tiết dạy ở phía sau hoặc biên dịch lần thứ 2 để cập nhật danh sách tiết. 

### Phần Tiết dạy

1. Hiện tại một tiết dạy học đầy đủ chia làm 4 hoạt động:
    - Hoạt động khởi động
    - Hoạt động hình thành kiến thức
    - Hoạt động luyện tập
    - Hoạt động vận dụng

    Trong đó, mỗi hoạt động bao gồm 4 phần:
    - Mục tiêu
    - Nội dung
    - Sản phẩm
    - Tổ chức thực hiện

2. Đối với phần **Mục tiêu**, thầy cô dùng lệnh `\muctieu` môi trường ```itemize``` để soạn.

    ```latex
    \muctieu

    \begin{itemize}
    \item ...
    \end{itemize}
    ```

3. Đối với hai phẩn **Nội dung** và **Sản phẩm**, ta soạn song song hai cột. 

    Ta soạn theo cấu trúc như sau, môi trường tự động đánh số:

    ```latex
    \noidungsanpham % Bắt đầu chia 2 cột

    \begin{<tên môi trường 1>}
        Nội dung...
        %%%
        \doicot
        %%% 
        Sản phảm dự kiến...
    \end{<tên môi trường 1>}

    \kengang % Dùng khi cần dòng kẻ ngang giữa hai môi trường

    \begin{<tên môi trường 2>}
        Nội dung...
        %%%
        \doicot
        %%% 
        Sản phảm dự kiến...
    \end{<tên môi trường 2>}
    ```

    Nếu muốn thay đổi tỉ lệ 2 cột (mặc định mỗi bên 0.5), thầy cô dùng lệnh:
    ```latex
    \noidungsanpham[0.4] % Cột 1 lấy 0.4, cột 2 lấy 0.6
    ```

    Một số môi trường đã được khai báo sẵn theo mẫu SGK **Kết nối tri thức với cuộc sống** đã được thống nhất sử dụng toàn quốc từ năm học 2027-2028:
    - ```modau```: Tình huống mở đầu
    - ```ontap```: Ôn tập
    - ```ttkp```: Tìm tòi - Khá phá *(không đánh số)*
    - ```dhnh```: Đọc hiểu - Nghe hiểu *(không đánh số)*
    - ```cauhoi```: Câu hỏi *(không đánh số)*
    - ```vidu```: Ví dụ
    - ```luyentap```: Luyện tập
    - ```thuchanh```: Thực hành
    - ```vandung```: Vận dung
    - ```tranhluan```: Tranh luận *(không đánh số)*
    - ```thuthachnho```: Thử thách nhỏ *(không đánh số)*
    - ```phieuhoctap```: Phiếu học tập
    - ```baitap```: Bài tập

    Một số khung chữ đã được tạo sẵn bằng gói `set_box`:
    - ```kttt```: Kiến thức trọng tâm
    - ```chuy```: Chú ý *(không đánh số)*
    - ```nhanxet```: Nhận xét *(không đánh số)*

    Một số môi trường từ gói `ex_test` dùng cho phiếu học tập:
    - ```ex```: Câu hỏi trắc nghiệm
    - ```bt```: Bài tập tự luận

4. Đối với phần **Tổ chức thực hiện**, thầy cô soạn theo câu trúc sau, phần này **KHÔNG tự đánh số**:

    ```latex
    \tochucthuchien

    \begin{tcth}[<tên môi trường>={<đánh số/nội dung>}]
        \buocmot
        \item ... 
        \buochai
        \item ... 
        \buocba
        \item ... 
        \buocbon
        \item ... 
    \end{tcth}
    ```

    Chẳng hạn, thầy cô muốn làm phần tổ chức thực hiện cho Hoạt động luyện tập, trong đó có Luyện tập 1 và Bài tập 1.1 đến 1.3:

    ```latex
    \tochucthuchien

    \begin{tcth}[luyentap={1}]
        \buocmot
        \item ... 
        \buochai
        \item ... 
        \buocba
        \item ... 
        \buocbon
        \item ... 
    \end{tcth}

    \begin{tcth}[baitap={từ 1.1 đến 1.3}]
        \buocmot
        \item ... 
        \buochai
        \item ... 
        \buocba
        \item ... 
        \buocbon
        \item ... 
    \end{tcth}
    ```

### Phần Phụ lục

- Thầy cô soạn theo cấu trúc giống gói `ex_test`:
    
    ```latex
    \subsection{Phụ lục}
    
    \paragraph{Phiếu học tập 1}

    \begin{ex}
        Câu 1
        \choice
        {}
        {}
        {}
        {}
    \end{ex}

    \begin{ex}
        Câu 2
        \choice
        {}
        {}
        {}
        {}
    \end{ex}

    \paragraph{Phiếu học tập 1}

    \begin{bt}
        Bài 1
    \end{bt}

    \begin{bt}
        Bài 2
    \end{bt}
    ```


