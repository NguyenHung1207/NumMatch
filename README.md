# NumMatch Game

## Mô tả Game

NumMatch là một trò chơi puzzle số học thú vị, nơi người chơi cần tìm và ghép các cặp số có tổng bằng 10 hoặc các số giống nhau để loại bỏ chúng khỏi lưới số.

## Gameplay

### Cách chơi
- **Mục tiêu**: Loại bỏ tất cả các số trên lưới 3x9 (27 ô)
- **Luật ghép**: 
  - Ghép 2 số có tổng = 10 (ví dụ: 1+9, 2+8, 3+7, 4+6, 5+5)
  - Ghép 2 số giống nhau (ví dụ: 1+1, 2+2, 3+3...)
- **Điều kiện ghép**: Hai số phải không bị chặn bởi số khác (có thể kết nối bằng đường thẳng)

### Cơ chế Game
- **Hiển thị**: Lưới 3x9 chứa các số từ 1 đến 9
- **Tương tác**: Click/tap để chọn và bỏ chọn số
- **Xử lý sau match**: Số bị loại bỏ, các số phía trên sẽ rơi xuống
- **Thêm số**: Khi hết nước đi, sao chép toàn bộ số chưa bị loại bỏ

## Chế độ chơi

### Mode Endless
- Chơi không giới hạn cho đến khi không còn nước đi
- **Điều kiện thua**: Hết move và không thể ghép được nữa
- **Cơ chế stage**: Tăng level khi loại bỏ hết tất cả số

### Mode Move
- Chế độ thử thách với số nước đi tối ưu
- **Thuật toán**: Tính toán 10 lời giải tối ưu cho mỗi layout
- **Mục tiêu**: Hoàn thành với số move ít nhất

## Cơ chế tạo màn chơi

### Quy tắc tạo số
- **Đủ số**: Mỗi stage luôn có đủ số từ 1 đến 9
- **Phân phối đều**: Các số được phân phối đều trong lưới
- **Số cặp cố định**:
  - Stage 1: 3 cặp
  - Stage 2: 2 cặp  
  - Stage 3+: 1 cặp

### Ví dụ phân phối
```
[5, 4, 5, 5, 4, 5, 5, 4, 5] - 9 số 5 và 4
```

## Âm thanh

Game bao gồm 4 loại hiệu ứng âm thanh:
- `sfx_choose_number`: Khi chọn số
- `sfx_row_clear`: Khi xóa hàng
- `sfx_pair_clear`: Khi ghép cặp thành công
- `sfx_pop_2`: Hiệu ứng pop

## Giao diện

### UI chính
- **Lưới số**: Hiển thị 3x9 số trong ma trận
- **Buttons**: Home, Settings, Add số
- **Responsive**: Tối ưu cho cả desktop và mobile

### Animation
- **Smooth**: Chuyển động mượt mà khi số rơi xuống
- **Feedback**: Hiệu ứng khi chọn/bỏ chọn số

## Yêu cầu kỹ thuật

### Unity Version
- Unity 2021.3 LTS

### Cấu trúc project
```
Assets/
├── Scripts/
├── Prefabs/
├── Scenes/
├── UI/
└── Sprites/
```

### Cấu trúc dữ liệu
- **Mảng 1 chiều**: Xử lý dữ liệu game thuận tiện cho thuật toán
- **Prefab system**: Số ô là prefab duy nhất có script

## Tính năng kỹ thuật

### Core Features
- ✅ Hiển thị lưới số 3x9
- ✅ Logic ghép số (tổng=10, giống nhau, không chặn)
- ✅ Input điều khiển responsive
- ✅ Xử lý sau match với animation
- ✅ Hệ thống âm thanh
- ✅ Cơ chế thêm số

### Gameplay Logic
- ✅ Xử lý dữ liệu bằng mảng 1 chiều
- ✅ Thuật toán tạo màn chơi
- ✅ Cơ chế tăng stage
- ✅ Xử lý điều kiện thua

### Technical
- ✅ Cấu trúc folder hợp lý
- ✅ Prefab system tối ưu
- ✅ Code clean với comment đầy đủ

## Hướng dẫn Development

### Setup
1. Tải Unity 2021.3 LTS
2. Import project assets
3. Nghiên cứu game NumMatch gốc để hiểu logic

### Testing
- Test tất cả tính năng core
- Kiểm tra responsive trên nhiều thiết bị
- Verify thuật toán tạo màn chơi

### Build & Deploy
- Package project
- Upload lên Google Drive/GitHub

## Thuật toán

### Match Logic
Thuật toán phát hiện cặp số có thể ghép:
- Kiểm tra tổng = 10 hoặc giống nhau
- Verify đường đi không bị chặn
- Xử lý loại bỏ và dịch chuyển số

### Optimal Move Algorithm
- Tính toán 10 lời giải tối ưu
- Đánh giá số move tối thiểu
- Hỗ trợ mode thử thách

## License

[Thêm thông tin license nếu cần]

## Credits

Developed using Unity 2021.3 LTS
[Thêm thông tin tác giả và contributor]
