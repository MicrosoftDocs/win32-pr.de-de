---
title: Schreiben der Fensterprozedur
description: Schreiben der Fensterprozedur
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832aba88211a7decf20c233f5d9ab4fbeb1b1c27
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105718"
---
# <a name="writing-the-window-procedure"></a>Schreiben der Fensterprozedur

Die [**DispatchMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) ruft die Fensterprozedur des Fensters auf, das das Ziel der Nachricht ist. Die Fensterprozedur weist die folgende Signatur auf.

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

Es gibt vier Parameter:

- *hwnd* ist ein Handle für das Fenster.
- *uMsg* ist der Nachrichtencode. Beispielsweise gibt die [**WM \_ SIZE-Meldung**](/windows/desktop/winmsg/wm-size) an, dass die Größe des Fensters geändert wurde.
- *wParam* und *lParam* enthalten zusätzliche Daten, die sich auf die Nachricht beziehen. Die genaue Bedeutung hängt vom Nachrichtencode ab.

**LRESULT** ist ein ganzzahliger Wert, den Ihr Programm an Windows zurückgibt. Sie enthält die Antwort Ihres Programms auf eine bestimmte Nachricht. Die Bedeutung dieses Werts hängt vom Nachrichtencode ab. **CALLBACK** ist die Aufrufkonvention für die Funktion.

Eine typische Fensterprozedur ist einfach eine große switch-Anweisung, die den Nachrichtencode einschaltet. Fügen Sie Fälle für jede Nachricht hinzu, die Sie behandeln möchten.

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

Zusätzliche Daten für die Nachricht sind in den *Parametern lParam* und *wParam* enthalten. Beide Parameter sind ganzzahlige Werte der Größe einer Zeigerbreite (32 Bits oder 64 Bits). Die Bedeutung der einzelnen Hängt vom Nachrichtencode *(uMsg*) ab. Für jede Nachricht müssen Sie den Nachrichtencode auf MSDN suchen und die Parameter in den richtigen Datentyp umschreiben. In der Regel sind die Daten entweder ein numerischer Wert oder ein Zeiger auf eine Struktur. Einige Nachrichten enthalten keine Daten.

In der Dokumentation für die [**WM \_ SIZE-Meldung**](/windows/desktop/winmsg/wm-size) wird beispielsweise Folgendes angezeigt:

- *wParam ist* ein Flag, das angibt, ob das Fenster minimiert, maximiert oder die Größe geändert wurde.
- *lParam* enthält die neue Breite und Höhe des Fensters als 16-Bit-Werte, die in eine 32- oder 64-Bit-Zahl gepackt sind. Sie müssen einige Bitverschiebungen durchführen, um diese Werte zu erhalten. Glücklicherweise enthält die Headerdatei WinDef.h Hilfsmakros, die dies tun.

Eine typische Fensterprozedur verarbeitet Dutzende von Nachrichten, sodass sie sehr lang werden kann. Eine Möglichkeit, Ihren Code modularer zu machen, besteht in der Logik für die Behandlung jeder Nachricht in einer separaten Funktion. Geben Sie in der Fensterprozedur die *Parameter wParam* und *lParam* in den richtigen Datentyp um, und übergeben Sie diese Werte an die Funktion. Um beispielsweise die WM [**\_ SIZE-Meldung zu**](/windows/desktop/winmsg/wm-size) verarbeiten, sieht die Fensterprozedur wie die folgende aus:

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_SIZE:
        {
            int width = LOWORD(lParam);  // Macro to get the low-order word.
            int height = HIWORD(lParam); // Macro to get the high-order word.

            // Respond to the message:
            OnSize(hwnd, (UINT)wParam, width, height);
        }
        break;
    }
}

void OnSize(HWND hwnd, UINT flag, int width, int height)
{
    // Handle resizing
}
```

Die [**MAKROs LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) und [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) erhalten die Werte für Breite und Höhe von 16 Bit aus *lParam.* (Sie können diese Art von Details in der MSDN-Dokumentation für jeden Meldungscode nachschauen.) Die Fensterprozedur extrahiert die Breite und Höhe und übergibt diese Werte dann an die `OnSize` Funktion.

## <a name="default-message-handling"></a>Standardnachrichtenbehandlung

Wenn Sie eine bestimmte Nachricht in Ihrer Fensterprozedur nicht verarbeiten, übergeben Sie die Nachrichtenparameter direkt an die [**DefWindowProc-Funktion.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Diese Funktion führt die Standardaktion für die Nachricht aus, die je nach Nachrichtentyp variiert.

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a>Vermeiden von Engpässen in der Fensterprozedur

Während die Fensterprozedur ausgeführt wird, werden alle anderen Meldungen für Fenster blockiert, die im selben Thread erstellt wurden. Vermeiden Sie daher eine lange Verarbeitung innerhalb der Fensterprozedur. Angenommen, Ihr Programm öffnet eine TCP-Verbindung und wartet unbegrenzt, bis der Server antwortet. Wenn Sie dies innerhalb der Fensterprozedur tun, antwortet Die Benutzeroberfläche erst, wenn die Anforderung abgeschlossen ist. Während dieser Zeit kann das Fenster keine Maus- oder Tastatureingaben verarbeiten, sich selbst neu malen oder sogar schließen.

Stattdessen sollten Sie die Arbeit in einen anderen Thread verschieben, indem Sie eine der in Windows integrierten Multitasking-Einrichtungen verwenden:

- Erstellen Sie einen neuen Thread.
- Verwenden von Threadpools.
- Verwenden Sie asynchrone E/A-Aufrufe.
- Verwenden Sie asynchrone Prozeduraufrufe.

## <a name="next"></a>Nächste

[Zeichnen des Fensters](painting-the-window.md)
