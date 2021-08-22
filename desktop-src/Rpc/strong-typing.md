---
title: Starke Typisierung
description: C ist eine schwach typierte Sprache, d. b. der Compiler lässt Vorgänge wie die Zuweisung und den Vergleich zwischen Variablen verschiedener Typen zu.
ms.assetid: 5f52adcc-22b9-4b4f-b921-5996d278b10e
keywords:
- Rpc-Aufruf einer Remoteprozedur , beschrieben, Datentypisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae47746119f4c1b22bc066075ed484ef836fa6a68ee103e06975018a6ae49012
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924846"
---
# <a name="strong-typing"></a>Starke Typisierung

C ist eine schwach typierte Sprache, d. b. der Compiler lässt Vorgänge wie die Zuweisung und den Vergleich zwischen Variablen verschiedener Typen zu. C ermöglicht z. B. das Casten des Werts einer Variablen in einen anderen Typ. Die Möglichkeit, Variablen verschiedener Typen im gleichen Ausdruck zu verwenden, fördert Flexibilität und Effizienz.

Eine stark typierte Sprache erzwingt Einschränkungen für Vorgänge zwischen Variablen verschiedener Typen. In diesen Fällen gibt der Compiler einen Fehler aus, der den Vorgang verhindert. Diese strengen Richtlinien in Bezug auf Datentypen sind darauf ausgelegt, potenzielle Fehler zu vermeiden.

Die Schwierigkeit bei der Verwendung einer schwach typierten Sprache wie C für Remoteprozeduraufrufe ist, dass verteilte Anwendungen auf mehreren verschiedenen Computern mit unterschiedlichen C-Compilern und verschiedenen Architekturen ausgeführt werden können. Wenn eine Anwendung nur auf einem Computer ausgeführt wird, müssen Sie sich nicht um das interne Datenformat kümmern, da die Daten konsistent verarbeitet werden. In einer verteilten Computingumgebung können verschiedene Computer jedoch unterschiedliche Definitionen für ihre Basisdatentypen verwenden. Beispielsweise definieren einige Computer den **Int-Typ,** sodass seine interne Darstellung 16 Bit beträgt, während andere Computer 32 Bits verwenden. Eine Computerarchitektur, die als "Little-Endian" bezeichnet wird, weist der niedrigsten Speicheradresse das am wenigsten signifikante Byte an Daten und das wichtigste Byte der höchsten Adresse zu. Eine andere Architektur, die als "Big-Endian" bezeichnet wird, weist das am wenigsten signifikante Byte der höchsten Speicheradresse zu, die diesen Daten zugeordnet ist.

Remoteprozeduraufrufe erfordern eine strenge Kontrolle über Parametertypen. Zur Verarbeitung der Datenübertragung und -konvertierung über das Netzwerk erzwingt MIDL strikt Typeinschränkungen für Daten, die über das Netzwerk übertragen werden. Aus diesem Grund enthält MIDL einen Satz klar definierter [Basistypen.](base-types.md) MIDL erzwingt eine starke Typisierung, indem die Verwendung von Schlüsselwörtern erzwungen wird, die die Größe und den Typ der Daten eindeutig definieren. Die sichtbarste Auswirkung der starken Typisierung ist, dass MIDL keine Variablen des Typs **void zu lässt. \***

In den folgenden Themen werden in diesem Abschnitt die MIDL-Sprachfeatures erläutert, die eine starke Datentypisierung erzwingen:

-   [Basistypen](base-types.md)
-   [Signierte und nicht signierte Typen](signed-and-unsigned-types.md)
-   [Breitzeichentypen](wide-character-types.md)
-   [Strukturen](structures.md)
-   [Unions](unions.md)
-   [Aufzählte Typen](enumerated-types.md)
-   [Arrays](arrays.md)
-   [Funktionsattribute](function-attributes.md)
-   [Feldattribute](field-attributes.md)
-   [Drei Zeigertypen](three-pointer-types.md)
-   [Typattribute](type-attributes.md)

 

 




