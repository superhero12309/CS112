# BTVN

**Nhóm 9:** Phân tích độ phức tạp thuật toán không đệ quy  

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

## Bài tập 2
Cho 2 hàm sau:
$f(n) = 5n^2 + 3n + 1, \quad g(n) = n^2$

Hãy chứng minh rằng: 
     $f(n) = \Theta(g(n))$ ($\Theta$ là kí hiệu Theta)


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

## Bài tập 4
Cho độ phức tạp của một thuật toán được mô tả bởi hàm: $T(n) = 3n^2 + 10n + 5\log n + 20$

Yêu cầu : Dựa theo **4 quy tắc phân tích độ phức tạp** hãy xác định độ phức tạp tiệm cận của $T(n)$.  