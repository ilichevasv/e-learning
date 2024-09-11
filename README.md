# e-learning
В данном проекте: 
- были проведены предварительные исследование, предобработка и подготовка данных,
- был проведен анализ о данных об уроках, курсах, тестах, сдаваемых студентами,
- построена RFM-кластеризация.

# Задачи, выполненные в рамках проекта:
1. Определить, сколько студентов успешно сдали только один курс.
2. Выявить самый сложный и самый простой экзамен: найди курсы и экзамены в рамках курса, которые обладают самой низкой и самой высокой завершаемостью*.
3. По каждому предмету определить средний срок сдачи экзаменов.
4. Выявить ТОП-3 популярных предметов по количеству регистраций на них. А также ТОП-3 предметов с самым большим оттоком.
5. В период с начала 2013 по конец 2014 выявить семестр с самой низкой завершаемостью курсов и самыми долгими средними сроками сдачи курсов.
6. Построить адаптированные RFM-кластеры студентов, чтобы качественно оценить аудиторию, со следующими метриками: R - среднее время сдачи одного экзамена, F - завершаемость курсов, M - среднее количество баллов, получаемое за экзамен.

# Описание данных:
- assessments.csv — этот файл содержит информацию об оценках в тесте. Обычно каждый предмет в семестре включает ряд тестов с оценками, за которыми следует заключительный экзаменационный тест (экзамен).
  - code_module — идентификационный код предмета.
  - code_presentation — семестр (Идентификационный код).
  - id_assessment — тест (Идентификационный номер ассессмента).
  - assessment_type — тип теста. Существуют три типа оценивания: оценка преподавателя (TMA), компьютерная оценка (СМА), экзамен по курсу (Exam).
  - date — информация об окончательной дате сдачи теста. Рассчитывается как количество дней с момента начала семестра. Дата начала семестра имеет номер 0 (ноль).
  - weight — вес теста в % в оценке за курс. Обычно экзамены рассматриваются отдельно и имеют вес 100%; сумма всех остальных оценок составляет 100%.
- courses.csv — файл содержит список предметов по семестрам.
  - code_module — предмет (идентификационный код).
  - code_presentation — семестр (идентификационный код).
  - module_presentation_length — продолжительность семестра в днях.
- studentAssessment.csv — этот файл содержит результаты тестов студентов. Если учащийся не отправляет работу на оценку, результат не записывается в таблицу.
  - id_assessment — тест (идентификационный номер).
  - id_student — идентификационный номер студента.
  - date_submitted — дата сдачи теста студентом, измеряемая как количество дней с начала семестра.
  - is_banked — факт перезачета теста с прошлого семестра (иногда курсы перезачитывают студентам, вернувшимся из академического отпуска).
  - score — оценка учащегося в этом тесте. Диапазон составляет от 0 до 100. Оценка ниже 40 неудачная/неуспешная сдача теста.
- studentRegistration.csv — этот файл содержит информацию о времени, когда студент зарегистрировался для прохождения курса в семестре.
  - code_module — предмет (идентификационный код).
  - code_presentation — семестр (идентификационный код)
  - id_student — идентификационный номер студента.
  - date_registration — дата регистрации студента. Это количество дней, измеренное от начала семестра (например, отрицательное значение -30 означает, что студент зарегистрировался на прохождение курса за 30 дней до его начала).
  - date_unregistration — дата отмены регистрации студента с предмета. У студентов, окончивших курс, это поле остается пустым.

# Примечание
Данный проект является учебным, был выполнен в рамках проекта "Аналитик данных".
