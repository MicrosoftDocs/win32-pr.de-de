---
title: Dialog Felder (Entwurfs Grundlagen)
description: Ein Dialogfeld ist ein sekundäres Fenster, das es Benutzern ermöglicht, einen Befehl auszuführen, Benutzer zu einer Frage zu bitten oder Benutzern Informationen oder ein Fortschritts Feedback bereitstellt.
ms.assetid: 2ded9f30-d45f-4027-a85d-4e7d0e412793
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0db9d705cb697cdad9ed29dad86faf5f96665dd5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104560999"
---
# <a name="dialog-boxes-design-basics"></a>Dialog Felder (Entwurfs Grundlagen)

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Ein Dialogfeld ist ein sekundäres Fenster, das es Benutzern ermöglicht, einen Befehl auszuführen, Benutzer zu einer Frage zu bitten oder Benutzern Informationen oder ein Fortschritts Feedback bereitstellt.

![Bildschirm Abbildung zur Identifizierung von Dialogfeld Elementen ](images/win-dialog-box-image1.png)

Ein typisches Dialogfeld.

Dialog Felder bestehen aus einer Titelleiste (zur Identifizierung des Befehls, der Funktion oder des Programms, aus dem ein Dialogfeld stammt), einer optionalen Haupt Anweisung (um das Ziel des Benutzers mit dem Dialogfeld zu erläutern), verschiedener Steuerelemente im Inhalts Bereich (zum Darstellen von Optionen) und Commit-Schaltflächen (um anzugeben, wie der Benutzer den Commit für die Aufgabe ausführen möchte).

Dialog Felder haben zwei grundlegende Typen:

-   Für **modale Dialogfelder** müssen Benutzer abgeschlossen und geschlossen werden, bevor Sie mit dem Besitzer Fenster fortfahren. Diese Dialogfelder eignen sich am besten für kritische oder seltene, einmalige Aufgaben, die abgeschlossen werden müssen, bevor Sie fortfahren.
-   Mit nicht modalem **Dialogfeldern** können Benutzer nach Belieben zwischen dem Dialogfeld und dem Besitzer Fenster wechseln. Diese Dialogfelder werden am besten für häufige, wiederkehrende, laufende Aufgaben verwendet.

**Ein Aufgaben Dialogfeld ist ein Dialogfeld, das mithilfe der Task Dialog-API (Application Programming Interface) implementiert wird.** Sie bestehen aus den folgenden Teilen, die in einer Vielzahl von Kombinationen zusammengefasst werden können:

-   Eine **Titelleiste** zur Identifizierung der Anwendung oder des System Features, von dem aus das Dialogfeld stammt.
-   Eine **Haupt Anweisung** mit einem optionalen Symbol, um das Ziel des Benutzers mit dem Dialogfeld zu identifizieren.
-   Ein **Inhalts Bereich** für beschreibende Informationen und Steuerelemente.
-   Einen **Befehlsbereich** für Commit-Schaltflächen, einschließlich einer Schaltfläche "Abbrechen", und optionale weitere Optionen, die nicht angezeigt werden <item> wieder-Steuerelemente.
-   Ein **fußnotiz Bereich** mit optionalen zusätzlichen Erläuterungen und Hilfe, der in der Regel auf weniger erfahrene Benutzer ausgerichtet ist.

![Screenshot eines typischen Aufgaben Dialogfelds ](images/win-dialog-box-image2.png)

Ein typisches Aufgaben Dialogfeld.

**Aufgaben Dialogfelder werden bei Bedarf empfohlen, da Sie einfach zu erstellen sind und ein konsistentes Erscheinungsbild erzielt werden.** Aufgaben Dialogfelder erfordern Windows Vista oder höher, sodass Sie nicht für frühere Versionen von Microsoft Windows geeignet sind.

Ein Aufgabenbereich ähnelt einem Dialogfeld, mit dem Unterschied, dass er nicht in einem separaten Fenster, sondern in einem Fensterbereich angezeigt wird. Daher haben Aufgabenbereiche ein direkteres kontextbezogenes Gefühl als Dialogfelder. Obwohl Sie technisch gesehen nicht identisch sind, **sind die Aufgabenbereiche so ähnlich wie in den entsprechenden Dialogfeldern, die in diesem Artikel vorgestellt werden**.

![Screenshot eines typischen Aufgabenbereichs ](images/win-dialog-box-image3.png)

Ein typischer Aufgabenbereich.

Eigenschaften [Fenster](win-property-win.md) sind eine spezielle Art von Dialogfeld zum Anzeigen und Ändern von Eigenschaften für ein Objekt, eine Auflistung von Objekten oder ein Programm. Außerdem unterstützen Eigenschaften Fenster in der Regel mehrere Aufgaben, wohingegen Dialogfelder in der Regel eine einzelne Aufgabe oder einen Schritt in einer Aufgabe unterstützen. Da ihre Verwendung spezialisiert ist, **werden Eigenschaften Fenster in einem anderen Satz von Richtlinien behandelt**.

Dialogfelder können [Registerkarten](ctrl-tabs.md)enthalten, und wenn dies der Fall ist, werden Sie als Dialogfelder im Register Format bezeichnet. Eigenschafts Fenster werden durch ihre Darstellung von Eigenschaften bestimmt, nicht durch die Verwendung von Registerkarten.

**Hinweis:** Die Richtlinien im Zusammenhang mit [Layout](vis-layout.md), [Fensterverwaltung](win-window-mgt.md), allgemeinen Dialogfeldern, [Eigenschaften Fenstern](win-property-win.md), [Assistenten](win-wizards.md), [Bestätigungen](mess-confirm.md), [Fehlermeldungen](mess-error.md)und [Warnmeldungen](mess-warn.md) werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Dient der Verwendung von Informationen, Benutzern eine Frage zu stellen oder Benutzern das Auswählen von Optionen zum Ausführen eines Befehls oder einer Aufgabe gestatten?** Wenn nicht, verwenden Sie eine andere Benutzeroberfläche (User Interface, UI).
-   **Dient das Anzeigen und Ändern von Eigenschaften für ein Objekt, eine Auflistung von Objekten oder ein Programm?** Wenn ja, verwenden Sie stattdessen ein [Eigenschaften Fenster](win-property-win.md) oder eine [Symbolleiste](cmd-toolbars.md) .
-   **Ist der Zweck, eine Auflistung von Befehlen oder Tools darzustellen?** Wenn dies der Fall ist, verwenden Sie eine Symbolleiste oder [Palette](glossary.md).
-   **Soll überprüft werden, ob der Benutzer eine Aktion fortsetzen möchte?** Gibt es einen eindeutigen Grund, den Vorgang nicht fortzusetzen, und eine angemessene Wahrscheinlichkeit, dass Benutzer manchmal nicht Wenn dies der Fall ist, verwenden Sie eine [Bestätigung](mess-confirm.md).
-   **Dient der Verwendung eines Fehlers oder einer Warnmeldung?** Wenn dies der Fall ist, verwenden Sie eine [Fehlermeldung](mess-error.md) oder eine [Warnmeldung](mess-warn.md).
-   Zweck:
    -   Dateien öffnen
    -   Dateien speichern
    -   Ordner öffnen
    -   Suchen oder Ersetzen von Text
    -   Drucken eines Dokuments
    -   Attribute einer gedruckten Seite auswählen
    -   Schriftart auswählen
    -   Farbe auswählen
    -   Datei, Ordner, Computer oder Drucker suchen
    -   Suchen nach Benutzern, Computern oder Gruppen in Microsoft Active Directory
    -   Eingabeaufforderung für Benutzername und Kennwort

Wenn dies der Fall ist, verwenden Sie stattdessen das entsprechende [Allgemeine Dialog](win-common-dlg.md) Feld. Viele dieser gängigen Dialogfelder sind erweiterbar.

-   **Ist der Zweck, eine mehrstufige Aufgabe auszuführen, für die mehr als ein einzelnes Fenster erforderlich ist?** Wenn dies der Fall ist, verwenden Sie stattdessen einen [Task Fluss](glossary.md) oder [Assistenten](win-wizards.md) .
-   **Soll der Benutzer über ein System-oder Programm Ereignis informiert werden, das sich nicht auf die aktuelle Benutzeraktivität bezieht, die keine sofortige Benutzeraktion erfordert, und die Benutzer kostenlos ignorieren können?** Wenn dies der Fall ist, verwenden Sie stattdessen eine [Benachrichtigung](mess-notif.md) .
-   **Soll der Programmstatus angezeigt werden?** Wenn dies der Fall ist, verwenden Sie stattdessen eine [Statusleiste](ctrl-status-bars.md) .
-   **Wäre es vorzuziehen, die direkte Benutzeroberfläche zu verwenden?** Dialog Felder können den Fluss des Benutzers unterbrechen, indem Sie die Aufmerksamkeit anfordern. In manchen Fällen ist die Unterbrechung im Flow gerechtfertigt, z. b. wenn der Benutzer eine Aktion ausführen muss, die außerhalb des aktuellen Kontexts liegt. In anderen Fällen ist es besser, die Benutzeroberfläche im Kontext zu präsentieren, entweder direkt mit einer direkten Benutzeroberfläche (z. b. einem Aufgabenbereich) oder nach Bedarf mithilfe [progressiver Offenlegung](ctrl-progressive-disclosure-controls.md).
-   **Ist der Zweck der Anzeige eines nicht kritischen Benutzereingabe Problems oder einer besonderen Bedingung?** Verwenden Sie in diesem Fall [stattdessen eine](ctrl-balloons.md) Sprechblase.
-   **Wäre es für Aufgaben Flüsse vorzuziehen, eine andere Seite zu verwenden?** Im Allgemeinen möchten Sie, dass eine Aufgabe innerhalb eines einzelnen Fensters von einer Seite an eine Seite weitergeleitet wird. Verwenden Sie Dialogfelder, um direkte Befehle zu bestätigen, Eingaben für direkte Befehle zu erhalten und sekundäre, eigenständige Aufgaben auszuführen, die am besten unabhängig voneinander und außerhalb des Hauptaufgaben Flusses ausgeführt werden.
-   **Werden die Optionen für die Auswahl von Optionen wahrscheinlich geändert?** Falls nicht, sollten Sie Alternativen in Erwägung nehmen, z. b.
    -   Verwenden der Standardoptionen, ohne zu Fragen, Benutzer jedoch später Änderungen vornehmen zu müssen.
    -   Bereitstellen einer Version mit Optionen (z **. b. Drucken...** in einem Menü) und einer Version ohne Optionen (z. b. **Drucken** auf der Symbolleiste). Im Allgemeinen sollten Symbolleisten Befehle direkt erfolgen und die Anzeige von Dialogfeldern vermeiden.
-   **Gibt es für die Auswahl von Optionen eine einfachere und direktere Möglichkeit zur Darstellung der Optionen?** Wenn dies der Fall ist, sollten Sie Alternativen in Erwägung gezogen haben:
    -   Verwenden einer [Trenn Schaltfläche](ctrl-command-buttons.md) , um Variationen eines Befehls auszuwählen.
    -   Verwenden eines Untermenüs für Befehle, Kontrollkästchen, Options Felder und einfache Listen.

![Screenshot, der ein Menü und ein unter Menü anzeigt.](images/win-dialog-box-image4.png)

![Screenshot eines Menüs und eines Untermenüs ](images/win-dialog-box-image5.png)

In diesen Beispielen werden Untermenüs anstelle von Dialogfeldern für die einfache Auswahl verwendet.

## <a name="design-concepts"></a>Entwurfskonzepte

Wenn Sie ordnungsgemäß verwendet werden, sind Dialogfelder eine hervorragend Möglichkeit, Ihrem Programm Leistungsfähigkeit und Flexibilität zu bieten. Wenn Sie missbraucht werden, stellen Dialogfelder eine einfache Möglichkeit dar, um Benutzer zu belästigen, den Flow zu unterbrechen und das Programm indirekt und mühsam zu verwenden. **Modale Dialogfelder erfordern eine Benutzer Aufmerksamkeit.** Dialog Felder sind häufig einfacher zu implementieren als Alternative Benutzeroberflächen, sodass Sie eher überlastet sind.

**Ein Dialogfeld ist am effektivsten, wenn dessen Entwurfs Merkmale der Verwendung entsprechen.** Der Entwurf eines Dialog Felds wird größtenteils durch seinen Zweck bestimmt (zum anbieten von Optionen, stellen von Fragen, Bereitstellen von Informationen oder Feedback), Typ (modal oder MODELESS) und Benutzerinteraktion (erforderlich, optionale Antwort oder Bestätigung), wohingegen seine Verwendung größtenteils durch den Kontext (Benutzer oder Programm initiiert), die Wahrscheinlichkeit der Benutzeraktion und die Anzeige Häufigkeit bestimmt wird.

Um effektive Dialogfelder zu entwerfen, verwenden Sie die folgenden Elemente effektiv:

-   Dialog Feld Text
-   Haupt Anleitung
-   Nicht anzeigen <item> erneut

**Wenn Sie nur eine Aktion ausführen...**

Stellen Sie sicher, dass der Entwurf des Dialog Felds (bestimmt durch den Zweck, den Typ und die Benutzerinteraktion) mit der Verwendung übereinstimmt (bestimmt durch den Kontext, die Wahrscheinlichkeit der Benutzeraktion und die Anzeige Häufigkeit).

## <a name="usage-patterns"></a>Verwendungsmuster

Dialog Felder weisen mehrere Verwendungs Muster auf:

-   Mit Frage Dialogfeldern (mithilfe von Schaltflächen) können Benutzer eine einzelne Frage stellen oder einen Befehl bestätigen und einfache Antworten in horizontal angeordneten Befehls Schaltflächen verwenden.
-   Mit Frage Dialogfeldern (über Befehls Verknüpfungen) können Benutzer eine einzelne Frage stellen oder eine auszuführende Aufgabe auswählen und ausführliche Antworten in vertikal angeordneten Befehls Verknüpfungen verwenden.
-   Auswahl Dialogfelder stellen Benutzern eine Reihe von Optionen zur Verfügung, in der Regel zur vollständigen Angabe eines Befehls. Anders als bei Frage Dialogfeldern können Auswahl Dialogfelder mehrere Fragen stellen.
-   Fortschritts Dialogfelder zeigen Benutzern während eines langen Vorgangs (mehr als fünf Sekunden) ein Fortschritts Feedback an, zusammen mit einem Befehl zum Abbrechen oder Beenden des Vorgangs.
-   Informations Dialogfelder zeigt vom Benutzer angeforderte Informationen an.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Verwenden Sie keine scrollfähigen Dialogfelder.** Verwenden Sie keine Dialogfelder, die erfordern, dass eine Schiebe Leiste während der normalen Verwendung vollständig angezeigt wird. Entwerfen Sie stattdessen das Dialogfeld neu. Verwenden Sie [Progressive Offenlegung](ctrl-progressive-disclosure-controls.md) oder [Registerkarten](ctrl-tabs.md).
-   **Sie haben keine Menüleiste oder Statusleiste.** Stattdessen können Sie den Zugriff auf Befehle und Status direkt im Dialogfeld selbst oder mithilfe von Kontextmenüs für die entsprechenden Steuerelemente ermöglichen.

    -   **Ausnahme:** Menüleisten sind akzeptabel, wenn ein Dialogfeld verwendet wird, um ein primäres Fenster (z. b. ein-Hilfsprogramm) zu implementieren.

    **Falsch:**

    ![Screenshot eines Dialog Felds mit einer Menüleiste ](images/win-dialog-box-image6.png)

    In diesem Beispiel ist die Option Zertifikate suchen ein nicht modalem Dialogfeld mit einer Menüleiste.

-   Wenn ein Dialogfeld sofortige Aufmerksamkeit erfordert und das Programm nicht aktiv ist, **blinken Sie die Task leisten Schaltfläche dreimal, um die Aufmerksamkeit zu zeichnen, und lassen Sie es hervorgehoben.** Führen Sie nichts anderes aus: Wiederherstellen oder aktivieren Sie das Fenster nicht, und spielen Sie keine Soundeffekte. Beachten Sie stattdessen die Fenster Zustands Auswahl des Benutzers, und lassen Sie den Benutzer das Fenster aktivieren, wenn Sie bereit sind.
-   Weitere Richtlinien und Beispiele finden Sie unter [Taskleiste](winenv-taskbar.md).

### <a name="modal-dialog-boxes"></a>Modale Dialogfelder

-   **Verwenden Sie für wichtige oder seltene, einmalige Aufgaben, die abgeschlossen werden müssen, bevor Sie fortfahren.**
-   Verwenden Sie ein [Verzögertes commitmodell](glossary.md) , damit Änderungen erst wirksam werden, wenn explizit ein Commit ausgeführt wird.
-   **Implementieren Sie immer dann mithilfe eines Aufgaben Dialogfelds, um ein konsistentes Aussehen zu erzielen.** Aufgaben Dialogfelder erfordern Windows Vista oder höher, sodass Sie nicht für frühere Versionen von Windows geeignet sind.

### <a name="modeless-dialog-boxes"></a>Nicht modante Dialogfelder

-   **Verwenden Sie für häufige, wiederkehrende, laufende Aufgaben.**
-   Verwenden Sie ein [sofortiges Commit-Modell](glossary.md) , damit Änderungen sofort wirksam werden.
-   Verwenden Sie für modaldialogfelder eine explizite Befehls Schaltfläche zum Schließen des Dialog Felds, um das Fenster zu schließen. Verwenden Sie für beide die Schaltfläche Schließen auf der Titelleiste, um das Fenster zu schließen.
-   **Sie sollten das andockbare Dialogfeld in Erwägung haben.** Andockbare nicht modale Dialogfelder ermöglichen eine flexiblere Platzierung.

![Screenshot eines andockbaren, nicht modablen Dialog Felds ](images/win-dialog-box-image7.png)

Einige nicht modlose Dialogfelder, die in Microsoft Office verwendet werden, sind Dockbar.

### <a name="multiple-dialog-boxes"></a>Mehrere Dialogfelder

-   **Zeigen Sie nicht mehr als ein eigenes Auswahl Dialogfeld gleichzeitig aus einem Dialogfeld für die Besitzer Auswahl an.** Wenn Sie mehr als eins anzeigen, ist die Bedeutung der Commit-Schaltflächen für Benutzer schwer zu verstehen. Möglicherweise werden bei Bedarf andere Dialogfeld Typen angezeigt (z. b. Frage Dialogfelder).
-   **Für eine Sequenz verwandter Dialoge sollten Sie ggf. ein mehrseitiges Dialogfeld verwenden.** Verwenden Sie einzelne Dialogfelder, wenn Sie nicht eindeutig verknüpft sind.

### <a name="multi-page-dialog-boxes"></a>Mehrseitige Dialogfelder

-   Verwenden Sie ein mehrseitiges Dialogfeld anstelle von einzelnen Dialogfeldern, wenn Sie die folgende Sequenz von verwandten Seiten haben:
    -   Eine einzelne Eingabe Seite (optional)
    -   Eine Fortschritts Seite
    -   Eine einzelne Ergebnisseite

Die Eingabe Seite ist optional, da die Aufgabe möglicherweise an einer anderen Stelle initiiert wurde. **Dadurch erhalten Sie einen stabilen, einfachen und einfachen Eindruck von der resultierenden Erfahrung.**

![Screenshot einer Statusanzeige ](images/win-dialog-box-image8.png)

![Screenshot der Meldung "Es wurden keine Probleme gefunden" ](images/win-dialog-box-image9.png)

In diesem Beispiel besteht die Windows-Netzwerk Diagnose aus den Seiten für Fortschritt und Ergebnisse.

-   **Verwenden Sie kein mehrseitiges Dialogfeld, wenn die Eingabe Seite ein Standard Dialogfeld ist.** In diesem Fall ist die Konsistenz der Verwendung eines Standard Dialogfelds wichtiger.
-   **Verwenden Sie nicht die Schaltflächen "weiter" oder "zurück", und haben Sie nicht mehr als** Mehrseitige Dialogfelder sind für Einzelschritt-Aufgaben mit Feedback. Sie sind keine [Assistenten](win-wizards.md), die für Aufgaben mit mehreren Schritten verwendet werden. Die Assistenten haben eine hohe, indirekte Ansicht im Vergleich zu mehrseitigen Dialogfeldern.
-   **Verwenden Sie auf der Seite Eingabe bestimmte Befehls Schaltflächen oder Befehls Verknüpfungen, um die Aufgabe zu initiieren.**
-   **Verwenden Sie die Schaltfläche Abbrechen auf den Seiten Eingabe und Status und die Schaltfläche Schließen auf der Seite Ergebnisse.**

**Entwickler:** Mithilfe der [TDM- \_ Navigations \_ Seiten](../controls/tdm-navigate-page.md) Meldung können Sie Aufgaben Dialogfelder mit mehreren Seiten erstellen.

### <a name="presentation"></a>Präsentation

Damit Dialogfelder leicht zu finden und darauf zugreifen können, ordnen Sie das Dialogfeld der Quelle zu, und arbeiten Sie gut mit mehreren Monitoren zusammen:

-   **Zeigen Sie zunächst die Dialogfelder "zentriert" oberhalb des Besitzer Fensters an.** In der nachfolgenden Anzeige sollten Sie die Anzeige an der letzten Position (relativ zum Besitzer Fenster) anzeigen, wenn dies wahrscheinlich bequemer ist.

![Diagramm des Dialog Felds, das auf ein Fenster hinter ihm zentriert ist ](images/win-dialog-box-image10.png)

Zentrieren Sie die Dialoge zunächst über das Besitzer Fenster.

-   **Wenn ein Dialogfeld kontextbezogen ist, sollten Sie es in der Nähe des Objekts anzeigen, von dem es gestartet wurde.** Platzieren Sie Sie jedoch (vorzugsweise nach unten und nach rechts), damit das Objekt nicht durch das Dialogfeld abgedeckt wird.

![Diagramm des Dialogfeld Offsets nach unten und rechts ](images/win-dialog-box-image11.png)

Die Eigenschaften eines Objekts werden in der Nähe des Objekts angezeigt.

-   **Bei nicht modalem Dialogfeldern zeigen Sie zunächst oberhalb des Besitzer Fensters an, um die Suche zu erleichtern.** Wenn der Benutzer das Besitzer Fenster aktiviert, kann dies das nicht modante Dialogfeld verbergen.
-   **Passen Sie ggf. den ursprünglichen Speicherort so an, dass das gesamte Dialogfeld innerhalb des Ziel Monitors sichtbar ist.** Wenn ein Fenster, das in der Größe geändert werden kann, größer als der Ziel Monitor ist, verringern Sie es.
-   **Wenn ein Dialogfeld erneut angezeigt wird, sollten Sie es in demselben Zustand wie zuletzt aufgerufen anzeigen.** Speichern Sie unter schließen den verwendeten Monitor, die Fenstergröße, den Speicherort und den Status (maximiert und Wiederherstellung). Stellen Sie bei der erneuten Anzeige die Größe, den Speicherort und den Zustand des gespeicherten Dialog Felds mithilfe des entsprechenden Monitors wieder her. Sie sollten diese Attribute auch auf Benutzerbasis über Programm Instanzen hinweg beibehalten.
-   **Legen Sie für Fenster mit Größenänderung eine minimale Fenstergröße fest, wenn eine Größe vorhanden ist, unter der der Inhalt nicht mehr verwendbar ist.** Sie sollten die Präsentation ändern, damit der Inhalt in geringerer Größe verwendet werden kann.

![Screenshot der Schaltflächen für zentrierte Medien Player ](images/win-dialog-box-image12.png)

In diesem Beispiel ändert Windows Media Player sein Format, wenn das Fenster für das Standardformat zu klein wird.

-   **Verwenden Sie das Top-Attribut "Always on" nicht.**
    -   **Ausnahme:** Wird nur verwendet, wenn ein Dialogfeld eine im wesentlichen modale Operation implementiert, es aber nur kurz angehalten werden muss, um auf das Besitzer Fenster zuzugreifen. Wenn Sie z. b. die Rechtschreibprüfung für ein Dokument durch Schreiben, können Benutzer gelegentlich das Dialogfeld Rechtschreibprüfung verlassen und auf das Dokument zugreifen, um Fehler zu beheben.

Weitere Informationen und Beispiele finden Sie unter [Fensterverwaltung](win-window-mgt.md).

### <a name="title-bars"></a>Titelleisten

-   **Dialog Felder haben keine Symbole für die Titelleiste.** Symbole der Titelleiste werden als visueller Unterschied zwischen [primären](glossary.md) und [sekundären Fenstern](glossary.md)verwendet.
    -   **Ausnahme:** Wenn ein-Dialogfeld verwendet wird, um ein primäres Fenster (z. b. ein-Hilfsprogramm) zu implementieren und daher auf der Taskleiste angezeigt wird, verfügt es über ein Titelleisten Symbol. Optimieren Sie in diesem Fall den Titel für die Anzeige auf der Taskleiste, indem Sie die Unterscheidungs Informationen an erster Stelle platzieren.
-   **Dialog Felder haben immer die Schaltfläche Schließen.** Nicht modaldialogfelder können auch eine Schaltfläche Minimieren aufweisen. Dialogfelder mit Größenänderung können eine Schaltfläche zum Maximieren haben.
-   **Deaktivieren Sie die Schaltfläche Schließen nicht.** Wenn Sie über eine Schaltfläche "Schließen" verfügen, können Benutzer die Kontrolle behalten, indem Sie Ihnen gestatten, Windows zu schließen.
    -   **Ausnahme:** Für Fortschritts Dialogfelder können Sie die Schaltfläche schließen deaktivieren, wenn die Aufgabe bis zum Abschluss ausgeführt werden muss, um einen gültigen Zustand zu erreichen oder Datenverluste zu verhindern.
-   **Die Schaltfläche Schließen auf der Titelleiste sollte dieselbe Auswirkung wie die Schaltfläche Abbrechen oder schließen** im Dialogfeld haben. Legen Sie den gleichen Effekt wie "OK".
-   Wenn die Titelleisten Beschriftung und das Symbol bereits auf eine deutliche Weise im oberen Bereich des Fensters angezeigt werden, können Sie die Beschriftung und das Symbol der Titelleiste ausblenden, um Redundanz zu vermeiden. Sie müssen jedoch immer noch einen passenden Titel für die Verwendung durch Windows festlegen.

### <a name="interaction"></a>Interaktion

-   **Wenn Sie angezeigt werden, sollten Benutzer initiierte Dialogfelder immer den Eingabefokus übernehmen.** Programm initiierte Dialogfelder sollten den Eingabefokus nicht übernehmen, da der Benutzer möglicherweise mit einem anderen Fenster interagiert. Solche Interaktionen, die im Dialogfeld falsch gesteuert werden, können unbeabsichtigte Folgen haben.
-   **Weisen Sie dem Steuerelement den anfänglichen Eingabefokus zu, mit dem Benutzer am wahrscheinlichsten mit der ersten Interaktion interagieren**, was in der Regel (aber nicht immer) das erste interaktive Steuerelement ist. Vermeiden Sie das Zuweisen des ersten Eingabefokus zu einem Hilfelink.
-   **Bei der Tastaturnavigation sollte die Aktivier Reihenfolge in einer logischen Reihenfolge von links nach rechts und von oben nach unten fließen.** Normalerweise folgt die Aktivier Reihenfolge auf die Lesefolge, aber Sie sollten diese Ausnahmen

    -   Fügen Sie die am häufigsten verwendeten Steuerelemente zuvor in der Aktivier Reihenfolge
    -   Fügen Sie Hilfe Links am unteren Rand eines Dialog Felds nach den Commit-Schaltflächen in der Aktivier Reihenfolge ein.

    Wenn Sie die Bestellung zuweisen, gehen Sie davon aus, dass Benutzerdialog Felder für ihren vorgesehenen Zweck anzeigen. beispielsweise zeigen Benutzer die Auswahl Dialogfelder an, um Auswahlmöglichkeiten zu treffen, und klicken auf "Abbrechen".

-   **Durch Drücken der ESC-Taste wird immer ein aktives Dialogfeld geschlossen.** Dies gilt für Dialogfelder mit "Abbrechen" oder "Schließen", auch wenn "Abbrechen" in "Close" umbenannt wurde, weil die Ergebnisse nicht mehr rückgängig gemacht werden können.

**Zugriffsschlüssel**

-   **Weisen Sie allen interaktiven Steuerelementen oder deren Bezeichnungen nach Möglichkeit eindeutige Zugriffstasten zu.** Schreibgeschützte [Textfelder](ctrl-text-boxes.md) sind interaktive Steuerelemente (da Benutzer einen Bildlauf durchführen und Text kopieren können), sodass Sie von Zugriffs Schlüsseln profitieren. **Weisen Sie keinen Zugriffsschlüssel zu:**
    -   **Schaltflächen OK, Abbrechen und schließen.** Enter und ESC werden für Ihre Zugriffsschlüssel verwendet. Weisen Sie jedoch immer einen Zugriffsschlüssel einem Steuerelement zu, das "OK" oder "Abbrechen" bedeutet, aber eine andere Bezeichnung hat.

        ![Screenshot des Dialog Felds "Datei löschen" ](images/win-dialog-box-image13.png)

        In diesem Beispiel ist der Schaltfläche positiver Commit eine Zugriffstaste zugewiesen.

    -   **Gruppen Bezeichnungen.** Normalerweise werden den einzelnen Steuerelementen innerhalb einer Gruppe Zugriffsschlüssel zugewiesen, sodass die Gruppen Bezeichnung keines benötigt. Wenn jedoch ein Mangel an Zugriffs Schlüsseln vorliegt, weisen Sie der Gruppen Bezeichnung einen Zugriffsschlüssel und nicht die einzelnen Steuerelemente zu.
    -   **Allgemeine Hilfe** Schaltflächen, auf die mit F1 zugegriffen wird.
    -   **Link Bezeichnungen.** Es gibt oft zu viele Verknüpfungen, um eindeutige Zugriffsschlüssel zuzuweisen, und die Unterstriche, die häufig verwendet werden, um Verknüpfungen anzugeben, blenden die Zugriffsschlüssel Unterstriche Greifen Sie stattdessen auf Links mit der Tab-Taste zu.
    -   **Registerkarten Namen.** Registerkarten werden mithilfe von STRG + TAB und STRG + UMSCHALT + TAB mithilfe von STRG + UMSCHALTTASTE gedrückt.
    -   **Durchsuchen von Schaltflächen mit der Bezeichnung "...".** Diesen Schaltflächen zum Durchsuchen können keine Zugriffsschlüssel eindeutig zugewiesen werden.
    -   **Nicht beschriftete Steuerelemente,** wie z. b. Dreh Steuerelemente, grafische Befehls Schaltflächen und unbezeichnete Steuerelemente für progressives
    -   **Statischer Text oder Bezeichnungen ohne Bezeichnung für Steuerelemente, die nicht interaktiv sind,** z. b. Status leisten.

-   **Weisen Sie nach Möglichkeit Zugriffsschlüssel für häufig verwendete Befehle gemäß den Standard Zuordnungen für Zugriffsschlüssel zu**. Obwohl konsistente Zugriffsschlüssel Zuweisungen nicht immer möglich sind, werden Sie sicherlich besonders für häufig verwendete Dialogfelder bevorzugt.
-   **Weisen Sie zuerst Zugriffsschlüssel für die Zugriffstaste zu, um sicherzustellen, dass Sie über die Standardschlüssel Zuweisungen verfügen** Wenn keine Standardschlüssel Zuweisung vorhanden ist, verwenden Sie den ersten Buchstaben des ersten Worts. Beispielsweise sollten die Schaltflächen Zugriffsschlüssel für Ja und kein Commit immer "Y" und "N" sein, unabhängig von den anderen Steuerelementen im Dialogfeld.
-   Damit **Zugriffsschlüssel leicht zu finden sind, weisen Sie die Tastenkombinationen einem Zeichen zu, das früh in der Bezeichnung angezeigt wird,** idealerweise das erste Zeichen, auch wenn es ein Schlüsselwort gibt, das später in der Bezeichnung angezeigt wird.
-   **Zeichen mit breiter Breite** (z. b. w, m und Großbuchstaben) bevorzugen.
-   **Bevorzugen Sie einen unverwechselbaren Konsonanten oder einen vowel,** z. b. "x" beim Beenden.
-   **Vermeiden Sie die Verwendung von Zeichen, die die Unterstreichung schwer zu erkennen machen,** wie z. b. (vom problematischsten bis zum geringsten problematischen)
    -   Buchstaben, die nur ein Pixel breit sind, z. b. i und l.
    -   Buchstaben mit Nachfolger, wie z. b. g, j, p, q und y.
    -   Buchstaben neben einem Buchstaben mit einem descender.

Weitere Richtlinien und Beispiele finden Sie unter [Tastatur](inter-keyboard.md).

### <a name="progress-dialogs"></a>Fortschritts Dialogfelder

Nehmen Sie für Aufgaben mit langer Ausführungszeit an, **dass Benutzer etwas anderes ausführen, während die Aufgabe abgeschlossen wird**. Entwerfen Sie den Task für die unbeaufsichtigte Ausführung.

-   **Zeigen Sie Benutzern das Dialogfeld Fortschritts Feedback an, wenn ein Vorgang länger als fünf Sekunden dauert**, und führen Sie einen Befehl aus, um den Vorgang abzubrechen oder zu beenden.
    -   **Ausnahme:** Verwenden Sie für Assistenten und taskflows ein modales Dialogfeld für den Fortschritt nur dann, wenn die Aufgabe auf derselben Seite bleibt (im Gegensatz zur Weiterentwicklung auf eine andere Seite) und die Benutzer während des Wartens keine Aktionen ausführen können. Verwenden Sie andernfalls eine Fortschritts Seite oder einen direkten Fortschritt.
-   Wenn es sich bei dem Vorgang um eine Aufgabe mit langer Ausführungsdauer (über 30 Sekunden) handelt, die im Hintergrund ausgeführt werden kann, verwenden Sie ein nicht modalem Status Dialogfeld, damit Benutzer das Programm weiterhin verwenden können, während Sie warten.
-   Nicht modalfortschritts Dialogfelder:
    -   Klicken Sie auf der Titelleiste auf die Schaltfläche minimieren.
    -   Werden auf der Taskleiste angezeigt.
-   Implementieren Sie nicht modalprogress-Dialogfelder, sodass Sie weiterhin ausgeführt werden, auch wenn das Besitzer Fenster geschlossen wird.

![Screenshot des Dialog Felds "Kopieren" mit Statusanzeige ](images/win-dialog-box-image14.png)

In diesem Beispiel wird die Dateikopie auch dann fortgesetzt, wenn das Besitzer Fenster geschlossen wird.

-   **Stellen Sie eine Befehls Schaltfläche bereit, um den Vorgang anzuhalten, wenn der Vorgang länger als ein paar Sekunden dauert, oder wenn das Potenzial nie fertiggestellt werden kann.** Kennzeichnen Sie die Schaltfläche "Abbrechen", wenn der Abbruch die Umgebung in ihren vorherigen Zustand zurückgibt (ohne Nebeneffekte). Andernfalls bezeichnen Sie die Schaltfläche "Abbrechen", um anzugeben, dass der teilweise abgeschlossene Vorgang unverändert bleibt. Sie können die Schaltflächen Bezeichnung von Abbrechen ändern, um in der Mitte des Vorgangs anzuhalten, wenn es zu einem bestimmten Zeitpunkt nicht möglich ist, die Umgebung in ihren vorherigen Zustand zurückzukehren.

![Screenshot des Dialog Felds mit der Schaltfläche "Abbrechen" ](images/win-dialog-box-image15.png)

In diesem Beispiel hat das Anhalten der Diagnose des Problems keinen Nebeneffekt.

-   **Geben Sie eine Befehls Schaltfläche an, um den Vorgang anzuhalten, wenn er mehr als einige Minuten dauert, und beeinträchtigt die Benutzer Fähigkeit, die Arbeit zu erledigen.** Dadurch wird der Benutzer nicht gezwungen, zwischen dem Abschließen der Aufgabe und dem erledigen ihrer Arbeit auszuwählen.
-   **Sammeln Sie so viele Informationen wie möglich, bevor Sie den Task starten.**
-   **Wenn wiederherstellbare Probleme erkannt werden, können Benutzer alle Probleme behandeln, die am Ende der Aufgabe gefunden wurden.** Wenn dies nicht praktikabel ist, können Benutzer mit Problemen umgehen, sobald sie auftreten.
-   **Verwerfen Sie Aufgaben nicht als Ergebnis BEHEB barer Fehler.**

![Screenshot des Dialog Felds mit der Schaltfläche "erneut versuchen" ](images/win-dialog-box-image16.png)

In diesem Beispiel können Benutzer mithilfe von Windows-Explorer die Aufgabe nach einem BEHEB baren Fehler fortsetzen.

-   **Zeigen Sie Probleme an, indem Sie die Statusanzeige rot aktivieren.**

![Screenshot der Statusanzeige und Schaltfläche "Wiederholen" ](images/win-dialog-box-image17.png)

In diesem Beispiel wurde ein Wechsel Datenträger während einer Dateikopie entfernt.

-   **Wenn die Ergebnisse für die Benutzer deutlich erkennbar sind, schließen Sie das Status Dialogfeld nach erfolgreichem Abschluss automatisch.** Verwenden Sie andernfalls Feedback nur, um Probleme zu melden:
    -   Zum Anzeigen von einfachem Feedback zeigen Sie das Feedback im Status Dialogfeld an, und ändern Sie die Schaltfläche Abbrechen in close.
    -   Um detailliertes Feedback anzuzeigen, schließen Sie das Dialogfeld Fortschritt, und zeigen Sie ein Informations Dialogfeld an.

**Verwenden Sie keine Benachrichtigung zum Abschluss des Feedbacks.** Verwenden Sie entweder ein Status Dialogfeld oder eine [Aktions Erfolgs Benachrichtigung](mess-notif.md), aber nicht beides.

**Verbleibende Zeit**

-   **Verwenden Sie die folgenden Zeitformate.** Beginnen Sie mit dem ersten der folgenden Formate, bei denen die größte Zeiteinheit nicht 0 (null) ist, und wechseln Sie dann zum nächsten Format, sobald die größte Zeiteinheit NULL wird.

**Für Status anzeigen:**

**Wenn verwandte Informationen in einem Doppelpunkt Format angezeigt werden:**

Verbleibende Zeit: h Stunden, m Minuten

Verbleibende Zeit: m Minuten, s Sekunden

Verbleibende Zeit: s Sekunden

**Wenn der Bildschirmbereich eine Premium-Kapazität hat:**

h Std. min. min. min.

m min. Sek. verbleibende Sek.

Verbleibende Sekunden

**Andernfalls:**

h Stunden, m Minuten verbleiben

m Minuten, verbleibende Sekunden

Verbleibende Sekunden

**Für Titelleisten:**

hh: mm Verb leibend

mm: verbleibende SS

0: verbleibende SS

In diesem Compact-Format werden die wichtigsten Informationen zuerst angezeigt, sodass Sie nicht auf der Taskleiste abgeschnitten werden.

-   **Schätzen Sie die Schätzungen, aber geben Sie keine falsche Genauigkeit an.** Wenn die größte Einheit Stunden ist, sollten Sie Minuten (falls sinnvoll), aber keine Sekunden angeben.

**Falsch:**

HH Stunden, mm Minuten, SS Sekunden

-   **Halten Sie die Schätzung auf dem neuesten Stand.** Die verbleibenden Updates verbleiben mindestens alle 5 Sekunden.
-   **Konzentrieren Sie sich auf die verbleibende Zeit** , da es sich dabei um die Informationen handelt, die Benutzern am meisten Geben Sie die gesamte verstrichene Zeit nur dann an, wenn es Szenarien gibt, in denen die verstrichene Zeit hilfreich ist (z. b., wenn die Aufgabe wahrscheinlich Wenn die geschätzte verbleibende Zeit mit einer Statusanzeige verknüpft ist, haben Sie keinen Prozentsatz für vollständigen Text, da diese Informationen von der Statusanzeige selbst übermittelt werden.
-   **Stimmen Sie ab.** Verwenden Sie Singular Einheiten, wenn die Zahl 1 ist.

**Falsch:**

1 Minute, 1 Sekunde

-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**

Weitere Informationen und Beispiele finden Sie unter Status [leisten](progress-bars.md).

### <a name="icons-and-graphics"></a>Symbole und Grafiken

**Grafiken**

-   **Verwenden Sie keine großen Grafiken, die über das Auffüllen von Platz mit Eye Candy hinausgehen.** Behalten Sie stattdessen die Darstellung einfach bei.

**Falsch:**

![Screenshot des Dialog Felds mit einer großen Grafik ](images/win-dialog-box-image18.png)

In diesem Beispiel ist die große Grafik nicht zweckmäßig.

**Symbole der Titelleiste**

-   **Dialog Felder haben keine Symbole für die Titelleiste.**
    -   **Ausnahme:** Wenn ein-Dialogfeld verwendet wird, um ein primäres Fenster (z. b. ein-Hilfsprogramm) zu implementieren und daher auf der Taskleiste angezeigt wird, verfügt es über ein Titelleisten Symbol.

**Textkörper Symbole**

-   **Wählen Sie das Textsymbol basierend auf dem Entwurfsmuster aus:**



|                                      |                                                                                                                            |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| **Muster**<br/>               | **Body-Symbol**<br/>                                                                                                   |
| **Frage Dialogfelder**<br/>      | Programm, Feature, Objekt, Warnsymbol (bei einem möglichen Verlust von Daten oder System Zugriff), Sicherheitswarnung oder keine.<br/> |
| **Auswahl Dialogfelder**<br/>        | Keine.<br/>                                                                                                           |
| **Fortschritts Dialogfelder**<br/>      | Keine (aber möglicherweise eine Animation).<br/>                                                                               |
| **Informations Dialogfelder**<br/> | Keine.<br/>                                                                                                           |



 

-   **Falsch:**

![Screenshot des Dialog Felds mit Warnsymbol ](images/win-dialog-box-image19.png)

In diesem Beispiel wird ein Warnsymbol fälschlicherweise für eine Frage verwendet, die keinen möglichen Datenverlust oder System Zugriff umfasst.

- **Verwenden Sie Symbole, um Benutzer bei der visuellen Erkennung der Programmfunktionen zu unterstützen.** Diese Technik ist am effektivsten, wenn die Symbole leicht erkennbar sind und an verschiedenen Positionen innerhalb des Programms verwendet werden.

![Screenshot des Dialog Felds "Favoriten" mit Stern Symbol ](images/win-dialog-box-image20.png)

In diesem Beispiel stellt das gelbe Stern Symbol Favoriten dar. Das Symbol ist leicht erkennbar und wird in Windows konsistent verwendet, um Favoriten darzustellen.

-   **Verwenden Sie Symbole, um Benutzern zu helfen, das betreffende Objekt zu erkennen.**

![Screenshot des Dialog Felds mit PowerPoint-Symbol ](images/win-dialog-box-image21.png)

In diesem Beispiel unterstützt das Symbol des-Objekts Benutzer dabei, den Typ der Datei zu erkennen, die geöffnet oder gespeichert wird.

-   **Verwenden Sie Symbole, um Features selbsterklärend zu machen.**

![Bilder von Pfeilen, die zeigen, wie Monitor positioniert wird ](images/win-dialog-box-image22.png)

In diesem Beispiel helfen Ihnen diese Symbole dabei, die Auswirkungen ihrer Features zu visualisieren.

-   **Verwenden Sie ein Symbol in Info Feld Dialogfeldern für das Branding von Anwendungen.**

![Screenshot des Info Dialogfelds mit Windows-Logo ](images/win-dialog-box-image23.png)

In diesem Beispiel wird eine Bitmap im Feld Info verwendet, um die Anwendung zu identifizieren und zu kennzeichnen.

**Fußnotiz-Symbole**

-   **Wenn Sie eine fußnotiz haben, können Sie ein Fußnote-Symbol verwenden, um den Betreff der fußnotiz zusammenzufassen.**

![Screenshot des Dialog Felds mit dem Fußnote-Symbol ](images/win-dialog-box-image24.png)

In diesem Beispiel gibt das fußnotiz Symbol an, dass die Frage Auswirkungen auf die Sicherheit hat.

-   **Verwenden Sie kein fußnotiz Symbol, das das Textsymbol wiederholt.**
-   **Verwenden Sie die Fehler-oder Informationsstandard Symbole nicht.** Fehlerbedingungen müssen über das Body-Symbol übermittelt werden, und Fußnoten sind immer für Informationen, sodass das Informationssymbol redundant ist. Sie können jedoch das Symbol Standard Warnung und das gelbe Sicherheitsschild verwenden, um Benutzer über riskante Konsequenzen zu benachrichtigen.

Weitere Informationen und Beispiele finden Sie unter [Symbole](vis-icons.md).

### <a name="commit-buttons"></a>Commit-Schaltflächen

**Hinweise:**

-   Diese Richtlinien gelten nicht für Frage Dialoge mithilfe von Befehls Verknüpfungen, da dieses Muster anstelle von Schaltflächen Befehls Verknüpfungen verwendet.
-   \[Tun Sie dies, \] und \[ machen Sie es nicht \] mit positiven bzw. negativen Antworten zur Haupt Anweisung.

**Allgemein**

-   **Wählen Sie die Schaltflächen "Commit" basierend auf dem Entwurfsmuster aus:**

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td><strong>Muster</strong><br/></td>
    <td><strong>Commit-Schaltflächen</strong><br/></td>
    </tr>
    <tr class="even">
    <td><strong>Frage Dialogfelder (mithilfe von Schaltflächen)</strong><br/></td>
    <td>Einer der folgenden Sätze präziser Befehle: Ja/Nein, Ja/Nein/Abbrechen, [Do it]/Cancel, [Do it]/[do this]/[do this]/[do this]/[Do it]/Cancel.<br/></td>
    </tr>
    <tr class="odd">
    <td><strong>Frage Dialogfelder (mithilfe von links)</strong><br/></td>
    <td>Abbrechen<br/></td>
    </tr>
    <tr class="even">
    <td><strong>Auswahl Dialogfelder</strong><br/></td>
    <td><ul>
    <li>Modale Dialogfelder: OK/Abbrechen oder [Do it]/Cancel</li>
    <li>Nicht modaldialogfelder: Schaltfläche "Schließen" im Dialogfeld und Titelleiste</li>
    <li>Aufgabenbereich: Schaltfläche "Schließen" auf der Titelleiste</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><strong>Fortschritts Dialogfelder</strong><br/></td>
    <td>Verwenden Sie "Abbrechen", wenn die Umgebung in ihren vorherigen Zustand zurückkehrt (ohne Nebeneffekt). Andernfalls verwenden Sie "Abbrechen".<br/></td>
    </tr>
    <tr class="even">
    <td><strong>Informations Dialogfelder</strong><br/></td>
    <td>Fast richtig.<br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   **Alle Commit-Schaltflächen außer Apply führen zum Schließen des Dialogfeld Fensters.**
-   **Bestätigen Sie keine Commit-Schaltflächen.** Unnötigerweise kann sehr lästig sein. **Ausnahmen:**

    -   Die Aktion ist potenziell schwerwiegend.
    -   Die Aktion ist mit anderen Aktionen eindeutig inkonsistent.
    -   Wenn die Aktion nicht korrekt ist, kann dies zu einem erheblichen Verlust von Daten, Zeit oder Aufwand im Namen des Benutzers führen.

    Weitere Richtlinien und Beispiele finden Sie unter [Bestätigungen](mess-confirm.md).

-   **Deaktivieren Sie keine Commit-Schaltflächen. Ausnahmen**
    -   **Wenn Benutzerrechte erhöhen müssen, um eine Änderung vorzunehmen, deaktivieren Sie die Schaltflächen für positives Commit, bis der Benutzer eine Änderung vornimmt.** Dadurch wird verhindert, dass Benutzer nur zum Schließen eines Fensters erweitert werden, indem Sie auf "Abbrechen" klicken.
    -   Weitere Ausnahmen finden Sie unter [deaktivieren oder Entfernen von Steuerelementen im Vergleich zum Erteilen von Fehlermeldungen](#disabling-or-removing-controls-vs-giving-error-messages).
-   **Rechtsbündig ausrichten von Commit-Schaltflächen in einer einzelnen Zeile über den unteren Rand des Dialog Felds,** aber über dem fußnotiz Bereich. Dies geschieht auch, wenn eine einzelne Commit-Schaltfläche (z. b. OK) vorhanden ist.

    **Falsch:**

    ![Screenshot der Nachricht mit zentrierter Schaltfläche "OK" ](images/win-dialog-box-image25.png)

    In diesem Beispiel ist die Schaltfläche OK nicht korrekt zentriert.

-   **Stellen Sie die Commit-Schaltflächen in der folgenden Reihenfolge bereit:**
    1.  OK/ \[ do \] /Yes
    2.  \[Nicht \] /No
    3.  Abbrechen
    4.  Anwenden (falls vorhanden)
    5.  Hilfe (sofern vorhanden)
-   **Wenn Sie über viele Verwandte Commit-Schaltflächen verfügen, konsolidieren Sie diese mithilfe von Trenn** Schaltflächen
-   **Sie haben eine klare Trennung von den Commit-Schaltflächen (die das Fenster schließen) und allen anderen Befehls Schaltflächen (z. b. erweitert).**

**Antworten auf die wichtigsten Anweisungen**

-   **Verwenden Sie positive Commit-Schaltflächen, bei denen es sich um spezifische Antworten auf die main-Anweisung handelt, anstelle von generischen Bezeichnungen wie OK oder Yes/No.** Benutzer sollten in der Lage sein, die Optionen zu verstehen, indem Sie den Schaltflächen Text alleine lesen. **Ausnahmen:**
    -   Verwenden Sie Close für Dialogfelder, die keine Einstellungen haben, z. b. Informations Dialoge. Verwenden Sie für Dialogfelder, die Einstellungen aufweisen, niemals close.
    -   Verwenden Sie OK, wenn die "spezifischen" Antworten immer noch generisch sind, z. b. speichern, auswählen oder auswählen. Verwenden Sie OK, wenn Sie eine bestimmte Einstellung oder eine Sammlung von Einstellungen ändern.
    -   **Für Legacy Dialogfelder ohne main-Anweisung können Sie generische Bezeichnungen wie z. b. OK verwenden.** Häufig sind solche Dialogfelder nicht für die Ausführung einer bestimmten Aufgabe konzipiert und verhindern so spezifischere Antworten.
    -   Bestimmte Aufgaben erfordern eine genauere und sorgfältige Lektüre von Benutzern, um fundierte Entscheidungen treffen zu können. Dies ist normalerweise die Groß-/Kleinschreibung bei [Bestätigungen](mess-confirm.md). **In solchen Fällen können Sie generische Commit-Schaltflächen Bezeichnungen absichtlich verwenden, um Benutzer zu zwingen, die Haupt Anweisungen zu lesen und übereilte Entscheidungen zu verhindern.**

        **Richtig:**

        ![Screenshot der Meldung mit den Schaltflächen "Ja" und "Nein"](images/win-dialog-box-image26.png)

        In diesem Beispiel zwingt die Verwendung von Ja/Nein-Commit-Schaltflächen, dass Benutzer mindestens die main-Anweisung lesen.

-   **Sie können das Wort "sowieso" auch der Schaltfläche "positive Commit-Schaltfläche" hinzufügen, um anzugeben, dass das Dialogfeld einen Grund** für das Fortsetzen des Vorgangs anzeigt und dass Benutzer das Dialogfeld sorgfältig lesen sollten, bevor Sie fortfahren

    **Richtig:**

    ![Screenshot der Schaltfläche "Meldung und Deinstallation" ](images/win-dialog-box-image27.png)

    In diesem Beispiel wird "sowieso" der Bezeichnung "Commit-Schaltfläche" hinzugefügt, um anzugeben, dass Benutzer sorgfältig vorgehen sollten.

-   **Verwenden Sie "Abbrechen" oder "Schließen" für negative Commit-Schaltflächen anstelle spezifischer Antworten auf die Haupt Anweisung.** Häufig bemerken Benutzer, dass Sie keine Aufgabe ausführen möchten, wenn ein Dialogfeld angezeigt wird. Wenn "Abbrechen" oder "Schließen" an bestimmte Antworten zurückkehrt, müssten die Benutzer alle Commit-Schaltflächen sorgfältig lesen, um zu bestimmen, wie die Kündigung abgebrochen werden soll. **Wenn Sie "Abbrechen" und "Schließen" durchgängig bezeichnen, machen Sie diese Ausnahmen**
    -   **Verwenden Sie Yes/Cancel nicht.** Verwenden Sie immer Yes/No als Paar.
    -   **Verwenden Sie eine bestimmte Antwort, wenn "Abbrechen" mehrdeutig ist.**
-   **Ordnen Sie mit Text im Inhalts Bereich keine generischen Bezeichnungen ihrer speziellen Bedeutung zu.** Verwenden Sie stattdessen bestimmte Commit-Schaltflächen Bezeichnungen oder ein Frage Dialogfeld mithilfe von Links, wenn die Bezeichnungen lang sind.

    **Falsch:**

    ![Screenshot der Nachricht mit unklarer Verwendung von Schaltflächen ](images/win-dialog-box-image28.png)

    In diesem Beispiel ist OK zugeordnet, um den Vorgang fortzusetzen, wenn der Vorgang auf der Seite beibehalten wird.

**Schaltflächen Ja und Nein**

-   **Bevorzugen Sie bestimmte Antworten auf Schaltflächen Ja und Nein.** Obwohl es keine Probleme mit der Verwendung von "Ja" und "Nein" gibt, können bestimmte Antworten schneller interpretiert werden, was zu einer effizienten Entscheidungsfindung führt. Allerdings haben [Bestätigungen](mess-confirm.md) in der Regel ja und keine Schaltflächen, um Benutzern [die Bestätigung vor](mess-confirm.md) der Reaktion zu geben.
-   **Verwenden Sie die Schaltflächen Ja und Nein, um auf Ja oder keine Fragen zu antworten.** Die Haupt Anweisung sollte natürlich als Ja oder keine Frage ausgedrückt werden. Verwenden Sie niemals OK und Abbrechen für Ja oder keine Fragen.

    **Falsch:**

    ![Screenshot, der eine Meldung mit "OK" für eine ja-keine Frage anzeigt.](images/win-dialog-box-image29.png)

    **Richtig:**

    ![Screenshot der Nachricht mit ja für dieselbe Frage ](images/win-dialog-box-image30.png)

    **Besserer**

    ![Screenshot der Nachricht mit der gleichen Frage ](images/win-dialog-box-image31.png)

    In diesen Beispielen sind "yes" und "No" gute Antworten auf "yes" und "No", aber auch bestimmte Antworten sind noch besser.

-   **Sie sollten die main-Anweisung als Ja oder gar keine Frage formulieren, wenn sich die Commit-Schaltflächen mit spezifischer Formulierung als lang oder umständlich erweisen.** Alternativ dazu können Sie Befehls Verknüpfungen für längere Antworten (fünf Wörter oder mehr) für die main-Anweisung verwenden.

    **Falsch:**

    ![Screenshot der Nachricht mit den Schaltflächen Bezeichnungen für "Verfassen" ](images/win-dialog-box-image32.png)

    **Richtig:**

    ![Screenshot der Nachricht mit "Ja/Nein"-Schaltflächen Bezeichnungen ](images/win-dialog-box-image33.png)

    Der spezifische Ausdruck im falschen Beispiel ist zu lang. im richtigen Beispiel wird also "yes" und "No" verwendet.

-   **Verwenden Sie nicht die Schaltflächen Ja und Nein, wenn die Bedeutung der No-Antwort unklar ist.** Wenn dies der Fall ist, verwenden Sie stattdessen bestimmte Antworten.

**OK-Schaltflächen**

-   **Klicken Sie in modalen Dialogfeldern auf OK, um die Werte zu übernehmen, die Aufgabe auszuführen und das Fenster zu schließen.**
-   **Verwenden Sie keine OK-Schaltflächen, um auf Fragen zu antworten.**
-   **Weisen Sie den Zugriffsschlüssel nicht zu OK zu, da Enter der Zugriffsschlüssel für die Standard Schaltfläche ist.** Dadurch können die anderen Zugriffsschlüssel leichter zugewiesen werden.
-   **Ordnungsgemäße Bezeichnung für OK.** Die Schaltfläche OK sollte mit OK, nicht OK oder okay gekennzeichnet werden.
-   **Verwenden Sie keine OK-Schaltflächen für Fehler oder Warnungen.** Probleme sind nie in Ordnung. Verwenden Sie stattdessen close.

    **Falsch:**

    ![Screenshot der Meldung mit der Schaltfläche "OK" ](images/win-dialog-box-image34.png)

    In diesem Beispiel sollte Close anstelle von OK verwendet werden.

-   **Verwenden Sie keine OK-Schaltflächen in nicht modalem Dialogfeldern.** Stattdessen sollten nicht modaldialoge aufgabenspezifische Commit-Schaltflächen (z. b. suchen) verwenden. Einige nicht modante Dialogfelder erfordern jedoch nur eine Schaltfläche "Schließen".

**Schaltflächen Abbrechen**

-   **Wenn Sie auf Abbrechen klicken, werden alle Änderungen verworfen, die Aufgabe abgebrochen, das Fenster wird geschlossen, und die Umgebung wird in den vorherigen Zustand zurückversetzt, ohne dass Nebeneffekte angezeigt werden.** Wenn Sie im Dialogfeld für die Auswahl von schetwahl auf Abbrechen klicken, werden im Dialogfeld Besitzer Auswahl alle Änderungen, die von den Dialogfeldern mit den eigenen Wahlmöglichkeiten
-   **Geben Sie eine Schaltfläche Abbrechen an, damit Benutzer Änderungen explizit verwerfen können.** Dialog Felder benötigen einen unklaren Beendigungs Punkt. Verlassen Sie sich nicht darauf, dass Benutzer die Schaltfläche Schließen auf der Titelleiste finden.

    -   **Ausnahme:** Geben Sie keine Abbruch Schaltfläche für Dialogfelder ohne Einstellungen an. Die Schaltflächen OK und schließen haben in diesem Fall denselben Effekt wie abbrechen.

    **Falsch:**

    ![Screenshot der Meldung mit der Schaltfläche "OK" ](images/win-dialog-box-image35.png)

    Wenn in diesem Beispiel nur die Schaltfläche Schließen auf der Titelleiste angezeigt wird, wird Sie so angezeigt, als ob die Benutzer keine Auswahl haben.

-   **Verwenden Sie die Schaltflächen Abbrechen nicht, um auf Fragen zu antworten.**

    **Falsch:**

    ![Screenshot der Nachricht mit "OK" für "yes" (keine Frage) ](images/win-dialog-box-image36.png)

    In diesem Beispiel werden "OK" und "Abbrechen" fälschlicherweise verwendet, um auf eine Ja-oder Nein-Frage zu antworten.

-   **Weisen Sie keine Zugriffsschlüssel zu, die abgebrochen werden, da ESC der Zugriffsschlüssel ist.** Dadurch können die anderen Zugriffsschlüssel leichter zugewiesen werden.
-   **Verwenden Sie nicht die Schaltflächen Abbrechen in nicht modalem Dialogfeldern.** Verwenden Sie stattdessen close.
-   **Deaktivieren Sie die Schaltfläche Abbrechen nicht.** Benutzer sollten immer in der Lage sein, Dialogfelder abzubrechen.
    -   **Ausnahme:** Sie können die Schaltfläche Abbrechen in einem Fortschritts Dialogfeld deaktivieren, wenn ein Zeitraum vorliegt, in dem der Vorgang nicht abgebrochen werden kann. Eine bessere Lösung besteht jedoch darin, solche Vorgänge so zu entwerfen, dass Sie immer abgebrochen werden können.

**Schließen von Schaltflächen**

-   **Verwenden Sie schließen-Schaltflächen für nicht modale Dialogfelder sowie modale Dialogfelder, die nicht abgebrochen werden können.**
-   **Wenn Sie auf Schließen klicken, schließen Sie das Dialogfeld Fenster, sodass alle vorhandenen Nebeneffekte bestehen.** Verwenden Sie done nicht, da es sich nicht um eine imperative Konstruktion handelt. Wenn Sie auf Schließen im Dialogfeld für die Auswahl von untersuchen klicken, werden alle Änderungen, die im Dialogfeld Besitzer Auswahl vorgenommen werden, beibehalten.
-   **Fügen Sie im Dialogfeld Text eine explizite Schaltfläche schließen ein.** Dialog Felder benötigen einen unklaren Beendigungs Punkt. Verlassen Sie sich nicht darauf, dass Benutzer die Schaltfläche Schließen auf der Titelleiste finden.
-   **Stellen Sie sicher, dass die Schaltfläche Schließen auf der Titelleiste dieselbe Auswirkung hat wie abbrechen oder schließen.**
-   **Weisen Sie die Tastenkombination nicht zu, da ESC die Zugriffstaste ist.** Dadurch können die anderen Zugriffsschlüssel leichter zugewiesen werden.

**Schaltflächen anwenden**

-   **Verwenden Sie keine Schaltflächen anwenden in Dialogfeldern, die keine Eigenschaften Blätter oder Steuerelemente sind.** Die Schaltfläche anwenden bedeutet, dass die ausstehenden Änderungen übernommen werden, das Fenster jedoch geöffnet lassen. Auf diese Weise können Benutzer die Änderungen auswerten, bevor Sie das Fenster schließen. Dies ist jedoch nur für Eigenschaften Blätter und Steuerelemente erforderlich.

    **Falsch:**

    ![Screenshot des Dialog Felds mit der Schaltfläche "anwenden" ](images/win-dialog-box-image37.png)

    In diesem Beispiel verfügt das Dialogfeld "Auswahl" unnötig über eine Schaltfläche "anwenden".

**Commit-Schaltflächen für indirekte Dialogfelder**

**Hinweis:** Indirekte Dialogfelder werden außerhalb des Kontexts angezeigt, entweder als indirektes Ergebnis einer Aufgabe oder als Ergebnis eines Problems mit einem System-oder Hintergrundprozess. In indirekten Dialogfeldern ist die Schaltfläche "Abbrechen" mehrdeutig, da Sie den Dialog abbrechen oder die gesamte Aufgabe abbrechen könnte.

-   **Wenn Benutzer das Dialogfeld und den Task abbrechen müssen, müssen Sie für beide Commit-Schaltflächen verwenden.** Bezeichnen Sie die Schaltfläche, mit der das Dialogfeld mit einer negativen Antwort auf die main-Anweisung abgebrochen wird. Bezeichnen Sie die Schaltfläche, mit der die gesamte Aufgabe abgebrochen wird. Wenn Sie Abbrechen verwenden, kann das Dialogfeld in vielen Kontexten verwendet werden.

    **Richtig:**

    ![Screenshot des Dialog Felds mit speichern/nicht speichern ](images/win-dialog-box-image38.png)

    In diesem Beispiel wird dieses Dialogfeld von Windows Paint als Ergebnis eines New-oder Exit-Befehls angezeigt, wenn die Grafik nicht gespeichert wurde. Nicht speichern schließt das Dialogfeld, ohne zu speichern, während Abbrechen den New-oder Exit-Befehl abbricht.

    **Falsch:**

    ![Screenshot des Dialog Felds mit Ja/Nein-Schaltflächen ](images/win-dialog-box-image39.png)

    In diesem Beispiel gibt es keine Möglichkeit, die Aufgabe abzubrechen (schließende Office-Verknüpfungs Leiste), die dazu geführt hat, dass dieses Dialogfeld angezeigt wird. Dieses Dialogfeld benötigt eine Schaltfläche "Abbrechen".

-   **Wenn Benutzer nur das Dialogfeld abbrechen müssen, aber nicht die Aufgabe, verwenden Sie eine Schaltfläche mit einer bestimmten, negativen Antwort auf die Haupt Anweisung** und verfügen nicht über eine Schaltfläche "Abbrechen".

    ![Screenshot des Dialog Felds mit "ausführen/nicht ausführen" ](images/win-dialog-box-image24.png)

    In diesem Beispiel wird dieses Dialogfeld indirekt als Ergebnis der Navigation zu einer Webseite angezeigt, auf der ein ActiveX-Steuerelement installiert ist. Die Verwendung von "Abbrechen" wäre hier nicht eindeutig, daher wird stattdessen nicht "Run" verwendet.

Weitere Informationen und Beispiele finden Sie unter [Befehls](ctrl-command-buttons.md)Schaltflächen.

### <a name="command-links"></a>Befehls Verknüpfungen

-   **Stellen Sie mithilfe von Befehls Verknüpfungen eine Reihe langer Befehle anstelle von Befehls Schaltflächen oder einer Kombination aus Options Feldern und der Schaltfläche OK dar.** Auf diese Weise können Benutzer mit einem einzigen Mausklick Antworten. Diese Vorgehensweise kann jedoch nur für eine einzige Frage verwendet werden.
-   **Präsentieren Sie zuerst die am häufigsten verwendeten Befehls Verknüpfungen.** Die resultierende Reihenfolge sollte ungefähr der Wahrscheinlichkeit der Verwendung, aber auch eines logischen Flows entsprechen.
    -   **Ausnahme:** Befehls Verknüpfungen, die zu allen Aufgaben führen, sollten zuerst platziert werden.
-   Wenn für einen Befehls Link eine weitere Erläuterung erforderlich ist, sollten Sie **eine zusätzliche Erläuterung angeben.** Ergänzende Erläuterungen beschreiben, warum Benutzer den Befehl auswählen können oder was geschieht, wenn der Befehl ausgewählt wird.
-   **Verwenden Sie keine ergänzenden Erklärungen, bei denen es sich um reanweisungen des Befehls Links handelt.** Verwenden Sie eine ergänzende Erläuterung nur dann, wenn Sie keinen Befehls Link selbsterklärend erstellen können. Das Bereitstellen einer ergänzenden Erklärung für einen Befehls Link bedeutet nicht, dass Sie Sie für alle Befehle bereitstellen müssen.

![Screenshot des Dialog Felds mit Optionen zum Anzeigen von Text ](images/win-dialog-box-image40.png)

In diesem Beispiel werden in der ergänzenden Erläuterung die Auswirkungen einer der Optionen beschrieben.

-   **Verwenden Sie Ausdrücke, die mit einem Verb beginnen, ohne das Beenden der Interpunktions Zeichen.**
-   **Wenn ein Befehl dringend empfohlen wird, sollten Sie "(empfohlen)" der Bezeichnung hinzufügen.** Stellen Sie sicher, dass Sie der Link Bezeichnung und nicht der ergänzenden Erläuterung hinzufügen.
-   **Wenn ein Befehl nur für fortgeschrittene Benutzer vorgesehen ist, sollten Sie der Bezeichnung "(Advanced)" hinzufügen.** Stellen Sie sicher, dass Sie der Link Bezeichnung und nicht der ergänzenden Erläuterung hinzufügen.
-   **Geben Sie immer eine explizite Schaltfläche Abbrechen an**. Verwenden Sie für diesen Zweck keinen Befehls Link.

**Falsch:**

![Screenshot des Dialog Felds mit dem Link "nicht beenden" ](images/win-dialog-box-image41.png)

In diesem Beispiel verwendet das Dialogfeld anstelle einer Schaltfläche Abbrechen einen Befehls Link.

Weitere Informationen und Beispiele finden Sie unter [Befehls Verknüpfungen](ctrl-command-links.md).

### <a name="dont-show-this-item-again"></a>Nicht anzeigen <item> erneut

-   **Verwenden Sie <item> die Option Diese Option nicht mehr anzeigen, um Benutzern das Unterdrücken eines wiederkehrenden Dialog Felds zu gestatten, wenn es keine bessere Alternative gibt.** Es ist immer besser, das Dialogfeld anzuzeigen, wenn Benutzer es wirklich benötigen, oder es einfach auszuschließen, wenn dies nicht der Fall ist.
-   **Verwenden Sie diesen speziellen Ausdruck, <item> der durch das jeweilige Element ersetzt wird.** Diese Erinnerung beispielsweise nicht mehr anzeigen. Wenn Sie auf ein Dialogfeld im Allgemeinen verweisen, verwenden Sie diese Meldung nicht mehr anzeigen.
-   **Geben Sie eindeutig an, wenn Benutzereingaben für künftige Standardwerte verwendet** werden, indem Sie den folgenden Satz unter der Option hinzufügen: Ihre Auswahl wird in Zukunft standardmäßig verwendet.
-   **Wählen Sie die Option nicht standardmäßig aus. Wenn das Dialogfeld wirklich nur einmal angezeigt werden soll, sollten Sie dies tun, ohne zu Fragen.** Verwenden Sie diese Option nicht als Ausrede, um Benutzer zu ärgern, dass das Standardverhalten nicht lästig ist.

**Falsch:**

![Screenshot der Nachricht, die unnötige Fragen gestellt hat ](images/win-dialog-box-image42.png)

In diesem Beispiel sollte die Nachricht nur einmal angezeigt werden. Sie müssen nicht Fragen.

-   **Legen Sie die Einstellung auf Benutzerbasis dauerhaft fest.**
-   **Wenn Benutzer die Option auswählen und auf Abbrechen klicken, wird diese Option wirksam.** Diese Einstellung ist eine Meta-Option, sodass Sie nicht dem standardmäßigen Abbruch Verhalten entspricht, bei dem kein Nebeneffekt besteht. Beachten Sie, dass Benutzer, die das Dialogfeld in Zukunft nicht sehen möchten, wahrscheinlich auch abbrechen möchten.
-   Wenn Benutzer diese Dialogfelder möglicherweise wiederherstellen müssen, geben Sie im Dialogfeld Optionen des Programms einen Befehl zum **Wiederherstellen von Nachrichten** an.

### <a name="ask-me-later"></a>Später nachfragen

-   Geben Sie diese Option an, um ein Dialogfeld nur zu schließen, wenn:
    -   **Das Dialogfeld ist indirekt**, sodass sich Benutzer wahrscheinlich auf eine andere Aufgabe konzentrieren können.
    -   **Benutzer müssen Antworten, aber nicht sofort**, damit Sie Ihre Arbeit fortsetzen können.
    -   **Die Frage ist ausreichend gedacht oder Aufwand** , damit Benutzer bessere Entscheidungen treffen können, wenn Sie mehr Zeit benötigen.
    -   **Das Dialogfeld oder die Option wird automatisch später** angezeigt (sodass Benutzer wirklich später gefragt werden).
-   **Falsch:**
-   ![Screenshot der Meldung mit der Option "Ask Me Later" ](images/win-dialog-box-image43.png)
-   In diesem Beispiel ist die Frage so einfach, dass Sie durch das Hinzufügen einer "Ask Me Later"-Option nur erschwert wird.
-   Andernfalls erwarten Benutzer, dass Sie jetzt reagieren, aber Sie können das Dialogfeld in der Regel mit "Abbrechen" oder "Schließen" schließen. Bei ordnungsgemäßer Verwendung sollte diese Option nur selten vorkommen.

### <a name="morefewer"></a>Mehr/weniger

-   **Verwenden Sie mehr oder weniger Progressive Offenlegungs Schaltflächen, um erweiterte oder selten verwendete Optionen, Befehle oder Details, die Ziel Benutzer in der Regel nicht benötigen, anzuzeigen oder auszublenden.** Dadurch wird das Dialogfeld für die typische Verwendung vereinfacht. Blenden Sie häufig verwendete Optionen, Befehle oder Informationen nicht aus, da Sie von Benutzern möglicherweise nicht gefunden werden.

![Screenshot des Dialog Felds mit der Schaltfläche "Weitere Optionen" ](images/win-dialog-box-image24.png)

In diesem Beispiel sind selten verwendete Optionen standardmäßig ausgeblendet.

-   **Verwenden Sie nicht mehr oder weniger Steuerelemente, es sei denn, es werden wirklich weitere Details angezeigt.** Geben Sie die gleichen Informationen nicht nur in einem anderen Format zurück.
-   **Verwenden Sie nicht mehr oder weniger Steuerelemente, um die Hilfe anzuzeigen.** Verwenden Sie stattdessen Hilfe Verknüpfungen oder Fußnoten.
-   **Vermeiden Sie mit Aufgaben Dialogfeldern das Kombinieren von mehr oder weniger Steuerelementen, und zeigen Sie dies <item> nicht mehr** Diese Kombination hat ein unangenehmes Erscheinungsbild.
-   Informationen zu Bezeichnungs Richtlinien finden Sie unter [Progressive Offenlegung](ctrl-progressive-disclosure-controls.md).

### <a name="footnotes"></a>Fußnoten

-   **Verwenden Sie Fußnoten für Informationen, die für den Zweck eines Dialog Felds nicht von Bedeutung sind, aber auch für Benutzer hilfreich sind, um Entscheidungen zu treffen.** Die meisten Benutzer sollten in der Lage sein, Fußnoten zu überspringen und in ihrer Reaktion auf das Dialogfeld weiterhin informierte Entscheidungen zu treffen.

![Screenshot des Dialog Felds mit einer Verdeutlichung Fußnote ](images/win-dialog-box-image44.png)

In diesem Beispiel sind die fußnotiz-Informationen ergänzend, nicht erforderlich.

### <a name="disabling-or-removing-controls-vs-giving-error-messages"></a>Deaktivieren oder Entfernen von Steuerelementen im Vergleich zu Fehlermeldungen

-   Wenn ein Steuerelement nicht im aktuellen Kontext angewendet wird, sollten Sie die folgenden Optionen berücksichtigen:
    -   **Entfernen Sie das-Steuerelement, wenn Benutzer es nicht aktivieren können, oder wenn Benutzer nicht erwarten, dass es angewendet wird und sich der Status nicht häufig ändert.** Dadurch wird das Dialogfeld vereinfacht, und Benutzer werden es nicht übersehen. Wenn ein Steuerelement häufig angezeigt und ausgeblendet wird, ist dies lästig.
    -   **Deaktivieren Sie das Steuerelement, wenn Benutzer erwarten, dass es angewendet wird oder sich der Status häufig ändert, und Benutzer können leicht ableiten, warum das Steuerelement deaktiviert ist.** Ein Beispiel für eine einfache Ableitung ist die Deaktivierung einer Commit-Schaltfläche, wenn ein einzelnes, leeres Textfeld vorhanden ist, das eine Eingabe erfordert. Sie können [Luftballons](ctrl-balloons.md) verwenden, um nicht kritische Benutzereingabe Probleme mit Textfeldern und bearbeitbaren Dropdown Listen anzuzeigen. Wenn das Problem jedoch nicht durch eine Sprechblase oder mehrere Steuerelemente erläutert werden kann, wäre die Ableitung nicht mehr einfach.
    -   **Andernfalls lassen Sie das Steuerelement aktiviert, übergeben Sie jedoch eine Fehlermeldung, wenn es falsch verwendet wird.** Wenn Sie in diesem Fall eine Deaktivierung durchführen, können Benutzer die Gründe für die Deaktivierung des Steuer Elements nicht verstehen. Benutzer werden gezwungen, das Problem durch Experimentieren und deduktive Logik zu ermitteln. Es ist besser, nur eine hilfreiche Fehlermeldung bereitzustellen, um das Problem explizit zu erläutern.
-   **Tipp:** Wenn Sie nicht sicher sind, ob Sie ein Steuerelement deaktivieren oder eine Fehlermeldung abgeben sollten, erstellen Sie zunächst die Fehlermeldung, die Sie möglicherweise erhalten. Wenn die Fehlermeldung hilfreiche Informationen enthält, die Ziel Benutzer wahrscheinlich nicht schnell ableiten, lassen Sie das Steuerelement aktiviert, und übergeben Sie den Fehler. Andernfalls deaktivieren Sie das Steuerelement.
-   **Wenn Sie ein Steuerelement deaktivieren, deaktivieren Sie auch alle zugeordneten Steuerelemente**, z. b. die Bezeichnung, zusätzliche Erläuterungen oder Befehls Schaltflächen. Deaktivieren Sie jedoch die [Gruppen Felder](ctrl-group-boxes.md), die Gruppen Bezeichnung oder die Gruppen Erklärung, falls vorhanden.

![Screenshot des Dialog Felds mit Abbild-Steuerelementen ](images/win-dialog-box-image45.png)

In diesem Beispiel werden die deaktivierten Textfeld-Bezeichnungen ebenfalls deaktiviert, deren Gruppen Bezeichnung und Gruppen Erklärung jedoch nicht.

### <a name="required-input"></a>Erforderliche Eingabe

-   Beachten Sie die folgenden Optionen, um anzugeben, dass Benutzerinformationen in einem-Steuerelement bereitstellen müssen:
    -   **Geben Sie nichts an, aber behandeln Sie fehlende erforderliche Eingaben mit Fehlermeldungen.** Diese Vorgehensweise verringert die Übersichtlichkeit und funktioniert gut, wenn die meisten Eingaben optional sind oder wenn die Benutzer wahrscheinlich keine Steuerelemente überspringen und so die Anzahl der Fehlermeldungen niedrig halten.
    -   **Geben Sie die erforderliche Eingabe mithilfe eines Sternchen am Anfang der Bezeichnung an.** Erläutern Sie das Sternchen mithilfe von:

        -   Eine Fußnote am unteren Rand des Inhalts Bereichs, in der die \* erforderliche Eingabe angegeben ist.
        -   Eine QuickInfo für das Sternchen, das die erforderliche Eingabe anzeigt.

        Diese Vorgehensweise funktioniert gut, wenn es nicht viele erforderliche Steuerelemente gibt, aber schlecht, wenn die meisten Steuerelemente erforderlich sind.

        ![Screenshot der Text Feld Bezeichnungen mit Sternchen ](images/win-dialog-box-image46.png)

        In diesem Beispiel werden Sternchen verwendet, um die erforderliche Eingabe anzugeben.

    -   **Wenn alle Steuerelemente Eingaben erfordern, geben Sie "alle Eingaben erforderlich" an geeigneter Stelle am oberen Rand des Inhalts Bereichs ein.** Bei diesem Ansatz wird die Übersichtlichkeit für diesen speziellen Fall reduziert.
    -   **Geben Sie optionale Eingaben mit "(optional)" nach der Bezeichnung an.** Diese Vorgehensweise funktioniert gut, wenn die meisten Eingaben erforderlich sind, andernfalls aber nicht.

-   **Verwenden Sie aus Gründen der Konsistenz die gleiche Methode, um die erforderliche Eingabe im gesamten Programm anzugeben.** Geben Sie insbesondere die erforderliche oder optionale Eingabe nach Bedarf an, aber vermeiden Sie, beide innerhalb desselben Programms zu verwenden.

### <a name="error-handling"></a>Fehlerbehandlung

-   Verhindern von Fehlern mithilfe von Steuerelementen, die auf gültige Benutzereingaben beschränkt sind. Sie können auch helfen, die Anzahl der Fehler zu verringern, indem Sie angemessene Standardwerte bereitstellen.
-   Überprüfen Sie die Benutzereingaben so bald wie möglich, und zeigen Sie die Fehler so nah wie möglich an der Eingabe an.
-   **Verwenden Sie bei Problemen mit der nicht modalem Fehler (direkte Fehler oder Luftballons) für Probleme bei der Benutzereingabe.**
    -   **Verwenden Sie für nicht kritische einpunktbenutzer-Eingabe Probleme, die bei einem Textfeld erkannt werden, oder unmittelbar nachdem ein Textfeld den Fokus verliert.** Für Luftballons ist kein verfügbarer Bildschirmbereich oder das dynamische Layout erforderlich, das zum Anzeigen von direkten Nachrichten erforderlich ist. Zeigen Sie jeweils nur eine Sprechblase an. Da das Problem nicht entscheidend ist, ist kein Fehler Symbol erforderlich. Beim Klicken auf das Problem, wenn das Problem behoben ist oder nach einem Timeout, werden die Ballons entfernt.

        ![Screenshot der Meldung "falsches Zeichen" ](images/win-dialog-box-image47.png)

        In diesem Beispiel gibt eine Sprechblase ein Eingabeproblem an, während Sie sich noch im-Steuerelement befinden.

-   Verwenden Sie direkte Fehler bei der **Erkennung verzögerter Fehler**, normalerweise durch Klicken auf die Schaltfläche Commit gefundene Fehler. (Verwenden Sie keine direkten Fehler für Einstellungen, für die sofort ein Commit ausgeführt wird.) Es können mehrere direkte Fehler gleichzeitig vorhanden sein. Verwenden Sie den normalen Text und ein 16x16-Pixel-Fehler Symbol, und platzieren Sie diese direkt neben dem Problem, wenn dies möglich ist. Direkte Fehler werden nicht entfernt, es sei denn, der Benutzer führt einen Commit aus, und es werden keine weiteren Fehler gefunden.

    ![Screenshot des Dialog Felds mit zwei Fehlermeldungen ](images/win-dialog-box-image48.png)

    In diesem Beispiel wird ein direkter Fehler für einen Fehler verwendet, der durch Klicken auf die Schaltfläche Commit gefunden wurde.

-   **Verwenden Sie die modale Fehlerbehandlung (Aufgaben Dialogfelder oder Meldungs Felder) für alle anderen Probleme,** einschließlich Fehlern, die mehrere Steuerelemente betreffen, oder nicht kontextabhängige oder nicht-Eingabefehler durch Klicken auf die Schaltfläche Commit.
-   **Wenn ein Eingabeproblem gefunden und gemeldet wird, legen Sie den Eingabefokus auf das erste Steuerelement mit den falschen Daten fest.** Scrollen Sie ggf. in das Steuerelement.

Weitere Informationen und Beispiele finden Sie unter [Fehlermeldungen](mess-error.md) und [Luftballons](ctrl-balloons.md).

### <a name="help"></a>Hilfe

-   Beachten Sie bei der Bereitstellung von Benutzerunterstützung die folgenden Optionen (in Ihrer bevorzugten Reihenfolge aufgelistet):
    -   Teilen Sie den interaktiven Steuerelementen selbsterklärende Bezeichnungen mit. Benutzer sind eher mit der Wahrscheinlichkeit vertraut, dass Sie die Bezeichnungen für interaktive Steuerelemente lesen als bei anderen Text.
    -   Stellen Sie mithilfe [statischer Text Bezeichnungen](text-ui.md)Kontext gesteuerte Erläuterungen bereit.
    -   Geben Sie einen bestimmten Hilfelink zu einem relevanten Hilfethema an.
-   **Suchen Sie Links im Inhalts Bereich des Dialog Felds nach Hilfe Links.** Wenn das Dialogfeld eine fußnotiz enthält und der Hilfelink darauf bezogen ist, platzieren Sie den Hilfelink in der Fußnote.

    ![Screenshot des Dialog Felds mit Hilfe Verknüpfung ](images/win-dialog-box-image40.png)

    In diesem Beispiel bezieht sich der Hilfelink auf das gesamte Dialogfeld.

    -   **Ausnahme:** Wenn ein Dialogfeld mehrere verschiedene Gruppen von Einstellungen mit separaten Hilfe Themen enthält (z. u. in Gruppen Feldern), suchen Sie die Hilfe Links unten in den Gruppen.

-   **Verwenden Sie keine allgemeinen oder ungenauen Hilfe Themen Links oder allgemeine Hilfe Schaltflächen.** Benutzer ignorieren häufig die generische Hilfe.

Weitere Informationen und Beispiele finden Sie in der [Hilfe](winenv-help.md).

### <a name="default-values"></a>Standardwerte

-   Fügen Sie in jedem Dialogfeld eine standardmäßige Commit-Schaltfläche ein.
-   Für Frage Dialoge:
    -   **Wählen Sie das sicherste (um den Verlust von Daten oder den System Zugriff zu vermeiden) und die sicherste Antwort als Standard.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequeme Antwort aus.
        -   **Ausnahme:** Nehmen Sie keine destruktive Reaktion auf den Standardwert vor, es sei denn, es gibt eine einfache, offensichtliche Möglichkeit, um den Befehl
-   For Choice-Dialogfelder:
    -   Wählen Sie für die anfänglichen Standardwerte **das sicherste (um den Verlust von Daten oder den System Zugriff zu vermeiden) und die sichersten Werte für jedes Steuer** Element aus. Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichsten oder bequemsten Optionen aus.
    -   Wählen Sie für die nachfolgenden Standardwerte **die zuvor ausgewählten Optionen erneut aus, wenn diese Werte wahrscheinlich wiederholt werden. Dies ist sicher und sicher.** Wählen Sie andernfalls die anfänglichen Standardwerte aus.

![Screenshot des Druck Dialogfelds ](images/win-dialog-box-image49.png)

In diesem Beispiel haben Benutzer wahrscheinlich dieselben Druckeinstellungen wie bei der letzten Änderung. Allerdings wird die Anzahl der gewünschten Kopien wahrscheinlich geändert, sodass diese Einstellung nicht erneut ausgewählt wird.

## <a name="recommended-sizing-and-spacing&quot;></a>Empfohlene Größe und Abstände

-   **Unterstützung der minimalen Windows Vista-Bildschirmauflösung von 800 x 600 Pixeln.** Layouts können mithilfe einer Bildschirmauflösung von 1024 x 768 Pixel für Fenster mit Größenänderung optimiert werden.
-   **Verwenden Sie nach Möglichkeit die Größe der Fenstergröße, um Scrollleisten und abgeschnittene Daten zu vermeiden.** Fenster mit dynamischen Inhalten und Listen profitieren am meisten von Fenstern mit Größenänderung.
-   **Fenster mit fester Größe müssen vollständig sichtbar und Größe aufweisen, damit Sie in den Arbeitsbereich passen.**
-   **Fenster mit Größenänderung können für eine höhere Auflösung optimiert werden, bei Bedarf aber zur Anzeigezeit auf die tatsächliche Bildschirmauflösung.**
-   **Wählen Sie eine Standardfenster Größe aus, die für den Inhalt geeignet ist.** Achten Sie darauf, größere anfängliche Fenstergrößen zu verwenden, wenn Sie den Raum effektiv verwenden können.

## <a name=&quot;text&quot;></a>Text

### <a name=&quot;general&quot;></a>Allgemein

-   **Entfernen Sie den redundanten Text.** Suchen Sie nach redundantem Text in Titeln, Haupt Anweisungen, ergänzenden Anweisungen, Inhalts Bereichen, Befehls Verknüpfungen und Commit-Schaltflächen. Im Allgemeinen sollten Sie voll Text in Anweisungen und interaktiven Steuerelementen belassen und Redundanz von den anderen Orten entfernen.
-   **Verwenden Sie einen positiven Ausdruck.** Die positive Formulierung ist für Benutzer leichter zu verstehen.

**Richtig:**

Möchten Sie die Datei-und Druckerfreigabe aktivieren?

**Falsch:**

Möchten Sie die Datei-und Druckerfreigabe deaktivieren?

Der Ausdruck muss jedoch mit dem zugeordneten Befehl identisch sein, auch wenn der Befehl negativ formuliert ist. Verwenden Sie z. b. deaktivieren, um einen deaktivierte Befehl zu bestätigen.

-   **Verwenden Sie ggf. das Wort &quot;Window&quot;, um auf das Dialogfeld selbst zu verweisen.**
-   **Verwenden Sie die zweite Person (&quot;you/your"), um den Benutzern mitzuteilen, was** in der Haupt Anweisung und im Inhalts Bereich zu tun ist. Häufig wird die zweite Person impliziert.

**Beispiele:**

Wählen Sie die Bilder aus, die Sie drucken möchten.

Wählen Sie ein Konto aus.

-   **Verwenden Sie die erste Person ("I/Me/My"), damit Benutzer dem Programm mitteilen können, welche** Aktionen in den Steuerelementen im Inhalts Bereich durchzuführen sind, die auf die Haupt Anweisung Antworten.

**Beispiel:** Drucken Sie die Fotos auf meiner Kamera.

### <a name="dialog-box-titles"></a>Dialog Feld Titel

-   **Verwenden Sie den Titel, um den Befehl, die Funktion oder das Programm zu identifizieren, aus dem ein Dialogfeld stammt.**
    -   Wenn das Dialogfeld vom Benutzer initiiert wurde, identifizieren Sie es mithilfe des Befehls-oder Featurenamens. **Ausnahmen:**
        -   Wenn ein Dialogfeld von vielen verschiedenen Befehlen angezeigt wird, sollten Sie stattdessen den Programmnamen verwenden.
        -   Wenn der Titel mit der Main-Anweisung redundant ist, verwenden Sie stattdessen den Programmnamen.
    -   Wenn es sich um ein Programm oder ein System handelt (und daher nicht im Kontext), identifizieren Sie es mithilfe des Programm-oder Featurenamens, um Kontext anzugeben.
    -   Verwenden Sie den Titel nicht, um zu erläutern, wie Sie im Dialogfeld mit der Main-Anweisung vorgehen sollten.
-   Verwenden Sie den genauen Befehlsnamen für Befehls basierte Namen, aber schließen Sie die Auslassungs Zeichen nicht ein, falls vorhanden. Wenn erforderlich, können Sie den Menütitel des Befehls einschließen, um einen guten Titel zu erstellen. Beispiel: für ein Objekt... Verwenden Sie in einem Einfügemenü das einfügeobjekt des Titels.
-   **Wenn auf der Taskleiste ein nicht modalem Dialogfeld angezeigt wird, optimieren Sie den Titel für die Anzeige auf der Taskleiste,** indem Sie die Unterscheidungs Informationen an erster Stelle platzieren. Beispiele: "66% Complete" und "3 Erinnerungen".
-   **Schließen Sie die Wörter "Dialog" oder "Fortschritt" nicht in den Titel ein.** Dies wird impliziert, und wenn Sie Sie deaktivieren, ist es für Benutzer einfacher, Sie zu scannen.
-   Verwenden Sie die Groß-/Kleinschreibung im [Titel](glossary.md), ohne die Beendigung zu beenden

### <a name="main-instructions"></a>Haupt Anleitung

-   **Verwenden Sie die main-Anweisung, um näher erläutern zu können, was im Dialogfeld zu tun ist.** Die Anweisung sollte eine bestimmte Anweisung, eine imperative Richtung oder eine Frage sein. Gute Anweisungen vermitteln das Ziel des Benutzers mit dem Dialogfeld, anstatt sich ausschließlich auf die Mechanismen der Bearbeitung zu konzentrieren.
-   **Lassen Sie die Haupt Anweisung Weg, wenn Sie nur offensichtlich sagen können.** In diesen Fällen ist der Inhalt des Dialog Felds selbsterklärend. Beispielsweise benötigen die Dialogfelder "Datei öffnen" und "Datei speichern" keine Haupt Anweisung, da Ihr Kontext und Ihr Entwurf ihren Zweck offenlegen.
-   **Lassen Sie Steuerelement Bezeichnungen aus, die die main-Anweisung wiedergeben.** In diesem Fall übernimmt die Haupt Anweisung den Zugriffsschlüssel.

**Annehmbar:**

![Screenshot des Textfelds mit redundanter Bezeichnung ](images/win-dialog-box-image50.png)

In diesem Beispiel ist die Textfeld-Bezeichnung lediglich eine erneute Anweisung der Main-Anweisung.

**Besserer**

![Screenshot desselben Textfelds mit einer Bezeichnung ](images/win-dialog-box-image51.png)

In diesem Beispiel wird die redundante Bezeichnung entfernt, sodass die Haupt Anweisung den Zugriffsschlüssel annimmt.

-   **Bei der präzisen Verwendung wird nur ein einzelner, kompletter Satz verwendet.** PiST die Haupt Anweisung der wichtigen Informationen. Wenn Sie etwas anderes erläutern müssen, verwenden Sie ergänzende Anweisungen.
-   **Verwenden Sie nach Möglichkeit bestimmte Verben.** Bestimmte Verben (Beispiele: verbinden, speichern, installieren) sind für Benutzer aussagekräftiger als generische (Beispiele: konfigurieren, verwalten, festlegen).
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   **Schließen Sie keine abschließenden Zeiträume ein, wenn die Anweisung eine-Anweisung ist.** Wenn die Anweisung eine Frage ist, müssen Sie ein endgültiges Fragezeichen einschließen.
-   **Verwenden Sie für Fortschritts Dialogfelder einen partizipformen-Ausdruck, der den gerade ausgeführten Vorgang kurz erläutert und** mit einem Ellipsen endet. Beispiel: Drucken Ihrer Bilder...
-   **Tipp:** Sie können eine Haupt Anweisung auswerten, indem Sie die Aussagen eines Friend-Codes vorstellen. Wenn die Antwort mit der Main-Anweisung unnatürlich, nicht hilfreich oder umständlich ist, bearbeiten Sie die Anweisung erneut.

### <a name="supplemental-instructions"></a>Ergänzende Anweisungen

-   **Verwenden Sie ggf. eine optionale ergänzende Anweisung, um zusätzliche Informationen zu präsentieren, die hilfreich sind, um die Seite zu verstehen oder zu verwenden.** Sie können ausführlichere Informationen bereitstellen und die Terminologie definieren.
-   **Wenn es sich bei der Darstellung des Dialog Felds um ein Programm oder einen System initiierten (und somit nicht um Kontext) handelt, verwenden Sie die ergänzende Anweisung, um zu erläutern, warum das Dialogfeld angezeigt wurde.** Bei solchen Dialogfeldern ist der Kontext in der Regel nicht offensichtlich.
-   **Wiederholen Sie die main-Anweisung nicht mit etwas anderen Formulierungen.** Lassen Sie stattdessen die ergänzende Anweisung Weg, wenn nicht mehr hinzugefügt werden muss.
-   Verwenden Sie vollständige Sätze, die Groß-/Kleinschreibung und die endinterpunktions Zeichen.

### <a name="command-links"></a>Befehls Verknüpfungen

-   **Wählen Sie einen präzisen Linktext aus, der eindeutig kommuniziert und die Funktionsweise des Befehls Links unterscheidet.** Es sollte selbsterklärend sein und der Haupt Anweisung entsprechen. Benutzer müssen nicht ermitteln, was der Link wirklich bedeutet, oder wie er sich von anderen Links unterscheidet.
-   **Starten Sie Befehls Verknüpfungen immer mit einem Verb.**
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Verwenden Sie keine Interpunktion am Ende.
-   **Stellen Sie ggf. eine weitere Erläuterung mithilfe von vollständigen Sätzen und der abschließenden Interpunktions Zeichen bereit.** Fügen Sie jedoch nur solche Erklärungen hinzu, wenn Sie die erforderlichen Informationen nicht allen Befehls Verknüpfungen hinzufügen, sondern nur, weil ein Befehls Link einen Befehl benötigt.

Weitere Informationen und Beispiele finden Sie unter Richtlinien für den [Befehls Link](ctrl-command-links.md) .

### <a name="commit-buttons"></a>Commit-Schaltflächen

-   **Verwenden Sie spezifische Commit-Schaltflächen Bezeichnungen, die selbst sinnvoll sind und eine Antwort auf die Haupt Anweisung sind.** Im Idealfall sollten Benutzer nichts anderes lesen müssen, um die Bezeichnung zu verstehen. Benutzer sind viel wahrscheinlicher, dass Befehlszeilen Bezeichnungen als statischer Text gelesen werden.
-   **Starten Sie Commit-Schaltflächen Bezeichnungen mit einem Verb. Ausnahmen sind "OK", "yes" und "No".**
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   Verwenden Sie keine Interpunktion am Ende.
-   Weisen Sie einen eindeutigen [Zugriffsschlüssel](glossary.md)zu.
    -   **Ausnahme:** Weisen Sie den Schaltflächen OK und Abbrechen keine Zugriffsschlüssel zu Dadurch können die anderen Zugriffsschlüssel leichter zugewiesen werden.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf die Dialogfelder:

-   Informationen zum Programmieren und zur anderen technischen Dokumentation finden Sie unter Dialogfelder als Dialogfelder. Weitere Informationen finden Sie in den Dialogfeldern nach Titel. Wenn die Titelleiste ausgeblendet ist, lesen Sie den Dialog mithilfe der Main-Anweisung.
-   Wenn Sie im Allgemeinen auf ein Dialogfeld verweisen müssen, verwenden Sie das Fenster in der Benutzerdokumentation. Sie können auf ein einfaches Frage Dialogfeld oder eine Bestätigung als Nachricht verweisen.
-   Verwenden Sie den genauen Titel oder Hauptanweisungs Text, einschließlich der Groß-/Kleinschreibung.
-   Formatieren Sie den Titel nach Möglichkeit mithilfe von fettem Text. Andernfalls sollten Sie den Titel nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Klicken Sie unter **Windows-Sicherheit** auf **Weitere Optionen**.

