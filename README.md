# 1 edition

Программа работает с файлом как с текстовым:
* ищется строка с раскрывающимеся скобками ( по типу [] ) 
* перед ней по-жесткому вставляются for-строки
* а вместо пустых [] вставляются символы

---

\
Пока что не найдено как лучше раскрывать. Кажется если считать скобки до ```=``` и после вставлять циклически индексы, то можно красиво складывать и перемножать матрицы:
```
a[][] = b[][] + c[][]

=>      for(int i_0 = 0; i_0 < k_size(a, 0); i_0++)
        for(int i_1 = 0; i_1 < k_size(a, 1); i_1++)
            a[i_0][i_1] += b[i_0][i_1] + c[i_0][i_1]
```


```
a[][] += b[][t:] * c[t][]

=>      for(... i_0 ...) for(... i_1 ...)
        for(int t = 0; t < k_size(b, 1); t++)
            a[i_0][i_1] += b[i_0][t] * c[t][i_1]
```

