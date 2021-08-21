---
title: Direktionale Attribute (Parameter)
description: Direktionale Attribute beschreiben, ob die Daten vom Client zum Server, vom Server zum Client oder von beiden übertragen werden.
ms.assetid: 1e4f92ae-2d98-412f-a693-54bb09ae4674
keywords:
- Rpc-Aufruf einer Remoteprozedur , beschrieben, direktionale Attribute
- in
- out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e08e9ff23e7e12acbd5cf301afe6786599268d2e149878a326a62f79cd91f7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930645"
---
# <a name="directional-parameter-attributes"></a>Direktionale Attribute (Parameter)

Direktionale Attribute beschreiben, ob die Daten vom Client zum Server, vom Server zum Client oder von beiden übertragen werden. Alle Parameter im Funktionsprototyp müssen direktionalen Attributen zugeordnet werden. Die drei möglichen Kombinationen von direktionalen Attributen sind: 1) \[ [**in**](/windows/desktop/Midl/in) \] , 2) \[ [**out**](/windows/desktop/Midl/out-idl) \] und 3) \[ **in**, **out** \] . Diese beschreiben die Art und Weise, wie Parameter zwischen aufrufenden und aufgerufenen Prozeduren übergeben werden. Wenn Sie im Standardmodus (erweiterter Microsoft-Modus) kompilieren und ein richtungsbasiertes Attribut für einen Parameter weglassen, geht der MIDL-Compiler von einem Standardwert \[ **in aus.** \]

Ein \[ [](/windows/desktop/Midl/out-idl) \] out-Parameter muss ein Zeiger sein. Tatsächlich ist das out-Attribut nicht sinnvoll, wenn es auf Parameter angewendet wird, die nicht als Zeiger fungieren, da C-Funktionsparameter \[  \] als Wert übergeben werden. In C empfängt die aufgerufene Funktion eine private Kopie des Parameterwerts. Sie kann den Wert der aufrufenden Funktion für diesen Parameter nicht ändern. Wenn der Parameter jedoch als Zeiger fungiert, kann er verwendet werden, um auf den Arbeitsspeicher zu zugreifen und ihn zu ändern. Das \[ **out-Attribut** gibt an, dass die Serverfunktion den Wert an die aufrufende Funktion des Clients zurückgeben soll und dass der dem Zeiger zugeordnete Arbeitsspeicher in Übereinstimmung mit den Attributen zurückgegeben werden soll, die dem Zeiger zugewiesen \] sind.

Die folgende Schnittstelle veranschaulicht die drei möglichen Kombinationen von direktionalen Attributen, die auf einen Parameter angewendet werden können. Die **Funktion InOutProc** ist in der IDL-Datei wie die folgenden definiert:

``` syntax
void InOutProc ([in]       short     s1,
                [in, out]  short *  ps2,
                [out]      float *  pf3);
```

Der erste Parameter, *s1,* ist \[ [**nur in**](/windows/desktop/Midl/in) \] . Der Wert wird an den Remotecomputer übertragen, aber nicht an die aufrufende Prozedur zurückgegeben. Obwohl die Serveranwendung ihren Wert für *s1* ändern kann, ist der Wert von *s1* auf dem Client vor und nach dem Aufruf identisch.

Der zweite Parameter *ps2* wird im Funktionsprototyp als Zeiger mit in- und \[ [](/windows/desktop/Midl/in) \] \[ [**out-Attributen**](/windows/desktop/Midl/out-idl) \] definiert. Das \[ **attribut in** \] gibt an, dass der Wert des Parameters vom Client an den Server übergeben wird. Das \[ **out-Attribut** gibt an, dass der Wert, auf den \] *ps2* verweist, an den Client zurückgegeben wird.

Der dritte Parameter ist \[ [**nur out.**](/windows/desktop/Midl/out-idl) \] Für den Parameter auf dem Server wird Speicherplatz zugeordnet, aber der Wert ist beim Eintrag nicht definiert. Wie bereits erwähnt, müssen \[ **alle** \] out-Parameter Zeiger sein.

Die Remoteprozedur ändert den Wert aller drei Parameter, aber nur die neuen Werte der Out- und \[ [](/windows/desktop/Midl/out-idl) \] \[ [**in-Parameter**](/windows/desktop/Midl/in) \] sind für den Client verfügbar.


```C++
#define MAX 257

void InOutProc(short    s1,
               short * ps2,
               float * pf3)
{
    *pf3 = (float) s1 / (float) *ps2;
    *ps2 = (short) MAX - s1;
    s1++;  // in only; not changed on the client side
    return;
}
```



Bei rückgabe des Aufrufs von **InOutProc** werden der zweite und der dritte Parameter geändert. Der erste Parameter, der \[ [**sich nur in**](/windows/desktop/Midl/in) \] befindet, ist unverändert.

![in Parametern](images/prog-a22.png)

![out-Parameter](images/prog-a23.png)

![In-Out-Parameter](images/prog-a21.png)

 

 