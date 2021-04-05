---
title: Aufzeichnen mit mciwnd-Steuerelementen
description: Aufzeichnen mit mciwnd-Steuerelementen
ms.assetid: 65a57400-aeea-4a27-8d51-37d3d9e9bd55
keywords:
- Mciwndcreate-Funktion
- Mciwndnew-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814bd9f92b895c03ccbb073f830dbf31dcd2e3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947429"
---
# <a name="recording-with-mciwnd-controls"></a>Aufzeichnen mit mciwnd-Steuerelementen

Im folgenden Beispiel wird Wellenform-Audiodaten mithilfe der integrierten Steuerelemente des mciwnd-Fensters aufgezeichnet. Im Beispiel wird ein mciwnd-Fenster erstellt, indem der mciwndf- \_ Daten Satz Fenster Stil mit der [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) -Funktion verwendet wird, um der Symbolleiste eine **Datensatz** -Schaltfläche hinzuzufügen. Das [**mciwndnew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) -Makro gibt an, dass eine neue Datei dem mciwnd-Fenster zugeordnet ist und dass ein Waveform-Audiogerät seinen Inhalt bereitstellt. Mit dem zweiten Menübefehl, IDM \_ savemciwnd, kann der Benutzer die Aufzeichnung speichern und einen Dateinamen mit dem [**mciwndsavedialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) -Makro auswählen.


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



 

 




