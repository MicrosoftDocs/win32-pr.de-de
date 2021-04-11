---
title: Anpassen des Aufzeichnungsprozesses
description: Anpassen des Aufzeichnungsprozesses
ms.assetid: 9453b9d3-ae9c-4f57-8dd6-f84b9a76618e
keywords:
- Mciwndcreate-Funktion
- Mciwndnew-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec46f61ef4624ba613025f01b081ccc1ebda1cad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947690"
---
# <a name="customizing-the-recording-process"></a>Anpassen des Aufzeichnungsprozesses

Sie können den Aufzeichnungsprozess anpassen, indem Sie die vollständige Kontrolle über die meisten Elemente Treffen – von der Erstellung des mciwnd-Fensters bis zum Speichern der aufgezeichneten Informationen in einer Datei. Im folgenden Beispiel wird das MCI-Gerät zum Aufzeichnen und Speichern von Funktionen abgefragt, und es werden Menübefehle zum Aufzeichnen am Anfang oder Ende des Inhalts eingeschlossen.

Im folgenden Beispiel wird die [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) -Funktion verwendet, um ein neues Fenster zu erstellen, und Sie können eine vorhandene Datei angeben, um die aufgezeichneten Daten zu speichern, und das [**mciwndnew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) -Makro, um dem Fenster eine neue Datei zuzuordnen. Alternativ können Sie das Makro [**mciwndopen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) oder [**mciwndopendialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) zum Angeben einer Datei verwenden.

Im Beispiel wird das Makro [**mciwndcanrecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) verwendet, um zu überprüfen, ob das Gerät und das [**mciwndcansave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) -Makro aufzeichnen kann, um zu überprüfen, ob das Gerät Informationen speichert. Im Beispiel wird die aktuelle Wiedergabe Position mithilfe der Makros [**mciwndhome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) und [**mciwndend**](/windows/desktop/api/Vfw/nf-vfw-mciwndend) festgelegt. Im Beispiel wird die Aufzeichnung mit dem [**mciwndrecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) -Makro gestartet. Nachdem die Informationen aufgezeichnet wurden, speichert das Beispiel Sie mithilfe des [**mciwndsavedialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) -Makros.


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate( hwnd, g_hinst, 
                WS_VISIBLE | WS_CHILD | 
                MCIWNDF_RECORD,                   // add Record button
                NULL ); 
 
            MCIWndNew(g_hwndMCIWnd, "waveaudio"); // new file 
 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MessageBox( hwnd, 
                "Press the red button on the toolbar to record.", 
                "MCIWnd Record", 
                MB_OK ); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK ); 
            } 
            break; 
        case IDM_RECORDATSTART: 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MCIWndHome(g_hwndMCIWnd); 
                MCIWndRecord(g_hwndMCIWnd); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK); 
            } 
            break; 
        case IDM_RECORDATEND: 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MCIWndEnd(g_hwndMCIWnd); 
                MCIWndRecord(g_hwndMCIWnd); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK); 
            } 
            break; 
        case IDM_SAVEMCIWND: 
            if( MCIWndCanSave(g_hwndMCIWnd) ) 
                MCIWndSaveDialog(g_hwndMCIWnd); 
    } 
    break; 
 
    // Handle other messages here. 
```



 

 




