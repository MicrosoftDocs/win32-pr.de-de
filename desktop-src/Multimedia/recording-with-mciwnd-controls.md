---
title: Aufzeichnen mit MCIWnd-Steuerelementen
description: Aufzeichnen mit MCIWnd-Steuerelementen
ms.assetid: 65a57400-aeea-4a27-8d51-37d3d9e9bd55
keywords:
- MCIWndCreate-Funktion
- MCIWndNew-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a02dfd62985b0267c685e6893512f977340f47f95801e8821d46005d5371397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805560"
---
# <a name="recording-with-mciwnd-controls"></a>Aufzeichnen mit MCIWnd-Steuerelementen

Im folgenden Beispiel werden Wellenformaudiodaten mithilfe der integrierten Steuerelemente des MCIWnd-Fensters aufgezeichnet. Im Beispiel wird ein MCIWnd-Fenster mithilfe des MCIWNDF \_ RECORD-Fensterstils mit der [**MCIWndCreate-Funktion**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) erstellt, um der Symbolleiste eine **Datensatzschaltfläche** hinzuzufügen. Das [**MCIWndNew-Makro**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) gibt an, dass dem MCIWnd-Fenster eine neue Datei zugeordnet ist und dass ein Waveform-Audiogerät seinen Inhalt bereitstellt. Mit dem zweiten Menübefehl IDM \_ SAVEMCIWND kann der Benutzer die Aufzeichnung speichern und mithilfe des [**MCIWndSaveDialog-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) einen Dateinamen auswählen.


```C++
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, 
            WS_VISIBLE | MCIWNDF_RECORD, NULL); 
        MCIWndNew(g_hwndMCIWnd, "waveaudio"); 
        break;    
    case IDM_SAVEMCIWND: 
        MCIWndSaveDialog(g_hwndMCIWnd); 
        break; 
    } 
```



 

 




