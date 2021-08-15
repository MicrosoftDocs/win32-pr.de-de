---
description: Unterklassen sind eine Technik, die es einer Anwendung ermöglicht, Nachrichten abzufangen und zu verarbeiten, die an ein bestimmtes Fenster gesendet oder an ein bestimmtes Fenster gesendet werden, bevor eine Fensterprozedur diese verarbeiten kann.
ms.assetid: 6f7ee9ff-479d-4cb0-8de1-1c3b671551f9
title: Unterklassen und automatische Nachrichtenübersetzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20147567bb4cd591d31e0da5f08b76a29d0229c9bc345b8c1827fc5350dd62d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390223"
---
# <a name="subclassing-and-automatic-message-translation"></a>Unterklassen und automatische Nachrichtenübersetzung

Unterklassen sind eine Technik, die es einer Anwendung ermöglicht, Nachrichten abzufangen und zu verarbeiten, die an ein bestimmtes Fenster gesendet oder an ein bestimmtes Fenster gesendet werden, bevor eine Fensterprozedur diese verarbeiten kann. Das Betriebssystem übersetzt Nachrichten automatisch in [Windows (ANSI)-Codepage](code-pages.md) oder [Unicode-Formular,](unicode.md) abhängig von der Form der Funktion, die die Fensterprozedur untergliedert hat.

Der folgende Aufruf der [**SetWindowLongA-Funktion**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) untergliedert die aktuelle Fensterprozedur, die dem durch den *hWnd-Parameter* identifizierten Fenster zugeordnet ist. Alternativ kann eine Anwendung [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)verwenden. Die neue Fensterprozedur **NewWndProc** empfängt Nachrichten mit Text im Windows Codepageformat.


```C++
OldWndProc = (WNDPROC) SetWindowLongA(hWnd,
             GWL_WNDPROC, (LONG)NewWndProc); 
```



Wenn **NewWndProc** die Verarbeitung einer Nachricht abgeschlossen hat, wird die [**CallWindowProc-Funktion**](/windows/win32/api/winuser/nf-winuser-callwindowproca) wie folgt verwendet, um die Nachricht an **OldWndProc** zu übergeben.


```C++
CallWindowProc(OldWndProc, hWnd, uMessage, wParam, lParam);
```



Wenn **OldWndProc** mit einem Unicode-Klassenstil erstellt wurde, werden Nachrichten aus dem von **NewWndProc** empfangenen Windows Codepageformular in Unicode übersetzt.

Auf ähnliche Weise wird bei einem Aufruf der [**Funktion SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) oder [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) die aktuelle Fensterprozedur mit einer Fensterprozedur klassifiziert, die Unicode-Textnachrichten erwartet. Die Nachrichtenübersetzung wird bei Bedarf während der Verarbeitung der [**CallWindowProc-Funktion**](/windows/win32/api/winuser/nf-winuser-callwindowproca) ausgeführt.

Weitere Informationen zum Unterklassening finden Sie unter [Window Procedures](../winmsg/window-procedures.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Unicode und Zeichensätzen](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
