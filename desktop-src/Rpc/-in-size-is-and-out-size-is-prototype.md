---
title: " in, size_is und Out, size_is Prototyp"
description: Der folgende Funktionsprototyp verwendet zwei gezählte Zeichen folgen. Der Entwickler muss Code sowohl auf dem Client als auch auf dem Server schreiben, um die Zeichen Array Längen und Pass Parameter zu verfolgen, die die stubwerte angeben, wie viele Array Elemente übertragen werden sollen.
ms.assetid: 334c5e0f-b1fb-41ca-8157-d92525e78b3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d03dbb4dd65d44122bea7ff086013295e0bf616d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390896"
---
# <a name="in-size_is-and-out-size_is-prototype"></a>\[in, Größe \_ ist \] und ausgehend \[ , Größe \_ ist \] Prototyp

Der folgende Funktionsprototyp verwendet zwei gezählte Zeichen folgen. Der Entwickler muss Code sowohl auf dem Client als auch auf dem Server schreiben, um die Zeichen Array Längen und Pass Parameter zu verfolgen, die die stubwerte angeben, wie viele Array Elemente übertragen werden sollen.

``` syntax
void Analyze(
    [in,  length_is(cbIn), size_is(STRSIZE)]    char  achIn[],
    [in]                                        long  cbIn,
    [out, length_is(*pcbOut), size_is(STRSIZE)] char  achOut[],
    [out]                                       long *pcbOut);
```

Beachten Sie, dass die Parameter, die die Array Länge beschreiben, in der gleichen Richtung wie die Arrays übertragen werden: *cbin* und *Achin* sind \[ [](/windows/desktop/Midl/in) \] Parameter, während *PCBout* und *achout* \[ [](/windows/desktop/Midl/out-idl) \] Parameter sind. Als **\[ out \]** -Parameter muss der Parameter *PCBout* der C-Konvention folgen und als Zeiger deklariert werden.

Der Client Code zählt die Anzahl der Zeichen in der Zeichenfolge, einschließlich der nachfolgenden NULL, vor dem Aufrufen der Remote Prozedur, wie hier gezeigt:

``` syntax
/* client */
char achIn[STRSIZE], achOut[STRSIZE];
long cbIn, cbOut;
...
gets_s(achIn, STRSIZE);                   // get patient input
cbIn = strlen(achIn) + 1;      // transmitted elements
Analyze(achIn, cbIn, achOut, &cbOut);
```

Die Remote Prozedur auf dem Server liefert die Länge des Rückgabe Puffers in *cbout* , wie hier gezeigt:

``` syntax
/* server */
void Analyze(char *pchIn,
             long cbIn,
             char *pchOut,
             long *pcbOut)
{
   ...
   *pcbOut = strlen(pchOut) + 1; // transmitted elements
   return;
}
```

Das \[ **String** - \] Attribut kann verwendet werden, wenn ein Parameter bekanntermaßen eine Zeichenfolge ist. Dieses Attribut weist den Stub an, die Zeichen folgen Größe zu berechnen. Dadurch entfällt der Aufwand, der der \[ [**Länge der Länge**](/windows/desktop/Midl/size-is) von \] Parametern zugeordnet ist. Außerdem wird der Stub angewiesen, zu überprüfen, ob die Zeichenfolge **null** endet, bevor der Parameter an die Anwendung übergeben wird.

 

 