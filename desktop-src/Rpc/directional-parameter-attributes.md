---
title: Direktionale Attribute (Parameter)
description: Direktionale Attribute beschreiben, ob die Daten vom Client an den Server, den Server an den Client oder beides übertragen werden.
ms.assetid: 1e4f92ae-2d98-412f-a693-54bb09ae4674
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, direktionale Attribute
- in
- out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec37dbf65919f5aae9e7674cf7102eddcdf5170
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101990"
---
# <a name="directional-parameter-attributes"></a>Direktionale Attribute (Parameter)

Direktionale Attribute beschreiben, ob die Daten vom Client an den Server, den Server an den Client oder beides übertragen werden. Alle Parameter im Funktionsprototyp müssen direktionalen Attributen zugeordnet werden. Die drei möglichen Kombinationen von direktionalen Attributen lauten: 1) \[ [**in**](/windows/desktop/Midl/in) \] , 2) ausgehend \[ [](/windows/desktop/Midl/out-idl) \] und 3) \[ **in**, **out** \] . Diese beschreiben, wie Parameter zwischen aufrufenden und aufgerufenen Prozeduren übermittelt werden. Wenn Sie im Standardmodus (Microsoft-erweiterter Modus) kompilieren und ein direktionales Attribut für einen Parameter weglassen, nimmt der Mittelwert Compiler den Standardwert \[ **in an** \] .

Ein \[ [**out**](/windows/desktop/Midl/out-idl) - \] Parameter muss ein Zeiger sein. Tatsächlich ist das \[ **out** - \] Attribut nicht sinnvoll, wenn es auf Parameter angewendet wird, die nicht als Zeiger fungieren, da C-Funktionsparameter als Wert übermittelt werden. In C empfängt die aufgerufene Funktion eine private Kopie des Parameter Werts. der Wert der aufrufenden Funktion für diesen Parameter kann nicht geändert werden. Wenn der Parameter jedoch als Zeiger fungiert, kann er verwendet werden, um auf den Speicher zuzugreifen und ihn zu ändern. Das \[ **out** \] -Attribut gibt an, dass die Server Funktion den Wert an die aufrufende Funktion des Clients zurückgeben soll und dass der dem Zeiger zugeordnete Arbeitsspeicher in Übereinstimmung mit den Attributen zurückgegeben werden soll, die dem Zeiger zugewiesen sind.

Die folgende Schnittstelle veranschaulicht die drei möglichen Kombinationen direktionaler Attribute, die auf einen Parameter angewendet werden können. Die **inoutproc** -Funktion ist in der IDL-Datei wie folgt definiert:

``` syntax
void InOutProc ([in]       short     s1,
                [in, out]  short *  ps2,
                [out]      float *  pf3);
```

Der erste Parameter ( *S1*) ist \[ nur [**in**](/windows/desktop/Midl/in) \] . Der Wert wird an den Remote Computer übertragen, aber nicht an die aufrufenden Prozeduren zurückgegeben. Obwohl die Serveranwendung ihren Wert für *S1* ändern kann, ist der Wert von *S1* auf dem Client vor und nach dem-Befehl identisch.

Der zweite Parameter, " *PS2*", wird im Funktionsprototyp als Zeiger mit den Attributen " \[ [**in**](/windows/desktop/Midl/in) " \] und " \[ [**out**](/windows/desktop/Midl/out-idl) " definiert \] . Das \[ **in** - \] Attribut gibt an, dass der Wert des-Parameters vom Client an den Server übergeben wird. Das \[ **out** - \] Attribut gibt an, dass der Wert, auf den von *PS2* verwiesen wird, dem Client zurückgegeben wird.

Der dritte Parameter ist \[ nur [**out**](/windows/desktop/Midl/out-idl) \] . Für den Parameter auf dem Server ist Speicherplatz zugeordnet, aber der Wert ist beim Eintrag nicht definiert. Wie bereits erwähnt, müssen alle \[ **out** - \] Parameter Zeiger sein.

Die Remote Prozedur ändert den Wert aller drei Parameter, aber nur die neuen Werte der \[ [](/windows/desktop/Midl/out-idl) \] Parameter out und \[ [**in**](/windows/desktop/Midl/in) stehen \] dem Client zur Verfügung.


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



Bei der Rückgabe des Aufrufes **inoutproc** werden der zweite und der dritte Parameter geändert. Der erste Parameter, der nur \[ [**in**](/windows/desktop/Midl/in) ist \] , ist unverändert.

![in-Parameter](images/prog-a22.png)

![out-Parameter](images/prog-a23.png)

![in-out-Parameter](images/prog-a21.png)

 

 