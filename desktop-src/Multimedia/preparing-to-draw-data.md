---
title: Zeichnen von Daten wird vorbereitet
description: Zeichnen von Daten wird vorbereitet
ms.assetid: 98adcee4-06c0-4684-bd9e-e030e3f9a59d
keywords:
- Videokomprimierungs-Manager (VCM), zeichnen
- VCM (Videokomprimierungs-Manager), zeichnen
- Icdrawbegin-Makro
- Icdrawend-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de20d23c0ded51d1933918c16da3f8827b77f796
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206687"
---
# <a name="preparing-to-draw-data"></a><span data-ttu-id="6eca5-107">Zeichnen von Daten wird vorbereitet</span><span class="sxs-lookup"><span data-stu-id="6eca5-107">Preparing to Draw Data</span></span>

<span data-ttu-id="6eca5-108">Das folgende Beispiel zeigt die Initialisierungs Sequenz, die den Dekompressor anweist, den voll Bildschirm zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="6eca5-108">The following example shows the initialization sequence that instructs the decompressor to draw full-screen.</span></span> <span data-ttu-id="6eca5-109">Sie verwendet die Makros [**icdrawbegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) und [**icdrawend**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) .</span><span class="sxs-lookup"><span data-stu-id="6eca5-109">It uses the [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) and [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) macros.</span></span>


```C++
// Assume lpbiIn has the input format, dwRate has the data rate. 

if (ICDrawBegin(hIC, ICDRAW_QUERY | ICDRAW_FULLSCREEN, NULL, NULL, 
    NULL, 0, 0, 0, 0, lpbiIn, 0, 0, 0, 0, dwRate, 
    dwScale) == ICERR_OK) 
{ 
    // Decompressor supports this drawing so set up to draw. 
    ICDrawBegin(hIC, ICDRAW_FULLSCREEN, hPal, NULL, NULL, 0, 0, 0, 
        0, lpbiIn, 0, 0, lbpi->biWidth, lpbi->biHeight, dwRate, 
        dwScale); 
    . 
    . // Start decompressing and drawing frames. 
    . 
 
    // Drawing done. Terminate procedure. 
    ICDrawEnd(hIC); 
} 
else 
{ 
    
    // Use another renderer to draw data on the screen; 
    // ICDraw does not support the format. 
} 
 
```



 

 




