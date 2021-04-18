---
title: Lesen von Streams aus einer AVI-Datei
description: Lesen von Streams aus einer AVI-Datei
ms.assetid: fa17cac4-bc6f-48ef-8960-286386b43c82
keywords:
- AVISTREAMINFO-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edbea431a5a5f08602b026e26fd15dfe684c555d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340610"
---
# <a name="reading-streams-from-an-avi-file"></a><span data-ttu-id="a0cb7-104">Lesen von Streams aus einer AVI-Datei</span><span class="sxs-lookup"><span data-stu-id="a0cb7-104">Reading Streams from an AVI File</span></span>

<span data-ttu-id="a0cb7-105">Die folgende Unterroutine ruft streaminformationen aus einer AVI-Datei ab und bestimmt den Streamtyp aus der [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) -Struktur, die von der [**AVISTREAMINFO**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a0cb7-105">The following subroutine obtains stream information from an AVI file and determines the stream type from the [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) structure returned by the [**AVIStreamInfo**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) function.</span></span>


```C++
// StreamTypes - opens the streams in an AVI file and determines 
// stream types. 
// 
// Global variables 
// gcpavi - count of streams in an AVI file 
// gapavi[] = array of stream-interface pointers 
 
void StreamTypes(HWND hwnd) 
{ 
    AVISTREAMINFO     avis; 
    LONG    r, lHeight = 0; 
    WORD    w; 
    int     i; 
    RECT    rc; 
 
// Walk through all streams. 
    for (i = 0; i < gcpavi; i++) { 
        AVIStreamInfo(gapavi[i], &avis, sizeof(avis)); 
 
        if (avis.fccType == streamtypeVIDEO) { 
 
        // Place video-processing functions here. 
 
        } 
        else if (avis.fccType == streamtypeAUDIO) { 
 
        // Place audio-processing functions here. 
 
        } 
        else if (avis.fccType == streamtypeTEXT) { 
 
        // Place text-processing functions here. 
 
        } 
    } 
} 
 
```



 

 




