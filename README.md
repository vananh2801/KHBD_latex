# KHBD_latex

Đây là mẫu kế hoạch bài dạy bằng $\LaTeX$, dựa trên mẫu kế hoạch bìa dạy đính kèm Công văn số 5512/BGDĐT-GDTrH ngày 18 tháng 12 năm 2020 của Bộ GDĐT.

## Hướng dẫn sử dụng

### Tên bài

- Thầy cô chỉnh sửa các thông tin chung ở trước ```\begin{document}```:

    ```latex
    \def\truong{<Tên trường>}
    \def\tobomon{<Tên tổ bộ môn>}
    \def\giaovien{<Tên giáo viên>}
    \def\monhoc{<Tên môn học>}
    \def\lophoc{<Tên lớp>}
    ```

- Ở các file dữ liệu riêng thì thầy cô cần khai báo số tiết trước khi khai báo tên bài:

    ```latex
    \def\thoigian{2}
    \section
    [<Tên bài trên mục lục>]
    {<TÊN BÀI>} % Template sẽ KHÔNG tự động in hoa
    ```

- Dối với các bài dạy không đánh số, chẳng hạn Luyện tập chung, Ôn tập cuối chương,... thầy cô dùng 

    ```latex
    \def\thoigian{2}
    \section*{<Tên bài>} % Template sẽ tự động in hoa
    ```

### Phần Mục tiêu và Thiết bị dạy học và học liệu

- Thầy cô lưu ý dùng ```\subsection``` cho đề mục lớn và ```\paragraph``` cho tiêu đề nhỏ. 
- Trong template này, lệnh ```\subsubsection``` chỉ dùng để chia Tiết 1, 2, 3,... Đối với thầy cô cần soạn riêng kế hoạch bài dạy cho từng tiết thì bỏ qua lệnh ```\subsubsection```.


    ```latex
    \subsection{Mục tiêu}

    \paragraph{Về kiến thức, kĩ năng}

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

    Bài học này dạy trong 02 tiết:

    \begin{itemize}
        \item Tiết 1: ...
        \item Tiết 2: ...
    \end{itemize}
    ```

### Giới thiệu về cách soạn

1. Cấu trúc một tiết dạy học

- Hiện tại một tiết dạy học đầy đủ chia làm 4 hoạt động (thầy cô dùng ```\paragraph```):
    - Hoạt động khởi động
    - Hoạt động hình thành kiến thức
    - Hoạt động luyện tập
    - Hoạt động vận dụng

    Trong đó, mỗi hoạt động bao gồm 4 phần
    - Mục tiêu
    - Nội dung
    - Sản phẩm
    - Tổ chức thực hiện

- Thầy cô dùng ```\subsubsection``` để khai báo tên tiết và dùng ```\paragraph``` để khai báo tên hoạt động.

    ```latex
    \subsubsection{<Tên tiết>}

    \paragraph{<Tên hoạt động>}
    ```

2. Đối với phần **Mục tiêu**, thầy cô dùng môi trường ```itemize``` để soạn.

    ```latex
    \muctieu

    \begin{itemize}
    \item ...
    \end{itemize}
    ```

3. Đối với hai phẩn **Nội dung** và **Sản phẩm**, ta soạn song song hai cột. 

    Ta soạn theo cấu trúc như sau, các đánh số sẽ tự động:

    ```latex
    \noidungsanpham

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

    Một số môi trường đã được khai báo sẵn theo mẫu SGK Kết nối tri thức đã được thống nhất sử dụng toàn quốc từ năm học 2027-2028:
    - ```modau```: Tình huống mở đầu
    - ```ontap```: Ôn tập
    - ```ttkp```: Tìm tòi - Khá phá
    - ```dhnh```: Đọc hiểu - Nghe hiểu
    - ```cauhoi```: Câu hỏi
    - ```vidu```: Ví dụ
    - ```luyentap```: Luyện tập
    - ```thuchanh```: Thực hành
    - ```vandung```: Vận dung
    - ```tranhluan```: Tranh luận
    - ```thuthachnho```: Thử thách nhỏ
    - ```phieuhoctap```: Phiếu học tập
    - ```baitap```: Bài tập

4. Đối với phần **Tổ chức thực hiện**, thầy cô soạn theo câu trúc sau, thầy cô phải tự chủ phần đánh số

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

5. Phần **Phụ lục**, thầy cô dùng như sau:
    
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


