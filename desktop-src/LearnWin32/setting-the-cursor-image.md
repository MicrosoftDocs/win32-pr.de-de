---
title: Festlegen des Cursor Bilds
description: Festlegen des Cursor Bilds
ms.assetid: FB223131-19AE-41DD-87DE-73992AE2A0CA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3bc993b7566dee1fa47bd2b53c270ad0e4f64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472893"
---
# <a name="setting-the-cursor-image"></a><span data-ttu-id="e04fb-103">Festlegen des Cursor Bilds</span><span class="sxs-lookup"><span data-stu-id="e04fb-103">Setting the Cursor Image</span></span>

<span data-ttu-id="e04fb-104">Der *Cursor* ist das kleine Bild, das die Position der Maus oder eines anderen Zeige Geräts anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e04fb-104">The *cursor* is the small image that shows the location of the mouse or other pointing device.</span></span> <span data-ttu-id="e04fb-105">Viele Anwendungen ändern das Cursor Bild, um dem Benutzer Feedback zu geben.</span><span class="sxs-lookup"><span data-stu-id="e04fb-105">Many applications change the cursor image to give feedback to the user.</span></span> <span data-ttu-id="e04fb-106">Obwohl es nicht erforderlich ist, wird Ihrer Anwendung ein gutes Paar von Polnisch hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e04fb-106">Although it is not required, it adds a nice bit of polish to your application.</span></span>

<span data-ttu-id="e04fb-107">Windows stellt eine Reihe von Standard Cursor Images bereit, die als *System Cursor* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="e04fb-107">Windows provides a set of standard cursor images, called *system cursors*.</span></span> <span data-ttu-id="e04fb-108">Diese umfassen den Pfeil, die Hand, den I-Beam, den Sanduhr (der jetzt ein drehende Kreis ist) und andere.</span><span class="sxs-lookup"><span data-stu-id="e04fb-108">These include the arrow, the hand, the I-beam, the hourglass (which is now a spinning circle), and others.</span></span> <span data-ttu-id="e04fb-109">In diesem Abschnitt wird die Verwendung der systemcursorn beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e04fb-109">This section describes how to use the system cursors.</span></span> <span data-ttu-id="e04fb-110">Erweiterte Aufgaben, wie das Erstellen von benutzerdefinierten Cursorn, finden Sie unter [Cursors](/windows/desktop/menurc/cursors).</span><span class="sxs-lookup"><span data-stu-id="e04fb-110">For more advanced tasks, such as creating custom cursors, see [Cursors](/windows/desktop/menurc/cursors).</span></span>

<span data-ttu-id="e04fb-111">Sie können einen Cursor einer Fenster Klasse zuordnen, indem Sie den **hcursor** -Member der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -oder [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur festlegen.</span><span class="sxs-lookup"><span data-stu-id="e04fb-111">You can associate a cursor with a window class by setting the **hCursor** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) or [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure.</span></span> <span data-ttu-id="e04fb-112">Andernfalls ist der Standard Cursor der Pfeil.</span><span class="sxs-lookup"><span data-stu-id="e04fb-112">Otherwise, the default cursor is the arrow.</span></span> <span data-ttu-id="e04fb-113">Wenn die Maus über ein Fenster bewegt wird, empfängt das Fenster eine [**WM- \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) -Nachricht (es sei denn, ein anderes Fenster hat die Maus erfasst).</span><span class="sxs-lookup"><span data-stu-id="e04fb-113">When the mouse moves over a window, the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message (unless another window has captured the mouse).</span></span> <span data-ttu-id="e04fb-114">An diesem Punkt tritt eines der folgenden Ereignisse auf:</span><span class="sxs-lookup"><span data-stu-id="e04fb-114">At this point, one of the following events occurs:</span></span>

-   <span data-ttu-id="e04fb-115">Die Anwendung legt den Cursor fest, und die Fenster Prozedur gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="e04fb-115">The application sets the cursor and the window procedure returns **TRUE**.</span></span>
-   <span data-ttu-id="e04fb-116">Die Anwendung führt nichts aus und übergibt [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="e04fb-116">The application does nothing and passes [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="e04fb-117">Zum Festlegen des Cursors führt ein Programm Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="e04fb-117">To set the cursor, a program does the following:</span></span>

1.  <span data-ttu-id="e04fb-118">Ruft [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) auf, um den Cursor in den Arbeitsspeicher zu laden.</span><span class="sxs-lookup"><span data-stu-id="e04fb-118">Calls [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) to load the cursor into memory.</span></span> <span data-ttu-id="e04fb-119">Diese Funktion gibt ein Handle für den Cursor zurück.</span><span class="sxs-lookup"><span data-stu-id="e04fb-119">This function returns a handle to the cursor.</span></span>
2.  <span data-ttu-id="e04fb-120">Ruft [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) auf und übergibt im Cursor handle.</span><span class="sxs-lookup"><span data-stu-id="e04fb-120">Calls [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) and passes in the cursor handle.</span></span>

<span data-ttu-id="e04fb-121">Andernfalls verwendet die **defwindowproc** -Funktion den folgenden Algorithmus zum Festlegen des Cursor Bilds, wenn die Anwendung [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergibt:</span><span class="sxs-lookup"><span data-stu-id="e04fb-121">Otherwise, if the application passes [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the **DefWindowProc** function uses the following algorithm to set the cursor image:</span></span>

1.  <span data-ttu-id="e04fb-122">Wenn das Fenster über ein übergeordnetes Element verfügt, leiten Sie die [**WM- \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) -Meldung an das übergeordnete Element weiter, um</span><span class="sxs-lookup"><span data-stu-id="e04fb-122">If the window has a parent, forward the [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message to the parent to handle.</span></span>
2.  <span data-ttu-id="e04fb-123">Wenn das Fenster über einen Klassen Cursor verfügt, legen Sie den Cursor auf den Klassen Cursor fest.</span><span class="sxs-lookup"><span data-stu-id="e04fb-123">Otherwise, if the window has a class cursor, set the cursor to the class cursor.</span></span>
3.  <span data-ttu-id="e04fb-124">Wenn kein Klassen Cursor vorhanden ist, legen Sie den Cursor auf den Pfeilcursor fest.</span><span class="sxs-lookup"><span data-stu-id="e04fb-124">If there is no class cursor, set the cursor to the arrow cursor.</span></span>

<span data-ttu-id="e04fb-125">Die [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) -Funktion kann entweder einen benutzerdefinierten Cursor aus einer Ressource oder einen der systemcursorn laden.</span><span class="sxs-lookup"><span data-stu-id="e04fb-125">The [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) function can load either a custom cursor from a resource, or one of the system cursors.</span></span> <span data-ttu-id="e04fb-126">Im folgenden Beispiel wird gezeigt, wie der Cursor auf den System Hand Cursor festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e04fb-126">The following example shows how to set the cursor to the system hand cursor.</span></span>


```C++
    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
```



<span data-ttu-id="e04fb-127">Wenn Sie den Cursor ändern, setzt das Cursor Bild bei der nächsten Mausbewegung zurück, es sei denn, Sie fangen die [**WM- \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) -Meldung an und legen den Cursor erneut fest.</span><span class="sxs-lookup"><span data-stu-id="e04fb-127">If you change the cursor, the cursor image resets on the next mouse move, unless you intercept the [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message and set the cursor again.</span></span> <span data-ttu-id="e04fb-128">Der folgende Code zeigt, wie **WM \_ SetCursor** behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="e04fb-128">The following code shows how to handle **WM\_SETCURSOR**.</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



<span data-ttu-id="e04fb-129">Mit diesem Code werden zunächst die unteren 16 Bits von *LPARAM* überprüft.</span><span class="sxs-lookup"><span data-stu-id="e04fb-129">This code first checks the lower 16 bits of *lParam*.</span></span> <span data-ttu-id="e04fb-130">Wenn `LOWORD(lParam)` " **htclient**" ist, bedeutet dies, dass sich der Cursor über dem Client Bereich des Fensters befindet.</span><span class="sxs-lookup"><span data-stu-id="e04fb-130">If `LOWORD(lParam)` equals **HTCLIENT**, it means the cursor is over the client area of the window.</span></span> <span data-ttu-id="e04fb-131">Andernfalls befindet sich der Cursor über dem nicht-Client Bereich.</span><span class="sxs-lookup"><span data-stu-id="e04fb-131">Otherwise, the cursor is over the nonclient area.</span></span> <span data-ttu-id="e04fb-132">Normalerweise sollten Sie nur den Cursor für den Client Bereich festlegen und Windows den Cursor für den nicht-Client Bereich festlegen lassen.</span><span class="sxs-lookup"><span data-stu-id="e04fb-132">Typically, you should only set the cursor for the client area, and let Windows set the cursor for the nonclient area.</span></span>

## <a name="next"></a><span data-ttu-id="e04fb-133">Nächste</span><span class="sxs-lookup"><span data-stu-id="e04fb-133">Next</span></span>

[<span data-ttu-id="e04fb-134">Benutzereingabe: erweitertes Beispiel</span><span class="sxs-lookup"><span data-stu-id="e04fb-134">User Input: Extended Example</span></span>](user-input--extended-example.md)

 

 