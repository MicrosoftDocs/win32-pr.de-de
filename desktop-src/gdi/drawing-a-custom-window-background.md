---
description: Sie können Ihren eigenen Fenster Hintergrund zeichnen, anstatt das System für Sie zu zeichnen.
ms.assetid: 72a342dc-2766-4ec9-b4c6-5ac3c550ea25
title: Zeichnen eines benutzerdefinierten Fenster Hintergrunds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437a88bec680a6f35e84f5444fc90a45f98da533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978649"
---
# <a name="drawing-a-custom-window-background"></a>Zeichnen eines benutzerdefinierten Fenster Hintergrunds

Sie können Ihren eigenen Fenster Hintergrund zeichnen, anstatt das System für Sie zu zeichnen. Die meisten Anwendungen geben ein Pinsel handle oder einen System Farbwert für den klassenhintergrund Pinsel beim Registrieren der Fenster Klasse an. Das System verwendet den Pinsel oder die Farbe zum Zeichnen des Hintergrunds. Wenn Sie den klassenhintergrund Pinsel jedoch auf **null** festlegen, sendet das System immer dann eine [**WM- \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md) -Meldung an die Fenster Prozedur, wenn der Hintergrund des Fensters gezeichnet werden muss, sodass Sie einen benutzerdefinierten Hintergrund zeichnen können.

Im folgenden Beispiel zeichnet die Fenster Prozedur ein großes Prüf Board-Muster, das sauber in das Fenster passt. Die Prozedur füllt den Client Bereich mit einem weißen Pinsel und zeichnet dann 13 20-bis-20 Rechtecke mit einem grauen Pinsel. Der Anzeigegeräte Kontext, der beim Zeichnen des Hintergrunds verwendet werden soll, wird im *wParam* -Parameter für die Nachricht angegeben.


```C++
HBRUSH hbrWhite, hbrGray; 
 
  . 
  . 
  . 
 
case WM_CREATE: 
    hbrWhite = GetStockObject(WHITE_BRUSH); 
    hbrGray  = GetStockObject(GRAY_BRUSH); 
    return 0L; 
 
case WM_ERASEBKGND: 
    hdc = (HDC) wParam; 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    FillRect(hdc, &rc, hbrWhite); 
 
    for (i = 0; i < 13; i++) 
    { 
        x = (i * 40) % 100; 
        y = ((i * 40) / 100) * 20; 
        SetRect(&rc, x, y, x + 20, y + 20); 
        FillRect(hdc, &rc, hbrGray); 
    } 
  return 1L; 
```



Wenn die Anwendung ein eigenes minimiertes Fenster zeichnet, sendet das System auch die " [**WM \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md) "-Meldung an die Fenster Prozedur, um den Hintergrund für das minimierte Fenster zu zeichnen. Sie können das gleiche Verfahren verwenden, das von [**WM \_ Paint**](wm-paint.md) verwendet wird, um zu bestimmen, ob das Fenster minimiert ist, und die Funktion [**isienic**](/windows/win32/api/winuser/nf-winuser-isiconic) aufzurufen und den Rückgabewert **true** zu überprüfen.

 

 
