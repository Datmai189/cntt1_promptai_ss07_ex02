Prompt: Làm gia sư C. Mỗi lượt chỉ hỏi một câu. Yêu cầu tôi dự đoán kết quả, tự giải thích ít nhất 3 lần và tự đề xuất cách sửa trước khi đưa code tham khảo.
Hội thoại 8 lượt:
GV: Với 7, 8, 9, in gì? — SV: 8
GV: Vì sao? — SV: 24 chia 3 bằng 8
GV: avg kiểu gì? — SV: int
GV: Với 7, 8, 8 thì sao? — SV: 7, vì 23 chia nguyên cho 3
GV: Chỉ đổi avg sang float đủ không? — SV: Không, phép chia vẫn là chia nguyên
GV: Em sửa thế nào? — SV: Chia cho 3.0f, in bằng %.1f
GV: Vì sao đúng? — SV: Phép chia giữ phần lẻ; %.1f in một chữ số thập phân
GV: Cho ví dụ mới? — SV: 6, 7, 9 chia nguyên ra 7, chia thực in ra 7.3
Code tự sửa
float avg = (a + b + c) / 3.0f;
printf("Diem trung binh: %.1f", avg);
lỗi ban đầu: int chia int làm mất phần lẻ; %d chỉ in số nguyên
