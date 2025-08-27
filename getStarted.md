# Добро пожаловать в документацию по разработке модификаций для Geometry Dash на индексе Geode.

Итак, вы наверняка знакомы с различными модификациями, которые облегчили вам игру или исправляли баги криворукого Роберта Лопаты

Так вот! Наверное вам тоже интересно как создаются моды в фреймворке Geode? Если да, то эта документация должна помочь вам разобраться в мире Geometry Dash, с её внутреностями и её секретами.

Скажу честно, я писал эту документацию по своим навыкам кодинга на C++ - поэтому, могут быть недочеты!

## Установка программ
<ins>**Для работы с модами вам потребуется следующее:**</ins>

- **Предварительное** знание C++. Так как изучать C++ параллельно с созданием модов очень сложно;
- Установка самого [Geode](https://geode-sdk.org/install/) для тестрования своих модов;

## Компиляторы C++
Чтобы использовать Geode SDK и, в свою очередь, создавать моды Geometry Dash, вам понадобится либо:
- [Visual Studio 2022](https://visualstudio.microsoft.com/ru/thank-you-downloading-visual-studio/?sku=Community&channel=Release&version=VS2022&source=VSLandingPage&cid=2030&passive=false) для Windows
- [Clang](https://docs.geode-sdk.org/getting-started/cpp-stuff/#macos) для MacOS
- [Секретная третья вещь](https://github.com/xDarinox/GeometryDashCreateMod/blob/main/getStarted.md#linux) для Linux

## Требования для C++
### Windows
Загрузите [Visual Studio 2022](https://visualstudio.microsoft.com/ru/thank-you-downloading-visual-studio/?sku=Community&channel=Release&version=VS2022&source=VSLandingPage&cid=2030&passive=false) с веб-сайта. Если вам нужен только компилятор, а не редактор кода, найдите инструменты сборки для Visual Studio ниже на странице.

После запуска программы установки выберите "Разработка на рабочем столе с использованием C++". Вы можете выбрать другие функции, но вам потребуется установить как минимум MSVC и Windows SDK.\
После установки Visual Studio у вас должен быть работающий компилятор C++, подходящий для разработки GD модов.

<ins>**Пожалуйста, обратите внимание, что требуется Visual Studio 2022 или выше. Версии 2019 или ниже работать не будут, так как они не поддерживают C++20 должным образом.**</ins>
### MacOS
Установите [brew](https://brew.sh/), если у вас его еще нет, а затем запустите:

```cmd
brew install llvm
```
### Linux
С Linux немного сложнее, так как официального релиза GD для Linux пока нет. Конечно, вы можете довольно хорошо запускать версию GD для Windows с помощью программного обеспечения, такого как [wine](https://www.winehq.org/), что, вероятно, вы уже делаете.\
По этой причине в этом руководстве вы научитесь [кросс-компиляции](https://en.wikipedia.org/wiki/Cross_compiler) Windows Geode mods из Linux.\
Во-первых, помимо Git и CMake, убедитесь, что у вас установлены ``clang`` и ``lld``.

- **On Ubuntu:**
```cmd
apt install clang-19 clang-tools-19 lld-19
```
- **On Arch-based systems:**
```cmd
pacman -S clang lld
```
Следующим шагом будет установка Windows SDK и набора инструментов CMake. Для упрощения установки сначала установите [Geode CLI](https://docs.geode-sdk.org/getting-started/geode-cli), а затем вернитесь сюда. Если вы хотите сделать это вручную, вы можете следовать [этому руководству](https://gist.github.com/matcool/abb65ee59ded3766717c673014c3a2a7).

После установки интерфейса командной строки запустите эту команду, чтобы установить все необходимые инструменты:
```cmd
geode sdk install-linux
```
[Следующий шаг ->](https://github.com/xDarinox/GeometryDashCreateMod/blob/main/docs/start/geodeCLI.md)
