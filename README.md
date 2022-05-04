# 10.2_Study_JVM_via_VisualVM

HEAP:
![Heap graphic](https://user-images.githubusercontent.com/23313144/166655808-41e46026-13e5-4a10-80e4-3f0aad4cc76b.jpg)
Пояснение: 
1. В начале происходит незначительное увеличение heap'a за счет метода loadToMetaspaceAllFrom;
2. Затем происходит уже значительное увеличение heap'a за счет createSimpleObjects (в нем мы создаем в ArrayList'e 3 раза по 5 миллионов Объектов SimpleObject)

Metaspace:
![MetaSpace_graphic](https://user-images.githubusercontent.com/23313144/166659083-9028cf33-1cbc-4587-b6a2-74ce857703a1.jpg)
Пояснение:
1. Наблюдаем увеличение метаспейса при загрузке классов;
2. В отличие от heap'a далее метаспейс не увеличивается при созданиие Объектов SimpleObject.
