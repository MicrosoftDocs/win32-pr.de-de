---
title: " in, out, Zeichen folgen Prototyp"
description: Der folgende Funktionsprototyp verwendet einen einzelnen \ in-, out-, String \-Parameter für die Eingabe-und Ausgabe Zeichenfolgen.
ms.assetid: 5a652b79-11ca-4780-aac1-60a22f96b4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed8ed47c02ea3e08672d529bf7ce9f627925518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948846"
---
# <a name="in-out-string-prototype"></a>\[in, out, Zeichen folgen \] Prototyp

Der folgende Funktionsprototyp verwendet einen einzelnen \[ [**in**](/windows/desktop/Midl/in)-, [**out**](/windows/desktop/Midl/out-idl)-und Zeichen folgen Parameter für die Eingabe-und Ausgabe [**Zeichenfolgen**](/windows/desktop/Midl/string) \] . Die Zeichenfolge enthält zunächst Patienten Eingaben und wird dann mit der Antwort des Arztes überschrieben, wie im folgenden gezeigt:

``` syntax
void Analyze([in, out, string, size_is(STRSIZE)] char  achInOut[]);
```

Dieses Beispiel ähnelt dem Beispiel, in dem eine Zeichenfolge mit einem Zeichen sowohl für die Eingabe als auch für die Ausgabe verwendet wurde. Wie bei diesem Beispiel bestimmt die \[ [**Größe \_**](/windows/desktop/Midl/size-is) " \] Attribute" die Anzahl der Elemente, die auf dem Server zugeordnet sind. Das \[ [**String**](/windows/desktop/Midl/string) - \] Attribut weist den Stub an, " **strinlen** " aufzurufen, um die Anzahl der übertragenen Elemente zu bestimmen.

Der Client ordnet den gesamten Arbeitsspeicher vor dem-Rückruf zu:

``` syntax
/* client */
char achInOut[STRSIZE];
...
gets_s(achInOut, STRSIZE);            // get patient input
Analyze(achInOut);
printf("%s\n", achInOut);  // display doctor response
```

Beachten Sie, dass die Funktion analysieren nicht mehr die Länge der Rückgabe Zeichenfolge berechnen muss, wie dies im Beispiel für eine gezählte Zeichenfolge geschehen ist, in dem das **\[ Zeichen \]** folgen Attribut nicht verwendet wurde. Die stubzeichen berechnen nun die Länge wie gezeigt:

``` syntax
/* server */
void Analyze(char *pchInOut)
{
   ...
   Respond(response, pchInOut); // don't need to call strlen
   return;                      // stubs handle size
}
```

 

 