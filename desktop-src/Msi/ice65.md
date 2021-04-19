---
description: ICE65 prüft, ob die Umgebungs Tabelle Ungültige Präfix-oder anfügewerte enthält.
ms.assetid: 95d4e618-9a19-40db-910a-daab105559ae
title: ICE65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3d2b7bcd844c970ccc7fddf376b27c2ec54f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373275"
---
# <a name="ice65"></a>ICE65

ICE65 prüft, ob die [Umgebungs Tabelle](environment-table.md) Ungültige Präfix-oder anfügewerte enthält.

Wenn eine Warnung oder ein Fehler, der von ICE65 gemeldet wird, nicht behoben wird, führt dies im Allgemeinen zu Problemen beim Installieren, deinstallieren oder Reparieren der Umgebungsvariablen. Beispielsweise können nur einige Werte einer bestimmten Variablen entfernt werden, wenn mindestens einer der Werte für diese Variable ein nachfolgendes Trennzeichen hat.

## <a name="result"></a>Ergebnis

ICE65 gibt eine Warnung oder einen Fehler aus, wenn die Umgebungs Tabelle Ungültige Präfix-oder anfügewerte aufweist.

## <a name="example"></a>Beispiel

ICE65 meldet den folgenden Fehler und die Warnung für das gezeigte Beispiel.

``` syntax
The environment variable 'Var3' has a separator beginning or ending its value.
```

Der nachfolgende NULL am Ende des Werts ( \[ ~ \] ) markiert diesen Wert, der einem vorhandenen Wert vorangestellt werden soll. Das Zeichen unmittelbar vor dem NULL-Zeichen (ein Semikolon) wird das Trennzeichen für diesen Wert. Dieser Wert enthält auch ein Semikolon am Anfang der Zeichenfolge.

Um diesen Fehler zu beheben, löschen Sie einfach das vorangehende Semikolon.

``` syntax
WARNING: The environment variable 'Var2' has an alphanumeric separator
```

Der führende Null-Wert im-Wert ( \[ ~ \] ) markiert diesen Wert, der an einen beliebigen vorhandenen Wert angehängt werden soll. Das Zeichen direkt nach dem NULL-Wert wird das Trennzeichen für diesen Wert. In diesem Fall handelt es sich bei diesem Zeichen um den Buchstaben "e", der auch in der Mitte der anzufügenden Zeichenfolge vorkommt. Diese Bedingung (mit einem Trennzeichen, das mit einem Zeichen innerhalb der anzufügenden Zeichenfolge identisch ist) kann zu unvorhersehbaren Ergebnissen führen.

Der Buchstabe "e", bei dem es sich um einen gemeinsamen Buchstaben handelt, wird wahrscheinlich im Wert gefunden. Eine bessere Wahl wäre ";" oder ein anderes nicht alphanumerisches Zeichen. (Wenn der Wert jedoch ein Pfad ist, sind ":" und " \\ " und "." riskante Entscheidungen.)

Um diese Warnung zu beheben, verwenden Sie ein anderes Trennzeichen.

[Umgebungs Tabelle](environment-table.md)



| Komponente | Verzeichnis | Attribute         | KEYPATH       |
|-----------|-----------|--------------------|---------------|
| Var1      | TestVar   | \[~\]; Appendthis   | Testcomponent |
| Var2      | TestVar   | \[~\]eappendthis   | Testcomponent |
| Var3      | TestVar   | ; Prepdthis;\[~\] | Testcomponent |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



