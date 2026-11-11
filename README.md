# EXE2PY - Công cụ chuyển đổi file EXE sang Python
# EXE2PY - EXE to Python Conversion Tool

#                                                     DO DUY MANH 
[![duy manh] ( https://img.shields.io/github/release/FlowiseAI/Flowise )] ( https://github.com/FlowiseAI/Flowise/releases )
[![Python Version](https://img.shields.io/badge/python-3.6%2B-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Author](https://img.shields.io/badge/author-HiepZ8-orange.svg)](https://github.com/hiep-py)

## 🇻🇳 Tiếng Việt

### Giới thiệu
EXE2PY là một bộ công cụ phân tích mạnh mẽ được thiết kế đặc biệt cho việc nghiên cứu và khôi phục mã nguồn từ các file thực thi (.exe) được đóng gói bằng PyInstaller. Công cụ này kết hợp nhiều kỹ thuật phân tích tiên tiến để giúp các nhà phát triển, chuyên gia bảo mật và kỹ sư ngược dịch truy cập vào mã Python ban đầu được nhúng trong các ứng dụng thực thi.

Được phát triển với mục tiêu cung cấp giải pháp toàn diện và thân thiện với người dùng, EXE2PY giải quyết những thách thức phức tạp trong quá trình khôi phục mã nguồn, từ việc xác định đúng phiên bản Python, xử lý các file .pyc được nén và mã hóa, đến việc chuyển đổi bytecode thành mã Python có thể đọc và chỉnh sửa được.

Công cụ sử dụng quy trình ba bước tinh vi để đảm bảo kết quả tối ưu:
1. **Trích xuất**: Phân tích cấu trúc PyInstaller archive và trích xuất tất cả các thành phần - bao gồm file .pyc, thư viện và tài nguyên
2. **Phân tích bytecode**: Chuyển đổi file .pyc sang định dạng bytecode để phân tích chuyên sâu
3. **Giải mã**: Sử dụng kỹ thuật decompile tân tiến để khôi phục mã Python từ các file bytecode

Ứng dụng thực tế của công cụ này rất đa dạng, từ khắc phục sự cố ứng dụng, mở rộng code nguồn mở, học tập kỹ thuật lập trình, đến phân tích mã độc an toàn trong môi trường cách ly.

### Tính năng chính
- 🔍 Trích xuất file từ EXE (PyInstaller archive) với phát hiện và xử lý tự động
- 🔄 Chuyển đổi file .pyc sang bytecode (.txt) để phân tích chuyên sâu
- 🧩 Giải mã bytecode thành mã Python đọc được thông qua các thuật toán tiên tiến
- 🌐 Hỗ trợ đầy đủ nhiều phiên bản Python (2.0 - 3.13) với xử lý đặc biệt cho từng phiên bản
- 🔧 Tự động phát hiện phiên bản PyInstaller và điều chỉnh phương pháp trích xuất phù hợp
- 🔐 Xử lý đặc biệt cho các file đã được mã hóa hoặc nén
- 🔄 Chức năng chuyển đổi hai chiều giữa .py và .pyc
- 🌍 Tích hợp API PyLingual.io cho khả năng giải mã nâng cao
- 🌈 Giao diện console trực quan với nhiều màu sắc và chỉ báo tiến trình
- 🗣️ Hỗ trợ đa ngôn ngữ (Tiếng Việt và Tiếng Anh) với khả năng mở rộng

### Cài đặt
```bash
# Clone repository
git clone https://github.com/hiep-py/exe2py.git

# Di chuyển vào thư mục dự án
cd exe2py

# Cài đặt các thư viện cần thiết
pip install -r requirements.txt
```

### Cách sử dụng
1. Chạy chương trình:
```bash
python exe2py.py
```

2. Chọn chức năng từ menu:
   - Bắt đầu phân tích file EXE
   - Xem thông tin về công cụ
   - Thoát
   - Thay đổi ngôn ngữ
   - Chuyển đổi file Python (py ↔ pyc)

3. Nhập đường dẫn file EXE cần chuyển đổi

4. Chọn có/không thực hiện chuyển đổi bytecode

5. Chọn có/không chuyển đổi thư viện

6. Tùy chọn: Giải mã file .pyc sang Python (.py) sử dụng API trực tuyến

### Lưu ý kỹ thuật
- File EXE phải được tạo bởi PyInstaller để có thể phân tích thành công
- Quy trình giải mã có thể có kết quả khác nhau tùy thuộc vào độ phức tạp của mã nguồn
- Có thể bỏ qua bước chuyển đổi bytecode nếu chỉ cần trích xuất tài nguyên
- Quá trình giải mã online yêu cầu kết nối internet và có thể mất nhiều thời gian
- Kết quả được lưu trong các thư mục riêng biệt để dễ quản lý và phân tích
- Công cụ hỗ trợ nhiều chiến lược decompile thay thế nếu phương pháp chính thất bại

## 🇬🇧 English

### Introduction
EXE2PY is a powerful analysis toolkit specifically designed for researching and recovering source code from executable files (.exe) packaged with PyInstaller. This tool combines multiple advanced analysis techniques to help developers, security professionals, and reverse engineers access the original Python code embedded within executable applications.

Developed with the goal of providing a comprehensive and user-friendly solution, EXE2PY addresses the complex challenges in source code recovery, from correctly identifying Python versions, handling compressed and encrypted .pyc files, to converting bytecode into readable and editable Python code.

The tool employs a sophisticated three-step process to ensure optimal results:
1. **Extraction**: Analyzes the PyInstaller archive structure and extracts all components - including .pyc files, libraries, and resources
2. **Bytecode Analysis**: Converts .pyc files to bytecode format for in-depth analysis
3. **Decompilation**: Uses advanced decompilation techniques to recover Python code from bytecode files

The practical applications of this tool are diverse, ranging from application troubleshooting, open-source code extension, programming technique learning, to safe malware analysis in isolated environments.

### Key Features
- 🔍 Extract files from EXE (PyInstaller archive) with automatic detection and handling
- 🔄 Convert .pyc files to bytecode (.txt) for in-depth analysis
- 🧩 Decompile bytecode into readable Python code through advanced algorithms
- 🌐 Full support for multiple Python versions (2.0 - 3.13) with special handling for each version
- 🔧 Auto-detect PyInstaller version and adjust extraction methods accordingly
- 🔐 Special handling for encrypted or compressed files
- 🔄 Two-way conversion functionality between .py and .pyc
- 🌍 Integration with PyLingual.io API for enhanced decompilation capabilities
- 🌈 Intuitive console interface with color coding and progress indicators
- 🗣️ Multi-language support (Vietnamese and English) with expansion capability

### Installation
```bash
# Clone repository
git clone https://github.com/hiep-py/exe2py.git

# Move to project directory
cd exe2py

# Install required libraries
pip install -r requirements.txt
```

### Usage
1. Run the program:
```bash
python exe2py.py
```

2. Choose function from menu:
   - Start analyzing EXE file
   - View tool information
   - Exit
   - Change language
   - Convert Python files (py ↔ pyc)

3. Enter the path of EXE file to convert

4. Choose whether to perform bytecode conversion

5. Choose whether to convert libraries

6. Optional: Decompile .pyc files to Python (.py) using online API

### Technical Notes
- EXE files must be created by PyInstaller for successful analysis
- The decompilation process may yield varying results depending on source code complexity
- Bytecode conversion step can be skipped if only resource extraction is needed
- Online decompilation process requires internet connection and may take considerable time
- Results are saved in separate directories for easy management and analysis
- The tool supports multiple alternative decompilation strategies if the primary method fails

## 📝 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author
- **Hồ Hiệp (HiepZ8)**
  - GitHub: [hiep-py](https://github.com/hiep-py)
  - TikTok: [@hiepz8py](https://www.tiktok.com/@hiepz8py)
  - YouTube: [@Hohiep-db2vx](https://www.youtube.com/@Hohiep-db2vx)

## ⭐ Support
If you find this tool helpful, please give it a star on GitHub! 
