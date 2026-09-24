# BÁO CÁO LAB A3

## THIẾT KẾ GIAO DIỆN VỚI XML LAYOUT & TÀI NGUYÊN

### 1. THÔNG TIN SINH VIÊN

* Họ và tên: **Huỳnh Ngọc Hiếu**
* MSSV: **241A010537**
* Lớp: **K26**
* Môn học: **Lập trình trên các thiết bị di động – INT4211**
* Bài thực hành: **Lab A3**
* Ngôn ngữ: **Java + XML**

---

## 2. ĐỦ THÀNH PHẦN THEO ĐẶC TẢ – 2.0 ĐIỂM

Giao diện đăng nhập gồm các thành phần:

* Ảnh bìa và avatar.
* Tiêu đề và phụ đề.
* Ô nhập MSSV và mật khẩu.
* Checkbox **Ghi nhớ**.
* **Quên mật khẩu**.
* Nút **Đăng nhập**.
* Nút **Tài khoản trường**.
* **Đăng ký**.
* Thẻ hồ sơ cá nhân.
* ScrollView.
* Họ tên và MSSV của sinh viên.

Checkpoint 1:
<img width="1917" height="1037" alt="Ảnh chụp màn hình 2026-09-24 225344" src="https://github.com/user-attachments/assets/bea1c71e-4e20-4a56-aeca-edeb970a09e0" />

**Hình 1. Giao diện chính của Lab A3**

<img width="1900" height="1076" alt="Ảnh chụp màn hình 2026-09-24 225540" src="https://github.com/user-attachments/assets/860a0415-f215-42d0-ade7-a660b9ac7ae8" />


**Hình 2. Snackbar sau khi nhấn Đăng nhập**

<img width="425" height="926" alt="Ảnh chụp màn hình 2026-09-24 231758" src="https://github.com/user-attachments/assets/01b7994c-e2bf-46a6-985b-04b858ec86b8" />

Checkpoint 1 yêu cầu giao diện đúng đặc tả, nút Đăng nhập hiển thị Snackbar và Logcat ghi nhận `res/layout`.

---

## 3. FRAMELAYOUT, WEIGHT, SPACE VÀ DRAWABLE – 2.0 ĐIỂM

* Sử dụng **FrameLayout** để tạo hiệu ứng avatar chồng lên ảnh bìa.
* Sử dụng **layout_weight** để chia đều các ô thống kê.
* Sử dụng **Space + weight** để bố trí khoảng trống.
* Sử dụng Drawable Shape cho header, avatar và các thành phần giao diện.


**Hình 3. FrameLayout và bố cục các thành phần**

<img width="1907" height="1078" alt="Ảnh chụp màn hình 2026-09-24 232030" src="https://github.com/user-attachments/assets/a3b31d1b-badc-4a46-a373-956202c4cb84" />

Các yêu cầu này nằm trong phần dựng giao diện bằng LinearLayout và FrameLayout của Lab A3.

---

## 4. TÁCH RESOURCE, DP/SP – 1.5 ĐIỂM

Các tài nguyên được tách riêng:

* `strings.xml`: nội dung chữ.
* `colors.xml`: màu sắc.
* `dimens.xml`: kích thước.
* `drawable/*.xml`: hình nền và shape.

Sử dụng:

* **dp** cho kích thước và khoảng cách.
* **sp** cho kích thước chữ.
* Không sử dụng px cho giao diện.

---

## 5. CONSTRAINTLAYOUT – 1.5 ĐIỂM

Tạo màn hình `ConstraintDemoActivity` bằng ConstraintLayout.

Các nội dung sử dụng:

* Constraint.
* `0dp` – Match Constraint.
* Chain.
* Guideline.

Mỗi View được thiết lập ràng buộc ngang và dọc để bố cục hoạt động đúng.


**Hình 4. Giao diện ConstraintLayout**

<img width="1886" height="1043" alt="Ảnh chụp màn hình 2026-09-24 233845" src="https://github.com/user-attachments/assets/51263cac-cffb-4a36-b130-be4f62a4ed06" />

Checkpoint này kiểm tra màn hình ConstraintLayout hoạt động đúng và các View có đầy đủ constraint.

### So sánh LinearLayout và ConstraintLayout

| Tiêu chí             | LinearLayout                        | ConstraintLayout          |
| -------------------- | ----------------------------------- | ------------------------- |
| Số tầng lồng nhau    | Nhiều hơn                           | Ít hơn                    |
| Số dòng XML          | Nhiều hơn                           | Có thể ít hơn             |
| Dễ đọc/dễ sửa        | Dễ với bố cục đơn giản              | Phù hợp bố cục phức tạp   |
| Khi màn hình rộng ra | Phụ thuộc hướng LinearLayout/weight | Linh hoạt theo constraint |

---

## 6. LAYOUT-LAND – 1.0 ĐIỂM

Tạo:

`res/layout-land/activity_main.xml`

Layout ngang sử dụng các **ID giống với layout dọc**, vì vậy Java không cần thay đổi.

Sau đó xoay máy ảo để kiểm tra giao diện Landscape.

<img width="702" height="675" alt="Ảnh chụp màn hình 2026-09-24 231344" src="https://github.com/user-attachments/assets/b6fbcd6c-65f9-4e14-a216-7146c5a16170" />

**Hình 5. Giao diện ứng dụng ở chế độ Landscape**

<img width="492" height="610" alt="Ảnh chụp màn hình 2026-09-24 231242" src="https://github.com/user-attachments/assets/a97117ca-f64f-4d08-ac73-c67ff1342e88" />


**Hình 6. Logcat xác nhận sử dụng `res/layout-land`**

<img width="1533" height="220" alt="Ảnh chụp màn hình 2026-09-24 231302" src="https://github.com/user-attachments/assets/08171f3d-c7f8-46bf-b0b4-294389b109e4" />
Tài liệu yêu cầu Android tự chọn `layout-land` khi thiết bị ở chế độ ngang và Logcat phải hiển thị `res/layout-land`.

---

## 7. BÀI NÂNG CAO – 2.0 ĐIỂM

### Bài nâng cao 2: NC1 – Chế độ Dark Mode
Chế độ Dark Mode dùng để thay đổi giao diện sang nền tối khi người dùng bật chế độ tối của hệ thống.

Tạo tài nguyên values-night/colors.xml để thiết lập màu sắc phù hợp với Dark Mode.

Khi chuyển giữa chế độ sáng và tối, giao diện tự động thay đổi màu sắc mà không cần thay đổi mã Java.
**Hình 7. Kết quả bài nâng cao 1**

<img width="1917" height="1037" alt="Ảnh chụp màn hình 2026-09-25 005729" src="https://github.com/user-attachments/assets/0230860d-6e86-42de-bd74-e8ac8a694c48" />

### Bài nâng cao 2: Giao diện Tablet 2 cột
Tạo giao diện riêng cho thiết bị có kích thước màn hình lớn bằng thư mục res/layout-sw600dp.

Khi chạy trên thiết bị có chiều rộng tối thiểu 600dp, giao diện được chia thành 2 cột để tận dụng không gian màn hình.

**Hình 8. Kết quả bài nâng cao 2**

<img width="1917" height="1078" alt="Ảnh chụp màn hình 2026-09-25 012311" src="https://github.com/user-attachments/assets/3bc1166b-8b99-4d84-b0a3-8297c42b9732" />

> Ghi đúng 2 bài NC đã thực hiện. Lab A3 cho phép chọn 2 trong 4 bài NC1, NC2, NC3, NC4.

---

## 8. GITHUB VÀ KẾT LUẬN

### GitHub

* Tên repository: **A3_241A010537**
* Số commit: **ít nhất 3 commit**
* Link GitHub: ....................................................

### Kết luận

Qua Lab A3, em đã thực hành xây dựng giao diện Android bằng XML Layout, sử dụng LinearLayout, FrameLayout và ConstraintLayout. Đồng thời biết cách tách tài nguyên, sử dụng layout-land và kiểm tra giao diện trên thiết bị.


---

