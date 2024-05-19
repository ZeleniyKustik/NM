!!!WARNING!!! 
I don't write well in English (automatic translation)


## NM

NM (Neural Module) or "Нейронный модуль"
It is a scheme for the mindustry game.
It is a tool for simulation and training of neural networks (yes, right in the game).
NM needs a mod [infinite Processor V7](https://github.com/freezemandu/infinite-processor) to work. 
It adds faster processors and roomy memory blocks.
NM has its own request-response language, thanks to which you can manage and configure NM.
NM uses the Forward-Forward algorithm ([presented by Jeffrey Hinton at the NeurIPS 2022 conference](https://arxiv.org/abs/2212.13345))
to train neural networks, as its more popular counterpart is back propagation
it requires more memory and calculations. It would also be nice to experiment with this relatively new algorithm.
NM uses a conventional perceptron as the architecture of a neural network (MLP). 
Only 1 activation function is supported (Hyperbalic tangent).

This is my first project to reach such scales. Please don't be too strict.

In the future it is planned to make NM2 with support for RNN, Back propogation, KAN. 
Also in version 2 it is planned to add more memory and add “multithreading” by adding additional processors. 
More precise network configuration is planned. 
For example:

Simple configuration:
Number of layers: 4

Number of neurons in a layer: 4
Use weights or bezier curves: Weights
Which activation function to use: ReLu
Maximum and minimum value of ReLu: -2; 3
Normalize layer: none
Pass layer signal to past layer (for RNN): no (This is the first layer of the past just no)

Number of neurons in the layer: 5
Use weights or bezier curves: bezier curves
Which activation function to use: bézier curve
Normalize layer: none
Pass layer signal to past layer (for RNN): yes
Use weights or bezier curves to transmit to past layer?: bezier curves

Number of neurons in a layer: 3
Use weights or bezier curves: bezier curves
Which activation function to use?: Hyperbolic Tangent
Normalize layer: yes
Transmit layer signal to past layer (for RNN): yes
Use weights or bezier curves to transmit to past layer?: bezier curves

Number of neurons in a layer: 2
Use weights or bezier curves: weights
Which activation function to use?: softmax
Normalize layer: yes
Pass layer signal to past layer (for RNN): yes
Use weights or bezier curves to transfer to past layer?: weights

Detailed customization:
Essentially the same thing but for each neuron separately


NM (Neural Module) или же "Нейронный модуль".
Является схемой для игры mindustry.
Это инструмент для симуляции и обучения нейронных сетей (да прям в игре).
Для работы NM нужен мод [infinite Processor V7](https://github.com/freezemandu/infinite-processor), 
он добавляет более быстрые процессоры и вместительные блоки памяти.
У NM есть свой язык типа запрос - ответ, благодаря которому можно управлять и настраивать NM.
NM использует алгорит Forward-Forward ([алгоритм представленный Джеффри Хинтоном, на конференции NeurIPS 2022](https://arxiv.org/abs/2212.13345))
для обучения нейронных сетей, так как его более популярный аналог back propogation
требует больше памяти и вычислений. 
Так же было бы не плохо по эксперементировать с этим относительно новым алгоритмом.
NM в качестве архитектуры нейросети использует обычный перцептрон (MLP). 
Потдерживаеться только 1 функция активации (Гипербалический тангенс).
Это мой первый проект достигший таких маштабов. Пожалуйста не будьте слишком строги.

В будущем планируется сделать NM2 С потдержкой RNN, Back propogation, KAN. 
Также во 2 версии планируется добавить больше памяти и добавить "многопоточность" путем добавления дополнительных процессоров. 
Планируется добавление более точной настройки сети. 
На пример:

Простая настройка:
Количество слоёв: 4

Количество нейронов в слое: 4
Использовать веса или кривые безье: веса
Какую функцию активации использовать?: ReLu
Максимальное и минимальное значение ReLu: -2; 3
Нормализировать слой: нет
Передавать сигнал слоя на прошлый слой (для RNN): нет (Это первый слой прошлого просто нет)

Количество нейронов в слое: 5
Использовать веса или кривые безье: кривые безье
Какую функцию активации использовать?: кривая бизье
Нормализировать слой: нет
Передавать сигнал слоя на прошлый слой (для RNN): да
Использовать веса или кривые безье для передачи на прошлый слой?: кривые безье

Количество нейронов в слое: 3
Использовать веса или кривые безье: кривые безье
Какую функцию активации использовать?: Гиперболический тангенс
Нормализировать слой: да
Передавать сигнал слоя на прошлый слой (для RNN): да
Использовать веса или кривые безье для передачи на прошлый слой?: кривые безье

Количество нейронов в слое: 2
Использовать веса или кривые безье: веса
Какую функцию активации использовать?: softmax
Нормализировать слой: да
Передавать сигнал слоя на прошлый слой (для RNN): да
Использовать веса или кривые безье для передачи на прошлый слой?: веса

Детальная настройка:
По сути всё тоже самое но для каждого нейрона по отдельности

NM:


![New](https://github.com/Zeleniykustik/NM/assets/126210243/1ff7ce06-c08f-4f2e-b321-7885306150fb)


<details>

<summary>Description of NM areas | Описание областей NM</summary>

| | EN | RU |
| --- | --- | --- |
| I | The memory block into which the request is entered | Блок памяти в который вводится запрос |
| O | A block of memory from which a massive response is usually output | Блок памяти из которого обычно выводится массивный ответ |
| NN | The array in which the neural network is stored | Массив в котором хранится нейронная сеть |
| DS | The array in which the Dataset is stored | Массив в котором хранится Датасет |
| NSc | This is a block for communicating with NS | Это блок для общения с NS |
| MLc | This is a block for communicating with ML | Это блок для общения с ML |
| NSr | This is NS RAM for neural network simulation | Это оперативная память NS для симуляции нейронных сетей |
| MLCB | This is the clipboard and RAM ML | Это буфер обмена и оперативная память ML |
| | | |
| T | The processor is a terminal that verifies the correctness of the request and automates the input of some variables for training | Процессор терминал, проверяющий правильность запроса и автоматизирующий ввод некоторых переменных для обучения |
| ML | The processor responsible for machine learning and working with data | Процессор отвечающий за машинное обучение и работу с данными |
| NS | The processor responsible for the simulation of neural networks  | Процессор отвечающий за симуляцию нейронных сетей |
</details>




The description of the language for communicating with NM is in [NM-language.txt](https://github.com/Zeleniykustik/NM/blob/main/NM-language.txt) |
Описание языка для общения с NM находится в [NM-language.txt](https://github.com/Zeleniykustik/NM/blob/main/NM-language.txt)

The instructions will be updated as functions are added |
Инструкция будет обновляться по мере добавления функций
