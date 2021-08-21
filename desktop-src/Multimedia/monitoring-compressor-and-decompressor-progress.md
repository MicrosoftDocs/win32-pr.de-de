---
title: Überwachen des Fortschritts von Überwachungs- und Dekomprimierungsfortschritten
description: Überwachen des Fortschritts von Überwachungs- und Dekomprimierungsfortschritten
ms.assetid: 7c87c688-75b6-4d3e-9dd5-5f509ff2e473
keywords:
- Videokomprimierungs-Manager (VCM), Überwachung
- VCM (Videokomprimierungs-Manager), Überwachung
- ICSetStatusProc-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724d3e6a8bee645717ef624eddd1276d3e55e856f1aab3c6edc5f9585b3f5feb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137181"
---
# <a name="monitoring-compressor-and-decompressor-progress"></a>Überwachen des Fortschritts von Überwachungs- und Dekomprimierungsfortschritten

Das folgende Beispiel zeigt, wie die [**ICSetStatusProc-Funktion**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) verwendet wird, um den Bzw. den Dekomprimierer über die Adresse der Rückruffunktion zu informieren:


```C++
ICSetStatusProc(compvars.hic, 0, (LPARAM) (UINT) hwndApp, 
    &PreviewStatusProc); 
 
```



Das folgende Beispiel zeigt die Rückruffunktion, die vom vorherigen Fragment installiert wurde:


```C++
LONG CALLBACK export PreviewStatusProc(LPARAM lParam, 
    UINT message, LONG l) 
{ 
    switch (message) 
    { 
        MSG msg; 
        case ICSTATUS_START: 
         
        // Create and display status dialog box. 
         
            break; 
        case ICSTATUS_STATUS: 
            ProSetBarPos((int) l); // sets status bar positions 
 
        // Watch for abort message 
            while(PeekMessage(&msg, NULL, 0, 0, PM_REMOVE)) 
            { 
                if (msg.message == WM_KEYDOWN && msg.wParam == 
                    VK_ESCAPE) 
                    return 1; 
                if (msg.message == WM_SYSCOMMAND && 
                    (msg.wParam & 0xFFF0) == SC_CLOSE) 
                    return 1; 
 
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
            break; 
        case ICSTATUS_END: 
         
        // Close and destroy status dialog box. 
         
            break; 
        case ICSTATUS_YIELD: 
         
         
         
            break; 
    } 
    return 0; 
} 
 
```



 

 




