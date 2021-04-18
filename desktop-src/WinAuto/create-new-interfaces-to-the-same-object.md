---
title: Erstellen neuer Schnittstellen für dasselbe Objekt
description: Erstellen neuer Schnittstellen für dasselbe Objekt
ms.assetid: 127c44b6-51a6-4fd6-9edc-9fbe0d08d458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b641eed3918af3acbf399427ad5f7427112f399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337575"
---
# <a name="create-new-interfaces-to-the-same-object"></a><span data-ttu-id="50bdd-103">Erstellen neuer Schnittstellen für dasselbe Objekt</span><span class="sxs-lookup"><span data-stu-id="50bdd-103">Create New Interfaces to the Same Object</span></span>

<span data-ttu-id="50bdd-104">In diesem Szenario antwortet der Server auf jede [**objID- \_ Client**](object-identifiers.md) Anforderung, indem er einen neuen Schnittstellen Zeiger auf das gleiche Objekt erhält.</span><span class="sxs-lookup"><span data-stu-id="50bdd-104">In this scenario, the server responds to each [**OBJID\_CLIENT**](object-identifiers.md) request by obtaining a new interface pointer to the same object.</span></span>

<span data-ttu-id="50bdd-105">Im folgenden Beispielcode ist *m \_ puiobj* ein Zeiger auf ein Objekt, das mehr als eine Component Object Model (com)-Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="50bdd-105">In the following example code, *m\_pUIObj* is a pointer to an object that supports more than one Component Object Model (COM) interface.</span></span> <span data-ttu-id="50bdd-106">Obwohl ein vorhandenes Objekt wieder verwendet wird, wird jedes Mal ein neuer Schnittstellen Zeiger erstellt, wenn das Objekt abgerufen wird, sodass der Verweis Zähler dekrementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="50bdd-106">Even though an existing object is reused, a new interface pointer is created each time the object is retrieved, so the reference count must be decremented.</span></span>


```C++
case WM_GETOBJECT:
   if ((DWORD)lParam == OBJID_CLIENT)
   {
      // Get a new interface to the same object. 
      IAccessible *pAcc = NULL;
      // The following increments the reference count. 
      m_pUIObj->QueryInterface(IID_IAccessible, (LPVOID*)&pAcc); 
      LRESULT lAcc = LresultFromObject(IID_IAccessible, wParam, 
            (LPUNKNOWN) &pAcc); 
      // Release our reference to the object.             
      pAcc->Release();               
      return lAcc;
   }
   break;  // Fall through to DefWindowProc. 
   
```



 

 




