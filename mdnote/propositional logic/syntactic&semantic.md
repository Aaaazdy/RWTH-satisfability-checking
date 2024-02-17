# semantic & syntactic

## 定义

- 语义后承（**semantic** consequence），符号是$\models$（\models）。语义后承在一般情况下是连接一个命题集合和一个命题。如果，在任何一种语义赋值下，只要命题集合中$\sum$的每一个命题都**为真**，那么$\phi$就一定**为真**，那么，我们就说$\phi$是$\sum$的语义后承，记作 $\sum \models \phi$ .
- 句法后承（**syntactic** consequence），符号是$\vdash$ (\vdash）。句法后承的用法和语义后承类似，也是连接一个命题集合和一个命题，如$\sum \vdash \phi$，表示的是$\phi$可以通过**句法证明**的方式从命题集$\sum$中得出。即，存在一个证明，使得每个前提要么是公理，要么是$\sum$中的命题，而证明的结论是$\phi$。具体来说，一个证明是一个命题序列，其中每个命题要么是公理，要么是前提，要么是由前面的命题通过证明规则得到的。其中最后一个称为结论。

***

## 区别

$\models$是语义 (semantic) 上的满足（一定正确的), 不谈证明. $\vdash$是语法 (syntactic) 上的满足（正确的), 不谈真假.

**Syntactic consequence (A ⊢ B)：**B 可以从 A <u>推导</u>出来，甚至**不用知道 A 是真是假**。 例如，“A 蕴含 B”可以转换为“非A 或 B”，无论“A 蕴含 B”是真还是假。 这是一个句法结果。 **模型（使 A 为真的所有可能方法）**<u>在这里并不重要</u>，因为真理并不重要，甚至 <u>A 是否为真都不重要</u>。

**Semantic consequence (C |= D)：**只要 C 为**真**，则 D 为**真**。

> e.g.
>
> > (1) If Socrates is a man, then Socrates is mortal.
> > (2) Socrates is not mortal.
> > (3) Therefore, Socrates is not a man.
>
> 为了解释为什么这个推理是有效的，可以考虑：
>
> 该结论是按照公认的规则得出的，即规则
>
> > A→B,¬B⇒¬A
>
> 这是有效性的句法概念：推理是有效的，因为它是根据给定规则正确构造的一串句子。
>
> 但是从语义上看，有悖常理。

***

## model

模型只是使格式正确的公式为真的符号组合。比如，我们在A∨B 中有 3 个可能的模型，它们是

| A     | B     | A∨B   | isModel |
| ----- | ----- | ----- | ------- |
| true  | true  | true  | true    |
| true  | false | true  | true    |
| false | true  | true  | true    |
| false | false | false | false   |

在这个例子中公式是 A∨B ，对A和B的赋值一共有四种，其中有三种使得公式为真，那么这三种对应的赋值（A和B是赋true还是false）就是三个模型。