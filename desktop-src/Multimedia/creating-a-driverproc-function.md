---
title: Erstellen einer driverproc-Funktion
description: Erstellen einer driverproc-Funktion
ms.assetid: 8182d115-ba0b-43f4-a6b9-9f6a19493247
keywords:
- installierbare Treiber, erstellen
- Erstellen der driverproc-Funktion
- Driverproc-Funktion
- installierbare Treiber, driverproc-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6865d5e13425fe873e74ac77af5ae66401280e6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341934"
---
# <a name="creating-a-driverproc-function"></a><span data-ttu-id="c3268-107">Erstellen einer driverproc-Funktion</span><span class="sxs-lookup"><span data-stu-id="c3268-107">Creating a DriverProc Function</span></span>

<span data-ttu-id="c3268-108">Sie erstellen eine [driverproc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) -Funktion auf die gleiche Weise wie bei der Erstellung einer Fenster Prozedur.</span><span class="sxs-lookup"><span data-stu-id="c3268-108">You create a [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function in much the same way as you create a window procedure.</span></span> <span data-ttu-id="c3268-109">Die Funktion besteht aus einer **Switch** -Anweisung, und jeder Fall verarbeitet eine bestimmte Treiber Nachricht und gibt einen Wert zurück, der den Erfolg oder Misserfolg angibt.</span><span class="sxs-lookup"><span data-stu-id="c3268-109">The function consists of a **switch** statement, and each case processes a given driver message, returning a value indicating success or failure.</span></span> <span data-ttu-id="c3268-110">Die **driverproc** -Funktion hat die folgende Form:</span><span class="sxs-lookup"><span data-stu-id="c3268-110">The **DriverProc** function has the following form:</span></span>


```C++
LONG DriverProc(DWORD dwDriverId, HDRVR hdrvr, UINT msg, 
    LONG lParam1, LONG lParam2)
{
    DWORD dwRes = 0L;

    switch (msg) {
    case DRV_LOAD:
    // Sent when the driver is loaded. This is always   
    // the first message received by a driver. 
        dwRes = 1L;  // returns 0L to fail
        break;

    case DRV_FREE:
    // Sent when the driver is about to be discarded.
    // This is the last message a driver receives
    // before it is freed.
        dwRes = 1L;  // return value ignored
        break;

    case DRV_OPEN:
    // Sent when the driver is opened.
        dwRes = 1L;  // returns 0L to fail
        break;       // value subsequently used
                     // for dwDriverId.

    case DRV_CLOSE:
    // Sent when the driver is closed. Drivers are
    // unloaded when the open count reaches zero.
        dwRes = 1L;  // returns 0L to fail
        break;

    case DRV_ENABLE:
    // Sent when the driver is loaded or reloaded and
    // when Windows is enabled. Install interrupt
    // handlers and initialize hardware. Expect the
    // driver to be in memory only between the enable
    // and disable messages.
        dwRes = 1L;  // return value ignored
        break;

    case DRV_DISABLE:
    // Sent before the driver is freed or when Windows
    // is disabled. Remove interrupt handlers and place
    // hardware in an inactive state.
        dwRes = 1L;  // return value ignored
        break;

    case DRV_INSTALL:
    // Sent when the driver is installed.
        dwRes = DRVCNF_OK;  // Can also return 
        break;              // DRVCNF_CANCEL
                            // and DRV_RESTART

    case DRV_REMOVE:
    // Sent when the driver is removed.
        dwRes = 1L;  // return value ignored
        break;

    case DRV_QUERYCONFIGURE:
    // Sent to determine if the driver can be
    // configured.
        dwRes = 0L;  // Zero indicates configuration
        break;       // NOT supported

    case DRV_CONFIGURE:
    // Sent to display the configuration
    // dialog box for the driver.
        dwRes = DRVCNF_OK;  // Can also return
        break;              // DRVCNF_CANCEL
                            // and DRVCNF_RESTART

    default:
    // Process any other messages.
        return DefDriverProc (dwDriverId, hdrvr, 
            msg, lParam1, lParam2);

    }
    return dwRes;
}
 
```



 

 