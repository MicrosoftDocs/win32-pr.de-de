---
description: Sie können dem Benutzer erlauben, Zeilen mit der Maus zu zeichnen, indem Sie ihre Fensterprozedur zeichnen lassen, während die WM \_ MOUSEMOVE-Nachricht verarbeitet wird.
ms.assetid: 5e8a54b6-05cc-4446-b82e-2b3e550d780a
title: Zeichnen mit der Maus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de7c75c768dcdd330e04a0877bacf59b63d59a6eeb9707011faff6a6b15055c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118250402"
---
# <a name="drawing-with-the-mouse"></a>Zeichnen mit der Maus

Sie können dem Benutzer erlauben, Zeilen mit der Maus zu zeichnen, indem Sie ihre Fensterprozedur zeichnen lassen, während die [**WM \_ MOUSEMOVE-Nachricht**](../inputdev/wm-mousemove.md) verarbeitet wird. Das System sendet die **WM \_ MOUSEMOVE-Nachricht** an die Fensterprozedur, wenn der Benutzer den Cursor innerhalb des Fensters bewegt. Um Linien zu zeichnen, kann die Fensterprozedur einen Anzeigegerätekontext abrufen und eine Linie im Fenster zwischen der aktuellen und der vorherigen Cursorposition zeichnen.

Im folgenden Beispiel bereitet sich die Fensterprozedur auf das Zeichnen vor, wenn der Benutzer drückt und die linke Maustaste gedrückt hält (senden der [**\_ WM-LBUTTONDOWN-Nachricht).**](../inputdev/wm-lbuttondown.md) Wenn der Benutzer den Cursor innerhalb des Fensters bewegt, empfängt die Fensterprozedur eine Reihe von [**WM \_ MOUSEMOVE-Meldungen.**](../inputdev/wm-mousemove.md) Für jede Nachricht zeichnet die Fensterprozedur eine Linie, die die vorherige Position und die aktuelle Position verbindet. Zum Zeichnen der Linie verwendet die Prozedur [**GetDC,**](/windows/desktop/api/Winuser/nf-winuser-getdc) um einen Anzeigegerätekontext abzurufen. sobald das Zeichnen abgeschlossen ist und bevor die Nachricht zurückgegeben wird, verwendet das Verfahren die [**ReleaseDC-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-releasedc) um den Anzeigegerätekontext freizugeben. Sobald der Benutzer die Maustaste loslässt, löscht die Fensterprozedur das Flag, und die Zeichnung wird angehalten (wodurch die [**\_ WM-LBUTTONUP-Nachricht**](../inputdev/wm-lbuttonup.md) gesendet wird).


```C++
BOOL fDraw = FALSE; 
POINT ptPrevious; 
 
  . 
  . 
  . 
 
case WM_LBUTTONDOWN: 
    fDraw = TRUE; 
    ptPrevious.x = LOWORD(lParam); 
    ptPrevious.y = HIWORD(lParam); 
    return 0L; 
 
case WM_LBUTTONUP: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, LOWORD(lParam), HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    fDraw = FALSE; 
    return 0L; 
 
case WM_MOUSEMOVE: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, ptPrevious.x = LOWORD(lParam), 
          ptPrevious.y = HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    return 0L; 
```



Eine Anwendung, die das Zeichnen wie in diesem Beispiel ermöglicht, zeichnet in der Regel entweder die Punkte oder Linien auf, sodass die Zeilen bei jeder Aktualisierung des Fensters neu gezeichnet werden können. Zeichnungsanwendungen verwenden häufig einen Speichergerätekontext und eine zugeordnete Bitmap, um Linien zu speichern, die mithilfe einer Maus gezeichnet wurden.

 

 
