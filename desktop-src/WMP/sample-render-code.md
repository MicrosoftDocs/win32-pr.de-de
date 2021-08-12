---
title: Beispiel für Rendercode
description: Beispiel für Rendercode
ms.assetid: 14978cf4-47fa-4b2e-ba51-799be873dc8a
keywords:
- Visualisierungen,Beispielcode
- Benutzerdefinierte Visualisierungen, Beispielcode
- Visualisierungen,Render-Funktion
- Benutzerdefinierte Visualisierungen, Renderfunktion
- Renderfunktion, Beispielcode
- Beispiele,Renderfunktion für Visualisierungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51265191ba7fd8b5eb9e4b1140990a7713eba08356d01c58097c727ec2fe533e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569786"
---
# <a name="sample-render-code"></a>Beispiel für Rendercode

Im Folgenden finden Sie Beispielcode, der die **Render-Funktion** verwendet, um eine Linie über den Bildschirm zu zeichnen. Die Höhe der Linie wird durch den Wellenformwert definiert.


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



Die **Render-Funktion** ist der Ort, an dem die Hauptarbeit ihres Codes stattfindet. Jedes Mal, Windows Media Player eine Momentaufnahme der Audiodatei erstellt, wird diese Funktion aufrufen, und Ihr Code wird ausgeführt.

Dieser Code führt die folgenden Aufgaben aus. Weitere Informationen zu bestimmten Windows finden Sie im Microsoft Windows Platform SDK für 32-Bit-Anwendungen.

## <a name="creating-objects"></a>Erstellen von Objekten

In der Regel verwenden Sie die Zeichnungsfunktionen, die im Microsoft Windows Graphical Display Interface (GDI) stehen. Sie müssen Stifte erstellen, um Linien und Pinsel zum Füllen von Bereichen zu zeichnen.

Es wird ein solider schwarzer Pinsel erstellt, um den Hintergrund zu füllen.

Ein solider Stift wird erstellt, um eine Linie zu zeichnen. Die Farbe ist die Vordergrundfarbe, wie von der Skin definiert, die die Visualisierung anzeigen soll.

## <a name="adding-the-object-to-the-dc"></a>Hinzufügen des Objekts zum DC

Sie müssen den Stift dem Gerätekontext (DC) hinzufügen. Der DC ist der Teil des Arbeitsspeichers, in dem alle Zeichnungsdaten und -objekte gespeichert werden. Im Wesentlichen ist der DC der Fensterdatenverkehr-Manager, der alles grafisch nachverfolgt.

Sie müssen das *von Ihnen* erstellte Stiftobjekt um casten und als alten Stift speichern. Verwenden Sie diese Codierungstechnik für alle neuen Stifte. Diese Technik ist für die 32-Bit-Programmierung erforderlich.

## <a name="filling-in-the-background"></a>Ausfüllen des Hintergrunds

Sie können jetzt zeichnen. Die **FillRect-Funktion** füllt das Rechteck des Fensters aus, wie durch die Parameter der **Render-Funktion definiert.** Das Rechteck wird mit einem schwarzen Pinsel gefüllt.

## <a name="getting-audio-data"></a>Abrufen von Audiodaten

Als Nächstes ruft der Code einige Audiodaten aus Windows Media Player. Mithilfe des Waveform-Arrays können Sie den aktuellen Wert der Audioleistung zum Zeitpunkt der Momentaufnahme erhalten. In diesem Fall verwenden Sie die Audiodaten des linken Kanals. Der erste Wert im Array ist der erste 1024. der Audiostrommomentaufnahme.

Diese Informationen werden verwendet, um eine Linie anzuzeigen, deren Höhe mit der Audiostrommomentaufnahme übereinstimmen wird.

## <a name="draw-the-line"></a>Einen Punkt machen

Die Linie wird mithilfe der GDI-Funktionen **MoveToEx** und **LineTo** von links nach rechts gezeichnet.

Zuerst verschieben Sie den Stift an den Anfangspunkt. In diesem Fall werden x und y verwendet, um die Werte von links nach rechts und von oben nach unten zu definieren, die dem Benutzer auf dem Bildschirm angezeigt werden. X wird durch das Rechteck PRC und insbesondere durch den Wert von prc->definiert. Y ist in diesem Moment als Wert der Wellenformdaten definiert.

Anschließend zeichnen Sie eine Linie zur anderen Seite des Fensters. Der Punkt, auf den Sie die Linie zeichnen, ist wieder ein x,y-Wert. X wird durch das Rechteck PRC definiert, dieses Mal jedoch durch prc->rechts. Y wird weiterhin durch die Wellenformdaten definiert und ist identisch mit dem Punkt, von dem aus Sie begonnen haben, da Sie eine gerade Linie von links nach rechts zeichnen.

## <a name="clean-up-everything"></a>Bereinigt alles

Sie müssen die objekte löschen, die Sie erstellen. Insbesondere müssen Sie alle Pinsel und Stifte löschen, die Sie erstellen. Es ist eine bewährte Methode, Stifte und Pinsel zu löschen, wenn Sie sie nicht mehr verwenden.

Wenn Sie sie nicht löschen, bevor Sie die Implementierung der **Render-Funktion** beenden, stürzt Ihre Visualisierung in einer Minute oder weniger ab. Sie müssen die Anzahl Ihrer Stifte und Pinsel behalten und jeden einzelnen zerstören. Achten Sie besonders darauf, in einer Codeschleife keine Stifte zu erstellen.

Verwenden Sie die im Beispiel gegebene Codierungstechnik, um Ihre Stifte und Pinsel zu zerstören.

-   **Wichtig** Zerstören Sie Ihre Stifte und Pinsel!

Wenn Sie die Bereinigung abgeschlossen haben, stellen Sie sicher, dass SIE S OK zurückgeben, damit Windows Media Player wissen, dass Sie mit dem \_ Zeichnen fertig sind. Sobald Sie fertig sind, wird ihre Zeichnung in das Fenster übertragen, eine weitere Momentaufnahme wird erstellt, **Render** fragt Ihren Code erneut, um zu zeichnen, und so weiter.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Rendern**](implementing-render.md)
</dt> </dl>

 

 




