---
title: Erstellen neuer Schnittstellen für dasselbe Objekt
description: Erstellen neuer Schnittstellen für dasselbe Objekt
ms.assetid: 127c44b6-51a6-4fd6-9edc-9fbe0d08d458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae1d6328b6d803e4d20207381fe596c5f584fee8281e1e6651ffc2325fb044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998710"
---
# <a name="create-new-interfaces-to-the-same-object"></a>Erstellen neuer Schnittstellen für dasselbe Objekt

In diesem Szenario antwortet der Server auf jede [**\_ OBJID-CLIENTanforderung,**](object-identifiers.md) indem er einen neuen Schnittstellenzeiger auf dasselbe Objekt abruft.

Im folgenden Beispielcode ist *m \_ pUIObj* ein Zeiger auf ein Objekt, das mehr als eine com-Schnittstelle (Component Object Model) unterstützt. Obwohl ein vorhandenes Objekt wiederverwendet wird, wird jedes Mal, wenn das Objekt abgerufen wird, ein neuer Schnittstellenzeiger erstellt, sodass die Verweisanzahl dekrementiert werden muss.


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



 

 




