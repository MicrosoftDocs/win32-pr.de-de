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
# <a name="create-new-interfaces-to-the-same-object"></a>Erstellen neuer Schnittstellen für dasselbe Objekt

In diesem Szenario antwortet der Server auf jede [**objID- \_ Client**](object-identifiers.md) Anforderung, indem er einen neuen Schnittstellen Zeiger auf das gleiche Objekt erhält.

Im folgenden Beispielcode ist *m \_ puiobj* ein Zeiger auf ein Objekt, das mehr als eine Component Object Model (com)-Schnittstelle unterstützt. Obwohl ein vorhandenes Objekt wieder verwendet wird, wird jedes Mal ein neuer Schnittstellen Zeiger erstellt, wenn das Objekt abgerufen wird, sodass der Verweis Zähler dekrementiert werden muss.


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



 

 




