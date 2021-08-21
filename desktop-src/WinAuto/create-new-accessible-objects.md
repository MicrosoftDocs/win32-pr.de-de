---
title: Erstellen neuer barrierefreier Objekte
description: Erstellen neuer barrierefreier Objekte
ms.assetid: d34a52d1-1eb2-4bb4-989c-a1ca4b5d815f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaaa9ee8669199a9f4de938b4e1cb9e6dd24336bd86527a2cc528709e303543e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052818"
---
# <a name="create-new-accessible-objects"></a>Erstellen neuer barrierefreier Objekte

In diesem Szenario erstellt der Server als Antwort auf jede OBJID CLIENT-Anforderung ein neues [**\_ barrierefreies**](object-identifiers.md) Objekt.

Im folgenden Beispielcode wird ein Zeiger auf das -Steuerelement aus den zusätzlichen Fensterdaten abgerufen. Dieses und das Fensterhand handle werden an den Konstruktor des Benutzerzugriffsserverobjekts (AccServer) übergeben. Dieses Objekt wird immer dann erstellt, [**wenn OBJID \_ CLIENT**](object-identifiers.md) empfangen wird.

Wenn das Objekt erstellt wird, erhält der Server einen Verweis, der nach dem Aufruf von [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)freigegeben werden muss, damit das Objekt zerstört wird, sobald der Client damit fertig ist. Beachten Sie, **dass LresultFromObject** die Verweisanzahl mehrmals erhöht, aber es liegt in der Verantwortung der Clientanwendungen und der Microsoft Active Accessibility Runtime, diese Verweise frei zu geben.


```C++
case WM_GETOBJECT:
{
    // Return the IAccessible object. 
    if ((DWORD)lParam == OBJID_CLIENT)
    {
        // Get the control.  
        CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
        AccServer* pAccServer = new AccServer(hwnd, pCustomList);
        if (pAccServer != NULL)  // NULL if out of memory. 
        {
            LRESULT Lresult = LresultFromObject(IID_IAccessible, wParam, pAccServer);
            pAccServer->Release();
            return Lresult;
        }
        else return 0;
    }
    break;
}
```



 

 




