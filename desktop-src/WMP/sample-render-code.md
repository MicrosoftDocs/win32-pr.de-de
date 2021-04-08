---
title: Beispiel-Rendering-Code
description: Beispiel-Rendering-Code
ms.assetid: 14978cf4-47fa-4b2e-ba51-799be873dc8a
keywords:
- Visualisierungen, Beispielcode
- benutzerdefinierte Visualisierungen, Beispielcode
- Visualisierungen, Rendering-Funktion
- benutzerdefinierte Visualisierungen, Rendering-Funktion
- Funktion "Rendering", Beispielcode
- Beispiele, Rendering-Funktion für Visualisierungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1ee5d00bc1aed5bd8bd91880e43e2ac2d1f6bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037204"
---
# <a name="sample-render-code"></a>Beispiel-Rendering-Code

Hier sehen Sie einen Beispielcode, der die Funktion " **Rendering** " verwendet, um eine Linie auf dem Bildschirm zu zeichnen. Die Höhe der Zeile wird durch den Wellenform-Wert definiert.


```C++
STDMETHODIMP CStock::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    // Create new brushes and pens.
    HBRUSH hNewBrush = ::CreateSolidBrush( 0 );
    // Create a new solid pen the color of the foreground.
    HPEN hNewPen = ::CreatePen( PS_SOLID, 0, m_clrForeground );


    // Add the pen to the device context.
    HPEN hOldPen= static_cast<HPEN>(::SelectObject( hdc, hNewPen ));

    // Fill the background with the black brush.
    ::FillRect( hdc, prc, hNewBrush );

    // Get the y value from the waveform.
    int y = pLevels->waveform[0][0];

    // Draw the line from left to right.
    ::MoveToEx( hdc, prc->left, y, NULL);  
    ::LineTo(hdc, prc->right, y); 

    // Delete your brush.
    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }
    // Delete your pen.
    if (hNewPen)
    {
        ::SelectObject( hdc, hOldPen );
        ::DeleteObject( hNewPen );
    }

    // You're done for this round.
    return S_OK;
}

```



Die Funktion " **Rendering** " ist der Ort, an dem die Hauptarbeit Ihres Codes erfolgt. Jedes Mal, wenn Windows Media Player eine Momentaufnahme der Audiodatei aufnimmt, wird diese Funktion aufgerufen, und der Code wird ausgeführt.

Dieser Code führt die folgenden Aufgaben aus: Weitere Informationen zu bestimmten Funktionen finden Sie im Microsoft Windows-Plattform-SDK für 32-Bit-Windows.

## <a name="creating-objects"></a>Erstellen von Objekten

Normalerweise verwenden Sie die Zeichnungsfunktionen von Microsoft Windows Graphical Display Interface (GDI). Sie müssen Stifte erstellen, um Linien und Pinsel zum Auffüllen von Bereichen zu zeichnen.

Ein solider schwarzer Pinsel wird erstellt, um den Hintergrund zu füllen.

Ein Vollstift wird erstellt, um eine Linie zu zeichnen. Die Farbe entspricht der Vordergrundfarbe, die von der Skin definiert wird, in der die Visualisierung angezeigt werden soll.

## <a name="adding-the-object-to-the-dc"></a>Hinzufügen des Objekts zum DC

Sie müssen den Stift dem Gerätekontext (DC) hinzufügen. Der Domänen Controller ist der Teil des Arbeitsspeichers, in dem alle Zeichnungsdaten und Objekte gespeichert werden. Im Wesentlichen ist der Domänen Controller der Fenster Traffic Manager, mit dem alles grafisch nachverfolgt wird.

Sie *müssen das von* Ihnen erstellte Pen-Objekt umwandeln und als alten Stift speichern. Verwenden Sie diese Codierungstechnik für alle neuen Stifte. Diese Technik ist für die 32-Bit-Programmierung erforderlich.

## <a name="filling-in-the-background"></a>Ausfüllen des Hintergrunds

Sie können jetzt zeichnen. Die **fillRect** -Funktion wird das Rechteck des Fensters auffüllen, wie durch die Parameter der Funktion " **Rendering** " definiert. Das Rechteck ist mit einem schwarzen Pinsel gefüllt.

## <a name="getting-audio-data"></a>Audiodaten werden erhalten.

Als Nächstes ruft der Code einige Audiodaten aus Windows Media Player ab. Mithilfe des Wellenform-Arrays können Sie den aktuellen Wert der audiopotenz zu dem Zeitpunkt, zu dem die Momentaufnahme erstellt wurde, erhalten. In diesem Fall nehmen Sie die Audiodaten des linken Kanals an. Der erste Wert im Array ist der erste 1024. der audiostrommomentaufnahme.

Diese Informationen werden verwendet, um eine Zeile anzuzeigen, deren Höhe mit der audiostrommomentaufnahme übereinstimmt.

## <a name="draw-the-line"></a>Linie zeichnen

Die Linie wird von links nach rechts mithilfe der Funktionen " **muveumex** " und " **LineTo** GDI" gezeichnet.

Zuerst verschieben Sie den Stift an den Ausgangspunkt. In diesem Fall werden x und y verwendet, um die Werte von links nach rechts und von oben nach unten zu definieren, die dem Benutzer auf dem Bildschirm angezeigt werden. X wird durch die Rechteck-PRC und insbesondere durch den Wert von PRC->left definiert. Y ist zu diesem Zeitpunkt als Wert der Wellenform-Daten definiert.

Anschließend zeichnen Sie eine Linie auf die andere Seite des Fensters. Der Punkt, zu dem Sie die Linie zeichnen, ist wieder ein x-, y-Wert. X wird durch die Rechteck-PRC definiert, aber diesmal von PRC->Recht. Y wird weiterhin durch die Wellenform Daten definiert und entspricht dem Punkt, von dem Sie gestartet haben, da Sie eine gerade Linie von links nach rechts zeichnen.

## <a name="clean-up-everything"></a>Alles bereinigen

Sie müssen die von Ihnen erstellten Objekte löschen. Insbesondere müssen Sie alle Pinsel und Stifte löschen, die Sie erstellen. Es empfiehlt sich, Stifte und Pinsel zu löschen, wenn Sie Sie nicht mehr verwenden.

Wenn Sie Sie nicht löschen, bevor Sie die Implementierung der **Rendering** -Funktion abschließen, stürzt die Visualisierung innerhalb weniger Minuten ab. Sie müssen die Anzahl der Stifte und Pinsel beibehalten und alle einzelnen Stifte zerstören. Achten Sie besonders darauf, keine Stifte innerhalb einer Code Schleife zu erstellen.

Verwenden Sie die im Beispiel angegebene Codierungsmethode, um ihre Stifte und Pinsel zu zerstören.

-   **Wichtig** Zerstören Sie Ihre Stifte und Pinsel!

Wenn Sie die Bereinigung abgeschlossen haben, stellen Sie sicher, dass Sie den Wert OK zurückgibt, \_ damit Windows Media Player weiß, dass Sie das Zeichnen abgeschlossen haben. Sobald Sie fertig sind, wird das Zeichnen in das Fenster übertragen, eine weitere Momentaufnahme wird erstellt, das **Rendering** fordert den Code auf, Sie erneut zu zeichnen, usw.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Rendering**](implementing-render.md)
</dt> </dl>

 

 




