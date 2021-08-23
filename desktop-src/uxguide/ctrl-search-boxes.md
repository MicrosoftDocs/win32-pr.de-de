---
title: Suchfelder
description: Mit einem Suchfeld können Benutzer schnell bestimmte Objekte oder Text in einem großen Satz von Daten finden, indem sie Übereinstimmungen filtern oder hervorheben.
ms.assetid: e2d77b36-e001-403c-9b66-2d136c394a24
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 71e0ce45e2fd0b84b0abda9462f2cb42c945790e93ea06e7dfc6ece0f65ffd65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842935"
---
# <a name="search-boxes"></a>Suchfelder

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Mit einem Suchfeld können Benutzer schnell bestimmte Objekte oder Text in einem großen Satz von Daten finden, indem sie Übereinstimmungen filtern oder hervorheben. Es gibt kein standardes Suchsteuerfeld, aber Sie sollten versuchen, die Suchfeatures Ihres Programms mit denen des Programms konsistent Windows.

Es gibt zwei Arten von Suchvorgängen:

-   **Sofortige Suche,** bei der die Ergebnisse sofort angezeigt werden, wenn der Benutzer eint. Es muss keine Schaltfläche angeklickt werden, sodass das Lupensuchsymbol als Grafik und nicht als Schaltfläche angezeigt wird.

    ![Screenshot: Sofortiges Suchfeld mit einer Eingabeaufforderung, die auf das Suchfeld zeigt, und einem Suchsymbol, das auf die Lupengrafik zeigt](images/ctrl-search-boxes-image1.png)

    Ein typisches Suchfeld mit sofortiger Suche. Die Suche wird bei jeder Tastatureingabe automatisch ausgeführt.

-   **Reguläre Suche,** bei der eine Suche durchgeführt wird, wenn der Benutzer auf die Suchschaltfläche klickt. Das Lupensuchsymbol wird auf einer Schaltfläche angezeigt.

    ![Screenshot eines regulären Suchfelds ](images/ctrl-search-boxes-image2.png)

    Ein typisches Suchfeld mit regulärer Suche. Benutzer klicken auf eine Schaltfläche, um die Suche durchzuführen.

    Sie können eine oder beide Arten von Suchoptionen für Ihre Benutzer bereitstellen.

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Sind bestimmte Objekte schwer zu finden?** Dies kann passieren, wenn:
    -   Es gibt viele -Objekte.
    -   Die Objekte befinden sich nicht an einer einzelnen Position. Die Suche ist besonders nützlich, um Objekte in Strukturen zu finden.
    -   Die Suchdaten sind schwer zu finden (z. B. Metadaten).
-   **Müssen Benutzer bestimmten Text in Dokumenten finden?**
-   **Gibt Ihr Feature innerhalb von fünf Sekunden relevante Suchergebnisse zurück?** Wenn nicht, können Sie ein Suchfeature bereitstellen, aber einen alternativen Entwurf verwenden, der sichtbares Feedback liefert, um Suchvorgänge mit langer Ausführungslauf, z. B. ein Suchdialogfeld, zu unterstützen.

## <a name="design-concepts"></a>Entwurfskonzepte

Die Suche ist ein wichtiger erster Schritt in vielen Szenarien: Benutzer müssen Objekte suchen, bevor sie sie verwenden können. Benutzer speichern immer mehr Objekte auf immer größeren Festplatten, aber die Suche nach Objekten lässt sich nicht gut skalieren. Die Suche muss ein einfacher, konsistenter, zuverlässiger Teil der Benutzererfahrung sein.

Suchfelder in Windows:

-   Sie sind Teil aller Explorer-Fenster, sodass sie leicht zu finden und zu erkennen sind.
-   Einheitliche Darstellung und einheitliches Verhalten.
-   Sie sind effizient und schnell und liefern sofortige Ergebnisse im Sofortigen Suchmodus.

Ein Suchfeld wird in folgenden Windows verwendet:

-   Explorer
-   Erfahrungen (Microsoft Windows Media Player, Windows Fotogalerie, Windows Internet Explorer)
-   Startmenü (zum Suchen von Programmen und aktuellen Dateien)
-   Systemsteuerung -Startseite (zum Suchen von Systemsteuerungselementen und -aufgaben)
-   Hilfe (um relevante Hilfethemen zu finden)

### <a name="look-and-feel"></a>Aussehen und Fühl

Das Gefühl der Suche in Windows wurde durch die Unterstützung der sofortigen Suche erheblich verbessert. Sofortige Ergebnisse machen Windows leistungsfähiger und direkter.

In Windows Explorer- und Anwendungsfenstern befindet sich die Suche in der oberen rechten Ecke, wenn es sich um einen zusätzlichen Einstiegspunkt handelt. In diesem Fall suchen Benutzer nach einem Suchmechanismus, wenn sie nicht finden, was sie im Fenster suchen. Wenn Die Suche jedoch der primäre Einstiegspunkt ist, wird sie oben im Fenster zentriert.

Die Schaltfläche Suchen ist visuell mit einem Suchfeld verbunden. Um Platz zu minimieren, wird eine optionale [Eingabeaufforderung](ctrl-text-boxes.md) in einem Suchfeld anstelle einer Bezeichnung verwendet. Bei der Eingabeaufforderung kann es sich um eine Anweisung (z. B. Typ für Suche) oder um den Bereich der Suche (z. B. Nach Bildern suchen) geben.

![Screenshot eines sofortigen Suchfelds ](images/ctrl-search-boxes-image3.png)

Ohne Bezeichnungen und separate Schaltflächen hat die sofortige Suche in Windows einfaches Aussehen.

Bei einer erfolgreichen Suche wird eine virtuelle Seite der Suchergebnisse erstellt und dem Stapel "Zurück" und der Adressleiste hinzufügt. Benutzer haben mehrere Möglichkeiten, die ursprüngliche Seite wiederherzustellen und ein Suchfeld zu löschen, z. B. durch Klicken auf Zurück, Klicken auf die ursprüngliche Seite in der Adressleiste, Drücken von ESC oder Löschen des Suchfelds.

Benutzer können auch einfach das Suchfeld löschen, ohne eine vorherige Seite mit Ergebnissen wiederherstellungen zu müssen. Im Suchmodus "Sofort" wird eine Schaltfläche zum Löschen angezeigt, nachdem der Benutzer mit der Eingabe beginnt. Ein "x" ersetzt das Lupensuchsymbol. Wenn Sie darauf klicken, erhält das "x" ein Schaltflächen-Aussehen und kann angeklickt werden.

![Screenshot eines Suchfelds mit einem "x"-Symbol ](images/ctrl-search-boxes-image4.png)

Der Benutzer kann das Suchfeld löschen, indem er am rechten Ende des Steuerelements auf "x" klickt.

Im regulären Suchmodus ist die Schaltfläche "Löschen" optional. Benutzer finden es möglicherweise hilfreich, wenn eine Suche z. B. lange dauern soll. Benutzer können auf das "x" klicken, um die Suche zu beenden. Wenn eine Suche bereits abgeschlossen wurde, können Benutzer auf das "x" klicken, um das Suchfeld zu löschen.

## <a name="guidelines"></a>Richtlinien

### <a name="location"></a>Standort

-   Suchen Sie für Anwendungsfenster in der oberen rechten Ecke nach Suchen.
-   Suchen Sie bei Popupfenstern nach Suchen, wo dies am sinnvollsten und praktischsten ist.
-   **Ausnahme:** Wenn Search in der Regel das erste Ist, was Benutzer in einem Fenster (dem primären Einstiegspunkt) tun, zentriert sie oben im Fenster.

### <a name="look"></a>Blick

-   Verwenden Sie die standarden Suchschaltflächengrafiken. Es gibt drei Versionen:
    -   **Nur Lupensuchsymbol (keine Schaltfläche beim Hovern).** Verwenden Sie für die sofortige Suche.
    -   **Lupensuchsymbol mit Schaltfläche.** Verwenden Sie , wenn auf die Schaltfläche geklickt werden muss, um die Suche zu starten.
    -   **Lupensuchsymbol mit Schaltfläche und Dropdownpfeil.** Fügen Sie einen Dropdownpfeil hinzu, wenn Benutzer den Bereich ändern können oder wenn andere Einstellungen verfügbar sind.
        -   Verwenden Sie für sofortige Suche nur einen Dropdownpfeil, und zeigen Sie eine Schaltfläche an, wenn Sie darauf zeigen.
        -   Zeigen Sie für die reguläre Suche den Dropdownpfeil auf einer Schaltfläche an.

![Abbildung von sofortigen Suchfeldern in unterschiedlichen Zuzuständen ](images/ctrl-search-boxes-image5.png)

Visuelle Spezifikationen für die sofortige Suche.

![Abbildung regulärer Suchfelder in unterschiedlichen Zuzuständen ](images/ctrl-search-boxes-image6.png)

Visuelle Spezifikationen für die reguläre Suche.

-   Verwenden Sie keine Bezeichnung. Verwenden Sie stattdessen eine optionale Eingabeaufforderung. Wenn Benutzer tendenziell davon ausgehen, dass es sich bei der Suche um eine generische Dateisuche handelt, verwenden Sie die Eingabeaufforderung, um den Bereich zu geben. Verwenden Sie andernfalls Typ für die Suche oder einen ähnlichen, präzisen Ausdruck.

    ![Screenshot der Eingabeaufforderung "Zu durchsuchende Typen" ](images/ctrl-search-boxes-image7.png)

    ![Screenshot der Eingabeaufforderung "Alle Gadgets durchsuchen" ](images/ctrl-search-boxes-image8.png)

    In diesen Beispielen unterstützen kurze Textaufforderungen Benutzer bei der Arbeit mit Search.

### <a name="interaction"></a>Interaktion

-   **Wählen Sie beim Eingabefokus automatisch einen zuvor eingegebenen Text aus.** Auf diese Weise können Benutzer eine neue Suche durch Eingabe von eingeben oder die vorherige Suche ändern, indem sie das Caretcursal mithilfe der Pfeiltasten positionieren.

    ![Screenshot des Suchfelds mit hervorgehobener Text ](images/ctrl-search-boxes-image9.png)

    In diesem Beispiel wird zuvor eingegebener Text auf dem Eingabefokus ausgewählt.

-   **Weisen Sie dem Suchfeld die Tastenkombination STRG+E zu.**

### <a name="functionality"></a>Funktionalität

-   **Unterstützen Sie nach Möglichkeit die sofortige Suche.** Stellen Sie sowohl normale als auch sofortige Suchvorgänge bereit, wenn es Szenarien gibt, in denen die reguläre Suche die zusätzliche Wartezeit wert ist.
-   Reguläre Suchvorgänge müssen innerhalb von fünf Sekunden relevante Ergebnisse zurückgeben, und bei der sofortigen Suche müssen innerhalb von zwei Sekunden Ergebnisse zurückgegeben werden. Nach diesem Punkt kann die Suche im Laufe der Zeit weniger relevante Ergebnisse liefern, solange das Programm reaktionsfähig ist und Benutzer andere Aufgaben ausführen können. Möglicherweise müssen Sie Ihre Suchdaten indizieren, um diese Reaktionsfähigkeit sicherzustellen.
-   Wenn Sie sowohl reguläre als auch sofortige Suchmodi angeben, müssen die Ergebnisse der sofortigen Suche eine Teilmenge der regulären Suchergebnisse sein.
-   Die gesamte Suche erfolgt präfixbasiert (keine Teilzeichenfolge oder Suffixsuche). Die Verwendung von nachgestellten Platzhalterzeichen ist optional und wirkt sich nicht auf die Ergebnisse aus. Wenn mehrere Wörter eingegeben werden, verwenden Sie DIE OR-Suche.
-   Bei einer erfolgreichen Suche wird dem Stapel "Zurück" und der Adressleiste eine virtuelle Seite mit den Suchergebnissen hinzugefügt. Mehrere Suchvorgänge führen zu einer einzelnen virtuellen Seite. Wenn Sie also auf Zurück klicken, wird immer die ursprüngliche Seite zurückgegeben.
-   Ordnen Sie bei Bedarf für die Skalierung die Suchergebnisse nach Relevanz an.
-   Eine leere Suche gibt die ursprüngliche Seite zurück.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größen- und Abstände

![Abbildung der Größe und des Abstands von Sofortsuchfeld ](images/ctrl-search-boxes-image10.png)

Empfohlene Größen- und Abstandsfunktion für die sofortige Suche.

![Abbildung der Größe und des Abstands des regulären Suchfelds ](images/ctrl-search-boxes-image11.png)

Empfohlene Größen- und Abstandsfunktion für die reguläre Suche.

## <a name="text"></a>Text

-   Geben Sie für die Formulierung der Eingabeaufforderung im Suchfeld entweder eine Anweisung an (z. B. Typ für Suche), oder geben Sie den Bereich der Suche an (z. B. Nach Bildern suchen).
-   Der Eingabeaufforderungstext sollte kurz sein. Ein einzelnes Wort oder ein kurzer Ausdruck sollte ausreichen.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Verwenden Sie keine endende Interpunktion oder Auslassungszeichen.

## <a name="documentation"></a>Dokumentation

-   Verweisen Sie auf dieses Steuerelement als Suchfeld. Großschreibung des Anfangsbuchstabens des ersten Worts; Großbuchstaben des Anfangsbuchstabens des Felds nicht groß schreiben.
-   Die beiden Suchtypen werden als Sofortige Suche und reguläre Suche bezeichnet. Großbuchstaben des Anfangsbuchstabens der sofortigen Suche Großbuchstaben der regulären Suche werden nicht groß geschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Glossar](glossary.md)
</dt> </dl>

 

 