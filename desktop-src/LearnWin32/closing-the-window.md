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
# <a name="closing-the-window"></a>Schließen des Fensters

Wenn der Benutzer ein Fenster schließt, löst diese Aktion eine Sequenz von Fenster Meldungen aus.

Der Benutzer kann ein Anwendungsfenster schließen, indem er auf die Schaltfläche **Schließen** klickt oder eine Tastenkombination wie Alt + F4 verwendet. Jede dieser Aktionen bewirkt, dass das Fenster eine " [**WM \_ Close**](/windows/desktop/winmsg/wm-close) "-Meldung empfängt. Die " **WM \_ Close** "-Meldung bietet Ihnen die Möglichkeit, den Benutzer vor dem Schließen des Fensters aufzufordern. Wenn Sie das Fenster wirklich schließen möchten, können Sie die Funktion " [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) " aufzurufen. Andernfalls wird von der " **WM \_ Close** "-Nachricht einfach NULL zurückgegeben, und das Betriebssystem ignoriert die Meldung und zerstört das Fenster nicht.

Im folgenden finden Sie ein Beispiel dafür, wie ein Programm die [**WM- \_ Schließung**](/windows/desktop/winmsg/wm-close)behandeln kann.

```C++
case WM_CLOSE:
    if (MessageBox(hwnd, L"Really quit?", L"My application", MB_OKCANCEL) == IDOK)
    {
        DestroyWindow(hwnd);
    }
    // Else: User canceled. Do nothing.
    return 0;
```

In diesem Beispiel zeigt die [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) -Funktion ein modales Dialogfeld, das die Schaltflächen **OK** und **Abbrechen** enthält. Wenn der Benutzer auf **OK** klickt, ruft das Programm [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow)auf. Wenn der Benutzer andernfalls auf **Abbrechen** klickt, wird der-Befehl von **DestroyWindow** übersprungen, und das Fenster bleibt geöffnet. Geben Sie in beiden Fällen NULL zurück, um anzugeben, dass Sie die Nachricht behandelt haben.

Wenn Sie das Fenster schließen möchten, ohne den Benutzer aufzufordern, können Sie einfach " [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) " ohne den Befehl " [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox)" aufzurufen. In diesem Fall gibt es jedoch eine Verknüpfung. Beachten Sie, dass [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die Standardaktion für jede Fenster Meldung ausführt. Im Fall von [**WM \_ Close**](/windows/desktop/winmsg/wm-close)ruft **defwindowproc** automatisch **DestroyWindow** auf. Wenn Sie also die " **WM \_ Close** "-Meldung in der **Switch** -Anweisung ignorieren, wird das Fenster standardmäßig zerstört.

Wenn ein Fenster zerstört wird, empfängt es eine WM-Lösch [**Nachricht \_**](/windows/desktop/winmsg/wm-destroy) . Diese Meldung wird gesendet, nachdem das Fenster aus dem Bildschirm entfernt wurde, jedoch bevor die Zerstörung erfolgt (insbesondere vor dem Löschen von untergeordneten Fenstern).

In Ihrem Hauptanwendungsfenster Antworten Sie in der Regel auf die [**WM- \_ Zerstörung**](/windows/desktop/winmsg/wm-destroy) , indem Sie [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage)aufrufen.

```C++
case WM_DESTROY:
    PostQuitMessage(0);
    return 0;
```

Wir haben im Abschnitt " [Fenster Meldungen](window-messages.md) " gesehen, dass [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) eine WM-Beendigungs Nachricht in der Nachrichten Warteschlange einfügt, wodurch die Nachrichten Schleife beendet wird. [**\_**](/windows/desktop/winmsg/wm-quit)

Hier sehen Sie ein Flussdiagramm, das die typische Methode zum Verarbeiten von " [**WM \_ Close**](/windows/desktop/winmsg/wm-close) "-und " [**WM \_**](/windows/desktop/winmsg/wm-destroy) :

![Flussdiagramm zur Behandlung von WM \- -Schließen-und WM-Lösch \- Meldungen](images/wmclose01.png)

## <a name="next"></a>Nächste

[Managing Application State (Verwalten eines Anwendungszustands)](managing-application-state-.md)