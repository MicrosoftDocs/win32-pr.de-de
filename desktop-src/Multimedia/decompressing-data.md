---
title: Dekomprimieren von Daten
description: Dekomprimieren von Daten
ms.assetid: 1faf0238-7bef-4363-9bbc-44737600c946
keywords:
- Videokomprimierungs-Manager (VCM), Dekomprimieren von Daten
- VCM (Videokomprimierungs-Manager), Dekomprimieren von Daten
- ICDecompressBegin-Makro
- ICDecompress-Funktion
- ICDecompressEnd-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a213a4d4762f782da817773aac6e8838155561ae47129dd998dad7a82ac5a4f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785430"
---
# <a name="decompressing-data"></a>Dekomprimieren von Daten

Das folgende Beispiel zeigt, wie eine Anwendung einen Dekomprimierer mithilfe des [**Makros ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) initialisieren, eine Framesequenz mithilfe der [**ICDecompress-Funktion**](/windows/desktop/api/Vfw/nf-vfw-icdecompress) dekomprimieren und die Dekomprimierung mithilfe des [**ICDecompressEnd-Makros**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) beenden kann.


```C++
LPBITMAPINFOHEADER lbpiIn, lpbiOut; 
LPVOID             lpIn, lpOut; 
LONG               lNumFrames, lFrameNum; 
 
// Assume lpbiIn and lpbiOut are initialized to the input and output 
// format and lpIn and lpOut are pointing to the buffers. 
if (ICDecompressBegin(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    for (lFrameNum = 0; lFrameNum < lNumFrames, lFrameNum++)
    { 
        if (ICDecompress(hIC, 0, lpbiIn, lpIn, lpbiOut, 
            lpOut) == ICERR_OK) 
        { 
            // Frame decompressed OK so we can process it as required. 
        } 
        else 
        { 
            // Handle the decompression error that occurred. 
        } 
    } 
    ICDecompressEnd(hIC); 
} 
else 
{ 
    // Handle the error identifying an unsupported format. 
} 
 
```



 

 




