---
title: Konfigurieren eines installierbaren Treibers
description: Konfigurieren eines installierbaren Treibers
ms.assetid: c81f4bcb-38c6-42f1-a50d-1f700c6a3c37
keywords:
- installierbare Treiber, konfigurieren
- Konfigurieren installier barer Treiber
- Opendriver-Funktion
- Senddrivermessage-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad0ad16d719152dba0dc0b2ca6224122831a0ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038820"
---
# <a name="configuring-an-installable-driver"></a><span data-ttu-id="dd504-107">Konfigurieren eines installierbaren Treibers</span><span class="sxs-lookup"><span data-stu-id="dd504-107">Configuring an Installable Driver</span></span>

<span data-ttu-id="dd504-108">Um einen installierbaren Treiber zum Ausführen nützlicher Aufgaben zu leiten, müssen Sie den Treiber mithilfe der [opendriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) -Funktion öffnen und mithilfe der [senddrivermessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) -Funktion senden.</span><span class="sxs-lookup"><span data-stu-id="dd504-108">To direct an installable driver to carry out useful tasks, you must open the driver by using the [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) function and send it messages by using the [SendDriverMessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) function.</span></span> <span data-ttu-id="dd504-109">Im folgenden Beispiel wird gezeigt, wie der Treiber angewiesen wird, das zugehörige Konfigurations Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="dd504-109">The following example shows how to direct the driver to display its configuration dialog box.</span></span>


```C++
LONG MyConfigureDriver()
{
    HDRVR hdrvr;
    DRVCONFIGINFO dci;
    LONG lRes;

    // Open the driver (no additional parameters needed this time).
    if ((hdrvr = OpenDriver(L"\\samples\\sample.drv", 0, 0)) == 0) {
        // Can't open the driver
        return DRVCNF_CANCEL;
    }

    // Make sure driver has a configuration dialog box.
    if (SendDriverMessage(hdrvr, DRV_QUERYCONFIGURE, 0, 0) != 0) {
        // Set the DRVCONFIGINFO structure and send the message
        dci.dwDCISize = sizeof (dci);
        dci.lpszDCISectionName = (LPWSTR)0;
        dci.lpszDCIAliasName = (LPWSTR)0;
        lRes = SendDriverMessage(hdrvr, DRV_CONFIGURE, 0, (LONG)&dci);
     }

    // Close the driver (no additional parameters needed this time).
    CloseDriver(hdrvr, 0, 0);

    return lRes;
}
 
```



 

 