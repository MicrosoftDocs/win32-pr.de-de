---
title: Manuelle Frame Erfassung
description: Manuelle Frame Erfassung
ms.assetid: 7c5576ff-2694-4f44-a386-03bbc6f9c2ed
keywords:
- WM_CAP_SINGLE_FRAME_OPEN Meldung
- WM_CAP_SINGLE_FRAME Meldung
- WM_CAP_SINGLE_FRAME_CLOSE Meldung
- capcapturesingleframeopen-Makro
- capcapturesingleframe-Makro
- capcapturesingleframeclose-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26899032d8e81be437e8f29acf36f0a37703c560
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855867"
---
# <a name="manual-frame-capture"></a><span data-ttu-id="fe0ee-109">Manuelle Frame Erfassung</span><span class="sxs-lookup"><span data-stu-id="fe0ee-109">Manual Frame Capture</span></span>

<span data-ttu-id="fe0ee-110">Wenn Sie die zu erfassenden Frames einzeln in einem Videostream angeben möchten, können Sie die Reihenfolge steuern, indem Sie die Makros zum Schließen eines einzelnen Frames vom Typ " [**WM \_ \_ \_ \_**](wm-cap-single-frame-open.md)", " [**WM \_ Cap \_ \_**](wm-cap-single-frame.md)Single Frame" und " [**WM Cap Single Frame \_ \_ \_ \_ Close**](wm-cap-single-frame-close.md) " (oder die Makros [**capcapturesingleframeopen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen), [**capcapturesingleframe**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe)und [**capcapturesingleframeclose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) ) verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-110">If you want to individually specify the frames to capture in a video stream, you can control the sequence by using the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md), [**WM\_CAP\_SINGLE\_FRAME**](wm-cap-single-frame.md), and [**WM\_CAP\_SINGLE\_FRAME\_CLOSE**](wm-cap-single-frame-close.md) messages (or the [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen), [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe), and [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) macros).</span></span> <span data-ttu-id="fe0ee-111">In der Regel werden diese Nachrichten verwendet, um eine Animation zu erstellen, indem einzelne Frames an die Erfassungs Datei angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-111">Typically, these messages are used to create animation by appending individual frames to the capture file.</span></span> <span data-ttu-id="fe0ee-112">WM-Abdeckung \_ \_ Single \_ Frame \_ Open öffnet eine Datei für einen manuell betriebenen Aufzeichnungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-112">WM\_CAP\_SINGLE\_FRAME\_OPEN opens a file for a manually driven capture operation.</span></span> <span data-ttu-id="fe0ee-113">Der \_ \_ einzelne \_ Rahmen der WM-Abdeckung erfasst einen einzelnen Frame und fügt ihn an die Erfassungs Datei an.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-113">WM\_CAP\_SINGLE\_FRAME captures an individual frame and appends it to the capture file.</span></span> <span data-ttu-id="fe0ee-114">WM \_ - \_ Cap \_ : einzelner Frame \_ schließt die Datei, die für die manuelle Frame Erfassung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-114">WM\_CAP\_SINGLE\_FRAME\_CLOSE closes the file used for manual frame capture.</span></span>

> [!Note]  
> <span data-ttu-id="fe0ee-115">Diese Aufzeichnungsmethode unterstützt keine gleichzeitige Audioerfassung mit Video Erfassung.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-115">This capture method does not support simultaneous audio capture with video capture.</span></span>

 

 

 




