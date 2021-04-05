---
title: Starke Typisierung
description: C ist eine schwach typisierte Sprache, d. h. der Compiler lässt Vorgänge wie Zuweisung und Vergleich zwischen Variablen verschiedener Typen zu.
ms.assetid: 5f52adcc-22b9-4b4f-b921-5996d278b10e
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, Dateneingabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea859e2d5c160048d79e3c371b47af2bc55e0a65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948058"
---
# <a name="strong-typing"></a>Starke Typisierung

C ist eine schwach typisierte Sprache, d. h. der Compiler lässt Vorgänge wie Zuweisung und Vergleich zwischen Variablen verschiedener Typen zu. Beispielsweise lässt C zu, dass der Wert einer Variablen in einen anderen Typ umgewandelt wird. Die Möglichkeit, Variablen unterschiedlicher Typen im gleichen Ausdruck zu verwenden, fördert Flexibilität und Effizienz.

Eine stark typisierte Sprache erzwingt Einschränkungen für Vorgänge zwischen Variablen unterschiedlicher Typen. In diesen Fällen gibt der Compiler einen Fehler aus, der den Vorgang untersagt. Diese strengen Richtlinien bezüglich der Datentypen sind darauf ausgelegt, potenzielle Fehler zu vermeiden.

Die Schwierigkeit bei der Verwendung einer schwach typisierten Sprache wie z. b. C für Remote Prozedur Aufrufe besteht darin, dass verteilte Anwendungen auf verschiedenen Computern mit unterschiedlichen C-Compilern und verschiedenen Architekturen ausgeführt werden können. Wenn eine Anwendung nur auf einem Computer ausgeführt wird, müssen Sie sich nicht mit dem internen Datenformat beschäftigen, da die Daten konsistent verarbeitet werden. In einer verteilten Computerumgebung können von verschiedenen Computern jedoch unterschiedliche Definitionen für die Basis Datentypen verwendet werden. Einige Computer definieren z. b. den **int** -Typ, sodass die interne Darstellung 16 Bits beträgt, während andere Computer 32 Bits verwenden. Eine Computerarchitektur, die als "Little Endian" bezeichnet wird, weist der niedrigsten Speicheradresse und dem signifikantesten der höchsten Adresse das am wenigsten signifikante Byte zu. Eine andere Architektur, die als "Big Endian" bezeichnet wird, weist das am wenigsten signifikante Byte der höchsten Speicheradresse zu, die diesen Daten zugeordnet ist.

Remote Prozedur Aufrufe erfordern eine strikte Kontrolle über Parametertypen. Um die Datenübertragung und-Konvertierung über das Netzwerk zu verarbeiten, erzwingt die Mittelwert Einschränkung Typeinschränkungen für Daten, die über das Netzwerk übertragen werden. Aus diesem Grund enthält die Mittel Menge eine Reihe von klar definierten [Basis Typen](base-types.md). Die Mittel Menge erzwingt eine starke Typisierung durch die Verwendung von Schlüsselwörtern, die die Größe und den Typ der Daten eindeutig definieren. Die offensichtlichste Auswirkung der starken Typisierung besteht darin, dass die Mittel l keine Variablen vom Typ " **void \***" zulässt.

In den folgenden Themen werden in diesem Abschnitt die Funktionen der mittleren Sprache erläutert, die eine starke Dateneingabe erzwingen:

-   [Basis Typen](base-types.md)
-   [Typen mit und ohne Vorzeichen](signed-and-unsigned-types.md)
-   [Breit Zeichen Typen](wide-character-types.md)
-   [Strukturen](structures.md)
-   [Unions](unions.md)
-   [Enumerierte Typen](enumerated-types.md)
-   [Arrays](arrays.md)
-   [Funktionsattribute](function-attributes.md)
-   [Feldattribute](field-attributes.md)
-   [Drei Zeiger Typen](three-pointer-types.md)
-   [Typattribute](type-attributes.md)

 

 




