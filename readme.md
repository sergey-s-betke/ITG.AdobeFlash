Adobe Flash Player для применения в корпоративной сети
======================================================

MSI пакет для распространения через GPO Adobe Flash Player.

Всем известна проблема с распространением через GPO Flash player, с его обновлением и отключением автообновления.
В этом пакете указанные проблемы решены.

P.S.Данное решение не предназначено для Windows 8, потому как в указанной ОС flash player уже входит в комплект
поставки.

Развёртывание пакета через GPO
------------------------------

Подготовленная административная точка установки расположена в подкаталоге [itgAdobeFlash\bin\Release\x64](../../tree/master/itgAdobeFlash/bin/Release/x64).
Дополнительной подготовки файла `itgAdobeFlash.msi` через `msiexec -a itgAdobeFlash.msi` не требуется.
Скачайте целиком папку указанную выше папку, разместите на сетевом ресурсе, и - разверните через GPO.

P.S. Версия для x86 - [itgAdobeFlash\bin\Release\x86](../../tree/master/itgAdobeFlash/bin/Release/x86).

Сборка .msi пакета
------------------

Для внесения изменений в пакет и повторной сборки пакета потребуются следующие продукты:

- Microsoft Visual Studio 2012 Shell:
  - [Isolated](http://www.microsoft.com/ru-ru/download/details.aspx?id=30670)
  - [Integrated](http://www.microsoft.com/ru-ru/download/details.aspx?id=30663)
- [Windows Installer XML Toolset - WIX](http://wixtoolset.org/)

Установить необходимо все пакеты в указанном порядке. В результате - получае MS Visual Studio 2012 с подготовленными
шаблонами проектов WiX. После этого открываем файл решения `itgAdobeFlash.sln` и собираем решение.

Дополнительные сведения
-----------------------

- [достаточно богатая на примеры статья по использованию WiX](http://habrahabr.ru/post/68616/)
