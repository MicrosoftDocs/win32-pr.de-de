---
title: Schreiben der Fenster Prozedur
description: .
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f11b22ba5dd0653905ca4e2bdb546d106183fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339480"
---
# <a name="writing-the-window-procedure"></a>Schreiben der Fenster Prozedur

Die [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) -Funktion Ruft die Fenster Prozedur des Fensters auf, das das Ziel der Nachricht ist. Die Fenster Prozedur weist die folgende Signatur auf.

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

Es gibt vier Parameter:

- *HWND* ist ein Handle für das Fenster.
- die *Umschlag* Sequenz ist der Nachrichten Code. Beispielsweise gibt die [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Meldung an, dass die Größe des Fensters angepasst wurde.
- *wParam* und *LPARAM* enthalten zusätzliche Daten, die sich auf die Nachricht beziehen. Die genaue Bedeutung hängt vom Nachrichten Code ab.

**LRESULT** ist ein ganzzahliger Wert, den das Programm an Windows zurückgibt. Sie enthält die Antwort des Programms auf eine bestimmte Nachricht. Die Bedeutung dieses Werts hängt vom Nachrichten Code ab. **Callback** ist die Aufruf Konvention für die Funktion.

Eine typische Fenster Prozedur ist einfach eine große Switch-Anweisung, die den Nachrichten Code schaltet. Fügen Sie für jede zu behandelnde Nachricht Fälle hinzu.

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

Zusätzliche Daten für die Nachricht sind in den *LPARAM* -und *wParam* -Parametern enthalten. Beide Parameter sind ganzzahlige Werte die Größe einer Zeiger Breite (32 Bits oder 64 Bits). Die Bedeutung der einzelnen hängt vom Nachrichten Code (*Umschlag*) ab. Für jede Nachricht müssen Sie den Nachrichten Code auf MSDN suchen und die Parameter in den richtigen Datentyp umwandeln. Normalerweise handelt es sich bei den Daten entweder um einen numerischen Wert oder um einen Zeiger auf eine-Struktur. Einige Nachrichten enthalten keine Daten.

In der Dokumentation für die WM- [**\_ Größe**](/windows/desktop/winmsg/wm-size) wird beispielsweise Folgendes angezeigt:

- *wParam* ist ein Flag, das angibt, ob das Fenster minimiert, maximiert oder verkleinert wurde.
- *LPARAM* enthält die neue Breite und Höhe des Fensters als 16-Bit-Werte, die in 1 32-oder 64-Bit-Zahlen verpackt sind. Sie müssen einige Bitverschiebungen durchführen, um diese Werte zu erhalten. Glücklicherweise enthält die Header Datei WINDEF. h Hilfsmakros, die dies tun.

Eine typische Fenster Prozedur verarbeitet Dutzende von Nachrichten, sodass Sie sehr lange anwachsen kann. Eine Möglichkeit, Ihren Code modularerer zu gestalten, besteht darin, die Logik für die Verarbeitung der einzelnen Nachrichten in einer separaten Funktion zu platzieren. Wandeln Sie in der Fenster Prozedur die *wParam* -und *LPARAM* -Parameter in den richtigen Datentyp um, und übergeben Sie diese Werte an die-Funktion. Um z. b. die [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Meldung zu verarbeiten, würde die Fenster Prozedur wie folgt aussehen:

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

Die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -und [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros erhalten die 16-Bit-Werte für Breite und Höhe von *LPARAM*. (In der MSDN-Dokumentation finden Sie Informationen zu den einzelnen Nachrichten Codes.) Die Fenster Prozedur extrahiert die Breite und Höhe und übergibt diese Werte dann an die `OnSize` Funktion.

## <a name="default-message-handling"></a>Standardmäßige Nachrichten Behandlung

Wenn Sie eine bestimmte Nachricht in der Fenster Prozedur nicht verarbeiten, übergeben Sie die Nachrichten Parameter direkt an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion. Diese Funktion führt die Standardaktion für die Nachricht aus, die je nach Nachrichtentyp variiert.

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a>Vermeiden von Engpässen in der Fenster Prozedur

Während die Fenster Prozedur ausgeführt wird, werden alle anderen Nachrichten für Windows, die im gleichen Thread erstellt wurden, blockiert. Vermeiden Sie daher eine lange Verarbeitung in der Fenster Prozedur. Angenommen, das Programm öffnet eine TCP-Verbindung und wartet unbegrenzt, bis der Server antwortet. Wenn Sie dies innerhalb der Fenster Prozedur tun, antwortet die Benutzeroberfläche erst, wenn die Anforderung abgeschlossen ist. Während dieser Zeit kann das Fenster keine Maus-oder Tastatureingaben verarbeiten, sich selbst neu zeichnen oder sogar schließen.

Stattdessen sollten Sie die Arbeit in einen anderen Thread verschieben. verwenden Sie dazu eine der in Windows integrierten Multitasking-Funktionen:

- Erstellen Sie einen neuen Thread.
- Verwenden von Threadpools.
- Verwenden Sie asynchrone e/a-Aufrufe.
- Verwenden Sie asynchrone Prozedur Aufrufe.

## <a name="next"></a>Nächste

[Zeichnen des Fensters](painting-the-window.md)