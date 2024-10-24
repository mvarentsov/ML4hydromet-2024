## Коллекция данных **DISO3***

\* **D**ataset of **I**n-**S**itu **O**bservations **o**ver the **O**cean, коллекция данных *in situ* наблюдений в море.

Эта коллекция данных унаследована от набора данных **ICOADS** [1] (International Comprehensive Ocean-Atmosphere Data Set) - набора данных попутных визуальных наблюдений и измерений. **ICOADS** содержит данные о морской поверхности и сопутствующие метеорологические наблюдения и измерения за период с 1662 года по настоящее время, а также простые сводные продукты в виде сеточных месячных массивов с разрешением сетки 2° по широте и 2° по долготе, начиная с 1800 года (и для ячеек размером 1°x1° с 1960 года). Эти данные и продукты распространяются свободно. Поскольку **ICOADS** содержит наблюдения из множества различных систем наблюдений, охватывающих развитие технологий измерения на протяжении сотен лет, **ICOADS**, вероятно, является самой полной гетерогенной коллекцией данных о морской поверхности, существующей в настоящее время.

**DISO3** - подмножество данных **ICOADS**, прошедшее тщательную фильтрацию и чистку, коррекцию значений характеристик облачности в ранние периоды наблюдений и в период смены и унификации стандартов, а также содержащее дополнительные расчетные переменные относительной влажности атмосферы (`rh`) над океаном и локальной высоты солнца (`hsun`) в точке наблюдения.

Данные коллекции **DISO3** покрывают период с 1880г. по 2017г. Данные записаны в форме таблицы с фиксированным размером колонок, без специально обозначенных разделителей. Спецификация колонок и назначение переменных описано в таблице ниже.

| No<br />кол. | Рек.<br />имя | Ширина<br />в символах | Тип<br />данных | описание переменной                                          | NaN-значение |
| ------------ | ------------- | ---------------------- | --------------- | ------------------------------------------------------------ | ------------ |
| 1            | year          | 4                      | str             | Номер года наблюдения                                        |              |
| 2            | mon           | 3                      | str             | Номер месяца наблюдения                                      |              |
| 3            | day           | 3                      | str             | Номер даты наблюдения                                        |              |
| 4            | hour          | 5                      | str             | Часовая компонента времени наблюдения                        |              |
| 5            | lat           | 10                     | float 7.2       | Широта наблюдения                                            |              |
| 6            | lon           | 9                      | float 6.2       | Долгота наблюдения                                           |              |
| 7            | hsun          | 7                      | float 4.2       | Высота солнца над горизонтом                                 |              |
| 8            | slp           | 8                      | float 5.2       | атмосферное давление в гПа                                   |              |
| 9            | ta            | 7                      | float 4.2       | температура атмосферы, °С                                    |              |
| 10           | sst           | 7                      | float 4.2       | температура поверхности океана, °С                           |              |
| 11           | td            | 7                      | float 4.2       | температура точки росы, °С                                   |              |
| 12           | rh            | 8                      | float 4.3       | относительная влажность (расчетное значение), в долях единицы |              |
| 13           | icn           | 3                      | int             | Балл общей облачности, в октах (0-8);<br />значение 9 кодирует состояние небосвода, при котором облака не могут быть наблюдены: туман, снег, др. метеорологические явления) | -9           |
| 14           | icl           | 3                      | int             | Балл облачности нижнего яруса, в окнах (0-8)                 | -9           |
| 15           | low           | 3                      | int             | Тип облачности нижнего яруса                                 | -9           |
| 16           | mid           | 3                      | int             | Тип облачности среднего яруса                                | -9           |
| 17           | high          | 3                      | int             | Тип облачности верхнего яруса                                | -9           |
| 18           | iww           | 4                      | int             | Код погоды согласно кодам ВМО по таблице 4677 [2] - коды погоды, передаваемые с неавтоматических погодных постов и станций | -99          |
| 19           | ws            | 6                      | float 4.1       | Скорость ветра, м/с                                          | -9.9         |
| 20           | wd            | 6                      | float 4.2       | Направление ветра, в градусах от направления на север        | -9.9         |

Полная коллекция данных **DISO3** в распакованном виде занимает более 15ГБ, поэтому для удобства она поставляется в виде декадных архивов с именами файлов вида `1XXX_1XXX_data.zip`, например, `1950_1959_data.zip`. В каждом из таких архивов представлены данные коллекции DISO3 за десятилетие, разбитые на помесячные файлы с именами вида `1XXX_XX_data.fwf`, например, `1880_01_data.fwf`. Далее в таблице приводятся ссылки для загрузки декадных архивов коллекции данных DISO3.

| Год начала<br />декады | Год окончания<br />декады | кол-во<br />файлов `*.fwf` | Объем архива, МБ | md5-сумма файла                  | download link                                    |
| ---------------------- | ------------------------- | -------------------------- | ---------------- | -------------------------------- | ------------------------------------------------ |
| 1880                   | 1889                      | 120                        | 16               | 29b710740539df1e70fbe8c6564af588 | [link >>](https://ml4es.ru/links/diso3-188x-zip) |
| 1890                   | 1899                      | 120                        | 2.3              | 27bff00891a92bba19d0aa3120cc7c7a | [link >>](https://ml4es.ru/links/diso3-189x-zip) |
| 1900                   | 1909                      | 120                        | 1.3              | 3d01c09c030f941444936793feccce1e | [link >>](https://ml4es.ru/links/diso3-190x-zip) |
| 1910                   | 1919                      | 120                        | 17               | fd55bec18126628b2fa74b1cbc3f71fa | [link >>](https://ml4es.ru/links/diso3-191x-zip) |
| 1920                   | 1929                      | 120                        | 39               | c046c2f40e29f50724a6611a7bebb84e | [link >>](https://ml4es.ru/links/diso3-192x-zip) |
| 1930                   | 1939                      | 120                        | 20               | 1b3000db3867bb8c2cdd3b4d52e790fb | [link >>](https://ml4es.ru/links/diso3-193x-zip) |
| 1940                   | 1949                      | 120                        | 57               | 45da349c1b84ac3b5557ef2f25577684 | [link >>](https://ml4es.ru/links/diso3-194x-zip) |
| 1950                   | 1959                      | 120                        | 204              | c1ac81818c78670fdadedfd5132a0963 | [link >>](https://ml4es.ru/links/diso3-195x-zip) |
| 1960                   | 1969                      | 120                        | 364              | a6210da57ea20c2eab759f03a5569aa1 | [link >>](https://ml4es.ru/links/diso3-196x-zip) |
| 1970                   | 1979                      | 120                        | 390              | 08fb550eb979e89ca352dc3422fb0a21 | [link >>](https://ml4es.ru/links/diso3-197x-zip) |
| 1980                   | 1989                      | 120                        | 369              | d529f785fb2e9da258a687eaab70893e | [link >>](https://ml4es.ru/links/diso3-198x-zip) |
| 1990                   | 1999                      | 120                        | 323              | 64c671cab9fba6938cfafcd09c3b9b7c | [link >>](https://ml4es.ru/links/diso3-199x-zip) |
| 2000                   | 2009                      | 120                        | 489              | 3d05fee3a57150e3302db4017f51dcab | [link >>](https://ml4es.ru/links/diso3-200x-zip) |
| 2010                   | 2017                      | 96                         | 716              | 426762cf9d751b6865065d364b230f1e | [link >>](https://ml4es.ru/links/diso3-201x-zip) |



[1] Freeman, E., S.D. Woodruff, S.J. Worley, S.J. Lubker, E.C. Kent, W.E. Angel, D.I . Berry, P. Brohan, R. Eastman, L. Gates, W. Gloeden, Z. Ji, J. Lawrimore, N.A. Rayner, G. Rosenhagen, and S.R. Smith, 2017: *ICOADS Release 3.0: A major update to the historical marine climate record*. Int. J. Climatol. (CLIMAR-IV Special Issue), 37, 2211-2237 doi:10.1002/joc.4775

[2] https://www.nodc.noaa.gov/archive/arc0021/0002199/1.1/data/0-data/HTML/WMO-CODE/WMO4677.HTM