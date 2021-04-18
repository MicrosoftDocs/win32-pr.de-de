---
title: Kombinieren von Array Attributen
description: Feld Attribute können in verschiedenen Kombinationen angegeben werden, solange der Stub die Informationen verwenden kann, um die Größe des Arrays und die Anzahl von Bytes zu bestimmen, die an den Server übertragen werden sollen.
ms.assetid: ff4f971f-9e46-4454-9d57-d8ebdf70b261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc60777caeb3950e37fe167fe09ecc181d88b8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337456"
---
# <a name="combining-array-attributes"></a>Kombinieren von Array Attributen

Feld Attribute können in verschiedenen Kombinationen angegeben werden, solange der Stub die Informationen verwenden kann, um die Größe des Arrays und die Anzahl von Bytes zu bestimmen, die an den Server übertragen werden sollen. Die Beziehungen zwischen den Attributen werden mithilfe der folgenden Formeln definiert:

``` syntax
size_is = max_is + 1;
length_is = last_is - first_is + 1;
```

Die den Attributen zugeordneten Werte müssen mehrere allgemeine, auf diesen Formeln basierende Regeln einhalten. Zu diesen Regeln gehören:

-   Geben Sie nicht an, dass ein \[ [**erster \_**](/windows/desktop/Midl/first-is) \] Index Wert kleiner als 0 (null) ist oder wenn ein \[ [**Letzter \_**](/windows/desktop/Midl/last-is) \] Wert größer als \[ [**Max \_ ist**](/windows/desktop/Midl/max-is) \] .
-   Geben Sie keine negative Größe für ein Array an. Definieren Sie das erste und das letzte Element, sodass Sie einen Längen Wert von 0 (null) oder größer ergeben. Definieren Sie den \[ Wert [**Max \_ ist**](/windows/desktop/Midl/max-is) \] Wert, sodass die Größe 0 (null) oder größer ist. Wenn mit der [**/Error**](/windows/desktop/Midl/-error) Bounds-Option "Mittelwert" aufgerufen wurde \_ , löst der Stub eine Ausnahme aus, wenn die Größe kleiner als 0 (null) ist, oder wenn die übertragene Länge kleiner als 0 (null) ist.
-   Verwenden Sie nicht die \[ [**Länge \_ ist**](/windows/desktop/Midl/length-is) \] und die \[ [**Last \_ sind**](/windows/desktop/Midl/last-is) \] Attribute gleichzeitig, und die \[ **Größe \_ ist** gleich \] \[ **\_** \] zeitig Attribute.

Aufgrund der Close-Beziehung zwischen Arrays und Zeigern in C können Sie mithilfe von "Mittel l" auch Arrays in Parameterlisten mithilfe der Zeiger Notation deklarieren. In der Mitte wird ein Parameter, bei dem es sich um einen Zeiger auf einen Typ handelt, als Array dieses Typs behandelt, wenn der Parameter über eines der Attribute verfügt, die häufig mit Arrays verknüpft sind.

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45)
  version(6.0) 
]
interface arraytest
{
  void fArray6([in] short sSize, 
               [in, out, size_is(sSize)] char * p1);
  void fArray7([in] short sSize, 
               [in, out, size_is(sSize)] char achArray[]);
}
```

Im vorherigen Beispiel sind die Array-und Zeiger Parameter in den Funktionen fArray6 und fArray7 Äquivalent.

 

 