---
title: Anhalten und Fortsetzen der Wiedergabe
description: Anhalten und Fortsetzen der Wiedergabe
ms.assetid: f5a7ef22-993c-4aab-bab0-2700289da7a7
keywords:
- Mciwndpause-Makro
- Mciwndresume-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1876417b821a57f7ebbac0cd35bec184cc9d2da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947606"
---
# <a name="pausing-and-resuming-playback"></a>Anhalten und Fortsetzen der Wiedergabe

Sie können die Wiedergabe eines Geräts oder einer Datei, das einem mciwnd-Fenster zugeordnet ist, mithilfe des [**mciwndpause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) -Makros unterbrechen. Anschließend können Sie die Wiedergabe mit dem [**mciwndresume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) -Makro neu starten. Wenn das Gerät die Wiederaufnahme nicht unterstützt, oder wenn ein Fehler auftritt, können Sie das [**mciwndplay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) -Makro verwenden, um die Wiedergabe neu zu starten.

Im folgenden Beispiel wird ein mciwnd-Fenster erstellt und eine AVI-Datei wiedergegeben. Die Menübefehle anhalten und fortsetzen sind für den Benutzer zum unterbrechen und erneuten Starten der Wiedergabe verfügbar.

Mciwnd-Fenster Stile werden temporär geändert, indem das [**mciwndchangestyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) -Makro verwendet wird, um zu verhindern, dass ein MCI-Fehler Dialogfeld angezeigt wird, wenn [**mciwndresume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) fehlschlägt.


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND:             // creates and plays clip 
            g_hwndMCIWnd = MCIWndCreate(hwnd,  
                g_hinst,                      
                WS_CHILD | WS_VISIBLE |    // standard styles
                MCIWNDF_NOPLAYBAR |        // hides toolbar 
                MCIWNDF_NOTIFYMODE,        // notifies of mode changes
                "sample.avi"); 
 
            MCIWndPlay(g_hwndMCIWnd); 
            break;    
        case IDM_PAUSEMCIWND:              // pauses playback 
            MCIWndPause(g_hwndMCIWnd); 
            MessageBox(hwnd, "MCIWnd", "Pausing Playback", MB_OK); 
            break; 
        case IDM_RESUMEMCIWND:          // resumes playback 
            MCIWndChangeStyles(      // hides error dialog messages
                g_hwndMCIWnd,        // MCIWnd window
                MCIWNDF_NOERRORDLG,  // mask of style to change
                MCIWNDF_NOERRORDLG); // suppresses MCI error dialogs 
 
            lResult = MCIWndResume(g_hwndMCIWnd); 
 
            if(lResult){                   // device doesn't resume 
                MessageBox(hwnd, "MCIWnd", 
                    "Resume with Stop and Play", MB_OK); 
                MCIWndStop(g_hwndMCIWnd); 
                MCIWndPlay(g_hwndMCIWnd); 
 
                MCIWndChangeStyles(        // resumes original styles
                    g_hwndMCIWnd, 
                    MCIWNDF_NOERRORDLG, 
                    NULL); 
        } 
        break; 
    } 
    break; 
 
// Handle other messages here. 
```



 

 




