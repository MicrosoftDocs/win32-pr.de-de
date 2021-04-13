---
title: Automatisieren der Wiedergabe für mciwnd
description: Automatisieren der Wiedergabe für mciwnd
ms.assetid: 7e38e8b1-f56d-4008-83a7-4fba8333e328
keywords:
- Mciwndcreate-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b9224cfa4f5a93488f226d1aefa83201b8b0637
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311130"
---
# <a name="automating-playback-for-mciwnd"></a>Automatisieren der Wiedergabe für mciwnd

Sie können die Wiedergabe für mciwnd automatisieren, indem Sie bestimmte Fenster Stile in der [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) -Funktion angeben. Zum Wiedergeben des Geräts benötigt das Fenster ein übergeordnetes Fenster zum Verarbeiten von Benachrichtigungs Meldungen, einen Wiedergabe Bereich zum Abspielen von AVI-Dateien und Benachrichtigungen über Änderungen im Geräte Modus, um zu ermitteln, wann die Wiedergabe beendet wird. Das Fenster benötigt keine Symbolleiste. Sie können diese Merkmale festlegen, indem Sie die entsprechenden Stile in **mciwndcreate** angeben.

Im folgenden Beispiel werden Menübefehle verwendet, um ein mciwnd-Fenster zum Wiedergeben von Inhalten verschiedener Gerätetypen zu erstellen. Die Funktion **mciwndcreate** erstellt das mciwnd-Fenster, und Geräte und Dateien werden mithilfe des [**mciwndopen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) -Makros in den gerätespezifischen Befehlen geladen. Wenn die Wiedergabe eines Geräts abgeschlossen ist, schließen Sie das Gerät, indem Sie die [**mciwndm-Meldung " \_ notifymode**](mciwndm-notifymode.md) " abfangen und das Makro " [**mciwndclose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) " ausgeben.


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



 

 




