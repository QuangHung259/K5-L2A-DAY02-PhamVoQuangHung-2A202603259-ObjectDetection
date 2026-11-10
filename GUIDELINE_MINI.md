# Mini guideline — bài làm cá nhân

> Điền nội dung này trước khi bắt đầu gán nhãn. Giữ lại các quyết định sau khi self-QC.

## Định nghĩa lớp

| Lớp   | Định nghĩa của bạn | Ví dụ/điểm phân biệt |
| ----- | ------------------ | -------------------- |
| `car` |

Xe con, xe du lịch và xe bán tải |

Sedan, hatchback, SUV, taxi, pickup truck |
| `truck` |

Xe tải chuyên chở hàng hóa hoặc xe đầu kéo |Xe tải thùng, xe tải chở hàng, xe đầu kéo. Không bao gồm xe bán tải |
| `bus` |
Xe buýt và minibus được thiết kế để chở hành khách |Xe buýt công cộng, xe khách, minibus chở khách |
| `van` |

Xe van hoặc minivan dùng để chở hàng hoặc chở người |Van chở hàng, van chở khách, minivan. Không bao gồm xe buýt lớn hoặc xe con thông thường |

## Quy tắc chung

- Box bám sát vật thể nghĩa là: Box bao quanh sát phần thân xe thực sự nhìn thấy được, không lấy thêm quá nhiều nền, mặt đường hoặc vật thể bên cạnh. Mỗi xe có một box riêng
- Vật thể bị che khuất: Nếu vẫn nhận diện được loại xe dựa trên phần thân xe còn nhìn thấy, tiếp tục gán nhãn theo class tương ứng. Box chỉ bao quanh phần nhìn thấy, không đoán phần bị che
- Vật thể bị cắt bởi rìa ảnh: Nếu xe bị cắt bởi mép ảnh nhưng vẫn nhận diện được class, không vẽ box vì không nhận diện được xe
- Vật thể rất nhỏ/mơ hồ: Nếu xe quá nhỏ, ở quá xa hoặc chỉ còn một phần không đủ thông tin để xác định class, không tự đoán nhãn

## Ghi lại quyết định cho ít nhất ba ca mơ hồ

| Ảnh             | Tình huống | Quyết định cuối | Lý do theo schema |
| --------------- | ---------- | --------------- | ----------------- |
| `drive_005.jpg` |

Xe bị cắt bởi rìa ảnh, chỉ còn chưa đến một nửa thân xe | còn chưa đến một nửa thân xe. | không tự ý gán box nếu xe không thấy rõ |
| `drive_012.jpg` |Xe ở rất xa, kích thước nhỏ và hình ảnh mơ hồ, không nhận diện được loại xe |Không gán nhãn khi không đủ căn cứ xác định class; ghi nhận để hỏi giảng viên |Không tự đoán class khi vật thể quá nhỏ hoặc không thể phân biệt car, truck, bus, van |
| `drive_020.jpg` |

Xe bị che bởi kết cấu cầu vượt, không nhìn thấy rõ toàn bộ thân xe |Nếu phần xe còn nhìn thấy đủ nhận diện class thì gán nhãn và vẽ box quanh phần nhìn thấy. Nếu không đủ căn cứ thì ghi nhận để hỏi giảng viên |Xe bị che một phần vẫn cần box nếu phần nhìn thấy đủ để nhận diện lớp |
