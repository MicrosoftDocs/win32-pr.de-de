---
title: Verarbeiten der MM_WOM_DONE-Nachricht
description: Verarbeiten der MM \_ WOM \_ DONE-Nachricht
ms.assetid: 215167d0-3020-453d-b6b3-cee5803836c9
keywords:
- Waveform-Audio, Nachrichten
- Hilfsaudio, Nachrichten
- Waveformaudio, MM_WOM_DONE Nachricht
- Hilfsaudio, MM_WOM_DONE Nachricht
- MM_WOM_DONE Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6aca93f23ed74a4a4974633d8345f2e897535e156ccc03f46eb0da92a2d2fdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037860"
---
# <a name="processing-the-mm_wom_done-message"></a>Verarbeiten der MM \_ WOM \_ DONE-Nachricht

Das folgende Beispiel zeigt, wie die [**MM \_ WOM \_ DONE-Nachricht verarbeitet**](mm-wom-done.md) wird. In diesem Beispiel wird davon ausgegangen, dass die Anwendung nicht mehrere Datenblöcke wiedergibt, sodass sie das Ausgabegerät nach dem Wiedergeben eines einzelnen Datenblocks schließen kann.


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



 

 




