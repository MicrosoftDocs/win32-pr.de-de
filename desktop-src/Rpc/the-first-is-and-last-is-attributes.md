---
title: Die First_is-und Last_is Attribute
description: Sie können die Anzahl der übertragenen Elemente ermitteln, indem Sie das erste und das letzte Element angeben.
ms.assetid: bd4dcf42-64a7-4b05-ac55-be77c381eb2e
keywords:
- first_is
- last_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159a2696db8e175f921b797176baaa8f3aa0263c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316316"
---
# <a name="the-first_is-and-last_is-attributes"></a>Das \[ erste \_ \] Attribut ist und das \[ Letzte \_ \] Attribut.

Sie können die Anzahl der übertragenen Elemente ermitteln, indem Sie das erste und das letzte Element angeben. Verwenden Sie die \[ Attribute [**First \_ is**](/windows/desktop/Midl/first-is) \] und \[ [**Last \_ is**](/windows/desktop/Midl/last-is) ( \] wie gezeigt):

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(4.0)
]
interface arraytest
{

  void fArray4([in]               short sSize,
               [in]               short sLast,
               [in]               short sFirst,
               [in, 
                out,
                size_is(sSize),
                first_is(sFirst),
                last_is(sLast)]   char achArray[]) ;
}
```

 

 