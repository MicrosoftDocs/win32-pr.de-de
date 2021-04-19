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
# <a name="subclassing-and-automatic-message-translation"></a><span data-ttu-id="a256a-103">Unterklassen und automatische Nachrichten Übersetzung</span><span class="sxs-lookup"><span data-stu-id="a256a-103">Subclassing and Automatic Message Translation</span></span>

<span data-ttu-id="a256a-104">Unterklassen sind eine Technik, die es einer Anwendung ermöglicht, Nachrichten abzufangen und zu verarbeiten, die an ein bestimmtes Fenster gesendet oder an ein bestimmtes Fenster gesendet werden, bevor eine Fenster Prozedur Sie verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="a256a-104">Subclassing is a technique that allows an application to intercept and process messages sent or posted to a particular window before a window procedure has a chance to process them.</span></span> <span data-ttu-id="a256a-105">Das Betriebssystem übersetzt Nachrichten automatisch in [Windows (ANSI)-Codepage](code-pages.md) oder [Unicode](unicode.md) -Formular, abhängig von der Form der Funktion, die die Fenster Prozedur untergeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a256a-105">The operating system automatically translates messages into [Windows (ANSI) code page](code-pages.md) or [Unicode](unicode.md) form, depending on the form of the function that has subclassed the window procedure.</span></span>

<span data-ttu-id="a256a-106">Der folgende aufrufsvorgang der [**setwindowlonga**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) -Funktion Unterklassen der aktuellen Fenster Prozedur, die dem durch den *HWND* -Parameter identifizierten Fenster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a256a-106">The following call to the [**SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function subclasses the current window procedure associated with the window identified by the *hWnd* parameter.</span></span> <span data-ttu-id="a256a-107">Alternativ kann eine Anwendung [**setwindowlongptra**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)verwenden.</span><span class="sxs-lookup"><span data-stu-id="a256a-107">Alternatively, an application can use [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra).</span></span> <span data-ttu-id="a256a-108">Die neue Fenster Prozedur **newwndproc** empfängt Nachrichten mit Text im Windows-Codepage-Format.</span><span class="sxs-lookup"><span data-stu-id="a256a-108">The new window procedure **NewWndProc**, will receive messages with text in Windows code page format.</span></span>


```C++
OldWndProc = (WNDPROC) SetWindowLongA(hWnd,
             GWL_WNDPROC, (LONG)NewWndProc); 
```



<span data-ttu-id="a256a-109">Wenn **newwndproc** die Verarbeitung einer Nachricht abgeschlossen hat, verwendet Sie die [**callwindowproc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) -Funktion wie folgt, um die Nachricht an **oldwndproc** zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="a256a-109">When **NewWndProc** has finished processing a message, it uses the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function as follows to pass the message to **OldWndProc**.</span></span>


```C++
CallWindowProc(OldWndProc, hWnd, uMessage, wParam, lParam);
```



<span data-ttu-id="a256a-110">Wenn **oldwndproc** mit einem Klassen Stil von Unicode erstellt wurde, werden Nachrichten aus dem Windows-Codepage-Formular übersetzt, das von **newwndproc** in Unicode empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="a256a-110">If **OldWndProc** was created with a class style of UNICODE, messages are translated from the Windows code page form received by **NewWndProc** into Unicode.</span></span>

<span data-ttu-id="a256a-111">Entsprechend wird durch einen Aufrufen der Funktion " [**setwindowlongw**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) " oder " [**setwindowlongptrw**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) " die aktuelle Fenster Prozedur mit einer Fenster Prozedur Unterklassen, die Unicode-Textnachrichten erwartet.</span><span class="sxs-lookup"><span data-stu-id="a256a-111">Similarly, a call to the [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) or [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) function subclasses the current window procedure with a window procedure that expects Unicode text messages.</span></span> <span data-ttu-id="a256a-112">Die Nachrichten Übersetzung erfolgt bei Bedarf während der Verarbeitung der [**callwindowproc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="a256a-112">Message translation, if necessary, is performed during the processing of the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function.</span></span>

<span data-ttu-id="a256a-113">Weitere Informationen zu Unterklassen finden Sie unter [Fenster Prozeduren](../winmsg/window-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="a256a-113">For more information about subclassing, see [Window Procedures](../winmsg/window-procedures.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a256a-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a256a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a256a-115">Verwenden von Unicode und Zeichensätzen</span><span class="sxs-lookup"><span data-stu-id="a256a-115">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
