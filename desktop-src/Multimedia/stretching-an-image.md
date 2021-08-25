---
title: Strecken eines Bilds
description: Strecken eines Bilds
ms.assetid: 7cfd91c3-0ebd-47eb-a33d-c81a66f820e5
keywords:
- MCIWndGetDest-Makro
- MCIWndPutDest-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 283ecc69af3298930b4fb9788a02fb60167483fc10b185dd21e696affe4ee58a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892570"
---
# <a name="stretching-an-image"></a>Strecken eines Bilds

Im folgenden Beispiel werden die Bilder eines Videoclips gestreckt. Sie erhöht die Abmessungen des Zielrechtecks mithilfe des [**MCIWndPutDest-Makros.**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) Die Größe des Wiedergabebereichs bleibt unverändert, sodass das Ergebnis ein verzerrtes, vergrößertes Bild ist. In den Beispielen wird die **MCIWndPutDest-Funktion** verwendet, um das Zielrechteck in Bezug auf den Wiedergabebereich neu zu positionieren und so verschiedene Teile des gestreckten Bilds anzuzeigen.


```C++
extern RECT rCurrent, rDest; 
 
case WM_COMMAND: 
   switch (wParam) 
   { 
       case IDM_CREATEMCIWND: 
           g_hwndMCIWnd = MCIWndCreate(hwnd, 
               g_hinst, 
               WS_CHILD | WS_VISIBLE, 
               "sample.avi"); 
           break; 
 
       case  IDM_STRETCHIMAGE:      // stretch destination RECT 3:2, 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rDest.top = rCurrent.top;               // new boundaries 
           rDest.right = rCurrent.right; 
           rDest.left = rCurrent.left + 
               ((rCurrent.left - rCurrent.right) * 3); 
           rDest.bottom = rCurrent.top + 
               ((rCurrent.bottom - rCurrent.top) * 2); 
           MCIWndPutDest(g_hwndMCIWnd, &rDest); // new destination 
           break; 
       case IDM_MOVEDOWN:           // move toward bottom of image 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.top -= 100;                    // new boundaries 
           rCurrent.bottom -= 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination
           break; 
       case IDM_MOVEUP:             // move toward top of image 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.top += 100;                    // new boundaries 
           rCurrent.bottom += 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
       case IDM_MOVELEFT:           // move toward left edge of image
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.right += 100;                  // new boundaries 
           rCurrent.left += 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
       case  IDM_MOVERIGHT:         // move toward right edge of image
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT
           rCurrent.right -= 100;                  // new boundaries 
           rCurrent.left -= 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
   } 
   break; 
 
   // Handle other messages here. 
```



 

 




