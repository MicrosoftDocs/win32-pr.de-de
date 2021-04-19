---
description: Unterklassen sind eine Technik, die es einer Anwendung ermöglicht, Nachrichten abzufangen und zu verarbeiten, die an ein bestimmtes Fenster gesendet oder an ein bestimmtes Fenster gesendet werden, bevor eine Fenster Prozedur Sie verarbeiten kann.
ms.assetid: 6f7ee9ff-479d-4cb0-8de1-1c3b671551f9
title: Unterklassen und automatische Nachrichten Übersetzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7f0aebabe4bde259a982152327ce61a14de915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357898"
---
# <a name="subclassing-and-automatic-message-translation"></a>Unterklassen und automatische Nachrichten Übersetzung

Unterklassen sind eine Technik, die es einer Anwendung ermöglicht, Nachrichten abzufangen und zu verarbeiten, die an ein bestimmtes Fenster gesendet oder an ein bestimmtes Fenster gesendet werden, bevor eine Fenster Prozedur Sie verarbeiten kann. Das Betriebssystem übersetzt Nachrichten automatisch in [Windows (ANSI)-Codepage](code-pages.md) oder [Unicode](unicode.md) -Formular, abhängig von der Form der Funktion, die die Fenster Prozedur untergeordnet ist.

Der folgende aufrufsvorgang der [**setwindowlonga**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) -Funktion Unterklassen der aktuellen Fenster Prozedur, die dem durch den *HWND* -Parameter identifizierten Fenster zugeordnet ist. Alternativ kann eine Anwendung [**setwindowlongptra**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)verwenden. Die neue Fenster Prozedur **newwndproc** empfängt Nachrichten mit Text im Windows-Codepage-Format.


```C++
OldWndProc = (WNDPROC) SetWindowLongA(hWnd,
             GWL_WNDPROC, (LONG)NewWndProc); 
```



Wenn **newwndproc** die Verarbeitung einer Nachricht abgeschlossen hat, verwendet Sie die [**callwindowproc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) -Funktion wie folgt, um die Nachricht an **oldwndproc** zu übergeben.


```C++
CallWindowProc(OldWndProc, hWnd, uMessage, wParam, lParam);
```



Wenn **oldwndproc** mit einem Klassen Stil von Unicode erstellt wurde, werden Nachrichten aus dem Windows-Codepage-Formular übersetzt, das von **newwndproc** in Unicode empfangen wurde.

Entsprechend wird durch einen Aufrufen der Funktion " [**setwindowlongw**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) " oder " [**setwindowlongptrw**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) " die aktuelle Fenster Prozedur mit einer Fenster Prozedur Unterklassen, die Unicode-Textnachrichten erwartet. Die Nachrichten Übersetzung erfolgt bei Bedarf während der Verarbeitung der [**callwindowproc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) -Funktion.

Weitere Informationen zu Unterklassen finden Sie unter [Fenster Prozeduren](../winmsg/window-procedures.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Unicode und Zeichensätzen](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
