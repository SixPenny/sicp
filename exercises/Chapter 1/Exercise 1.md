## Exercise 1.1
10                                       answer: 10
(+ 5 3 4)                                answer: 12 
(- 9 1)                                  answer: 8
(/ 6 2)                                  answer: 3
(+ (* 2 4) (- 4 6))                      answer: 6
(define a 3)                             answer: a
(define b (+ a 1))                       answer: b
(+ a b (* a b))                          answer: 19
(= a b)                                  answer: #f
(if (and (> b a) (< b (* a b)))          
	b                                        
	a)                                   answer: 4
(cond ((= a 4) 6)                        
	((= b 4) (+ 6 7 a))                  
	(else 25))                           answer: 16
(+ 2 (if (> b a) b a))                   answer: 6
(* (cond ((> a b) a)                     
	((< a b) b)                              
	(else -1))                               
	(+ a 1))                             answer: 16
	
## Exercise 1.2
$$\frac{5 + 4 + ( 2 - ( 3 - ( 6 + {4\over 5} ) ) ) }{ 3(6 - 2)(2 - 7)}$$ 
(/ (+ 5 (+ 4 (- 2 (- 3 (+ 6 (/ 4 5)))))) (* 3 (* (- 6 2) (- 2 7))))

##Exercise 1.3
(define (square x) (* x x))
(define (isbetween x y z) (and (>= x y) (<= x z)))
(define (ismax x y z) (and (>= x y) (>= x z)))
(define (sencond_max_of_three x y z) (cond ((isbetween x y z) x) ((isbetween y x z) y) ((isbetween z y x) z)))
(define (max_of_tree x y z) (cond ((ismax x y z) x) ((ismax y x z) y) ((ismax z x y) z) ))
(define (sum_of_max_two_square x y z) (+ (square (max_of_tree x y z)) (square (sencond_max_of_three x y z))))

##Exercise 1.4
(define (a-plus-abs-b a b) (if (> b 0) + -) a b) 操作符也可以使用表达式来计算，妙！

