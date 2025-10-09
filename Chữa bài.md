# BTVN

**Nhóm 9:** Phân tích độ phức tạp thuật toán không đệ quy  

---

## Bài tập 1
Sắp xếp các độ phức tạp sau theo thứ tự tăng dần khi $n \to \infty$

- $O(2^n)$
- $O(\log n)$
- $O(n^3)$
- $O(n)$
- $O(n \log n)$
- $O(n^2)$
- $O(1)$
- $O(n!)$

**Thứ tự tăng dần:**  
$O(1)$ < $O(log n)$ < $O(n)$ < $O(n log n)$ < $O(n^2)$ < $O(n^3)$ < $O(2^n)$ < $O(n!)$

---

## Bài tập 2

Cho 2 hàm sau:
$f(n) = 5n^2 + 3n + 1, \quad g(n) = n^2$

Hãy chứng minh rằng: 
     $f(n) = \Theta(g(n))$ ($\Theta$ là kí hiệu Theta)

**Lời giải:**  
Ta có:  
Với $n$ đủ lớn,  
- $5n^2 + 3n + 1$ ≤ $9n^2$ ⇒ $f(n)$ ≤ $9g(n)$  
- $5n^2 + 3n + 1$ ≥ $5n^2$ ⇒ $f(n)$ ≥ $5g(n)$

⇒ Tồn tại hằng số $c_1 = 5$, $c_2 = 9$ và $n_0 = 1$ sao cho:  
$c_1 * g(n)$ ≤ $f(n)$ ≤ $c_2 * g(n)$ với mọi $n$ ≥ $n_0$.  

**Kết luận:** $f(n) = \Theta(g(n))$

---

## Bài tập 3

Cho đoạn code sau: 

```cpp
for (int i = 1; i <= n; i *= 2) {
    for (int j = 1; j <= i; j++) {
        // O(1)
    }
}
```
Dựa vào các phương pháp để phân tích độ phức tạp thời gian của thuật toán.

Đặt $(k = \lfloor \log_2 n \rfloor)$. Khi đó các giá trị của $i$ là $(2^0, 2^1, 2^2, ..., 2^k)$.  
Tổng số lần thực hiện khối $O(1)$:

$$
T(n) = \sum_{t=0}^{k} 2^t = 2^{k+1} - 1.
$$

Vì $(2^k \le n < 2^{k+1})$ nên $(T(n) < 2^{k+1} \le 2n)$.  
Suy ra:

$$
T(n) = O(n).
$$

(Mở rộng do $(T(n) \le 2n)$ và $(T(n) > n)$ nên $(T(n) = \Theta(n))$).

---

## Bài tập 4

Cho độ phức tạp của một thuật toán được mô tả bởi hàm: $T(n) = 3n^2 + 10n + 5\log n + 20$

Yêu cầu : Dựa theo **4 quy tắc phân tích độ phức tạp** hãy xác định độ phức tạp tiệm cận của $T(n)$.  

## Áp dụng quy tắc bỏ hằng số
Hệ số nhân (3, 10, 5) và hằng số cộng (20) không ảnh hưởng đến bậc tăng trưởng tiệm cận,  
nên ta có:
$$
T(n) = n^2 + n + \log n
$$

## Áp dụng quy tắc lấy max
So sánh các thành phần theo tốc độ tăng khi $n \to \infty$:
$$
n^2 > n > \log n
$$
Do đó, thành phần chiếm ưu thế là $n^2$.

## Kết luận
$$
T(n) = O(n^2)
$$

---

## Thang điểm (10/10)

| Mục | Điểm tối đa | Yêu cầu |
|------|--------------|-----------|
| Bài 1 | 2 | Sắp xếp đúng thứ tự tăng dần |
| Bài 2 | 2| Chứng minh đúng theo định nghĩa Theta |
| Bài 3 | 2 | Phân tích vòng lặp chính xác và đưa ra đúng độ phức tạp thời gian |
| Bài 4 | 2 | Xác định đúng bậc tiệm cận |
| Trình bày | 2 | Rõ ràng, dễ hiểu |
| **Tổng cộng** | **10/10** | Hoàn thành tốt |

---
