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
# <a name="processing-the-mm_wom_done-message"></a>Verarbeiten der von mm \_ WOM verarbeiteten \_ Nachricht

Im folgenden Beispiel wird gezeigt, wie die Meldung [**mm \_ WOM \_ done**](mm-wom-done.md) verarbeitet wird. In diesem Beispiel wird davon ausgegangen, dass die Anwendung nicht mehrere Datenblöcke wieder gibt, sodass das Ausgabegerät nach der Wiedergabe eines einzelnen Datenblocks geschlossen werden kann.


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



 

 




