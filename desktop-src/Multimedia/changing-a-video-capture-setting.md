---
title: Ändern einer Videoaufnahmeeinstellung
description: Ändern einer Videoaufnahmeeinstellung
ms.assetid: a5fe7e1e-084d-4102-91d4-ffe5d1d0e5c8
keywords:
- capCaptureGetSetup-Makro
- capCaptureSetSetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af4142880fcbd272bc133d7f488afac02928614cfe33be6d209df27ccd1bc76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145113"
---
# <a name="changing-a-video-capture-setting"></a>Ändern einer Videoaufnahmeeinstellung

Im folgenden Beispiel werden die Makros [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) und [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) verwendet, um die Erfassungsrate vom Standardwert (15 Frames pro Sekunde) in 10 Frames pro Sekunde zu ändern.


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

[Verwenden von Video Capture](using-video-capture.md)
</dt> </dl>

 

 




