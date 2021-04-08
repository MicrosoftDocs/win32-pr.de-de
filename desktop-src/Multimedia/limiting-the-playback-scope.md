---
title: Einschränken des Wiedergabe Bereichs
description: Einschränken des Wiedergabe Bereichs
ms.assetid: 080ab96f-1cb5-48d4-ac0a-8fd9ba68a31a
keywords:
- Mciwndplayfrom-Makro
- Mciwndplayto-Makro
- Mciwndplayfromto-Makro
- MCI-Wiedergabe Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 465bcf7a7b6b5811de8413a1c89f7befcf81037f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855875"
---
# <a name="limiting-the-playback-scope"></a>Einschränken des Wiedergabe Bereichs

Das Steuern der Wiedergabe beginnt mit dem [**mciwndplay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) -Makro, das den Inhalt oder die Datei wieder gibt, der mit einem mciwnd-Fenster von der aktuellen Wiedergabe Position bis zum Ende des Inhalts verknüpft ist. Wenn Sie die Wiedergabe auf einen bestimmten Teil des Inhalts oder der Datei beschränken möchten, können Sie zwischen den anderen Wiedergabe-mciwnd-Makros wählen: [**mciwndplayfrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom), [**mciwndplayto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)und [**mciwndplayfromto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto).

Außerdem müssen Sie ein geeignetes Zeitformat festlegen. Das Zeitformat bestimmt, ob der Inhalt in Frames, Millisekunden, Spuren oder anderen Einheiten gemessen wird.

Im folgenden Beispiel wird ein mciwnd-Fenster erstellt und Menübefehle bereitstellt, um das letzte Dritte, erste Dritte oder mittlere dritte des Inhalts wiederzugeben. Diese Menübefehle verwenden **mciwndplayfrom**, **mciwndplayto** und **mciwndplayfromto** zum Wiedergeben der Inhalts Segmente. Das Beispiel verwendet auch die Makros " [**mciwndgetstart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) " und " [**mciwndgetend**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) ", um den Anfang und das Ende des Inhalts zu identifizieren, und verwendet das [**mciwndhome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) -Makro, um die Wiedergabe Position an den Anfang des Inhalts zu verschieben.

Die [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) -Funktion verwendet \_ zusätzlich zu den Standardfenster Stilen die WS-Beschriftung und mciwndf- \_ ShowAll-Stile, um den Dateinamen, den Modus und die aktuelle Wiedergabe Position in der Titelleiste des mciwnd-Fensters anzuzeigen.


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



 

 




