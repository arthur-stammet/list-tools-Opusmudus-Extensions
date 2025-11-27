# List Tools Extensions

Author: **Arthur Stammet**  
Created: November 2025  
Location: `~/Opusmodus/User Source/Extensions/`

---

## 📖 Overview
The **List Tools Extensions** provide utility functions for slicing and reorganizing lists in structured ways.  
They are useful for algorithmic composition, rhythmic grouping, or any situation where you want to partition or traverse lists with regular steps and patterns.

Supported behaviours:
- **Step list** → take every *n*‑th element from a list
- **Step list loop** → partition a list into *n* interleaved sublists
- **Pendulum list** → partition into *n* sublists, alternating forward/backward order

---

## ⚙️ Functions

### `step-list`
Return every `step`‑th element from a list, starting at index 0.

```lisp
(step-list '(a b c d e f g h i j) 2)
;; → (a c e g i)
```

### `step-list-loop`
Partition a list into step sublists, each starting at offsets 0..(step-1).

```lisp
(step-list-loop '(a b c d e f g h i j) 2)
;; → ((a c e g i) (b d f h j))
```

### `pendulum-list`
Partition a list into step sublists, alternating forward and backward order.

```lisp
(pendulum-list '(a b c d e f g h i j) 3)
;; → ((a d g j) (i f c) (b e h))
```

## 📂 Installation
Place the file list-tools.opmo in:

```Code
~/Opusmodus/User Source/Extensions/
```

Restart Opusmodus, and the functions will be globally available.

## ✅ Summary
- **Step list** → simple stride extraction
- **Step list loop** → interleaved partitioning
- **Pendulum list** → pendulum alternation for expressive sequencing

Designed for algorithmic composition and creative coding workflows
