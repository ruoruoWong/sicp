### 练习
#### 1.1
```lisp
 10 ;; 10
```

```lisp
(+ 5 3 4) ;; 12
```

```lisp
(- 9 1) ;; 8
```

```lisp
(/ 6 2) ;; 3
```

```lisp
(+ (* 2 4) (- 4 6)) ;; 6
```

```lisp
(define a 3)

(define b (+ a 1))

(+ a b (* a b)) ;; 19

(= a b) ;; false

(if (and (> b a) (< b (* a b))) b a) ;; 7

(cond ((= a 4) 6)
((= b 4) (+ 6 7 a))
(else 25)) ;; 25

(+ 2 (if (> b a) b a)) ;; 9

(* (cond ((> a b) a)
((< a b) b)
(else -1))
      (+ a 1)) ;; 28
```