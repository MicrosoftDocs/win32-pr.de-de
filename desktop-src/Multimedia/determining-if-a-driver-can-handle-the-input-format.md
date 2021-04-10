---
title: Bestimmen, ob ein Treiber das Eingabe Format verarbeiten kann
description: Bestimmen, ob ein Treiber das Eingabe Format verarbeiten kann
ms.assetid: 456eab43-d830-4a28-b724-3ef35b852372
keywords:
- Videokomprimierungs-Manager (VCM), Eingabeformat
- VCM (Videokomprimierungs-Manager), Eingabeformat
- Icdrawquery-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b3e2da69f8c061a7d0aefe847f40113d5104d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036945"
---
# <a name="determining-if-a-driver-can-handle-the-input-format"></a><span data-ttu-id="8fe37-106">Bestimmen, ob ein Treiber das Eingabe Format verarbeiten kann</span><span class="sxs-lookup"><span data-stu-id="8fe37-106">Determining If a Driver Can Handle the Input Format</span></span>

<span data-ttu-id="8fe37-107">Im folgenden Beispiel wird gezeigt, wie das Eingabeformat mit dem [**icdrawquery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) -Makro überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="8fe37-107">The following example shows how to check the input format with the [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) macro.</span></span>


```C++
// lpbiIn points to BITMAPINFOHEADER structure indicating the input 
// format. 

if (ICDrawQuery(hIC, lpbiIn) == ICERR_OK) 
{ 
    // Driver recognizes the input format. 
} 
else 
{ 
    // Need a different decompressor. 
} 
 
```



 

 




