---
title: Benennen der Erfassungs Datei
description: Benennen der Erfassungs Datei
ms.assetid: fae2fd6a-4c2f-432f-a714-9faae6daeafe
keywords:
- capfilesetcapturefile-Makro
- capfilezuweisung-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ea091a36777e176124689ba57be6c0fb75d07d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310384"
---
# <a name="naming-the-capture-file"></a><span data-ttu-id="48f1e-105">Benennen der Erfassungs Datei</span><span class="sxs-lookup"><span data-stu-id="48f1e-105">Naming the Capture File</span></span>

<span data-ttu-id="48f1e-106">Im folgenden Beispiel wird das [**capfilesetcapturefile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) -Makro verwendet, um einen alternativen Dateinamen (MYCAP.AVI) für die Erfassungs Datei anzugeben, und das [**capfilealloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) -Makro, um eine Datei mit einer Größe von 5 MB vorab zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="48f1e-106">The following example uses the [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) macro to specify an alternate filename (MYCAP.AVI) for the capture file and the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro to preallocate a file of 5 MB.</span></span>


```C++
char szCaptureFile[] = "MYCAP.AVI";

capFileSetCaptureFile( hWndC, szCaptureFile); 
capFileAlloc( hWndC, (1024L * 1024L * 5)); 
 
```



## <a name="related-topics"></a><span data-ttu-id="48f1e-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48f1e-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48f1e-108">Verwenden der Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="48f1e-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




