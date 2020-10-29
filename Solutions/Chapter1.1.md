#### Exercise 1.1 输出以下表达式的值

```scheme
10
(+ 5 3 4)
(- 9 1)
(/ 6 2)
(+ (* 2 4) (- 4 6))
(define a 3)
(define b (+ a 1))
(+ a b (* a b))
(= a b)
(if (and (> b a) (< b (* a b)))
    b
    a)
(cond ((= a 4) 6)
      ((= b 4) (+ 6 7 a))
      (else 25))
(+ 2
   (if (> b a) b a))
(* (cond ((> a b) a)
         ((< a b) b)
         (else -1))
   (+ a 1))
```

**答案**

```html
10
12
8
3
6
Value: a ; a = 3
Value: b ; b = 4
19
#f
4
16
6
16
```



#### Exercise 1.2 前缀表示

```scheme
(/ (+ 5
      4
      (- 2
         (- 3
            (+ 6
               (/ 4 5)))))
   (* 3
      (- 6 2)
      (- 2 7)))
;; -37/150
```



#### Exercise 1.3 定义过程，以三个数为参数，返回较大的两个数之和

```scheme
(define (two_max_sum a b c) 
  (if (> a b)
      (if (> b c)
          (+ a b)
          (+ a c))
      (if (> a c)
          (+ b a)
          (+ b c))))
  ;; (two_max_sum 1 2 3)
  ;; 5
```



#### Exercise 1.4 描述下面过程的行为

```scheme
(define (a-plus-abs-b a b)
  ((if (> b 0) + -) a b))
;; (a-plus-abs-b 1 -3) 4
;; (a-plus-abs-b 1 3) 4
;; A + |B|：A加上B的绝对值
```



#### Exercise 1.5 应用序和正则序求解

```scheme
(define (p) (p))
(define (test x y)
  (if (= x 0)
      0
      y))
(test 0 (p))
```

**应用序**



**正则序**





