---
title: Zuschneiden eines Bilds
description: Zuschneiden eines Bilds
ms.assetid: 6600751c-d4b6-481d-bf69-be2d34244c05
keywords:
- Mciwndgetsource-Makro
- Mciwndputsource-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d73eb37792c124ad907f660d4b906ca80e715d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471189"
---
# <a name="cropping-an-image"></a>Zuschneiden eines Bilds

Im folgenden Beispiel wird ein mciwnd-Fenster erstellt und eine AVI-Datei geladen. Das Fenster enthält einen Befehl zum Zuschneiden im Menü, das eine Viertel der Höhe oder Breite von jeder der vier Seiten des Frames aufbindet. Im Beispiel werden die aktuellen (anfänglichen) Dimensionen des Quell Rechtecks mithilfe des [**mciwndgetsource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) -Makros abgerufen. Das geänderte Quell Rechteck ist die Hälfte der ursprünglichen Höhe und Breite und wird im ursprünglichen Frame zentriert. Der-Befehl zum [**mciwndputsource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) -Makro definiert die Koordinaten des Quell Rechtecks neu.


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



 

 




