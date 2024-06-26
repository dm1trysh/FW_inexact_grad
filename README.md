# FW_inexact_grad

 В рамках курса Практика ведения научной работы мы исследовали сходимость Алгоритма Франк-Вульфа при условии неточного градиента. Используя два ранных подхода, были получены оценки сходимости. 

## Первая оценка 
```math
f(x_N) -f^{*} \leq \frac{8LD^2}{N+2} + \frac{3N \Delta ^2}{4L}
```

 Первая оценка очень похожа на оценку сходимости метода условного градиента (Теорема 1, но имеет существенный недостаток ввиде дополнительного слагаемого, включающего в себя произведение числа итераций алгоритма на квадрат ошибки, что при большом числе итераций может давать плохие результаты.

## Вторая оценка
```math
f(x_N) -f^{*} \leq \frac{\sqrt{4LD^2 (f(x_1) - f^{*})}}{\sqrt{N}} + \sqrt{2} D \Delta
```

 Вторая оценка имеет худшую скорость сходимости, что говорит о не самых точных приближениях, используемых при ее получении. Так же разность f(x1)−f∗ в числителе может быть не очень информативным показателем.

## Сравнение
 Сравнивая две полученные выше оценки, можно сказать, что первая хороша, когда количество шагов алгоритма не очень большое, например, когда мы ограничиваем выполнение алгоритма конкретным числом итераций, в противном случае
накопится большая ошибка. Вторая оценка имеет существенный недостаток из-за
того, что имеет не линейную сходимость, но в то же время накопление ошибки не
зависит от числа итераций, что может быть существенным плюсом. При выборе
оценки нужно так же следить за константами L и D, а так же ориентироваться
на исходную задачу и ее характерные черты.

 Подробнее можно ознакомиться в работе.
