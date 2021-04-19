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
# <a name="sspi-handles"></a><span data-ttu-id="7ec74-103">SSPI-Handles</span><span class="sxs-lookup"><span data-stu-id="7ec74-103">SSPI Handles</span></span>

<span data-ttu-id="7ec74-104">SSPI verwendet die folgenden handle-Typen und Zeiger auf diese Handles:</span><span class="sxs-lookup"><span data-stu-id="7ec74-104">SSPI uses the following handle types and pointer to these handles:</span></span>

-   <span data-ttu-id="7ec74-105">**Sechandle** und **psechandle**</span><span class="sxs-lookup"><span data-stu-id="7ec74-105">**SecHandle** and **PSecHandle**</span></span>
-   <span data-ttu-id="7ec74-106">" **Kredhandle** " und " **pkredhandle** "</span><span class="sxs-lookup"><span data-stu-id="7ec74-106">**CredHandle** and **PCredHandle**</span></span>
-   <span data-ttu-id="7ec74-107">**Ctxthandle** und **pctxthandle**</span><span class="sxs-lookup"><span data-stu-id="7ec74-107">**CtxtHandle** and **PCtxtHandle**</span></span>

<span data-ttu-id="7ec74-108">Diese handle-Typen und Zeiger auf diese Handle-Typen werden wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="7ec74-108">These handle types and pointers to these handle types are defined as follows.</span></span>


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



 

 



