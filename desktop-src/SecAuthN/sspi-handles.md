---
description: Listet die von der SSPI-API verwendeten Handles auf.
ms.assetid: 94b622d0-7c04-4513-841f-0df9b5d49136
title: SSPI-Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e388633cfee0d0f0470e519bac124a0bd1c70fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359447"
---
# <a name="sspi-handles"></a>SSPI-Handles

SSPI verwendet die folgenden handle-Typen und Zeiger auf diese Handles:

-   **Sechandle** und **psechandle**
-   " **Kredhandle** " und " **pkredhandle** "
-   **Ctxthandle** und **pctxthandle**

Diese handle-Typen und Zeiger auf diese Handle-Typen werden wie folgt definiert.


```C++
typedef struct _SecHandle {
  ULONG_PTR       dwLower;
  ULONG_PTR       dwUpper;
} SecHandle, * PSecHandle;

typedef SecHandle    CredHandle;
typedef PSecHandle   PCredHandle;

typedef SecHandle    CtxtHandle;
typedef PSecHandle   PCtxtHandle;
```



 

 



