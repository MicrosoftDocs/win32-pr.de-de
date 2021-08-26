---
title: " in, size_is und out, size_is Prototype"
description: Der folgende Funktionsprototyp verwendet zwei gezählte Zeichenfolgen. Der Entwickler muss Code sowohl auf dem Client als auch auf dem Server schreiben, um die Längen des Zeichenarrays zu verfolgen und Parameter zu übergeben, die den Stubs mitteilen, wie viele Arrayelemente übertragen werden sollen.
ms.assetid: 334c5e0f-b1fb-41ca-8157-d92525e78b3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75075ccabe4a29ca1765a189c371c407c791cb868d2980386488879415e8f60d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073630"
---
# <a name="in-size_is-and-out-size_is-prototype"></a>\[in, size \_ is \] and \[ out, size is \_ \] Prototype

Der folgende Funktionsprototyp verwendet zwei gezählte Zeichenfolgen. Der Entwickler muss Code sowohl auf dem Client als auch auf dem Server schreiben, um die Längen des Zeichenarrays zu verfolgen und Parameter zu übergeben, die den Stubs mitteilen, wie viele Arrayelemente übertragen werden sollen.

``` syntax
void Analyze(
    [in,  length_is(cbIn), size_is(STRSIZE)]    char  achIn[],
    [in]                                        long  cbIn,
    [out, length_is(*pcbOut), size_is(STRSIZE)] char  achOut[],
    [out]                                       long *pcbOut);
```

Beachten Sie, dass die Parameter, die die Arraylänge beschreiben, in der gleichen Richtung wie die Arrays übertragen werden: *cbIn* und *bitteIn* befinden sich \[ [**in**](/windows/desktop/Midl/in) \] Parametern, während es sich bei *"ungOut"* und *"ungOut"* um \[ [**out-Parameter**](/windows/desktop/Midl/out-idl) \] handelt. Als **\[ out-Parameter \]** muss der *Parameter "ungOut"* der C-Konvention folgen und als Zeiger deklariert werden.

Der Clientcode zählt die Anzahl der Zeichen in der Zeichenfolge, einschließlich der nachfolgenden Null, bevor die Remoteprozedur wie gezeigt aufruft:

``` syntax
/* client */
char achIn[STRSIZE], achOut[STRSIZE];
long cbIn, cbOut;
...
gets_s(achIn, STRSIZE);                   // get patient input
cbIn = strlen(achIn) + 1;      // transmitted elements
Analyze(achIn, cbIn, achOut, &cbOut);
```

Die Remoteprozedur auf dem Server gibt die Länge des Rückgabepuffers in *cbOut* wie gezeigt an:

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

Das \[  \] Zeichenfolgenattribut kann verwendet werden, wenn bekannt ist, dass ein Parameter eine Zeichenfolge ist. Dieses Attribut leitet den Stub an, die Zeichenfolgengröße zu berechnen, wodurch der Mehraufwand, der der Länge zugeordnet \[ [**ist, durch Parameter beseitigt**](/windows/desktop/Midl/size-is) \] wird. Darüber hinaus wird der Stub an  die Überprüfung der NULL-Terminierung der Zeichenfolge übergeben, bevor der Parameter an die Anwendung übergeben wird.

 

 