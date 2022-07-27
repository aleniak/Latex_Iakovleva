Яковлева Алёна, второй курс ПАД
Летний мини-курс по Latex, 2022

Спасибо за этот курс, было очень интересно принимать в нем участие!

Говоря о моем гайде по Latex, я думаю, что стоит начать с пунктов, которые нужно подготовить перед тем, как приступать к работе!

1)Нужно иметь компьютер )
Очевидно, но как факт, он ведь нужен)

2)Скачать Latex или выбрать онлайн сервис, в котором можно работать.
Тут тоже все ясно, нужно иметь то, где писать код!

3)Дальше – интереснее. Теперь нужно создать документ.
Тут мы выбираем тип документа, создаем его. Тут же нужно вписать автора, дату и название.
Например: 

\documentclass{beamer}
\title[] 
{My presentation}
\subtitle{About cats}
\author{Alena Iakovleva}}
\institute{ 
  Faculty of Computer Science \\
  HSE University
}
\date{2022}

4)Как ни странно, тут же нужно закончить документ, чтобы он мог нормально компилироваться. 
Это делается так: 

\end{document}

5)Далее нам нужно выбрать, какие библиотеки мы будем использовать. Не все функции доступны без включения дополнительных библиотек.
Например: 

\usepackage[utf8]{inputenc}
\usepackage{graphicx}
\usepackage{color}
\usepackage{subcaption}

6)Теперь, когда мы подготовили свою среду к тому, чтобы в ней работать, можно начинать непосредственную работу.
Как и с любой работой, нужно выбрать то, о чем вы собираетесь писать. И особенно важно то, на каком языке вы собираетесь его писать. Я, как студентка образовательной программы Прикладной анализ данных, обычно выбираю английский, так как моя учеба полностью проходит на нем. В любом случае, можно выбрать и русский язык. Да и любой другой. В общем, подходит почти всем.

7)Далее нужно научиться создавать секции, главы и так далее.

Это очень важно для того, чтобы у документа была удобная и читаемая структура. 

Любую секцию, как и документ, нужно открыть и закрыть.

Пример кода: 

\chapter{Theory}
\end{chapter}

8)Далее стоит научиться вставлять в ваш документ картинки и различные изображения.

Тут не стоит объяснять, насколько это важно ведь изображения очевидно делают презентацию информацию более наглядной и приятной для просмотра. Например, можно вставить фото котят, чтобы поднять настроение читателям своего документа. 
Пример кода для вставки в документ:

\begin{figure}[h]
\centering
\includegraphics[width=0.5\textwidth]{/Users/aiakovleva/Documents/ACOS\ books/lab04/picture1.jpg}
\end{figure}

9)Решите, нужны ли вам таблицы. Они тоже делаются по довольно простой схеме. 

Таблицы можно создавать вручную, а можно использовать различные инструменты:

Таблицы создаются при помощи окружения tabular, а их расположение в документе и заголовки задаются в окружении table
Пример кода для создания таблицы вручную в документе:

\begin{tabular}{ |r|c|c|c|c|c|}
\multicolumn{1}{r}{Source} &  \multicolumn{1}{c}{DF} & \multicolumn{1}{c}{SS} & \multicolumn{1}{c}{MS} & \multicolumn{1}{c}{F} & \multicolumn{1}{c}{p-value} \\
\cline{1-6} Factor & k - 1 & B & B/(k - 1) & $\frac{B/(k - 1)}{W/(n - k)} & p \\
\cline{1-6} Error & n - k & W & W/(n - k) & &  \\
\cline{1-6} Total & n - 1 & B + W & & &\\
\hline
\end{tabular}

Говоря о создании не вручную, а с помощью инструментов: для это существует множество пакетов.

Также можно открыть таблицу из готового csv файла. 

10)Также в Latex можно создать различные маркированные списки. 

Пример кода для создания списка:

begin{enumerate}
\item Total variation
\[ $Total SS = B + W = $\sum\limits_{j=1}^k  $\sum\limits_{i=1}^{n_j} X_{ij}^2 - nX^2 \]

\item Residual (Error) SS
\[  $Residual (Error) SS = W =  $\sum\limits_{j=1}^k  $\sum\limits_{i=1}^{n_j} X_{ij}^2 - nX^2 - $\sum\limits_{j=1}^k n_j \overline{X}_{.j}^2  = $\sum\limits_{j=1}^k(n_j -1){S_j}^2 \]
\end{enumerate}
![image](https://user-images.githubusercontent.com/76155996/181350580-f16a0d36-ae5b-40a7-93f9-3c6765acda39.png)
