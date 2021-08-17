---
title: Lesen Streams aus einer AVI-Datei
description: Lesen Streams aus einer AVI-Datei
ms.assetid: fa17cac4-bc6f-48ef-8960-286386b43c82
keywords:
- AVIStreamInfo-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d42c4682c1875fffbea079ab9ef55d954f15d3e9d49c2da1309504da68aa92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371515"
---
# <a name="reading-streams-from-an-avi-file"></a>Lesen Streams aus einer AVI-Datei

Die folgende Unterroutine ruft Streaminformationen aus einer AVI-Datei ab und bestimmt den Streamtyp aus der [**AVISTREAMINFO-Struktur,**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) die von der [**AVIStreamInfo-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) zurückgegeben wird.


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



 

 




