# 课时七：二元关系（1）

> **考点分布**
> 
> | 考点 | 重要程度 | 分值 | 常见题型 |
> |------|---------|------|---------|
> | 1. 有序对与笛卡尔积 | ★★★ | 0 ~ 3 | 填空、解答 |
> | 2. 二元关系 | ★★★★★ | 6 ~ 8 | 选择、填空 |
> | 3. 关系的运算 | ★★★★ | 0 ~ 4 | 填空、解答 |

---

## 1. 有序对与笛卡尔积

### 📖 基本概念

**有序对（序偶）**：由两个元素 \\(x\\) 和 \\(y\\) 按照一定顺序排列而成的二元组，记作 \\(\langle x, y \rangle\\)，其中 \\(x\\) 是第一元素，\\(y\\) 是第二元素。

**笛卡尔积**：设 \\(A, B\\) 为集合，用 \\(A\\) 中元素为第一元素，\\(B\\) 中元素为第二元素构成有序对，所有这样的有序对组成的集合称作 \\(A\\) 和 \\(B\\) 的笛卡尔积，记作 \\(A \times B\\)。

\\[
A \times B = \\{\langle x, y \rangle \mid x \in A \land y \in B\\}
\\]

**重要性质**：
- 若 \\(|A| = m\\), \\(|B| = n\\)，则 \\(|A \times B| = mn\\)

### 💡 笛卡尔积的性质

1. **空集性质**：
   - \\(A \times \emptyset = \emptyset\\)
   - \\(\emptyset \times A = \emptyset\\)

2. **不满足交换律**：
   - \\(A \times B \neq B \times A\\)（当 \\(A \neq \emptyset \land B \neq \emptyset \land A \neq B\\) 时）

3. **不满足结合律**：
   - \\((A \times B) \times C \neq A \times (B \times C)\\)（当 \\(A \neq \emptyset \land B \neq \emptyset \land C \neq \emptyset\\) 时）

4. **分配律**：
   \\[
   \begin{align}
   A \times (B \cup C) &= (A \times B) \cup (A \times C) \\\\
   (B \cup C) \times A &= (B \times A) \cup (C \times A) \\\\
   A \times (B \cap C) &= (A \times B) \cap (A \times C) \\\\
   (B \cap C) \times A &= (B \times A) \cap (C \times A)
   \end{align}
   \\]

### 📝 例题

**例题1**：设 \\(A = \\{a,b\\}\\)，\\(B = \\{0,1,2\\}\\)，求 \\(A \times B\\) 和 \\(B \times A\\)。

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**\\(A \times B\\)**：
\\[
A \times B = \\{\langle a, 0 \rangle, \langle a, 1 \rangle, \langle a, 2 \rangle, \langle b, 0 \rangle, \langle b, 1 \rangle, \langle b, 2 \rangle\\}
\\]

**\\(B \times A\\)**：
\\[
B \times A = \\{\langle 0, a \rangle, \langle 0, b \rangle, \langle 1, a \rangle, \langle 1, b \rangle, \langle 2, a \rangle, \langle 2, b \rangle\\}
\\]

**验证**：
- \\(|A| = 2\\), \\(|B| = 3\\)
- \\(|A \times B| = 2 \times 3 = 6\\) ✅
- \\(|B \times A| = 3 \times 2 = 6\\) ✅

**注意**：\\(A \times B \neq B \times A\\)（元素顺序不同）

</details>

---

## 2. 二元关系

### 📖 基本概念

**二元关系**：如果一个集合满足以下条件之一：
- 集合非空，且它的元素都是有序对
- 集合是空集

则称该集合为一个**二元关系**，记作 \\(R\\)。对于二元关系 \\(R\\)，如果 \\(\langle x,y \rangle \in R\\)，则记作 \\(xRy\\)。

**从 \\(A\\) 到 \\(B\\) 的二元关系**：设 \\(A, B\\) 为集合，\\(A \times B\\) 的任何子集所定义的二元关系称作从 \\(A\\) 到 \\(B\\) 的二元关系。

**\\(A\\) 上的二元关系**：特别当 \\(A = B\\) 时，称作 \\(A\\) 上的二元关系。

**重要性质**：
- 若 \\(|A| = n\\)，那么 \\(|A \times A| = n^2\\)
- \\(A \times A\\) 的子集有 \\(2^{n^2}\\) 个
- 因此 \\(A\\) 上有 \\(2^{n^2}\\) 个不同的二元关系

### 💡 特殊关系

**空关系**：空集 \\(\emptyset\\)

**全域关系**：
\\[
E_A = \\{\langle x, y \rangle \mid x \in A \land y \in A\\} = A \times A
\\]

**恒等关系**：
\\[
I_A = \\{\langle x, x \rangle \mid x \in A\\}
\\]

### 📊 关系的表示方法

#### 方法1：集合表达式

直接列出所有有序对。

#### 方法2：关系矩阵

设 \\(A = \\{x_1, x_2, \ldots, x_n\\}\\)，\\(R\\) 是 \\(A\\) 上的关系，\\(R\\) 的关系矩阵 \\(M_R\\) 是一个 \\(n \times n\\) 矩阵，其中：

\\[
M_R[i,j] = \begin{cases}
1 & \text{如果 } \langle x_i, x_j \rangle \in R \\\\
0 & \text{如果 } \langle x_i, x_j \rangle \notin R
\end{cases}
\\]

#### 方法3：关系图

设 \\(A = \\{x_1, x_2, \ldots, x_n\\}\\)，\\(R\\) 是 \\(A\\) 上的关系，\\(R\\) 的关系图记作 \\(G_R\\)：
- \\(G_R\\) 有 \\(n\\) 个顶点 \\(x_1, x_2, \ldots, x_n\\)
- 若 \\(\langle x_i, x_j \rangle \in R\\)，在 \\(G_R\\) 中就有一条从 \\(x_i\\) 到 \\(x_j\\) 的有向边

### 📝 例题

**例题1**：设集合 \\(X = \\{1,2,3\\}\\)，设关系 \\(R\\) 为 \\(X\\) 上的小于关系，则 \\(R =\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**小于关系**：\\(x < y\\)

\\[
R = \\{\langle 1,2 \rangle, \langle 1,3 \rangle, \langle 2,3 \rangle\\}
\\]

**答案**：\\(\\{\langle 1,2 \rangle, \langle 1,3 \rangle, \langle 2,3 \rangle\\}\\)

</details>

---

**例题2**：设 \\(A\\) 为集合，且 \\(|A| = 3\\)，则 \\(A\\) 上最多可定义\\underline{\\quad}个不同的二元关系。

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**计算**：
- \\(|A \times A| = 3^2 = 9\\)
- \\(A \times A\\) 的子集个数 = \\(2^9 = 512\\)

**答案**：512

</details>

---

**例题3**：\\(A = \\{1,2,3,4\\}\\), \\(R = \\{\langle 1,1 \rangle, \langle 1,2 \rangle, \langle 2,3 \rangle, \langle 2,4 \rangle, \langle 4,2 \rangle\\}\\)，则 \\(R\\) 的关系矩阵是？

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**关系矩阵**（按元素顺序 1, 2, 3, 4）：

\\[
M_R = \begin{bmatrix}
1 & 1 & 0 & 0 \\\\
0 & 0 & 1 & 1 \\\\
0 & 0 & 0 & 0 \\\\
0 & 1 & 0 & 0
\end{bmatrix}
\\]

**说明**：
- 第1行：\\(\langle 1,1 \rangle = 1\\), \\(\langle 1,2 \rangle = 1\\)
- 第2行：\\(\langle 2,3 \rangle = 1\\), \\(\langle 2,4 \rangle = 1\\)
- 第3行：无关系
- 第4行：\\(\langle 4,2 \rangle = 1\\)

</details>

---

**例题4**：已知集合 \\(A = \\{a,b,c\\}\\) 上的二元关系 \\(R\\) 的关系矩阵 \\(M_R = \begin{bmatrix} 0 & 1 & 0 \\\\ 1 & 1 & 0 \\\\ 1 & 0 & 0 \end{bmatrix}\\)，那么 \\(R =\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**按元素顺序 \\(a, b, c\\)**：

- 第1行（\\(a\\)）：\\(\langle a, b \rangle = 1\\)
- 第2行（\\(b\\)）：\\(\langle b, a \rangle = 1\\), \\(\langle b, b \rangle = 1\\)
- 第3行（\\(c\\)）：\\(\langle c, a \rangle = 1\\)

**答案**：\\(\\{\langle a,b \rangle, \langle b,a \rangle, \langle b,b \rangle, \langle c,a \rangle\\}\\)

</details>

---

## 3. 关系的运算

### 📖 基本概念

设 \\(R\\) 是二元关系：

#### 3.1 定义域

\\[
dom R = \\{x \mid \exists y (\langle x, y \rangle \in R)\\}
\\]

#### 3.2 值域

\\[
ran R = \\{y \mid \exists x (\langle x, y \rangle \in R)\\}
\\]

#### 3.3 域

\\[
fld R = dom R \cup ran R
\\]

#### 3.4 逆关系

\\[
R^{-1} = \\{\langle y, x \rangle \mid \langle x, y \rangle \in R\\}
\\]

#### 3.5 右复合

设 \\(F, G\\) 为二元关系，\\(G\\) 对 \\(F\\) 的右复合记作 \\(F \circ G\\)：

\\[
F \circ G = \\{\langle x, y \rangle \mid \exists t (\langle x, t \rangle \in F \land \langle t, y \rangle \in G)\\}
\\]

**含义**：先通过 \\(F\\) 关系，再通过 \\(G\\) 关系。

### 📝 例题

**例题1**：\\(R = \\{\langle 1,2 \rangle, \langle 1,3 \rangle, \langle 2,4 \rangle, \langle 4,3 \rangle\\}\\)，求 \\(dom R\\), \\(ran R\\), \\(fld R\\)。

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**定义域 \\(dom R\\)**：所有有序对的第一元素
\\[
dom R = \\{1, 2, 4\\}
\\]

**值域 \\(ran R\\)**：所有有序对的第二元素
\\[
ran R = \\{2, 3, 4\\}
\\]

**域 \\(fld R\\)**：定义域和值域的并集
\\[
fld R = dom R \cup ran R = \\{1, 2, 3, 4\\}
\\]

</details>

---

**例题2**：设 \\(F = \\{\langle 3,3 \rangle, \langle 6,2 \rangle\\}\\)，\\(G = \\{\langle 2,3 \rangle\\}\\)，求 \\(F^{-1}\\), \\(F \circ G\\), \\(G \circ F\\)。

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**\\(F^{-1}\\)（逆关系）**：
\\[
F^{-1} = \\{\langle 3,3 \rangle, \langle 2,6 \rangle\\}
\\]

**\\(F \circ G\\)（右复合）**：
- 需要找到 \\(\langle x, t \rangle \in F\\) 且 \\(\langle t, y \rangle \in G\\)
- \\(\langle 6,2 \rangle \in F\\) 且 \\(\langle 2,3 \rangle \in G\\) → \\(\langle 6,3 \rangle \in F \circ G\\)
\\[
F \circ G = \\{\langle 6,3 \rangle\\}
\\]

**\\(G \circ F\\)（右复合）**：
- 需要找到 \\(\langle x, t \rangle \in G\\) 且 \\(\langle t, y \rangle \in F\\)
- \\(\langle 2,3 \rangle \in G\\) 且 \\(\langle 3,3 \rangle \in F\\) → \\(\langle 2,3 \rangle \in G \circ F\\)
\\[
G \circ F = \\{\langle 2,3 \rangle\\}
\\]

**注意**：\\(F \circ G \neq G \circ F\\)（复合运算不满足交换律）

</details>

---

## 4. 练习题

### 练习1

设有限集 \\(A, B\\)，\\(|A| = m\\)，\\(|B| = n\\)，则笛卡尔积 \\(A \times B\\) 的子集个数有\\underline{\\quad}。

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**计算**：
- \\(|A \times B| = mn\\)
- \\(A \times B\\) 的子集个数 = \\(2^{mn}\\)

**答案**：\\(2^{mn}\\)

</details>

---

### 练习2

设 \\(A = \\{a, b\\}\\)，求 \\(P(A) \times A\\)。

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**步骤1：求 \\(P(A)\\)**

\\[
P(A) = \\{\emptyset, \\{a\\}, \\{b\\}, \\{a,b\\}\\}
\\]

**步骤2：求 \\(P(A) \times A\\)**

\\[
\begin{align}
P(A) \times A = \\{
&\langle \emptyset, a \rangle, \langle \emptyset, b \rangle, \\\\
&\langle \\{a\\}, a \rangle, \langle \\{a\\}, b \rangle, \\\\
&\langle \\{b\\}, a \rangle, \langle \\{b\\}, b \rangle, \\\\
&\langle \\{a,b\\}, a \rangle, \langle \\{a,b\\}, b \rangle
\\}
\end{align}
\\]

**答案**：共8个有序对

</details>

---

### 练习3

设 \\(A = \\{1,2,3\\}\\)，则 \\(A\\) 上有（ ）个二元关系。

A. \\(2^3\\)

B. \\(3^2\\)

C. \\(2^{2^3}\\)

D. \\(2^{3^2}\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**计算**：
- \\(|A| = 3\\)
- \\(|A \times A| = 3^2 = 9\\)
- \\(A\\) 上的二元关系个数 = \\(2^{3^2} = 2^9 = 512\\)

**答案**：D

</details>

---

### 练习4

设 \\(X = \\{a, b, c, d\\}\\)，\\(Y = \\{1, 2, 3, 4, 5\\}\\)，\\(f = \\{\langle a, 1 \rangle, \langle b, 3 \rangle, \langle c, 4 \rangle, \langle d, 4 \rangle\\}\\)，则 \\(dom f =\\underline{\\quad}\\)，\\(ran f =\\underline{\\quad}\\)。

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**定义域 \\(dom f\\)**：
\\[
dom f = \\{a, b, c, d\\}
\\]

**值域 \\(ran f\\)**：
\\[
ran f = \\{1, 3, 4\\}
\\]

**答案**：\\(\\{a, b, c, d\\}\\)，\\(\\{1, 3, 4\\}\\)

</details>

---

### 练习5

设 \\(A = \\{1,2,3,4,5,6\\}\\)，\\(B = \\{1,2,3\\}\\)，从 \\(A\\) 到 \\(B\\) 的关系 \\(R = \\{\langle x,y \rangle \mid x = 2y\\}\\)，则 \\(R^{-1} =\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**步骤1：求 \\(R\\)**

\\(x = 2y\\)，且 \\(x \in A\\), \\(y \in B\\)：
- \\(y = 1\\) → \\(x = 2\\) → \\(\langle 2,1 \rangle\\)
- \\(y = 2\\) → \\(x = 4\\) → \\(\langle 4,2 \rangle\\)
- \\(y = 3\\) → \\(x = 6\\) → \\(\langle 6,3 \rangle\\)

\\[
R = \\{\langle 2,1 \rangle, \langle 4,2 \rangle, \langle 6,3 \rangle\\}
\\]

**步骤2：求 \\(R^{-1}\\)**

\\[
R^{-1} = \\{\langle 1,2 \rangle, \langle 2,4 \rangle, \langle 3,6 \rangle\\}
\\]

**答案**：\\(\\{\langle 1,2 \rangle, \langle 2,4 \rangle, \langle 3,6 \rangle\\}\\)

</details>

---

### 练习6

\\(R_1 = \\{\langle 1,2 \rangle, \langle 1,3 \rangle, \langle 2,3 \rangle\\}\\)，\\(R_2 = \\{\langle 2,2 \rangle, \langle 2,3 \rangle, \langle 3,4 \rangle\\}\\)，求：

(1) \\(R_2 - R_1\\)

(2) \\(R_2^{-1}\\)

(3) \\(R_2 \circ R_1\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**(1) \\(R_2 - R_1\\)（差集）**

\\[
R_2 - R_1 = \\{\langle 2,2 \rangle, \langle 3,4 \rangle\\}
\\]
（\\(\langle 2,3 \rangle\\) 在 \\(R_1\\) 中，所以被减去）

**(2) \\(R_2^{-1}\\)（逆关系）**

\\[
R_2^{-1} = \\{\langle 2,2 \rangle, \langle 3,2 \rangle, \langle 4,3 \rangle\\}
\\]

**(3) \\(R_2 \circ R_1\\)（右复合）**

需要找到 \\(\langle x, t \rangle \in R_1\\) 且 \\(\langle t, y \rangle \in R_2\\)：
- \\(\langle 1,2 \rangle \in R_1\\) 且 \\(\langle 2,2 \rangle \in R_2\\) → \\(\langle 1,2 \rangle\\)
- \\(\langle 1,2 \rangle \in R_1\\) 且 \\(\langle 2,3 \rangle \in R_2\\) → \\(\langle 1,3 \rangle\\)
- \\(\langle 2,3 \rangle \in R_1\\) 且 \\(\langle 3,4 \rangle \in R_2\\) → \\(\langle 2,4 \rangle\\)

\\[
R_2 \circ R_1 = \\{\langle 1,2 \rangle, \langle 1,3 \rangle, \langle 2,4 \rangle\\}
\\]

**答案**：
- (1) \\(\\{\langle 2,2 \rangle, \langle 3,4 \rangle\\}\\)
- (2) \\(\\{\langle 2,2 \rangle, \langle 3,2 \rangle, \langle 4,3 \rangle\\}\\)
- (3) \\(\\{\langle 1,2 \rangle, \langle 1,3 \rangle, \langle 2,4 \rangle\\}\\)

</details>

---

## 📌 总结

### 关键要点

1. **笛卡尔积**：
   - \\(|A \times B| = |A| \times |B|\\)
   - 不满足交换律和结合律
   - 满足分配律（对并、交运算）

2. **二元关系**：
   - \\(A\\) 上的二元关系个数：\\(2^{n^2}\\)（\\(n = |A|\\)）
   - 特殊关系：空关系、全域关系、恒等关系

3. **关系的表示**：
   - 集合表达式
   - 关系矩阵
   - 关系图

4. **关系的运算**：
   - 定义域、值域、域
   - 逆关系
   - 右复合

### 记忆技巧

- **笛卡尔积元素个数**：\\(m \times n\\)
- **关系个数**：\\(2^{n^2}\\)
- **右复合**：先 \\(F\\) 后 \\(G\\)，即 \\(F \circ G\\)
