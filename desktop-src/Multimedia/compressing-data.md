---
title: Komprimieren von Daten
description: Komprimieren von Daten
ms.assetid: b231316b-0c81-410a-b2fe-b58ab7aca02b
keywords:
- Videokomprimierungs-Manager (VCM), Komprimieren von Daten
- VCM (Videokomprimierungs-Manager),Komprimieren von Daten
- ICCompressBegin-Makro
- ICCompress-Funktion
- ICCompressEnd-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f45c7b592b4b55e77b71390d7ffd79b23714242ea678d641d4a3f5b8118bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145003"
---
# <a name="compressing-data"></a>Komprimieren von Daten

Im folgenden Beispiel werden Bilddaten für die Verwendung in einer AVI-Datei komprimiert. Es wird davon ausgegangen, dass die VIDCF \_ CRUNCH- oder VIDCF TEMPORAL-Flags von der Vidcf nicht unterstützt \_ werden, aber sie unterstützt VIDCF \_ QUALITY. Im Beispiel werden das [**ICCompressBegin-Makro,**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) die [**ICCompress-Funktion**](/windows/desktop/api/Vfw/nf-vfw-iccompress) und das [**ICCompressEnd-Makro**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) verwendet.


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



 

 




