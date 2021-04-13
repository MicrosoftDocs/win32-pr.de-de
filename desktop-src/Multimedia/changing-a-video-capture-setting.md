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
# <a name="changing-a-video-capture-setting"></a>Ändern einer Video Erfassungs Einstellung

Im folgenden Beispiel [**wird die**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) Erfassungs Rate vom Standardwert [](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) (15 Frames pro Sekunde) auf 10 Frames pro Sekunde geändert, um die Erfassungs Rate vom Standardwert (15 Frames pro Sekunde) auf 10 Frames zu ändern.


```C++
CAPTUREPARMS CaptureParms;
float FramesPerSec = 10.0;

capCaptureGetSetup(hWndC, &CaptureParms, sizeof(CAPTUREPARMS));

CaptureParms.dwRequestMicroSecPerFrame = (DWORD) (1.0e6 / 
    FramesPerSec);
capCaptureSetSetup(hWndC, &CaptureParms, sizeof (CAPTUREPARMS)); 
 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Video Erfassung](using-video-capture.md)
</dt> </dl>

 

 




