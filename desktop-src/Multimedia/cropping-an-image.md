---
title: Zuschneiden eines Bilds
description: Zuschneiden eines Bilds
ms.assetid: 6600751c-d4b6-481d-bf69-be2d34244c05
keywords:
- MCIWndGetSource-Makro
- MCIWndPutSource-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0150962dc85e1e179e52a06c7af6c29193b40b50e9acc7a9feecd0570ab4214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144607"
---
# <a name="cropping-an-image"></a>Zuschneiden eines Bilds

Im folgenden Beispiel wird ein MCIWnd-Fenster erstellt und eine AVI-Datei geladen. Das Fenster enthält einen Zuschneidebefehl im Menü, der ein Viertel der Höhe oder Breite von jeder der vier Seiten des Rahmens zuschneiden kann. Im Beispiel werden die aktuellen (anfänglichen) Dimensionen des Quellrechtecks mithilfe des [**MCIWndGetSource-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) abgerufen. Das geänderte Quellrechteck ist halb so groß wie die ursprüngliche Höhe und Breite und wird im ursprünglichen Rahmen zentriert. Der Aufruf des [**MCIWndPutSource-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) definiert die Koordinaten des Quellrechtecks neu.


```C++
// extern RECT rSource, rDest; 
 
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate( hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE, 
                "sample.avi" ); 
            break; 
        case IDM_CROPIMAGE:                          // crops image 
            MCIWndGetSource(g_hwndMCIWnd, &rSource); // source rectangle
            rDest.left = rSource.left +              // new boundaries
                ((rSource.right - rSource.left) / 4); 
            rDest.right = rSource.right - 
                ((rSource.right - rSource.left) / 4); 
            rDest.top = rSource.top + 
                ((rSource.bottom - rSource.top) / 4); 
            rDest.bottom = rSource.bottom - 
                ((rSource.bottom - rSource.top) / 4); 
 
            MCIWndPutSource(g_hwndMCIWnd, &rDest);   // new source rectangle 
    } 
    break; 

    // Handle other messages here. 
```



 

 




