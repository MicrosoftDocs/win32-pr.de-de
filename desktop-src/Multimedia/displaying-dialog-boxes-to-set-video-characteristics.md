---
title: Anzeigen von Dialogfeldern zum Festlegen von Videomerkmalen
description: Anzeigen von Dialogfeldern zum Festlegen von Videomerkmalen
ms.assetid: 8074f7d1-e8ab-46c3-acc2-a18be0eb4cc7
keywords:
- CAPDRIVERCAPS-Struktur
- capDriverGetCaps-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e6ebfa0f75f4bcec63a693636085f16c342e53761b2cb1e67a0e2536fa5cef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144473"
---
# <a name="displaying-dialog-boxes-to-set-video-characteristics"></a>Anzeigen von Dialogfeldern zum Festlegen von Videomerkmalen

Jeder Erfassungstreiber kann bis zu drei verschiedene Dialogfelder bereitstellen, um Aspekte der Videoaufnahme und des Erfassungsprozesses zu steuern. Im folgenden Beispiel wird veranschaulicht, wie diese Dialogfelder angezeigt werden. Vor dem Anzeigen der einzelnen Dialogfelder ruft das Beispiel das [**Makro capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) auf und überprüft die zurückgegebene [**CAPDRIVERCAPS-Struktur,**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) um zu prüfen, ob der Erfassungstreiber sie anzeigen kann.


```C++
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

CAPDRIVERCAPS CapDriverCaps = { }; 
CAPSTATUS     CapStatus = { };

capDriverGetCaps(hWndC, &CapDriverCaps, sizeof(CAPDRIVERCAPS)); 
 
// Video source dialog box. 
if (CapDriverCaps.fHasDlgVideoSource)
{
    capDlgVideoSource(hWndC); 
}
 
// Video format dialog box. 
if (CapDriverCaps.fHasDlgVideoFormat) 
{
    capDlgVideoFormat(hWndC); 

    // Are there new image dimensions?
    capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS));

    // If so, notify the parent of a size change.
} 
 
// Video display dialog box. 
if (CapDriverCaps.fHasDlgVideoDisplay)
{
    capDlgVideoDisplay(hWndC); 
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Video Capture](using-video-capture.md)
</dt> <dt>

[**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps)
</dt> </dl>

 

 




