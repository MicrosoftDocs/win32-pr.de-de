---
title: Datentypen im Schnittstellen Text
description: Der Schnittstellen Text, der in geschweiften Klammern () eingeschlossen ist, enthält die Datentypen, die in Remote Prozedur aufrufen und Prototypen für die Funktionen verwendet werden, die Remote ausgeführt werden.
ms.assetid: a5130744-6b14-48a4-b439-16f0ecaf08c2
keywords:
- Schnittstellen-Mittell, Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bdbbb90c4cbecd4a6a4e3cc74ba9775772dd0a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339196"
---
# <a name="data-types-in-the-interface-body"></a>Datentypen im Schnittstellen Text

Der Schnittstellen Text, der in geschweiften Klammern ({}) eingeschlossen ist, enthält die Datentypen, die in Remote Prozedur aufrufen und Prototypen für die Funktionen verwendet werden, die Remote ausgeführt werden. Ein Schnittstellen Text kann Importe, Pragmas, Konstante Deklarationen, Typdeklarationen und Funktions Deklarationen enthalten. Mit Ausnahme des OSF-Kompatibilitätsmodus lässt der Mittelwert Compiler auch implizite Deklarationen in Form von Variablen Definitionen zu.

Beachten Sie, dass die OSF-DCE-Spezifikation für RPC-Schnittstellen nicht mehrere Schnittstellen in einer einzelnen IDL-Datei zulässt. Wenn Sie also im OSF-Kompatibilitätsmodus ( [**/OSF**](-osf.md)) von mittlerer l kompilieren, kann die IDL-Datei nur eine Schnittstelle enthalten.

Ausführliche Informationen zur Verwendung des-Mittell-Compilers zum Erstellen von Typbibliotheken finden Sie unter Erstellen [einer Typbibliothek mit mittlerer l](generating-a-type-library-with-midl-2.md).

In Microsoft RPC kann eine IDL-Datei mehrere Schnittstellen enthalten, und diese Schnittstellen können vorwärts (innerhalb der IDL-Datei, die Sie definiert) als deklariert werden. Beispiel:

``` syntax
interface ITwo; //forward declaration
interface IOne 
{
...uses ITwo...
}
interface ITwo 
{
...uses IOne...
}
```

 

 




