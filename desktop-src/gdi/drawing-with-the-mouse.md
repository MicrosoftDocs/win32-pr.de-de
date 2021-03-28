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
# <a name="drawing-with-the-mouse"></a><span data-ttu-id="586a7-103">Zeichnen mit der Maus</span><span class="sxs-lookup"><span data-stu-id="586a7-103">Drawing with the Mouse</span></span>

<span data-ttu-id="586a7-104">Sie können es Benutzern ermöglichen, Linien mit der Maus zu zeichnen, indem Sie während der Verarbeitung der [**WM- \_ MouseMove**](../inputdev/wm-mousemove.md) -Nachricht die Fenster Prozedur zeichnen.</span><span class="sxs-lookup"><span data-stu-id="586a7-104">You can permit the user to draw lines with the mouse by having your window procedure draw while processing the [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) message.</span></span> <span data-ttu-id="586a7-105">Das System sendet die **WM- \_ mousetmove** -Meldung an die Fenster Prozedur, wenn der Benutzer den Cursor innerhalb des Fensters verschiebt.</span><span class="sxs-lookup"><span data-stu-id="586a7-105">The system sends the **WM\_MOUSEMOVE** message to the window procedure whenever the user moves the cursor within the window.</span></span> <span data-ttu-id="586a7-106">Zum Zeichnen von Linien kann die Fenster Prozedur einen Anzeigegeräte Kontext abrufen und eine Linie im Fenster zwischen der aktuellen und der vorherigen Cursorposition zeichnen.</span><span class="sxs-lookup"><span data-stu-id="586a7-106">To draw lines, the window procedure can retrieve a display device context and draw a line in the window between the current and previous cursor positions.</span></span>

<span data-ttu-id="586a7-107">Im folgenden Beispiel bereitet die Fenster Prozedur das Zeichnen vor, wenn der Benutzer die linke Maustaste drückt (und die [**WM- \_ lbuttondown**](../inputdev/wm-lbuttondown.md) -Meldung sendet).</span><span class="sxs-lookup"><span data-stu-id="586a7-107">In the following example, the window procedure prepares for drawing when the user presses and holds the left mouse button (sending the [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message).</span></span> <span data-ttu-id="586a7-108">Wenn der Benutzer den Cursor innerhalb des Fensters bewegt, empfängt die Fenster Prozedur eine Reihe von [**WM- \_ mousetmove**](../inputdev/wm-mousemove.md) -Meldungen.</span><span class="sxs-lookup"><span data-stu-id="586a7-108">As the user moves the cursor within the window, the window procedure receives a series of [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) messages.</span></span> <span data-ttu-id="586a7-109">Für jede Nachricht zeichnet die Fenster Prozedur eine Linie, die die vorherige Position und die aktuelle Position verbindet.</span><span class="sxs-lookup"><span data-stu-id="586a7-109">For each message, the window procedure draws a line connecting the previous position and the current position.</span></span> <span data-ttu-id="586a7-110">Zum Zeichnen der Linie verwendet die Prozedur [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) zum Abrufen eines Anzeigegeräte Kontexts. Sobald das Zeichnen beendet ist und die Nachricht vor der Rückgabe von der Nachricht zurückgegeben wird, verwendet die Prozedur die [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) -Funktion, um den Anzeigegeräte kontextfrei zugeben.</span><span class="sxs-lookup"><span data-stu-id="586a7-110">To draw the line, the procedure uses [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) to retrieve a display device context; then, as soon as drawing is complete and before returning from the message, the procedure uses the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) function to release the display device context.</span></span> <span data-ttu-id="586a7-111">Sobald der Benutzer die Maustaste loslässt, löscht die Fenster Prozedur das-Flag, und die Zeichnung wird beendet (wodurch die [**WM \_ lbuttonup**](../inputdev/wm-lbuttonup.md) -Meldung gesendet wird).</span><span class="sxs-lookup"><span data-stu-id="586a7-111">As soon as the user releases the mouse button, the window procedure clears the flag, and the drawing stops (which sends the [**WM\_LBUTTONUP**](../inputdev/wm-lbuttonup.md) message).</span></span>


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



<span data-ttu-id="586a7-112">Eine Anwendung, die das Zeichnen ermöglicht, wie in diesem Beispiel, zeichnet in der Regel entweder die Punkte oder Zeilen auf, sodass die Zeilen neu gezeichnet werden können, wenn das Fenster aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="586a7-112">An application that enables drawing, as in this example, typically records either the points or lines so that the lines can be redrawn whenever the window is updated.</span></span> <span data-ttu-id="586a7-113">Zeichen Anwendungen verwenden häufig einen Speichergeräte Kontext und eine zugeordnete Bitmap zum Speichern von Linien, die mit einer Maus gezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="586a7-113">Drawing applications often use a memory device context and an associated bitmap to store lines that were drawn by using a mouse.</span></span>

 

 
