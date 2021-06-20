---
title: Vorschau von Videos (Windows Multimedia)
description: In diesem Beispiel in Windows Multimedia wird capPreviewRate verwendet, um die Bildanzeigerate für den Vorschaumodus und capPreview so zu festlegen, dass das Erfassungsfenster in den Vorschaumodus gesetzt wird.
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- capPreview-Makro
- capPreviewRate-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc3aaeb9a8ff0f040218fca4822af93ab8bfe29
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405543"
---
# <a name="previewing-video-windows-multimedia"></a><span data-ttu-id="86df1-105">Vorschau von Videos (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="86df1-105">Previewing Video (Windows Multimedia)</span></span>

<span data-ttu-id="86df1-106">Im folgenden Beispiel wird das [**Makro capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) verwendet, um die Bildanzeigerate für den Vorschaumodus auf 66 Millisekunden pro Frame zu setzen. Anschließend wird das [**CapPreview-Makro**](/windows/desktop/api/Vfw/nf-vfw-cappreview) verwendet, um das Erfassungsfenster im Vorschaumodus zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="86df1-106">The following example uses the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro to set the frame display rate for preview mode to 66 milliseconds per frame and then uses the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro to place the capture window in preview mode.</span></span>


```C++
// Create the capture window.
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

capPreviewRate(hWndC, 66);     // rate, in milliseconds
capPreview(hWndC, TRUE);       // starts preview 

// Preview

capPreview(hWndC, FALSE);        // disables preview 
```



## <a name="related-topics"></a><span data-ttu-id="86df1-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="86df1-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86df1-108">Verwenden von Video Capture</span><span class="sxs-lookup"><span data-stu-id="86df1-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




