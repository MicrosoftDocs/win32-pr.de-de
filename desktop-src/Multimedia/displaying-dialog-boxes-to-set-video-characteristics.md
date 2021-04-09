---
title: Anzeigen von Dialog Feldern zum Festlegen von Video Merkmalen
description: Anzeigen von Dialog Feldern zum Festlegen von Video Merkmalen
ms.assetid: 8074f7d1-e8ab-46c3-acc2-a18be0eb4cc7
keywords:
- Capdrivercaps-Struktur
- capdrivergetcaps-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73eea12d69a3d23b0345bee3495d32cbb1ad0ffe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856816"
---
# <a name="displaying-dialog-boxes-to-set-video-characteristics"></a><span data-ttu-id="4b2a8-105">Anzeigen von Dialog Feldern zum Festlegen von Video Merkmalen</span><span class="sxs-lookup"><span data-stu-id="4b2a8-105">Displaying Dialog Boxes to Set Video Characteristics</span></span>

<span data-ttu-id="4b2a8-106">Jeder Aufzeichnungs Treiber kann bis zu drei verschiedene Dialogfelder bereitstellen, die zum Steuern der Aspekte der Video Digitalisierung und des Aufzeichnungsprozesses verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b2a8-106">Each capture driver can provide up to three different dialog boxes used to control aspects of the video digitization and capture process.</span></span> <span data-ttu-id="4b2a8-107">Im folgenden Beispiel wird veranschaulicht, wie diese Dialogfelder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4b2a8-107">The following example demonstrates how to display these dialog boxes.</span></span> <span data-ttu-id="4b2a8-108">Vor dem Anzeigen der einzelnen Dialogfelder wird im Beispiel das [**capdrivergetcaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) -Makro aufgerufen und die [**capdrivercaps**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) -Struktur überprüft, um festzustellen, ob der Erfassungs Treiber Sie anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="4b2a8-108">Before displaying each dialog box, the example calls the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro and checks the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure returned to see if the capture driver can display it.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4b2a8-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b2a8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b2a8-110">Verwenden der Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="4b2a8-110">Using Video Capture</span></span>](using-video-capture.md)
</dt> <dt>

[<span data-ttu-id="4b2a8-111">**capdrivergetcaps**</span><span class="sxs-lookup"><span data-stu-id="4b2a8-111">**capDriverGetCaps**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps)
</dt> </dl>

 

 




