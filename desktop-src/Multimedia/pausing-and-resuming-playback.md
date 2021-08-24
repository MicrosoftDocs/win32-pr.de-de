---
title: Anhalten und Fortsetzen der Wiedergabe
description: Anhalten und Fortsetzen der Wiedergabe
ms.assetid: f5a7ef22-993c-4aab-bab0-2700289da7a7
keywords:
- MCIWndPause-Makro
- MCIWndResume-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce70a95000cda6fc471967e5075b16fe7bad837c71eed4e6216ddeaddddc4508
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805970"
---
# <a name="pausing-and-resuming-playback"></a>Anhalten und Fortsetzen der Wiedergabe

Sie können die Wiedergabe eines Geräts oder einer Datei unterbrechen, die einem MCIWnd-Fenster zugeordnet ist, indem Sie das [**MCIWndPause-Makro**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) verwenden. Anschließend können Sie die Wiedergabe mithilfe des [**MCIWndResume-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) neu starten. Wenn das Gerät fortsetzen nicht unterstützt oder ein Fehler auftritt, können Sie das [**MCIWndPlay-Makro**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) verwenden, um die Wiedergabe neu zu starten.

Im folgenden Beispiel wird ein MCIWnd-Fenster erstellt und eine AVI-Datei wiedergegeben. Menübefehle zum Anhalten und Fortsetzen stehen dem Benutzer zur Verfügung, um die Wiedergabe zu unterbrechen und neu zu starten.

MCIWnd-Fensterstile werden vorübergehend geändert, indem das [**MCIWndChangeStyles-Makro**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) verwendet wird, um die Anzeige eines MCI-Fehlerdialogfelds zu verhindern, wenn [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) fehlschlägt.


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



 

 




