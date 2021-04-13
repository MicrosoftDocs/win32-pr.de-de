---
title: Zeichnen des Fensters
description: Sie haben Ihr Fenster erstellt. Nun möchten Sie etwas darin anzeigen. In der Windows-Terminologie wird dies als "Zeichnen des Fensters" bezeichnet. Zum Kombinieren von Metaphern ist ein Fenster ein leerer Zeichenbereich, der darauf wartet, dass Sie ihn ausfüllen.
ms.assetid: db97a4c9-7592-42d1-a5de-9c468169eefc
ms.topic: article
ms.date: 08/16/2019
ms.openlocfilehash: f0f9d5c2759ea1735e370eb258743364980daee8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104551949"
---
# <a name="painting-the-window"></a>Zeichnen des Fensters

Sie haben Ihr Fenster erstellt. Nun möchten Sie etwas darin anzeigen. In der Windows-Terminologie wird dies als "Zeichnen des Fensters" bezeichnet. Zum Kombinieren von Metaphern ist ein Fenster ein leerer Zeichenbereich, der darauf wartet, dass Sie ihn ausfüllen.

Manchmal initiiert das Programm das Zeichnen, um die Darstellung des Fensters zu aktualisieren. Zu anderen Zeiten werden Sie vom Betriebssystem benachrichtigt, dass Sie einen Teil des Fensters neu zeichnen müssen. In diesem Fall sendet das Betriebssystem dem Fenster eine [**WM- \_**](/windows/desktop/gdi/wm-paint) Zeichnungs Nachricht. Der Teil des Fensters, der gezeichnet werden muss, wird als *Update Bereich* bezeichnet.

Wenn ein Fenster zum ersten Mal angezeigt wird, muss der gesamte Client Bereich des Fensters gezeichnet werden. Daher erhalten Sie immer mindestens eine WM-Zeichnungs [**Nachricht \_**](/windows/desktop/gdi/wm-paint) , wenn Sie ein Fenster anzeigen.

![Abbildung mit dem Aktualisierungs Bereich eines Fensters](images/painting01.png)

Sie sind nur für das Zeichnen des Client Bereichs verantwortlich. Der umgebende Frame einschließlich der Titelleiste wird automatisch vom Betriebssystem gezeichnet. Nachdem Sie den Client Bereich gezeichnet haben, löschen Sie den Aktualisierungs Bereich, der dem Betriebssystem mitteilt, dass keine weitere WM-Zeichnungs [**Nachricht \_**](/windows/desktop/gdi/wm-paint) gesendet werden muss, bis etwas geändert wird.

Nehmen Sie jetzt an, dass der Benutzer ein anderes Fenster verschiebt, sodass ein Teil des Fensters verdeckt wird. Wenn der verdeckte Teil wieder sichtbar wird, wird dieser Teil dem Aktualisierungs Bereich hinzugefügt, und Ihr Fenster empfängt eine weitere WM-Zeichnungs Nachricht. [**\_**](/windows/desktop/gdi/wm-paint)

![Abbildung, die zeigt, wie sich der Update Bereich ändert, wenn sich zwei Fenster](images/painting02.png)

Der Aktualisierungs Bereich ändert sich auch, wenn der Benutzer das Fenster ausdehnt. Im folgenden Diagramm wird das Fenster vom Benutzer nach rechts gestreckt. Der neu verfügbar gemachte Bereich auf der rechten Seite des Fensters wird der Aktualisierungs Region hinzugefügt:

![Abbildung, die zeigt, wie sich der Update Bereich ändert, wenn die Größe eines Fensters geändert wird](images/painting03.png)

Im ersten Beispielprogramm ist die Zeichnungs Routine sehr einfach. Es füllt nur den gesamten Client Bereich mit einer voll Tonfarbe aus. Dennoch genügt dieses Beispiel, um einige wichtige Konzepte zu veranschaulichen.

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

Starten Sie den Zeichnungs Vorgang, indem Sie die [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) -Funktion aufrufen. Diese Funktion füllt die [**paintstruct**](/windows/win32/api/winuser/ns-winuser-paintstruct) -Struktur mit Informationen über die Repaint-Anforderung aus. Der aktuelle Aktualisierungs Bereich wird im **rcpaint** -Member von **paintstruct** angegeben. Dieser Aktualisierungs Bereich ist relativ zum Client Bereich definiert:

![Abbildung, die den Ursprung des Client Bereichs anzeigt](images/painting04.png)

In Ihrem Zeichnungs Code haben Sie zwei grundlegende Optionen:

- Zeichnen Sie den gesamten Client Bereich unabhängig von der Größe des Aktualisierungs Bereichs. Alle Elemente, die außerhalb des Aktualisierungs Bereichs liegen, werden abgeschnitten. Das heißt, das Betriebssystem ignoriert es.
- Optimieren Sie, indem Sie nur den Teil des Fensters innerhalb des Aktualisierungs Bereichs zeichnen.

Wenn Sie immer den gesamten Client Bereich zeichnen, ist der Code einfacher. Wenn Sie jedoch eine komplizierte Zeichnungs Logik haben, kann es effizienter sein, die Bereiche außerhalb der Aktualisierungs Region zu überspringen.

Die folgende Codezeile füllt den Update Bereich mit einer einzelnen Farbe auf, wobei die Hintergrundfarbe des System definierten Fensters (**Farb \_ Fenster**) verwendet wird. Die tatsächliche Farbe, die durch das **Farb \_ Fenster** angegeben ist, hängt vom aktuellen Farbschema des Benutzers ab.

```C++
FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
```

Die Details von [**fillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) sind für dieses Beispiel nicht wichtig, aber der zweite Parameter gibt die Koordinaten des Rechtecks an, das ausgefüllt werden soll. In diesem Fall übergeben wir den gesamten Update Bereich (den **rcpaint** -Member von [**paintstruct**](/windows/win32/api/winuser/ns-winuser-paintstruct)). Bei der ersten [**WM \_**](/windows/desktop/gdi/wm-paint) -Zeichnungs Nachricht muss der gesamte Client Bereich gezeichnet werden, sodass **rcpaint** den gesamten Client Bereich enthält. Bei nachfolgenden **WM \_ Paint** -Meldungen enthält **rcpaint** möglicherweise ein kleineres Rechteck.

Die [**fillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) -Funktion ist Teil des Graphics Device Interface (GDI), das für einen sehr langen Zeitraum Windows-Grafiken betrieben hat. In Windows 7 führte Microsoft eine neue Grafik-Engine mit dem Namen Direct2D ein, die hochleistungsfähige Grafik Vorgänge wie Hardwarebeschleunigung unterstützt. Direct2D ist auch für Windows Vista über das [Platt Form Update für Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md) und für Windows Server 2008 über das Platt Form Update für Windows Server 2008 verfügbar. (GDI wird weiterhin vollständig unterstützt.)

Nachdem Sie das Zeichnen abgeschlossen haben, können Sie die [**endpaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) -Funktion aufzurufen. Diese Funktion löscht den Update Bereich, der Windows signalisiert, dass das Fenster das Zeichnen selbst abgeschlossen hat.

## <a name="next"></a>Nächste

[Schließen des Fensters](closing-the-window.md)