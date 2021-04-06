---
title: Neue barrierefreie Objekte erstellen
description: Neue barrierefreie Objekte erstellen
ms.assetid: d34a52d1-1eb2-4bb4-989c-a1ca4b5d815f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efa85e44d6d51105e6363d276ecb7e5f33d8378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711093"
---
# <a name="create-new-accessible-objects"></a><span data-ttu-id="a95ed-103">Neue barrierefreie Objekte erstellen</span><span class="sxs-lookup"><span data-stu-id="a95ed-103">Create New Accessible Objects</span></span>

<span data-ttu-id="a95ed-104">In diesem Szenario erstellt der Server ein neues Barrierefreies Objekt als Reaktion auf jede [**objID- \_ Client**](object-identifiers.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a95ed-104">In this scenario, the server creates a new accessible object in response to each [**OBJID\_CLIENT**](object-identifiers.md) request.</span></span>

<span data-ttu-id="a95ed-105">Im folgenden Beispielcode wird ein Zeiger auf das-Steuerelement aus den zusätzlichen Fenster Daten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a95ed-105">In the following example code, a pointer to the control is retrieved from the extra window data.</span></span> <span data-ttu-id="a95ed-106">Diese und das Fenster Handle werden an den Konstruktor des benutzerdefinierten Barrierefreiheits Server-Objekts (accserver) übergeben.</span><span class="sxs-lookup"><span data-stu-id="a95ed-106">This and the window handle are passed to the constructor of the custom accessibility server (AccServer) object.</span></span> <span data-ttu-id="a95ed-107">Dieses Objekt wird immer dann erstellt, wenn der [**objID- \_ Client**](object-identifiers.md) empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="a95ed-107">This object is created whenever [**OBJID\_CLIENT**](object-identifiers.md) is received.</span></span>

<span data-ttu-id="a95ed-108">Wenn das-Objekt erstellt wird, ruft der Server einen Verweis ab, der nach dem Aufrufen von [**lresultfroscject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)freigegeben werden muss, damit das Objekt zerstört wird, sobald der Client damit fertig ist.</span><span class="sxs-lookup"><span data-stu-id="a95ed-108">When the object is created, the server obtains a reference, which must be released after calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), so that the object is destroyed as soon as the client is finished with it.</span></span> <span data-ttu-id="a95ed-109">Beachten Sie, dass **lresultfrovibject** den Verweis Zähler mehrmals inkremenkt, aber es liegt in der Verantwortung der Client Anwendungen und der Microsoft Active Accessibility-Laufzeit, diese Verweise freizugeben.</span><span class="sxs-lookup"><span data-stu-id="a95ed-109">Note that **LresultFromObject** increments the reference count several times, but it is the responsibility of client applications, and the Microsoft Active Accessibility runtime, to release these references.</span></span>


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



 

 




