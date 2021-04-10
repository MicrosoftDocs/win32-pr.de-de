---
title: Komprimieren von Daten
description: Komprimieren von Daten
ms.assetid: b231316b-0c81-410a-b2fe-b58ab7aca02b
keywords:
- Videokomprimierungs-Manager (VCM), Komprimieren von Daten
- VCM (Videokomprimierungs-Manager), Komprimieren von Daten
- Iccompressbegin-Makro
- Iccompress-Funktion
- Iccompressend-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c08308b695bf022d2d2b76bda6727d9f9c1a9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036831"
---
# <a name="compressing-data"></a><span data-ttu-id="74e1c-108">Komprimieren von Daten</span><span class="sxs-lookup"><span data-stu-id="74e1c-108">Compressing Data</span></span>

<span data-ttu-id="74e1c-109">Im folgenden Beispiel werden Bilddaten für die Verwendung in einer AVI-Datei komprimiert.</span><span class="sxs-lookup"><span data-stu-id="74e1c-109">The following example compresses image data for use in an AVI file.</span></span> <span data-ttu-id="74e1c-110">Es wird davon ausgegangen, dass der-Kompressor die Temporal-Flags von vidcf \_ Crunch oder vidcf nicht unterstützt \_ , sondern die vidcf-Qualität unterstützt \_ .</span><span class="sxs-lookup"><span data-stu-id="74e1c-110">It assumes the compressor does not support the VIDCF\_CRUNCH or VIDCF\_TEMPORAL flags, but it does support VIDCF\_QUALITY.</span></span> <span data-ttu-id="74e1c-111">Das Beispiel verwendet das [**iccompressbegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) -Makro, die [**iccompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) -Funktion und das [**iccompressend**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) -Makro.</span><span class="sxs-lookup"><span data-stu-id="74e1c-111">The example uses the [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) macro, the [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) function, and the [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) macro.</span></span>


```C++
DWORD dwCkID; 
DWORD dwCompFlags; 
DWORD dwQuality; 
LONG  lNumFrames, lFrameNum; 
// Assume dwNumFrames is initialized to the total number of frames. 
// Assume dwQuality holds the proper quality value (0-10000). 
// Assume lpbiOut, lpOut, lpbiIn, and lpIn are initialized properly. 
 
// If OK to start, compress each frame. 
if (ICCompressBegin(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    for ( lFrameNum = 0; lFrameNum < lNumFrames; lFrameNum++)
    { 
        if (ICCompress(hIC, 0, lpbiOut, lpOut, lpbiIn, lpIn, 
            &dwCkID, &dwCompFlags, lFrameNum, 
            0, dwQuality, NULL, NULL) == ICERR_OK)
        { 
            // Write compressed data to the AVI file. 
             
            // Set lpIn to the next frame in the sequence. 
             
        } 
        else 
        { 
            // Handle compressor error. 
        } 
    } 
    ICCompressEnd(hIC);    // terminate compression 
} 
else 
{ 
    // Handle the error identifying the unsupported format. 
} 
 
```



 

 




