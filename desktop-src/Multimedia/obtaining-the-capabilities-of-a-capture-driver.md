---
title: Abrufen der Funktionen eines Erfassungs Treibers
description: Abrufen der Funktionen eines Erfassungs Treibers
ms.assetid: 17e90ca6-3646-41cb-8d7a-a2102bc16cc5
keywords:
- WM_CAP_DRIVER_GET_CAPS Meldung
- capdrivergetcaps-Makro
- Capdrivercaps-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d15a3b1e01ccff738494f287126b7e1ab033056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337398"
---
# <a name="obtaining-the-capabilities-of-a-capture-driver"></a><span data-ttu-id="dbb41-106">Abrufen der Funktionen eines Erfassungs Treibers</span><span class="sxs-lookup"><span data-stu-id="dbb41-106">Obtaining the Capabilities of a Capture Driver</span></span>

<span data-ttu-id="dbb41-107">Die Meldung " [**WM- \_ Cap- \_ Treiber \_ get \_ Caps**](wm-cap-driver-get-caps.md) " gibt die Funktionen des Aufzeichnungs Treibers und der zugrunde liegenden Hardware in der [**capdrivercaps**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="dbb41-107">The [**WM\_CAP\_DRIVER\_GET\_CAPS**](wm-cap-driver-get-caps.md) message returns the capabilities of the capture driver and underlying hardware in the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span> <span data-ttu-id="dbb41-108">Jedes Mal, wenn eine Anwendung einen neuen Aufzeichnungs Treiber mit dem Erfassungsfenster verbindet, sollte Sie die **capdrivercaps** -Struktur aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="dbb41-108">Each time an application connects a new capture driver to the capture window, it should update the **CAPDRIVERCAPS** structure.</span></span> <span data-ttu-id="dbb41-109">Im folgenden Beispiel wird das [**capdrivergetcaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) -Makro verwendet, um die Aufzeichnungs Treiberfunktionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="dbb41-109">The following example uses the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro to obtain the capture driver capabilities.</span></span>


```C++
CAPDRIVERCAPS CapDrvCaps; 

SendMessage (hWndC, WM_CAP_DRIVER_GET_CAPS, 
    sizeof (CAPDRIVERCAPS), (LONG) (LPVOID) &CapDrvCaps); 

// Or, use the macro to retrieve the driver capabilities. 
// capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 
```



## <a name="related-topics"></a><span data-ttu-id="dbb41-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dbb41-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbb41-111">Verwenden der Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="dbb41-111">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




