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
# <a name="combining-array-attributes"></a><span data-ttu-id="038b1-103">Kombinieren von Array Attributen</span><span class="sxs-lookup"><span data-stu-id="038b1-103">Combining Array Attributes</span></span>

<span data-ttu-id="038b1-104">Feld Attribute können in verschiedenen Kombinationen angegeben werden, solange der Stub die Informationen verwenden kann, um die Größe des Arrays und die Anzahl von Bytes zu bestimmen, die an den Server übertragen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="038b1-104">Field attributes can be supplied in various combinations as long as the stub can use the information to determine the size of the array and the number of bytes to transmit to the server.</span></span> <span data-ttu-id="038b1-105">Die Beziehungen zwischen den Attributen werden mithilfe der folgenden Formeln definiert:</span><span class="sxs-lookup"><span data-stu-id="038b1-105">The relationships between the attributes are defined using the following formulas:</span></span>

``` syntax
size_is = max_is + 1;
length_is = last_is - first_is + 1;
```

<span data-ttu-id="038b1-106">Die den Attributen zugeordneten Werte müssen mehrere allgemeine, auf diesen Formeln basierende Regeln einhalten.</span><span class="sxs-lookup"><span data-stu-id="038b1-106">The values associated with the attributes must obey several common-sense rules based on those formulas.</span></span> <span data-ttu-id="038b1-107">Zu diesen Regeln gehören:</span><span class="sxs-lookup"><span data-stu-id="038b1-107">These rules are:</span></span>

-   <span data-ttu-id="038b1-108">Geben Sie nicht an, dass ein \[ [**erster \_**](/windows/desktop/Midl/first-is) \] Index Wert kleiner als 0 (null) ist oder wenn ein \[ [**Letzter \_**](/windows/desktop/Midl/last-is) \] Wert größer als \[ [**Max \_ ist**](/windows/desktop/Midl/max-is) \] .</span><span class="sxs-lookup"><span data-stu-id="038b1-108">Do not specify a \[[**first\_is**](/windows/desktop/Midl/first-is)\] index value smaller than zero or a \[[**last\_is**](/windows/desktop/Midl/last-is)\] value greater than \[[**max\_is**](/windows/desktop/Midl/max-is)\].</span></span>
-   <span data-ttu-id="038b1-109">Geben Sie keine negative Größe für ein Array an.</span><span class="sxs-lookup"><span data-stu-id="038b1-109">Do not specify a negative size for an array.</span></span> <span data-ttu-id="038b1-110">Definieren Sie das erste und das letzte Element, sodass Sie einen Längen Wert von 0 (null) oder größer ergeben.</span><span class="sxs-lookup"><span data-stu-id="038b1-110">Define the first and last elements so that they result in a length value of zero or greater.</span></span> <span data-ttu-id="038b1-111">Definieren Sie den \[ Wert [**Max \_ ist**](/windows/desktop/Midl/max-is) \] Wert, sodass die Größe 0 (null) oder größer ist.</span><span class="sxs-lookup"><span data-stu-id="038b1-111">Define the \[[**max\_is**](/windows/desktop/Midl/max-is)\] value so that the size is zero or greater.</span></span> <span data-ttu-id="038b1-112">Wenn mit der [**/Error**](/windows/desktop/Midl/-error) Bounds-Option "Mittelwert" aufgerufen wurde \_ , löst der Stub eine Ausnahme aus, wenn die Größe kleiner als 0 (null) ist, oder wenn die übertragene Länge kleiner als 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="038b1-112">If MIDL was invoked with the [**/error**](/windows/desktop/Midl/-error) bounds\_check option, then the stub raises an exception when the size is less than zero, or the transmitted length is less than zero.</span></span>
-   <span data-ttu-id="038b1-113">Verwenden Sie nicht die \[ [**Länge \_ ist**](/windows/desktop/Midl/length-is) \] und die \[ [**Last \_ sind**](/windows/desktop/Midl/last-is) \] Attribute gleichzeitig, und die \[ **Größe \_ ist** gleich \] \[ **\_** \] zeitig Attribute.</span><span class="sxs-lookup"><span data-stu-id="038b1-113">Do not use the \[[**length\_is**](/windows/desktop/Midl/length-is)\] and \[[**last\_is**](/windows/desktop/Midl/last-is)\] attributes at the same time, nor the \[**size\_is**\] and \[**last\_is**\] attributes at the same time.</span></span>

<span data-ttu-id="038b1-114">Aufgrund der Close-Beziehung zwischen Arrays und Zeigern in C können Sie mithilfe von "Mittel l" auch Arrays in Parameterlisten mithilfe der Zeiger Notation deklarieren.</span><span class="sxs-lookup"><span data-stu-id="038b1-114">Because of the close relationship in C between arrays and pointers, MIDL also lets you declare arrays in parameter lists using pointer notation.</span></span> <span data-ttu-id="038b1-115">In der Mitte wird ein Parameter, bei dem es sich um einen Zeiger auf einen Typ handelt, als Array dieses Typs behandelt, wenn der Parameter über eines der Attribute verfügt, die häufig mit Arrays verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="038b1-115">MIDL treats a parameter that is a pointer to a type as an array of that type if the parameter has any of the attributes commonly associated with arrays.</span></span>

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

<span data-ttu-id="038b1-116">Im vorherigen Beispiel sind die Array-und Zeiger Parameter in den Funktionen fArray6 und fArray7 Äquivalent.</span><span class="sxs-lookup"><span data-stu-id="038b1-116">In the preceding example, the array and pointer parameters in the functions fArray6 and fArray7 are equivalent.</span></span>

 

 