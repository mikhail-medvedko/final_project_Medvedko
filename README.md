# final_project_Medvedko
Михаил Медведко, BAE'26, Финальный проект по курсу "Наука о Данных"

## О проекте
В рамках проекта я анализирую макроэкономические данные о закредитованности россиян. Отдельное внимание уделяется кредитам в микрофинансовых и микрокредитных организациях популярность которых, к сожалению, в последние несколько лет только растет. Я смотрю на общие статистические данные, предоставленные ЦБ и Росстатом, анализирую данные по закредитованности в региональном разрезе и проверяю гипотезу о портрете среднего заемщика в МФО. 

## Технические моменты

1. В проекте данные для многих графиков были взяты из excel-таблиц ЦБ или Росстата, на сайтах они присутствуют только в таком виде. Я обычно предварительно вытягивал нужные показатели в отдельный csv-файл, чтобы сократить количество ненужного кода для выделения отдельных строчек из нагруженных многостраничных статистических сводок. Оригиналы всех файлов могут быть найдены в папке data_raw, уже подготовленные csv лежат в репозитории.
2. Для отрисовки нескольких карт по регионам я использовал карту России в GeoJSON. К сожалению, весит она больше 25мб и поэтому я не нашел способа загрузить ее на GitHub. В превью файла с проектом (final_project_Medvedko.ipynb) карты отображаются (по крайней мере у меня), но если вы хотите запускать ячейки с кодом, придется скачать файл Russia_geojson_OSM/GeoJson's/Countries/Russia_regions.geojson из репозитория по ссылке: https://github.com/timurkanaz/Russia_geojson_OSM/tree/master и приложить его к Google Collab.
3. В проекте есть интерактивные графики, которые у меня лично в превью не отрисовываются. Чтобы посмотреть на их отрисовку с кодом, опять же, придется загрузить необходимые файлы в Google Collab и запустить ячкейки.

## Использованные технлогии и библиотеки

1. **matplotlib** и **plotly** для визуализации данных, в том числе интерактивных графиков
2. **pandas** и **numpy** для работы с датасетами и данными внутри них
3. **geopandas** для работы с географическими данными 
4. **requests** и **BeautifulSoup** для веб-скреппинга и работы с API
5. **statsmodels** для сглаживания сезонности и отслеживания трендов в данных
6. **регулярные выражения** для соединения датасетов
