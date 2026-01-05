# 课时五：谓词逻辑等值演算与推理

> **考点分布**
> 
> | 考点 | 重要程度 | 分值 | 常见题型 |
> |------|---------|------|---------|
> | 1. 谓词逻辑等值式与置换规则 | ★★★ | 0 ~ 4 | 选择、填空 |
> | 2. 谓词逻辑前束范式 | ★★★★ | 0 ~ 4 | 选择、解答 |
> | 3. 谓词逻辑推理理论 | 🔥必考 | 6 ~ 12 | 证明 |

---

## 1. 谓词逻辑等值式与置换规则

### 📖 基本概念

设 \\(A, B\\) 是谓词逻辑中任意两个公式，若 \\(A \leftrightarrow B\\) 是**永真式**，则称 \\(A\\) 与 \\(B\\) 等值，记作 \\(A \Leftrightarrow B\\)。

### 📚 基本等值式

#### 1.1 量词否定等值式

设公式 \\(A(x)\\) 含自由出现的个体变项 \\(x\\)，则：

\\[
\begin{align}
\neg \forall x A(x) &\Leftrightarrow \exists x \neg A(x) \\\\
\neg \exists x A(x) &\Leftrightarrow \forall x \neg A(x)
\end{align}
\\]

**记忆技巧**：
- 否定全称 = 存在否定
- 否定存在 = 全称否定

#### 1.2 量词辖域收缩与扩张等值式

设公式 \\(A(x)\\) 含自由出现的个体变项 \\(x\\)，\\(B\\) 不含 \\(x\\) 的自由出现，则：

**全称量词**：
\\[
\begin{align}
\forall x (A(x) \vee B) &\Leftrightarrow \forall x A(x) \vee B \\\\
\forall x (A(x) \land B) &\Leftrightarrow \forall x A(x) \land B \\\\
\forall x (A(x) \rightarrow B) &\Leftrightarrow \exists x A(x) \rightarrow B \\\\
\forall x (B \rightarrow A(x)) &\Leftrightarrow B \rightarrow \forall x A(x)
\end{align}
\\]

**存在量词**：
\\[
\begin{align}
\exists x (A(x) \vee B) &\Leftrightarrow \exists x A(x) \vee B \\\\
\exists x (A(x) \land B) &\Leftrightarrow \exists x A(x) \land B \\\\
\exists x (A(x) \rightarrow B) &\Leftrightarrow \forall x A(x) \rightarrow B \\\\
\exists x (B \rightarrow A(x)) &\Leftrightarrow B \rightarrow \exists x A(x)
\end{align}
\\]

#### 1.3 量词分配等值式

设公式 \\(A(x), B(x)\\) 含自由出现的个体变项 \\(x\\)，则：

\\[
\begin{align}
\forall x (A(x) \land B(x)) &\Leftrightarrow \forall x A(x) \land \forall x B(x) \\\\
\exists x (A(x) \vee B(x)) &\Leftrightarrow \exists x A(x) \vee \exists x B(x) \\\\
\forall x A(x) \vee \forall x B(x) &\Rightarrow \forall x (A(x) \vee B(x)) \\\\
\exists x (A(x) \land B(x)) &\Rightarrow \exists x A(x) \land \exists x B(x)
\end{align}
\\]

**注意**：后两个是**推理关系**（\\(\Rightarrow\\)），不是等值关系（\\(\Leftrightarrow\\)）。

#### 1.4 命题逻辑重言式的代换实例

命题逻辑中的重言式的代换实例都是谓词逻辑中的永真式。

例如：
- \\(\forall x F(x) \Leftrightarrow \neg \neg \forall x F(x)\\)
- \\(F(x) \to G(y) \Leftrightarrow \neg F(x) \lor G(y)\\)

### 📝 例题

**例题1**：设个体域 \\(D = \\{a,b,c\\}\\)，将下列公式的量词消去：

(1) \\(\forall x(F(x) \to G(x))\\)

(2) \\(\forall x(F(x) \lor \exists yG(y))\\)

(3) \\(\exists x \forall y F(x,y)\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**(1) \\(\forall x(F(x) \to G(x))\\)**

**消去量词**：
\\[
(F(a) \to G(a)) \land (F(b) \to G(b)) \land (F(c) \to G(c))
\\]

**(2) \\(\forall x(F(x) \lor \exists yG(y))\\)**

**步骤1：缩小量词辖域**

使用量词辖域收缩等值式：
\\[
\forall x(F(x) \lor \exists yG(y)) \Leftrightarrow \forall x F(x) \lor \exists y G(y)
\\]

**步骤2：消去量词**

\\[
(F(a) \land F(b) \land F(c)) \vee (G(a) \vee G(b) \vee G(c))
\\]

**(3) \\(\exists x \forall y F(x,y)\\)**

**步骤1：先消去 \\(\forall y\\)**

\\[
\exists x (F(x,a) \land F(x,b) \land F(x,c))
\\]

**步骤2：再消去 \\(\exists x\\)**

\\[
\begin{align}
&(F(a,a) \land F(a,b) \land F(a,c)) \\\\
&\quad \vee (F(b,a) \land F(b,b) \land F(b,c)) \\\\
&\quad \vee (F(c,a) \land F(c,b) \land F(c,c))
\end{align}
\\]

</details>

---

**例题2**：设 \\(B\\) 是不含变元 \\(x\\) 的公式，谓词公式 \\((\exists x)(B \to A(x))\\) 等价于（ ）。

A. \\(B \to (\exists x) A(x)\\)

B. \\(B \to (\forall x) A(x)\\)

C. \\((\exists x) A(x) \to B\\)

D. \\(B \to A(x)\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**使用量词辖域收缩等值式**：

\\(\exists x (B \to A(x)) \Leftrightarrow \forall x B \to \exists x A(x)\\)

但更简单的方法是使用：\\(\exists x (B \to A(x)) \Leftrightarrow B \to \exists x A(x)\\)

因为 \\(B\\) 不含 \\(x\\)，所以：
\\[
\exists x (B \to A(x)) \Leftrightarrow B \to \exists x A(x)
\\]

**答案**：A

**说明**：
- 当 \\(B\\) 不含 \\(x\\) 时，\\(\exists x (B \to A(x)) \Leftrightarrow B \to \exists x A(x)\\)
- 这是量词辖域收缩等值式的应用

</details>

---

**例题3**：谓词公式 \\(\forall x \exists y P(x,y)\\) 的真值为？其中，\\(P(x,y)\\)：\\(x = y\\)，定义域：\\(D = \\{1,2\\}\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**步骤1：先消去 \\(\exists y\\)**

\\[
\forall x (P(x,1) \lor P(x,2))
\\]

**步骤2：再消去 \\(\forall x\\)**

\\[
(P(1,1) \lor P(1,2)) \land (P(2,1) \lor P(2,2))
\\]

**步骤3：计算真值**

- \\(P(1,1) = 1\\)（1 = 1为真）
- \\(P(1,2) = 0\\)（1 = 2为假）
- \\(P(2,1) = 0\\)（2 = 1为假）
- \\(P(2,2) = 1\\)（2 = 2为真）

所以：
\\[
(1 \vee 0) \land (0 \vee 1) = 1 \land 1 = 1
\\]

**答案**：1（真）

</details>

---

## 2. 谓词逻辑前束范式

### 📖 基本概念

**前束范式**：具有如下形式的谓词逻辑公式：

\\[
Q_1 x_1 Q_2 x_2 \ldots Q_k x_k B
\\]

其中 \\(Q_i (1 \leq i \leq k)\\) 为 \\(\forall\\) 或 \\(\exists\\)，\\(B\\) 为不含量词的公式。

**特点**：
- 所有量词都在公式的最前面
- 量词后面是不含量词的公式

**示例**：
- ✅ \\(\forall x \forall y(F(x) \land G(y) \to H(x,y))\\) 是前束范式
- ❌ \\(\forall x (F(y) \to \exists y (G(y) \land H(x,y)))\\) 不是前束范式（量词不在最前面）

**前束范式存在定理**：谓词逻辑中的任何公式都存在等值的前束范式。

### 📝 转换方法

**步骤**：

1. **把条件或双条件联结词转化**：\\(A \to B \Leftrightarrow \neg A \lor B\\)
2. **利用量词否定公式，把否定深入到命题变元和谓词公式的前面**
3. **换名**：如果量词指导变元冲突，需要换名
4. **利用量词作用域的扩张和收缩等价式，把量词提到前面**

### 📝 例题

**例题1**：下列哪项为前束范式（ ）。

A. \\(\neg \forall x F(x)\\)

B. \\(\exists x F(x) \to \forall x G(x)\\)

C. \\(\exists x \exists y (F(x,t) \to G(x,y))\\)

D. \\(\exists x F(x) \to H(x,y)\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**检查每个选项**：

**选项A**：\\(\neg \forall x F(x)\\)
- 量词在否定后面，不是前束范式 ❌

**选项B**：\\(\exists x F(x) \to \forall x G(x)\\)
- 量词在蕴涵式两侧，不是前束范式 ❌

**选项C**：\\(\exists x \exists y (F(x,t) \to G(x,y))\\)
- 所有量词都在最前面 ✅
- 后面是不含量词的公式 ✅
- **是前束范式** ✅

**选项D**：\\(\exists x F(x) \to H(x,y)\\)
- 量词不在最前面 ❌

**答案**：C

</details>

---

**例题2**：求下列各式的前束范式：

(1) \\(\forall x F(x) \land \neg \exists x G(x)\\)

(2) \\(\forall x_1 F(x_1,x_2) \to \neg \exists x_2 G(x_2)\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**(1) \\(\forall x F(x) \land \neg \exists x G(x)\\)**

\\[
\begin{align}
&\forall x F(x) \land \neg \exists x G(x) \\\\
\Leftrightarrow &\forall x F(x) \land \forall x \neg G(x) \quad \text{（量词否定等值式）} \\\\
\Leftrightarrow &\forall x F(x) \land \forall y \neg G(y) \quad \text{（换名）} \\\\
\Leftrightarrow &\forall x \forall y (F(x) \land \neg G(y)) \quad \text{（量词分配）}
\end{align}
\\]

**答案**：\\(\forall x \forall y (F(x) \land \neg G(y))\\)

**(2) \\(\forall x_1 F(x_1,x_2) \to \neg \exists x_2 G(x_2)\\)**

\\[
\begin{align}
&\forall x_1 F(x_1,x_2) \to \neg \exists x_2 G(x_2) \\\\
\Leftrightarrow &\neg \forall x_1 F(x_1,x_2) \lor \neg \exists x_2 G(x_2) \quad \text{（蕴涵等值式）} \\\\
\Leftrightarrow &\exists x_1 \neg F(x_1,x_2) \lor \exists x_2 G(x_2) \quad \text{（量词否定等值式）} \\\\
\Leftrightarrow &\exists x_1 \neg F(x_1,x_2) \lor \exists x_3 G(x_3) \quad \text{（换名）} \\\\
\Leftrightarrow &\exists x_1 \exists x_3 (\neg F(x_1,x_2) \lor G(x_3)) \quad \text{（量词分配）}
\end{align}
\\]

**答案**：\\(\exists x_1 \exists x_3 (\neg F(x_1,x_2) \lor G(x_3))\\)

</details>

---

## 3. 谓词逻辑推理理论 🔥必考重点

### 📖 基本概念

在谓词逻辑中，从前提 \\(A_1, A_2, \ldots, A_k\\) 出发推出结论 \\(B\\) 的推理的形式结构：

\\[
A_1 \land A_2 \land \ldots \land A_k \to B
\\]

若上式为**永真式**，则推理正确，否则称推理不正确。

### 📚 推理定律

#### 3.1 命题逻辑推理定律的代换实例

例如：
- \\(\forall x F(x) \land \forall y G(y) \Rightarrow \forall x F(x)\\)（化简律）
- \\(\forall x F(x) \Rightarrow \forall x F(x) \vee \exists y G(y)\\)（附加律）

#### 3.2 基本等值式生成的推理实例

例如：
- \\(\neg \forall x F(x) \Rightarrow \exists x \neg F(x)\\)（量词否定等值式）
- \\(\exists x \neg F(x) \Rightarrow \neg \forall x F(x)\\)（量词否定等值式）

#### 3.3 常用的重要推理定律

\\[
\begin{align}
\forall x A(x) \vee \forall x B(x) &\Rightarrow \forall x (A(x) \vee B(x)) \\\\
\exists x (A(x) \land B(x)) &\Rightarrow \exists x A(x) \land \exists x B(x) \\\\
\forall x (A(x) \to B(x)) &\Rightarrow \forall x A(x) \to \forall x B(x) \\\\
\forall x (A(x) \to B(x)) &\Rightarrow \exists x A(x) \to \exists x B(x)
\end{align}
\\]

#### 3.4 量词消去和引入规则

**全称量词消去规则** \\((\forall -)\\)：
- \\(\forall x G(x) \Rightarrow G(y)\\)，\\(y\\) 不在 \\(G(x)\\) 中约束出现
- 或 \\(\forall x G(x) \Rightarrow G(c)\\)，\\(c\\) 为任意个体常量

**存在量词消去规则** \\((\exists -)\\)：
- \\(\exists x G(x) \Rightarrow G(c)\\)，\\(c\\) 为使得 \\(G(c)\\) 为真的特定的个体常量

**全称量词引入规则** \\((\forall +)\\)：
- \\(G(c) \Rightarrow \forall x G(x)\\)，\\(G(c)\\) 中无变元 \\(x\\)

**存在量词引入规则** \\((\exists +)\\)：
- \\(G(c) \Rightarrow \exists x G(x)\\)，\\(c\\) 为特定个体常量

### 📝 例题

**例题1**：构造下面推理的证明

**前提**：\\(\forall x(F(x) \to G(x))\\), \\(\exists x(F(x) \land H(x))\\)

**结论**：\\(\exists x(G(x) \land H(x))\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**证明**：

| 步骤 | 公式 | 依据 |
|------|------|------|
| ① | \\(\exists x(F(x) \land H(x))\\) | 前提引入 |
| ② | \\(F(a) \land H(a)\\) | ① \\(\exists -\\) |
| ③ | \\(F(a)\\) | ② 化简律 |
| ④ | \\(H(a)\\) | ② 化简律 |
| ⑤ | \\(\forall x (F(x) \to G(x))\\) | 前提引入 |
| ⑥ | \\(F(a) \to G(a)\\) | ⑤ \\(\forall -\\) |
| ⑦ | \\(G(a)\\) | ③⑥ 假言推理 |
| ⑧ | \\(G(a) \land H(a)\\) | ④⑦ 合取 |
| ⑨ | \\(\exists x(G(x) \land H(x))\\) | ⑧ \\(\exists +\\) |

**得证**：\\(\exists x(G(x) \land H(x))\\) 是有效结论。

**证明思路**：
1. 从存在量词前提中引入个体 \\(a\\)
2. 使用全称量词消去规则，得到 \\(F(a) \to G(a)\\)
3. 使用假言推理得到 \\(G(a)\\)
4. 合取得到 \\(G(a) \land H(a)\\)
5. 使用存在量词引入规则得到结论

</details>

---

**例题2**：构造下面推理证明：

**前提**：\\(\forall x(F(x) \lor G(x))\\)

**结论**：\\(\neg \forall x F(x) \to \exists x G(x)\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**证明**：使用**附加前提法**

| 步骤 | 公式 | 依据 |
|------|------|------|
| ① | \\(\neg \forall x F(x)\\) | 附加前提引入 |
| ② | \\(\exists x \neg F(x)\\) | ① 置换（量词否定等值式） |
| ③ | \\(\neg F(a)\\) | ② \\(\exists -\\) |
| ④ | \\(\forall x(F(x) \lor G(x))\\) | 前提引入 |
| ⑤ | \\(F(a) \lor G(a)\\) | ④ \\(\forall -\\) |
| ⑥ | \\(G(a)\\) | ③⑤ 析取三段论 |
| ⑦ | \\(\exists x G(x)\\) | ⑥ \\(\exists +\\) |

**得证**：\\(\neg \forall x F(x) \to \exists x G(x)\\) 是有效结论。

**证明思路**：
1. 引入附加前提 \\(\neg \forall x F(x)\\)
2. 使用量词否定等值式转换为存在量词
3. 使用存在量词消去规则引入个体 \\(a\\)
4. 从全称量词前提中得到 \\(F(a) \lor G(a)\\)
5. 使用析取三段论得到 \\(G(a)\\)
6. 使用存在量词引入规则得到结论

</details>

---

**例题3**：证明下列各式

所有北极熊都是白色的，没有棕熊是白色的，所以北极熊不是棕熊。

<details>
<summary><strong>点击查看答案</strong></summary>

**解**：命题符号化

- \\(F(x)\\)：\\(x\\) 是北极熊
- \\(G(x)\\)：\\(x\\) 是白色的
- \\(H(x)\\)：\\(x\\) 是棕熊

**前提**：
- \\(\forall x(F(x) \to G(x))\\)
- \\(\neg \exists x(H(x) \land G(x))\\)

**结论**：\\(\forall x(F(x) \to \neg H(x))\\)

**证明**：使用**归谬法**

| 步骤 | 公式 | 依据 |
|------|------|------|
| ① | \\(\neg \forall x(F(x) \to \neg H(x))\\) | 结论的否定引入 |
| ② | \\(\exists x(F(x) \land H(x))\\) | ① 置换 |
| ③ | \\(F(a) \land H(a)\\) | ② \\(\exists -\\) |
| ④ | \\(F(a)\\) | ③ 化简律 |
| ⑤ | \\(H(a)\\) | ③ 化简律 |
| ⑥ | \\(\forall x(F(x) \to G(x))\\) | 前提引入 |
| ⑦ | \\(F(a) \to G(a)\\) | ⑥ \\(\forall -\\) |
| ⑧ | \\(G(a)\\) | ④⑦ 假言推理 |
| ⑨ | \\(H(a) \land G(a)\\) | ⑤⑧ 合取 |
| ⑩ | \\(\exists x(H(x) \land G(x))\\) | ⑨ \\(\exists +\\) |

**分析**：
- 第⑩步得到 \\(\exists x(H(x) \land G(x))\\)
- 但前提中有 \\(\neg \exists x(H(x) \land G(x))\\)
- 矛盾！所以推理正确

**得证**：\\(\forall x(F(x) \to \neg H(x))\\) 是有效结论。

</details>

---

## 4. 练习题

### 练习1

下列四个公式正确的有（ ）。

A. \\(\forall x(A(x) \land B(x)) \Rightarrow \forall x A(x) \land \forall x B(x)\\)

B. \\(\forall x(A(x) \lor B(x)) \Rightarrow \forall x A(x) \lor \forall x B(x)\\)

C. \\(\exists x(A(x) \lor B(x)) \Rightarrow \exists x A(x) \lor \exists x B(x)\\)

D. \\(\exists x A(x) \land \exists x B(x) \Rightarrow \exists x(A(x) \land B(x))\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**选项A**：\\(\forall x(A(x) \land B(x)) \Rightarrow \forall x A(x) \land \forall x B(x)\\)
- 这是量词分配等值式，正确 ✅

**选项B**：\\(\forall x(A(x) \lor B(x)) \Rightarrow \forall x A(x) \lor \forall x B(x)\\)
- 这是单方向推理，但方向反了 ❌
- 正确应该是：\\(\forall x A(x) \lor \forall x B(x) \Rightarrow \forall x(A(x) \lor B(x))\\)

**选项C**：\\(\exists x(A(x) \lor B(x)) \Rightarrow \exists x A(x) \lor \exists x B(x)\\)
- 这是等值式，正确 ✅

**选项D**：\\(\exists x A(x) \land \exists x B(x) \Rightarrow \exists x(A(x) \land B(x))\\)
- 这是单方向推理，但方向反了 ❌
- 正确应该是：\\(\exists x(A(x) \land B(x)) \Rightarrow \exists x A(x) \land \exists x B(x)\\)

**答案**：A、C

</details>

---

### 练习2

在个体域 \\(D = \\{1, 2\\}\\) 中，若 \\(f(1) = 2\\)，\\(f(2) = 1\\)，谓词 \\(P\\) 有 \\(P(1,1) = T\\)，\\(P(1,2) = F\\)，\\(P(2,1) = T\\)，\\(P(2,2) = F\\)，求 \\((\forall x)(\exists y)(P(x,y) \to P(y,f(x)))\\) 的真值。

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**步骤1：消去内层存在量词**

\\[
\forall x ((P(x,1) \to P(1,f(x))) \lor (P(x,2) \to P(2,f(x))))
\\]

**步骤2：计算每个 \\(f(x)\\) 的值**

- \\(f(1) = 2\\)，所以 \\(P(1,f(1)) = P(1,2) = F\\)
- \\(f(2) = 1\\)，所以 \\(P(2,f(2)) = P(2,1) = T\\)

**步骤3：消去全称量词**

\\[
\begin{align}
&((P(1,1) \to P(1,f(1))) \lor (P(1,2) \to P(2,f(1)))) \\\\
&\quad \land ((P(2,1) \to P(1,f(2))) \lor (P(2,2) \to P(2,f(2))))
\end{align}
\\]

**步骤4：代入真值**

\\[
\begin{align}
&((T \to F) \lor (F \to F)) \land ((T \to T) \lor (F \to T)) \\\\
=& (F \lor T) \land (T \lor T) \\\\
=& T \land T \\\\
=& T
\end{align}
\\]

**答案**：真（T）

</details>

---

### 练习3

下列等价关系正确的是（ ）。

A. \\(\forall x(P(x) \lor Q(x)) \Leftrightarrow \forall x P(x) \lor \forall x Q(x)\\)

B. \\(\exists x(P(x) \lor Q(x)) \Leftrightarrow \exists x P(x) \lor \exists x Q(x)\\)

C. \\(\forall x(P(x) \to Q) \Leftrightarrow \forall x P(x) \to Q\\)

D. \\(\exists x(P(x) \to Q) \Leftrightarrow \exists x P(x) \to Q\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**选项A**：\\(\forall x(P(x) \lor Q(x)) \Leftrightarrow \forall x P(x) \lor \forall x Q(x)\\)
- 这是单方向推理，不是等值 ❌

**选项B**：\\(\exists x(P(x) \lor Q(x)) \Leftrightarrow \exists x P(x) \lor \exists x Q(x)\\)
- 这是量词分配等值式，正确 ✅

**选项C**：\\(\forall x(P(x) \to Q) \Leftrightarrow \forall x P(x) \to Q\\)
- 当 \\(Q\\) 不含 \\(x\\) 时，这是量词辖域收缩等值式，但需要检查
- \\(\forall x(P(x) \to Q) \Leftrightarrow \exists x P(x) \to Q\\)（量词辖域收缩等值式）
- 但题目中是 \\(\forall x P(x) \to Q\\)，不一定等价 ❌

**选项D**：\\(\exists x(P(x) \to Q) \Leftrightarrow \exists x P(x) \to Q\\)
- 当 \\(Q\\) 不含 \\(x\\) 时，\\(\exists x(P(x) \to Q) \Leftrightarrow \forall x P(x) \to Q\\)
- 但题目中是 \\(\exists x P(x) \to Q\\)，不一定等价 ❌

**答案**：B

</details>

---

### 练习4

设个体域 \\(D = \\{a, b, c\\}\\)，消去公式中的量词。

(1) \\(\exists x F(x) \to \forall y G(y)\\)

(2) \\(\forall x \forall y(F(x) \to G(y))\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**(1) \\(\exists x F(x) \to \forall y G(y)\\)**

\\[
\begin{align}
&\exists x F(x) \to \forall y G(y) \\\\
\Leftrightarrow &(F(a) \vee F(b) \vee F(c)) \to (G(a) \land G(b) \land G(c))
\end{align}
\\]

**(2) \\(\forall x \forall y(F(x) \to G(y))\\)**

\\[
\begin{align}
&\forall x \forall y(F(x) \to G(y)) \\\\
\Leftrightarrow &\forall x ((F(x) \to G(a)) \land (F(x) \to G(b)) \land (F(x) \to G(c))) \\\\
\Leftrightarrow &(F(a) \to G(a)) \land (F(a) \to G(b)) \land (F(a) \to G(c)) \\\\
&\quad \land (F(b) \to G(a)) \land (F(b) \to G(b)) \land (F(b) \to G(c)) \\\\
&\quad \land (F(c) \to G(a)) \land (F(c) \to G(b)) \land (F(c) \to G(c))
\end{align}
\\]

**答案**：
- (1) \\((F(a) \vee F(b) \vee F(c)) \to (G(a) \land G(b) \land G(c))\\)
- (2) 所有 \\(F(x) \to G(y)\\) 的合取（共9项）

</details>

---

### 练习5

下列谓词公式中是前束范式的是（ ）。

A. \\((\forall x)F(x) \land \neg (\exists x)G(x)\\)

B. \\((\forall x)F(x) \lor (\forall y)G(y)\\)

C. \\((\forall x)(\exists y)(P(x) \to Q(x,y))\\)

D. \\((\forall x)(P(x) \to (\exists y)Q(x,y))\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

**检查每个选项**：

**选项A**：\\((\forall x)F(x) \land \neg (\exists x)G(x)\\)
- 量词不在最前面（有否定在中间）❌

**选项B**：\\((\forall x)F(x) \lor (\forall y)G(y)\\)
- 两个量词分别在不同部分，不是统一的前束范式 ❌

**选项C**：\\((\forall x)(\exists y)(P(x) \to Q(x,y))\\)
- 所有量词都在最前面 ✅
- 后面是不含量词的公式 ✅
- **是前束范式** ✅

**选项D**：\\((\forall x)(P(x) \to (\exists y)Q(x,y))\\)
- 存在量词 \\(\exists y\\) 不在最前面 ❌

**答案**：C

</details>

---

### 练习6

求合式公式 \\(\exists x P(x) \to \exists x Q(x,y)\\) 的前束范式

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

\\[
\begin{align}
&\exists x P(x) \to \exists x Q(x,y) \\\\
\Leftrightarrow &\neg \exists x P(x) \lor \exists x Q(x,y) \quad \text{（蕴涵等值式）} \\\\
\Leftrightarrow &\forall x \neg P(x) \lor \exists x Q(x,y) \quad \text{（量词否定等值式）} \\\\
\Leftrightarrow &\forall x \neg P(x) \lor \exists z Q(z,y) \quad \text{（换名）} \\\\
\Leftrightarrow &\forall x \exists z (\neg P(x) \lor Q(z,y)) \quad \text{（量词分配）}
\end{align}
\\]

**答案**：\\(\forall x \exists z (\neg P(x) \lor Q(z,y))\\)

</details>

---

### 练习7

求谓词公式的前束范式：\\(\neg \forall x (F(x) \to G(x))\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**解答**：

\\[
\begin{align}
&\neg \forall x (F(x) \to G(x)) \\\\
\Leftrightarrow &\exists x \neg (F(x) \to G(x)) \quad \text{（量词否定等值式）} \\\\
\Leftrightarrow &\exists x \neg (\neg F(x) \lor G(x)) \quad \text{（蕴涵等值式）} \\\\
\Leftrightarrow &\exists x (F(x) \land \neg G(x)) \quad \text{（德摩根律）}
\end{align}
\\]

**答案**：\\(\exists x (F(x) \land \neg G(x))\\)

</details>

---

### 练习8

在自然推理系统F中构造下面推理的证明：

**前提**：\\(\exists x F(x) \to \forall y(G(y) \to H(y))\\), \\(\exists x R(x) \to \exists y G(y)\\)

**结论**：\\(\exists x(F(x) \land R(x)) \to \exists x H(x)\\)

<details>
<summary><strong>点击查看答案</strong></summary>

**证明**：使用**附加前提法**

| 步骤 | 公式 | 依据 |
|------|------|------|
| ① | \\(\exists x(F(x) \land R(x))\\) | 附加前提引入 |
| ② | \\(F(a) \land R(a)\\) | ① \\(\exists -\\) |
| ③ | \\(F(a)\\) | ② 化简律 |
| ④ | \\(R(a)\\) | ② 化简律 |
| ⑤ | \\(\exists x F(x) \to \forall y(G(y) \to H(y))\\) | 前提引入 |
| ⑥ | \\(\exists x F(x)\\) | ③ \\(\exists +\\) |
| ⑦ | \\(\forall y(G(y) \to H(y))\\) | ⑤⑥ 假言推理 |
| ⑧ | \\(\exists x R(x) \to \exists y G(y)\\) | 前提引入 |
| ⑨ | \\(\exists x R(x)\\) | ④ \\(\exists +\\) |
| ⑩ | \\(\exists y G(y)\\) | ⑧⑨ 假言推理 |
| ⑪ | \\(G(b)\\) | ⑩ \\(\exists -\\) |
| ⑫ | \\(G(b) \to H(b)\\) | ⑦ \\(\forall -\\) |
| ⑬ | \\(H(b)\\) | ⑪⑫ 假言推理 |
| ⑭ | \\(\exists x H(x)\\) | ⑬ \\(\exists +\\) |

**得证**：\\(\exists x(F(x) \land R(x)) \to \exists x H(x)\\) 是有效结论。

</details>

---

### 练习9

先将下列推理符号化，再利用推理规则证明推理的正确性。

所有的大一学生都要学习英语；并非所有的大一学生都要学习离散数学；故有些学习英语的不学习离散数学。

假设谓词如下：\\(P(x)\\)：\\(x\\) 是大一学生；\\(Q(x)\\)：\\(x\\) 要学习英语；\\(R(x)\\)：\\(x\\) 要学习离散数学。

<details>
<summary><strong>点击查看答案</strong></summary>

**符号化**：

**前提**：
- \\(\forall x(P(x) \to Q(x))\\)
- \\(\neg \forall x(P(x) \to R(x))\\)

**结论**：\\(\exists x(Q(x) \land \neg R(x))\\)

**证明**：

| 步骤 | 公式 | 依据 |
|------|------|------|
| ① | \\(\neg \forall x(P(x) \to R(x))\\) | 前提引入 |
| ② | \\(\exists x \neg (P(x) \to R(x))\\) | ① 置换（量词否定等值式） |
| ③ | \\(\exists x (P(x) \land \neg R(x))\\) | ② 置换（蕴涵等值式、德摩根律） |
| ④ | \\(P(a) \land \neg R(a)\\) | ③ \\(\exists -\\) |
| ⑤ | \\(P(a)\\) | ④ 化简律 |
| ⑥ | \\(\neg R(a)\\) | ④ 化简律 |
| ⑦ | \\(\forall x(P(x) \to Q(x))\\) | 前提引入 |
| ⑧ | \\(P(a) \to Q(a)\\) | ⑦ \\(\forall -\\) |
| ⑨ | \\(Q(a)\\) | ⑤⑧ 假言推理 |
| ⑩ | \\(Q(a) \land \neg R(a)\\) | ⑥⑨ 合取 |
| ⑪ | \\(\exists x(Q(x) \land \neg R(x))\\) | ⑩ \\(\exists +\\) |

**得证**：\\(\exists x(Q(x) \land \neg R(x))\\) 是有效结论。

</details>

---

## 📌 总结

### 关键要点

1. **量词否定等值式**：
   - \\(\neg \forall x A(x) \Leftrightarrow \exists x \neg A(x)\\)
   - \\(\neg \exists x A(x) \Leftrightarrow \forall x \neg A(x)\\)

2. **量词分配等值式**：
   - \\(\forall x (A(x) \land B(x)) \Leftrightarrow \forall x A(x) \land \forall x B(x)\\)
   - \\(\exists x (A(x) \vee B(x)) \Leftrightarrow \exists x A(x) \vee \exists x B(x)\\)

3. **前束范式**：所有量词都在公式最前面，后面是不含量词的公式

4. **量词消去和引入规则**：
   - \\(\forall -\\)：从全称量词消去
   - \\(\exists -\\)：从存在量词消去
   - \\(\forall +\\)：引入全称量词
   - \\(\exists +\\)：引入存在量词

### 记忆技巧

- **量词否定**：否定全称 = 存在否定，否定存在 = 全称否定
- **前束范式**：量词全部提到最前面
- **推理步骤**：消去量词 → 命题逻辑推理 → 引入量词
