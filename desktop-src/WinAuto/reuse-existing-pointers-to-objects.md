---
title: Wiederverwenden vorhandener Zeiger auf Objekte
description: Wiederverwenden vorhandener Zeiger auf Objekte
ms.assetid: 7e1610c6-89b2-4e7e-aee5-94a6cab87a22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14571234ee937d2237d3102316665f15a9ab55415042ddaeda749bfaa21e4807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998120"
---
# <a name="reuse-existing-pointers-to-objects"></a>Wiederverwenden vorhandener Zeiger auf Objekte

In diesem Szenario antwortet der Server jedes Mal mit [](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) demselben IAccessible-Schnittstellenzeiger auf eine [**OBJID-CLIENTanforderung. \_**](object-identifiers.md)

Im folgenden Beispielcode wird das Steuerelementobjekt aus den zusätzlichen Fensterdaten abgerufen, und eine Methode des Steuerelements wird aufgerufen, um das Zugriffsserverobjekt (die anwendungsdefinierte AccServer-Klasse) abzurufen, sofern vorhanden. Wenn der Barrierefreiheitsserver noch nicht vorhanden ist, wird er erstellt.

Wenn das Barrierefreiheitsserverobjekt erstellt wird, hat es den Verweiszähler 1. [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) erhöht den Verweiszähler mehrmals, aber diese Verweise werden freigegeben, wenn der Client mit dem -Objekt fertig ist. Der Server gibt seinen Verweis frei, wenn das Steuerungsfenster zerstört wird.


```C++
case WM_GETOBJECT:
    {
        // Return the IAccessible object. 
        if ((DWORD)lParam == (DWORD)OBJID_CLIENT)
        {
            // Get the control.  
            CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
            // Create the accessible object. 
            AccServer* pAccServer = pCustomList->GetAccServer();
            if (pAccServer == NULL)
            {
                pAccServer = new AccServer(hwnd, pCustomList);
                pCustomList->SetAccServer(pAccServer);
            }
            if (pAccServer != NULL)  // NULL if out of memory. 
            {
                LRESULT Lresult = LresultFromObject(IID_IAccessible, wParam, pAccServer);
                return Lresult;
            }
            else return 0;
        }
        break;
    }

    
case WM_DESTROY:
    {
    CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
    AccServer* pAccServer = pCustomList->GetAccServer();
    if (pAccServer!= NULL)
    {
        // Notify the accessibility object that the control no longer exists. 
        pAccServer->SetControlIsAlive(false);
        // Release the reference created in WM_GETOBJECT. 
        pAccServer->Release(); 
    }   
    // Destroy the control. 
    delete pCustomList;
     break;
    }
```



 

 




