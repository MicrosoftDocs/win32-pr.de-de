---
title: Das length_is Attribut
description: Mit dem Attribut \_ \size is\ können Sie die maximale Größe des Arrays angeben.
ms.assetid: 577a1efd-2d16-40d6-99bb-998d81ee2f8c
keywords:
- length_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436559961d815adb417d83de5ffa8c06d8497fa0899644411d252c84d6e34ea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924259"
---
# <a name="the-length_is-attribute"></a>Die \[ Länge \_ ist \] "Attribute".

Mit \[ [**dem Attribut size \_ is**](/windows/desktop/Midl/size-is) \] können Sie die maximale Größe des Arrays angeben. Wenn dies das einzige Attribut ist, werden alle Elemente des Arrays übertragen. Anstatt alle Elemente des Arrays zu senden, können Sie die übertragenen Elemente wie folgt mithilfe des \[ [**length \_ is-Attributs**](/windows/desktop/Midl/length-is) \] angeben:

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

Größe beschreibt die Zuordnung, während die Länge die Übertragung beschreibt. Die Anzahl der übertragenen Elemente muss immer kleiner oder gleich der Anzahl der zugeordneten Elemente sein. Der wert, der **der Länge zugeordnet \_ ist,** ist immer kleiner oder gleich **der \_ Größe**.

 

 