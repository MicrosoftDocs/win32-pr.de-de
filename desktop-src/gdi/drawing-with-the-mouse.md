---
description: Sie können es Benutzern ermöglichen, Linien mit der Maus zu zeichnen, indem Sie während der Verarbeitung der WM- \_ MouseMove-Nachricht die Fenster Prozedur zeichnen.
ms.assetid: 5e8a54b6-05cc-4446-b82e-2b3e550d780a
title: Zeichnen mit der Maus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ad38e7ef8af5c39918bac7231aea4dde285caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041974"
---
# <a name="drawing-with-the-mouse"></a>Zeichnen mit der Maus

Sie können es Benutzern ermöglichen, Linien mit der Maus zu zeichnen, indem Sie während der Verarbeitung der [**WM- \_ MouseMove**](../inputdev/wm-mousemove.md) -Nachricht die Fenster Prozedur zeichnen. Das System sendet die **WM- \_ mousetmove** -Meldung an die Fenster Prozedur, wenn der Benutzer den Cursor innerhalb des Fensters verschiebt. Zum Zeichnen von Linien kann die Fenster Prozedur einen Anzeigegeräte Kontext abrufen und eine Linie im Fenster zwischen der aktuellen und der vorherigen Cursorposition zeichnen.

Im folgenden Beispiel bereitet die Fenster Prozedur das Zeichnen vor, wenn der Benutzer die linke Maustaste drückt (und die [**WM- \_ lbuttondown**](../inputdev/wm-lbuttondown.md) -Meldung sendet). Wenn der Benutzer den Cursor innerhalb des Fensters bewegt, empfängt die Fenster Prozedur eine Reihe von [**WM- \_ mousetmove**](../inputdev/wm-mousemove.md) -Meldungen. Für jede Nachricht zeichnet die Fenster Prozedur eine Linie, die die vorherige Position und die aktuelle Position verbindet. Zum Zeichnen der Linie verwendet die Prozedur [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) zum Abrufen eines Anzeigegeräte Kontexts. Sobald das Zeichnen beendet ist und die Nachricht vor der Rückgabe von der Nachricht zurückgegeben wird, verwendet die Prozedur die [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) -Funktion, um den Anzeigegeräte kontextfrei zugeben. Sobald der Benutzer die Maustaste loslässt, löscht die Fenster Prozedur das-Flag, und die Zeichnung wird beendet (wodurch die [**WM \_ lbuttonup**](../inputdev/wm-lbuttonup.md) -Meldung gesendet wird).


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



Eine Anwendung, die das Zeichnen ermöglicht, wie in diesem Beispiel, zeichnet in der Regel entweder die Punkte oder Zeilen auf, sodass die Zeilen neu gezeichnet werden können, wenn das Fenster aktualisiert wird. Zeichen Anwendungen verwenden häufig einen Speichergeräte Kontext und eine zugeordnete Bitmap zum Speichern von Linien, die mit einer Maus gezeichnet wurden.

 

 
