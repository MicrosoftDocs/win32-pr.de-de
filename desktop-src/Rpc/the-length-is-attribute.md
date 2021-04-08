---
title: Das length_is-Attribut
description: Mit dem Attribut \ size \_ is \ können Sie die maximale Größe des Arrays angeben.
ms.assetid: 577a1efd-2d16-40d6-99bb-998d81ee2f8c
keywords:
- length_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f49ad63b2546d39dcc00d251f39143b7eec354c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729792"
---
# <a name="the-length_is-attribute"></a><span data-ttu-id="97692-104">Die \[ Länge \_ ist " \] Attribute".</span><span class="sxs-lookup"><span data-stu-id="97692-104">The \[length\_is\] Attribute</span></span>

<span data-ttu-id="97692-105">\[Mit dem Attribut [**Größe \_ ist**](/windows/desktop/Midl/size-is) \] Attribut können Sie die maximale Größe des Arrays angeben.</span><span class="sxs-lookup"><span data-stu-id="97692-105">The \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute lets you specify the maximum size of the array.</span></span> <span data-ttu-id="97692-106">Wenn dies das einzige Attribut ist, werden alle Elemente des Arrays übertragen.</span><span class="sxs-lookup"><span data-stu-id="97692-106">When this is the only attribute, all elements of the array are transmitted.</span></span> <span data-ttu-id="97692-107">Anstatt alle Elemente des Arrays zu senden, können Sie die übertragenen Elemente wie folgt mithilfe der \[ [**length \_**](/windows/desktop/Midl/length-is) - \] Eigenschaft angeben:</span><span class="sxs-lookup"><span data-stu-id="97692-107">Instead of sending all elements of the array, you can specify the transmitted elements using the \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute, as follows:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(3.0)
]
interface arraytest
{
  void fArray3([in] short sSize,
               [in] short sLength
               [in, out, size_is(sSize), 
                 length_is(sLength)] char achArray[*]);
}
```

<span data-ttu-id="97692-108">Größe beschreibt die Zuordnung, während length die Übertragung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="97692-108">Size describes allocation while length describes transmission.</span></span> <span data-ttu-id="97692-109">Die Anzahl der übertragenen Elemente muss immer kleiner oder gleich der Anzahl der zugewiesenen Elemente sein.</span><span class="sxs-lookup"><span data-stu-id="97692-109">The number of elements transmitted must always be less than or equal to the number of elements allocated.</span></span> <span data-ttu-id="97692-110">Der Wert für **length ist \_** immer kleiner oder gleich der **Größe \_**.</span><span class="sxs-lookup"><span data-stu-id="97692-110">The value associated with **length\_is** is always less than or equal to **size\_is**.</span></span>

 

 