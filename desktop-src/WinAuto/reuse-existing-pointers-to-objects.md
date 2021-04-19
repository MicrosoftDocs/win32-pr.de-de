---
title: Wieder verwenden vorhandener Zeiger auf Objekte
description: Wieder verwenden vorhandener Zeiger auf Objekte
ms.assetid: 7e1610c6-89b2-4e7e-aee5-94a6cab87a22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c151b8d957fb82718721ad81b452a81a2c71ec84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341638"
---
# <a name="reuse-existing-pointers-to-objects"></a><span data-ttu-id="7dfa0-103">Wieder verwenden vorhandener Zeiger auf Objekte</span><span class="sxs-lookup"><span data-stu-id="7dfa0-103">Reuse Existing Pointers to Objects</span></span>

<span data-ttu-id="7dfa0-104">In diesem Szenario antwortet der Server jedes Mal auf eine [**objID- \_ Client**](object-identifiers.md) Anforderung, die denselben [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger verwendet.</span><span class="sxs-lookup"><span data-stu-id="7dfa0-104">In this scenario, the server responds to an [**OBJID\_CLIENT**](object-identifiers.md) request using the same [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer each time.</span></span>

<span data-ttu-id="7dfa0-105">Im folgenden Beispielcode wird das-Steuerelement Objekt aus den zusätzlichen Fenster Daten abgerufen, und eine-Methode des-Steuer Elements wird aufgerufen, um das Barrierefreiheits Server Objekt (die Anwendungs definierte accserver-Klasse) abzurufen, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7dfa0-105">In the following example code, the control object is retrieved from the extra window data, and a method of the control is called to retrieve the accessibility server object (the application-defined AccServer class), if any.</span></span> <span data-ttu-id="7dfa0-106">Wenn der Barrierefreiheits Server noch nicht vorhanden ist, wird er erstellt.</span><span class="sxs-lookup"><span data-stu-id="7dfa0-106">If the accessibility server does not yet exist, it is created.</span></span>

<span data-ttu-id="7dfa0-107">Wenn das Barrierefreiheits Server Objekt erstellt wird, weist es einen Verweis Zähler von 1 auf.</span><span class="sxs-lookup"><span data-stu-id="7dfa0-107">When the accessibility server object is created, it has a reference count of 1.</span></span> <span data-ttu-id="7dfa0-108">[**Lresultfrovibject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) erhöht den Verweis Zähler mehrmals. diese Verweise werden jedoch freigegeben, wenn der Client das Objekt beendet hat.</span><span class="sxs-lookup"><span data-stu-id="7dfa0-108">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) increments the reference count several times, but these references will be released when the client is finished with the object.</span></span> <span data-ttu-id="7dfa0-109">Der Server gibt seinen Verweis frei, wenn das Steuerelement Fenster zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="7dfa0-109">The server releases its reference when the control window is destroyed.</span></span>


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



 

 




