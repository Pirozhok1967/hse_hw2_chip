# Домашнее задание №2
Пирожкина Мария группа 4

## Задание основное
[Collab](https://colab.research.google.com/drive/10IPYai5ftrE648XTtJP4mKO1mm-EvBOv?usp=sharing) <br>
Для задания были выбраны клеточная линия DND-41, гистоновая Метка H3K27me3 <br>
<b> Анализ FastQC </b> <br>
[Папка с отчетами](https://github.com/Pirozhok1967/hse_hw2_chip/tree/main/fastqc)<br>
![Снимок экрана 2022-03-10 в 20 53 18](https://user-images.githubusercontent.com/34075090/157725868-bb01ff23-4a09-4ebe-b822-224b60703f6b.png)
![Снимок экрана 2022-03-10 в 20 53 27](https://user-images.githubusercontent.com/34075090/157725867-1b07d47a-2de3-4f88-8853-a5c71bae2b9c.png)
![Снимок экрана 2022-03-10 в 20 53 40](https://user-images.githubusercontent.com/34075090/157725865-9293175c-bea5-4fbe-81f8-78a4bf41e7cd.png)
![Снимок экрана 2022-03-10 в 20 54 03](https://user-images.githubusercontent.com/34075090/157725857-e86b532a-8616-48fb-a9fa-227aae57a248.png)
<br>
В ENCFF438GPS наблюдается большое количество ридов с большой долей GC нуклеотидов (примерно 56%), также на графике наблюдается второй пик, возможно это свойство чтений, качество чтений неочень хорошее, поэтому была сделана фильтрация. <br>
<b>ENCFF000AQN </b><br>
![Снимок экрана 2022-03-10 в 20 59 35](https://user-images.githubusercontent.com/34075090/157726149-f8c2e0d3-0110-4c1a-84e4-0008e5446689.png)
![Снимок экрана 2022-03-10 в 21 00 01](https://user-images.githubusercontent.com/34075090/157726139-bcb6e516-3be0-4735-8580-d0bb0203ca9a.png)
![Снимок экрана 2022-03-10 в 21 00 06](https://user-images.githubusercontent.com/34075090/157726144-1f70b353-8229-4978-a2f4-f3a31263d494.png)
![Снимок экрана 2022-03-10 в 21 00 15](https://user-images.githubusercontent.com/34075090/157726151-afd9c40f-2f63-4d01-b8dc-b8ba6678d959.png)<br>
 Здесь всё хорошо <br>
 <br>
<b>ENCFF000AOG </b><br>
![Снимок экрана 2022-03-10 в 21 03 02](https://user-images.githubusercontent.com/34075090/157726742-a117e3fe-3bf7-4958-8eee-75f1ec316710.png)
![Снимок экрана 2022-03-10 в 21 03 07](https://user-images.githubusercontent.com/34075090/157726748-f48018de-0c62-464f-a1dd-92374813c302.png)
![Снимок экрана 2022-03-10 в 21 03 12](https://user-images.githubusercontent.com/34075090/157726749-359043ae-3e5b-4aa9-9f76-273f9b1d3fbb.png)
![Снимок экрана 2022-03-10 в 21 03 19](https://user-images.githubusercontent.com/34075090/157726751-88063826-3970-4edf-ae78-992c8d36e5c0.png)
Здесь всё хорошо <br>
<br>
<b> Выравнивание на 14 хромосому </b> <br>
Таблицы/таблица со статистикой по каждому из 3 образцов <br>
![Снимок экрана 2022-03-10 в 21 36 22](https://user-images.githubusercontent.com/34075090/157731860-e0e18258-1a77-472d-85b1-e61803acdf61.png)<br>
По таблице видно, что много чтений (около 80%) ни разу не выровнялось, скорее всего это связано с тем, что мы картируем не на весь геном, а только на одну 14 хромосому. Также можно заметить некоторых число множественных выравниваний, возможно это какие-то повторяющиеся в нескольких местах последовательности, на которые садятся гистоны. 14 хромосома занимает от 3 до 3,5 % генома, и это примерно соотносится с количеством уникальных чтений. 
<br>
<b>Картинку с диаграммой Венна о пересечении наших MACS2 пиков и ENCODE пиков для двух реплик (pdf в репозитории) </b> <br>
[GPS](https://github.com/Pirozhok1967/hse_hw2_chip/tree/main/vene/GPS) <br>![Снимок экрана 2022-03-10 в 22 22 42](https://user-images.githubusercontent.com/34075090/157738990-3c212f55-96bb-4a71-9b2d-6067c339661f.png)
![Снимок экрана 2022-03-10 в 22 22 50](https://user-images.githubusercontent.com/34075090/157738999-440f819d-11df-4cc0-9147-9eee1eda9040.png)

[AGN](https://github.com/Pirozhok1967/hse_hw2_chip/tree/main/vene/AGN) <br>![Снимок экрана 2022-03-10 в 22 21 39](https://user-images.githubusercontent.com/34075090/157738835-a1eeb4ff-5ff2-4bff-aba0-0aa685e7b527.png)
![Снимок экрана 2022-03-10 в 22 22 11](https://user-images.githubusercontent.com/34075090/157738891-524f482f-8d37-4867-9730-c8bcf62159dc.png)

Как можно объяснить различия в количестве пересечений?<br>
Различия появляются, потому что сначала мы накладываем одни участки на другие, а потом вторые на первые
<br>
<b> Результаты выполнения бонусного задания </b> <br>
По пикам, полученным из базы данных ENCODE был построены ngs plot и heatmap для двух реплик <br>
Выбранная метка H3K27me3 присутствует после промотера в начале гена, что соответствует её обычному расположению.
![result](https://user-images.githubusercontent.com/34075090/157735771-0f1326d8-8cb7-4675-ac12-7f1f8ce88acf.png)

