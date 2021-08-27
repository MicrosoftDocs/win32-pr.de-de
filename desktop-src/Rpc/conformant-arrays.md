---
title: Konforme Arrays
description: Die Größe eines konformen Arrays kann jedes Mal variieren oder entsprechen, wenn der Client es an eine Remoteprozedur auf dem Server übergibt.
ms.assetid: b4aaec77-b7ae-495d-8666-4702017e675f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19766b7b9552bcab08a4d194629892e51d5185ed39b0bedddbaef32f08cececf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073430"
---
# <a name="conformant-arrays"></a>Konforme Arrays

Die Größe eines konformen Arrays kann jedes Mal variieren oder entsprechen, wenn der Client es an eine Remoteprozedur auf dem Server übergibt. Die Schnittstellendefinition in der MIDL-Datei der Anwendung ermöglicht es dem Client, bei jedem Aufruf der Remoteprozedur die Größe des Arrays anzugeben. Verwenden Sie leere eckige Klammern ( \[ \] ) oder ein Sternchen in den eckigen Klammern ( \[ \* \] ) in der Arraydefinition, um ein konformes Array anzugeben.

Das folgende Beispiel enthält die Definition einer Remoteprozedur in einer Schnittstelle in einer MIDL-Datei. Der Client gibt die Größe des Arrays an, das vom Parameter *arraySize* an den Server übergeben wird.

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    MyRemoteProc(
         long lArraySize,
         [size_is(lArraySize)] char achArray[*]
    );

    /* Other interface procedures are defined here. */
}
```

Die Schnittstellendefinition verwendet die MIDL-Attributgröße, um die Größe des \[ [**\_**](/windows/desktop/Midl/size-is) \] Arrays anzugeben, das der Client an den Server übergibt. Wenn Sie stattdessen den maximalen Wert der Indexnummern des Arrays angeben möchten, verwenden Sie stattdessen das \[ [**Attribut max \_ is.**](/windows/desktop/Midl/max-is) \] Weitere Informationen zu diesen MIDL-Attributen finden Sie unter [Arrayattribute.](array-attributes.md)

Das folgende Codefragment veranschaulicht, wie ein Client die in der vorherigen MIDL-Datei definierte Remoteprozedur aufrufen kann.


```C++
long lArrayLength = 20;
char achCharArray[20], achAnotherCharArray[200];

// Code to store 20 chars in achCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achCharArray);

lArrayLength = 200;

// Code to store 200 chars in achAnotherCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achAnotherCharArray);
```



Dieses Fragment ruft die Remoteprozedur MyRemoteProc zweimal auf. Beim ersten Aufruf wird ein Array von 20 Elementen übergeben. Beim zweiten Aufruf übergibt der Client ein Array von 200 Elementen.

 

 