---
title: Variierende Arrays
description: In MIDL sind unterschiedliche Arrays in der Größe festgelegt. Sie ermöglichen Clients, verschiedene Teile von Arrays von Clients an Server zu übergeben. Die Größe des Arrayteils kann von Aufruf zu Aufruf variieren. Die Größe des gesamten Arrays ist jedoch festgelegt.
ms.assetid: 31c4bc63-de55-4937-832e-8dde9bcc47b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3919eed28ef7a9c888d7c23e4ebe12a1db39c97b18fa325c6daf8a4cd62d6554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010548"
---
# <a name="varying-arrays"></a>Variierende Arrays

In MIDL sind unterschiedliche Arrays in der Größe festgelegt. Sie ermöglichen Clients, verschiedene Teile von Arrays von Clients an Server zu übergeben. Die Größe des Arrayteils kann von Aufruf zu Aufruf variieren. Die Größe des gesamten Arrays ist jedoch festgelegt.

Das folgende Beispiel zeigt beispielsweise die Definition einer Remoteprozedur in einer Schnittstelle in einer MIDL-Datei. Die Größe des Arrays, das der Client an den Server übergibt, wird durch die Konstante ARRAY \_ SIZE festgelegt. Die -Schnittstelle gibt den Teil des Arrays an, den der Client in den Parametern firstElement und chunkSize an den Server übergibt.

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

Die Schnittstellendefinition verwendet zuerst das MIDL-Attribut, \[ [**\_**](/windows/desktop/Midl/first-is) um \] die Indexnummer des ersten Elements im Teil des Arrays anzugeben, das der Client an den Server übergibt. Das \[ [**length \_ is-Attribut**](/windows/desktop/Midl/length-is) \] gibt die Gesamtzahl der Arrayelemente an, die der Client übergibt. Weitere Informationen zu diesen MIDL-Attributen finden Sie unter [Arrayattribute.](array-attributes.md)

Das folgende Codefragment veranschaulicht, wie ein Client die in der vorherigen MIDL-Datei definierte Remoteprozedur aufrufen kann.


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



Dieses Fragment ruft die Remoteprozedur MyRemoteProc zweimal auf. Beim ersten Aufruf werden die Arrayelemente mit der Nummer 20 bis 119 übergeben, wie durch die Werte in den Variablen firstArrayElementNumber und totalElementsPassed angegeben. Beim zweiten Aufruf übergibt der Client die Arrayelemente mit der Nummer 120 bis 319.

 

 