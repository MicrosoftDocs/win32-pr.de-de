---
title: Aktivieren der Video Überlagerung
description: Aktivieren der Video Überlagerung
ms.assetid: f0b4f24c-3e35-4a18-ac77-8cae7083b0fe
keywords:
- capdrivergetcaps-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce51a3b7c77fbb161007ddde7dfe91c36152121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713607"
---
# <a name="enabling-video-overlay"></a><span data-ttu-id="6df0e-104">Aktivieren der Video Überlagerung</span><span class="sxs-lookup"><span data-stu-id="6df0e-104">Enabling Video Overlay</span></span>

<span data-ttu-id="6df0e-105">Im folgenden Beispiel wird das [**capdrivergetcaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) -Makro verwendet, um zu bestimmen, ob ein Erfassungs Treiber über Overlay-Funktionen verfügt. Wenn dies der Fall ist, aktiviert das Makro das Overlay.</span><span class="sxs-lookup"><span data-stu-id="6df0e-105">The following example uses the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro to determine whether a capture driver has overlay capabilities; if it does, the macro enables the overlay.</span></span>


```C++
CAPDRIVERCAPS CapDrvCaps; 

capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 

if (CapDrvCaps.fHasOverlay) 
    capOverlay(hWndC, TRUE);
 
```



## <a name="related-topics"></a><span data-ttu-id="6df0e-106">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6df0e-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6df0e-107">Verwenden der Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="6df0e-107">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




