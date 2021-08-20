---
title: Automatisieren der Wiedergabe für MCIWnd
description: Automatisieren der Wiedergabe für MCIWnd
ms.assetid: 7e38e8b1-f56d-4008-83a7-4fba8333e328
keywords:
- MCIWndCreate-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27328367e58ffa21a2f83abe8ecab9d9a4259e6fb61b7b0a36d3104adaea5d9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065600"
---
# <a name="automating-playback-for-mciwnd"></a>Automatisieren der Wiedergabe für MCIWnd

Sie können die Wiedergabe für MCIWnd automatisieren, indem Sie bestimmte Fensterstile in der [**MCIWndCreate-Funktion**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) angeben. Um das Gerät wiedergeben zu können, benötigt das Fenster ein übergeordnetes Fenster zum Verarbeiten von Benachrichtigungsmeldungen, einen Wiedergabebereich zum Wiedergeben von AVI-Dateien und eine Benachrichtigung über Gerätemodusänderungen, um zu erkennen, wann die Wiedergabe beendet wird. Das Fenster benötigt keine Symbolleiste. Sie können diese Merkmale festlegen, indem Sie die entsprechenden Stile in **MCIWndCreate angeben.**

Im folgenden Beispiel werden Menübefehle verwendet, um ein MCIWnd-Fenster zu erstellen, um Inhalte von verschiedenen Gerätetypen wieder anzuzeigen. Die **MCIWndCreate-Funktion** erstellt das MCIWnd-Fenster, und Geräte und Dateien werden mithilfe des [**MCIWndOpen-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) in den gerätespezifischen Befehlen geladen. Wenn die Wiedergabe eines Geräts abgeschlossen ist, schließen Sie das Gerät, indem Sie die [**MCIWNDM \_ NOTIFYMODE-Nachricht**](mciwndm-notifymode.md) abfangen und das [**MCIWndClose-Makro**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) ausstellen.


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            dwMCIWndStyle = WS_CHILD |     // child window
                WS_VISIBLE |               // visible
                MCIWNDF_NOTIFYMODE |       // notifies of mode changes
                MCIWNDF_NOPLAYBAR;            // hides toolbar 
            g_hwndMCIWnd = MCIWndCreate(hwnd, 
                g_hinst, dwMCIWndStyle, NULL); 
            break; 
        case IDM_PLAYCDA: 
            LoadNGoMCIWnd(hwnd, "CDAudio"); 
            break; 
        case IDM_PLAYWAVE: 
            LoadNGoMCIWnd(hwnd, "SoundWave.WAV"); 
            break; 
        case IDM_PLAYMIDI: 
            LoadNGoMCIWnd(hwnd, "MIDIFile.MID"); 
            break; 
        case IDM_PLAYAVI: 
            LoadNGoMCIWnd(hwnd, "AVIFile.AVI"); 
            break; 
        case IDM_EXIT: 
            MCIWndDestroy(g_hwndMCIWnd); 
            DestroyWindow(hwnd); 
            break; 
    } 
    break; 
 
case MCIWNDM_NOTIFYMODE: 
    if (lParam == MCI_MODE_STOP)  // device stopped
    { 
        MessageBox(hwnd,"","Closing Device",MB_OK); 
        MCIWndClose(g_hwndMCIWnd); 
    } 
    break; 

// Handle other messages here. 
 
// LoadNGoMCIWnd - automatically loads and plays a multimedia device 
// 
// hwnd -  handle to the parent window 
// lpstr - pointer to device or filename played by device 
// 
// Global variable 
// extern HINSTANCE g_hwndMCIWnd;  instance handle to MCIWnd window 
 
VOID LoadNGoMCIWnd(HWND hwnd, LPSTR lpstr) 
{ 
    MessageBox(hwnd, lpstr, "Loading Device", MB_OK); 
    MCIWndOpen(g_hwndMCIWnd, lpstr, NULL);   // new device in window 
    MCIWndPlay(g_hwndMCIWnd);                // plays device 
} 
```



 

 




