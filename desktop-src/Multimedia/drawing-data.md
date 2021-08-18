---
title: Zeichnen von Daten
description: Zeichnen von Daten
ms.assetid: cc4f383d-54d4-4027-ad6a-da19bb07c17f
keywords:
- Videokomprimierungs-Manager (VCM), Zeichnen
- VCM (Videokomprimierungs-Manager),Zeichnen
- ICDraw-Funktion
- ICDrawStart-Makro
- ICDrawStop-Makro
- ICDrawFlush-Makro
- ICDrawEnd-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcbb9f0c9c39da17c4f60af3dfb9c3a7e0179ebf4c8ed6e5bcac4cdc6f24828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496710"
---
# <a name="drawing-data"></a>Zeichnen von Daten

Im folgenden Beispiel werden die [**ICDraw-Funktion**](/windows/desktop/api/Vfw/nf-vfw-icdraw) und die [**IcDrawStart-,**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) [**ICDrawStop-,**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) [**ICDrawFlush-**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush)und [**ICDrawEnd-Makros**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) verwendet, um Daten auf dem Bildschirm zu zeichnen.


```C++
DWORD    dwNumBuffers; 
 
// Find out how many buffers need filling before drawing starts.

ICGetBuffersWanted(hIC, &dwNumBuffers); 
for (dw = 0; dw < dwNumBuffers; dw++)
{ 
    ICDraw(hIC, 0, lpFormat, lpData, cbData, dw); // fill the pipeline
    
    // Point lpFormat and lpData to next format and buffer.
    
} 
ICDrawStart(hIC);  // starts the clock 
dw = 0; 
while (fPlaying) 
{ 
    ICDraw(hIC, 0, lpFormat, lpData, chData, dw); // fill more buffers 
    
    // Point lpFormat and lpData to next format and buffer,
    // update dw.
} 
 
ICDrawStop(hIC);   // stops drawing and decompressing when done 
ICDrawFlush(hIC);  // flushes any existing buffers 
ICDrawEnd(hIC);    // ends decompression 
 
```



 

 




