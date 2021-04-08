---
title: Suchfelder
description: Mithilfe eines Suchfeld können Benutzer mithilfe von Filtern oder Hervorhebungen von Übereinstimmungen bestimmte Objekte oder Text innerhalb eines großen Satzes von Daten schnell finden.
ms.assetid: e2d77b36-e001-403c-9b66-2d136c394a24
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e9d1fca8fdb96b17098cee79fd5b62ecd7ab7531
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103961078"
---
# <a name="search-boxes"></a>Suchfelder

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Mithilfe eines Suchfeld können Benutzer mithilfe von Filtern oder Hervorhebungen von Übereinstimmungen bestimmte Objekte oder Text innerhalb eines großen Satzes von Daten schnell finden. Es gibt kein Standard-Such Steuerelement, aber Sie sollten sich darauf konzentrieren, die Suchfunktionen Ihres Programms mit denen von Windows konsistent zu machen.

Es gibt zwei Arten von Such Vorgängen:

-   **Sofortige Suche**, bei der die Ergebnisse sofort angezeigt werden, wenn der Benutzer Sie eingibt. Es muss keine Schaltfläche geklickt werden, sodass das Lupen Suchsymbol als Grafik und nicht als Schaltfläche angezeigt wird.

    ![Screenshot, der ein sofortiges Suchfeld mit einer "Prompt"-Legende anzeigt, die auf das Suchfeld zeigt, und ein Symbol "Suchsymbol", das auf die Lupen Grafik zeigt.](images/ctrl-search-boxes-image1.png)

    Ein typisches Suchfeld mit sofortiger Suche. Die Suche wird automatisch auf jedem Tastatur Strich ausgeführt.

-   **Reguläre Suche**, bei der eine Suche durchgeführt wird, wenn der Benutzer auf die Such Schaltfläche klickt. Das Lupen Suchsymbol wird auf einer Schaltfläche angezeigt.

    ![Screenshot eines regulären Suchfelds ](images/ctrl-search-boxes-image2.png)

    Ein typisches Suchfeld mit regulärer Suche. Benutzer klicken auf eine Schaltfläche, um die Suche auszuführen.

    Sie können eine oder beide Arten von Suchoptionen für Ihre Benutzer bereitstellen.

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Sind bestimmte Objekte schwer zu finden?** Dies kann passieren, wenn:
    -   Es sind viele Objekte vorhanden.
    -   Die Objekte befinden sich nicht an einem einzigen Speicherort. Die Suche ist besonders nützlich für das Auffinden von Objekten in Strukturen.
    -   Die Suchdaten sind schwer zu finden (z. b. Metadaten).
-   **Müssen Benutzer bestimmten Text in Dokumenten finden?**
-   **Gibt ihre Funktion relevante Suchergebnisse innerhalb von fünf Sekunden zurück?** Wenn dies nicht der Fall ist, können Sie eine Suchfunktion bereitstellen, aber einen alternativen Entwurf verwenden, der ein sichtbares Feedback bietet, um Suchvorgänge mit langer Ausführungszeit zu ermöglichen

## <a name="design-concepts"></a>Entwurfskonzepte

Die Suche ist ein wichtiger erster Schritt in vielen Szenarien: Benutzer müssen Objekte suchen, bevor Sie Sie verwenden können. Benutzer speichern mehr und mehr Objekte auf immer größeren Festplatten, aber das Durchsuchen nach Objekten ist nicht gut skalierbar. Die Suche muss ein einfacher, konsistentes und zuverlässiger Teil des Benutzer Erlebnisses sein.

Suchfelder in Windows:

-   Sind Teil aller Explorer-Fenster, sodass Sie leicht zu finden und zu erkennen sind.
-   Konsistente Darstellung und Verhalten.
-   Sind effizient und schnell und geben sofortige Ergebnisse im sofort Suchmodus aus.

In Windows wird an diesen Stellen ein Suchfeld verwendet:

-   Explorer
-   Erlebnisse (Microsoft Windows Media Player, Windows-Fotogalerie, Windows Internet Explorer)
-   Startmenü (zum Suchen nach Programmen und zuletzt verwendeten Dateien)
-   Startseite der Systemsteuerung (um System Steuerungselemente und Aufgaben zu suchen)
-   Hilfe (um relevante Hilfe Themen zu finden)

### <a name="look-and-feel"></a>Aussehen und Gefühl

Das Gefühl der Suche in Windows wird durch die Unterstützung der sofortigen Suche erheblich verbessert. Wenn Sie sofortige Ergebnisse haben, ist das Gefühl von Windows leistungsfähiger und direkter.

In Windows-Explorer und Anwendungs Fenstern befindet sich die Suche in der oberen rechten Ecke, wenn es sich um einen ergänzenden Einstiegspunkt handelt. In diesem Fall suchen Benutzer nach einem Suchmechanismus, wenn Sie im Fenster nicht finden, was Sie suchen. Wenn die Suche jedoch der primäre Einstiegspunkt ist, wird Sie am oberen Rand des Fensters zentriert.

Die Such Schaltfläche ist visuell mit einem Suchfeld verbunden. Um den Speicherplatz zu minimieren, wird eine optionale [Eingabeaufforderung](ctrl-text-boxes.md) in einem Suchfeld anstelle einer Bezeichnung verwendet. Die Eingabeaufforderung kann eine Anweisung sein (z. b. zum Suchen eingeben) oder den Suchbereich angeben (z. b. Suche nach Bildern).

![Screenshot eines sofort Suchfelds ](images/ctrl-search-boxes-image3.png)

Ohne Bezeichnungen und separate Schaltflächen weist die sofortige Suche in Windows ein schlankes Aussehen auf.

Durch das Durchführen einer erfolgreichen Suche wird eine virtuelle Seite der Suchergebnisse erstellt und dem Hintergrund Stapel und der Adressleiste hinzugefügt. Benutzer haben mehrere Möglichkeiten, die ursprüngliche Seite wiederherzustellen und ein Suchfeld zu löschen. dazu gehören das Klicken auf die ursprüngliche Seite in der Adressleiste, das Drücken der ESC-Taste oder das Löschen des Suchfelds.

Benutzer können auch einfach das Suchfeld löschen, ohne eine vorherige Seite der Ergebnisse wiederherzustellen. Im sofort Suchmodus wird eine Schaltfläche Clear angezeigt, nachdem der Benutzer mit der Eingabe begonnen hat. ein "x" ersetzt das Lupen Suchsymbol. Wenn Sie darauf zeigen, erhält das "x" eine Schaltfläche, auf die geklickt werden kann.

![Screenshot eines Suchfeld mit dem Symbol "x" ](images/ctrl-search-boxes-image4.png)

Der Benutzer kann das Suchfeld durch Klicken auf "x" am rechten Ende des Steuer Elements löschen.

Im regulären Suchmodus ist die Schaltfläche Clear optional. Benutzer sind möglicherweise hilfreich, z. b. Wenn eine Suche eine lange Zeit in Anspruch nimmt. Benutzer können auf das "x" klicken, um die Suche zu verhindern. Wenn eine Suche bereits abgeschlossen ist, können Benutzer auf das "x" klicken, um das Suchfeld zu löschen.

## <a name="guidelines"></a>Richtlinien

### <a name="location"></a>Standort

-   Suchen Sie unter Anwendungsfenster in der oberen rechten Ecke nach suchen.
-   Für Popup Fenster Suchen Sie nach wo immer sinnvollsten und bequemsten.
-   **Ausnahme:** Wenn die Suche in der Regel das erste ist, das Benutzer in einem Fenster ausführen (der primäre Einstiegspunkt), zentrieren Sie es am oberen Rand des Fensters.

### <a name="look"></a>Blicke

-   Verwenden Sie die Standardgrafiken für die Such Schaltfläche. Es gibt drei Versionen:
    -   **Nur Lupen Suchsymbol (keine Schaltfläche auf dem Mauszeiger).** Verwenden Sie für die sofortige Suche.
    -   **Lupen Suchsymbol mit Schaltfläche.** Verwenden Sie, wenn auf die Schaltfläche zum Starten der Suche geklickt werden muss.
    -   **Lupen Suchsymbol mit Schaltfläche und Dropdown Pfeil.** Fügen Sie einen Dropdown Pfeil hinzu, wenn Benutzer den Bereich ändern können oder wenn andere Einstellungen verfügbar sind.
        -   Verwenden Sie für die sofortige Suche nur einen Dropdown Pfeil, und klicken Sie auf die Schaltfläche mit dem Mauszeiger.
        -   Zeigen Sie bei regulärer Suche den Dropdown Pfeil auf einer Schaltfläche an.

![Abbildung der Felder für die sofortige Suche in verschiedenen Zuständen ](images/ctrl-search-boxes-image5.png)

Visuelle Spezifikationen für die sofortige Suche.

![Abbildung regulärer Suchfelder in unterschiedlichen Zuständen ](images/ctrl-search-boxes-image6.png)

Visuelle Spezifikationen für die reguläre Suche.

-   Verwenden Sie keine Bezeichnung. Verwenden Sie stattdessen eine optionale Eingabeaufforderung. Wenn Benutzer tendenziell davon ausgehen, dass es sich bei der Suche um eine generische Dateisuche handelt, verwenden Sie die Eingabeaufforderung, um den Bereich anzugeben. Verwenden Sie andernfalls Type, um zu suchen, oder einen ähnlichen, präzisen Ausdruck.

    ![Screenshot der Eingabeaufforderung "Typ für Suche" ](images/ctrl-search-boxes-image7.png)

    ![Screenshot der Eingabeaufforderung "alle Gadgets suchen" ](images/ctrl-search-boxes-image8.png)

    In diesen Beispielen helfen Ihnen kurze Text Aufforderungen beim Arbeiten mit der Suche.

### <a name="interaction"></a>Interaktion

-   **Wählen Sie im Eingabefokus automatisch einen zuvor eingegebenen Text aus.** Auf diese Weise können Benutzer eine neue Suche eingeben, indem Sie eingeben oder die vorherige Suche ändern, indem Sie die Einfügemarke mithilfe der Pfeiltasten positionieren.

    ![Screenshot des Suchfelds mit markiertem Text ](images/ctrl-search-boxes-image9.png)

    In diesem Beispiel wird der zuvor eingegebene Text im Eingabefokus ausgewählt.

-   **Weisen Sie die Tastenkombination für das Suchfeld STRG + E zu.**

### <a name="functionality"></a>Funktionalität

-   **Unterstützung von Instant Search, wann immer möglich.** Stellen Sie sowohl reguläre als auch sofortige suchen bereit, wenn es Szenarien gibt, in denen die reguläre Suche die zusätzliche Wartezeit Wert ist.
-   Reguläre Suchvorgänge müssen innerhalb von fünf Sekunden relevante Ergebnisse zurückgeben, und die sofortige Suche muss innerhalb von zwei Sekunden Ergebnisse zurückgeben. Nach diesem Punkt kann die Suche weiterhin weniger relevante Ergebnisse im Laufe der Zeit ausfüllen, wenn das Programm reaktionsfähig ist und Benutzer andere Aufgaben ausführen können. Möglicherweise müssen Sie Ihre Suchdaten indizieren, um die Reaktionsfähigkeit sicherzustellen.
-   Wenn Sie sowohl reguläre als auch sofortige Suchmodi bereitstellen, muss es sich bei den unmittelbaren Suchergebnissen um eine Teilmenge der regulären Suchergebnisse handeln.
-   Alle Suchvorgänge sind Präfix basiert (keine Teil Zeichenfolge oder suffixsuche). Die Verwendung von nachfolgenden Platzhalter Zeichen ist optional und wirkt sich nicht auf die Ergebnisse aus. Wenn mehrere Wörter eingegeben werden, verwenden Sie, oder suchen Sie nach.
-   Bei einer erfolgreichen Suche wird dem BackStack und der Adressleiste eine virtuelle Seite mit den Suchergebnissen hinzugefügt. Mehrere Suchvorgänge führen zu einer einzelnen virtuellen Seite. Wenn Sie auf "zurück" klicken, wird die ursprüngliche Seite zurückgegeben.
-   Ordnen Sie bei Bedarf die Suchergebnisse nach Relevanz zu.
-   Bei einer leeren Suche wird die ursprüngliche Seite zurückgegeben.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größe und Abstände

![Abbildung der Größe und des Abstands des unmittelbaren Suchfelds ](images/ctrl-search-boxes-image10.png)

Empfohlene Größe und Abstände für die sofortige Suche.

![Abbildung der regulären Größe und des Abstands von Suchfeldern ](images/ctrl-search-boxes-image11.png)

Empfohlene Größe und Abstände für die reguläre Suche.

## <a name="text"></a>Text

-   Geben Sie für den Wortlaut der Eingabeaufforderung im Suchfeld entweder eine Anweisung an (z. b. zum Suchen eingeben), oder geben Sie den Suchbereich an (z. b. nach Bildern suchen).
-   Der Eingabe Aufforderungs Text sollte kurz sein. Ein einzelnes Wort oder ein kurzer Ausdruck sollten ausreichen.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Verwenden Sie keine endinterpunktions Zeichen oder Ellipsen.

## <a name="documentation"></a>Dokumentation

-   Dieses Steuerelement wird als Suchfeld bezeichnet. Den ersten Buchstaben des ersten Worts groß schreiben; Schreiben Sie den ersten Buchstaben von Box nicht in Großbuchstaben.
-   Weitere Informationen finden Sie in den beiden Such Typen als sofortige Suche und reguläre Suche. Den anfänglichen Buchstaben der sofortigen Suche groß schreiben Schreiben Sie den ersten Buchstaben der regulären Suche nicht groß.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Glossar](glossary.md)
</dt> </dl>

 

 