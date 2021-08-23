---
title: Schreiben der Fensterprozedur
description: Schreiben der Fensterprozedur
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853f5effe693e10ad0c5515e9d2ea87d200a1e7dd9b0c79da46228909e53deef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520460"
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

Zusätzliche Daten für die Nachricht sind in den *Parametern lParam* und *wParam* enthalten. Beide Parameter sind ganzzahlige Werte der Größe einer Zeigerbreite (32 Bits oder 64 Bits). Die Bedeutung der einzelnen Hängt vom Nachrichtencode *(uMsg*) ab. Für jede Nachricht müssen Sie den Nachrichtencode auf MSDN suchen und die Parameter in den richtigen Datentyp umschreiben. In der Regel sind die Daten entweder ein numerischer Wert oder ein Zeiger auf eine -Struktur. Einige Nachrichten enthalten keine Daten.

In der Dokumentation für die [**WM \_ SIZE-Meldung**](/windows/desktop/winmsg/wm-size) wird beispielsweise Folgendes angezeigt:

- *wParam* ist ein Flag, das angibt, ob das Fenster minimiert, maximiert oder seine Größe geändert wurde.
- *lParam* enthält die neue Breite und Höhe des Fensters als 16-Bit-Werte, die in eine 32- oder 64-Bit-Zahl gepackt sind. Sie müssen eine Bitverschiebung durchführen, um diese Werte zu erhalten. Glücklicherweise enthält die Headerdatei WinDef.h Hilfsmakros, die dies tun.

Eine typische Fensterprozedur verarbeitet Dutzende von Nachrichten, sodass sie recht lang werden kann. Eine Möglichkeit, Ihren Code modularer zu gestalten, besteht darin, die Logik für die Verarbeitung jeder Nachricht in eine separate Funktion zu setzen. Geben Sie in der Fensterprozedur die *Parameter wParam* und *lParam* in den richtigen Datentyp um, und übergeben Sie diese Werte an die Funktion. Um z. B. die [**WM \_ SIZE-Meldung**](/windows/desktop/winmsg/wm-size) zu verarbeiten, würde die Fensterprozedur wie folgt aussehen:

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

Die [**Makros LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) und [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) erhalten die 16-Bit-Werte für Breite und Höhe aus *lParam.* (Diese Details finden Sie in der MSDN-Dokumentation für jeden Nachrichtencode.) Die Fensterprozedur extrahiert die Breite und Höhe und übergibt diese Werte dann an die `OnSize` Funktion.

## <a name="default-message-handling"></a>Standardmäßige Nachrichtenverarbeitung

Wenn Sie eine bestimmte Nachricht in Ihrer Fensterprozedur nicht behandeln, übergeben Sie die Nachrichtenparameter direkt an die [**DefWindowProc-Funktion.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Diese Funktion führt die Standardaktion für die Nachricht aus, die je nach Nachrichtentyp variiert.

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a>Vermeiden von Engpässen in der Fensterprozedur

Während die Fensterprozedur ausgeführt wird, werden alle anderen Meldungen für Fenster blockiert, die im gleichen Thread erstellt wurden. Vermeiden Sie daher eine lange Verarbeitung innerhalb der Fensterprozedur. Angenommen, Ihr Programm öffnet eine TCP-Verbindung und wartet unbegrenzt, bis der Server antwortet. Wenn Sie dies innerhalb der Fensterprozedur tun, antwortet Die Benutzeroberfläche erst, wenn die Anforderung abgeschlossen ist. Während dieser Zeit kann das Fenster keine Maus- oder Tastatureingaben verarbeiten, sich selbst neu malen oder sogar schließen.

Stattdessen sollten Sie die Arbeit in einen anderen Thread verschieben, indem Sie eine der Multitasking-Einrichtungen verwenden, die in Windows integriert sind:

- Erstellen Sie einen neuen Thread.
- Verwenden von Threadpools.
- Verwenden Sie asynchrone E/A-Aufrufe.
- Verwenden Sie asynchrone Prozeduraufrufe.

## <a name="next"></a>Nächste

[Zeichnen des Fensters](painting-the-window.md)
