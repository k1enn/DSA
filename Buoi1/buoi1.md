Trường ĐH HUFLIT – Bộ môn HTTT, Khoa CNTT 	Bài tập thực hành Cấu trúc dữ liệu & giải thuật

**LAB 01**
**Chủ đề: Cơ bản về phương pháp lập trình hướng đối tượng**
Cho thông tin của sinh viên gồm:

- *Mã số sinh viên (maSo): Chuỗi ký tự*
- *Họ tên sinh viên (hoTen): Chuỗi ký tự*
- *Chuyên ngành (chuyenNganh): Chuỗi ký tự*
- *Năm sinh (namSinh): Số nguyên*
- *Điểm trung bình tích lũy (diemTB): Số thực*
- *Xếp loại (loai): Chuỗi ký tự*

Hãy thiết kế lớp sinh viên (SinhVien) gồm các thông tin trên.

## Yêu cầu:
### Yêu cầu 1: Lớp sinh viên (SinhVien) gồm có các chức năng:
1.	Nhập, xuất thông tin sinh viên
2.	Xếp loại sinh viên dựa vào điểm trung bình tích lũy theo tiêu chí (diemTB < 5: Kém; 5 <= diemTB < 7: Trung bình; 7 <= diemTB < 8: Khá; còn lại là Giỏi) 
Lưu ý các ràng buộc: 
-	Tuổi của sinh viên từ 17 đến 70
-	Điểm trung bình từ 0 đến 10	Tạo một Project ngôn ngữ C# mới với tên là HoVaTenSV_Lab01 (trong đó: HoVaTenSV là họ và tên của sinh viên, không khoảng trắng và không dấu tiếng Việt) 
Bước 1. Tạo class mới đặt tên file là SinhVien
Bước 2. Khai báo các thuộc tính
```cs
namespace HoVaTenSV_Lab01
{
    class SinhVien
    {
        private string maSo;
        private string hoTen;
        private string chuyenNganh;
        private int namSinh;
        private float diemTB;
        private string loai;

	 //Các phương thức ...
    }
}
```
Bước 3. Bổ sung vào class SinhVien
1.	Các properties get/set
2.	Các constructors
-	Default: public SinhVien() { }
-	Parameter: 
public SinhVien(string ms, string ht, string cn, int ns, float dtb) { }
(Thông tin xếp loại được thực hiện bên trong constructor này bằng cách gọi phương thức XepLoai(), không cần truyền vào tham số loại của sinh viên)
-	Copy: public SinhVien(SinhVien sv) { }
3.	Các phương thức theo yêu cầu
-	Kiểm tra ràng buộc tuổi: public bool KiemTraNamSinh(int ns) { }
-	Kiểm tra ràng buộc điểm: public bool KiemTraDiemTB(float dtb) { }
-	Nhập: public void Nhap() { }
-	Xuất: public void Xuat() { }
-	Xếp loại: public void XepLoai() { }
### Yêu cầu 2: Chương trình thực hiện theo yêu cầu sau:
1.	Tạo 1 đối tượng rỗng svA
2.	Nhập thông tin cho svA
3.	Xuất thông tin svA
4.	Tạo 1 đối tượng svB gồm các thông tin: mã số sinh viên: “18DH001”; họ và tên: “Lam Thanh Ngoc”; chuyên ngành: “CNPM”; năm sinh: 2000; và điểm trung bình tích lũy: 7.6
5.	Xuất thông tin svB
6.	Tạo 1 đối tượng svC được sao chép thông tin từ svB
7.	Nhập họ tên, điểm trung bình tích lũy và cập nhật thông tin cho svC
8.	Xuất thông tin svC
9.	Xuất thông tin svB
10.	Kiểm tra xem thông tin của svB có thay đổi không (nếu svB bị thay đổi như thông tin svC thì Copy Contructor viết sai và phải chỉnh sửa lại)
### Yêu cầu 3: 
Tạo lớp mảng chứa n (0<n≤1000000) sinh viên (MangSinhVien) gồm có các chức năng: Nhập và xuất danh sách sinh viên.

