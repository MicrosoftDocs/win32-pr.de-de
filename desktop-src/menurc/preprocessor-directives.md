---
title: Präprozessordirektiven (Menüs und andere Ressourcen)
description: Sie können die in der folgenden Tabelle beschriebenen Anweisungen nach Bedarf in Ihrem Ressourcen Skript verwenden. Sie weisen RC an, Aktionen auszuführen oder den Namen Werte zuzuweisen.
ms.assetid: 162f946e-54d8-4e23-9aa7-8e91eda4ee68
keywords:
- Ressourcen Compiler, Präprozessordirektiven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e8c32f1d32dab784d5d947fdf64b7018451a5a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340238"
---
# <a name="preprocessor-directives-menus-and-other-resources"></a>Präprozessordirektiven (Menüs und andere Ressourcen)

Sie können die in der folgenden Tabelle beschriebenen Anweisungen nach Bedarf in Ihrem Ressourcen Skript verwenden. Sie weisen RC an, Aktionen auszuführen oder den Namen Werte zuzuweisen.



| Anweisung                     | Beschreibung                                                           |
|-------------------------------|-----------------------------------------------------------------------|
| [**\#definieren**](-define.md)   | Definiert einen angegebenen Namen, indem ihm ein angegebener Wert zugewiesen wird.               |
| [**\#elif**](-elif.md)       | Markiert eine optionale Klausel eines Blocks für die bedingte Kompilierung.          |
| [**\#else**](-else.md)       | Markiert die letzte optionale Klausel eines Blocks für die bedingte Kompilierung.    |
| [**\#endif**](-endif.md)     | Markiert das Ende eines Blocks für die bedingte Kompilierung.                     |
| [**\#sei**](-if.md)           | Kompiliert das Skript bedingt, wenn ein angegebener Ausdruck true ist.  |
| [**\#ifdef**](-ifdef.md)     | Kompiliert das Skript bedingt, wenn ein angegebener Name definiert ist.     |
| [**\#ifndef**](-ifndef.md)   | Kompiliert das Skript bedingt, wenn ein angegebener Name nicht definiert ist. |
| [**\#darunter**](-include.md) | Kopiert den Inhalt einer Datei in die Ressourcen Definitionsdatei.      |
| [**\#undef**](-undef.md)     | Entfernt die Definition des angegebenen Namens.                         |



 

Zum Definieren von Symbolen für Ihre Ressourcen Bezeichner verwenden Sie die **\# define** -Direktive, um Sie in einer Header Datei zu definieren. Fügen Sie diesen Header sowohl im Ressourcen Skript als auch in den Quellcode der Anwendung ein. Entsprechend definieren Sie die Werte für Ressourcen Attribute und-Stile durch Einschließen von Windows. h in das Ressourcen Skript.

RC behandelt Dateien mit den Erweiterungen ". c" und ". h" auf besondere Weise. Dabei wird davon ausgegangen, dass eine Datei mit einer dieser Erweiterungen keine Ressourcen enthält. Wenn eine Datei die Dateinamenerweiterung ". c" oder ". h" enthält, ignoriert RC alle Zeilen in der Datei mit Ausnahme der Präprozessordirektiven. Wenn Sie also eine Datei einschließen möchten, die Ressourcen in einem anderen Ressourcen Skript enthält, geben Sie die Datei an, die eine andere Erweiterung als ". c" oder ". h" enthalten soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pragma-Direktiven](pragma-directives.md)
</dt> </dl>

 

 




