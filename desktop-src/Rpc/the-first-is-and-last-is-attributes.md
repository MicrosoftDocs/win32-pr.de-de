---
title: Die first_is und last_is Attribute
description: Sie können die Anzahl der übertragenen Elemente ermitteln, indem Sie das erste und das letzte Element angeben.
ms.assetid: bd4dcf42-64a7-4b05-ac55-be77c381eb2e
keywords:
- first_is
- last_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16c30c2e7e6689ba2a61f7f5e694a5b29f39af5cadcf7fa2ca2f51e14e1f3457
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017140"
---
# <a name="the-first_is-and-last_is-attributes"></a>Der \[ erste ist , und der letzte ist \_ \] \[ \_ \] Attribute.

Sie können die Anzahl der übertragenen Elemente ermitteln, indem Sie das erste und das letzte Element angeben. Verwenden Sie \[ [**die Attribute \_ "first**](/windows/desktop/Midl/first-is) \] \[ is" und [**\_ "last is",**](/windows/desktop/Midl/last-is) \] wie gezeigt:

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

 

 