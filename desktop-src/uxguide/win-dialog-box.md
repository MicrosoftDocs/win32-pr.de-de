---
title: Dialogfelder (Entwurfsgrundlagen)
description: Ein Dialogfeld ist ein sekundäres Fenster, in dem Benutzer einen Befehl ausführen, Benutzern eine Frage stellen oder Benutzern Informationen oder Fortschrittsfeedback zur Verfügung stellen können.
ms.assetid: 2ded9f30-d45f-4027-a85d-4e7d0e412793
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b0e0deb28a706436e4d33ece35a40c26bd7499e0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444851"
---
# <a name="dialog-boxes-design-basics"></a>Dialogfelder (Entwurfsgrundlagen)

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Ein Dialogfeld ist ein sekundäres Fenster, in dem Benutzer einen Befehl ausführen, Benutzern eine Frage stellen oder Benutzern Informationen oder Fortschrittsfeedback zur Verfügung stellen können.

![Screenshot: Identifizieren von Dialogfeldelementen ](images/win-dialog-box-image1.png)

Ein typisches Dialogfeld.

Dialogfelder bestehen aus einer Titelleiste (um den Befehl, das Feature oder das Programm zu identifizieren, von dem ein Dialogfeld stammt), einer optionalen Hauptanweisung (um das Ziel des Benutzers mit dem Dialogfeld zu erklären), verschiedenen Steuerelementen im Inhaltsbereich (um Optionen anzuzeigen) und Commitschaltflächen (um anzugeben, wie der Benutzer einen Commit für die Aufgabe ausführen möchte).

Dialogfelder verfügen über zwei grundlegende Typen:

-   **Modale Dialogfelder** erfordern, dass Benutzer abgeschlossen und geschlossen werden, bevor sie mit dem Besitzerfenster fortfahren. Diese Dialogfelder eignen sich am besten für kritische oder seltene, einmalige Aufgaben, die abgeschlossen werden müssen, bevor Sie fortfahren.
-   **Mithilfe** von dialogfelder ohne Modus können Benutzer nach Bedarf zwischen dem Dialogfeld und dem Besitzerfenster wechseln. Diese Dialogfelder eignen sich am besten für häufige, sich wiederholende, laufende Aufgaben.

**Ein Aufgabendialog ist ein Dialogfeld, das mithilfe der Api (Application Programming Interface) des Aufgabendialogfelds implementiert wird.** Sie bestehen aus den folgenden Teilen, die in einer Vielzahl von Kombinationen zusammengesetzt werden können:

-   Eine **Titelleiste** zum Identifizieren der Anwendungs- oder Systemfunktion, von der das Dialogfeld stammt.
-   Eine **Hauptanweisung** mit einem optionalen Symbol, um das Ziel des Benutzers mit dem Dialogfeld zu identifizieren.
-   Ein **Inhaltsbereich** für beschreibende Informationen und Steuerelemente.
-   Einen **Befehlsbereich** für Commitschaltflächen, einschließlich der Schaltfläche Abbrechen, und optionale Optionen "Weitere" und "Nicht anzeigen" <item> -Steuerelemente erneut.
-   Ein **Fußnotenbereich** für optionale zusätzliche Erklärungen und Hilfe, der in der Regel für weniger erfahrene Benutzer vorgesehen ist.

![Screenshot eines typischen Aufgabendialogfelds ](images/win-dialog-box-image2.png)

Ein typisches Aufgabendialogfeld.

**Aufgabendialoge werden nach Bedarf empfohlen, da sie einfach zu erstellen sind und ein konsistentes Aussehen erzielen.** Aufgabendialogfelder erfordern Windows Vista oder höher, sodass sie nicht für frühere Versionen von Microsoft Windows geeignet sind.

Ein Aufgabenbereich ähnelt einem Dialogfeld, mit dem Unterschied, dass er in einem Fensterbereich anstelle eines separaten Fensters angezeigt wird. Daher haben Aufgabenbereiche ein direkteres, kontextbezogenes Gefühl als Dialogfelder. Obwohl sie technisch gesehen nicht identisch sind, **ähneln Aufgabenbereiche Dialogfeldern so, dass ihre Richtlinien in diesem Artikel vorgestellt werden.**

![Screenshot eines typischen Aufgabenbereichs ](images/win-dialog-box-image3.png)

Ein typischer Aufgabenbereich.

[Eigenschaftenfenster](win-property-win.md) sind ein spezieller Dialogfeldtyp, der zum Anzeigen und Ändern von Eigenschaften für ein Objekt, eine Auflistung von Objekten oder ein Programm verwendet wird. Darüber hinaus unterstützen Eigenschaftenfenster in der Regel mehrere Aufgaben, während Dialogfelder in der Regel einen einzelnen Task oder Schritt in einer Aufgabe unterstützen. Da ihre Verwendung spezialisiert ist, **werden Eigenschaftenfenster in einem anderen Satz von Richtlinien behandelt.**

Dialogfelder können [Registerkarten](ctrl-tabs.md)aufweisen, und wenn ja, werden sie als Dialogfelder im Registerkartenbett bezeichnet. Eigenschaftenfenster werden durch ihre Darstellung von Eigenschaften bestimmt, nicht durch die Verwendung von Registerkarten.

**Hinweis:** Richtlinien im Zusammenhang mit [Layout,](vis-layout.md) [Fensterverwaltung,](win-window-mgt.md)allgemeinen Dialogfeldern, [Eigenschaftenfenstern,](win-property-win.md) [Assistenten,](win-wizards.md) [Bestätigungen,](mess-confirm.md) [Fehlermeldungen](mess-error.md)und [Warnmeldungen](mess-warn.md) werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Sollen Benutzer Informationen bereitstellen, Benutzern eine Frage stellen oder Benutzern erlauben, Optionen zum Ausführen eines Befehls oder einer Aufgabe auszuwählen?** Falls nicht, verwenden Sie eine andere Benutzeroberfläche .
-   **Sollen Eigenschaften für ein Objekt, eine Auflistung von Objekten oder ein Programm angezeigt und geändert werden?** Verwenden Sie in diesem Falle stattdessen ein [Eigenschaftenfenster](win-property-win.md) oder eine [Symbolleiste.](cmd-toolbars.md)
-   **Soll eine Sammlung von Befehlen oder Tools präsentiert werden?** Verwenden Sie in diesem Falle eine Symbolleiste oder ein [Palettenfenster.](glossary.md)
-   **Soll überprüft werden, ob der Benutzer mit einer Aktion fortfahren möchte?** Gibt es einen eindeutigen Grund, nicht fortzufahren, und eine angemessene Wahrscheinlichkeit, dass Benutzer dies manchmal nicht tun? Verwenden Sie in diesem Falle eine [Bestätigung.](mess-confirm.md)
-   **Soll ein Fehler oder eine Warnmeldung ausgegeben werden?** Verwenden Sie in diesem Falle eine [Fehlermeldung](mess-error.md) oder [eine Warnmeldung.](mess-warn.md)
-   Der Zweck ist Folgendes:
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
-   **Soll ein nicht kritisches Benutzereingabeproblem oder eine besondere Bedingung angezeigt werden?** Verwenden Sie in diesem Falle stattdessen eine [Sprechblase.](ctrl-balloons.md)
-   **Wäre es für Aufgabenflows besser, eine andere Seite zu verwenden?** Im Allgemeinen möchten Sie, dass eine Aufgabe innerhalb eines einzelnen Fensters von Seite zu Seite fließt. Verwenden Sie Dialogfelder, um direkt ausgeführte Befehle zu bestätigen, Eingaben für direkt ausgeführte Befehle abzurufen und sekundäre, eigenständige Aufgaben auszuführen, die am besten unabhängig und außerhalb des Haupttaskflows ausgeführt werden.
-   **Ändern Benutzer die Optionen wahrscheinlich für die Auswahl von Optionen?** Falls nicht, sollten Sie Alternativen in Betracht ziehen, z. B.:
    -   Verwenden sie die Standardoptionen, ohne die Benutzer zu fragen, aber später Änderungen vornehmen zu können.
    -   Bereitstellen einer Version mit Optionen **(z. B. Drucken...** in einem Menü) sowie einer Version ohne Optionen (z. B. **Drucken** in der Symbolleiste). Im Allgemeinen sollten Symbolleistenbefehle sofort sein und das Anzeigen von Dialogfeldern vermeiden.
-   **Gibt es für die Auswahl von Optionen eine einfachere, direktere Möglichkeit, die Optionen darzustellen?** Ziehen Sie in diesem Falle Alternativen in Betracht, z. B.:
    -   Verwenden einer [unterteilten Schaltfläche](ctrl-command-buttons.md) zum Auswählen von Variationen eines Befehls.
    -   Verwenden eines Untermenüs für Befehle, Kontrollkästchen, Optionsfelder und einfache Listen.

![Screenshot: Menü und Untermenü](images/win-dialog-box-image4.png)

![Screenshot eines Menüs und eines Untermenüs ](images/win-dialog-box-image5.png)

In diesen Beispielen werden Untermenüs anstelle von Dialogfeldern für einfache Auswahl verwendet.

## <a name="design-concepts"></a>Entwurfskonzepte

Bei ordnungsgemäßer Verwendung sind Dialogfelder eine hervorragende Möglichkeit, Ihrem Programm Energie und Flexibilität zu geben. Wenn sie missbraucht werden, sind Dialogfelder eine einfache Möglichkeit, Benutzer zu verärgern, ihren Flow zu unterbrechen und das Programm indirekt und mühsam zu verwenden. **Modale Dialogfelder erfordern die Aufmerksamkeit der Benutzer.** Dialogfelder lassen sich häufig einfacher implementieren als alternative Benutzeroberflächen, sodass sie tendenziell überladen sind.

**Ein Dialogfeld ist am effektivsten, wenn seine Entwurfsmerkmale der Verwendung entsprechen.** Der Entwurf eines Dialogfelds wird größtenteils durch seinen Zweck bestimmt (zum Anbieten von Optionen, Stellen von Fragen, Bereitstellen von Informationen oder Feedback), Typ (modal oder moduslos) und Benutzerinteraktion (erforderlich, optionale Antwort oder Bestätigung), während seine Verwendung größtenteils durch den Kontext (benutzer- oder programminitiiert), die Wahrscheinlichkeit von Benutzeraktionen und die Häufigkeit der Anzeige bestimmt wird.

Um effektive Dialogfelder zu entwerfen, verwenden Sie die folgenden Elemente effektiv:

-   Text im Dialogfeld
-   Hauptanweisungen
-   Zeigen Sie dies nicht an. <item> Option "again"

**Wenn Sie nur eine Sache tun...**

Stellen Sie sicher, dass der Entwurf des Dialogfelds (bestimmt durch Zweck, Typ und Benutzerinteraktion) mit seiner Verwendung übereinstimmt (bestimmt durch den Kontext, die Wahrscheinlichkeit der Benutzeraktion und die Häufigkeit der Anzeige).

## <a name="usage-patterns"></a>Verwendungsmuster

Dialogfelder weisen mehrere Verwendungsmuster auf:

-   Fragedialoge (mitHilfe von Schaltflächen) stellen Benutzern eine einzelne Frage oder zum Bestätigen eines Befehls und verwenden einfache Antworten in horizontal angeordneten Befehlsschaltflächen.
-   Fragedialoge (mithilfe von Befehlslinks) stellen Benutzern eine einzelne Frage, oder um eine auszuführende Aufgabe auszuwählen und ausführliche Antworten in vertikal angeordneten Befehlslinks zu verwenden.
-   Auswahldialogfelder stellen Benutzern eine Reihe von Optionen zur Verfügung, in der Regel, um einen Befehl vollständiger anzugeben. Im Gegensatz zu Fragedialogen können Auswahldialoge mehrere Fragen stellen.
-   Statusdialoge zeigen Benutzern während eines längeren Vorgangs (länger als fünf Sekunden) ein Statusfeedback sowie einen Befehl zum Abbrechen oder Beenden des Vorgangs an.
-   Informationsdialogfelder zeigen vom Benutzer angeforderte Informationen an.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Verwenden Sie keine bildlauffähigen Dialogfelder.** Verwenden Sie keine Dialogfelder, für die die Verwendung einer Bildlaufleiste während der normalen Nutzung vollständig angezeigt werden muss. Gestalten Sie stattdessen das Dialogfeld neu. Erwägen Sie die Verwendung von [progressiver Offenlegung](ctrl-progressive-disclosure-controls.md) oder [Registerkarten](ctrl-tabs.md).
-   **Sie verfügen nicht über eine Menüleiste oder Statusleiste.** Stellen Sie stattdessen direkt im Dialogfeld selbst oder mithilfe von Kontextmenüs für die relevanten Steuerelemente Zugriff auf Befehle und den Status bereit.

    -   **Ausnahme:** Menüleisten sind akzeptabel, wenn ein Dialogfeld verwendet wird, um ein primäres Fenster (z. B. ein Hilfsprogramm) zu implementieren.

    **Falsch:**

    ![Screenshot eines Dialogfelds mit einer Menüleiste ](images/win-dialog-box-image6.png)

    In diesem Beispiel ist Zertifikate suchen ein modusloses Dialogfeld mit einer Menüleiste.

-   Wenn ein Dialogfeld sofortige Aufmerksamkeit erfordert und das Programm nicht aktiv ist, blinken Sie **die Taskleistenschaltfläche dreimal, um die Aufmerksamkeit zu lenken, und lassen Sie es hervorgehoben.** Machen Sie nichts anderes: Stellen Sie das Fenster nicht wieder her, oder aktivieren Sie es nicht, und geben Sie keine Soundeffekte wieder. Berücksichtigen Sie stattdessen die Fensterzustandsauswahl des Benutzers, und lassen Sie den Benutzer das Fenster aktivieren, wenn er bereit ist.
-   Weitere Richtlinien und Beispiele finden Sie unter [Taskleiste](winenv-taskbar.md).

### <a name="modal-dialog-boxes"></a>Modale Dialogfelder

-   **Verwenden Sie für kritische oder seltene, einmalige Aufgaben, die abgeschlossen werden müssen, bevor Sie fortfahren.**
-   Verwenden Sie ein [verzögertes Commitmodell,](glossary.md) damit Änderungen erst wirksam werden, wenn ein expliziter Commit ausgeführt wurde.
-   **Implementieren Sie nach Bedarf mithilfe eines Aufgabendialogfelds, um ein konsistentes Aussehen zu erzielen.** Aufgabendialogfelder erfordern Windows Vista oder höher, sodass sie nicht für frühere Versionen von Windows geeignet sind.

### <a name="modeless-dialog-boxes"></a>Dialogfelder ohne Modus

-   **Verwenden Sie für häufige, sich wiederholende, laufende Aufgaben.**
-   Verwenden Sie ein Modell mit [sofortigem Commit,](glossary.md) damit Änderungen sofort wirksam werden.
-   Verwenden Sie für dialoglose Dialoge eine explizite Befehlsschaltfläche Schließen im Dialogfeld, um das Fenster zu schließen. Verwenden Sie für beide die Schaltfläche Schließen auf der Titelleiste, um das Fenster zu schließen.
-   **Erwägen Sie, moduslose Dialogfelder andockbar zu machen.** Andockbare dialoglose Dialoge ermöglichen eine flexiblere Platzierung.

![Screenshot eines andockbaren, moduslosen Dialogfelds ](images/win-dialog-box-image7.png)

Einige in Microsoft Office verwendete dialogfelder ohne Modus können andockbar sein.

### <a name="multiple-dialog-boxes"></a>Mehrere Dialogfelder

-   **Zeigen Sie in einem Dialogfeld für die Auswahl des Besitzers nicht mehr als ein Dialogfeld für die Auswahl im Besitz gleichzeitig an.** Das Anzeigen mehrerer Schaltflächen erschwert es Benutzern, die Bedeutung der Commitschaltflächen zu verstehen. Sie können bei Bedarf andere Arten von Dialogfeldern (z. B. Fragedialoge) anzeigen.
-   **Für eine Sequenz verwandter Dialoge sollten Sie nach Möglichkeit einen mehrseitigen Dialog verwenden.** Verwenden Sie einzelne Dialoge, wenn sie nicht eindeutig verknüpft sind.

### <a name="multi-page-dialog-boxes"></a>Dialogfelder mit mehreren Seiten

-   Verwenden Sie ein mehrseitiges Dialogfeld anstelle einzelner Dialogfelder, wenn Sie über die folgende Sequenz verwandter Seiten verfügen:
    -   Eine einzelne Eingabeseite (optional)
    -   Eine Statusseite
    -   Eine einzelne Ergebnisseite

Die Eingabeseite ist optional, da die Aufgabe möglicherweise an einer anderen Stelle initiiert wurde. **Dadurch erhält die resultierende Erfahrung ein stabiles, einfaches, einfaches Gefühl.**

![Screenshot einer Statusanzeige ](images/win-dialog-box-image8.png)

![Screenshot der Meldung "Keine Probleme gefunden" ](images/win-dialog-box-image9.png)

In diesem Beispiel besteht die Windows-Netzwerkdiagnose aus Status- und Ergebnisseiten.

-   **Verwenden Sie kein mehrseitiges Dialogfeld, wenn es sich bei der Eingabeseite um ein Standarddialogfeld handelt.** In diesem Fall ist die Konsistenz der Verwendung eines Standarddialogs wichtiger.
-   **Verwenden Sie keine Schaltflächen Weiter oder Zurück, und haben Sie nicht mehr als drei Seiten.** Mehrseitige Dialogfelder sind für Einzelschrittaufgaben mit Feedback vorgesehen. Sie sind keine [Assistenten,](win-wizards.md)die für mehrstufige Aufgaben verwendet werden. Assistenten haben im Vergleich zu Dialogfeldern mit mehreren Seiten eine starke, indirekte Haptik.
-   **Verwenden Sie auf der Eingabeseite bestimmte Befehlsschaltflächen oder Befehlslinks, um die Aufgabe zu initiieren.**
-   **Verwenden Sie auf den Eingabe- und Statusseiten die Schaltfläche Abbrechen und auf der Ergebnisseite die Schaltfläche Schließen.**

**Entwickler:** Sie können Dialogfelder für mehrseitige Aufgaben mithilfe der [TDM \_ NAVIGATE \_ PAGE-Meldung](../controls/tdm-navigate-page.md) erstellen.

### <a name="presentation"></a>Präsentation

Damit Dialogfelder leicht zu finden und darauf zugreifen können, ordnen Sie den Dialog eindeutig der Quelle zu und funktionieren gut mit mehreren Monitoren:

-   **Anfänglich werden Dialoge "zentriert" über dem Besitzerfenster angezeigt.** Erwägen Sie für die nachfolgende Anzeige die Anzeige am letzten Speicherort (relativ zum Besitzerfenster), wenn dies wahrscheinlich bequemer ist.

![Diagramm des Dialogfelds, das auf dem Fenster im Hintergrund zentriert ist ](images/win-dialog-box-image10.png)

Anfangs zentren Dialoge über dem Besitzerfenster.

-   **Wenn ein Dialogfeld kontextabhängig ist, zeigen Sie es in der Nähe des Objekts an, von dem aus es gestartet wurde.** Platzieren Sie es jedoch außerhalb des Wegs (vorzugsweise nach unten und nach rechts), sodass das Objekt nicht durch den Dialog abgedeckt wird.

![Diagramm des Offsets des Dialogfelds nach unten und rechts ](images/win-dialog-box-image11.png)

Die Eigenschaften eines Objekts werden in der Nähe des -Objekts angezeigt.

-   **Zeigen Sie für dialoglose Dialoge zunächst über dem Besitzerfenster an, um die Suche zu vereinfachen.** Wenn der Benutzer das Besitzerfenster aktiviert, kann dies den moduslosen Dialog verdecken.
-   **Passen Sie bei Bedarf die ursprüngliche Position so an, dass der gesamte Dialog innerhalb des Zielmonitors angezeigt wird.** Wenn ein Fenster mit größenveränderbarer Größe größer als der Zielmonitor ist, reduzieren Sie es, damit es passt.
-   **Wenn ein Dialogfeld erneut angezeigt wird, sollten Sie erwägen, es im selben Zustand wie der zuletzt aufgerufene anzuzeigen.** Speichern Sie beim Schließen den verwendeten Monitor, die Fenstergröße, den Speicherort und den Zustand (maximiert im Vergleich zur Wiederherstellung). Stellen Sie bei der erneuten Anzeige die gespeicherte Dialoggröße, den Speicherort und den Status mithilfe des entsprechenden Monitors wieder her. Erwägen Sie außerdem, diese Attribute auf Programminstanzen pro Benutzer dauerhaft zu speichern.
-   **Legen Sie für Fenster mit größenveränderlicher Größe eine minimale Fenstergröße fest, wenn eine Größe vorhanden ist, unter der der Inhalt nicht mehr verwendet werden kann.** Erwägen Sie, die Präsentation zu ändern, damit der Inhalt in kleineren Größen verwendet werden kann.

![Screenshot der zentrierten Media Player-Schaltflächen ](images/win-dialog-box-image12.png)

In diesem Beispiel ändert Windows Media Player sein Format, wenn das Fenster für das Standardformat zu klein wird.

-   **Verwenden Sie nicht das Always On Top-Attribut.**
    -   **Ausnahme:** Verwenden Sie nur, wenn ein Dialogfeld einen im Wesentlichen modalen Vorgang implementiert, aber kurz angehalten werden muss, um auf das Besitzerfenster zuzugreifen. Beispielsweise können Benutzer bei der Rechtschreibprüfung eines Dokuments gelegentlich das Rechtschreibprüfungsdialogfeld verlassen und auf das Dokument zugreifen, um Fehler zu beheben.

Weitere Informationen und Beispiele finden Sie unter [Fensterverwaltung.](win-window-mgt.md)

### <a name="title-bars"></a>Titelleisten

-   **Dialogfelder verfügen nicht über Titelleistensymbole.** Titelleistensymbole werden als visueller Unterschied zwischen [primären und](glossary.md) [sekundären Fenstern](glossary.md)verwendet.
    -   **Ausnahme:** Wenn ein Dialogfeld zum Implementieren eines primären Fensters (z. B. eines Hilfsprogramms) verwendet wird und daher auf der Taskleiste angezeigt wird, verfügt es über ein Titelleistensymbol. Optimieren Sie in diesem Fall den Titel für die Anzeige auf der Taskleiste, indem Sie zuerst die Unterscheidungsinformationen präzise platzieren.
-   **Dialogfelder verfügen immer über die Schaltfläche Schließen.** Dialogfelder ohne Modus können auch über die Schaltfläche Minimieren verfügen. Veränderbare Dialoge können über die Schaltfläche Maximieren verfügen.
-   **Deaktivieren Sie nicht die Schaltfläche Schließen.** Die Schaltfläche Schließen hilft Benutzern, die Kontrolle zu behalten, da sie Fenster schließen können, die sie nicht wünschen.
    -   **Ausnahme:** Für Statusdialogfelder können Sie die Schaltfläche Schließen deaktivieren, wenn der Task bis zum Abschluss ausgeführt werden muss, um einen gültigen Zustand zu erreichen oder Datenverluste zu verhindern.
-   **Die Schaltfläche Schließen auf der Titelleiste sollte die gleiche Auswirkung wie die Schaltfläche Abbrechen oder Schließen** im Dialogfeld haben. Geben Sie ihm niemals den gleichen Effekt wie OK.
-   Wenn die Titelleistenbeschriftung und das Symbol am oberen Rand des Fensters bereits hervorgehoben angezeigt werden, können Sie die Titelleistenbeschriftung und das Symbol ausblenden, um Redundanz zu vermeiden. Sie müssen jedoch intern einen geeigneten Titel für die Verwendung durch Windows festlegen.

### <a name="interaction"></a>Interaktion

-   **Wenn sie angezeigt werden, sollten vom Benutzer initiierte Dialogfelder immer den Eingabefokus übernehmen.** Vom Programm initiierte Dialogfelder sollten den Eingabefokus nicht übernehmen, da der Benutzer möglicherweise mit einem anderen Fenster interagiert. Eine solche Interaktion, die im Dialogfeld fehlgeleitet wird, kann unbeabsichtigte Folgen haben.
-   **Weisen Sie dem Steuerelement den anfänglichen Eingabefokus zu,** mit dem Benutzer höchstwahrscheinlich mit dem ersten interagieren. Dies ist normalerweise (aber nicht immer) das erste interaktive Steuerelement. Vermeiden Sie es, einem Hilfelink den anfänglichen Eingabefokus zuzuweisen.
-   **Für die Tastaturnavigation sollte die Tabstoppreihenfolge in einer logischen Reihenfolge ablaufen, in der Regel von links nach rechts, von oben nach unten.** In der Regel folgt die Tabstoppreihenfolge der Lesereihenfolge, aber erwägen Sie, diese Ausnahmen zu treffen:

    -   Ordnen Sie die am häufigsten verwendeten Steuerelemente weiter oben in der Tabstoppreihenfolge an.
    -   Setzen Sie Hilfelinks am unteren Rand eines Dialogfelds nach den Commitschaltflächen in tabellarischer Reihenfolge.

    Gehen Sie beim Zuweisen der Reihenfolge davon aus, dass Benutzer Dialogfelder für ihren beabsichtigten Zweck anzeigen. Benutzer zeigen z. B. Auswahldialogfelder an, um Entscheidungen zu treffen, nicht, um sie zu überprüfen und auf Abbrechen zu klicken.

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
    -   Steuerelemente ohne **Bezeichnung,** z. B. Drehsteuerelemente, Schaltflächen für grafische Befehle und steuerelemente für die progressive Offenlegung ohne Bezeichnung.
    -   **Statischer Text ohne Bezeichnung oder Bezeichnungen für Steuerelemente, die nicht interaktiv sind,** z. B. Statusleisten.

-   Weisen Sie nach **Möglichkeit Zugriffsschlüssel für häufig verwendete Befehle gemäß den Standardzugriffsschlüsselzuweisungen zu.** Konsistente Zuweisungen von Zugriffsschlüsseln sind zwar nicht immer möglich, werden jedoch insbesondere für häufig verwendete Dialogfelder bevorzugt.
-   **Weisen Sie zunächst Zugriffsschlüssel für commit-Schaltflächen zu, um sicherzustellen, dass sie über die Standardschlüsselzuweisungen verfügen.** Wenn keine Standardschlüsselzuweisung vorhanden ist, verwenden Sie den ersten Buchstaben des ersten Worts. Beispielsweise sollte der Zugriffsschlüssel für die Schaltflächen Ja und Kein Commit immer "Y" und "N" sein, unabhängig von den anderen Steuerelementen im Dialogfeld.
-   **Um die Suche nach Zugriffsschlüsseln zu vereinfachen, weisen Sie die Zugriffsschlüssel einem Zeichen zu, das früh in der Bezeichnung angezeigt wird,** idealerweise dem ersten Zeichen, auch wenn es ein Schlüsselwort gibt, das später in der Bezeichnung angezeigt wird.
-   **Bevorzugen Sie Zeichen mit breiter Breite,** z. B. w, m und Großbuchstaben.
-   **Bevorzugen Sie einen typischen Konsonanten oder einen Vokal,** z. B. "x" in Exit.
-   **Vermeiden Sie die Verwendung von Zeichen, die die Unterstreichung schwierig zu erkennen machen,** z. B. (von den problematischsten bis zu den am wenigsten problematischen):
    -   Buchstaben, die nur ein Pixel breit sind, z. B. i und l.
    -   Buchstaben mit Nachfolgern wie g, j, p, q und y.
    -   Buchstaben neben einem Buchstaben mit einem Nachfolger.

Weitere Richtlinien und Beispiele finden Sie unter [Tastatur.](inter-keyboard.md)

### <a name="progress-dialogs"></a>Statusdialoge

Gehen Sie bei Aufgaben mit langer Ausführungslaufzeit **davon aus, dass Benutzer etwas anderes tun, während die Aufgabe abgeschlossen ist.** Entwerfen Sie die Aufgabe so, dass sie unbeaufsichtigt ausgeführt wird.

-   Zeigen Sie Benutzern das **Dialogfeld "Statusfeedback" an, wenn der Abschluss eines Vorgangs länger als fünf Sekunden dauert,** zusammen mit einem Befehl zum Abbrechen oder Beenden des Vorgangs.
    -   **Ausnahme:** Verwenden Sie für Assistenten und Aufgabenflows nur dann ein modales Dialogfeld für den Fortschritt, wenn der Task auf derselben Seite verbleibt (anstatt zu einer anderen Seite zu wechseln), und Benutzer während des Wartens nichts tun können. Verwenden Sie andernfalls eine Statusseite oder einen statusbasierten Status.
-   Wenn es sich bei dem Vorgang um eine Aufgabe mit langer Ausführung (mehr als 30 Sekunden) handelt und im Hintergrund ausgeführt werden kann, verwenden Sie ein statusloses Dialogfeld, damit Benutzer Das Programm während des Wartens weiterhin verwenden können.
-   Statusdialogfelder ohne Modus:
    -   Klicken Sie auf der Titelleiste auf die Schaltfläche Minimieren.
    -   Werden auf der Taskleiste angezeigt.
-   Implementieren Sie statuslose Statusdialogfelder, sodass sie auch dann weiterhin ausgeführt werden, wenn das Besitzerfenster geschlossen ist.

![Screenshot des Kopierdialogfelds mit Statusanzeige ](images/win-dialog-box-image14.png)

In diesem Beispiel wird der Dateikopiervorgang auch dann fortgesetzt, wenn das Besitzerfenster geschlossen ist.

-   **Geben Sie eine Befehlsschaltfläche an, um den Vorgang anzuhalten, wenn der Vorgang mehr als ein paar Sekunden dauert oder möglicherweise nie abgeschlossen werden kann.** Beschriften Sie die Schaltfläche Abbrechen, wenn beim Abbrechen die Umgebung in den vorherigen Zustand zurückgesetzt wird (ohne Nebeneffekte). Beschriften Sie andernfalls die Schaltfläche Beenden, um anzugeben, dass der teilweise abgeschlossene Vorgang intakt bleibt. Sie können die Schaltflächenbezeichnung in der Mitte des Vorgangs von Abbrechen in Beenden ändern, wenn es zu einem bestimmten Zeitpunkt nicht möglich ist, die Umgebung in den vorherigen Zustand zurückzuversetzen.

![Screenshot des Dialogfelds mit der Schaltfläche "Abbrechen" ](images/win-dialog-box-image15.png)

In diesem Beispiel hat das Anhalten der Problemdiagnose keine Nebeneffekte.

-   **Geben Sie eine Befehlsschaltfläche an, um den Vorgang anzuhalten, wenn der Vorgang mehr als mehrere Minuten dauert und die Benutzer nicht mehr in der Lage sind, ihre Arbeit zu erledigen.** Dies zwingt den Benutzer nicht, zwischen dem Abschließen der Aufgabe und dem Erledigen seiner Arbeit zu wählen.
-   **Sammeln Sie so viele Informationen wie sie können, bevor Sie die Aufgabe starten.**
-   **Wenn wiederherstellbare Probleme erkannt werden, lassen Sie benutzer alle Probleme behandeln, die am Ende der Aufgabe gefunden wurden.** Wenn dies nicht praktikabel ist, sollten Benutzer probleme behandeln, sobald sie auftreten.
-   **Verwerfen Sie Tasks nicht als Ergebnis wiederherstellbarer Fehler.**

![Screenshot des Dialogfelds mit der Schaltfläche "Erneut versuchen" ](images/win-dialog-box-image16.png)

In diesem Beispiel ermöglicht Windows-Explorer Benutzern, die Aufgabe nach einem wiederherstellbaren Fehler fortzusetzen.

-   **Zeigen Sie Probleme an, indem Sie die Statusanzeige rot drehen.**

![Screenshot der Statusanzeige und schaltfläche "Erneut versuchen" ](images/win-dialog-box-image17.png)

In diesem Beispiel wurde ein Wechseldatenträger während eines Dateikopiervorgang entfernt.

-   **Wenn die Ergebnisse für Benutzer deutlich erkennbar sind, schließen Sie das Statusdialogfeld automatisch nach erfolgreichem Abschluss.** Verwenden Sie andernfalls Nur Feedback, um Probleme zu melden:
    -   Um einfaches Feedback anzuzeigen, zeigen Sie das Feedback im Statusdialogfeld an, und ändern Sie die Schaltfläche Abbrechen in Schließen.
    -   Um ausführliches Feedback anzuzeigen, schließen Sie das Statusdialogfeld, und zeigen Sie ein Informationsdialogfeld an.

**Verwenden Sie keine Benachrichtigung für Das Feedback zur Vervollständigung.** Verwenden Sie entweder ein Statusdialogfeld oder eine [Aktionserfolgsbenachrichtigung,](mess-notif.md)aber nicht beides.

**Verbleibende Zeit**

-   **Verwenden Sie die folgenden Zeitformate.** Beginnen Sie mit dem ersten der folgenden Formate, bei dem die größte Zeiteinheit nicht 0 (null) ist, und wechseln Sie dann in das nächste Format, sobald die größte Zeiteinheit 0 (null) wird.

**Für Statusleisten:**

**Wenn verwandte Informationen in einem Doppelpunktformat angezeigt werden:**

Verbleibende Zeit: h Stunden, m Minuten

Verbleibende Zeit: m Minuten, s Sekunden

Verbleibende Zeit: s Sekunden

**Wenn der Bildschirmbereich premium ist:**

h hrs, m mins remaining

m mins, s secs remaining

Verbleibende Sekunden

**Andernfalls:**

h Stunden, verbleibende m Minuten

m Minuten, verbleibende Sekunden

Verbleibende Sekunden

**Für Titelleisten:**

hh:mm remaining

mm:ss verbleibende

Verbleibende 0:ss

In diesem kompakten Format werden zuerst die wichtigsten Informationen angezeigt, damit sie nicht auf der Taskleiste abgeschnitten werden.

-   **Machen Sie Schätzungen präzise, aber geben Sie keine falsche Genauigkeit.** Wenn die größte Einheit Stunden ist, geben Sie Minuten an (sofern sinnvoll), aber keine Sekunden.

**Falsch:**

hh hours, mm minutes, ss seconds

-   **Halten Sie die Schätzung auf dem neuesten Stand.** Die verbleibende Aktualisierungszeit wird mindestens alle 5 Sekunden geschätzt.
-   **Konzentrieren Sie sich auf die verbleibende Zeit,** da dies die Informationen sind, die benutzern am wichtigsten sind. Geben Sie die gesamte verstrichene Zeit nur dann an, wenn es Szenarien gibt, in denen die verstrichene Zeit hilfreich ist (z. B. wenn die Aufgabe wahrscheinlich wiederholt wird). Wenn die verbleibende Schätzung einer Statusleiste zugeordnet ist, sollten Sie keinen vollständigen Prozenttext haben, da diese Informationen von der Statusleiste selbst übermittelt werden.
-   **Grammatikalisch korrekt sein.** Verwenden Sie Singulareinheiten, wenn die Zahl eins ist.

**Falsch:**

1 Minuten, 1 Sekunde

-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**

Weitere Informationen und Beispiele finden Sie unter [Statusleisten.](progress-bars.md)

### <a name="icons-and-graphics"></a>Symbole und Grafiken

**Grafiken**

-   **Verwenden Sie keine großen Grafiken, die keinen Zweck erfüllen, außer den Platz mit Augenbrillen zu füllen.** Halten Sie stattdessen die Darstellung einfach.

**Falsch:**

![Screenshot des Dialogfelds mit einer großen Grafik ](images/win-dialog-box-image18.png)

In diesem Beispiel hat die große Grafik keinen Zweck.

**Titelleistensymbole**

-   **Dialogfelder verfügen nicht über Titelleistensymbole.**
    -   **Ausnahme:** Wenn ein Dialogfeld zum Implementieren eines primären Fensters (z. B. eines Hilfsprogramms) verwendet wird und daher auf der Taskleiste angezeigt wird, verfügt es über ein Titelleistensymbol.

**Textsymbole**

-   **Wählen Sie das Textsymbol basierend auf dem Entwurfsmuster aus:**



| Muster | Textsymbol |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| **Fragedialogfelder**<br/>      | Programm, Feature, Objekt, Warnsymbol (bei potenziellem Verlust des Daten- oder Systemzugriffs), Sicherheitswarnung oder keine.<br/> |
| **Auswahldialogfelder**<br/>        | Keine.<br/>                                                                                                           |
| **Statusdialogfelder**<br/>      | Keine (kann aber eine Animation haben).<br/>                                                                               |
| **Informationsdialoge**<br/> | Keine.<br/>                                                                                                           |



 

-   **Falsch:**

![Screenshot des Dialogfelds mit Warnsymbol ](images/win-dialog-box-image19.png)

In diesem Beispiel wird ein Warnsymbol fälschlicherweise für eine Frage verwendet, die keinen potenziellen Verlust des Daten- oder Systemzugriffs beinhaltet.

- **Erwägen Sie die Verwendung von Symbolen, um Benutzern zu helfen, die Features Ihres Programms visuell zu erkennen.** Diese Technik ist am effektivsten, wenn die Symbole leicht erkennbar sind und an mehreren Stellen in Ihrem Programm verwendet werden können.

![Screenshot des Dialogfelds "Favoriten" mit Sternsymbol ](images/win-dialog-box-image20.png)

In diesem Beispiel stellt das gelbe Sternsymbol Favoriten dar. Das Symbol ist leicht zu erkennen und wird durchgängig in Windows verwendet, um Favoriten zu darstellen.

-   **Verwenden Sie Symbole, damit Benutzer das objekt erkennen können.**

![Screenshot des Dialogfelds mit PowerPoint-Symbol ](images/win-dialog-box-image21.png)

In diesem Beispiel hilft das Symbol des Objekts Benutzern, den Typ der Datei zu erkennen, die geöffnet oder gespeichert wird.

-   **Erwägen Sie die Verwendung von Symbolen, um Features selbsterklärend zu machen.**

![Bilder von Pfeilen, die zeigen, wie der Monitor positioniert wird ](images/win-dialog-box-image22.png)

In diesem Beispiel helfen diese Symbole Benutzern, die Auswirkungen ihrer Features zu visualisieren.

-   **Verwenden Sie ein Symbol in den Dialogfeldern "About Box" (Informationen zu Box) für das Anwendungsbranding.**

![Screenshot des Dialogfelds "About" mit Windows-Logo ](images/win-dialog-box-image23.png)

In diesem Beispiel wird eine Bitmap in der About Box verwendet, um die Anwendung zu identifizieren und als Marke zu verwenden.

**Fußnotensymbole**

-   **Wenn Sie eine Fußnote haben, sollten Sie ein Fußnotesymbol verwenden, um das Thema der Fußnote zusammenzufassen.**

![Screenshot des Dialogfelds mit Fußnotesymbol ](images/win-dialog-box-image24.png)

In diesem Beispiel gibt das Fußnotesymbol an, dass die Frage Auswirkungen auf die Sicherheit hat.

-   **Verwenden Sie kein Fußnotesymbol, das das Textsymbol wiederholt.**
-   **Verwenden Sie nicht die Standardsymbole für Fehler oder Informationen.** Fehlerbedingungen müssen über das Textsymbol vermittelt werden, und Fußnotes sind immer für Informationen, wodurch das Informationssymbol redundant wird. Sie können jedoch das Standardwarnungssymbol und den gelben Sicherheitsschutz verwenden, um Benutzer vor riskanten Konsequenzen zu warnen.

Weitere Informationen und Beispiele finden Sie unter [Symbole](vis-icons.md).

### <a name="commit-buttons"></a>Commitschaltflächen

**Hinweise:**

-   Diese Richtlinien gelten nicht für Fragedialoge, die Befehlslinks verwenden, da dieses Muster Befehlslinks anstelle von Schaltflächen verwendet.
-   \[Tun Sie dies, und Tun Sie dies nicht, sind positive bzw. negative Antworten auf \] \[ die \] main-Anweisung.

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
    <td><strong>Fragedialogfelder (mithilfe von Schaltflächen)</strong><br/></td>
    <td>Einer der folgenden präzisen Befehle: Ja/Nein, Ja/Nein/Abbrechen, [Do it]/Cancel, [Do it]/[Don't do it], [Do it]/[Don't do it]/Cancel.<br/></td>
    </tr>
    <tr class="odd">
    <td><strong>Fragedialoge (über Links)</strong><br/></td>
    <td>Abbrechen<br/></td>
    </tr>
    <tr class="even">
    <td><strong>Auswahldialogfelder</strong><br/></td>
    <td><ul>
    <li>Modale Dialogfelder: OK/Abbrechen oder [Do it]/Cancel</li>
    <li>Moduslose Dialogfelder: Schaltfläche "Schließen" im Dialogfeld und in der Titelleiste</li>
    <li>Aufgabenbereich: Schaltfläche "Schließen" auf der Titelleiste</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><strong>Statusdialogfelder</strong><br/></td>
    <td>Verwenden Sie Abbrechen, wenn die Umgebung in ihren vorherigen Zustand zurückgibt (ohne Nebeneffekt). Verwenden Sie andernfalls Beenden.<br/></td>
    </tr>
    <tr class="even">
    <td><strong>Informationsdialoge</strong><br/></td>
    <td>Fast richtig.<br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   **Alle Commitschaltflächen mit Ausnahme von Anwenden führen dazu, dass das Dialogfeld geschlossen wird.**
-   **Bestätigen Sie keine Commitschaltflächen.** Dies kann unnötigerweise sehr lästig sein. **Ausnahmen:**

    -   Die Aktion ist potenziell schwerwiegender.
    -   Die Aktion ist eindeutig inkonsistent mit anderen Aktionen.
    -   Wenn die Aktion falsch ist, kann dies zu einem erheblichen Verlust von Daten, Zeit oder Aufwand im Auftrag des Benutzers führen.

    Weitere Richtlinien und Beispiele finden Sie unter [Bestätigungen.](mess-confirm.md)

-   **Deaktivieren Sie keine Commitschaltflächen. Ausnahmen:**
    -   **Wenn Benutzer eine Erhöhte Rechte erhöhen müssen, um eine Änderung zu ändern, deaktivieren Sie die Schaltflächen für positive Commits, bis der Benutzer eine Änderung vorn hat.** Dadurch wird verhindert, dass Benutzer eine Erhöhung nur zum Schließen eines Fensters erzwingen, indem sie auf Abbrechenklicken.
    -   Weitere Ausnahmen finden Sie unter [Deaktivieren oder Entfernen von Steuerelementen im Vergleich zur Angabe von Fehlermeldungen.](#disabling-or-removing-controls-vs-giving-error-messages)
-   **Richten Sie commit-Schaltflächen in einer einzelnen Zeile** am unteren Rand des Dialogfelds aus, aber über dem Fußnotenbereich. Dies gilt auch, wenn eine einzelne Commitschaltfläche (z. B. OK) angezeigt wird.

    **Falsch:**

    ![Screenshot der Nachricht mit zentrierter SCHALTFLÄCHE "OK" ](images/win-dialog-box-image25.png)

    In diesem Beispiel ist die Schaltfläche OK falsch zentriert.

-   **Stellen Sie die Commitschaltflächen in der folgenden Reihenfolge vor:**
    1.  OK/ \[ Do it \] /Yes
    2.  \[Don't do it \] /No
    3.  Abbrechen
    4.  Anwenden (falls vorhanden)
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
-   **Ordnen Sie generische Bezeichnungen nicht ihrer spezifischen Bedeutung mit Text im Inhaltsbereich zu.** Verwenden Sie stattdessen bestimmte Bezeichnungen für Commitschaltfläche oder ein Fragedialogfeld mit Links, wenn die Bezeichnungen lang sind.

    **Falsch:**

    ![Screenshot der Nachricht mit unklarer Verwendung von Schaltflächen ](images/win-dialog-box-image28.png)

    In diesem Beispiel wird OK Continue zugeordnet, Abbrechen wird Auf Seite verbleiben zugeordnet.

**Schaltflächen "Ja" und "Nein"**

-   **Bevorzugen Sie bestimmte Antworten auf die Schaltflächen Ja und Nein.** Auch wenn die Verwendung von Ja und Nein kein Fehler ist, können bestimmte Antworten schneller verstanden werden, was zu einer effizienten Entscheidungsfindung führt. Bestätigungen [verfügen jedoch in der](mess-confirm.md) Regel über die Schaltflächen Ja und Nein, damit Benutzer der Bestätigung vor der Antwort einige Gedanken machen können. [](mess-confirm.md)
-   **Verwenden Sie die Schaltflächen Ja und Nein nur, um auf Ja- oder Nein-Fragen zu antworten.** Die Hauptanweisung sollte auf natürliche Weise als Ja- oder Nein-Frage ausgedrückt werden. Verwenden Sie für Ja- oder Nein-Fragen niemals OK und Abbrechen.

    **Falsch:**

    ![Screenshot, der eine Meldung mit einem "OK" für eine Ja-Nein-Frage zeigt.](images/win-dialog-box-image29.png)

    **Richtig:**

    ![Screenshot der Nachricht mit "Ja" für dieselbe Frage ](images/win-dialog-box-image30.png)

    **Besser:**

    ![Screenshot der Nachricht mit Ausführung für dieselbe Frage ](images/win-dialog-box-image31.png)

    In diesen Beispielen sind Ja und Nein gute Antworten auf Ja und keine Fragen, aber bestimmte Antworten sind noch besser.

-   **Ziehen Sie in Betracht, die Main-Anweisung als "Ja" oder "Keine Frage" zu formulieren, wenn commit-Schaltflächen mit bestimmten Formulierungen lang oder umgedreht sind.** Alternativ können Sie Befehlslinks für längere Antworten (fünf Wörter oder mehr) auf die main-Anweisung verwenden.

    **Falsch:**

    ![Screenshot der Nachricht mit wortigen Schaltflächenbezeichnungen ](images/win-dialog-box-image32.png)

    **Richtig:**

    ![Screenshot der Nachricht mit Schaltflächenbezeichnungen "Ja/Nein" ](images/win-dialog-box-image33.png)

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

-   **Wenn Sie auf Abbrechen klicken, werden alle Änderungen abgebrochen, die Aufgabe abgebrochen, das Fenster geschlossen und die Umgebung in den vorherigen Zustand zurückwechselt, ohne dass nebeneffekten.** Bei geschachtelten Auswahldialogfeldern bedeutet das Klicken auf Abbrechen im Dialogfeld für die Besitzerauswahl, dass alle Änderungen, die von Dialogfeldern für die Auswahl im Besitz des Besitzers vorgenommen wurden, ebenfalls verworfen werden.
-   **Geben Sie die Schaltfläche Abbrechen an, damit Benutzer Änderungen explizit abbrechen können.** Dialogfelder benötigen einen eindeutigen Ausgangspunkt. Verlassen Sie sich nicht darauf, dass Benutzer die Schaltfläche Schließen auf der Titelleiste finden.

    -   **Ausnahme:** Geben Sie keine Schaltfläche Abbrechen für Dialogfelder ohne Einstellungen an. Die Schaltflächen OK und Schließen haben in diesem Fall die gleichen Auswirkungen wie Abbrechen.

    **Falsch:**

    ![Screenshot der Meldung nur mit schaltfläche "OK" ](images/win-dialog-box-image35.png)

    In diesem Beispiel wird nur die Schaltfläche Schließen auf der Titelleiste angezeigt, als hätten Benutzer keine Auswahl.

-   **Verwenden Sie keine Schaltflächen Abbrechen, um auf Fragen zu antworten.**

    **Falsch:**

    ![Screenshot der Meldung mit "ok" für Ja-Nein-Frage ](images/win-dialog-box-image36.png)

    In diesem Beispiel werden OK und Abbrechen fälschlicherweise verwendet, um auf eine Ja- oder Nein-Frage zu antworten.

-   **Weisen Sie Cancel keine Zugriffsschlüssel zu, da ESC der Zugriffsschlüssel ist.** Auf diese Weise können die anderen Zugriffsschlüssel einfacher zugewiesen werden.
-   **Verwenden Sie in nicht moduslosen Dialogfeldern keine Schaltflächen Abbrechen.** Verwenden Sie stattdessen Close.
-   **Deaktivieren Sie nicht die Schaltfläche Abbrechen.** Benutzer sollten immer in der Lage sein, Dialogfelder abzubrechen.
    -   **Ausnahme:** Sie können die Schaltfläche Abbrechen in einem Statusdialogfeld deaktivieren, wenn es einen Zeitraum gibt, in dem der Vorgang nicht abgebrochen werden kann. Eine bessere Lösung besteht jedoch darin, solche Vorgänge so zu entwerfen, dass sie immer abgebrochen werden können.

**Schaltflächen schließen**

-   **Verwenden Sie Schaltflächen schließen für nicht moduslose Dialogfelder sowie modale Dialoge, die nicht abgebrochen werden können.**
-   **Wenn Sie auf Schließen klicken, wird das Dialogfeldfenster geschlossen, und vorhandene Nebeneffekte bleiben bestehen.** Verwenden Sie Done nicht, da es sich nicht um eine imperative Konstruktion handelt. Wenn Sie für geschachtelte Auswahldialogfelder im Dialogfeld "Besitzerauswahl" auf Schließen klicken, werden alle Änderungen beibehalten, die im Besitz von Auswahldialogfeldern vorgenommen werden.
-   **Legen Sie eine explizite Schaltfläche Schließen in den Text des Dialogfelds ein.** Dialogfelder benötigen einen eindeutigen Endpunkt. Verlassen Sie sich nicht darauf, dass Benutzer die Schaltfläche Schließen auf der Titelleiste finden.
-   **Stellen Sie sicher, dass die Schaltfläche Schließen auf der Titelleiste die gleiche Auswirkung wie Abbrechen oder Schließen hat.**
-   **Weisen Sie Close keine Zugriffsschlüssel zu, da es sich bei ESC um den Zugriffsschlüssel handelt.** Auf diese Weise können die anderen Zugriffsschlüssel einfacher zugewiesen werden.

**Schaltflächen anwenden**

-   **Verwenden Sie keine Schaltflächen anwenden in Dialogfeldern, die keine Eigenschaftenblätter oder Steuerelementpanels sind.** Die Schaltfläche Anwenden bedeutet, dass die ausstehenden Änderungen angewendet werden, aber lassen Sie das Fenster geöffnet. Auf diese Weise können Benutzer die Änderungen vor dem Schließen des Fensters auswerten. Dies ist jedoch nur für Eigenschaftenblatt und Steuerelementpanels erforderlich.

    **Falsch:**

    ![Screenshot des Dialogfelds mit der Schaltfläche "Anwenden" ](images/win-dialog-box-image37.png)

    In diesem Beispiel verfügt ein Auswahldialogfeld unnötigerweise über die Schaltfläche Übernehmen.

**Commitschaltflächen für indirekte Dialogfelder**

**Hinweis:** Indirekte Dialogfelder werden außerhalb des Kontexts angezeigt, entweder als indirektes Ergebnis einer Aufgabe oder als Ergebnis eines Problems mit einem System- oder Hintergrundprozess. Bei indirekten Dialogen ist die Schaltfläche Abbrechen mehrdeutig, da sie dazu führen kann, dass der Dialog abgebrochen oder die gesamte Aufgabe abgebrochen wird.

-   **Wenn Benutzer das Dialogfeld und die Aufgabe abbrechen müssen, geben Sie Commitschaltflächen an, um beides zu erledigen.** Bezeichnen Sie die Schaltfläche, die das Dialogfeld abbricht, mit einer negativen Antwort auf die Hauptanweisung. Bezeichnen Sie die Schaltfläche, die die gesamte Aufgabe abbricht, mit Abbrechen. Die Verwendung von Abbrechen ermöglicht die Verwendung des Dialogfelds in vielen Kontexten.

    **Richtig:**

    ![Screenshot des Dialogfelds mit "Speichern/nicht speichern" ](images/win-dialog-box-image38.png)

    In diesem Beispiel wird dieses Dialogfeld von Windows Paint als Ergebnis eines New- oder Exit-Befehls angezeigt, wenn die Grafik nicht gespeichert wurde. Speichern schließt das Dialogfeld ohne Speichern, während Abbrechen den Befehl Neu oder Beenden abbricht.

    **Falsch:**

    ![Screenshot des Dialogfelds mit Ja/Nein-Schaltflächen ](images/win-dialog-box-image39.png)

    In diesem Beispiel gibt es keine Möglichkeit, die Aufgabe (schließende Office-Verknüpfungsleiste) abzubrechen, die zum Anzeigen dieses Dialogfelds geführt hat. Für dieses Dialogfeld ist die Schaltfläche Abbrechen erforderlich.

-   **Wenn Benutzer nur den Dialog abbrechen müssen, aber nicht die Aufgabe, verwenden Sie eine Schaltfläche mit einer bestimmten, negativen Antwort auf die Hauptanweisung und** haben keine Schaltfläche Abbrechen.

    ![Screenshot des Dialogfelds mit "Ausführen/Nicht ausführen" ](images/win-dialog-box-image24.png)

    In diesem Beispiel wird dieses Dialogfeld indirekt als Ergebnis der Navigation zu einer Webseite angezeigt, die ein ActiveX-Steuerelement installiert. Die Verwendung von Abbrechen wäre hier mehrdeutig, daher wird stattdessen Nicht ausführen verwendet.

Weitere Informationen und Beispiele finden Sie unter [Befehlsschaltflächen.](ctrl-command-buttons.md)

### <a name="command-links"></a>Befehlslinks

-   **Stellen Sie eine Reihe von langen Befehlen mit Befehlslinks anstelle von Befehlsschaltflächen oder einer Kombination von Optionsfeldern und einer OK-Schaltfläche dar.** Auf diese Weise können Benutzer mit einem einzigen Klick antworten. Dieser Ansatz funktioniert jedoch nur für eine einzelne Frage.
-   **Zeigen Sie zuerst die am häufigsten verwendeten Befehlslinks an.** Die resultierende Reihenfolge sollte ungefähr der Wahrscheinlichkeit der Verwendung entsprechen, aber auch einen logischen Ablauf aufweisen.
    -   **Ausnahme:** Befehlslinks, die dazu führen, dass alles erledigt wird, sollten zuerst platziert werden.
-   Wenn ein Befehlslink eine weitere Erläuterung erfordert, **geben Sie eine ergänzende Erklärung an.** Ergänzende Erklärungen beschreiben, warum Benutzer den Befehl auswählen möchten oder was geschieht, wenn der Befehl ausgewählt wird.
-   **Verwenden Sie keine ergänzenden Erklärungen, bei denen es sich um wortliche Neuangaben des Befehlslinks handelt.** Verwenden Sie eine ergänzende Erklärung nur, wenn Sie einen Befehlslink nicht selbsterklärend machen können. Das Bereitstellen einer ergänzenden Erklärung für einen Befehlslink bedeutet nicht, dass Sie sie für alle Befehle bereitstellen müssen.

![Screenshot des Dialogfelds mit Textbeschriftungsoptionen ](images/win-dialog-box-image40.png)

In diesem Beispiel beschreibt die ergänzende Erläuterung die Auswirkungen einer der Optionen.

-   **Verwenden Sie Ausdrücke, die mit einem Verb beginnen, ohne die Interpunktion zu beenden.**
-   **Wenn ein Befehl dringend empfohlen wird, sollten Sie der Bezeichnung "(empfohlen)" hinzufügen.** Achten Sie darauf, der Linkbezeichnung und nicht der ergänzenden Erklärung hinzuzufügen.
-   **Wenn ein Befehl nur für fortgeschrittene Benutzer vorgesehen ist, sollten Sie der Bezeichnung "(advanced)" hinzufügen.** Achten Sie darauf, der Linkbezeichnung und nicht der ergänzenden Erklärung hinzuzufügen.
-   **Geben Sie immer eine explizite Schaltfläche Abbrechen an.** Verwenden Sie zu diesem Zweck keinen Befehlslink.

**Falsch:**

![Screenshot des Dialogfelds ohne Link zum Beenden ](images/win-dialog-box-image41.png)

In diesem Beispiel verwendet das Dialogfeld anstelle der Schaltfläche Abbrechen einen Befehlslink.

Weitere Informationen und Beispiele finden Sie unter [Befehlslinks.](ctrl-command-links.md)

### <a name="dont-show-this-item-again"></a>Zeigen Sie dies nicht an. <item> Wieder

-   **Erwägen Sie die Verwendung der Option Diese Option nicht <item> erneut anzeigen, damit Benutzer ein wiederkehrendes Dialogfeld nur unterdrücken können, wenn es keine bessere Alternative gibt.** Es ist besser, den Dialog immer anzuzeigen, wenn er wirklich von Benutzern benötigt wird, oder ihn einfach zu entfernen, wenn dies nicht dere ist.
-   **Verwenden Sie diesen spezifischen Ausdruck, und ersetzen Sie <item> durch das jeweilige Element.** Zeigen Sie diese Erinnerung z. B. nicht erneut an. Wenn Sie im Allgemeinen auf ein Dialogfeld verweisen, verwenden Sie Diese Meldung nicht mehr anzeigen.
-   **Geben Sie eindeutig an, wann Benutzereingaben für zukünftige Standardwerte verwendet werden** sollen, indem Sie den folgenden Satz unter der Option hinzufügen: Ihre Auswahl wird in Zukunft standardmäßig verwendet.
-   **Wählen Sie die Option nicht standardmäßig aus. Wenn das Dialogfeld wirklich nur einmal angezeigt werden soll, tun Sie dies ohne Nachfrage.** Verwenden Sie diese Option nicht, um Benutzer zu verärgern, und stellen Sie sicher, dass das Standardverhalten nicht mäßig ist.

**Falsch:**

![Screenshot der Meldung, die eine unnötige Frage stellt ](images/win-dialog-box-image42.png)

In diesem Beispiel sollte die Meldung nur einmal angezeigt werden. Sie müssen keine Fragen stellen.

-   **Legen Sie fest, dass die Einstellung pro Benutzer beibehalten wird.**
-   **Wenn Benutzer die Option auswählen und auf Abbrechen klicken, wird diese Option wirksam.** Diese Einstellung ist eine Metaoption, sodass sie nicht dem standardmäßigen Cancel-Verhalten entspricht, bei dem keine Nebeneffekte übrig bleiben. Beachten Sie Folgendes: Wenn Benutzer den Dialog in Zukunft nicht mehr sehen möchten, möchten sie es wahrscheinlich auch abbrechen.
-   Wenn Benutzer diese Dialogfelder möglicherweise wiederherstellen müssen, geben Sie im Dialogfeld Optionen des Programms den Befehl **Meldungen wiederherstellen** an.

### <a name="ask-me-later"></a>Später nachfragen

-   Geben Sie diese Option an, um ein Dialogfeld nur dann zu schließen, wenn:
    -   **Das Dialogfeld ist indirekt,** sodass benutzer sich wahrscheinlich auf eine andere Aufgabe konzentrieren.
    -   **Benutzer müssen reagieren, aber nicht sofort,** damit sie mit ihrer Arbeit fortfahren können.
    -   **Die Frage erfordert genügend Gedanken oder Aufwand,** damit Benutzer bessere Entscheidungen treffen können, wenn sie mehr Zeit haben.
    -   **Das Dialogfeld oder die Option wird später automatisch angezeigt** (sodass Benutzer später wirklich gefragt werden).
-   **Falsch:**
-   ![Screenshot der Nachricht mit der Option "Später fragen" ](images/win-dialog-box-image43.png)
-   In diesem Beispiel ist die Frage so einfach, dass das Hinzufügen der Option Später fragen dies nur erschwert.
-   Gehen Sie andernfalls davon aus, dass Benutzer jetzt antworten, aber erlauben Sie ihnen, das Dialogfeld normal mit Abbrechen oder Schließen zu schließen. Bei ordnungsgemäßer Verwendung sollte diese Option selten sein.

### <a name="morefewer"></a>Mehr/Weniger

-   **Verwenden Sie mehr/weniger Schaltflächen für die progressive Offenlegung, um erweiterte oder selten verwendete Optionen, Befehle oder Details anzuzeigen oder auszublenden, die benutzerin der Regel nicht benötigt werden.** Dadurch wird das Dialogfeld für die typische Verwendung vereinfacht. Blenden Sie häufig verwendete Optionen, Befehle oder Informationen nicht aus, da Benutzer sie möglicherweise nicht finden.

![Screenshot des Dialogfelds mit der Schaltfläche "Weitere Optionen" ](images/win-dialog-box-image24.png)

In diesem Beispiel werden selten verwendete Optionen standardmäßig ausgeblendet.

-   **Verwenden Sie keine Mehr/Weniger-Steuerelemente, es sei denn, es sind mehr Details zu sehen.** Verwenden Sie nicht nur die gleichen Informationen in einem anderen Format.
-   **Verwenden Sie keine Mehr/Weniger-Steuerelemente, um Hilfe zu zeigen.** Verwenden Sie stattdessen Hilfelinks oder Fußnotes.
-   **Vermeiden Sie bei Aufgabendialogfeldern die Kombination von Mehr/Weniger-Steuerelementen mit Nicht mehr <item> anzeigen.** Diese Kombination hat eine ums andere Darstellung.
-   Bezeichnungsrichtlinien finden Sie unter [Progressive Disclosure](ctrl-progressive-disclosure-controls.md).

### <a name="footnotes"></a>Fußnoten

-   **Verwenden Sie Fußnoten für Informationen, die für den Zweck eines Dialogfelds nicht von entscheidender Bedeutung sind, die Benutzer jedoch möglicherweise hilfreich finden, um Entscheidungen zu treffen.** Die meisten Benutzer sollten in der Lage sein, Fußnoten zu überspringen und dennoch fundierte Entscheidungen in ihrer Antwort auf das Dialogfeld zu treffen.

![Screenshot des Dialogfelds mit Verdeutlichung der Fußnote ](images/win-dialog-box-image44.png)

In diesem Beispiel sind die Fußnoteinformationen ergänzend und nicht wichtig.

### <a name="disabling-or-removing-controls-vs-giving-error-messages"></a>Deaktivieren oder Entfernen von Steuerelementen im Vergleich zum Senden von Fehlermeldungen

-   Wenn ein Steuerelement im aktuellen Kontext nicht angewendet wird, sollten Sie die folgenden Optionen in Betracht ziehen:
    -   **Entfernen Sie das Steuerelement, wenn es benutzern nicht möglich ist, es zu aktivieren, oder benutzer nicht erwarten, dass es angewendet wird und sich sein Zustand nicht häufig ändert.** Dadurch wird das Dialogfeld vereinfacht, und Benutzer werden es nicht übersehen. Es ist lästig, wenn ein Steuerelement häufig angezeigt und verschwindet.
    -   **Deaktivieren Sie das Steuerelement, wenn Benutzer erwarten, dass es angewendet wird oder sich sein Zustand häufig ändert, und Benutzer können leicht erkennen, warum das Steuerelement deaktiviert ist.** Ein Beispiel für eine einfache Ableitung ist das Deaktivieren einer Commitschaltfläche, wenn ein einzelnes, leeres Textfeld eine Eingabe erfordert. Sie können [Sprechblasen](ctrl-balloons.md) verwenden, um nicht kritische Benutzereingabeprobleme mit Textfeldern und bearbeitbaren Dropdownlisten anzuzeigen. Wenn das Problem jedoch nicht mit einem Balloon oder mehreren Steuerelementen erklärt werden kann, wäre die Ableitung nicht mehr einfach.
    -   **Lassen Sie andernfalls das Steuerelement aktiviert, aber geben Sie eine Fehlermeldung aus, wenn es falsch verwendet wird.** Wenn Sie in diesem Fall deaktivieren, ist es für Benutzer schwierig zu verstehen, warum das Steuerelement deaktiviert ist. Benutzer werden gezwungen, das Problem durch Experimentieren und dektive Logik zu bestimmen. Es ist besser, nur eine hilfreiche Fehlermeldung zu geben, um das Problem explizit zu erklären.
-   **Tipp:** Wenn Sie nicht sicher sind, ob Sie ein Steuerelement deaktivieren oder eine Fehlermeldung senden sollten, beginnen Sie mit dem Verfassen der Fehlermeldung, die Sie möglicherweise geben. Wenn die Fehlermeldung hilfreiche Informationen enthält, von denen Zielbenutzer wahrscheinlich nicht schnell abzuleiten sind, lassen Sie das Steuerelement aktiviert, und geben Sie den Fehler an. Deaktivieren Sie andernfalls das -Steuerelement.
-   **Wenn Sie ein Steuerelement deaktivieren, deaktivieren Sie auch alle** zugeordneten Steuerelemente, z. B. dessen Bezeichnung, ergänzende Erklärungen oder Befehlsschaltflächen. Deaktivieren Sie jedoch nicht die [Gruppenfelder,](ctrl-group-boxes.md)die Gruppenbezeichnung oder die Gruppenerklärung, falls diese noch nicht angegeben sind.

![Screenshot des Dialogfelds mit abgeblendeten Steuerelementen ](images/win-dialog-box-image45.png)

In diesem Beispiel sind die deaktivierten Textfeldbezeichnungen ebenfalls deaktiviert, ihre Gruppenbezeichnung und Gruppenerklärung jedoch nicht.

### <a name="required-input"></a>Erforderliche Eingabe

-   Um anzugeben, dass Benutzer Informationen in einem Steuerelement bereitstellen müssen, ziehen Sie die folgenden Optionen in Betracht:
    -   **Geben Sie nichts an, sondern behandeln Sie fehlende erforderliche Eingaben mit Fehlermeldungen.** Dieser Ansatz reduziert unübersichtlich und funktioniert gut, wenn die meisten Eingaben optional sind oder Benutzer wahrscheinlich keine Steuerelemente überspringen, wodurch die Anzahl der Fehlermeldungen niedrig bleibt.
    -   **Geben Sie die erforderliche Eingabe mit einem Sternchen am Anfang der Bezeichnung an.** Erläutern Sie das Sternchen mit einer der folgenden:

        -   Eine Fußnote am unteren Rand des Inhaltsbereichs mit dem Text \* Erforderliche Eingabe.
        -   Eine QuickInfo auf dem Sternchen mit dem Text Erforderliche Eingabe.

        Dieser Ansatz funktioniert gut, wenn es nicht viele erforderliche Steuerelemente gibt, aber schlecht, wenn die meisten Steuerelemente erforderlich sind.

        ![Screenshot von Textfeldbezeichnungen mit Sternchen ](images/win-dialog-box-image46.png)

        In diesem Beispiel werden Sternchen verwendet, um die erforderliche Eingabe anzugeben.

    -   **Wenn alle Steuerelemente eine Eingabe erfordern, geben Sie "Alle Eingaben erforderlich" an einer geeigneten Stelle oben im Inhaltsbereich an.** Dieser Ansatz reduziert die Übersichtlichkeit für diesen speziellen Fall.
    -   **Geben Sie optionale Eingaben mit "(optional)" nach der Bezeichnung an.** Dieser Ansatz funktioniert gut, wenn die meisten Eingaben erforderlich sind, andernfalls jedoch schlecht.

-   **Versuchen Sie zur Konsistenz, dieselbe Methode zu verwenden, um die erforderliche Eingabe im gesamten Programm anzugeben.** Geben Sie bei Bedarf entweder erforderliche oder optionale Eingaben an, vermeiden Sie jedoch die Verwendung beider Eingaben innerhalb desselben Programms.

### <a name="error-handling"></a>Fehlerbehandlung

-   Vermeiden Sie Fehler, indem Sie Steuerelemente verwenden, die auf gültige Benutzereingaben beschränkt sind. Sie können auch dazu beitragen, die Anzahl von Fehlern zu reduzieren, indem Sie sinnvolle Standardwerte bereitstellen.
-   Überprüfen Sie die Benutzereingabe so bald wie möglich, und zeigen Sie Fehler so nah wie möglich am Eingabepunkt an.
-   **Verwenden Sie die moduslose Fehlerbehandlung (Fehler oder Sprechblasen) für Benutzereingabeprobleme.**
    -   **Verwenden Sie Sprechblasen für nicht kritische Einzelpunkt-Benutzereingabeprobleme, die während eines Textfelds oder unmittelbar nach dem Verlust des Fokus eines Textfelds erkannt wurden.** Für Sprechblasen ist kein verfügbarer Bildschirmbereich oder das dynamische Layout erforderlich, das zum Anzeigen von Meldungen an Ort und Stelle erforderlich ist. Zeigt immer nur einen einzelnen Balloon an. Da das Problem nicht kritisch ist, ist kein Fehlersymbol erforderlich. Sprechblasen gehen beim Klicken, beim Beheben des Problems oder nach einem Timeout weg.

        ![Screenshot der Meldung "Falsches Zeichen" ](images/win-dialog-box-image47.png)

        In diesem Beispiel weist eine Sprechblase auf ein Eingabeproblem hin, das sich noch im -Steuerelement befing.

-   **Verwenden Sie für die verzögerte Fehlererkennung** in der Regel Fehler, die durch Klicken auf eine Commitschaltfläche gefunden werden. (Verwenden Sie keine direkt verfügbaren Fehler für Einstellungen, für die sofort ein Committed erfolgt.) Es können mehrere Fehler gleichzeitig auftreten. Verwenden Sie normalen Text und ein 16 x 16 Pixel großes Fehlersymbol, und platzieren Sie sie nach Möglichkeit direkt neben dem Problem. Direkt aufgetretene Fehler werden nur dann entfernt, wenn der Benutzer committ und keine anderen Fehler gefunden werden.

    ![Screenshot des Dialogfelds mit zwei Fehlermeldungen ](images/win-dialog-box-image48.png)

    In diesem Beispiel wird für einen Fehler, der durch Klicken auf die Schaltfläche "Commit" gefunden wurde, ein fehlerfehler verwendet.

-   **Verwenden Sie die modale** Fehlerbehandlung (Aufgabendialogfelder oder Meldungsfelder) für alle anderen Probleme, einschließlich Fehler, die mehrere Steuerelemente umfassen oder nicht kontextbezogene oder nicht eingabebezogene Fehler sind, die durch Klicken auf eine Commitschaltfläche gefunden werden.
-   **Wenn ein Eingabeproblem gefunden und gemeldet wird, legen Sie den Eingabefokus auf das erste Steuerelement mit den falschen Daten fest.** Scrollen Sie das Steuerelement bei Bedarf in die Ansicht.

Weitere Informationen und Beispiele finden Sie unter [Fehlermeldungen](mess-error.md) und [Balloons](ctrl-balloons.md).

### <a name="help"></a>Hilfe

-   Berücksichtigen Sie beim Bereitstellen von Benutzerunterstützung die folgenden Optionen (in der Reihenfolge ihrer Präferenz aufgeführt):
    -   Geben Sie interaktiven Steuerelementen selbsterklärende Bezeichnungen. Benutzer lesen die Bezeichnungen wahrscheinlicher auf interaktiven Steuerelementen als jeder andere Text.
    -   Stellen Sie Kontexterklärungen mit [statischen Textbezeichnungen zur Verfügung.](text-ui.md)
    -   Geben Sie einen bestimmten Hilfelink zu einem relevanten Hilfethema an.
-   **Suchen Sie unten im Inhaltsbereich des Dialogfelds nach Hilfelinks.** Wenn das Dialogfeld eine Fußnote hat und der Hilfelink damit verknüpft ist, platzieren Sie den Hilfelink in der Fußnote.

    ![Screenshot des Dialogfelds mit Hilfelink ](images/win-dialog-box-image40.png)

    In diesem Beispiel gilt der Hilfelink für den gesamten Dialog.

    -   **Ausnahme:** Wenn ein Dialogfeld über mehrere unterschiedliche Gruppen von Einstellungen verfügt, die separate Hilfethemen (z. B. in Gruppenfeldern) enthalten, suchen Sie die Hilfelinks unten in den Gruppen.

-   **Verwenden Sie keine allgemeinen oder ungenauen Links zu Hilfethemas oder generische Hilfeschaltflächen.** Benutzer ignorieren häufig die generische Hilfe.

Weitere Informationen und Beispiele finden Sie unter [Hilfe.](winenv-help.md)

### <a name="default-values"></a>Standardwerte

-   Fügen Sie in jedem Dialogfeld eine Standardschaltfläche für Commits ein.
-   Für Fragedialoge:
    -   **Wählen Sie die sicherste Antwort (um Datenverluste oder Systemzugriffe zu verhindern), als Standardantwort aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequemste Antwort aus.
        -   **Ausnahme:** Machen Sie eine destruktive Antwort nur dann zur Standardantwort, wenn es eine einfache, offensichtliche Möglichkeit gibt, den Befehl rückgängig zu machen.
-   Für Auswahldialoge:
    -   Wählen Sie für die anfänglichen Standardwerte die sichersten Werte (um Datenverluste oder Systemzugriffe zu verhindern) und die sichersten Werte **für jedes Steuerelement aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichsten oder bequemsten Optionen aus.
    -   Wählen Sie für die nachfolgenden Standardwerte die zuvor ausgewählten Optionen erneut aus, wenn diese Werte wahrscheinlich wiederholt werden, und dies **ist sicher und sicher.** Wählen Sie andernfalls die anfänglichen Standardwerte aus.

![Screenshot des Dialogfelds "Drucken" ](images/win-dialog-box-image49.png)

In diesem Beispiel wählen Benutzer wahrscheinlich die gleichen Druckeinstellungen wie beim letzten Mal aus. Die gewünschte Anzahl von Kopien wird sich jedoch wahrscheinlich ändern, sodass diese Einstellung nicht erneut ausgewählt wird.

## <a name="recommended-sizing-and-spacing&quot;></a>Empfohlene Größe und Abstand

-   **Unterstützung der Mindestauflösung des Windows Vista-Bildschirms von 800 x 600 Pixeln.** Layouts können für vergrößerbare Fenster mit einer Bildschirmauflösung von 1024 x 768 Pixeln optimiert werden.
-   **Verwenden Sie nach Möglichkeit verstellbare Fenster, um Bildlaufleisten und abgeschnittene Daten zu vermeiden.** Windows mit dynamischem Inhalt und Listen profitieren am meisten von verstellbaren Fenstern.
-   **Fenster mit fester Größe müssen vollständig sichtbar sein und so dimensioniert sein, dass sie in den Arbeitsbereich passen.**
-   **Vergrößerbare Fenster können für höhere Auflösungen optimiert werden, aber bei Bedarf zur Anzeigezeit auf die tatsächliche Bildschirmauflösung heruntersetzbar sein.**
-   **Wählen Sie eine für den Inhalt geeignete Standardfenstergröße aus.** Sie sollten keine größeren Anfangsfenster verwenden, wenn Sie den Platz effektiv nutzen können.

## <a name=&quot;text&quot;></a>Text

### <a name=&quot;general&quot;></a>Allgemein

-   **Entfernen Sie redundanten Text.** Suchen Sie in Titeln, Hauptanweisungen, ergänzenden Anweisungen, Inhaltbereichen, Befehlslinks und Commitschaltflächen nach redundantem Text. Lassen Sie im Allgemeinen vollständigen Text in Anweisungen und interaktiven Steuerelementen, und entfernen Sie alle Redundanzen von den anderen Stellen.
-   **Verwenden Sie positive Formulierungen.** Positive Formulierungen sind für Benutzer einfacher zu verstehen.

**Richtig:**

Möchten Sie die Datei- und Druckerfreigabe aktivieren?

**Falsch:**

Möchten Sie die Datei- und Druckerfreigabe deaktivieren?

Der Ausdruck muss jedoch mit dem zugeordneten Befehl übereinstimmen, auch wenn der Befehl negativ formuliert ist. verwenden Sie also beispielsweise disable, um einen Disable-Befehl zu bestätigen.

-   **Verwenden Sie bei Bedarf das Wort &quot;window&quot;, um auf das Dialogfeld selbst zu verweisen.**
-   **Verwenden Sie die zweite Person (&quot;Sie/Ihr"),** um Benutzern zu sagen, was im Hauptanweisungs- und Inhaltsbereich zu tun ist. Häufig wird die zweite Person impliziert.

**Beispiele:**

Wählen Sie die Bilder aus, die Sie drucken möchten.

Wählen Sie ein Konto aus.

-   **Verwenden Sie die erste Person ("I/me/my"),** damit Benutzer dem Programm mitteilen können, was in Steuerelementen im Inhaltsbereich zu tun ist, die auf die Hauptanweisung reagieren.

**Beispiel:** Drucken Sie die Fotos auf meiner Kamera.

### <a name="dialog-box-titles"></a>Titel des Dialogfelds

-   **Verwenden Sie den Titel, um den Befehl, das Feature oder das Programm zu identifizieren, von dem bzw. dem ein Dialogfeld stammt.**
    -   Wenn das Dialogfeld vom Benutzer initiiert wird, identifizieren Sie es mithilfe des Befehls oder Featurenamens. **Ausnahmen:**
        -   Wenn ein Dialogfeld von vielen verschiedenen Befehlen angezeigt wird, sollten Sie stattdessen den Programmnamen verwenden.
        -   Wenn dieser Titel mit der main-Anweisung redundant wäre, verwenden Sie stattdessen den Programmnamen.
    -   Wenn es programm- oder systemin initiiert ist (und daher nicht im Kontext liegt), identifizieren Sie es mithilfe des Programm- oder Featurenamens, um Kontext zu geben.
    -   Verwenden Sie den Titel nicht, um zu erläutern, was im Dialog zu tun ist, der der Zweck der Hauptanweisung ist.
-   Verwenden Sie den genauen Befehlsnamen für befehlsbasierte Namen, aber schließen Sie die Auslassungsellipse nicht ein, wenn ein Befehlsnamen vor ort ist. Sie können den Menütitel des Befehls bei Bedarf hinzufügen, um einen guten Titel zu erstellen. Beispiel: für ein Objekt... Befehl in einem Insert-Menü verwenden Sie den Titel Objekt einfügen.
-   **Wenn ein modusloses Dialogfeld** auf der Taskleiste angezeigt wird, optimieren Sie den Titel für die Anzeige auf der Taskleiste, indem Sie die unterscheidenden Informationen präzise an erster Stelle platzieren. Beispiele: "66 % abgeschlossen" und "3 Erinnerungen".
-   **Schließen Sie die Wörter "dialog" oder "progress" nicht in den Titel ein.** Dies ist impliziert, und das Deaktivieren erleichtert benutzern das Scannen.
-   Verwenden [Sie die Groß-/End-Groß-/Formatvorlage,](glossary.md)ohne die Interpunktion zu beenden.

### <a name="main-instructions"></a>Hauptanweisungen

-   **Verwenden Sie die Main-Anweisung, um kurz zu erläutern, was im Dialog zu tun ist.** Die Anweisung sollte eine bestimmte Anweisung, imperative Richtung oder Frage sein. Gute Anweisungen kommunizieren das Ziel des Benutzers mit dem Dialog, anstatt sich ausschließlich auf die Mechanismen der Bearbeitung zu konzentrieren.
-   **Lassen Sie die main-Anweisung weg, wenn das einzige, was Sie sagen können, offensichtlich ist.** In solchen Fällen ist der Inhalt des Dialogfelds selbsterklärend. Beispielsweise benötigen die allgemeinen Dialogfelder Datei öffnen und Datei speichern keine Hauptanweisung, da ihr Kontext und Ihr Entwurf ihren Zweck offensichtlich machen.
-   **Lassen Sie Steuerelementbezeichnungen weg, die die Hauptanweisung neu erstellen.** In diesem Fall übernimmt die main-Anweisung den Zugriffsschlüssel.

**Annehmbar:**

![Screenshot des Textfelds mit redundanter Bezeichnung ](images/win-dialog-box-image50.png)

In diesem Beispiel ist die Textfeldbezeichnung nur eine Neuformung der Main-Anweisung.

**Besser:**

![Screenshot des gleichen Textfelds mit einer Bezeichnung ](images/win-dialog-box-image51.png)

In diesem Beispiel wird die redundante Bezeichnung entfernt, sodass die main-Anweisung den Zugriffsschlüssel übernimmt.

-   **Seien Sie präzise, verwenden Sie nur einen einzelnen vollständigen Satz.** Machen Sie die Hauptanweisung auf die wesentlichen Informationen zurück. Wenn Sie mehr erklären müssen, verwenden Sie zusätzliche Anweisungen.
-   **Verwenden Sie nach Möglichkeit bestimmte Verben.** Bestimmte Verben (Beispiele: Verbinden, Speichern, Installieren) sind für Benutzer sinnvoller als generische Verben (Beispiele: Konfigurieren, Verwalten, Festlegen).
-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)
-   **Schließen Sie keine abschließenden Zeiträume ein, wenn die Anweisung eine -Anweisung ist.** Wenn es sich bei der Anweisung um eine Frage handelt, fügen Sie ein abschließendes Fragezeichen ein.
-   **Verwenden Sie für Statusdialoge einen Gerund-Ausdruck,** der den vorgang in Bearbeitung kurz erläutert und mit auslassungsenden Auslassungsfeldern endet. Beispiel: Drucken ihrer Bilder...
-   **Tipp:** Sie können eine Main-Anweisung auswerten, indem Sie sich vorstellbar machen, was Sie einem Freund sagen würden. Wenn die Antwort mit der main-Anweisung unnatürlich, nicht hilfreich oder umstirnlich wäre, überarbeiten Sie die Anweisung.

### <a name="supplemental-instructions"></a>Zusätzliche Anweisungen

-   **Verwenden Sie bei Bedarf eine optionale zusätzliche Anweisung, um zusätzliche Informationen anzuzeigen, die für das Verständnis oder die Verwendung der Seite hilfreich sind.** Sie können ausführlichere Informationen bereitstellen und Terminologie definieren.
-   **Wenn die Darstellung des Dialogfelds programm- oder systemin initiiert ist (und daher nicht im Kontext liegt), verwenden Sie die ergänzende Anweisung, um zu erläutern, warum der Dialog angezeigt wurde.** Bei solchen Dialogen ist der Kontext in der Regel nicht offensichtlich.
-   **Wiederholen Sie die Hauptanweisung nicht mit etwas anderen Formulierungen.** Lassen Sie stattdessen die zusätzliche Anweisung weg, wenn nicht mehr hinzugefügt werden muss.
-   Verwenden Sie vollständige Sätze, Groß- und Groß-/Endzeichen im Satzstil.

### <a name="command-links"></a>Befehlslinks

-   **Wählen Sie präzisen Linktext aus, der eindeutig kommuniziert und unterscheidet, was der Befehlslink tut.** Sie sollte selbsterklärend sein und der Hauptanweisung entsprechen. Benutzer sollten nicht herausfinden müssen, was der Link wirklich bedeutet oder wie er sich von anderen Links unterscheidet.
-   **Der Befehl "Start" wird immer mit einem Verb verknüpft.**
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Verwenden Sie keine Interpunktion am Ende.
-   **Geben Sie bei Bedarf mit vollständigen Sätzen und beendenden Satzzeichen weitere Erläuterungen an.** Fügen Sie solche Erklärungen jedoch nur bei Bedarf hinzu, fügen Sie nicht allen Befehlslinks Erklärungen hinzu, nur weil ein Befehlslink eine solche benötigt.

Weitere Informationen und Beispiele finden Sie unter [Richtlinien für Befehlslinks.](ctrl-command-links.md)

### <a name="commit-buttons"></a>Commitschaltflächen

-   **Verwenden Sie bestimmte Commitschaltflächenbezeichnungen, die allein sinnvoll sind und eine Antwort auf die Hauptanweisung sind.** Im Idealfall sollten Benutzer nichts anderes lesen müssen, um die Bezeichnung zu verstehen. Benutzer lesen die Bezeichnungen der Befehlsschaltfläche viel wahrscheinlicher als statischen Text.
-   **Starten Sie Die Bezeichnungen der Commitschaltfläche mit einem Verb. Ausnahmen sind OK, Ja und Nein.**
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Verwenden Sie keine Interpunktion am Ende.
-   Weisen Sie einen [eindeutigen Zugriffsschlüssel zu.](glossary.md)
    -   **Ausnahme:** Weisen Sie den Schaltflächen OK und Abbrechen keine Zugriffsschlüssel zu, da DIE EINGABETASTE und ESC ihre Zugriffsschlüssel sind. Dadurch wird die Zuweisung der anderen Zugriffsschlüssel vereinfacht.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Dialogfelder:

-   Verweisen Sie in der Programmierung und anderen technischen Dokumentationen auf Dialogfelder als Dialogfelder. Verweisen Sie überall auf Dialogfelder, indem Sie ihren Titel verwenden. Wenn die Titelleiste ausgeblendet ist, verweisen Sie mithilfe der main-Anweisung auf den Dialog.
-   Wenn Sie im Allgemeinen auf ein Dialogfeld verweisen müssen, verwenden Sie das Fenster in der Benutzerdokumentation. Sie können auf ein einfaches Fragedialogfeld oder eine Bestätigung als Nachricht verweisen.
-   Verwenden Sie den genauen Titel- oder Hauptanweisungstext, einschließlich der Groß-/Groß-/Groß-/A-
-   Formatieren Sie den Titel nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie den Titel nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Klicken **Windows-Sicherheit** auf **Weitere Optionen.**

