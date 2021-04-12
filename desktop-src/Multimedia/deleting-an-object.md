---
title: Löschen eines Objekts
description: Löschen eines Objekts
ms.assetid: 54ea1e7d-75b5-461f-b0d6-a976c33d66fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f77ad42700e01e5594faa5b8bb299fcc5841d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471404"
---
# <a name="deleting-an-object"></a><span data-ttu-id="38804-103">Löschen eines Objekts</span><span class="sxs-lookup"><span data-stu-id="38804-103">Deleting an Object</span></span>

<span data-ttu-id="38804-104">Die **releasemethode** löscht das-Objekt, wenn der Verweis Zähler Null ist.</span><span class="sxs-lookup"><span data-stu-id="38804-104">The **Release** method deletes the object when its reference count is zero.</span></span>


```C++
STDMETHODIMP_(ULONG) CAVIFileCF::Release() 
{ 
    if (!--m_refs) 
    { 
        delete this;   // If O, delete this instance. 
        return 0; 
    } 
    return m_refs; 
} 

```



 

 




