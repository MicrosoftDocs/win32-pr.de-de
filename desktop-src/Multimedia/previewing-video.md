---
title: Videovorschau (Windows Multimedia)
description: In diesem Beispiel in Windows Multimedia wird capPreviewRate verwendet, um die Bildanzeigerate für den Vorschaumodus festzulegen, und capPreview, um das Erfassungsfenster in den Vorschaumodus zu versetzen.
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- capPreview-Makro
- capPreviewRate-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e70d0520af3bb71906c6b0ea4d1c0a61464559eedfd2385753b228841fa6af4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037910"
---
# <a name="previewing-video-windows-multimedia"></a>Videovorschau (Windows Multimedia)

Im folgenden Beispiel wird das [**capPreviewRate-Makro**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) verwendet, um die Bildanzeigerate für den Vorschaumodus auf 66 Millisekunden pro Frame festzulegen. Anschließend wird das [**CapPreview-Makro**](/windows/desktop/api/Vfw/nf-vfw-cappreview) verwendet, um das Erfassungsfenster im Vorschaumodus zu platzieren.


```C++
// Create the capture window.
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

capPreviewRate(hWndC, 66);     // rate, in milliseconds
capPreview(hWndC, TRUE);       // starts preview 

// Preview

capPreview(hWndC, FALSE);        // disables preview 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Video capture](using-video-capture.md)
</dt> </dl>

 

 




