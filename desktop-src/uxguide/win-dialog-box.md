---
title: Dialogfelder (Entwurfsgrundeinstellungen)
description: Ein Dialogfeld ist ein sekundäres Fenster, in dem Benutzer einen Befehl ausführen, Benutzern eine Frage stellen oder Benutzern Informationen oder Fortschrittsfeedback zur Verfügung stellen können.
ms.assetid: 2ded9f30-d45f-4027-a85d-4e7d0e412793
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2fe9b7545961f7e06b1edf1656531779d5122b339d0cf16294e5ef5c4be9a69f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031163"
---
# <a name="dialog-boxes-design-basics"></a>Dialogfelder (Entwurfsgrundeinstellungen)

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Ein Dialogfeld ist ein sekundäres Fenster, in dem Benutzer einen Befehl ausführen, Benutzern eine Frage stellen oder Benutzern Informationen oder Fortschrittsfeedback zur Verfügung stellen können.

![Screenshot: Identifizieren von Dialogfeldelementen ](images/win-dialog-box-image1.png)

Ein typisches Dialogfeld.

Dialogfelder bestehen aus einer Titelleiste (um den Befehl, das Feature oder das Programm zu identifizieren, von dem ein Dialogfeld stammt), einer optionalen Hauptanweisung (um das Ziel des Benutzers mit dem Dialogfeld zu erklären), verschiedenen Steuerelementen im Inhaltsbereich (um Optionen anzuzeigen) und Commitschaltflächen (um anzugeben, wie der Benutzer einen Commit für die Aufgabe ausführen möchte).

Dialogfelder verfügen über zwei grundlegende Typen:

-   **Modale Dialogfelder** erfordern, dass Benutzer abgeschlossen und geschlossen werden, bevor sie mit dem Besitzerfenster fortfahren. Diese Dialogfelder eignen sich am besten für kritische oder seltene, einmalige Aufgaben, die abgeschlossen werden müssen, bevor Sie fortfahren.
-   **Mithilfe von Dialogfeldern ohne** Modus können Benutzer nach Bedarf zwischen dem Dialogfeld und dem Besitzerfenster wechseln. Diese Dialogfelder eignen sich am besten für häufige, sich wiederholende, laufende Aufgaben.

**Ein Aufgabendialog ist ein Dialogfeld, das mithilfe der Api (Application Programming Interface) des Aufgabendialogfelds implementiert wird.** Sie bestehen aus den folgenden Teilen, die in einer Vielzahl von Kombinationen zusammengesetzt werden können:

-   Eine **Titelleiste** zum Identifizieren der Anwendungs- oder Systemfunktion, von der das Dialogfeld stammt.
-   Eine **Hauptanweisung** mit einem optionalen Symbol, um das Ziel des Benutzers mit dem Dialogfeld zu identifizieren.
-   Ein **Inhaltsbereich** für beschreibende Informationen und Steuerelemente.
-   Einen **Befehlsbereich** für Commitschaltflächen, einschließlich der Schaltfläche Abbrechen, und optionale Optionen "Weitere" und "Nicht anzeigen" <item> -Steuerelemente erneut.
-   Ein **Fußnotenbereich** für optionale zusätzliche Erklärungen und Hilfe, der in der Regel für weniger erfahrene Benutzer vorgesehen ist.

![Screenshot eines typischen Aufgabendialogfelds ](images/win-dialog-box-image2.png)

Ein typisches Aufgabendialogfeld.

**Aufgabendialoge werden nach Bedarf empfohlen, da sie einfach zu erstellen sind und ein konsistentes Aussehen erzielen.** Aufgabendialogfelder erfordern Windows Vista oder höher, sodass sie nicht für frühere Versionen von Microsoft Windows geeignet sind.

Ein Aufgabenbereich ähnelt einem Dialogfeld, mit der Ausnahme, dass er in einem Fensterbereich anstelle eines separaten Fensters angezeigt wird. Daher haben Aufgabenbereiche ein direkteres kontextbezogenes Gefühl als Dialogfelder. Obwohl sie technisch gesehen nicht identisch sind, **ähneln Aufgabenbereiche Dialogfeldern so, dass ihre Richtlinien in diesem Artikel vorgestellt werden.**

![Screenshot eines typischen Aufgabenbereichs ](images/win-dialog-box-image3.png)

Ein typischer Aufgabenbereich.

[Eigenschaftenfenster](win-property-win.md) sind ein spezieller Dialogfeldtyp, der zum Anzeigen und Ändern von Eigenschaften für ein Objekt, eine Auflistung von Objekten oder ein Programm verwendet wird. Darüber hinaus unterstützen Eigenschaftenfenster in der Regel mehrere Aufgaben, während Dialogfelder in der Regel einen einzelnen Task oder Schritt in einer Aufgabe unterstützen. Da ihre Verwendung spezialisiert ist, **werden Eigenschaftenfenster in einer anderen Reihe von Richtlinien behandelt.**

Dialogfelder können [Registerkarten](ctrl-tabs.md)aufweisen, und wenn ja, werden sie als Dialogfelder im Registerkartenbett bezeichnet. Eigenschaftenfenster werden durch ihre Darstellung von Eigenschaften bestimmt, nicht durch die Verwendung von Registerkarten.

**Hinweis:** Richtlinien im Zusammenhang mit [Layout,](vis-layout.md) [Fensterverwaltung,](win-window-mgt.md)allgemeinen Dialogfeldern, [Eigenschaftenfenstern,](win-property-win.md) [Assistenten,](win-wizards.md) [Bestätigungen,](mess-confirm.md) [Fehlermeldungen](mess-error.md)und [Warnmeldungen](mess-warn.md) werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Sollen Benutzer Informationen bereitstellen, Benutzern eine Frage stellen oder Benutzern erlauben, Optionen zum Ausführen eines Befehls oder einer Aufgabe auszuwählen?** Falls nicht, verwenden Sie eine andere Benutzeroberfläche .
-   **Sollen Eigenschaften für ein Objekt, eine Auflistung von Objekten oder ein Programm angezeigt und geändert werden?** Verwenden Sie in diesem Falle stattdessen ein [Eigenschaftenfenster](win-property-win.md) oder eine [Symbolleiste.](cmd-toolbars.md)
-   **Soll eine Sammlung von Befehlen oder Tools präsentiert werden?** Verwenden Sie in diesem Falle eine Symbolleiste oder ein [Palettenfenster.](glossary.md)
-   **Soll überprüft werden, ob der Benutzer mit einer Aktion fortfahren möchte?** Gibt es einen eindeutigen Grund, nicht fortzufahren, und eine angemessene Wahrscheinlichkeit, dass benutzer dies manchmal nicht tun? Wenn ja, verwenden Sie eine [Bestätigung.](mess-confirm.md)
-   **Soll ein Fehler oder eine Warnmeldung ausgegeben werden?** Verwenden Sie in diesem Falle eine [Fehlermeldung](mess-error.md) oder [eine Warnmeldung.](mess-warn.md)
-   Ist der Zweck für Folgendes:
    -   Öffnen von Dateien
    -   Speichern von Dateien
    -   Öffnen von Ordnern
    -   Suchen oder Ersetzen von Text
    -   Drucken eines Dokuments
    -   Auswählen von Attributen einer gedruckten Seite
    -   Auswählen einer Schriftart
    -   Auswählen einer Farbe
    -   Suchen nach einer Datei, einem Ordner, einem Computer oder einem Drucker
    -   Suchen nach Benutzern, Computern oder Gruppen in Microsoft Active Directory
    -   Geben Sie einen Benutzernamen und ein Kennwort ein?

Verwenden Sie in diesem Falle stattdessen das entsprechende [allgemeine Dialogfeld.](win-common-dlg.md) Viele dieser allgemeinen Dialoge sind erweiterbar.

-   **Ist der Zweck, eine mehrstufige Aufgabe auszuführen, die mehr als ein einzelnes Fenster erfordert?** Verwenden Sie in diesem Falle stattdessen einen [Taskflow](glossary.md) oder [Assistenten.](win-wizards.md)
-   **Soll der Zweck darin besteht, Benutzer über ein System- oder Programmereignis zu informieren, das nicht mit der aktuellen Benutzeraktivität in Zusammenhang steht, das keine sofortige Benutzeraktion erfordert und die Benutzer frei ignorieren können?** Verwenden Sie in diesem Falle stattdessen eine [Benachrichtigung.](mess-notif.md)
-   **Soll der Programmstatus angezeigt werden?** Verwenden Sie in diesem Falle stattdessen eine [Statusleiste.](ctrl-status-bars.md)
-   **Wäre es besser, die benutzeroberfläche vor Ort zu verwenden?** Dialogfelder können den Benutzerflow unterbrechen, indem sie die Aufmerksamkeit erfordern. Manchmal ist diese Unterbrechung des Flows gerechtfertigt, z. B. wenn der Benutzer eine Aktion ausführen muss, die sich außerhalb des aktuellen Kontexts befindet. In anderen Fällen besteht ein besserer Ansatz darin, die Benutzeroberfläche im Kontext darzustellen, entweder direkt mit der direkten Benutzeroberfläche (z. B. einem Aufgabenbereich) oder bei Bedarf mithilfe der [progressiven Offenlegung.](ctrl-progressive-disclosure-controls.md)
-   **Soll ein nicht kritisches Benutzereingabeproblem oder eine besondere Bedingung angezeigt werden?** Verwenden Sie in diesem Falle stattdessen einen [Balloon.](ctrl-balloons.md)
-   **Wäre es für Aufgabenflows besser, eine andere Seite zu verwenden?** Im Allgemeinen möchten Sie, dass eine Aufgabe innerhalb eines einzelnen Fensters von Seite zu Seite fließt. Verwenden Sie Dialogfelder, um direkt ausgeführte Befehle zu bestätigen, Eingaben für direkt ausgeführte Befehle abzurufen und sekundäre, eigenständige Aufgaben auszuführen, die am besten unabhängig und außerhalb des Haupttaskflows ausgeführt werden.
-   **Ändern Benutzer die Optionen wahrscheinlich für die Auswahl von Optionen?** Falls nicht, sollten Sie Alternativen in Betracht ziehen, z. B.:
    -   Verwenden sie die Standardoptionen, ohne die Benutzer zu fragen, aber später Änderungen vornehmen zu können.
    -   Bereitstellen einer Version mit Optionen **(z. B. Drucken...** in einem Menü) sowie einer Version ohne Optionen (z. B. **Drucken** auf der Symbolleiste). Im Allgemeinen sollten Symbolleistenbefehle sofort sein und das Anzeigen von Dialogfeldern vermeiden.
-   **Gibt es für die Auswahl von Optionen eine einfachere, direktere Möglichkeit, die Optionen darzustellen?** Ziehen Sie in diesem Falle Alternativen in Betracht, z. B.:
    -   Verwenden einer [unterteilten Schaltfläche](ctrl-command-buttons.md) zum Auswählen von Variationen eines Befehls.
    -   Verwenden eines Untermenüs für Befehle, Kontrollkästchen, Optionsfelder und einfache Listen.

![Screenshot: Menü und Untermenü](images/win-dialog-box-image4.png)

![Screenshot eines Menüs und Untermenüs ](images/win-dialog-box-image5.png)

In diesen Beispielen werden Untermenüs anstelle von Dialogfeldern für einfache Auswahl verwendet.

## <a name="design-concepts"></a>Entwurfskonzepte

Bei ordnungsgemäßer Verwendung sind Dialogfelder eine hervorragende Möglichkeit, Ihrem Programm Energie und Flexibilität zu geben. Wenn sie missbraucht werden, sind Dialogfelder eine einfache Möglichkeit, Benutzer zu verärgern, ihren Flow zu unterbrechen und das Programm indirekt und mühsam zu verwenden. **Modale Dialogfelder erfordern die Aufmerksamkeit der Benutzer.** Dialogfelder lassen sich häufig einfacher implementieren als alternative Benutzeroberflächen, sodass sie tendenziell überladen sind.

**Ein Dialogfeld ist am effektivsten, wenn seine Entwurfsmerkmale der Verwendung entsprechen.** Der Entwurf eines Dialogfelds wird größtenteils durch seinen Zweck bestimmt (zum Anbieten von Optionen, Stellen von Fragen, Bereitstellen von Informationen oder Feedback), Typ (modal oder moduslos) und Benutzerinteraktion (erforderlich, optionale Antwort oder Bestätigung), während seine Verwendung größtenteils durch den Kontext (benutzer- oder programminitiiert), die Wahrscheinlichkeit von Benutzeraktionen und die Häufigkeit der Anzeige bestimmt wird.

Um effektive Dialogfelder zu entwerfen, verwenden Sie die folgenden Elemente effektiv:

-   Text im Dialogfeld
-   Hauptanweisungen
-   Nicht anzeigen <item> again-Option

**Wenn Sie nur eins tun...**

Stellen Sie sicher, dass der Entwurf Ihres Dialogfelds (bestimmt durch seinen Zweck, Typ und die Benutzerinteraktion) mit seiner Verwendung (bestimmt durch den Kontext, die Wahrscheinlichkeit der Benutzeraktion und die Häufigkeit der Anzeige) entspricht.

## <a name="usage-patterns"></a>Verwendungsmuster

Dialogfelder verfügen über mehrere Verwendungsmuster:

-   Fragedialogfelder (mithilfe von Schaltflächen) stellen Benutzern eine einzelne Frage oder , um einen Befehl zu bestätigen, und verwenden einfache Antworten in horizontal angeordneten Befehlsschaltflächen.
-   Fragedialoge (über Befehlslinks) stellen Benutzern eine einzelne Frage oder , um eine auszuführende Aufgabe auszuwählen und detaillierte Antworten in vertikal angeordneten Befehlslinks zu verwenden.
-   Auswahldialoge bieten Benutzern eine Reihe von Optionen, in der Regel, um einen Befehl vollständig anzugeben. Im Gegensatz zu Fragedialogen können Auswahldialoge mehrere Fragen stellen.
-   Statusdialogfelder stellen Benutzern während eines längeren Vorgangs (länger als fünf Sekunden) Statusfeedback sowie einen Befehl zum Abbrechen oder Beenden des Vorgangs zur Verfügung.
-   In Informationsdialogfeldern werden vom Benutzer angeforderte Informationen angezeigt.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Verwenden Sie keine scrollbaren Dialogfelder.** Verwenden Sie keine Dialogfelder, in denen die Verwendung einer Scrollleiste während der normalen Nutzung vollständig angezeigt werden muss. Gestalten Sie stattdessen das Dialogfeld neu. Erwägen Sie die [Verwendung der progressiven Offenlegung](ctrl-progressive-disclosure-controls.md) oder der [Registerkarten](ctrl-tabs.md).
-   **Sie verfügen nicht über eine Menüleiste oder Statusleiste.** Stellen Sie stattdessen den Zugriff auf Befehle und Status direkt im Dialogfeld selbst oder mithilfe von Kontextmenüs für die relevanten Steuerelemente zur Verfügung.

    -   **Ausnahme:** Menüleisten sind akzeptabel, wenn ein Dialogfeld verwendet wird, um ein primäres Fenster (z. B. ein Hilfsprogramm) zu implementieren.

    **Falsch:**

    ![Screenshot eines Dialogfelds mit einer Menüleiste ](images/win-dialog-box-image6.png)

    In diesem Beispiel ist Zertifikat suchen ein modusloses Dialogfeld mit einer Menüleiste.

-   Wenn ein Dialogfeld sofortige Aufmerksamkeit erfordert und das Programm nicht aktiv ist, drücken Sie die **Taskleistenschaltfläche dreimal,** um die Aufmerksamkeit zu erhalten, und lassen Sie es hervorgehoben. Führen Sie nichts anderes aus: Stellen Sie das Fenster nicht wieder wieder, oder aktivieren Sie es nicht, und geben Sie keine Soundeffekte wieder. Achten Sie stattdessen auf die Fensterzustandsauswahl des Benutzers, und lassen Sie den Benutzer das Fenster aktivieren, wenn er bereit ist.
-   Weitere Richtlinien und Beispiele finden Sie unter [Taskleiste](winenv-taskbar.md).

### <a name="modal-dialog-boxes"></a>Modale Dialogfelder

-   **Verwenden Sie für kritische oder selten auftretende einmalige Aufgaben, die abgeschlossen werden müssen, bevor Sie fortfahren.**
-   Verwenden Sie [ein Modell mit verzögerten](glossary.md) Commits, damit Änderungen erst wirksam werden, wenn explizit ein Commit erfolgt ist.
-   **Implementieren Sie nach Bedarf mithilfe eines Aufgabendialogfelds, um ein konsistentes Aussehen zu erzielen.** Taskdialogfelder erfordern Windows Vista oder höher, sodass sie nicht für frühere Versionen von Windows.

### <a name="modeless-dialog-boxes"></a>Dialogfelder ohne Modus

-   **Verwenden Sie für häufige, sich wiederholende, sich wiederholende Aufgaben.**
-   Verwenden Sie [ein Direkt-Commit-Modell,](glossary.md) damit Änderungen sofort wirksam werden.
-   Verwenden Sie für nicht moduslose Dialogfelder eine explizite Befehlsschaltfläche Schließen im Dialogfeld, um das Fenster zu schließen. Verwenden Sie für beides die Schaltfläche Schließen auf der Titelleiste, um das Fenster zu schließen.
-   **Erwägen Sie, moduslose Dialogfelder andockbar zu machen.** Andockbare, moduslose Dialoge ermöglichen eine flexiblere Platzierung.

![Screenshot eines andockbaren, moduslosen Dialogfelds ](images/win-dialog-box-image7.png)

Einige in der -Datei verwendete moduslose Dialogfelder Microsoft Office andockbar.

### <a name="multiple-dialog-boxes"></a>Mehrere Dialogfelder

-   **Zeigen Sie in einem Dialogfeld für die Besitzerauswahl nicht mehr als einen Auswahldialog gleichzeitig an.** Das Anzeigen von mehr als einem macht die Bedeutung der Commitschaltflächen für Benutzer schwer zu verstehen. Sie können bei Bedarf andere Arten von Dialogfeldern (z. B. Fragedialoge) anzeigen.
-   **Für eine Sequenz verwandter Dialoge sollten Sie nach Möglichkeit einen mehrseitigen Dialog verwenden.** Verwenden Sie einzelne Dialoge, wenn sie nicht eindeutig verknüpft sind.

### <a name="multi-page-dialog-boxes"></a>Dialogfelder mit mehreren Seiten

-   Verwenden Sie ein Mehrseitendialogfeld anstelle einzelner Dialogfelder, wenn sie über die folgende Sequenz verwandter Seiten verfügen:
    -   Eine einzelne Eingabeseite (optional)
    -   Eine Statusseite
    -   Eine einzelne Ergebnisseite

Die Eingabeseite ist optional, da die Aufgabe möglicherweise an einer anderen Stelle initiiert wurde. **Dadurch erhält die resultierende Erfahrung ein stabiles, einfaches und einfaches Gefühl.**

![Screenshot einer Statusleiste ](images/win-dialog-box-image8.png)

![Screenshot der Meldung "Keine Probleme gefunden" ](images/win-dialog-box-image9.png)

In diesem Beispiel besteht Windows Netzwerkdiagnose aus Fortschritts- und Ergebnisseiten.

-   **Verwenden Sie keinen mehrseitigen Dialog, wenn es sich bei der Eingabeseite um einen Standarddialog handelt.** In diesem Fall ist die Konsistenz der Verwendung eines Standarddialogfelds wichtiger.
-   **Verwenden Sie die Schaltflächen Weiter oder Zurück nicht, und sie haben nicht mehr als drei Seiten.** Mehrseitige Dialogfelder sind für Einzelschrittaufgaben mit Feedback. Es handelt sich nicht um [Assistenten,](win-wizards.md)die für mehrstufige Aufgaben verwendet werden. Assistenten haben im Vergleich zu Dialogfeldern mit mehreren Seiten ein starkes, indirektes Gefühl.
-   **Verwenden Sie auf der Eingabeseite bestimmte Befehlsschaltflächen oder Befehlslinks, um die Aufgabe zu initiieren.**
-   **Verwenden Sie auf den Eingabe- und Fortschrittsseiten die Schaltfläche Abbrechen und auf der Ergebnisseite die Schaltfläche Schließen.**

**Entwickler:** Sie können Mehrseitentaskdialogfelder mithilfe der [TDM \_ NAVIGATE \_ PAGE-Meldung](../controls/tdm-navigate-page.md) erstellen.

### <a name="presentation"></a>Präsentation

Damit Dialogfelder leicht zu finden und darauf zugreifen können, ordnen Sie den Dialog eindeutig der Quelle zu und funktionieren gut mit mehreren Monitoren:

-   **Zunächst werden Dialoge "zentriert" über dem Besitzerfenster angezeigt.** Erwägen Sie für die nachfolgende Anzeige die Anzeige an der letzten Position (relativ zum Besitzerfenster), wenn dies wahrscheinlich bequemer ist.

![Diagramm des Dialogfelds, das auf einem Fenster darauf zentriert ist ](images/win-dialog-box-image10.png)

Zentriert Dialoge zunächst über dem Besitzerfenster.

-   **Wenn ein Dialogfeld kontextbezogen ist, zeigen Sie es in der Nähe des Objekts an, von dem es gestartet wurde.** Platzieren Sie sie jedoch in den anderen Richtungen (vorzugsweise nach unten und rechts versetzt), damit das Objekt nicht durch den Dialog abgedeckt wird.

![Diagramm des Dialogfeldoffsets nach unten und rechts ](images/win-dialog-box-image11.png)

Die Eigenschaften eines Objekts werden in der Nähe des Objekts angezeigt.

-   **Für nicht moduslose Dialogfelder wird zunächst oben im Besitzerfenster angezeigt, um die Suche zu ermöglichen.** Wenn der Benutzer das Besitzerfenster aktiviert, kann dies den moduslosen Dialog verdecken.
-   **Passen Sie bei Bedarf den anfänglichen Speicherort so an, dass der gesamte Dialog im Zielmonitor sichtbar ist.** Wenn ein Fenster, das die Größe ändern kann, größer als der Zielmonitor ist, reduzieren Sie es an seine Größe.
-   **Wenn ein Dialogfeld erneut angezeigt wird, sollten Sie erwägen, es im gleichen Zustand wie beim letzten Zugriff anzuzeigen.** Speichern Sie beim Schließen den verwendeten Monitor, die Fenstergröße, den Speicherort und den Zustand (maximiert im Vergleich zur Wiederherstellung). Stellen Sie bei der erneuten Anzeige die gespeicherte Dialoggröße, den Speicherort und den Zustand mithilfe des entsprechenden Monitors wieder wieder auf. Erwägen Sie außerdem, diese Attribute pro Benutzer über Programminstanzen hinweg persistent zu halten.
-   **Legen Sie für fenster, die die Größe ändern können, eine Mindestfenstergröße fest, wenn es eine Größe gibt, unter der der Inhalt nicht mehr verwendet werden kann.** Ändern Sie die Präsentation, um den Inhalt in kleineren Größen nutzbar zu machen.

![Screenshot der zentrierten Media Player-Schaltflächen ](images/win-dialog-box-image12.png)

In diesem Beispiel wird Windows Media Player Format geändert, wenn das Fenster für das Standardformat zu klein wird.

-   **Verwenden Sie nicht das Always On Top-Attribut.**
    -   **Ausnahme:** Verwenden Sie nur, wenn ein Dialogfeld einen im Wesentlichen modalen Vorgang implementiert, aber kurz angehalten werden muss, um auf das Besitzerfenster zugreifen zu können. Bei der Rechtschreibprüfung eines Dokuments können Benutzer z. B. gelegentlich das Rechtschreibprüfungsdialogfeld verlassen und auf das Dokument zugreifen, um Fehler zu beheben.

Weitere Informationen und Beispiele finden Sie unter [Fensterverwaltung](win-window-mgt.md).

### <a name="title-bars"></a>Titelleisten

-   **Dialogfelder verfügen nicht über Titelleistensymbole.** Titelleistensymbole werden als visuelle Unterscheidung zwischen [primären und](glossary.md) [sekundären Fenstern verwendet.](glossary.md)
    -   **Ausnahme:** Wenn ein Dialogfeld zum Implementieren eines primären Fensters (z. B. eines Hilfsprogramms) verwendet wird und daher auf der Taskleiste angezeigt wird, verfügt es über ein Titelleistensymbol. Optimieren Sie in diesem Fall den Titel für die Anzeige auf der Taskleiste, indem Sie die unterscheidenden Informationen präzise an erster Stelle platzieren.
-   **Dialogfelder verfügen immer über die Schaltfläche Schließen.** Moduslose Dialoge können auch über die Schaltfläche Minimieren verfügen. Dialogfelder, deren Größe geändert werden kann, können über die Schaltfläche Maximieren verfügen.
-   **Deaktivieren Sie nicht die Schaltfläche Schließen.** Die Schaltfläche Schließen hilft Benutzern, die Kontrolle zu behalten, indem sie Fenster schließen können, die sie nicht wünschen.
    -   **Ausnahme:** Für Statusdialogfelder können Sie die Schaltfläche Schließen deaktivieren, wenn der Task bis zum Abschluss ausgeführt werden muss, um einen gültigen Zustand zu erreichen oder Datenverluste zu verhindern.
-   **Die Schaltfläche Schließen auf der Titelleiste sollte die gleiche Auswirkung wie die Schaltfläche Abbrechen oder Schließen** im Dialogfeld haben. Geben Sie ihm niemals den gleichen Effekt wie OK.
-   Wenn die Titelleistenbeschriftung und das Symbol am oberen Rand des Fensters bereits hervorgehoben angezeigt werden, können Sie die Titelleistenbeschriftung und das Symbol ausblenden, um Redundanz zu vermeiden. Sie müssen jedoch intern einen geeigneten Titel für die Verwendung durch Windows festlegen.

### <a name="interaction"></a>Interaktion

-   **Wenn sie angezeigt werden, sollten vom Benutzer initiierte Dialogfelder immer den Eingabefokus haben.** Vom Programm initiierte Dialogfelder sollten den Eingabefokus nicht übernehmen, da der Benutzer möglicherweise mit einem anderen Fenster interagiert. Eine solche Interaktion, die im Dialogfeld fehlgeleitet wird, kann unbeabsichtigte Folgen haben.
-   **Weisen Sie dem Steuerelement den anfänglichen Eingabefokus zu,** mit dem Benutzer höchstwahrscheinlich mit dem ersten interagieren. Dies ist normalerweise (aber nicht immer) das erste interaktive Steuerelement. Vermeiden Sie es, einem Hilfelink den anfänglichen Eingabefokus zuzuweisen.
-   **Für die Tastaturnavigation sollte die Tabstoppreihenfolge in einer logischen Reihenfolge ablaufen, in der Regel von links nach rechts, von oben nach unten.** In der Regel folgt die Tabstoppreihenfolge der Lesereihenfolge, aber erwägen Sie, diese Ausnahmen zu treffen:

    -   Ordnen Sie die am häufigsten verwendeten Steuerelemente weiter oben in der Tabstoppreihenfolge an.
    -   Setzen Sie Hilfelinks am unteren Rand eines Dialogfelds nach den Commitschaltflächen in der Tabstoppreihenfolge.

    Gehen Sie beim Zuweisen der Reihenfolge davon aus, dass Benutzer Dialogfelder für ihren beabsichtigten Zweck anzeigen. So zeigen Benutzer beispielsweise Auswahldialogfelder an, um Entscheidungen zu treffen, dürfen sie nicht überprüfen und auf Abbrechen klicken.

-   **Durch Drücken der ESC-TASTE wird immer ein aktives Dialogfeld geschlossen.** Dies gilt für Dialogfelder mit Abbrechen oder Schließen. Dies gilt auch, wenn Abbrechen in Schließen umbenannt wurde, da die Ergebnisse nicht mehr rückgängig gemacht werden können.

**Zugriffsschlüssel**

-   **Weisen Sie nach Möglichkeit allen interaktiven Steuerelementen oder deren Bezeichnungen eindeutige Zugriffsschlüssel zu.** [Schreibgeschützte Textfelder](ctrl-text-boxes.md) sind interaktive Steuerelemente (da Benutzer sie scrollen und Text kopieren können), sodass sie von Zugriffsschlüsseln profitieren. **Weisen Sie folgenden Benutzern keine Zugriffsschlüssel zu:**
    -   **Die Schaltflächen OK, Abbrechen und Schließen.** Eingabe und ESC werden für ihre Zugriffsschlüssel verwendet. Weisen Sie einem Steuerelement jedoch immer einen Zugriffsschlüssel zu, der OK oder Abbrechen bedeutet, aber eine andere Bezeichnung aufweist.

        ![Screenshot des Dialogfelds "Datei löschen" ](images/win-dialog-box-image13.png)

        In diesem Beispiel ist der Schaltfläche für positive Commits ein Zugriffsschlüssel zugewiesen.

    -   **Gruppenbezeichnungen.** Normalerweise werden den einzelnen Steuerelementen innerhalb einer Gruppe Zugriffsschlüssel zugewiesen, sodass die Gruppenbezeichnung keine benötigt. Wenn es jedoch zu einem Mangel an Zugriffsschlüsseln kommt, weisen Sie der Gruppenbezeichnung und nicht den einzelnen Steuerelementen einen Zugriffsschlüssel zu.
    -   **Generische Hilfeschaltflächen,** auf die mit F1 zugegriffen wird.
    -   **Linkbezeichnungen.** Es gibt häufig zu viele Links, um eindeutige Zugriffsschlüssel zuzuweisen, und die Unterstriche, die häufig zum Kennzeichnen von Links verwendet werden, blenden die Unterstriche des Zugriffsschlüssels aus. Greifen Sie stattdessen auf Links mit der TAB-TASTE zu.
    -   **Registerkartennamen.** Registerkarten werden mit STRG+TAB und STRG+UMSCHALT+TAB zyklust.
    -   **Schaltflächen zum Durchsuchen mit der Bezeichnung "...".** Diesen Schaltflächen durchsuchen können keine eindeutigen Zugriffsschlüssel zugewiesen werden.
    -   Steuerelemente ohne **Bezeichnung,** z. B. Drehsteuerelemente, Schaltflächen für grafische Befehle und steuerelemente für die progressive Offenlegung ohne Bezeichnungen.
    -   **Nicht bezeichnungsbasierter statischer Text oder Bezeichnungen für Steuerelemente, die nicht interaktiv sind,** z. B. Statusleisten.

-   Weisen Sie nach **Möglichkeit Zugriffsschlüssel für häufig verwendete Befehle gemäß den Standardzugriffsschlüsselzuweisungen zu.** Konsistente Zuweisungen von Zugriffsschlüsseln sind zwar nicht immer möglich, werden aber insbesondere für häufig verwendete Dialogfelder bevorzugt.
-   **Weisen Sie zunächst Zugriffsschlüssel für commit-Schaltflächen zu, um sicherzustellen, dass sie über die Standardschlüsselzuweisungen verfügen.** Wenn keine Standardschlüsselzuweisung vorhanden ist, verwenden Sie den ersten Buchstaben des ersten Worts. Beispielsweise sollte der Zugriffsschlüssel für die Schaltflächen Ja und Kein Commit immer "Y" und "N" sein, unabhängig von den anderen Steuerelementen im Dialogfeld.
-   **Um die Suche nach Zugriffsschlüsseln zu vereinfachen, weisen Sie die Zugriffsschlüssel einem Zeichen zu, das früh in der Bezeichnung angezeigt wird,** idealerweise dem ersten Zeichen, auch wenn ein Schlüsselwort vorhanden ist, das später in der Bezeichnung angezeigt wird.
-   **Bevorzugen Sie Zeichen mit breiter Breite,** z. B. w, m und Großbuchstaben.
-   **Bevorzugen Sie einen typischen Konsonanten oder einen Vokal,** z. B. "x" in Exit.
-   **Vermeiden Sie die Verwendung von Zeichen, die die Unterstreichung schwierig zu erkennen machen,** z. B. (von den problematischsten bis zu den am wenigsten problematischen):
    -   Buchstaben, die nur ein Pixel breit sind, z. B. i und l.
    -   Buchstaben mit Nachfolgern wie g, j, p, q und y.
    -   Buchstaben neben einem Buchstaben mit einem Nachfolger.

Weitere Richtlinien und Beispiele finden Sie unter [Tastatur.](inter-keyboard.md)

### <a name="progress-dialogs"></a>Statusdialoge

Bei Aufgaben mit langer Ausführungslaufzeit **wird davon ausgegangen, dass Benutzer etwas anderes tun, während die Aufgabe abgeschlossen ist.** Entwerfen Sie die Aufgabe so, dass sie unbeaufsichtigt ausgeführt wird.

-   Zeigen Sie Benutzern das **Dialogfeld "Statusfeedback" an, wenn der Abschluss eines Vorgangs länger als fünf Sekunden dauert,** zusammen mit einem Befehl zum Abbrechen oder Beenden des Vorgangs.
    -   **Ausnahme:** Verwenden Sie für Assistenten und Aufgabenflows nur dann ein modales Dialogfeld für den Fortschritt, wenn der Task auf derselben Seite verbleibt (anstatt zu einer anderen Seite zu wechseln), und Benutzer während des Wartens nichts tun können. Verwenden Sie andernfalls eine Statusseite oder einen statusbasierten Status.
-   Wenn es sich bei dem Vorgang um eine Aufgabe mit langer Ausführung (mehr als 30 Sekunden) handelt und im Hintergrund ausgeführt werden kann, verwenden Sie ein statusloses Dialogfeld, damit Benutzer Das Programm während des Wartens weiterhin verwenden können.
-   Statusdialogfelder ohne Modus:
    -   Klicken Sie auf der Titelleiste auf die Schaltfläche Minimieren.
    -   Werden auf der Taskleiste angezeigt.
-   Implementieren Sie statuslose Statusdialogfelder, sodass sie auch dann weiterhin ausgeführt werden, wenn das Besitzerfenster geschlossen ist.

![Screenshot des Kopierdialogfelds mit Statusanzeige ](images/win-dialog-box-image14.png)

In diesem Beispiel wird der Dateikopiervorgang auch dann fortgesetzt, wenn das Besitzerfenster geschlossen ist.

-   **Geben Sie eine Befehlsschaltfläche an, um den Vorgang anzuhalten, wenn der Vorgang mehr als ein paar Sekunden dauert oder möglicherweise nie abgeschlossen werden kann.** Beschriften Sie die Schaltfläche Abbrechen, wenn das Abbrechen die Umgebung in den vorherigen Zustand zurückgibt (ohne Nebeneffekte). Beschriften Sie andernfalls die Schaltfläche Beenden, um anzugeben, dass der teilweise abgeschlossene Vorgang intakt bleibt. Sie können die Schaltflächenbezeichnung in der Mitte des Vorgangs von Abbrechen in Beenden ändern, wenn es zu einem bestimmten Zeitpunkt nicht möglich ist, die Umgebung in den vorherigen Zustand zurückzuversetzen.

![Screenshot des Dialogfelds mit der Schaltfläche "Abbrechen" ](images/win-dialog-box-image15.png)

In diesem Beispiel hat das Anhalten der Problemdiagnose keine Nebeneffekte.

-   **Geben Sie eine Befehlsschaltfläche an, um den Vorgang anzuhalten, wenn der Vorgang mehr als einige Minuten dauert und die Benutzer nicht mehr in der Lage sind, ihre Arbeit zu erledigen.** Dies zwingt den Benutzer nicht, zwischen dem Abschließen der Aufgabe und dem Erledigen seiner Arbeit zu wählen.
-   **Sammeln Sie so viele Informationen wie sie können, bevor Sie die Aufgabe starten.**
-   **Wenn wiederherstellbare Probleme erkannt werden, lassen Sie benutzer alle Probleme behandeln, die am Ende der Aufgabe gefunden wurden.** Wenn dies nicht praktikabel ist, sollten Benutzer probleme behandeln, sobald sie auftreten.
-   **Verwerfen Sie Tasks nicht als Ergebnis wiederherstellbarer Fehler.**

![Screenshot des Dialogfelds mit der Schaltfläche "Erneut versuchen" ](images/win-dialog-box-image16.png)

In diesem Beispiel ermöglicht Windows Explorer Benutzern, die Aufgabe nach einem wiederherstellbaren Fehler fortzusetzen.

-   **Zeigen Sie Probleme an, indem Sie die Statusanzeige rot drehen.**

![Screenshot der Statusanzeige und schaltfläche "Erneut versuchen" ](images/win-dialog-box-image17.png)

In diesem Beispiel wurde ein Wechseldatenträger während einer Dateikopie entfernt.

-   **Wenn die Ergebnisse für Benutzer deutlich sichtbar sind, schließen Sie das Statusdialogfeld automatisch nach erfolgreichem Abschluss.** Verwenden Sie andernfalls Feedback nur, um Probleme zu melden:
    -   Um einfaches Feedback anzuzeigen, zeigen Sie das Feedback im Statusdialogfeld an, und ändern Sie die Schaltfläche Abbrechen in Schließen.
    -   Um ausführliches Feedback anzuzeigen, schließen Sie das Statusdialogfeld, und zeigen Sie ein Informationsdialogfeld an.

**Verwenden Sie keine Benachrichtigung für Das Feedback zur Vervollständigung.** Verwenden Sie entweder ein Statusdialogfeld oder eine [Aktionserfolgsbenachrichtigung,](mess-notif.md)aber nicht beides.

**Verbleibende Zeit**

-   **Verwenden Sie die folgenden Zeitformate.** Beginnen Sie mit dem ersten der folgenden Formate, bei denen die größte Zeiteinheit nicht 0 (null) ist, und wechseln Sie dann in das nächste Format, sobald die größte Zeiteinheit 0 (null) wird.

**Für Statusleisten:**

**Wenn verwandte Informationen in einem Doppelpunktformat angezeigt werden:**

Verbleibende Zeit: h Stunden, m Minuten

Verbleibende Zeit: m Minuten, s Sekunden

Verbleibende Zeit: s Sekunden

**Wenn der Bildschirmbereich premium ist:**

h hrs, m mins remaining

m Minuten, s Sekunden verbleibend

s verbleibende Sekunden

**Andernfalls:**

h Stunden, m Minuten verbleibend

m Minuten, s Sekunden verbleibend

s verbleibende Sekunden

**Für Titelleisten:**

hh:mm verbleibend

mm:ss verbleibend

0:ss verbleibend

Dieses kompakte Format zeigt zuerst die wichtigsten Informationen an, damit sie nicht auf der Taskleiste abgeschnitten werden.

-   **Treffen Sie Schätzungen genau, geben Sie jedoch keine falsche Genauigkeit an.** Wenn die größte Einheit Stunden ist, geben Sie Minuten (sofern sinnvoll), aber nicht Sekunden ein.

**Falsch:**

hh hours, mm minutes, ss seconds

-   **Halten Sie die Schätzung auf dem neuesten Stand.** Die verbleibende Aktualisierungszeit wird mindestens alle 5 Sekunden geschätzt.
-   **Konzentrieren Sie sich auf die verbleibende Zeit,** da dies die Informationen sind, die den Benutzern am meisten interessieren. Geben Sie die insgesamt verstrichene Zeit nur dann an, wenn es Szenarien gibt, in denen die verstrichene Zeit hilfreich ist (z. B. wenn die Aufgabe wahrscheinlich wiederholt wird). Wenn die verbleibende Zeitschätzung einer Statusanzeige zugeordnet ist, verfügen Sie nicht über vollständigen Text in Prozent, da diese Informationen von der Statusleiste selbst übermittelt werden.
-   **Seien Sie grammatisch korrekt.** Verwenden Sie singulare Einheiten, wenn die Zahl 1 ist.

**Falsch:**

1 Minuten, 1 Sekunden

-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**

Weitere Informationen und Beispiele finden Sie unter [Statusleisten.](progress-bars.md)

### <a name="icons-and-graphics"></a>Symbole und Grafiken

**Grafiken**

-   **Verwenden Sie keine großen Grafiken, die über das Auffüllen von Raum mit Augenschmaus hinaus keinen Zweck erfüllen.** Halten Sie stattdessen die Darstellung einfach.

**Falsch:**

![Screenshot des Dialogfelds mit einer großen Grafik ](images/win-dialog-box-image18.png)

In diesem Beispiel erfüllt die große Grafik keinen Zweck.

**Titelleistensymbole**

-   **Dialogfelder verfügen nicht über Titelleistensymbole.**
    -   **Ausnahme:** Wenn ein Dialogfeld zum Implementieren eines primären Fensters (z. B. eines Hilfsprogramms) verwendet wird und daher auf der Taskleiste angezeigt wird, verfügt es über ein Titelleistensymbol.

**Textsymbole**

-   **Wählen Sie das Textsymbol basierend auf dem Entwurfsmuster aus:**



| Muster | Textsymbol |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| **Fragedialoge**<br/>      | Programm, Feature, Objekt, Warnsymbol (bei potenziellem Daten- oder Systemzugriffsverlust), Sicherheitswarnung oder keine.<br/> |
| **Auswahldialoge**<br/>        | Keine.<br/>                                                                                                           |
| **Statusdialoge**<br/>      | Keine (kann aber über eine Animation verfügen).<br/>                                                                               |
| **Informationsdialoge**<br/> | Keine.<br/>                                                                                                           |



 

-   **Falsch:**

![Screenshot des Dialogfelds mit Warnsymbol ](images/win-dialog-box-image19.png)

In diesem Beispiel wird fälschlicherweise ein Warnsymbol für eine Frage verwendet, die keinen potenziellen Verlust von Daten oder Systemzugriff mit sich bringt.

- **Erwägen Sie die Verwendung von Symbolen, damit Benutzer die Funktionen Ihres Programms visuell erkennen können.** Diese Technik ist am effektivsten, wenn die Symbole leicht erkennbar und an mehreren Stellen im Programm verwendet werden können.

![Screenshot des Dialogfelds "Favoriten" mit Sternsymbol ](images/win-dialog-box-image20.png)

In diesem Beispiel stellt das gelbe Sternsymbol Favoriten dar. Das Symbol ist leicht zu erkennen und wird durchgängig in Windows verwendet, um Favoriten darzustellen.

-   **Verwenden Sie Symbole, damit Benutzer das betreffende Objekt erkennen können.**

![Screenshot des Dialogfelds mit powerpoint-Symbol ](images/win-dialog-box-image21.png)

In diesem Beispiel hilft das Objektsymbol Benutzern, den Dateityp zu erkennen, der geöffnet oder gespeichert wird.

-   **Erwägen Sie die Verwendung von Symbolen, um Features selbsterklärend zu machen.**

![Abbildungen von Pfeilen, die zeigen, wie der Monitor positioniert wird ](images/win-dialog-box-image22.png)

In diesem Beispiel helfen diese Symbole Benutzern, die Auswirkungen ihrer Features zu visualisieren.

-   **Verwenden Sie ein Symbol in About Box-Dialogfeldern für das Anwendungsbranding.**

![Screenshot des Dialogfelds "About" mit Windows-Logo ](images/win-dialog-box-image23.png)

In diesem Beispiel wird eine Bitmap in der About Box verwendet, um die Anwendung zu identifizieren und zu kennzeichnen.

**Fußnotensymbole**

-   **Wenn Sie über eine Fußnote verfügen, sollten Sie ein Fußnotensymbol verwenden, um das Thema der Fußnote zusammenzufassen.**

![Screenshot des Dialogfelds mit Fußnotensymbol ](images/win-dialog-box-image24.png)

In diesem Beispiel gibt das Fußnotensymbol an, dass die Frage Auswirkungen auf die Sicherheit hat.

-   **Verwenden Sie kein Fußnotensymbol, das das Textsymbol wiederholt.**
-   **Verwenden Sie nicht die Standardsymbole für Fehler oder Informationen.** Fehlerbedingungen müssen über das Textsymbol übermittelt werden, und Fußnoten dienen immer zu Informationszwecken, sodass das Informationssymbol redundant wird. Sie können jedoch das Standardwarnungssymbol und den gelben Sicherheitsschild verwenden, um Benutzer vor riskanten Folgen zu warnen.

Weitere Informationen und Beispiele finden Sie unter [Symbole.](vis-icons.md)

### <a name="commit-buttons"></a>Commitschaltflächen

**Hinweise:**

-   Diese Richtlinien gelten nicht für Fragedialoge, die Befehlslinks verwenden, da dieses Muster Befehlslinks anstelle von Schaltflächen verwendet.
-   \[Tun Sie \] \[ dies, und don't do \] it are positive bzw. negative responses, respectively, to the main instruction.

**Allgemein**

-   **Wählen Sie die Commitschaltflächen basierend auf dem Entwurfsmuster aus:**

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td><strong>Muster</strong><br/></td>
    <td><strong>Commitschaltflächen</strong><br/></td>
    </tr>
    <tr class="even">
    <td><strong>Fragedialoge (mitHilfe von Schaltflächen)</strong><br/></td>
    <td>Einer der folgenden präzisen Befehle: Ja/Nein, Ja/Nein/Abbrechen, [Do it]/Cancel, [Do it]/[Don't do it], [Do it]/[Don't do it]/Cancel.<br/></td>
    </tr>
    <tr class="odd">
    <td><strong>Fragedialoge (über Links)</strong><br/></td>
    <td>Abbrechen<br/></td>
    </tr>
    <tr class="even">
    <td><strong>Auswahldialoge</strong><br/></td>
    <td><ul>
    <li>Modale Dialoge: OK/Abbrechen oder [Durchführen]/Abbrechen</li>
    <li>Dialogfelder ohne Modus: Schaltfläche "Schließen" in Dialogfeld und Titelleiste</li>
    <li>Aufgabenbereich: Schaltfläche "Schließen" auf der Titelleiste</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><strong>Statusdialoge</strong><br/></td>
    <td>Verwenden Sie Abbrechen, wenn die Umgebung in den vorherigen Zustand zurückgibt (ohne Nebeneffekt). Verwenden Sie andernfalls Beenden.<br/></td>
    </tr>
    <tr class="even">
    <td><strong>Informationsdialoge</strong><br/></td>
    <td>Fast richtig.<br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   **Alle Commitschaltflächen mit Ausnahme von Anwenden führen zum Schließen des Dialogfeldfensters.**
-   **Bestätigen Sie keine Commitschaltflächen.** Dies kann unnötigerweise sehr ungern sein. **Ausnahmen:**

    -   Die Aktion ist möglicherweise schwerwiegender.
    -   Die Aktion ist eindeutig inkonsistent mit anderen Aktionen.
    -   Wenn die Aktion falsch ist, kann dies zu einem erheblichen Verlust von Daten, Zeit oder Aufwand im Namen des Benutzers führen.

    Weitere Richtlinien und Beispiele finden Sie unter [Bestätigungen.](mess-confirm.md)

-   **Deaktivieren Sie keine Commitschaltflächen. Ausnahmen:**
    -   **Wenn Benutzer eine Erhöhte Rechte erhöhen müssen, um eine Änderung zu ändern, deaktivieren Sie die Schaltflächen für positive Commits, bis der Benutzer eine Änderung vorn hat.** Dadurch wird verhindert, dass Benutzer die Erhöhung nur zum Schließen eines Fensters erhöhen, indem sie gezwungen werden, auf Abbrechen zu klicken.
    -   Weitere Ausnahmen finden Sie unter [Deaktivieren oder Entfernen von Steuerelementen im Vergleich zur Angabe von Fehlermeldungen.](#disabling-or-removing-controls-vs-giving-error-messages)
-   **Richten Sie commit-Schaltflächen in einer einzelnen Zeile** am unteren Rand des Dialogfelds, jedoch über dem Fußnotenbereich, mit der rechten Ausrichtung aus. Dies ist auch dann der Fall, wenn eine einzelne Commitschaltfläche (z. B. OK) angezeigt wird.

    **Falsch:**

    ![Screenshot der Nachricht mit zentrierter SCHALTFLÄCHE "OK" ](images/win-dialog-box-image25.png)

    In diesem Beispiel ist die Schaltfläche OK falsch zentriert.

-   **Stellen Sie die Commitschaltflächen in der folgenden Reihenfolge vor:**
    1.  OK/ \[ Do it \] /Yes
    2.  \[Don't do it \] /No
    3.  Abbrechen
    4.  Übernehmen (falls vorhanden)
    5.  Hilfe (falls vorhanden)
-   **Wenn Sie über viele zugehörige Commitschaltflächen verfügen, konsolidieren Sie sie mithilfe von geteilten Schaltflächen.**
-   **Sie haben eine klare Trennung von Commitschaltflächen (die das Fenster schließen) und allen anderen Befehlsschaltflächen (z. B. Erweitert).**

**Reagieren auf Hauptanweisungen**

-   **Verwenden Sie positive Commitschaltflächen, die bestimmte Antworten auf die Hauptanweisung sind, anstelle generischer Bezeichnungen wie OK oder Ja/Nein.** Benutzer sollten die Optionen verstehen können, indem sie den Schaltflächentext allein lesen. **Ausnahmen:**
    -   Verwenden Sie Schließen für Dialoge, die keine Einstellungen haben, z. B. Informationsdialoge. Verwenden Sie nie Schließen für Dialogfelder, die Einstellungen haben.
    -   Verwenden Sie OK, wenn die "spezifischen" Antworten immer noch generisch sind, z. B. Speichern, Auswählen oder Auswählen. Verwenden Sie OK, wenn Sie eine bestimmte Einstellung oder eine Sammlung von Einstellungen ändern.
    -   **Für ältere Dialogfelder ohne Main-Anweisung können Sie generische Bezeichnungen wie OK verwenden.** Solche Dialogfelder sind häufig nicht für die Ausführung einer bestimmten Aufgabe konzipiert und verhindern spezifischere Antworten.
    -   Bestimmte Aufgaben erfordern mehr Überdacht und sorgfältiges Lesen, damit Benutzer fundierte Entscheidungen treffen können. Dies ist in der Regel bei [Bestätigungen der Fall.](mess-confirm.md) **In solchen Fällen können Sie generische Schaltflächenbezeichnungen für Commits verwenden, um Benutzer zu zwingen, die Hauptanweisungen zu lesen und hastige Entscheidungen zu verhindern.**

        **Richtig:**

        ![Screenshot der Nachricht mit Schaltflächen "Ja" und "Nein"](images/win-dialog-box-image26.png)

        In diesem Beispiel erzwingt die Verwendung von Ja/Nein-Commitschaltflächen, dass Benutzer zumindest die Hauptanweisung lesen müssen.

-   Alternativ können Sie der Schaltflächenbezeichnung für positive Commits das Wort **"anyway" hinzufügen,** um anzugeben, dass das Dialogfeld einen Grund für die nicht fortgesetzte Vorgehensweise enthält und dass Benutzer den Dialog sorgfältig lesen sollten, bevor Sie fortfahren.

    **Richtig:**

    ![Screenshot der Meldung und Schaltfläche "Trotzdem deinstallieren" ](images/win-dialog-box-image27.png)

    In diesem Beispiel wird der Schaltflächenbezeichnung "Commit" "anyway" hinzugefügt, um anzugeben, dass Benutzer sorgfältig fortfahren sollten.

-   **Verwenden Sie Abbrechen oder Schließen für negative Commitschaltflächen anstelle bestimmter Antworten auf die Main-Anweisung.** Häufig stellen Benutzer fest, dass sie keine Aufgabe ausführen möchten, sobald ein Dialogfeld angezeigt wird. Wenn Abbrechen oder Schließen für bestimmte Antworten umbenennen würde, müssten Benutzer sorgfältig alle Commitschaltflächen lesen, um zu bestimmen, wie der Vorgang abgebrochen werden soll. **Durch die durchgängige Bezeichnung Abbrechen und Schließen sind sie leicht zu finden. Ausnahmen:**
    -   **Verwenden Sie nicht Ja/Abbrechen.** Verwenden Sie immer Ja/Nein als Paar.
    -   **Verwenden Sie eine bestimmte Antwort, wenn Abbrechen mehrdeutig ist.**
-   **Ordnen Sie generische Bezeichnungen nicht ihrer spezifischen Bedeutung mit Text im Inhaltsbereich zu.** Verwenden Sie stattdessen bestimmte Beschriftungen für Commitschaltfläche oder ein Fragedialogfeld mit Links, wenn die Bezeichnungen lang sind.

    **Falsch:**

    ![Screenshot der Nachricht mit unklarer Verwendung von Schaltflächen ](images/win-dialog-box-image28.png)

    In diesem Beispiel wird OK continue zugeordnet, Cancel wird Remain on Page (Auf Seite verbleiben) zugeordnet.

**Schaltflächen "Ja" und "Nein"**

-   **Bevorzugen Sie bestimmte Antworten auf die Schaltflächen Ja und Nein.** Auch wenn die Verwendung von Ja und Nein kein Fehler ist, können bestimmte Antworten schneller verstanden werden, was zu einer effizienten Entscheidungsfindung führt. Bestätigungen verfügen [jedoch in der](mess-confirm.md) Regel über die Schaltflächen Ja und Nein, damit Benutzer der Bestätigung vor der Antwort einige Gedanken machen können. [](mess-confirm.md)
-   **Verwenden Sie die Schaltflächen Ja und Nein, um nur auf Ja- oder Nein-Fragen zu antworten.** Die Hauptanweisung sollte natürlich als Ja oder Nein-Frage ausgedrückt werden. Verwenden Sie für Ja- oder Nein-Fragen niemals OK und Abbrechen.

    **Falsch:**

    ![Screenshot, der eine Meldung mit einem "OK" für eine Ja-Nein-Frage zeigt.](images/win-dialog-box-image29.png)

    **Richtig:**

    ![Screenshot der Nachricht mit "Ja" für dieselbe Frage ](images/win-dialog-box-image30.png)

    **Besser:**

    ![Screenshot der Nachricht mit Ausführung für dieselbe Frage ](images/win-dialog-box-image31.png)

    In diesen Beispielen sind Ja und Nein gute Antworten auf Ja und keine Fragen, aber bestimmte Antworten sind noch besser.

-   **Ziehen Sie in Betracht, die Hauptanweisung als "Ja" oder "Keine Frage" zu formulieren, wenn commit-Schaltflächen mit bestimmten Formulierungen lang oder umkweislich sind.** Alternativ können Sie Befehlslinks für längere Antworten (fünf Wörter oder mehr) auf die Main-Anweisung verwenden.

    **Falsch:**

    ![Screenshot der Nachricht mit wortigen Schaltflächenbezeichnungen ](images/win-dialog-box-image32.png)

    **Richtig:**

    ![Screenshot der Nachricht mit Ja/Nein-Schaltflächenbezeichnungen ](images/win-dialog-box-image33.png)

    Der spezifische Ausdruck im falschen Beispiel ist zu lang, sodass im richtigen Beispiel Ja und Nein verwendet werden.

-   **Verwenden Sie die Schaltflächen Ja und Nein nicht, wenn die Bedeutung der Antwort Nein unklar ist.** Falls ja, verwenden Sie stattdessen bestimmte Antworten.

**OK-Schaltflächen**

-   **Klicken Sie in modalen Dialogfeldern auf OK, um die Werte anzuwenden, die Aufgabe auszuführen und das Fenster zu schließen.**
-   **Verwenden Sie keine OK-Schaltflächen, um auf Fragen zu antworten.**
-   **Weisen Sie OK keine Zugriffsschlüssel zu, da die EINGABETASTE der Zugriffsschlüssel für die Standardschaltfläche ist.** Dadurch wird die Zuweisung der anderen Zugriffsschlüssel vereinfacht.
-   **Beschriften Sie die Schaltflächen OK ordnungsgemäß.** Die Schaltfläche OK sollte die Bezeichnung OK haben, nicht OK oder Ok.
-   **Verwenden Sie keine OK-Schaltflächen für Fehler oder Warnungen.** Probleme sind nie ok. Verwenden Sie stattdessen Schließen.

    **Falsch:**

    ![Screenshot der Nachricht mit der Schaltfläche "OK" ](images/win-dialog-box-image34.png)

    In diesem Beispiel sollte Close anstelle von OK verwendet werden.

-   **Verwenden Sie in nicht moduslosen Dialogfeldern keine OK-Schaltflächen.** Stattdessen sollten moduslose Dialoge taskspezifische Commitschaltflächen verwenden (z. B. Suchen). Für einige nicht moduslose Dialogfelder ist jedoch nur die Schaltfläche Schließen erforderlich.

**Schaltflächen "Abbrechen"**

-   **Wenn Sie auf Abbrechen klicken, werden alle Änderungen abgebrochen, die Aufgabe abgebrochen, das Fenster geschlossen und die Umgebung in den vorherigen Zustand zurückwechselt, ohne dass Nebeneffekten angezeigt werden.** Bei geschachtelten Auswahldialogfeldern bedeutet das Klicken auf Abbrechen im Dialogfeld für die Besitzerauswahl, dass alle Änderungen, die von Dialogfeldern für die Auswahl im Besitz des Besitzers vorgenommen wurden, ebenfalls verworfen werden.
-   **Geben Sie die Schaltfläche Abbrechen an, damit Benutzer Änderungen explizit abbrechen können.** Dialogfelder benötigen einen eindeutigen Ausgangspunkt. Verlassen Sie sich nicht darauf, dass Benutzer die Schaltfläche Schließen auf der Titelleiste finden.

    -   **Ausnahme:** Geben Sie keine Schaltfläche Abbrechen für Dialogfelder ohne Einstellungen an. Die Schaltflächen OK und Schließen haben in diesem Fall die gleiche Wirkung wie Abbrechen.

    **Falsch:**

    ![Screenshot der Nachricht nur mit der Schaltfläche "OK" ](images/win-dialog-box-image35.png)

    In diesem Beispiel wird die Schaltfläche Schließen auf der Titelleiste so angezeigt, als hätten Benutzer keine Auswahl.

-   **Verwenden Sie die Schaltflächen Abbrechen nicht, um auf Fragen zu antworten.**

    **Falsch:**

    ![Screenshot der Nachricht mit "OK" für Ja-Nein-Frage ](images/win-dialog-box-image36.png)

    In diesem Beispiel werden OK und Abbrechen fälschlicherweise verwendet, um auf die Frage Ja oder Nein zu antworten.

-   **Weisen Sie Cancel keine Zugriffsschlüssel zu, da esc der Zugriffsschlüssel ist.** Dadurch wird die Zuweisung der anderen Zugriffsschlüssel vereinfacht.
-   **Verwenden Sie in nicht moduslosen Dialogfeldern keine Schaltflächen abbrechen.** Verwenden Sie stattdessen Schließen.
-   **Deaktivieren Sie nicht die Schaltfläche Abbrechen.** Benutzer sollten immer in der Lage sein, Dialogfelder abzubricht.
    -   **Ausnahme:** Sie können die Schaltfläche Abbrechen in einem Statusdialogfeld deaktivieren, wenn es einen Zeitraum gibt, in dem der Vorgang nicht abgebrochen werden kann. Eine bessere Lösung ist jedoch, solche Vorgänge so zu entwerfen, dass sie immer abgebrochen werden können.

**Schaltflächen schließen**

-   **Verwenden Sie Schaltflächen schließen für nicht modale Dialogfelder sowie modale Dialoge, die nicht abgebrochen werden können.**
-   **Wenn Sie auf Schließen klicken, wird das Dialogfeldfenster geschlossen, und es werden alle vorhandenen Nebeneffekte hinterlassen.** Verwenden Sie done nicht, da es sich nicht um eine imperative Konstruktion handelt. Bei geschachtelten Auswahldialogfeldern bedeutet das Klicken auf Schließen im Dialogfeld für die Besitzerauswahl, dass alle Änderungen beibehalten werden, die von Dialogfeldern für die Auswahl im Besitz des Besitzers vorgenommen wurden.
-   **Legen Sie eine explizite Schaltfläche Schließen in den Text des Dialogfelds ein.** Dialogfelder benötigen einen eindeutigen Ausgangspunkt. Verlassen Sie sich nicht darauf, dass Benutzer die Schaltfläche Schließen auf der Titelleiste finden.
-   **Stellen Sie sicher, dass die Schaltfläche Schließen auf der Titelleiste die gleiche Auswirkung wie Abbrechen oder Schließen hat.**
-   **Weisen Sie close keine Zugriffsschlüssel zu, da es sich bei esc um den Zugriffsschlüssel handelt.** Dadurch wird die Zuweisung der anderen Zugriffsschlüssel vereinfacht.

**Schaltflächen anwenden**

-   **Verwenden Sie keine Schaltflächen anwenden in Dialogfeldern, bei denen es sich nicht um Eigenschaftenblätter oder Systemsteuerungen handelt.** Die Schaltfläche Übernehmen bedeutet, dass die ausstehenden Änderungen angewendet werden, aber das Fenster geöffnet lassen. Auf diese Weise können Benutzer die Änderungen auswerten, bevor sie das Fenster schließen. Diese Notwendigkeit ist jedoch nur für Eigenschaftenblätter und Steuerungspanels notwendig.

    **Falsch:**

    ![Screenshot des Dialogfelds mit Schaltfläche "Anwenden" ](images/win-dialog-box-image37.png)

    In diesem Beispiel verfügt ein Auswahldialogfeld unnötigerweise über die Schaltfläche Anwenden.

**Commitschaltflächen für indirekte Dialogfelder**

**Hinweis:** Indirekte Dialogfelder werden nicht im Kontext angezeigt, entweder als indirektes Ergebnis einer Aufgabe oder als Ergebnis eines Problems mit einem System- oder Hintergrundprozess. Bei indirekten Dialogen ist die Schaltfläche Abbrechen mehrdeutig, da dies bedeuten kann, dass der Dialog abgebrochen oder die gesamte Aufgabe abgebrochen wird.

-   **Wenn Benutzer sowohl das Dialogfeld als auch die Aufgabe abbrechen müssen, geben Sie Commitschaltflächen an, um beides zu tun.** Beschriften Sie die Schaltfläche, die das Dialogfeld mit einer negativen Antwort auf die main-Anweisung abbricht. Beschriften Sie die Schaltfläche, die die gesamte Aufgabe abbricht, mit Abbrechen. Die Verwendung von Abbrechen ermöglicht die Verwendung des Dialogfelds in vielen Kontexten.

    **Richtig:**

    ![Screenshot des Dialogfelds mit "Speichern"/"Nicht speichern" ](images/win-dialog-box-image38.png)

    In diesem Beispiel wird dieses Dialogfeld von Windows Paint als Ergebnis eines New- oder Exit-Befehls angezeigt, wenn die Grafik nicht gespeichert wurde. Nicht speichern schließt das Dialogfeld, ohne es zu speichern, während Abbrechen den Befehl Neu oder Beenden abbricht.

    **Falsch:**

    ![Screenshot des Dialogfelds mit Ja/Nein-Schaltflächen ](images/win-dialog-box-image39.png)

    In diesem Beispiel gibt es keine Möglichkeit, die Aufgabe abzubricht (schließen Office Verknüpfungsleiste), die zur Anzeige dieses Dialogfelds geführt hat. Dieses Dialogfeld benötigt die Schaltfläche Abbrechen.

-   **Wenn Benutzer nur den** Dialog abbrechen müssen, aber nicht die Aufgabe, verwenden Sie eine Schaltfläche mit einer bestimmten, negativen Antwort auf die main-Anweisung, und verfügen nicht über die Schaltfläche Abbrechen.

    ![Screenshot des Dialogfelds mit "Ausführen/Nicht ausführen" ](images/win-dialog-box-image24.png)

    In diesem Beispiel wird dieses Dialogfeld indirekt als Ergebnis der Navigation zu einer Webseite angezeigt, die ein ActiveX installiert. Die Verwendung von Abbrechen wäre hier mehrdeutig, daher wird stattdessen Nicht ausführen verwendet.

Weitere Informationen und Beispiele finden Sie unter [Befehlsschaltflächen.](ctrl-command-buttons.md)

### <a name="command-links"></a>Befehlslinks

-   **Stellen Sie eine Reihe von langen Befehlen mit Befehlslinks anstelle von Befehlsschaltflächen oder einer Kombination aus Optionsfeldern und einer SCHALTFLÄCHE OK vor.** Auf diese Weise können Benutzer mit einem einzigen Klick antworten. Dieser Ansatz funktioniert jedoch nur für eine einzelne Frage.
-   **Stellen Sie zuerst die am häufigsten verwendeten Befehlslinks vor.** Die resultierende Reihenfolge sollte ungefähr der Wahrscheinlichkeit der Verwendung folgen, aber auch einen logischen Fluss haben.
    -   **Ausnahme:** Befehlslinks, die dazu führen, dass alles ausgeführt wird, sollten zuerst platziert werden.
-   Wenn ein Befehlslink eine weitere Erläuterung erfordert, **geben Sie eine zusätzliche Erklärung an.** Ergänzende Erläuterungen beschreiben, warum Benutzer den Befehl auswählen möchten oder was geschieht, wenn der Befehl ausgewählt wird.
-   **Verwenden Sie keine ergänzenden Erklärungen, bei denen es sich um wortige Neuordnungen des Befehlslinks handelt.** Verwenden Sie eine ergänzende Erklärung nur, wenn Sie einen Befehlslink nicht selbsterklärend machen können. Das Bereitstellen einer ergänzenden Erklärung für einen Befehlslink bedeutet nicht, dass Sie sie für alle Befehle bereitstellen müssen.

![Screenshot des Dialogfelds mit Text notierungsoptionen ](images/win-dialog-box-image40.png)

In diesem Beispiel beschreibt die ergänzende Erklärung die Auswirkungen einer der Optionen.

-   **Verwenden Sie Ausdrücke, die mit einem Verb beginnen, ohne die Interpunktion zu beenden.**
-   **Wenn ein Befehl dringend empfohlen wird, sollten Sie der Bezeichnung "(recommended)" hinzufügen.** Achten Sie darauf, der Linkbezeichnung und nicht der ergänzenden Erklärung hinzuzufügen.
-   **Wenn ein Befehl nur für fortgeschrittene Benutzer vorgesehen ist, sollten Sie der Bezeichnung "(advanced)" hinzufügen.** Achten Sie darauf, der Linkbezeichnung und nicht der ergänzenden Erklärung hinzuzufügen.
-   **Geben Sie immer eine explizite Schaltfläche Abbrechen an.** Verwenden Sie zu diesem Zweck keinen Befehlslink.

**Falsch:**

![Screenshot des Dialogfelds ohne Link zum Beenden ](images/win-dialog-box-image41.png)

In diesem Beispiel verwendet das Dialogfeld einen Befehlslink anstelle einer Schaltfläche Abbrechen.

Weitere Informationen und Beispiele finden Sie unter [Befehlslinks.](ctrl-command-links.md)

### <a name="dont-show-this-item-again"></a>Nicht anzeigen <item> Wieder

-   **Erwägen Sie die Verwendung der Option Nicht mehr anzeigen, damit Benutzer ein wiederkehrendes Dialogfeld unterdrücken können, nur wenn es keine bessere <item> Alternative gibt.** Es ist besser, den Dialog immer anzuzeigen, wenn Benutzer ihn wirklich benötigen, oder ihn einfach zu beseitigen, wenn dies nicht der Fehler ist.
-   **Verwenden Sie diesen spezifischen Ausdruck, und <item> ersetzen Sie durch das spezifische Element.** Zeigen Sie diese Erinnerung beispielsweise nicht erneut an. Wenn Sie im Allgemeinen auf ein Dialogfeld verweisen, verwenden Sie Diese Meldung nicht erneut anzeigen.
-   **Geben Sie eindeutig an,** wann Benutzereingaben für zukünftige Standardwerte verwendet werden, indem Sie den folgenden Satz unter der Option hinzufügen: Ihre Auswahl wird in Zukunft standardmäßig verwendet.
-   **Wählen Sie die Option nicht standardmäßig aus. Wenn das Dialogfeld wirklich nur einmal angezeigt werden soll, tun Sie dies, ohne eine Frage zu stellen.** Verwenden Sie diese Option nicht als lästig für lästige Benutzer, um sicherzustellen, dass das Standardverhalten nicht lästig ist.

**Falsch:**

![Screenshot der Meldung mit unnötiger Frage ](images/win-dialog-box-image42.png)

In diesem Beispiel sollte die Meldung nur einmal angezeigt werden. Es ist nicht notwendig, zu fragen.

-   **Sorgen Sie dafür, dass die Einstellung auf Benutzerbasis beibehalten wird.**
-   **Wenn Benutzer die Option auswählen und auf Abbrechen klicken, wird diese Option wirksam.** Diese Einstellung ist eine Metaoption, sodass sie nicht dem standardmäßigen Cancel-Verhalten folgt, bei dem keine Nebeneffekte hinterlassen werden. Beachten Sie: Wenn Benutzer den Dialog in Zukunft nicht mehr sehen möchten, möchten sie ihn wahrscheinlich auch abbrechen.
-   Wenn Benutzer diese Dialogfelder möglicherweise wiederherstellen müssen, geben Sie im Dialogfeld Optionen des Programms den Befehl Nachrichten wiederherstellen an. 

### <a name="ask-me-later"></a>Später nachfragen

-   Geben Sie diese Option an, um ein Dialogfeld nur dann zu schließen, wenn:
    -   **Das Dialogfeld ist indirekt,** sodass benutzer sich wahrscheinlich auf eine andere Aufgabe konzentrieren.
    -   **Benutzer müssen reagieren, aber nicht sofort,** damit sie ihre Arbeit fortsetzen können.
    -   **Die Frage erfordert ausreichende Überlegungen oder Anstrengungen,** sodass Benutzer bessere Entscheidungen treffen können, wenn ihnen mehr Zeit zur Verfügung steht.
    -   **Das Dialogfeld oder die Option wird später automatisch angezeigt** (sodass Benutzer später wirklich gefragt werden).
-   **Falsch:**
-   ![Screenshot der Nachricht mit der Option "Später fragen" ](images/win-dialog-box-image43.png)
-   In diesem Beispiel ist die Frage so einfach, dass das Hinzufügen einer Später stellen-Option dies nur erschwert.
-   Andernfalls erwarten Sie, dass Benutzer jetzt antworten, aber zulassen, dass sie das Dialogfeld normalerweise mit Abbrechen oder Schließen schließen können. Bei ordnungsgemäßer Verwendung sollte diese Option selten sein.

### <a name="morefewer"></a>Mehr/weniger

-   **Verwenden Sie mehr/weniger Schaltflächen für die progressive Offenlegung, um erweiterte oder selten verwendete Optionen, Befehle oder Details anzuzeigen oder auszublenden, die Benutzer normalerweise nicht benötigen.** Dadurch wird das Dialogfeld für die typische Verwendung vereinfacht. Blenden Sie häufig verwendete Optionen, Befehle oder Informationen nicht aus, da Benutzer sie möglicherweise nicht finden.

![Screenshot des Dialogfelds mit schaltfläche "Weitere Optionen" ](images/win-dialog-box-image24.png)

In diesem Beispiel werden selten verwendete Optionen standardmäßig ausgeblendet.

-   **Verwenden Sie keine Mehr-/Weniger-Steuerelemente, es sei denn, es sind wirklich mehr Details zu sehen.** Stellen Sie nicht einfach die gleichen Informationen in einem anderen Format wieder her.
-   **Verwenden Sie keine Mehr/Weniger-Steuerelemente, um Hilfe anzuzeigen.** Verwenden Sie stattdessen Hilfelinks oder Fußnoten.
-   **Vermeiden Sie bei Aufgabendialogen die Kombination von Mehr/Weniger-Steuerelementen mit Nicht <item> mehr anzeigen.** Diese Kombination hat eine umständliche Darstellung.
-   Informationen zu Bezeichnungsrichtlinien finden Sie unter [Progressive Offenlegung.](ctrl-progressive-disclosure-controls.md)

### <a name="footnotes"></a>Fußnoten

-   **Verwenden Sie Fußnoten für Informationen, die für den Zweck eines Dialogfelds nicht wichtig sind, die benutzer jedoch möglicherweise hilfreich sind, um Entscheidungen zu treffen.** Die meisten Benutzer sollten Fußnoten überspringen und dennoch fundierte Entscheidungen in ihrer Reaktion auf das Dialogfeld treffen können.

![Screenshot des Dialogfelds mit verdeutlichender Fußnote ](images/win-dialog-box-image44.png)

In diesem Beispiel sind die Fußnoteninformationen ergänzend, nicht wesentlich.

### <a name="disabling-or-removing-controls-vs-giving-error-messages"></a>Deaktivieren oder Entfernen von Steuerelementen im Vergleich zur Angabe von Fehlermeldungen

-   Wenn ein Steuerelement im aktuellen Kontext nicht angewendet wird, sollten Sie die folgenden Optionen in Betracht ziehen:
    -   **Entfernen Sie das Steuerelement, wenn es für Benutzer nicht möglich ist, es zu aktivieren, oder Benutzer nicht erwarten, dass es angewendet wird und sich sein Zustand nicht häufig ändert.** Dadurch wird das Dialogfeld vereinfacht, und Benutzer werden es nicht übersehen. Es ist ungärrlich, wenn ein Steuerelement häufig angezeigt und ausgeblendet wird.
    -   **Deaktivieren Sie das Steuerelement, wenn Benutzer erwarten, dass es angewendet wird oder sich sein Zustand häufig ändert, und Benutzer leicht ableiten können, warum das Steuerelement deaktiviert ist.** Ein Beispiel für eine einfache Ableitung ist das Deaktivieren einer Commitschaltfläche, wenn ein einzelnes leeres Textfeld vorhanden ist, das eine Eingabe erfordert. Sie können [Sprechblasen](ctrl-balloons.md) verwenden, um nicht kritische Benutzereingabeprobleme mit Textfeldern und bearbeitbaren Dropdownlisten anzuzeigen. Wenn das Problem jedoch nicht mit einem Balloon erklärt werden kann oder mehrere Steuerelemente umfasst, wäre die Ableitung nicht mehr einfach.
    -   **Andernfalls lassen Sie das Steuerelement aktiviert, geben aber eine Fehlermeldung aus, wenn es falsch verwendet wird.** Wenn Sie in diesem Fall deaktivieren, ist es für Benutzer schwierig zu verstehen, warum das Steuerelement deaktiviert ist. Benutzer werden gezwungen, das Problem durch Experimentieren und deductive Logik zu bestimmen. Es ist besser, nur eine hilfreiche Fehlermeldung bereitzustellen, um das Problem explizit zu erklären.
-   **Tipp:** Wenn Sie nicht sicher sind, ob Sie ein Steuerelement deaktivieren oder eine Fehlermeldung geben sollten, erstellen Sie zunächst die Fehlermeldung, die Sie möglicherweise geben. Wenn die Fehlermeldung hilfreiche Informationen enthält, die Zielbenutzer wahrscheinlich nicht schnell ableiten, lassen Sie das Steuerelement aktiviert, und geben Sie den Fehler an. Andernfalls deaktivieren Sie das Steuerelement.
-   **Wenn Sie ein Steuerelement deaktivieren, deaktivieren Sie auch alle zugeordneten Steuerelemente,** z. B. die zugehörige Bezeichnung, ergänzende Erklärungen oder Befehlsschaltflächen. Deaktivieren Sie jedoch nicht die [Gruppenfelder](ctrl-group-boxes.md), die Gruppenbezeichnung oder die Gruppenerklärung, falls vorhanden.

![Screenshot des Dialogfelds mit abgeblendeten Steuerelementen ](images/win-dialog-box-image45.png)

In diesem Beispiel sind die deaktivierten Textfeldbezeichnungen ebenfalls deaktiviert, die Gruppenbezeichnung und die Gruppenerklärung hingegen nicht.

### <a name="required-input"></a>Erforderliche Eingabe

-   Um anzugeben, dass Benutzer Informationen in einem Steuerelement bereitstellen müssen, sollten Sie die folgenden Optionen in Betracht ziehen:
    -   **Geben Sie nichts an, aber behandeln Sie fehlende erforderliche Eingaben mit Fehlermeldungen.** Dieser Ansatz reduziert die Unübersichtlichkeit und funktioniert gut, wenn die meisten Eingaben optional sind oder Benutzer die Steuerelemente wahrscheinlich nicht überspringen, wodurch die Anzahl der Fehlermeldungen gering bleibt.
    -   **Geben Sie die erforderliche Eingabe mit einem Sternchen am Anfang der Bezeichnung an.** Erläutern Sie das Sternchen mit einem der beiden:

        -   Eine Fußnote am unteren Rand des Inhaltsbereichs mit \* erforderlicher Eingabe.
        -   Eine QuickInfo auf dem Sternchen mit der Angabe Erforderliche Eingabe.

        Dieser Ansatz funktioniert gut, wenn nicht viele erforderliche Steuerelemente erforderlich sind, aber schlecht, wenn die meisten Steuerelemente erforderlich sind.

        ![Screenshot von Textfeldbeschriftungen mit Sternchen ](images/win-dialog-box-image46.png)

        In diesem Beispiel werden Sternchen verwendet, um die erforderliche Eingabe anzugeben.

    -   **Wenn alle Steuerelemente Eingaben erfordern, geben Sie "Alle Eingaben erforderlich" an einer geeigneten Stelle am oberen Rand des Inhaltsbereichs an.** Dieser Ansatz reduziert die Unübersichtlich für diesen speziellen Fall.
    -   **Geben Sie optionale Eingaben mit "(optional)" nach der Bezeichnung an.** Dieser Ansatz funktioniert gut, wenn die meisten Eingaben erforderlich sind, andernfalls jedoch schlecht.

-   **Versuchen Sie aus Konsistenzgründen, dieselbe Methode zu verwenden, um die erforderliche Eingabe im gesamten Programm anzugeben.** Geben Sie bei Bedarf entweder erforderliche oder optionale Eingaben an, vermeiden Sie jedoch die Verwendung beider Eingaben innerhalb desselben Programms.

### <a name="error-handling"></a>Fehlerbehandlung

-   Verhindern Sie Fehler, indem Sie Steuerelemente verwenden, die auf gültige Benutzereingaben beschränkt sind. Sie können auch die Anzahl der Fehler reduzieren, indem Sie sinnvolle Standardwerte bereitstellen.
-   Überprüfen Sie die Benutzereingabe so schnell wie möglich, und zeigen Sie Fehler so genau wie möglich an den Eingabepunkt an.
-   **Verwenden Sie die moduslose Fehlerbehandlung (direkt auftretende Fehler oder Sprechblasen) für Benutzereingabeprobleme.**
    -   **Verwenden Sie Sprechblasen für nicht kritische Benutzereingabeprobleme mit nur einem Punkt, die erkannt wurden, während sie in einem Textfeld oder unmittelbar nach dem Verlust des Fokus in einem Textfeld erkannt wurden.** Für Sprechblasen ist kein verfügbarer Bildschirmbereich oder das dynamische Layout erforderlich, das zum Anzeigen von Nachrichten an Ort und Stelle erforderlich ist. Zeigt nur einen einzelnen Sprechblasen gleichzeitig an. Da das Problem nicht kritisch ist, ist kein Fehlersymbol erforderlich. Sprechblasen werden beim Klicken, beim Beheben des Problems oder nach einem Timeout entfernt.

        ![Screenshot der Meldung "Falsches Zeichen" ](images/win-dialog-box-image47.png)

        In diesem Beispiel zeigt eine Sprechblase ein Eingabeproblem an, während es sich noch im -Steuerelement begibt.

-   **Verwenden Sie für die verzögerte Fehlererkennung fehlerbasierte Fehler.** In der Regel werden Fehler gefunden, indem Sie auf eine Commitschaltfläche klicken. (Verwenden Sie keine direkten Fehler für Einstellungen, für die sofort ein Commit ausgeführt wird.) Es können mehrere fehlerverdingende Fehler gleichzeitig auftreten. Verwenden Sie normalen Text und ein 16 x 16 Pixel großes Fehlersymbol, und platzieren Sie sie nach Möglichkeit direkt neben dem Problem. Direkt auftretende Fehler werden nur dann entfernt, wenn der Benutzer einen Commit vorgibt und keine anderen Fehler gefunden werden.

    ![Screenshot des Dialogfelds mit zwei Fehlermeldungen ](images/win-dialog-box-image48.png)

    In diesem Beispiel wird ein direkt auftretender Fehler für einen Fehler verwendet, der durch Klicken auf die Commitschaltfläche gefunden wurde.

-   **Verwenden Sie modale Fehlerbehandlung (Aufgabendialoge oder Meldungsfelder) für alle anderen Probleme,** einschließlich Fehlern, die mehrere Steuerelemente betreffen, oder bei denen es sich um nicht kontextbezogene oder nicht eingabebezogene Fehler handelt, die durch Klicken auf eine Commitschaltfläche gefunden werden.
-   **Wenn ein Eingabeproblem gefunden und gemeldet wird, legen Sie den Eingabefokus auf das erste Steuerelement mit den falschen Daten fest.** Scrollen Sie das Steuerelement bei Bedarf in die Ansicht.

Weitere Informationen und Beispiele finden Sie unter [Fehlermeldungen](mess-error.md) und [Sprechblasen.](ctrl-balloons.md)

### <a name="help"></a>Hilfe

-   Berücksichtigen Sie bei der Bereitstellung von Benutzerunterstützung die folgenden Optionen (in ihrer Bevorzugtkeitsreihenfolge aufgeführt):
    -   Geben Sie interaktiven Steuerelementen selbsterklärende Bezeichnungen. Benutzer lesen die Bezeichnungen in interaktiven Steuerelementen wahrscheinlicher als jeder andere Text.
    -   Geben Sie Kontexterklärungen mit [statischen Textbeschriftungen](text-ui.md)an.
    -   Geben Sie einen bestimmten Hilfelink zu einem relevanten Hilfethema an.
-   **Suchen Sie unten im Inhaltsbereich des Dialogfelds nach Hilfelinks.** Wenn das Dialogfeld eine Fußnote enthält und der Link Hilfe damit verknüpft ist, platzieren Sie den Hilfelink in der Fußnote.

    ![Screenshot des Dialogfelds mit Hilfelink ](images/win-dialog-box-image40.png)

    In diesem Beispiel gilt der Hilfelink für den gesamten Dialog.

    -   **Ausnahme:** Wenn ein Dialogfeld mehrere verschiedene Gruppen von Einstellungen mit separaten Hilfethemen (möglicherweise innerhalb von Gruppenfeldern) enthält, suchen Sie die Hilfelinks am unteren Rand der Gruppen.

-   **Verwenden Sie keine allgemeinen oder ungenauen Links zu Hilfethemen oder generische Hilfeschaltflächen.** Benutzer ignorieren häufig die generische Hilfe.

Weitere Informationen und Beispiele finden Sie unter [Hilfe.](winenv-help.md)

### <a name="default-values"></a>Standardwerte

-   Fügen Sie in jedem Dialogfeld eine Standardschaltfläche für Commits ein.
-   Für Fragedialoge:
    -   **Wählen Sie die sicherste Antwort (um Datenverluste oder Systemzugriffe zu verhindern), als Standardantwort aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequemste Antwort aus.
        -   **Ausnahme:** Machen Sie keine destruktive Antwort als Standard, es sei denn, es gibt eine einfache, offensichtliche Möglichkeit, den Befehl rückgängig zu machen.
-   Für Auswahldialoge:
    -   Wählen Sie für die anfänglichen Standardwerte die sichersten Werte (um Datenverluste oder Systemzugriffe zu verhindern) und die sichersten Werte **für jedes Steuerelement aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichsten oder bequemsten Optionen aus.
    -   Wählen Sie für die nachfolgenden Standardwerte die zuvor ausgewählten Optionen erneut aus, wenn diese Werte wahrscheinlich wiederholt werden, und dies **ist sicher und sicher.** Wählen Sie andernfalls die anfänglichen Standardwerte aus.

![Screenshot des Dialogfelds "Drucken" ](images/win-dialog-box-image49.png)

In diesem Beispiel wählen Benutzer wahrscheinlich die gleichen Druckeinstellungen wie beim letzten Mal aus. Die gewünschte Anzahl von Kopien wird sich jedoch wahrscheinlich ändern, sodass diese Einstellung nicht erneut ausgewählt wird.

## <a name="recommended-sizing-and-spacing&quot;></a>Empfohlene Größe und Abstand

-   **Unterstützen Sie die Windows Vista-Bildschirmauflösung von 800 x 600 Pixel.** Layouts können für vergrößerbare Fenster mit einer Bildschirmauflösung von 1024 x 768 Pixeln optimiert werden.
-   **Verwenden Sie nach Möglichkeit verstellbare Fenster, um Bildlaufleisten und abgeschnittene Daten zu vermeiden.** Windows dynamischen Inhalten und Listen profitieren am meisten von verstellbaren Fenstern.
-   **Fenster mit fester Größe müssen vollständig sichtbar sein und so dimensioniert sein, dass sie in den Arbeitsbereich passen.**
-   **Vergrößerbare Fenster können für höhere Auflösungen optimiert werden, aber bei Bedarf zur Anzeigezeit auf die tatsächliche Bildschirmauflösung heruntersetzbar sein.**
-   **Wählen Sie eine Standardfenstergröße aus, die für ihren Inhalt geeignet ist.** Sie sollten keine größeren Anfangsfenster verwenden, wenn Sie den Platz effektiv nutzen können.

## <a name=&quot;text&quot;></a>Text

### <a name=&quot;general&quot;></a>Allgemein

-   **Entfernen Sie redundanten Text.** Suchen Sie in Titeln, Hauptanweisungen, ergänzenden Anweisungen, Inhaltbereichen, Befehlslinks und Commitschaltflächen nach redundantem Text. Lassen Sie im Allgemeinen vollständigen Text in Anweisungen und interaktiven Steuerelementen, und entfernen Sie alle Redundanzen von den anderen Stellen.
-   **Verwenden Sie positive Formulierungen.** Positive Formulierungen sind für Benutzer einfacher zu verstehen.

**Richtig:**

Möchten Sie die Datei- und Druckerfreigabe aktivieren?

**Falsch:**

Möchten Sie die Datei- und Druckerfreigabe deaktivieren?

Der Ausdruck muss jedoch mit dem zugeordneten Befehl übereinstimmen, auch wenn der Befehl negativ formuliert ist. verwenden Sie z. B. disable, um einen Disable-Befehl zu bestätigen.

-   **Verwenden Sie bei Bedarf das Wort &quot;window&quot;, um auf das Dialogfeld selbst zu verweisen.**
-   **Verwenden Sie die zweite Person (&quot;Sie/Ihr"),** um Benutzern zu sagen, was im Hauptanweisungs- und Inhaltsbereich zu tun ist. Häufig wird die zweite Person impliziert.

**Beispiele:**

Wählen Sie die Bilder aus, die Sie drucken möchten.

Wählen Sie ein Konto aus.

-   **Verwenden Sie die erste Person ("I/me/my"),** damit Benutzer dem Programm mitteilen können, was in Steuerelementen im Inhaltsbereich zu tun ist, die auf die Hauptanweisung reagieren.

**Beispiel:** Drucken Sie die Fotos auf meiner Kamera.

### <a name="dialog-box-titles"></a>Titel des Dialogfelds

-   **Verwenden Sie den Titel, um den Befehl, das Feature oder das Programm zu identifizieren, von dem bzw. dem ein Dialogfeld stammt.**
    -   Wenn das Dialogfeld vom Benutzer initiiert wird, identifizieren Sie es mithilfe des Befehls oder des Featurenamens. **Ausnahmen:**
        -   Wenn ein Dialogfeld von vielen verschiedenen Befehlen angezeigt wird, sollten Sie stattdessen den Programmnamen verwenden.
        -   Wenn dieser Titel mit der main-Anweisung redundant wäre, verwenden Sie stattdessen den Programmnamen.
    -   Wenn es programm- oder systemin initiiert ist (und daher nicht im Kontext liegt), identifizieren Sie es mithilfe des Programm- oder Featurenamens, um Kontext zu geben.
    -   Verwenden Sie den Titel nicht, um zu erläutern, was im Dialog zu tun ist, der der Zweck der Hauptanweisung ist.
-   Verwenden Sie den genauen Befehlsnamen für befehlsbasierte Namen, aber schließen Sie die Auslassungsellipse nicht ein, wenn ein Befehlsnamen vor ort ist. Sie können den Menütitel des Befehls bei Bedarf hinzufügen, um einen guten Titel zu erstellen. Beispiel: für ein Objekt... Befehl in einem Insert-Menü verwenden Sie den Titel Objekt einfügen.
-   **Wenn ein modusloses Dialogfeld** auf der Taskleiste angezeigt wird, optimieren Sie den Titel für die Anzeige auf der Taskleiste, indem Sie die unterscheidenden Informationen präzise an erster Stelle platzieren. Beispiele: "66 % abgeschlossen" und "3 Erinnerungen".
-   **Schließen Sie die Wörter "dialog" oder "progress" nicht in den Titel ein.** Dies ist impliziert, und das Deaktivieren erleichtert benutzern das Scannen.
-   Verwenden [Sie die Groß-/End-Groß-/Formatvorlage,](glossary.md)ohne die Interpunktion zu beenden.

### <a name="main-instructions"></a>Hauptanweisungen

-   **Verwenden Sie die Main-Anweisung, um präzise zu erläutern, was im Dialog zu tun ist.** Die Anweisung sollte eine bestimmte Anweisung, imperative Richtung oder Frage sein. Gute Anweisungen kommunizieren das Ziel des Benutzers mit dem Dialog, anstatt sich ausschließlich auf die Mechanismen der Bearbeitung zu konzentrieren.
-   **Lassen Sie die main-Anweisung weg, wenn das einzige, was Sie sagen können, offensichtlich ist.** In solchen Fällen ist der Inhalt des Dialogfelds selbsterklärend. Beispielsweise benötigen die allgemeinen Dialogfelder Datei öffnen und Datei speichern keine Hauptanweisung, da ihr Kontext und Ihr Entwurf ihren Zweck offensichtlich machen.
-   **Lassen Sie Steuerelementbezeichnungen weg, die die Hauptanweisung neu erstellen.** In diesem Fall übernimmt die main-Anweisung den Zugriffsschlüssel.

**Annehmbar:**

![Screenshot des Textfelds mit redundanter Bezeichnung ](images/win-dialog-box-image50.png)

In diesem Beispiel ist die Textfeldbezeichnung nur eine Neuformung der Main-Anweisung.

**Besser:**

![Screenshot des gleichen Textfelds mit einer Bezeichnung ](images/win-dialog-box-image51.png)

In diesem Beispiel wird die redundante Bezeichnung entfernt, sodass die main-Anweisung den Zugriffsschlüssel übernimmt.

-   **Seien Sie präzise, verwenden Sie nur einen einzelnen vollständigen Satz.** Sehen Sie sich die Hauptanweisung auf die wesentlichen Informationen an. Wenn Sie mehr erklären müssen, verwenden Sie zusätzliche Anweisungen.
-   **Verwenden Sie nach Möglichkeit bestimmte Verben.** Bestimmte Verben (Beispiele: Verbinden, Speichern, Installieren) sind für Benutzer sinnvoller als generische Verben (Beispiele: Konfigurieren, Verwalten, Festlegen).
-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)
-   **Schließen Sie keine abschließenden Zeiträume ein, wenn die Anweisung eine -Anweisung ist.** Wenn es sich bei der Anweisung um eine Frage handelt, fügen Sie ein abschließendes Fragezeichen ein.
-   **Verwenden Sie für Statusdialoge einen Gerund-Ausdruck,** der den vorgang in Bearbeitung kurz erläutert und mit auslassungsenden Auslassungsfeldern endet. Beispiel: Drucken ihrer Bilder...
-   **Tipp:** Sie können eine Hauptanweisung auswerten, indem Sie sich vorstellbar machen, was Sie einem Freund sagen würden. Wenn die Antwort mit der main-Anweisung unnatürlich, nicht hilfreich oder umstirnlich wäre, überarbeiten Sie die Anweisung.

### <a name="supplemental-instructions"></a>Zusätzliche Anweisungen

-   **Verwenden Sie bei Bedarf eine optionale zusätzliche Anweisung, um zusätzliche Informationen anzuzeigen, die für das Verständnis oder die Verwendung der Seite hilfreich sind.** Sie können ausführlichere Informationen bereitstellen und Terminologie definieren.
-   **Wenn die Darstellung des Dialogfelds programm- oder systemin initiiert ist (und daher nicht im Kontext liegt), verwenden Sie die ergänzende Anweisung, um zu erläutern, warum der Dialog angezeigt wurde.** Bei solchen Dialogen ist der Kontext in der Regel nicht offensichtlich.
-   **Wiederholen Sie die Hauptanweisung nicht mit etwas anderen Formulierungen.** Lassen Sie stattdessen die zusätzliche Anweisung weg, wenn nicht mehr hinzugefügt werden muss.
-   Verwenden Sie vollständige Sätze, Groß- und Groß-/Endzeichen im Satzstil.

### <a name="command-links"></a>Befehlslinks

-   **Wählen Sie präzisen Linktext aus, der eindeutig kommuniziert und unterscheidet, was der Befehlslink tut.** Sie sollte selbsterklärend sein und der Main-Anweisung entsprechen. Benutzer sollten nicht herausfinden müssen, was der Link wirklich bedeutet oder wie er sich von anderen Links unterscheidet.
-   **Der Befehl "Start" wird immer mit einem Verb verknüpft.**
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Verwenden Sie keine Interpunktion am Ende.
-   **Geben Sie ggf. eine weitere Erklärung mit vollständigen Sätzen und endender Interpunktion an.** Fügen Sie solche Erklärungen jedoch nur bei Bedarf hinzu, und fügen Sie nicht allen Befehlslinks Erklärungen hinzu, nur weil ein Befehlslink einen benötigt.

Weitere Informationen und Beispiele finden Sie unter Richtlinien für [Befehlslinks.](ctrl-command-links.md)

### <a name="commit-buttons"></a>Commitschaltflächen

-   **Verwenden Sie bestimmte Commitschaltflächenbezeichnungen, die eigenständig sinnvoll sind und eine Antwort auf die Hauptanweisung sind.** Im Idealfall sollten Benutzer nichts anderes lesen müssen, um die Bezeichnung zu verstehen. Die Wahrscheinlichkeit, dass Benutzer Befehlsschaltflächenbezeichnungen lesen, ist weitaus wahrscheinlicher als statischer Text.
-   **Starten Sie Commit-Schaltflächenbezeichnungen mit einem Verb. Ausnahmen sind OK, Ja und Nein.**
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Verwenden Sie keine Interpunktion am Ende.
-   Weisen Sie einen eindeutigen [Zugriffsschlüssel zu.](glossary.md)
    -   **Ausnahme:** Weisen Sie den Schaltflächen OK und Abbrechen keine Zugriffsschlüssel zu, da eingabe und esc ihre Zugriffsschlüssel sind. Auf diese Weise können die anderen Zugriffsschlüssel einfacher zugewiesen werden.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Dialogfelder:

-   In der Programmierung und anderen technischen Dokumentationen finden Sie dialogfelder als Dialogfelder. Verweisen Sie an allen anderen Stellen anhand ihres Titels auf Dialogfelder. Wenn die Titelleiste ausgeblendet ist, lesen Sie den Dialog mithilfe der Main-Anweisung.
-   Wenn Sie im Allgemeinen auf ein Dialogfeld verweisen müssen, verwenden Sie das Fenster in der Benutzerdokumentation. Sie können auf ein einfaches Fragedialogfeld oder eine Bestätigung als Nachricht verweisen.
-   Verwenden Sie den genauen Titel oder Hauptanweisungstext, einschließlich der Groß-/Großschreibung.
-   Formatieren Sie den Titel nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie den Titel nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

Beispiel: Klicken Sie **in Windows-Sicherheit** auf **Weitere Optionen.**

