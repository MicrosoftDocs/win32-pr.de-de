---
title: Einschränken des Wiedergabebereichs
description: Einschränken des Wiedergabebereichs
ms.assetid: 080ab96f-1cb5-48d4-ac0a-8fd9ba68a31a
keywords:
- MCIWndPlayFrom-Makro
- MCIWndPlayTo-Makro
- MCIWndPlayFromTo-Makro
- MCI-Wiedergabebefehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 064f62e913c33bef0582efaa950ee376e31a5b06a54d0e70674192e31a679a9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139483"
---
# <a name="limiting-the-playback-scope"></a>Einschränken des Wiedergabebereichs

Die Steuerung der Wiedergabe beginnt mit dem [**MCIWndPlay-Makro,**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) das den Inhalt oder die Datei, die einem MCIWnd-Fenster zugeordnet ist, von der aktuellen Wiedergabeposition bis zum Ende des Inhalts wiedergibt. Wenn Sie die Wiedergabe auf einen bestimmten Teil des Inhalts oder der Datei beschränken möchten, können Sie aus den anderen MCIWnd-Wiedergabemakros auswählen: [**MCIWndPlayFrom,**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)und [**MCIWndPlayFromTo.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)

Außerdem müssen Sie ein geeignetes Zeitformat festlegen. Das Zeitformat bestimmt, ob der Inhalt in Frames, Millisekunden, Spuren oder anderen Einheiten gemessen wird.

Im folgenden Beispiel wird ein MCIWnd-Fenster erstellt und Menübefehle zum Wiedergeben des letzten, ersten dritten oder mittleren Drittels des Inhalts angezeigt. Diese Menübefehle verwenden **MCIWndPlayFrom,** **MCIWndPlayTo** und **MCIWndPlayFromTo,** um die Inhaltssegmente wiederzugeben. Im Beispiel werden auch die Makros [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) und [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) verwendet, um den Anfang und das Ende des Inhalts zu identifizieren, und es wird das [**MCIWndHome-Makro**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) verwendet, um die Wiedergabeposition an den Anfang des Inhalts zu verschieben.

Die [**MCIWndCreate-Funktion**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) verwendet die WS \_ CAPTION- und MCIWNDF \_ SHOWALL-Stile zusätzlich zu den Standardfensterstilen, um den Dateinamen, den Modus und die aktuelle Wiedergabeposition in der Titelleiste des MCIWnd-Fensters anzuzeigen.


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate(hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE | WS_CAPTION | 
                MCIWNDF_SHOWALL, 
                "sample.avi"); 
            break;
        case IDM_PLAYFROM:                // plays last third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback end position. 
            lPlayStart = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFrom(g_hwndMCIWnd, lPlayStart); 
            break; 
        case IDM_PLAYTO:                  // plays first third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start position. 
            lPlayEnd = (lEnd - lStart) / 3 + lStart;
 
            MCIWndHome(g_hwndMCIWnd); 
            MCIWndPlayTo(g_hwndMCIWnd, lPlayEnd); 
            break; 
        case IDM_PLAYSOME:               // plays middle third of clip 
            MCIWndUseTime(g_hwndMCIWnd); // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start and end positions. 
            lPlayStart = (lEnd - lStart) / 3 + lStart;
            lPlayEnd = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFromTo(g_hwndMCIWnd, lPlayStart, lPlayEnd); 
            break; 
    
    // Handle other commands here. 
    } 
```



 

 




