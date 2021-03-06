### 练习
#### 1.1
Below is a sequence of expressions. What is the result printed by the interpreter in
response to each expression? Assume that the sequence is to be evaluated in the order in which it is
presented.
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

#### 1.2
Translate the following expression into prefix form
```lisp
(/ (+ 5 (+ 4 (- 2 (- 3 (+ 6 (/ 4 3)))))) (* 3 (* (- 6 2) (- 2 7))))
```

#### 1.3
Define a procedure that takes three numbers as arguments and returns the sum of the
squares of the two larger numbers.
```lisp
(define (square x) (* x x))
(define (sum-of-squares x y ) (+ (square x) (square y)))
(define (min x y) (if (< x y) x y))
(define (max x y) (if (< x y) y x))

(define (sum-squares-2-biggest x y z)
  (
   sum-of-squares (max x y) (max z (min x y))
		  )

)
```

#### 1.4
Observe that our model of evaluation allows for combinations whose operators are
compound expressions. Use this observation to describe the behavior of the following procedure:
(define (a-plus-abs-b a b)

```txt
a plus a abs(b)
```

#### 1.5
Ben Bitdiddle has invented a test to determine whether the interpreter he is faced with is
using applicative-order evaluation or normal-order evaluation. He defines the following two
procedures:

```txt
不停执行p function
```