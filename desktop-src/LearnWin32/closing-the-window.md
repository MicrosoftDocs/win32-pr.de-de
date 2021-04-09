---
title: Schließen des Fensters
description: Wenn der Benutzer ein Fenster schließt, löst diese Aktion eine Sequenz von Fenster Meldungen aus.
ms.assetid: f0449f11-0569-4a3a-92bc-bced7e0db516
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6422966d6b0351654632a1c77b7ebf07e2b5ffef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858260"
---
# <a name="closing-the-window"></a><span data-ttu-id="99356-103">Schließen des Fensters</span><span class="sxs-lookup"><span data-stu-id="99356-103">Closing the Window</span></span>

<span data-ttu-id="99356-104">Wenn der Benutzer ein Fenster schließt, löst diese Aktion eine Sequenz von Fenster Meldungen aus.</span><span class="sxs-lookup"><span data-stu-id="99356-104">When the user closes a window, that action triggers a sequence of window messages.</span></span>

<span data-ttu-id="99356-105">Der Benutzer kann ein Anwendungsfenster schließen, indem er auf die Schaltfläche **Schließen** klickt oder eine Tastenkombination wie Alt + F4 verwendet.</span><span class="sxs-lookup"><span data-stu-id="99356-105">The user can close an application window by clicking the **Close** button, or by using a keyboard shortcut such as ALT+F4.</span></span> <span data-ttu-id="99356-106">Jede dieser Aktionen bewirkt, dass das Fenster eine " [**WM \_ Close**](/windows/desktop/winmsg/wm-close) "-Meldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="99356-106">Any of these actions causes the window to receive a [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close) message.</span></span> <span data-ttu-id="99356-107">Die " **WM \_ Close** "-Meldung bietet Ihnen die Möglichkeit, den Benutzer vor dem Schließen des Fensters aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="99356-107">The **WM\_CLOSE** message gives you an opportunity to prompt the user before closing the window.</span></span> <span data-ttu-id="99356-108">Wenn Sie das Fenster wirklich schließen möchten, können Sie die Funktion " [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) " aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="99356-108">If you really do want to close the window, call the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function.</span></span> <span data-ttu-id="99356-109">Andernfalls wird von der " **WM \_ Close** "-Nachricht einfach NULL zurückgegeben, und das Betriebssystem ignoriert die Meldung und zerstört das Fenster nicht.</span><span class="sxs-lookup"><span data-stu-id="99356-109">Otherwise, simply return zero from the **WM\_CLOSE** message, and the operating system will ignore the message and not destroy the window.</span></span>

<span data-ttu-id="99356-110">Im folgenden finden Sie ein Beispiel dafür, wie ein Programm die [**WM- \_ Schließung**](/windows/desktop/winmsg/wm-close)behandeln kann.</span><span class="sxs-lookup"><span data-stu-id="99356-110">Here is an example of how a program might handle [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close).</span></span>

```C++
case WM_CLOSE:
    if (MessageBox(hwnd, L"Really quit?", L"My application", MB_OKCANCEL) == IDOK)
    {
        DestroyWindow(hwnd);
    }
    // Else: User canceled. Do nothing.
    return 0;
```

<span data-ttu-id="99356-111">In diesem Beispiel zeigt die [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) -Funktion ein modales Dialogfeld, das die Schaltflächen **OK** und **Abbrechen** enthält.</span><span class="sxs-lookup"><span data-stu-id="99356-111">In this example, the [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) function shows a modal dialog that contains **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="99356-112">Wenn der Benutzer auf **OK** klickt, ruft das Programm [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow)auf.</span><span class="sxs-lookup"><span data-stu-id="99356-112">If the user clicks **OK**, the program calls [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow).</span></span> <span data-ttu-id="99356-113">Wenn der Benutzer andernfalls auf **Abbrechen** klickt, wird der-Befehl von **DestroyWindow** übersprungen, und das Fenster bleibt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="99356-113">Otherwise, if the user clicks **Cancel**, the call to **DestroyWindow** is skipped, and the window remains open.</span></span> <span data-ttu-id="99356-114">Geben Sie in beiden Fällen NULL zurück, um anzugeben, dass Sie die Nachricht behandelt haben.</span><span class="sxs-lookup"><span data-stu-id="99356-114">In either case, return zero to indicate that you handled the message.</span></span>

<span data-ttu-id="99356-115">Wenn Sie das Fenster schließen möchten, ohne den Benutzer aufzufordern, können Sie einfach " [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) " ohne den Befehl " [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox)" aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="99356-115">If you want to close the window without prompting the user, you could simply call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) without the call to [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).</span></span> <span data-ttu-id="99356-116">In diesem Fall gibt es jedoch eine Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="99356-116">However, there is a shortcut in this case.</span></span> <span data-ttu-id="99356-117">Beachten Sie, dass [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die Standardaktion für jede Fenster Meldung ausführt.</span><span class="sxs-lookup"><span data-stu-id="99356-117">Recall that [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) executes the default action for any window message.</span></span> <span data-ttu-id="99356-118">Im Fall von [**WM \_ Close**](/windows/desktop/winmsg/wm-close)ruft **defwindowproc** automatisch **DestroyWindow** auf.</span><span class="sxs-lookup"><span data-stu-id="99356-118">In the case of [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close), **DefWindowProc** automatically calls **DestroyWindow**.</span></span> <span data-ttu-id="99356-119">Wenn Sie also die " **WM \_ Close** "-Meldung in der **Switch** -Anweisung ignorieren, wird das Fenster standardmäßig zerstört.</span><span class="sxs-lookup"><span data-stu-id="99356-119">That means if you ignore the **WM\_CLOSE** message in your **switch** statement, the window is destroyed by default.</span></span>

<span data-ttu-id="99356-120">Wenn ein Fenster zerstört wird, empfängt es eine WM-Lösch [**Nachricht \_**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="99356-120">When a window is about to be destroyed, it receives a [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span> <span data-ttu-id="99356-121">Diese Meldung wird gesendet, nachdem das Fenster aus dem Bildschirm entfernt wurde, jedoch bevor die Zerstörung erfolgt (insbesondere vor dem Löschen von untergeordneten Fenstern).</span><span class="sxs-lookup"><span data-stu-id="99356-121">This message is sent after the window is removed from the screen, but before the destruction occurs (in particular, before any child windows are destroyed).</span></span>

<span data-ttu-id="99356-122">In Ihrem Hauptanwendungsfenster Antworten Sie in der Regel auf die [**WM- \_ Zerstörung**](/windows/desktop/winmsg/wm-destroy) , indem Sie [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="99356-122">In your main application window, you will typically respond to [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) by calling [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).</span></span>

```C++
case WM_DESTROY:
    PostQuitMessage(0);
    return 0;
```

<span data-ttu-id="99356-123">Wir haben im Abschnitt " [Fenster Meldungen](window-messages.md) " gesehen, dass [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) eine WM-Beendigungs Nachricht in der Nachrichten Warteschlange einfügt, wodurch die Nachrichten Schleife beendet wird. [**\_**](/windows/desktop/winmsg/wm-quit)</span><span class="sxs-lookup"><span data-stu-id="99356-123">We saw in the [Window Messages](window-messages.md) section that [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) puts a [**WM\_QUIT**](/windows/desktop/winmsg/wm-quit) message on the message queue, causing the message loop to end.</span></span>

<span data-ttu-id="99356-124">Hier sehen Sie ein Flussdiagramm, das die typische Methode zum Verarbeiten von " [**WM \_ Close**](/windows/desktop/winmsg/wm-close) "-und " [**WM \_**](/windows/desktop/winmsg/wm-destroy) :</span><span class="sxs-lookup"><span data-stu-id="99356-124">Here is a flow chart showing the typical way to process [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close) and [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) messages:</span></span>

![Flussdiagramm zur Behandlung von WM \- -Schließen-und WM-Lösch \- Meldungen](images/wmclose01.png)

## <a name="next"></a><span data-ttu-id="99356-126">Nächste</span><span class="sxs-lookup"><span data-stu-id="99356-126">Next</span></span>

[<span data-ttu-id="99356-127">Managing Application State (Verwalten eines Anwendungszustands)</span><span class="sxs-lookup"><span data-stu-id="99356-127">Managing Application State</span></span>](managing-application-state-.md)