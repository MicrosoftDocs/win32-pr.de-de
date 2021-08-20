---
description: ICE65 überprüft, ob die Tabelle Environment keine ungültigen Präfix- oder Anfügewerte enthält.
ms.assetid: 95d4e618-9a19-40db-910a-daab105559ae
title: ICE65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 543c75f3abe6cb44a405f41bcb788dc71adf85ae954f013244bfc1cded4e6d27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946587"
---
# <a name="ice65"></a>ICE65

ICE65 überprüft, ob die [Tabelle Environment](environment-table.md) keine ungültigen Präfix- oder Anfügewerte enthält.

Wenn eine von ICE65 gemeldete Warnung oder ein Fehler nicht behoben wird, führt dies im Allgemeinen zu Problemen bei der Installation, Deinstallation oder Reparatur der Umgebungsvariablen. Beispielsweise können nur einige Werte einer bestimmten Variablen entfernt werden, wenn mindestens einer der Werte für diese Variable ein nachgestelltes Trennzeichen hat.

## <a name="result"></a>Ergebnis

ICE65 gibt eine Warnung oder einen Fehler aus, wenn die Umgebungstabelle ungültige Präfix- oder Anfügewerte aufweist.

## <a name="example"></a>Beispiel

ICE65 meldet den folgenden Fehler und die folgende Warnung für das gezeigte Beispiel.

``` syntax
The environment variable 'Var3' has a separator beginning or ending its value.
```

Der nachfolgende NULL-Wert am Ende des Werts ( ) markiert diesen Wert, der \[ ~ \] einem vorhandenen Wert vorangestellt wird. Das Zeichen unmittelbar vor dem NULL-Wert (ein Semikolon) wird zum Trennzeichen für diesen Wert. Dieser Wert weist am Anfang der Zeichenfolge ebenfalls ein Semikolon auf.

Um diesen Fehler zu beheben, löschen Sie einfach das führende Semikolon.

``` syntax
WARNING: The environment variable 'Var2' has an alphanumeric separator
```

Der führende NULL-Wert im Wert ( \[ ~ \] ) markiert diesen Wert, der an einen vorhandenen Wert angefügt werden soll. Das Zeichen unmittelbar nach dem NULL-Wert wird zum Trennzeichen für diesen Wert. In diesem Fall ist dieses Zeichen der Buchstabe "e", der auch in der Mitte der anzufügenden Zeichenfolge vorkommt. Diese Bedingung (mit einem Trennzeichen, das mit einem Zeichen innerhalb der anzufügenden Zeichenfolge identisch ist) kann zu unvorhersehbaren Ergebnissen führen.

Der Buchstabe "e" ist ein allgemeiner Buchstabe und befindet sich wahrscheinlich im -Wert. Eine bessere Wahl wäre ";" oder ein anderes nicht alphanumerisches Zeichen. (Wenn der Wert jedoch ein Pfad ist, sind ":" und \\ "" und "." riskante Optionen.)

Verwenden Sie ein anderes Trennzeichen, um diese Warnung zu beheben.

[Umgebungstabelle](environment-table.md)



| Komponente | Verzeichnis | Attribute         | KeyPath       |
|-----------|-----------|--------------------|---------------|
| Var1      | TestVar   | \[~\]; AppendThis   | TestComponent |
| Var2      | TestVar   | \[~\]eAppendThis   | TestComponent |
| Var3      | TestVar   | ; PrependThis;\[~\] | TestComponent |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



