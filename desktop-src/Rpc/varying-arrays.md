---
title: Variierende Arrays
description: In der mittleren l sind unterschiedliche Arrays in der Größe fester Größe. Sie ermöglichen es Clients, verschiedene Teile von Arrays von Clients an Server zu übergeben. Die Größe des Array Teils kann vom Aufruf zum Aufruf abweichen. Allerdings ist die Größe des gesamten Arrays korrigiert.
ms.assetid: 31c4bc63-de55-4937-832e-8dde9bcc47b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b2d79ee37f3e366bbf232b362306f78ca6ada4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473877"
---
# <a name="varying-arrays"></a>Variierende Arrays

In der mittleren l sind unterschiedliche Arrays in der Größe fester Größe. Sie ermöglichen es Clients, verschiedene Teile von Arrays von Clients an Server zu übergeben. Die Größe des Array Teils kann vom Aufruf zum Aufruf abweichen. Allerdings ist die Größe des gesamten Arrays korrigiert.

Das folgende Beispiel zeigt beispielsweise die Definition einer Remote Prozedur in einer Schnittstelle in einer Mittel l-Datei. Die Größe des Arrays, das der Client an den Server übergibt, wird durch die Konstante Array \_ Größe festgesetzt. Die-Schnittstelle gibt den Teil des Arrays an, den der Client in den Parametern firstelement und ChunkSize an den Server übergibt.

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(
        [in] long lFirstElement,
        [in] long lChunkSize,
        [in, first_is(lFirstElement), 
          length_is(lChunkSize)] char achArray[ARRAY_SIZE]
    );

    /* Other interface procedures are defined here. */
}
```

Die Schnittstellen Definition verwendet zuerst das Attribut "Mittel" \[ [**\_**](/windows/desktop/Midl/first-is) \] , um die Indexnummer des ersten Elements in dem Array anzugeben, das der Client an den Server übergibt. Das \[ [**length \_ is**](/windows/desktop/Midl/length-is) - \] Attribut gibt die Gesamtanzahl der Array Elemente an, die der Client übergibt. Weitere Informationen zu diesen Mittelwert Attributen finden Sie unter [Array Attribute](array-attributes.md).

Das folgende Code Fragment veranschaulicht, wie ein Client möglicherweise die in der vorhergehenden-Datei definierte Remote Prozedur aufruft.


```C++
long lFirstArrayElementNumber = 20;
long lTotalElementsPassed = 100;
char achCharArray[ARRAY_SIZE];

// Code to store chars in the array goes here.

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);

firstArrayElementNumber = 120;
totalElementsPassed = 200;

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);
```



Dieses Fragment Ruft die Remote Prozedur myremoteproc zweimal auf. Beim ersten Aufruf übergibt Sie die Array Elemente mit der Nummerierung 20 bis 119, wie durch die Werte in den Variablen firstarrayelementnumber und totalelementsp; angegeben. Beim zweiten-Befehl übergibt der Client die Array Elemente mit der Nummerierung 120 bis 319.

 

 