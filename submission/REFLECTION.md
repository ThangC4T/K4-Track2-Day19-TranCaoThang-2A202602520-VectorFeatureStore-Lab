# Reflection — Lab 19

**Tên:** Trần Cao Thắng
**Cohort:** A20-K4
**Path đã chạy:** lite

---

## Câu hỏi (≤ 200 chữ)

> Trên golden set 50 queries, mode nào thắng ở loại query nào (`exact` /
> `paraphrase` / `mixed`), và tại sao? Khi nào bạn **không** dùng hybrid
> (i.e. khi nào pure BM25 hoặc pure vector là lựa chọn đúng)?

Trên golden set 50 queries, benchmark lite cho thấy hybrid RRF thắng trung bình:
BM25 77.8%, semantic 73.2%, hybrid 78.6%. Với `exact`, BM25 và hybrid cùng cao
nhất vì query chứa thuật ngữ xuất hiện nguyên văn trong corpus. Với `mixed`,
hybrid thắng rõ nhất (100.0%) vì kết hợp được tín hiệu keyword chính xác và ngữ
nghĩa. Với `paraphrase`, kết quả lite thấp hơn do `bge-small-en-v1.5` là model
thiên tiếng Anh; semantic không luôn thắng tiếng Việt diễn đạt lại. Em sẽ không
dùng hybrid khi query gần như toàn exact keyword và cần latency/rank dễ giải
thích, lúc đó BM25 đủ tốt; hoặc khi người dùng diễn đạt tự nhiên đa ngôn ngữ và
có embedding multilingual mạnh như `bge-m3`, pure vector có thể hợp lý hơn.

---

## Điều ngạc nhiên nhất khi làm lab này

Điều bất ngờ nhất là hybrid không cần “model thông minh hơn” vẫn thắng nhờ
fusion đơn giản, nhưng chất lượng paraphrase lại phụ thuộc rất mạnh vào model
embedding.

---

## Bonus challenge

- [ ] Đã làm bonus (xem `bonus/`)
- [ ] Pair work với: _<tên đồng đội nếu có>_
