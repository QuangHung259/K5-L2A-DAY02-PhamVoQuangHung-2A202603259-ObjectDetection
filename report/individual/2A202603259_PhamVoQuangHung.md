# Báo cáo cá nhân — Ngày 2 Object Detection

Đổi tên file theo `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md`. Điền kết quả thật, xóa dòng hướng dẫn khi nộp. Xem [quy định nộp](../../SUBMISSION.md).

## 1. Thông tin học viên

- Họ tên:Phạm Võ Quang Hưng
- MSSV: 2A202603259
- Email:quanghungphamvo@gmail.com
- Lớp: 2B
- Link repo bài làm: https://github.com/QuangHung259/K5-L2A-DAY02-PhamVoQuangHung-2A202603259-ObjectDetection
- Link Colab đã chạy: https://colab.research.google.com/drive/1k58yBMduh0r-_smS46p617w6OsinBn5e?usp=sharing

## 2. Schema và mini guideline

Dẫn tới [GUIDELINE_MINI.md](https://github.com/QuangHung259/K5-L2A-DAY02-PhamVoQuangHung-2A202603259-ObjectDetection/blob/main/GUIDELINE_MINI.md). Tóm tắt ba ca mơ hồ đã quyết định, cách áp dụng schema và phần cần giảng viên làm rõ.

## 3. Annotation và self-QC

- Số file nhãn train: 50
- Kết quả checker và lỗi đã xử lý:
- Danh sách ít nhất 10 ảnh đã rà bằng mắt: drive_001.jpg, drive_002.jpg, drive_003.jpg, drive_004.jpg, drive_005.jpg, drive_006.jpg, drive_007.jpg, drive_008.jpg, drive_009.jpg, drive_0010.jpg
- Lỗi bỏ sót/box/class phát hiện khi rà và cách sửa:
- Commit khóa nhãn ban đầu:

## 4. Gold QC và rework

| Chỉ số | Trước sửa | Sau sửa nếu có |
|---|---:|---:|
| TP |439 | |
| FP |420 | |
| FN |214 | |
| Precision |0.5111 | |
| Recall |0.6723 | |
| F1 |0.5807 | |
| mean_iou_of_matches |0.8295 | |
| passed |false | |

Dẫn tới `outputs/annotation_evaluation.json` trong repo. Nếu rework, ghi ảnh, lỗi đã kiểm, quyết định sửa/giữ và lý do. Không suy nguyên nhân chỉ từ FP/FN. Không có rework thì ghi rõ.

## 5. Kết quả YOLO

- Runtime, GPU/CPU, phiên bản Ultralytics và Torch:
- Các tham số thay đổi so với notebook nếu có và lý do:
- Đường dẫn best checkpoint trong phiên chạy:

| Chỉ số trên 10 ảnh eval | Giá trị |
|---|---:|
| Precision |0.18277673848474232 |
| Recall | 0.3119919067017738|
| mAP50 | 0.2876445145316125|
| mAP50–95 | 0.2003699371515734|

Đặt cả 2 folder `assets/eval_predictions/` và `assets/yolo26_runs/` (giải nén từ `day2_colab_outputs.zip`) cạnh báo cáo và dẫn link tương đối. Không chỉ ghi số; chỉ ra ít nhất một ảnh và vật thể cụ thể.

Trả lời bốn câu hỏi cuối notebook:

1. Lớp nào recall thấp nhất? Ảnh nào minh họa?
2. Nếu mAP50 cao nhưng mAP50–95 thấp, cần kiểm điều gì trên box?
3. Lỗi class nào có thể liên quan guideline? Dữ kiện nào hỗ trợ nhận xét?
4. Vì sao không dùng 10 ảnh eval để train? Vai trò validation của chúng trong notebook là gì?

## 6. Khó khăn và cách xử lý

| Bước/thời điểm | Lỗi quan sát | Cách đã thử | Kết quả/còn thiếu |
|---|---|---|---|
| chạy gold_train_labels| nhiều hình còn thiếu box đã gắn và nhiều hình còn dư box | dán thêm những hình còn thiếu | không thực hiện được tất cả các hình còn thiếu box hoặc dư |

## 7. Tự đánh giá theo rubric

Đối chiếu [RUBRIC.md](../../RUBRIC.md): phần nào đã có kết quả, phần nào còn thiếu hoặc chưa kiểm được. Không tự nhận hoàn thành bước chưa chạy.

## 8. Công cụ AI và tài liệu tham khảo

Ghi công cụ đã dùng, dùng ở bước nào và phần đã tự kiểm tra; không dùng thì ghi rõ. Liệt kê nguồn ngoài repo được sử dụng. Không ghi mật khẩu/token hoặc đính kèm gold train.
