---
title: UX-Prüfliste für Desktopanwendungen
description: Im Folgenden finden Sie eine Sammlung einiger wichtiger Richtlinien im Leitfaden zur Benutzererfahrung. Sie können dies als Prüfliste verwenden, um sicherzustellen, dass Die Benutzeroberfläche Ihres Programms diese wichtigen Elemente richtig macht.
ms.assetid: 4705a807-5949-4957-8ea6-70871beaf8e0
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 712b31a7a5166e41e590470aea48f60a1f159850da3ea6917b36ece9ada80fa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119332470"
---
# <a name="ux-checklist-for-desktop-applications"></a>UX-Prüfliste für Desktopanwendungen

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Im Folgenden finden Sie eine Sammlung einiger wichtiger Richtlinien im Leitfaden zur Benutzererfahrung. Sie können dies als Prüfliste verwenden, um sicherzustellen, dass Die Benutzeroberfläche Ihres Programms diese wichtigen Elemente richtig macht.

## <a name="windows"></a>Windows

-   **Unterstützen Sie die minimale Windows effektive Auflösung von 800 x 600 Pixeln.** Für kritische Benutzeroberflächen , die im abgesicherten Modus funktionieren müssen, wird eine [effektive Auflösung](glossary.md) von 640 x 480 Pixel unterstützt. Achten Sie darauf, den von der Taskleiste belegten Speicherplatz zu berücksichtigen, indem Sie 48 vertikale [relative Pixel](glossary.md) für Fenster reservieren, die mit der Taskleiste angezeigt werden.
-   **Optimieren Sie größenveränderbare Fensterlayouts für eine effektive Auflösung von 1024 x 768 Pixeln.** Ändern Sie die Größe dieser Fenster für niedrigere Bildschirmauflösungen automatisch auf eine Weise, die weiterhin funktionsfähig ist.
-   **Stellen Sie sicher, dass Sie Ihre Fenster in den Modi 96 Punkte pro Zoll (dpi) (bei 800 x 600 Pixel), 120 dpi (bei 1024 x 768 Pixel) und 144 dpi (bei 1200 x 900 Pixel) testen.** Überprüfen Sie, ob Layoutprobleme auftreten, z. B. Das Ausschneiden von Steuerelementen, Text und Fenstern und das Strecken von Symbolen und Bitmaps.
-   **Für Programme mit Toucheingabe- und mobilen Verwendungsszenarien optimieren Sie für 120 dpi.** Bildschirme mit hohem DPI-Wert sind derzeit auf Touch- und mobilen PCs weit verbreitet.
-   **Wenn es sich bei einem Fenster um ein eigenes Fenster handelt, wird es zunächst "zentriert" über dem Besitzerfenster angezeigt.** Nie darunter. Für die nachfolgende Anzeige sollten Sie die Anzeige am letzten Speicherort (relativ zum Besitzerfenster) in Betracht ziehen, wenn dies wahrscheinlich bequemer ist.
-   **Wenn ein Fenster kontextabhängig ist, zeigen Sie es immer in der Nähe des Objekts an, von dem aus es gestartet wurde.** Platzieren Sie es jedoch außerhalb des Wegs (vorzugsweise nach unten und rechts versetzt), sodass das Objekt nicht durch das Fenster abgedeckt wird.

## <a name="layout"></a>Layout

-   **Größensteuerelemente und Bereiche innerhalb eines Fensters entsprechend ihren typischen Inhalten.** Vermeiden Sie abgeschnittenen Text und die zugehörigen Ausellipsen. Benutzer sollten nie mit einem Fenster interagieren müssen, um den typischen Inhalt anzuzeigen. Ändern Sie die Größe, und scrollen Sie nach ungewöhnlich großen Inhalten. Überprüfen Sie insbesondere Folgendes:
    -   **Steuerungsgrößen.** Größe von Steuerelementen auf ihren typischen Inhalt, sodass Steuerelemente bei Bedarf breiter, höher oder mehrzeiliger sind. Größensteuerelemente zum Entfernen oder Reduzieren des Scrollens in Fenstern, die über genügend verfügbaren Speicherplatz verfügen. Außerdem sollte es niemals abgeschnittene Bezeichnungen oder abgeschnittenen Text innerhalb von Fenstern geben, die über genügend verfügbaren Speicherplatz verfügen. Um das Lesen von Text zu vereinfachen, sollten Sie jedoch die Linienbreite auf 65 Zeichen beschränken.
    -   **Spaltenbreiten.** Stellen Sie sicher, dass die Spalten der Listenansicht über die geeignete Standard-, Mindest- und Maximale Größe verfügen. Wählen Sie listenansichten Standardspaltenbreiten aus, die nicht zu abgeschnittenen Text führen, insbesondere dann, wenn in der Listenansicht Platz verfügbar ist.
    -   **Layoutausgleich.** Das Layout eines Fensters sollte ungefähr ausgeglichen sein. Wenn sich das Layout linkslastig anfühlt, sollten Sie erwägen, Steuerelemente breiter zu gestalten und einige Steuerelemente nach rechts zu verschieben.
    -   **Ändern der Layoutgröße.** Wenn die Größe eines Fensters geändert werden kann und Daten abgeschnitten werden, stellen Sie sicher, dass größere Fenster mehr Daten anzeigen. Wenn Daten abgeschnitten werden, erwarten Benutzer, dass die Größe von Fenstern geändert wird, um weitere Informationen anzuzeigen.
-   **Legen Sie eine minimale Fenstergröße fest, wenn eine Größe vorhanden ist, unter der der Inhalt nicht mehr verwendet werden kann.** Legen Sie bei Steuerelementen, deren Größe geändert werden kann, die minimalen Größen für größenveränderbare Elemente auf ihre kleinsten Funktionalen Größen fest, z. B. minimale Funktionale Spaltenbreiten in Listenansichten.

## <a name="text"></a>Text

-   **Verwenden Sie nach Möglichkeit normale Konversationsbegriffe.** Konzentrieren Sie sich auf die Benutzerziele, nicht auf die Technologie. Dies ist besonders effektiv, wenn Sie ein komplexes technisches Konzept oder eine komplexe Aktion erläutern. Imagine sich selbst über die Benutzer schauen und erläutern, wie die Aufgabe ausgeführt werden kann.
-   **Seien Sie heiter, heiter und ermutigend.** Der Benutzer sollte sich nie verhört, beschimpft oder eingeschüchtet fühlen.
-   **Entfernen Sie redundanten Text.** Suchen Sie in Fenstertiteln, Hauptanweisungen, zusätzlichen Anweisungen, Inhaltbereichen, Befehlslinks und Commitschaltflächen nach redundanten Text. Lassen Sie im Allgemeinen den vollständigen Text in den Hauptanweisungen und interaktiven Steuerelementen, und entfernen Sie redundanzen von den anderen Stellen.
-   **Verwenden Sie Die Groß-/Großschreibung im Titelstil für Titel und die Großschreibung im Satzstil für alle anderen Benutzeroberflächenelemente.** Dies ist für den Windows Tonfall besser geeignet.
    -   **Ausnahme:** Bei älteren Anwendungen können Sie bei Bedarf großgeschriebene Titel für Befehlsschaltflächen, Menüs und Spaltenüberschriften verwenden, um großgeschriebene Stile zu vermeiden.
-   **Bei Feature- und Technologienamen ist die Großschreibung konservativer.** In der Regel sollten nur Hauptkomponenten großgeschrieben werden (mithilfe der Groß-/Großschreibung im Titelstil).
-   **Bei Feature- und Technologienamen ist die Groß-/Großschreibung konsistent.** Wenn der Name auf einem Benutzeroberflächenbildschirm mehr als einmal angezeigt wird, sollte er immer auf die gleiche Weise angezeigt werden. Ebenso sollte der Name auf allen Bildschirmen der Benutzeroberfläche im Programm konsistent dargestellt werden.
-   **Groß-/Großschreibung der Namen generischer Benutzeroberflächenelemente wie** Symbolleiste, Menü, Scrollleiste, Schaltfläche und Symbol nicht.
    -   **Ausnahmen:** Adressleiste, Linkleiste, Menüband.
-   **Verwenden Sie nicht alle Großbuchstaben für Tastaturtasten.** Befolgen Sie stattdessen die von Standardtastaturen verwendete Groß-/Kleinschreibung oder Kleinbuchstaben, wenn die Taste nicht auf der Tastatur beschriftet ist.
-   **Ellipsen bedeuten Unvollständigkeit.** Verwenden Sie Ellipsen im Benutzeroberflächentext wie folgt:
    -   **Befehle.** Geben Sie an, dass ein Befehl zusätzliche Informationen benötigt. Verwenden Sie keine Auslassungszeichen, wenn eine Aktion ein anderes Fenster anzeigt – nur wenn zusätzliche Informationen erforderlich sind. Befehle, deren implizites Verb das Anzeigen eines anderen Fensters ist, nehmen keine Auslassungszeichen wie Erweitert, Hilfe, Optionen, Eigenschaften oder Einstellungen.
    -   **Daten.** Geben Sie an, dass Text abgeschnitten wird.
    -   **Etiketten.** Geben Sie an, dass eine Aufgabe ausgeführt wird (z. B. "Suchen...").

**Tipp:** Abgeschnittener Text in einem Fenster oder einer Seite mit nicht verwendeter Fläche weist auf ein schlechtes Layout oder eine zu kleine Standardfenstergröße hin. Achten Sie auf Layouts und Standardfenstergrößen, die die Menge abgeschnittenen Texts beseitigen oder verringern. Weitere Informationen finden Sie unter [Layout](vis-layout.md).

-   **Verwenden Sie keinen blauen Text, der kein Link ist, da Benutzer davon ausgehen können, dass es sich um einen Link handelt.** Verwenden Sie fett oder grau, wo Sie andernfalls farbigen Text verwenden würden.
-   **Verwenden Sie fett, um die Aufmerksamkeit auf Text zu lenken, den Benutzer lesen müssen.**
-   **Verwenden Sie die Hauptanweisung, um präzise zu erläutern, was Benutzer in einem bestimmten Fenster oder auf einer bestimmten Seite tun sollten.** Gute Hauptanweisungen kommunizieren das Ziel des Benutzers, anstatt sich nur auf die Bearbeitung der Benutzeroberfläche zu konzentrieren.
-   **Ausdrücken der Hauptanweisung in Form einer imperativen Richtung oder einer bestimmten Frage.**
-   **Platzieren Sie keine Zeiträume am Ende von Steuerelementbezeichnungen oder Hauptanweisungen.**
-   **Verwenden Sie ein Leerzeichen zwischen Sätzen.** Nicht zwei.

## <a name="controls"></a>Steuerelemente

-   **Allgemein**
    -   **Bezeichnen Sie jedes Steuerelement oder jede Gruppe von Steuerelementen. Ausnahmen:**
        -   Textfelder und Dropdownlisten können mithilfe von Eingabeaufforderungen bezeichnet werden.
        -   Untergeordnete Steuerelemente verwenden die Bezeichnung ihres zugeordneten Steuerelements. Drehsteuerelemente sind immer untergeordnete Steuerelemente.
    -   **Wählen Sie für alle Steuerelemente den sichersten Wert (um Daten- oder Systemzugriffsverluste zu verhindern) standardmäßig aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie den wahrscheinlichsten oder bequemsten Wert aus.
    -   **Eingeschränkte Steuerelemente bevorzugen.** Verwenden Sie nach Möglichkeit eingeschränkte Steuerelemente wie Listen und Schieberegler anstelle von uneingeschränkten Steuerelementen wie Textfeldern, um die Notwendigkeit von Texteingaben zu reduzieren.
    -   **Deaktivierte Steuerelemente wurden deaktiviert.** Deaktivierte Steuerelemente können schwierig zu verwenden sein, da Benutzer wörtlich ableiten müssen, warum sie deaktiviert sind. Deaktivieren Sie ein Steuerelement, wenn Benutzer erwarten, dass es angewendet wird, und sie können leicht ableiten, warum das Steuerelement deaktiviert ist. Entfernen Sie das Steuerelement, wenn es für Benutzer nicht möglich ist, es zu aktivieren, oder sie nicht erwarten, dass es angewendet wird, oder lassen Sie es aktiviert, geben Sie jedoch eine Fehlermeldung an, wenn es falsch verwendet wird.
        -   **Tipp:** Wenn Sie nicht sicher sind, ob Sie ein Steuerelement deaktivieren oder eine Fehlermeldung bereitstellen sollten, erstellen Sie zunächst die Fehlermeldung, die Sie möglicherweise angeben. Wenn die Fehlermeldung hilfreiche Informationen enthält, die Zielbenutzer wahrscheinlich nicht schnell ableiten, lassen Sie das Steuerelement aktiviert, und geben Sie den Fehler an. Andernfalls deaktivieren Sie das Steuerelement.
-   **Befehlsschaltflächen**
    -   **Bevorzugen Sie bestimmte Bezeichnungen gegenüber generischen Bezeichnungen.** Im Idealfall sollten Benutzer nichts anderes lesen müssen, um die Bezeichnung zu verstehen. Die Wahrscheinlichkeit, dass Benutzer Befehlsschaltflächenbezeichnungen lesen, ist weitaus wahrscheinlicher als statischer Text.
        -   **Ausnahme:** Benennen Sie die Schaltfläche Abbrechen nicht um, wenn die Bedeutung des Abbrechens eindeutig ist. Benutzer sollten nicht alle Schaltflächen lesen müssen, um zu bestimmen, welche Schaltfläche eine Aktion abbricht. Benennen Sie Cancel jedoch um, wenn unklar ist, welche Aktion abgebrochen wird, z. B. wenn mehrere ausstehende Aktionen vorhanden sind.
    -   **Wenn Sie eine Frage stellen, verwenden Sie Bezeichnungen, die mit der Frage übereinstimmen.** Geben Sie beispielsweise Ja- und Nein-Antworten auf eine Ja- oder Nein-Frage an.
    -   **Verwenden Sie keine Schaltflächen anwenden in Dialogfeldern, bei denen es sich nicht um Eigenschaftenblätter oder Systemsteuerungselemente handelt.** Die Schaltfläche Anwenden bedeutet, dass die ausstehenden Änderungen angewendet werden, aber lassen Sie das Fenster geöffnet. Auf diese Weise können Benutzer die Änderungen vor dem Schließen des Fensters auswerten. Allerdings ist dies nur für Eigenschaftenblätter und Systemsteuerungselemente erforderlich.
    -   Beschriften sie eine Schaltfläche Abbrechen, wenn beim Abbrechen die Umgebung in den vorherigen Zustand zurückgesetzt wird (ohne Nebeneffekt). Beschriften Sie andernfalls die Schaltfläche Schließen (wenn der Vorgang abgeschlossen ist) oder Beenden (wenn der Vorgang ausgeführt wird), um anzugeben, dass der aktuelle geänderte Zustand unverändert bleibt.
-   **Befehlslinks**
    -   **Befehlslinks werden immer in einer Gruppe von zwei oder mehr Befehlslinks dargestellt.** Logischerweise gibt es keinen Grund, eine Frage mit nur einer Antwort zu stellen.
    -   **Geben Sie eine explizite Schaltfläche Abbrechen an.** Verwenden Sie zu diesem Zweck keinen Befehlslink. Häufig stellen Benutzer fest, dass sie keine Aufgabe ausführen möchten. Wenn Sie einen Befehlslink zum Abbrechen verwenden, müssen Benutzer alle Befehlslinks sorgfältig lesen, um zu bestimmen, welcher Befehl abgebrochen werden soll. Mit einer expliziten Schaltfläche Abbrechen können Benutzer eine Aufgabe effizient abbrechen.
    -   **Wenn eine explizite Schaltfläche Abbrechen einen einzelnen Befehlslink verlässt, geben Sie sowohl einen Befehlslink zum Abbrechen als auch eine Schaltfläche Abbrechen an.** Dadurch wird deutlich, dass Benutzer eine Auswahl treffen können. Formulieren Sie diesen Befehlslink in Bezug darauf, wie er sich von der ersten Antwort unterscheidet, anstatt nur "Abbrechen" oder eine Variation.
-   **Kontrollkästchen "Dies nicht \<item\> erneut anzeigen"**
    -   **Erwägen Sie die Verwendung der Option "Dies nicht \<item\> erneut anzeigen", damit Benutzer ein wiederkehrendes Dialogfeld nur unterdrücken können, wenn es keine bessere Alternative gibt.** Es ist besser, den Dialog immer anzuzeigen, wenn er wirklich von Benutzern benötigt wird, oder ihn einfach zu entfernen, wenn dies nicht dere ist.
    -   **Ersetzen Sie durch \<item\> das spezifische Element.** Zeigen Sie diese Erinnerung z. B. nicht erneut an. Wenn Sie im Allgemeinen auf ein Dialogfeld verweisen, verwenden Sie Diese Meldung nicht mehr anzeigen.
    -   **Geben Sie eindeutig an, wann benutzereingaben für zukünftige Standardwerte verwendet werden sollen,** indem Sie den folgenden Satz unter der Option hinzufügen: Ihre Auswahl wird in Zukunft standardmäßig verwendet.
    -   **Wählen Sie die Option nicht standardmäßig aus. Wenn das Dialogfeld wirklich nur einmal angezeigt werden soll, tun Sie dies ohne Nachfrage.** Verwenden Sie diese Option nicht als Versuch, Benutzer zu verärgern. Stellen Sie sicher, dass das Standardverhalten nicht mäßig ist.
    -   **Wenn Benutzer die Option auswählen und auf Abbrechen klicken, wird diese Option wirksam.** Diese Einstellung ist eine Metaoption, sodass sie nicht dem standardmäßigen Cancel-Verhalten entspricht, bei dem keine Nebeneffekte übrig bleiben. Beachten Sie Folgendes: Wenn Benutzer den Dialog in Zukunft nicht sehen möchten, möchten sie es wahrscheinlich auch abbrechen.
-   **Links**
    -   **Weisen Sie keinen** [Zugriffsschlüssel](glossary.md)zu. Der Zugriff auf Links erfolgt über die TAB-TASTE.
    -   **Fügen Sie dem Linktext nicht "Click" oder "Click here" hinzu.** Dies ist nicht erforderlich, da ein Link ein Klicken impliziert.
-   **QuickInfos**
    -   **Verwenden Sie QuickInfos, um Bezeichnungen für Steuerelemente ohne Bezeichnung bereitzustellen.** Aus Gründen der Konsistenz müssen Sie keine QuickInfos für beschriftete Steuerelemente geben.
    -   **QuickInfos können auch ausführlichere Informationen für beschriftete Symbolleistenschaltflächen bereitstellen, wenn dies hilfreich ist.** Wiederholen Sie nicht einfach das, was bereits in der Bezeichnung vorhanden ist, oder geben Sie eine wortliche Neustellung an.
    -   **Vermeiden Sie das Abdecken des Objekts, das der Benutzer anzeigen oder mit dem er interagieren soll.** Platzieren Sie den Tipp immer auf der Seite des Objekts, auch wenn dies eine Trennung zwischen zeiger und tip erfordert. Eine Trennung ist kein Problem, solange die Beziehung zwischen dem Objekt und seinem Trinkgeld klar ist.
        -   **Ausnahme:** QuickInfos mit vollständigem Namen, die in Listen und Strukturen verwendet werden.
    -   **Vermeiden Sie bei Auflistungen von Elementen das Abdecken des nächsten Objekts, das der Benutzer wahrscheinlich anzeigen oder mit dem er interagieren wird.** Vermeiden Sie bei horizontal angeordneten Elementen das Platzieren von Tipps auf der rechten Seite. Für vertikal angeordnete Elemente vermeiden Sie das Platzieren von Tipps unten.
-   **Schrittweise Offenlegung**
    -   **Verwenden Sie mehr/weniger Schaltflächen für die progressive Offenlegung, um erweiterte oder selten verwendete Optionen, Befehle und Details auszublenden, die Benutzer in der Regel nicht benötigen.** Blenden Sie häufig verwendete Elemente nicht aus, da Benutzer sie möglicherweise nicht finden. Stellen Sie jedoch sicher, dass alles, was ausgeblendet ist, einen Wert hat.
    -   Wenn auf der Oberfläche immer einige Optionen, Befehle oder Details angezeigt werden, verwenden Sie die folgenden Bezeichnungspaare:
        -   **Mehr/Weniger Optionen.** Verwenden Sie für Optionen oder eine Mischung aus Optionen, Befehlen und Details.
        -   **Mehr/Weniger Befehle.** Nur für Befehle verwenden.
        -   **Weitere/weniger Details.** Verwenden Sie nur für Informationen.
        -   **Mehr/weniger \<object name\> .** Verwenden Sie für andere Objekttypen, z. B. Ordner.
    -   Andernfalls:
        -   **Optionen zum Ein-/Ausblenden.** Verwenden Sie für Optionen oder eine Mischung aus Optionen, Befehlen und Details.
        -   **Befehle ein-/ausblenden.** Nur für Befehle verwenden.
        -   **Details ein-/ausblenden.** Verwenden Sie nur für Informationen.
        -   **Ein-/Ausblenden \<object name\> von .** Verwenden Sie für andere Objekttypen, z. B. Ordner.
-   **Statusanzeigen**
    -   **Verwenden Sie determinierte Statusanzeigen für Vorgänge, die eine bestimmte Zeitspanne erfordern,** auch wenn diese Zeitspanne nicht genau vorhergesagt werden kann. Unbestimmte Statusanzeigen zeigen an, dass der Fortschritt ausgeführt wird, geben aber keine weiteren Informationen an. Wählen Sie keine unbestimmte Statusanzeige aus, die nur auf der möglichen fehlenden Genauigkeit basiert.
    -   **Geben Sie eine schätzungsweise verbleibende Zeit an, wenn Sie dies genau tun können.** Genaue Schätzungen der verbleibenden Zeit sind nützlich, aber Schätzungen, die weit von der Marke entfernt sind oder deutlich abprallen, sind nicht hilfreich. Möglicherweise müssen Sie einige Verarbeitungsaufgaben ausführen, bevor Sie genaue Schätzungen vornehmen können. In diesem Falle sollten Sie während dieses anfänglichen Zeitraums keine potenziell ungenauen Schätzungen anzeigen.
    -   **Starten Sie den Fortschritt nicht neu.** Eine Statusanzeige verliert ihren Wert, wenn sie neu gestartet wird (möglicherweise weil ein Schritt im Vorgang abgeschlossen wird), da Benutzer nicht wissen können, wann der Vorgang abgeschlossen wird. Lassen Sie stattdessen alle Schritte im Vorgang einen Teil des Fortschritts teilen, und lassen Sie die Statusanzeige einmal abgeschlossen werden.
    -   **Geben Sie nützliche Statusdetails an.** Geben Sie zusätzliche Statusinformationen an, aber nur, wenn Benutzer damit etwas tun können. Stellen Sie sicher, dass der Text lange genug angezeigt wird, damit Benutzer ihn lesen können.
    -   **Kombinieren Sie keine Statusanzeige mit einem ausgelasteten Zeiger.** Verwenden Sie das eine oder das andere, aber nicht beide gleichzeitig.
-   **Eingabeaufforderungen**
    -   **Verwenden Sie eine Eingabeaufforderung, wenn der Bildschirmbereich so premium ist, dass die Verwendung einer Bezeichnung oder Anweisung unerwünscht ist,** z. B. auf einer Symbolleiste.
    -   **Die Eingabeaufforderung dient in erster Linie dazu, den Zweck des Textfelds oder Kombinationsfelds auf kompakte Weise zu identifizieren.** Es dürfen keine entscheidenden Informationen sein, die der Benutzer bei der Verwendung des Steuerelements sehen muss.
    -   **Der Eingabeaufforderungstext darf nicht mit echtem Text verwechselt werden.** Dazu ist Folgendes erforderlich:
        -   Zeichnen Sie den Eingabeaufforderungstext in italischem Grau und den tatsächlichen Eingabetext in romanischem Schwarz.
        -   Der Eingabeaufforderungstext sollte nicht bearbeitbar sein und nicht mehr angezeigt werden, sobald Benutzer auf das Textfeld klicken oder die Registerkarte öffnen.
            -   **Ausnahme:** Wenn das Textfeld über den Standardeingabefokus verfügt, wird die Eingabeaufforderung angezeigt und verschwindet, sobald der Benutzer mit der Eingabe beginnt.
    -   Verwenden Sie keine endenden Interpunktionen oder Auslassungszeichen.
-   **Benachrichtigungen**
    -   **Verwenden Sie Benachrichtigungen für Ereignisse, die nicht mit der aktuellen Benutzeraktivität in Zusammenhang stehen, keine sofortige Benutzeraktion erfordern und Benutzer frei ignorieren können.**
    -   **Benachrichtigungen nicht missbrauchen:**
        -   **Verwenden Sie Benachrichtigungen nur bei Bedarf.** Wenn Sie eine Benachrichtigung anzeigen, unterbrechen Sie möglicherweise Benutzer oder stören sie sogar. Stellen Sie sicher, dass die Unterbrechung gerechtfertigt ist.
        -   **Verwenden Sie Benachrichtigungen für nicht kritische Ereignisse oder Situationen, die keine sofortige Benutzeraktion erfordern.** Verwenden Sie für kritische Ereignisse oder Situationen, die eine sofortige Benutzeraktion erfordern, ein alternatives Benutzeroberflächenelement (z. B. ein modales Dialogfeld).
        -   **Verwenden Sie keine Benachrichtigungen für Featureanzeigen!**

## <a name="keyboard"></a>Tastatur

-   **Weisen Sie dem Steuerelement,** mit dem Benutzer höchstwahrscheinlich zuerst interagieren, den anfänglichen Eingabefokus zu. Dies ist häufig das erste interaktive Steuerelement. Wenn das erste interaktive Steuerelement keine gute Wahl ist, sollten Sie das Layout des Fensters ändern.
-   **Zuweisen von Registerkartenstopps zu allen interaktiven Steuerelementen, einschließlich schreibgeschützter Bearbeitungsfelder. Ausnahmen:**
    -   Gruppen von verwandten Steuerelementen, die sich wie ein einzelnes Steuerelement verhalten, z. B. Optionsfelder. Solche Gruppen verfügen über einen einzelnen Tabstopp.
    -   Sie müssen Gruppen ordnungsgemäß enthalten, damit die Pfeiltasten innerhalb der Gruppe vorwärts und rückwärts zyklen und innerhalb der Gruppe bleiben.
-   **Die Reihenfolge der Registerkarten sollte von links nach rechts, von oben nach unten fließen.** Im Allgemeinen sollte die Reihenfolge der Registerkarten der Lese reihenfolge folgen. Erwägen Sie, Ausnahmen für häufig verwendete Steuerelemente zu machen, indem Sie sie früher in der Reihenfolge der Registerkarten setzen. Die Registerkarte sollte alle Registerkartenstopps in beide Richtungen durchzyklen, ohne anzuhalten. Innerhalb einer Gruppe sollte die Reihenfolge der Registerkarten ohne Ausnahmen sequenziell sein.
-   **Innerhalb eines Tabstopps sollte die Reihenfolge der Pfeiltasten** ohne Ausnahmen von links nach rechts, von oben nach unten fließen. Die Pfeiltasten sollten alle Elemente in beide Richtungen durchzyklen, ohne anzuhalten.
-   **Stellen Sie die Commitschaltflächen in der folgenden Reihenfolge vor:**
    -   OK/ \[ Do it \] /Yes
    -   \[Don't do it \] /No
    -   Abbrechen
    -   Übernehmen (falls vorhanden)

Dabei handelt es sich bei "Do it" und \[ \] \[ "Don't do" \] um spezifische Antworten auf die Main-Anweisung.

-   **Verwechseln Sie Zugriffsschlüssel nicht mit Tastenkombinationen.** Obwohl sowohl Zugriffstasten als auch Tastenkombinationen den Tastaturzugriff auf die Benutzeroberfläche ermöglichen, haben sie unterschiedliche Zwecke und Richtlinien.
-   **Weisen Sie nach Möglichkeit allen interaktiven Steuerelementen oder deren Bezeichnungen eindeutige Zugriffsschlüssel zu.** [Schreibgeschützte Textfelder sind](ctrl-text-boxes.md) interaktive Steuerelemente (da Benutzer scrollen und Text kopieren können), sodass sie von Zugriffsschlüsseln profitieren. **Weisen Sie keine Zugriffsschlüssel zu:**
    -   Schaltflächen OK, Abbrechen und Schließen. Eingabe und ESC werden für ihre Zugriffsschlüssel verwendet. Weisen Sie einem Steuerelement jedoch immer einen Zugriffsschlüssel zu, der OK oder Abbrechen bedeutet, aber eine andere Bezeichnung hat.
-   **Weisen Sie den am häufigsten verwendeten Befehlen Tastenkombinationen zu.** Selten verwendete Programme und Features benötigen keine Tastenkombinationen, da Benutzer stattdessen Zugriffsschlüssel verwenden können.
-   **Machen Sie keine Tastenkombination zur einzigen Möglichkeit, eine Aufgabe auszuführen.** Benutzer sollten auch in der Lage sein, die Maus oder tastatur mit TAB-TASTE, Pfeil und Zugriffstasten zu verwenden.
-   **Weisen Sie bekannten Tastenkombinationen keine anderen Bedeutungen zu.** Da sie auswendig sind, sind inkonsistente Bedeutungen für bekannte Verknüpfungen frustrierend und fehleranfällig.
-   **Versuchen Sie nicht, systemweite Programmtasten zu zuweisen.** Die Tastenkombinationen Des Programms haben nur dann Auswirkungen, wenn ihr Programm den Eingabefokus besitzt.

## <a name="mouse"></a>Maus

-   **Erfordern Sie niemals, dass Benutzer auf ein Objekt klicken, um zu bestimmen, ob es angeklickt werden kann.** Benutzer müssen die Klickbarkeit allein durch visuelle Überprüfung bestimmen können.
    -   Die primäre Benutzeroberfläche (z. B. Commitschaltflächen) muss über ein statisches Klick-Affordance verfügen. Benutzer sollten nicht darauf bewegen müssen, um die primäre Benutzeroberfläche zu entdecken.
    -   Die sekundäre Benutzeroberfläche (z. B. sekundäre Befehle oder Steuerelemente für die progressive Offenlegung) kann ihr Klick-Affordance beim Zeigen anzeigen.
    -   Textlinks sollten linktext statisch vorschlagen und dann ihr Klick-Affordance (Unterstrich oder andere Präsentationsänderung, mit Handzeiger) anzeigen, wenn Sie darauf zeigen.
    -   Grafiklinks zeigen nur einen Handzeiger an, wenn darauf gezeigt wird.
-   **Verwenden Sie den Handzeiger (oder "Linkauswahl") nur für Text- und Grafiklinks.** Andernfalls müssten Benutzer auf Objekte klicken, um zu ermitteln, ob es sich um Links handelt.

## <a name="dialog-boxes"></a>Dialogfelder

-   **Modale Dialogfelder erfordern eine Interaktion. Verwenden Sie sie daher für Dinge, auf die Benutzer reagieren müssen, bevor sie mit ihrer Aufgabe fortfahren.** Stellen Sie sicher, dass die Unterbrechung gerechtfertigt ist, z. B. bei kritischen oder seltenen einmaligen Aufgaben, die abgeschlossen werden müssen. Ziehen Sie andernfalls moduslose Alternativen in Betracht.
-   **Für nicht moduslose Dialogfelder ist keine Interaktion erforderlich. Verwenden Sie sie daher, wenn Benutzer zwischen einem Dialogfeld und dem Besitzerfenster wechseln müssen.** Sie werden am besten für häufige, sich wiederholende oder laufende Aufgaben verwendet. Menübänder, Symbolleisten und Palettenfenster sind jedoch häufig bessere Alternativen.

## <a name="property-sheets"></a>Eigenschaftenblätter

-   **Stellen Sie sicher, dass die Eigenschaften erforderlich sind.** Überladen Sie Ihre Eigenschaftenseiten nicht mit unnötigen Eigenschaften, nur um keine hartgeformten Entwurfsentscheidungen zu treffen.
-   **Präsentieren Sie Eigenschaften in Bezug auf Benutzerziele anstelle von Technologie.** Nur weil eine Eigenschaft eine bestimmte Technologie konfiguriert, bedeutet dies nicht, dass Sie die Eigenschaft in Bezug auf diese Technologie präsentieren müssen.
    -   Wenn Sie Einstellungen in Bezug auf die Technologie angeben müssen (z. B. weil Ihre Benutzer den Namen der Technologie erkennen), geben Sie eine kurze Beschreibung des Benutzervorteils an.
-   **Verwenden Sie spezifische, aussagekräftige Registerkartenbezeichnungen.** Vermeiden Sie generische Registerkartenbezeichnungen, die auf alle Registerkarten angewendet werden können, z. B. Allgemein, Erweitert oder Einstellungen.
-   **Vermeiden Sie allgemeine Seiten.** Sie müssen nicht über eine Seite Allgemein verfügen. Verwenden Sie eine Seite Allgemein nur, wenn:
    -   Die Eigenschaften gelten für mehrere Aufgaben und sind für die meisten Benutzer sinnvoll. Legen Sie keine speziellen oder erweiterten Eigenschaften auf der Seite Allgemein ab, aber Sie können sie über eine Befehlsschaltfläche auf der Seite Allgemein zugänglich machen.
    -   Die Eigenschaften passen nicht zu einer spezifischeren Kategorie. Wenn sie dies tun, verwenden Sie stattdessen diesen Namen für die Seite.
-   **Vermeiden Sie Erweiterte Seiten.** Verwenden Sie eine Seite Erweitert nur, wenn:
    -   Die Eigenschaften gelten für ungewöhnliche Aufgaben und sind in erster Linie für fortgeschrittene Benutzer sinnvoll.
    -   Die Eigenschaften passen nicht zu einer spezifischeren Kategorie. Wenn sie dies tun, verwenden Sie stattdessen diesen Namen für die Seite.
-   **Verwenden Sie keine Registerkarten, wenn ein Eigenschaftenfenster nur über eine einzige Registerkarte verfügt und nicht erweiterbar ist.** Verwenden Sie stattdessen ein reguläres Dialogfeld mit OK, Abbrechen und einer optionalen Schaltfläche Anwenden. Erweiterbare Eigenschaftenfenster (die von Drittanbietern erweitert werden können) müssen jedoch Registerkarten verwenden.

## <a name="wizards"></a>Assistenten

-   **Ziehen Sie zunächst einfache Alternativen in Betracht, z. B. Dialogfelder, Aufgabenbereiche oder einzelne Seiten.** Assistenten sind eine hohe Benutzeroberfläche, die am besten für aufgabenbasierte, selten ausgeführte Mehrschritte verwendet wird. Sie müssen keine Assistenten verwenden. Sie können hilfreiche Informationen und Unterstützung auf jeder Benutzeroberfläche bereitstellen.
-   **Verwenden Sie Weiter nur, wenn Sie ohne Verpflichtung zur nächsten Seite überschreiten.** Der Fortschritt zur nächsten Seite wird als Verpflichtung betrachtet, wenn deren Auswirkung nicht durch Klicken auf Zurück oder Abbrechen rückgängig gemacht werden kann.
-   **Verwenden Sie nur Zurück, um Fehler zu beheben.** Abgesehen von der Korrektur von Fehlern sollten Benutzer nicht auf Zurück klicken müssen, um einen Fortschritt in einer Aufgabe zu erzielen.
-   **Wenn Benutzer einen Commit für eine Aufgabe committen, verwenden Sie eine Commitschaltfläche, die eine bestimmte Antwort auf die Main-Anweisung ist (z. B. Drucken, Verbinden oder Starten).** Verwenden Sie keine generischen Bezeichnungen wie Next (was keine Verpflichtung impliziert) oder Finish (was nicht spezifisch ist) für das Committen einer Aufgabe. Die Bezeichnungen auf diesen Commitschaltflächen sollten allein sinnvoll sein. Starten Sie die Schaltflächenbezeichnungen für Commits immer mit einem Verb. **Ausnahmen:**
    -   Verwenden Sie Fertig stellen, wenn die spezifischen Antworten immer noch generisch sind, z. B. Speichern, Auswählen, Auswählen oder Get.
    -   Verwenden Sie Fertig stellen, um eine bestimmte Einstellung oder eine Sammlung von Einstellungen zu ändern.
-   **Verwenden Sie Befehlslinks nur für Auswahlmöglichkeiten, nicht für Verpflichtungen.** Bestimmte Commitschaltflächen weisen auf eine deutlich bessere Verpflichtung hin als Befehlslinks in einem Assistenten.
-   **Wenn Sie Befehlslinks verwenden, blenden Sie die Schaltfläche Weiter aus, aber lassen Sie die Schaltfläche Abbrechen.**
-   **Verwenden Sie Schließen für Follow-Up und Vervollständigungsseiten.** Verwenden Sie Abbrechen nicht, da durch das Schließen des Fensters keine Änderungen oder Aktionen abgebrochen werden, die an diesem Punkt vorgenommen wurden. Verwenden Sie Done nicht, da es sich nicht um ein imperatives Verb handelt.
-   **Verwenden Sie "Assistent" nicht in Assistentennamen.** Verwenden Sie beispielsweise "Verbinden zu einem Netzwerk" anstelle von "Netzwerk Setup-Assistant". Es ist jedoch akzeptabel, Assistenten als Assistenten zu bezeichnen. Beispiel: "Wenn Sie zum ersten Mal ein Netzwerk einrichten, können Sie Hilfe erhalten, indem Sie den Assistenten Verbinden Netzwerk verwenden."
-   **Behalten Sie die Benutzerauswahl über die Navigation bei.** Wenn der Benutzer z. B. Änderungen vorsingt, auf Zurück und dann auf Weiter klickt, sollten diese Änderungen beibehalten werden. Benutzer erwarten nicht, dass sie Änderungen erneut eingeben müssen, es sei denn, sie haben sich explizit dafür entschieden, sie zu löschen.

## <a name="wizard-pages"></a>Seiten des Assistenten

-   **Konzentrieren Sie sich auf eine effiziente Entscheidungsfindung.** Reduzieren Sie die Anzahl der Seiten, um sich auf das Wesentliche zu konzentrieren. Konsolidieren Sie verwandte Seiten, und nehmen Sie optionale Seiten aus dem Hauptfluss heraus. Wenn Benutzer im Assistenten vollständig auf Weiter klicken, scheint es zunächst eine gute Erfahrung zu sein, aber wenn Benutzer die Standardwerte nie ändern müssen, sind die Seiten wahrscheinlich unnötig.
-   **Verwenden Sie keine Willkommensseiten. Sorgen Sie dafür, dass die erste Seite nach Möglichkeit funktionsfähig ist.** Verwenden Sie eine optionale Erste Schritte nur in den:
    -   Der Assistent verfügt über voraussetzungen, die erforderlich sind, um den Assistenten erfolgreich abzuschließen.
    -   Benutzer können den Zweck des Assistenten basierend auf der ersten Auswahlseite möglicherweise nicht verstehen, und es gibt keinen Raum für weitere Erläuterungen.
    -   Die Hauptanweisung für Erste Schritte seiten ist "Before you begin:".
-   **Optimieren Sie auf Seiten, auf denen Benutzer zur Auswahl aufgefordert werden, für die wahrscheinlichsten Fälle.** Diese Arten von Seiten sollten tatsächliche Auswahlmöglichkeiten bieten, nicht nur Anweisungen.
    -   Wenn Sie keine Seite Erste Schritte, erläutern Sie den Zweck des Assistenten oben auf der ersten Auswahlseite.
-   **Verwenden Sie Commitseiten, um deutlich zu machen, wann Benutzer einen Commit für die Aufgabe committen.** In der Regel ist die Commitseite die letzte Auswahlseite, und die Schaltfläche Weiter wird neu bezeichnet, um anzugeben, für welche Aufgabe ein Commit erfolgt.
    -   Verwenden Sie keine Zusammenfassungsseiten, die lediglich die vorherigen Auswahlen des Benutzers zusammenfassen, es sei denn, die Aufgabe ist riskant (mit Sicherheit oder Zeit- oder Geldverlust), oder es besteht die gute Möglichkeit, dass Benutzer ihre Auswahl nicht verstehen und sie überprüfen müssen.
-   **Verwenden Sie keine Herzlichen Glückwunschseiten, die nichts anderes tun, als den Assistenten zu beenden.** Wenn die Ergebnisse des Assistenten für Benutzer deutlich erkennbar sind, schließen Sie einfach den Assistenten auf der Schaltfläche für den endgültigen Commit.
    -   Verwenden Follow-Up Seiten, wenn es verwandte Aufgaben gibt, die Benutzer wahrscheinlich im Anschluss ausführen werden. Vermeiden Sie vertraute Folgeaufgaben, z. B. "E-Mail-Nachricht senden".
    -   Verwenden Sie Vervollständigungsseiten nur, wenn die Ergebnisse nicht sichtbar sind und es keine bessere Möglichkeit gibt, Feedback zur Aufgabenerledigung zu geben.
    -   Assistenten mit Statusseiten müssen eine Abschlussseite oder eine Follow-Up verwenden, um den Abschluss der Aufgabe anzugeben. Schließen Sie den Assistenten auf der Seite Commit, und verwenden Sie Benachrichtigungen, um Feedback zu geben.

## <a name="error-messages"></a>Fehlermeldungen

-   **Geben Sie keine Fehlermeldungen aus, wenn** Benutzer wahrscheinlich keine Aktion ausführen oder ihr Verhalten als Ergebnis der Nachricht ändern. Wenn es keine Aktion gibt, die Benutzer ergreifen können, oder wenn das Problem nicht signifikant ist, unterdrücken Sie die Fehlermeldung.
-   **Schlagen Sie nach Möglichkeit eine Lösung vor, damit Benutzer das Problem beheben können.** Stellen Sie jedoch sicher, dass das Problem wahrscheinlich durch die vorgeschlagene Lösung gelöst wird. Verschwenden Sie die Zeit der Benutzer nicht, indem Sie mögliche, aber nicht unwahrscheinliche Lösungen vorschlagen.
-   **Seien Sie spezifisch.** Vermeiden Sie ungenaue Formulierungen, z. B. Syntaxfehler und unzulässige Operation. Geben Sie bestimmte Namen, Speicherorte und Werte der beteiligten Objekte an.
-   **Verwenden Sie keinen Ausdruck, der den Benutzer verantwortlich macht oder einen Benutzerfehler impliziert.** Vermeiden Sie es, Sie und im Ausdruck zu verwenden. Obwohl die aktive Stimme im Allgemeinen bevorzugt wird, verwenden Sie die passive Stimme, wenn der Benutzer das Subjekt ist, und können sich für den Fehler verantwortlich machen, wenn die aktive Stimme verwendet wird.
-   **Verwenden Sie für Fehlermeldungen nicht OK.** Benutzer sehen Fehler nicht als ok. Wenn die Fehlermeldung keine direkte Aktion enthält, verwenden Sie stattdessen Schließen.
-   **Verwenden Sie nicht die folgenden Wörter:**
    -   Fehler, Fehler (verwenden Sie stattdessen Problem)
    -   Failed to (use unable to instead)
    -   Ungültig, ungültig, ungültig (verwenden Sie stattdessen falsch oder ungültig)
    -   Abbrechen, Beenden, Beenden (stattdessen beenden)
    -   Schwerwiegend, schwerwiegend (verwenden Sie stattdessen "schwerwiegend")

Diese Begriffe sind unnötig und stehen im Gegensatz zum ermutigenden Tonfall Windows. Stattdessen gibt ein Fehlersymbol bei [ordnungsgemäßer Verwendung](vis-std-icons.md)ausreichend an, dass ein Problem vor liegt.

-   **Begleiten Sie Fehlermeldungen nicht mit Soundeffekten.** Dies ist nicht erforderlich.

## <a name="warning-messages"></a>Warnmeldungen

-   **Warnungen beschreiben eine Bedingung, die in Zukunft ein Problem verursachen kann.** Warnungen sind keine Fehler oder Fragen. Geben Sie daher keine Routinefragen als Warnungen aus.
-   **Geben Sie keine Warnmeldungen aus, wenn Benutzer wahrscheinlich keine Aktion ausführen oder ihr Verhalten als Ergebnis der Nachricht ändern.** Wenn es keine Aktion gibt, die Benutzer ergreifen können, oder wenn die Bedingung nicht signifikant ist, unterdrücken Sie die Warnmeldung.

## <a name="confirmations"></a>Bestätigungen

-   **Verwenden Sie keine unnötigen Bestätigungen.** Verwenden Sie Bestätigungen nur in den:
    -   Es gibt einen eindeutigen Grund, nicht fortzufahren, und eine angemessene Wahrscheinlichkeit, dass Benutzer dies manchmal nicht machen.
    -   Die Aktion hat erhebliche Folgen oder kann nicht einfach rückgängig gemacht werden.
    -   Die Aktion hat Konsequenzen, die Benutzer möglicherweise nicht kennen.
    -   Wenn Sie mit der Aktion fortfahren, müssen Benutzer eine Auswahl treffen, die keine geeignete Standardeinstellung hat.
    -   Angesichts des aktuellen Kontexts ist es wahrscheinlich, dass Benutzer eine Aktion mit einem Fehler ausgeführt haben.
-   **Bestätigungen von Ausdrücken als "Ja" oder "Nein" und "Ja" oder "Nein" geben Antworten.** Im Gegensatz zu anderen Dialogfeldern sind Bestätigungen so konzipiert, dass Benutzer keine schnellen Entscheidungen treffen können. Wenn Benutzer ihre Antwort nicht berücksichtigen, hat eine Bestätigung keinen Wert.

## <a name="icons"></a>Symbole

-   **Alle Symbole sollten den** [Richtlinien für Symbole im Stil von Stilen entsprechen.](vis-icons.md) Ersetzen Sie Windows Symbole im XP-Stil.
-   **Wählen Sie Standardsymbole basierend auf ihrem Nachrichtentyp und nicht dem Schweregrad des zugrunde liegenden Problems aus:**
    -   **Fehler.** Ein Fehler oder ein Problem, das aufgetreten ist.
    -   **Warnung.** Eine Bedingung, die in Zukunft ein Problem verursachen kann.
    -   **Informationen.** Nützliche Informationen.

Wenn ein Problem verschiedene Nachrichtentypen kombiniert, konzentrieren Sie sich auf den wichtigsten Aspekt, auf den Benutzer agieren müssen.

-   **Symbole müssen immer mit der Hauptanweisung oder einem anderen entsprechenden Text übereinstimmen.**
-   **Fehlersymbole sind für nicht kritische Benutzereingabeprobleme nicht erforderlich.** Für direkte Fehler sind jedoch Symbole erforderlich, da ein solches kontextbezogenes Feedback andernfalls zu leicht übersehen werden kann.
-   **Verwenden Sie keine Warnsymbole, um nicht kritische Fehler zu "entschweisen".** Fehler sind keine Warnungen. Wenden Sie stattdessen die Richtlinien für das Fehlersymbol an.
-   **Verwenden Sie für Fragedialoge nur Warnsymbole für Fragen mit erheblichen Folgen.** Verwenden Sie keine Warnsymbole für routinemäßige Fragen.

## <a name="help"></a>Hilfe

-   **Link zu bestimmten relevanten Hilfethemen.** Verknüpfen Sie nicht die Startseite der Hilfe, das Inhaltsverzeichnis, eine Liste mit Suchergebnissen oder eine Seite, die nur mit anderen Seiten verknüpft ist. Vermeiden Sie das Verknüpfen mit Seiten, die als eine große Liste häufig gestellter Fragen strukturiert sind, da benutzer dazu zwingt, nach der Seite zu suchen, die dem link entspricht, auf den sie geklickt haben. Verknüpfen Sie nicht mit bestimmten Hilfethemen, die für die jeweilige Aufgabe nicht relevant und hilfreich sind. Verlinken Sie niemals mit leeren Seiten.
-   **Stellen Sie aus Gründen der Konsistenz nicht in jedem Fenster oder jeder Seite Hilfelinks.** Das Bereitstellen eines Hilfelinks an einem Ort bedeutet nicht, dass Sie sie überall bereitstellen müssen.
-   **Wenn möglich, verknüpft der Ausdruck Hilfe Text im Hinblick auf die primäre Frage, die durch den Hilfeinhalt beantwortet wird.** Verwenden Sie nicht den Ausdruck "Weitere Informationen" oder "Hilfe dazu erhalten".
-   **Verwenden Sie den gesamten Hilfelink für den Linktext, nicht** nur die Schlüsselwörter.
-   **Verwenden Sie vollständige Sätze.**
-   **Verwenden Sie keine endenden Interpunktionen oder Ausellipsen, mit Ausnahme von Fragezeichen.**
-   **Wenn der Hilfeinhalt online ist, machen Sie dies im Linktext deutlich.** Dies trägt dazu bei, das Ergebnis der Links vorhersagbar zu machen.

