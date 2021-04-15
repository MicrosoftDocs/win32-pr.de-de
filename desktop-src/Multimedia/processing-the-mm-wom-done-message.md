---
title: Verarbeiten der MM_WOM_DONE Nachricht
description: Verarbeiten der von mm \_ WOM verarbeiteten \_ Nachricht
ms.assetid: 215167d0-3020-453d-b6b3-cee5803836c9
keywords:
- Wellenform-Audiodaten, Meldungen
- zusätzliches Audiomaterial, Meldungen
- Wellenform-Audiodatei, MM_WOM_DONE Meldung
- Zusatz Audiodatei, MM_WOM_DONE Meldung
- MM_WOM_DONE Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e909777c115b6b10500e081a08bde6cfe24b00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471252"
---
# <a name="processing-the-mm_wom_done-message"></a><span data-ttu-id="ad2a7-108">Verarbeiten der von mm \_ WOM verarbeiteten \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="ad2a7-108">Processing the MM\_WOM\_DONE Message</span></span>

<span data-ttu-id="ad2a7-109">Im folgenden Beispiel wird gezeigt, wie die Meldung [**mm \_ WOM \_ done**](mm-wom-done.md) verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="ad2a7-109">The following example shows how to process the [**MM\_WOM\_DONE**](mm-wom-done.md) message.</span></span> <span data-ttu-id="ad2a7-110">In diesem Beispiel wird davon ausgegangen, dass die Anwendung nicht mehrere Datenblöcke wieder gibt, sodass das Ausgabegerät nach der Wiedergabe eines einzelnen Datenblocks geschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ad2a7-110">This example assumes the application does not play multiple data blocks, so it can close the output device after playing a single data block.</span></span>


```C++
// WndProc--Main window procedure. 
LRESULT FAR PASCAL WndProc(HWND hWnd, UINT msg, WPARAM wParam, 
    LPARAM lParam) 
{ 
switch (msg) 
{ 
    case MM_WOM_DONE: 
 
    // A waveform-audio data block has been played and 
    // can now be freed. 
    waveOutUnprepareHeader((HWAVEOUT) wParam, 
        (LPWAVEHDR) lParam, sizeof(WAVEHDR) ); 
    
    // Free hData memory. 
    
    waveOutClose((HWAVEOUT) wParam); 
    break; 
    } 
    return DefWindowProc(hWnd, msg, wParam, lParam); 
} 
```



 

 




