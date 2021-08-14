---
title: Kombinieren von Arrayattributen
description: Feldattribute können in verschiedenen Kombinationen bereitgestellt werden, solange der Stub die Informationen verwenden kann, um die Größe des Arrays und die Anzahl von Bytes zu bestimmen, die an den Server übertragen werden sollen.
ms.assetid: ff4f971f-9e46-4454-9d57-d8ebdf70b261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd440251a658dd5b888df7275f578369419d4b8b2d4f920b263bc5095c4bd948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931753"
---
# <a name="combining-array-attributes"></a>Kombinieren von Arrayattributen

Feldattribute können in verschiedenen Kombinationen bereitgestellt werden, solange der Stub die Informationen verwenden kann, um die Größe des Arrays und die Anzahl von Bytes zu bestimmen, die an den Server übertragen werden sollen. Die Beziehungen zwischen den Attributen werden mithilfe der folgenden Formeln definiert:

``` syntax
size_is = max_is + 1;
length_is = last_is - first_is + 1;
```

Die werte, die den Attributen zugeordnet sind, müssen auf grundlage dieser Formeln mehrere Regeln des allgemeinen Sinns einhalten. Zu diesen Regeln gehören:

-   Geben Sie nicht \[ [**an, dass first \_ ein Indexwert**](/windows/desktop/Midl/first-is) kleiner als 0 (null) oder ein \] letzter \[ [**\_ wert**](/windows/desktop/Midl/last-is) \] größer als max \[ [**\_ ist.**](/windows/desktop/Midl/max-is) \]
-   Geben Sie keine negative Größe für ein Array an. Definieren Sie das erste und das letzte Element so, dass sie zu einem Längenwert von 0 (null) oder größer führen. Definieren Sie \[ [**den Wert max \_ is**](/windows/desktop/Midl/max-is) \] value, sodass die Größe 0 (null) oder größer ist. Wenn MIDL mit der Option [**/error**](/windows/desktop/Midl/-error) bounds check aufgerufen wurde, löst der Stub eine Ausnahme aus, wenn die Größe kleiner als 0 (null) oder die übertragene Länge kleiner als 0 (null) \_ ist.
-   Verwenden Sie nicht \[ [**die Attribute length \_ is**](/windows/desktop/Midl/length-is) und last is zur gleichen Zeit, und die Größe ist nicht, und last ist Attribute \] \[ [**\_**](/windows/desktop/Midl/last-is) \] \[ **\_** \] \[ **\_** \] gleichzeitig.

Aufgrund der engen Beziehung zwischen Arrays und Zeigern in C können Sie mit MIDL auch Arrays in Parameterlisten mit zeigeriger Notation deklarieren. MIDL behandelt einen Parameter, der ein Zeiger auf einen Typ ist, als Array dieses Typs, wenn der Parameter über eines der Attribute verfügt, die häufig Arrays zugeordnet sind.

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

Im vorherigen Beispiel sind die Array- und Zeigerparameter in den Funktionen fArray6 und fArray7 gleichwertig.

 

 