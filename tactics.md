Tactics
=======

exact
-----

If 

exact H : closes goal of the form

```
H : a + r = b + r → a = b
⊢ a + r = b + r → a = b
```

***

Induction a with d hd

Changes goal from
```
1 goal
P : ℕ → Prop,
n : ℕ
⊢ P n
```

to

```
2 goals
case nat.zero
P : ℕ → Prop
⊢ P 0

case nat.succ
P : ℕ → Prop,
d : ℕ,
hd : P d
⊢ P (succ d)
```

***

Example:

`induction n with d Hd,`

takes

```
1 goal
n : xnat
⊢ zero + n = n
```

to

```
2 goals
case xena.xnat.zero
⊢ zero + zero = zero

case xena.xnat.succ
d : xnat,
Hd : zero + d = d
⊢ zero + succ d = succ d
```
***

rw

does what it says on the tin.