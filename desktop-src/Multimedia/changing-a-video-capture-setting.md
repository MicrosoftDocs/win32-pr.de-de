---
title: Ändern einer Video Erfassungs Einstellung
description: Ändern einer Video Erfassungs Einstellung
ms.assetid: a5fe7e1e-084d-4102-91d4-ffe5d1d0e5c8
keywords:
- capcapturegetsetup-Makro
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b3f2629325c67bcad1fed26a9fed4d053372392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388713"
---
# <a name="changing-a-video-capture-setting"></a><span data-ttu-id="0c15e-105">Ändern einer Video Erfassungs Einstellung</span><span class="sxs-lookup"><span data-stu-id="0c15e-105">Changing a Video Capture Setting</span></span>

<span data-ttu-id="0c15e-106">Im folgenden Beispiel [**wird die**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) Erfassungs Rate vom Standardwert [](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) (15 Frames pro Sekunde) auf 10 Frames pro Sekunde geändert, um die Erfassungs Rate vom Standardwert (15 Frames pro Sekunde) auf 10 Frames zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0c15e-106">The following example uses the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) and [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macros to change the capture rate from the default value (15 frames per second) to 10 frames per second.</span></span>


```C++
CAPTUREPARMS CaptureParms;
float FramesPerSec = 10.0;

capCaptureGetSetup(hWndC, &CaptureParms, sizeof(CAPTUREPARMS));

CaptureParms.dwRequestMicroSecPerFrame = (DWORD) (1.0e6 / 
    FramesPerSec);
capCaptureSetSetup(hWndC, &CaptureParms, sizeof (CAPTUREPARMS)); 
 
```



## <a name="related-topics"></a><span data-ttu-id="0c15e-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0c15e-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c15e-108">Verwenden der Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="0c15e-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




