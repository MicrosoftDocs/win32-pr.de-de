---
title: Datentypen im Schnittstellentext
description: Der Schnittstellentext, der in geschweifte Klammern () eingeschlossen ist, enthält die Datentypen, die in Remoteprozeduraufrufen und Prototypen für die Funktionen verwendet werden, die remote ausgeführt werden.
ms.assetid: a5130744-6b14-48a4-b439-16f0ecaf08c2
keywords:
- Schnittstellen MIDL , Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6691ccf89e1bff3b0e980678a30c6f706b724e4f30192d7960183c00cc00c237
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979709"
---
# <a name="data-types-in-the-interface-body"></a>Datentypen im Schnittstellentext

Der Schnittstellentext, der in geschweifte Klammern ({ }) eingeschlossen ist, enthält die Datentypen, die in Remoteprozeduraufrufen und Prototypen für die Funktionen verwendet werden, die remote ausgeführt werden. Ein Schnittstellentext kann Importe, Pragmas, konstanten Deklarationen, Typdeklarationen und Funktionsdeklarationen enthalten. Mit Ausnahme des OSF-Kompatibilitätsmodus lässt der MIDL-Compiler auch implizite Deklarationen in Form von Variablendefinitionen zu.

Beachten Sie, dass die OSF-DCE-Spezifikation für RPC-Schnittstellen nicht mehrere Schnittstellen in einer einzelnen IDL-Datei zulässt. Wenn Sie also im OSF-Kompatibilitätsmodus [**(/osf)**](-osf.md)von MIDL kompilieren, kann Ihre IDL-Datei nur eine Schnittstelle enthalten.

Ausführliche Informationen zur Verwendung des MIDL-Compilers zum Erstellen von Typbibliotheken finden Sie unter [Generieren einer Typbibliothek mit MIDL.](generating-a-type-library-with-midl-2.md)

In Microsoft RPC kann eine IDL-Datei mehrere Schnittstellen enthalten, und diese Schnittstellen können vorwärts deklariert werden (innerhalb der IDL-Datei, die sie definiert). Beispiel:

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

 

 




