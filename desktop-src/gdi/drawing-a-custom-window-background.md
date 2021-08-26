---
description: Sie können Ihren eigenen Fensterhintergrund zeichnen, anstatt das System für Sie zeichnen zu lassen.
ms.assetid: 72a342dc-2766-4ec9-b4c6-5ac3c550ea25
title: Zeichnen eines benutzerdefinierten Fensterhintergrunds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4248f7d7a1ae27ae09c93e95734fd72285028e1185b6d35110e5141fcbf88c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966010"
---
# <a name="drawing-a-custom-window-background"></a>Zeichnen eines benutzerdefinierten Fensterhintergrunds

Sie können Ihren eigenen Fensterhintergrund zeichnen, anstatt das System für Sie zeichnen zu lassen. Die meisten Anwendungen geben beim Registrieren der Fensterklasse einen Pinselhandle oder einen Systemfarbwert für den Hintergrundpinsel der Klasse an. das System verwendet den Pinsel oder die Farbe, um den Hintergrund zu zeichnen. Wenn Sie den Hintergrundpinsel der Klasse auf **NULL** festlegen, sendet das System jedoch immer dann eine [**WM \_ ERASEBKGND-Meldung**](../winmsg/wm-erasebkgnd.md) an Ihre Fensterprozedur, wenn der Fensterhintergrund gezeichnet werden muss, sodass Sie einen benutzerdefinierten Hintergrund zeichnen können.

Im folgenden Beispiel zeichnet die Fensterprozedur ein großes Checkerboardmuster, das gut in das Fenster passt. Die Prozedur füllt den Clientbereich mit einem weißen Pinsel und zeichnet dann 20 mal 20 Rechtecken mit einem grauen Pinsel. Der Anzeigegerätekontext, der beim Zeichnen des Hintergrunds verwendet werden soll, wird im *wParam-Parameter* für die Nachricht angegeben.


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



Wenn die Anwendung ein eigenes minimiertes Fenster zeichnet, sendet das System auch die [**WM \_ ERASEBKGND-Nachricht**](../winmsg/wm-erasebkgnd.md) an die Fensterprozedur, um den Hintergrund für das minimierte Fenster zu zeichnen. Sie können die gleiche Technik verwenden, die von [**WM \_ PAINT**](wm-paint.md) verwendet wird, um zu bestimmen, ob das Fenster minimiert ist, d. h. die [**IsIconic-Funktion**](/windows/win32/api/winuser/nf-winuser-isiconic) aufzurufen und den Rückgabewert **TRUE** zu überprüfen.

 

 
