---
title: Konforme Arrays
description: Die Größe eines konformen Arrays kann je nachdem, wann der Client es an eine Remote Prozedur auf dem Server übergibt.
ms.assetid: b4aaec77-b7ae-495d-8666-4702017e675f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6f1491354f9cd26ef6100ab8d21f2ace3133f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039441"
---
# <a name="conformant-arrays"></a>Konforme Arrays

Die Größe eines konformen Arrays kann je nachdem, wann der Client es an eine Remote Prozedur auf dem Server übergibt. Die Schnittstellen Definition in der mittleren l-Datei der Anwendung ermöglicht es dem Client, die Größe des Arrays jedes Mal anzugeben, wenn die Remote Prozedur aufgerufen wird. Verwenden \[ \] Sie in der Array Definition leere eckige Klammern () oder ein Sternchen in den eckigen Klammern ( \[ \* \] ), um ein konformes Array anzugeben.

Das folgende Beispiel enthält die Definition einer Remote Prozedur in einer Schnittstelle in einer Mittel l-Datei. Der Client gibt die Größe des Arrays an, das durch den Parameter *arraySize* an den Server übergeben wird.

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

Die Schnittstellen Definition verwendet die mittlere Attribut \[ [**Größe \_**](/windows/desktop/Midl/size-is) \] , um die Größe des Arrays anzugeben, das der Client an den Server übergibt. Wenn Sie den maximalen Wert für die Indexnummern des Arrays angeben möchten, verwenden Sie stattdessen das \[ [**Maximum \_ is**](/windows/desktop/Midl/max-is) - \] Attribut. Weitere Informationen zu diesen Mittelwert Attributen finden Sie unter [Array Attribute](array-attributes.md).

Das folgende Code Fragment veranschaulicht, wie ein Client möglicherweise die in der vorhergehenden-Datei definierte Remote Prozedur aufruft.


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



Dieses Fragment Ruft die Remote Prozedur myremoteproc zweimal auf. Beim ersten Aufruf übergibt Sie ein Array von 20 Elementen. Beim zweiten-Befehl übergibt der Client ein Array aus 200 Elementen.

 

 