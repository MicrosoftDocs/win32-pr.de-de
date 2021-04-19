---
title: Anzeigen einer Vorschau für Videos (Windows Multimedia)
description: Anzeigen einer Vorschau für Videos
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- cappreview-Makro
- cappreviewrate-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79c8e24d30fd5141b5b1ac14de99d83e0b2bc620
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341980"
---
# <a name="previewing-video-windows-multimedia"></a><span data-ttu-id="43dad-105">Anzeigen einer Vorschau für Videos (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="43dad-105">Previewing Video (Windows Multimedia)</span></span>

<span data-ttu-id="43dad-106">Im folgenden Beispiel wird das [**cappreviewrate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) -Makro verwendet, um die Frame-Anzeige Rate für den Vorschaumodus auf 66 Millisekunden pro Frame festzulegen. Anschließend wird das Aufzeichnungs Fenster mithilfe des [**cappreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) -Makros im Vorschaumodus platziert.</span><span class="sxs-lookup"><span data-stu-id="43dad-106">The following example uses the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro to set the frame display rate for preview mode to 66 milliseconds per frame and then uses the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro to place the capture window in preview mode.</span></span>


```C++
// Create the capture window.
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

capPreviewRate(hWndC, 66);     // rate, in milliseconds
capPreview(hWndC, TRUE);       // starts preview 

// Preview

capPreview(hWndC, FALSE);        // disables preview 
```



## <a name="related-topics"></a><span data-ttu-id="43dad-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43dad-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43dad-108">Verwenden der Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="43dad-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




