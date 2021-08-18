---
title: Zeichnen des Fensters
description: Sie haben Ihr Fenster erstellt. Nun möchten Sie etwas darin anzeigen. In Windows Terminologie wird dies als Zeichnen des Fensters bezeichnet. Um Metaphern zu mischen, ist ein Fenster ein leerer Zeichenbereich, der darauf wartet, dass Sie es ausfüllen.
ms.assetid: db97a4c9-7592-42d1-a5de-9c468169eefc
ms.topic: article
ms.date: 08/16/2019
ms.openlocfilehash: 93d0cb0234975b61ee7ffc05a680b5e1e6b1e01b9d4de7235fc4239ec5573f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897018"
---
# <a name="painting-the-window"></a>Zeichnen des Fensters

Sie haben Ihr Fenster erstellt. Nun möchten Sie etwas darin anzeigen. In Windows Terminologie wird dies als Zeichnen des Fensters bezeichnet. Um Metaphern zu mischen, ist ein Fenster ein leerer Zeichenbereich, der darauf wartet, dass Sie es ausfüllen.

Manchmal initiiert Ihr Programm das Zeichnen, um die Darstellung des Fensters zu aktualisieren. In anderen Fällen werden Sie vom Betriebssystem benachrichtigt, dass Sie einen Teil des Fensters neu malieren müssen. In diesem Fall sendet das Betriebssystem dem Fenster eine [**WM \_ PAINT-Meldung.**](/windows/desktop/gdi/wm-paint) Der Teil des Fensters, der gezeichnet werden muss, wird als *Updatebereich* bezeichnet.

Wenn ein Fenster zum ersten Mal angezeigt wird, muss der gesamte Clientbereich des Fensters gezeichnet werden. Daher erhalten Sie immer mindestens eine [**WM \_ PAINT-Meldung,**](/windows/desktop/gdi/wm-paint) wenn Sie ein Fenster anzeigen.

![Abbildung des Updatebereichs eines Fensters](images/painting01.png)

Sie sind nur für das Zeichnen des Clientbereichs verantwortlich. Der umgebende Frame, einschließlich der Titelleiste, wird automatisch vom Betriebssystem gezeichnet. Nachdem Sie das Zeichnen des Clientbereichs abgeschlossen haben, löschen Sie den Updatebereich, der dem Betriebssystem mitteilt, dass keine weitere [**WM \_ PAINT-Nachricht**](/windows/desktop/gdi/wm-paint) gesendet werden muss, bis sich etwas ändert.

Angenommen, der Benutzer verschiebt ein anderes Fenster, sodass ein Teil des Fensters verdeckt wird. Wenn der verdeckte Teil wieder sichtbar wird, wird dieser Teil dem Updatebereich hinzugefügt, und Ihr Fenster empfängt eine weitere [**WM \_ PAINT-Meldung.**](/windows/desktop/gdi/wm-paint)

![Abbildung, die zeigt, wie sich der Updatebereich ändert, wenn sich zwei Fenster überlappen](images/painting02.png)

Der Updatebereich ändert sich auch, wenn der Benutzer das Fenster streckt. Im folgenden Diagramm streckt der Benutzer das Fenster nach rechts. Der neu verfügbar gemachte Bereich auf der rechten Seite des Fensters wird dem Updatebereich hinzugefügt:

![Abbildung, die zeigt, wie sich der Updatebereich ändert, wenn die Größe eines Fensters geändert wird](images/painting03.png)

In unserem ersten Beispielprogramm ist die Zeichnungsroutine sehr einfach. Er füllt nur den gesamten Clientbereich mit einer Volltonfarbe aus. Dennoch reicht dieses Beispiel aus, um einige der wichtigen Konzepte zu veranschaulichen.

```C++
switch (uMsg)
{
    case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);

        // All painting occurs here, between BeginPaint and EndPaint.

        FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));

        EndPaint(hwnd, &ps);
    }
    return 0;
}
```

Starten Sie den Zeichnungsvorgang, indem Sie die [**BeginPaint-Funktion**](/windows/desktop/api/winuser/nf-winuser-beginpaint) aufrufen. Diese Funktion füllt die [**PAINTSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-paintstruct) mit Informationen zur Anforderung zum erneuten Zeichnen auf. Der aktuelle Updatebereich wird im **rcPaint-Member** von **PAINTSTRUCT angegeben.** Diese Updateregion wird relativ zum Clientbereich definiert:

![Abbildung, die den Ursprung des Clientbereichs zeigt](images/painting04.png)

In Ihrem Zeichnungscode haben Sie zwei grundlegende Optionen:

- Paint den gesamten Clientbereich, unabhängig von der Größe der Updateregion. Alles, was außerhalb des Updatebereichs liegt, wird abgeschnitten. Das heißt, das Betriebssystem ignoriert dies.
- Optimieren Sie , indem Sie nur den Teil des Fensters innerhalb des Updatebereichs zeichnen.

Wenn Sie immer den gesamten Clientbereich zeichnen, ist der Code einfacher. Wenn Sie jedoch eine komplizierte Zeichnungslogik haben, kann es effizienter sein, die Bereiche außerhalb der Updateregion zu überspringen.

Die folgende Codezeile füllt den Aktualisierungsbereich mit einer einzelnen Farbe aus, wobei die systemdefinierte Fensterhintergrundfarbe (**COLOR \_ WINDOW**) verwendet wird. Die tatsächliche Farbe, die durch **COLOR \_ WINDOW** angegeben wird, hängt vom aktuellen Farbschema des Benutzers ab.

```C++
FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
```

Die Details von [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) sind für dieses Beispiel nicht wichtig, aber der zweite Parameter gibt die Koordinaten des zu füllenden Rechtecks an. In diesem Fall übergeben wir den gesamten Updatebereich (den **rcPaint-Member** von [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)). Bei der ersten [**WM \_ PAINT-Nachricht**](/windows/desktop/gdi/wm-paint) muss der gesamte Clientbereich gezeichnet werden, sodass **rcPaint** den gesamten Clientbereich enthält. Bei nachfolgenden **WM \_ PAINT-Nachrichten** kann **rcPaint** ein kleineres Rechteck enthalten.

Die [**FillRect-Funktion**](/windows/desktop/api/winuser/nf-winuser-fillrect) ist Teil des Graphics Device Interface (GDI), das Windows Grafiken sehr lange unterstützt. In Windows 7 hat Microsoft eine neue Grafik-Engine namens Direct2D eingeführt, die leistungsstarke Grafikvorgänge wie die Hardwarebeschleunigung unterstützt. Direct2D ist auch für Windows Vista über das [Plattformupdate für Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md) und für Windows Server 2008 über das Plattformupdate für Windows Server 2008 verfügbar. (GDI wird weiterhin vollständig unterstützt.)

Nachdem Sie mit dem Zeichnen fertig sind, rufen Sie die [**EndPaint-Funktion**](/windows/desktop/api/winuser/nf-winuser-endpaint) auf. Diese Funktion löscht den Updatebereich, der Windows signalisiert, dass das Fenster das Zeichnen selbst abgeschlossen hat.

## <a name="next"></a>Nächste

[Schließen des Fensters](closing-the-window.md)