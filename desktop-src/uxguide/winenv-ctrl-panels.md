---
title: Steuerelemente
description: Verwenden Sie System Steuerungselemente, um Benutzern zu helfen, Features auf Systemebene zu konfigurieren und verwandte Aufgaben auszuführen. Programme, die über eine Benutzeroberfläche verfügen, sollten stattdessen direkt über die Benutzeroberfläche konfiguriert werden.
ms.assetid: 845325ef-9f1d-4aa7-a5b0-685fac74a9f8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dde41544f2bf8c920365f160f71dce7e88d89b81
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103961069"
---
# <a name="control-panels"></a>Steuerelemente

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Verwenden Sie System Steuerungselemente, um Benutzern zu helfen, Features auf Systemebene zu konfigurieren und verwandte Aufgaben auszuführen. Programme, die über eine Benutzeroberfläche verfügen, sollten stattdessen direkt über die Benutzeroberfläche konfiguriert werden.

Mit der Systemsteuerung in Microsoft Windows können Benutzer Features auf Systemebene konfigurieren und verwandte Aufgaben durchführen. Beispiele für die featurekonfiguration auf Systemebene sind Hardware-und Software Einrichtung, Konfiguration, Sicherheit, Systemwartung und Benutzerkonten Verwaltung.

Der Begriff "Systemsteuerung" bezieht sich auf die gesamte System Steuerungsfunktion von Windows. Einzelne Steuerelemente werden als System Steuerungselemente bezeichnet. Ein System Steuerungselement wird als oberste Ebene betrachtet, wenn es über die Startseite der Systemsteuerung oder eine Kategorieseite direkt zugänglich ist.

![Screenshot der Sprachkategorie der Systemsteuerung ](images/winenv-ctrl-panels-image1.png)

Ein typisches Element der Systemsteuerung.

Die Startseite der Systemsteuerung ist der Haupteinstiegspunkt für alle System Steuerungselemente. Dabei werden die Elemente nach ihrer Kategorie zusammen mit den gängigsten Aufgaben aufgelistet. Sie wird angezeigt, wenn Benutzer im Startmenü auf Systemsteuerung klicken.

Auf der Seite System Steuerungs Kategorie werden die Elemente in einer einzelnen Kategorie zusammen mit den häufigsten Aufgaben aufgelistet. Sie wird angezeigt, wenn Benutzer auf der Startseite auf einen Kategorienamen klicken.

System Steuerungselemente werden mithilfe von [Task Flows](glossary.md) oder Eigenschaften Blättern implementiert. Bei Windows Vista und höher sind die Aufgaben Flüsse die bevorzugte Benutzeroberfläche (User Interface, UI).

**Entwickler:** Informationen zum Erstellen von System Steuerungselementen finden Sie unter [System Steuerungselemente](/previous-versions//bb776838(v=vs.85)).

**Hinweis:** Richtlinien, die sich auf [Eigenschaften Blätter](win-property-win.md) beziehen, werden in einem separaten Artikel dargestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Dient der Konfiguration von Features auf Systemebene?** Andernfalls sollten Sie einen anderen Integrationspunkt verwenden. Aktivieren Sie die Konfigurierung Ihrer Anwendungsfunktionen direkt über die Benutzeroberfläche mithilfe der Dialogfelder Optionen anstelle der Systemsteuerung. Verwenden Sie für Hilfsprogramme, die nicht für Setup, Konfiguration oder verwandte Tasks verwendet werden (z. b. Problembehandlung) das Startmenü als Integrationspunkt.
-   **Hat das Feature auf Systemebene eine eigene Benutzeroberfläche?** Wenn dies der Fall ist, können Benutzer über diese Benutzeroberfläche Änderungen vornehmen. Beispielsweise sollte ein Dienstprogramm für die Systemsicherung aus den Programmoptionen anstelle der Systemsteuerung konfiguriert werden.
-   **Müssen Benutzer die Konfiguration häufig ändern?** Wenn dies der Fall ist (z.b. mehrmals pro Woche), sollten Sie alternative Lösungen in Erwägung gezogen, vielleicht zusätzlich zur Systemsteuerung. Beispielsweise kann die Einstellung Windows-Master Volume direkt über das Symbol im Benachrichtigungsbereich konfiguriert werden. Einige Einstellungen können automatisch konfiguriert werden. In Windows-Explorer kann z. b. auf der Registerkarte Kompatibilität für Anwendungseigenschaften eine Anwendung im Farb Modus 256 ausgeführt werden, anstatt dass Benutzer den Videomodus manuell ändern müssen.
-   **Handelt es sich bei den Ziel Benutzern um IT-Experten?** Wenn dies der Fall ist, verwenden Sie stattdessen ein [Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) -Snap-in, das speziell für Systemverwaltungsaufgaben konzipiert ist. In einigen Fällen besteht die beste Lösung darin, sowohl ein System Steuerungselement für allgemeine Benutzer als auch ein MMC-Snap-in für IT-Experten zu haben.

    ![Screenshot des Fensters "Computer Verwaltung" ](images/winenv-ctrl-panels-image2.png)

    In diesem Beispiel bietet das MMC-Snap-in "lokale Benutzer und Gruppen" eine Benutzerverwaltung für IT-Experten. Andere Benutzer verwenden in der Systemsteuerung eher das Element Benutzerkonten.

-   **Ist das Feature eine OEM-Funktion, die nur während der anfänglichen Systemkonfiguration verwendet wird?** Wenn dies der Fall ist, verwenden Sie das Windows-Willkommens Center als Integrationspunkt.

System Steuerungselemente sind erforderlich, da viele Features auf Systemebene keinen offensichtlicheren oder direkten Integrationspunkt aufweisen. Die Systemsteuerung sollte jedoch nicht als "ein Ort" für alle Konfigurationseinstellungen angezeigt werden. **Programme, die über eine Benutzeroberfläche verfügen, sollten direkt über die Benutzeroberfläche konfiguriert werden, anstatt System Steuerungselemente zu verwenden.**

**Falsch:**

![Screenshot der System Steuerungs Option "Internet Options Element" ](images/winenv-ctrl-panels-image3.png)

In diesem Beispiel sollte Windows Internet Explorer nicht in der Systemsteuerung dargestellt werden, da die eigene Benutzeroberfläche ein besserer Integrationspunkt ist.

### <a name="create-a-new-control-panel-item-or-extend-an-existing-one"></a>Erstellen Sie ein neues System Steuerungselement, oder erweitern Sie ein vorhandenes Element?

Orientieren Sie sich an folgenden Fragen:

-   **Können die Funktionen als Aufgaben ausgedrückt werden, die in ein vorhandenes, erweiterbares System Steuerungselement eingebunden werden können?** Die folgenden System Steuerungselemente sind erweiterbar: Bluetooth-Geräte, Anzeige, Internet, Tastatur, Maus, Netzwerk, Strom, System, drahtlos (Infrarot).
-   **Ersetzen die Eigenschaften und Tasks die Features des vorhandenen erweiterbaren System Steuerungs Elements?** Wenn dies der Fall ist, sollten Sie das vorhandene System Steuerungselement erweitern, da dies zu einer einfacheren Benutzer Darstellung führt. Falls nicht, erstellen Sie ein neues System Steuerungselement.

## <a name="design-concepts"></a>Entwurfskonzepte

**Das System Steuerungskonzept basiert auf einem echten Metapher.** Eine reale Systemsteuerung ist eine Sammlung von Steuerelementen (Knoten, Switches, Messgeräte und anzeigen), mit denen ein Gerät überwacht und gesteuert wird. Benutzer solcher Steuerelemente benötigen häufig Schulungen, um zu verstehen, wie Sie verwendet werden können.

Im Gegensatz zu den realen Gegenstücken **werden die Windows-System Steuerungs Entwürfe für erstmalige Benutzer optimiert.** Benutzer führen die meisten Aufgaben in der Systemsteuerung nicht sehr oft aus, Sie merken sich also in der Regel nicht, wie Sie Sie durchführen können, und müssen Sie jedes Mal erneut erlernen.

So entwerfen Sie ein System Steuerungselement, das nützlich und einfach zu verwenden ist:

-   Stellen Sie sicher, dass die Eigenschaften erforderlich sind.
-   Stellen Sie Eigenschaften in Bezug auf die Benutzer Ziele anstelle der Technologie dar.
-   Stellen Sie die Eigenschaften auf der rechten Ebene dar.
-   Entwurfs Seiten für bestimmte Aufgaben.
-   Entwurfs Seiten für Standard Benutzer und geschützte Administratoren.

Wenn Sie in der Systemsteuerung Einzuschließende Elemente entwerfen und auswerten, bestimmen Sie die allgemeinen Aufgaben, die Benutzer ausführen, und stellen Sie sicher, dass ein eindeutiger Pfad zum Ausführen dieser Aufgaben vorhanden ist. Benutzer führen in der Regel die folgenden Aufgaben Typen mit System Steuerungselementen aus:

-   Anfängliche Konfiguration
-   Seltene Änderungen (für die meisten Einstellungen)
-   Häufige Änderungen (für einige wichtige Einstellungen)
-   Rollback von Einstellungen auf einen anfänglichen oder vorherigen Zustand
-   Problembehandlung

**Wenn Sie nur eine Aktion ausführen...**

Entwerfen Sie die System Steuerungs Seiten für bestimmte Aufgaben, und stellen Sie Sie im Hinblick auf die Benutzer Ziele anstelle der Technologie dar.

## <a name="usage-patterns"></a>Verwendungsmuster

Bei System Steuerungselementen können Sie einen Task Ablauf oder ein Eigenschaften Blatt verwenden. Dies sind die Verwendungs Muster:

### <a name="task-flow-patterns"></a>Aufgaben Fluss Muster

Aufgaben Fluss Elemente verwenden eine Hub-Seite, um die allgemeine Auswahl anzuzeigen, und sprechen Seiten, um die tatsächliche Konfiguration auszuführen.

**Hub-Seiten**

-   Task basierte Hub-Seiten. Diese Hub-Seiten stellen die am häufigsten verwendeten Aufgaben dar. Sie eignen sich am besten für einige häufig verwendete oder wichtige Aufgaben, bei denen Benutzer mehr Anleitungen und Erläuterungen benötigen. Hub-Seiten haben keine Commit-Schaltflächen. Auf Hybrid Aufgaben basierende Hub-Seiten verfügen auch direkt über einige Eigenschaften oder Befehle. Hybride Hub-Seiten werden dringend empfohlen, wenn Benutzer mit der höchsten Wahrscheinlichkeit die Systemsteuerung verwenden, um auf diese Eigenschaften und Befehle zuzugreifen.
-   Objektbasierte Hub-Seiten. Diese Hub-Seiten stellen die verfügbaren Objekte mithilfe eines Listenansicht-Steuer Elements bereit. Diese werden am besten verwendet, wenn mehrere Objekte vorhanden sein könnten. Hub-Seiten haben keine Commit-Schaltflächen.

**Sprachseiten**

-   Aufgabenseiten. Diese Sprachseiten stellen eine Aufgabe oder einen Schritt in einer Aufgabe mit einer bestimmten, aufgabenbasierten Haupt Anweisung dar. Sie eignen sich am besten für Aufgaben, die von zusätzlichen Anleitungen und Erläuterungen profitieren.
-   Formular Seiten. Diese Sprachseiten stellen eine Auflistung verwandter Eigenschaften und Aufgaben auf Grundlage einer allgemeinen Haupt Anweisung dar. Sie eignen sich am besten für Funktionen, die über viele Eigenschaften verfügen und von einer direkten Darstellung mit nur einer Seite profitieren, wie z. b. Erweiterte Eigenschaften.

### <a name="property-sheet-patterns"></a>Eigenschaften Blattmuster

-   Eigenschaften Blätter werden am besten in Legacy Elementen mit vielen Einstellungen verwendet, die auf Erweiterte Benutzer ausgerichtet sind. Neue Elemente können mit einem Aufgaben Fluss mithilfe des Formular Seiten Musters denselben Effekt erzielen.

## <a name="guidelines"></a>Richtlinien

### <a name="property-sheet-control-panel-items"></a>Eigenschaften Blatt-System Steuerungselemente

-   **Verwenden Sie für neue System Steuerungselemente keine Eigenschaften Blätter.** Verwenden Sie stattdessen taskflows, um eine nahtlose Funktion zu erstellen und die Kategorisierung und Suchfunktion der System Steuerungs-Startseite vollständig zu nutzen.

### <a name="task-flow-control-panel-items"></a>Aufgaben Fluss-System Steuerungselemente

**Allgemein**

-   **Behalten Sie den wichtigsten Inhalt und die Steuerelemente ohne Bildlauf sichtbar.** Die Benutzer Scrollen nicht zum Anzeigen von Seiten Inhalten, es sei denn, Sie haben einen Grund für. Sie können Commit-Schaltflächen immer sichtbar machen, indem Sie Sie in einen [Befehlsbereich](glossary.md) anstatt im Inhalts Bereich platzieren. Unterbrechen Sie die Seiten nicht, um einen Bildlauf zu vermeiden.
    -   **Sie können lange Seiten vertikal scrollen,** solange die wichtigsten Steuerelemente ohne Bildlauf sichtbar sind.
    -   **Verwenden Sie keinen horizontalen Bildlauf.** Entwerfen Sie stattdessen den Seiten Inhalt neu, und verwenden Sie das vertikale Scrollen. Seiten können nur dann horizontale Scrollleisten aufweisen, wenn Sie sehr schmal sind.
-   **So navigieren Sie zwischen Seiten:**
    -   Verwenden Sie [Aufgaben Verknüpfungen](glossary.md) , um eine Aufgabe zu starten.
    -   Verwenden Sie Aufgaben Verknüpfungen oder eine Schaltfläche "weiter", um zur nächsten Seite in einer mehrstufigen Aufgabe zu navigieren.
    -   Verwenden Sie Commit-Schaltflächen, um eine Aufgabe abzuschließen.
    -   Verwenden Sie die Schaltfläche zurück in der Menüleiste, um zu den zuvor angezeigten Seiten zurückzukehren. Fügen Sie dem Befehlsbereich keine Schaltfläche "zurück" hinzu.
    -   Verwenden Sie die Adressleiste, um direkt zur System Steuerungs-Startseite zurückzukehren.
    -   Verwenden Sie auch Links im Aufgabenbereich, um zu Seiten in anderen System Steuerungselementen zu navigieren. Andernfalls sollte die Navigation innerhalb eines einzelnen Elements der Systemsteuerung bleiben.
-   **Legen Sie in der Adressleiste nur die Startseite der Systemsteuerung ab.** Wenn Sie auf diesen Link klicken, wird die Startseite der Systemsteuerung zurückgegeben, wobei alle laufenden Arbeiten ohne [Bestätigung](https://msdn.microsoft.com/library/windows/desktop/aa511273.aspx)abgebrochen werden.
-   **Legen Sie auf den Seiten der Systemsteuerung keine Schaltfläche "Schließen".** Benutzer können ein System Steuerungs Fenster mithilfe der Schaltfläche Schließen auf der Titelleiste schließen.

**Aufgaben Verknüpfungen und Schaltflächen**

-   **Wenn eine Seite einen kleinen Satz fester Optionen aufweist, verwenden Sie Aufgaben Verknüpfungen anstelle einer Kombination aus Options Feldern und der Schaltfläche Weiter.** Dies ermöglicht es Benutzern, eine Antwort mit einem einzigen Mausklick auszuwählen.
-   Sie können Aufgaben Verknüpfungen und Schaltflächen an den folgenden Stellen platzieren (in der Reihenfolge der Auffindbarkeit):
    -   Der [Befehlsbereich](glossary.md) (für Befehls Schaltflächen nur auf Sprachseiten).
    -   Der [Inhalts Bereich](glossary.md):
        -   Befehls Schaltflächen
        -   Aufgaben Verknüpfungen
        -   Weitere Links
    -   Links im [Aufgaben](glossary.md) Bereich (nur Hub-Seiten).
-   **Basieren Sie auf dem Speicherort von Aufgaben Verknüpfungen und Schaltflächen auf Wichtigkeit, und benötigen Sie eine Erkennbarkeit**
    -   **Legen Sie im Befehlsbereich nur Commit-Schaltflächen ab.**
    -   **Legen Sie wichtige Aufgaben im Inhalts Bereich ab.** Befehls Schaltflächen neigen dazu, die meiste Aufmerksamkeit zu zeichnen, sodass Sie für Befehle reserviert werden, die Benutzern angezeigt werden. Aufgaben Verknüpfungen zeichnen auch Aufmerksamkeit, aber weniger als Befehls Schaltflächen.
    -   **Reservieren Sie den Aufgabenbereich und einfache Links für sekundäre (weniger wichtige) Aufgaben.** Der Aufgabenbereich ist der am wenigsten ermittelbare Bereich einer Aufgabenseite, und einfache Links sind nicht so sichtbar wie Befehls Schaltflächen und Aufgaben Verknüpfungen.
-   Für Aufgaben Verknüpfungen, die im Inhalts Bereich angezeigt werden:
    -   **Wenn mehr als sieben Links vorhanden sind, Gruppieren Sie die Verknüpfungen in Kategorien.** Stellen Sie Überschriften für jede Gruppe bereit.
    -   **Stellen Sie für weniger als sieben Links die Verknüpfungen in einer einzelnen Gruppe ohne Überschrift dar.**
-   **Stellen Sie Aufgaben Verknüpfungen und Schaltflächen in einer logischen Reihenfolge dar.** Aufgaben Verknüpfungen vertikal auflisten, Befehls Schaltflächen horizontal.
-   Teilen Sie die Befehle innerhalb von Kategorien **in Verwandte Gruppen auf.** Präsentieren Sie die Aufgaben Gruppen, indem Sie die am häufigsten verwendeten Aufgaben platzieren und die am häufigsten verwendeten Aufgaben in jeder Gruppe platzieren. **Die resultierende Reihenfolge sollte ungefähr der Wahrscheinlichkeit der Verwendung, aber auch eines logischen Flows entsprechen.**
    -   **Ausnahme:** Aufgaben Verknüpfungen, die zu allen Aufgaben führen, sollten zuerst platziert werden.
-   **Wenn viele Aufgaben Verknüpfungen vorhanden sind, sollten Sie die wichtigsten Aufgaben** mit einem Symbol rund um die Uhr und zwei Textzeilen besser ansehen. Verwenden Sie für weniger wichtige Aufgaben ein 16x16-Pixel-Symbol oder kein Symbol und eine einzelne Textzeile.

    ![Screenshot von Elementen mit großen und kleinen Symbolen ](images/winenv-ctrl-panels-image4.png)

    In diesem Beispiel erhalten wichtige Befehle eine stärkere Darstellung.

-   **Löschen Sie die physische Trennung zwischen häufig verwendeten Befehlen und destruktiven Befehlen.** Andernfalls können Benutzer versehentlich auf zerstörerische Befehle klicken. Möglicherweise müssen Sie Ihre Befehle etwas neu anordnen, um zerstörerische Befehle zu platzieren.
-   **Bereitstellen des Mechanismus zum Rückgängigmachen von Befehlen direkt auf der Seite.** Benutzer müssen nicht an einer anderen Stelle navigieren, um einen Fehler rückgängig zu machen.
-   **Verwenden Sie für Aufgaben Verknüpfungen entweder alle standardmäßigen Task Verknüpfungs Symbole oder alle benutzerdefinierten Symbole.** Mischen Sie diese nicht. Verwenden Sie benutzerdefinierte Symbole nur dann, wenn Folgendes gilt:
    -   Sie unterstützen Benutzer beim Verständnis der Aufgaben.
    -   Sie entsprechen den [Aero-Symbol Standards](vis-icons.md).
    -   Sie haben eine unaufdringliche Darstellung.

**Dialogfelder**

Wenn Sie taskflows verwenden, möchten Sie im Allgemeinen, dass eine Aufgabe innerhalb eines einzelnen Fensters von einer Seite an eine Seite weitergeleitet wird, aber die folgenden Umstände sind Ausnahmen. Verwenden Sie die Dialogfelder in folgenden Situationen:

-   , Um Benutzer zur Eingabe eines Administrator Benutzernamens und Kennworts aufzufordern. Verwenden Sie für diesen Zweck immer das Dialogfeld Anmelde Informationsverwaltung. (Sollte [Modal](glossary.md)sein.)
-   So bestätigen Sie einen direkten Befehl mithilfe eines Aufgaben Dialogfelds oder eines Meldungs Felds. (Sollte modal sein.)
-   Um Eingaben für direkte Befehle zu erhalten, z. b. für die Befehle New, Add, Save As, Rename und Print.

    ![Screenshot des Dialog Felds "Netzwerkspeicher Orte löschen" ](images/winenv-ctrl-panels-image5.png)

    In diesem Beispiel wird der DELETE-Befehl in einem Dialogfeld anstelle einer separaten Seite ausgeführt.

-   Um sekundäre, eigenständige Aufgaben auszuführen. Mit einem nicht modalem, sekundären [Fenster können solche](glossary.md)Aufgaben unabhängig und außerhalb des Hauptaufgaben Flusses ausgeführt werden.

### <a name="hub-pages"></a>Hub-Seiten

**Allgemein**

-   Verwenden Sie aufgabenbasierte Hub-Seiten in folgenden Aufgaben:
    -   **Es gibt eine kleine Anzahl häufig verwendeter oder wichtiger Aufgaben.**
    -   **Die Konfiguration umfasst ein oder zwei Objekte** (Beispiele: Monitore, Tastatur, Maus, Spiele Controller).
    -   **Die Konfiguration ist systemweit anwendbar** (Beispiele: Datum und Uhrzeit, Sicherheit, Energieoptionen).
-   Verwenden Sie objektbasierte Hub-Seiten in folgenden:
    -   **Die Konfiguration kann mehrere Objekte umfassen** (Beispiele: Benutzerkonten, Netzwerkverbindungen, Drucker).
    -   **Die Konfiguration gilt nur für das ausgewählte Objekt**.
-   **Verwenden Sie keine Hub-Seite, wenn das System Steuerungselement über eine einzelne Seite verfügt** , die alle beteiligten Tasks und Eigenschaften enthält.

**Objektlisten**

-   **Listet die Elemente in einer logischen Reihenfolge auf.** Sortieren Sie benannte Objekte in alphabetischer Reihenfolge, Zahlen in numerischer Reihenfolge und Datumsangaben in chronologischer Reihenfolge.
-   Stellen Sie bei objektbasierten Hubs **Objekt Ansichts Befehle im Aufgabenbereich bereit, wenn die Möglichkeit zum Ändern der Ansicht für die Aufgaben wichtig ist**. Die Fähigkeit zum Ändern von Ansichten ist wichtig, wenn viele Objekte vorhanden sind und die Standarddarstellung für alle Szenarien nicht gut funktioniert. Benutzer können die Listenansicht ändern, auch wenn es keine expliziten Befehle im Kontextmenü der Listenansicht gibt, aber weniger auffallen.

Weitere Richtlinien zum Darstellen von Objektlisten finden Sie unter [Auflisten von Ansichten](ctrl-list-views.md).

**Interaktion**

-   **Legen Sie keine Commit-Schaltflächen auf den Hub-Seiten** Hub-Seiten sind grundlegende Startpunkte. Benutzer haben niemals einen Commit für die Hub-Seiten durchgeführt Und commitschaltflächen auf Hub-Seiten machen alle Tasks, die von einem Hub initiiert werden, verwirrend (Benutzer Fragen sich, ob ein Commit für diese Aufgaben ausgeführt werden muss)
    -   **Ausnahme:** Wenn das Ändern einer Einstellung eine [Erhöhung](glossary.md)erfordert, geben Sie eine Schaltfläche anwenden mit einem [Sicherheitsschild Symbol](winenv-uac.md)an. Deaktivieren Sie die Schaltfläche Commit, nachdem die Änderungen angewendet wurden.
-   **Sie sollten die nützlichsten Eigenschaften direkt auf den Hub-Seiten platzieren.** Solche Hybrid-Hub-Seiten werden dringend empfohlen, wenn Benutzer mit der höchsten Wahrscheinlichkeit die Systemsteuerung verwenden, um auf diese Eigenschaften zuzugreifen.

    ![Screenshot der Seite "Energieoptionen-Hub" ](images/winenv-ctrl-panels-image6.png)

    In diesem Beispiel verfügt das System Steuerungselement Energieoptionen über die nützlichsten Einstellungen direkt auf der Hub-Seite.

-   **Verwenden Sie ein sofortiges Commit-Modell für alle Einstellungen auf Hybrid-Hub-Seiten, damit Änderungen sofort vorgenommen werden.** Auch hier haben Benutzer niemals einen Commit für eine Hub-Seite. Wenn eine Einstellung eine Commit-Schaltfläche erfordert, platzieren Sie Sie nicht auf einer Hub-Seite.
-   **Es empfiehlt sich, einfache, "einstufige" Befehle direkt auf den Hub-Seiten zu platzieren, anstatt Navigationslinks zu verwenden.**
-   **Bestätigen Sie direkte Befehle, deren Auswirkungen nicht einfach rückgängig gemacht werden können.** Verwenden Sie ein [Aufgaben Dialogfeld](win-dialog-box.md) oder Meldungs [Feld](glossary.md).

    ![Screenshot des Dialog Felds "Löschen bestätigen" ](images/winenv-ctrl-panels-image7.png)

    In diesem Beispiel wird der Befehl Delete mit einem Dialogfeld bestätigt.

-   **Identifizieren Sie für aufgabenbasierte Hub-Seiten jede Aufgabe mit einem Aufgaben Link und einem Symbol.** Sie können auch eine optionale Beschreibung für jeden Link angeben. Versuchen Sie jedoch, die Aufgaben Verknüpfungen selbsterklärend zu machen, und geben Sie optionale Beschreibungen nur für Links an, die Sie wirklich benötigen.

    ![Screenshot der Seite "Computer Leistungs-Hub" ](images/winenv-ctrl-panels-image8.png)

    In diesem Beispiel verfügt jede Aufgabe über einen Aufgaben Link und ein Symbol.

-   **Bei objektbasierten Hub-Seiten wählt das einmalige klicken auf Objekte und das Doppelklicken ein Objekt aus und navigiert zur Standardseite.** Die Standardseite ist in der Regel eine Eigenschaften Seite oder eine aufgabenbasierte Hub-Seite.
-   **Eine objektbasierte Hub-Seite kann zu einem aufgabenbasierten Hub für die ausgewählten Objekte navigieren.** Diese sekundären Hubs sollten jedoch vermieden werden, da Sie ein System Steuerungselement zu indirekt machen.

**Aufgabenbereiche**

Verwenden Sie Aufgabenbereiche, um Links zu Befehlen, Ansichten und zugehörigen System Steuerungselementen anzuzeigen.

-   Stellen Sie für Aufgabenbereiche in Task basierten Hubs Links in der folgenden Reihenfolge dar:
    -   **Sekundäre Befehle**. Stellen Sie primär Aufgaben nur im Inhalts Bereich dar. Verwenden Sie den Aufgabenbereich für sekundäre, optionale Tasks. Angenommen, eine Aufgabe ist primär, wenn Benutzer Sie in wichtigen Szenarien ermitteln müssen. sekundär, wenn es für Benutzer akzeptabel ist, Sie nicht zu ermitteln.
    -   **Siehe auch**. Die optionalen Links, die zu verwandten System Steuerungselementen navigieren.
-   Stellen Sie für Aufgabenbereiche in objektbasierten Hubs Links in der folgenden Reihenfolge dar:
    -   **Objekt Ansichten**. Die optionalen Links, die zum Steuern der Darstellung der-Objekte verwendet werden.
    -   Die **Befehle wurden korrigiert**. Die Befehle, die unabhängig von den derzeit ausgewählten Objekten sind.
    -   **Kontextabhängige Befehle**. Die Befehle, die von den derzeit ausgewählten Objekten abhängen und daher nicht immer angezeigt werden.
    -   **Siehe auch**. Die optionalen Links, die zu verwandten System Steuerungselementen navigieren.
-   **Verwenden Sie keine Aufgabenbereiche in den Sprachseiten.** Anders als bei Hub-Seiten sollten sich die Sprachseiten auf das Abschließen der Aufgabe konzentrieren. Sie möchten Benutzer nicht ermutigen, vor dem Abschluss zu navigieren.

**Siehe auch Links**

-   **Stellen Sie auch Links im Aufgabenbereich bereit, um Benutzern die Suche nach verwandten System Steuerungselementen oder dem richtigen System Steuerungselement zu erleichtern.** Link zu Elementen, die Benutzer mit dem System Steuerungselement verknüpfen.

    ![Screenshot der Verknüpfungen des Aktions Centers "Siehe auch" ](images/winenv-ctrl-panels-image9.png)

    In diesem Beispiel ist das System Steuerungselement "Action Center" mit den zugehörigen System Steuerungselementen verknüpft.

-   **Verknüpfen Sie eine bestimmte Aufgabenseite, wenn dies für die Benutzer wahrscheinlicher ist.** Andernfalls können Sie eine Verknüpfung mit dem gesamten System Steuerungselement herstellen. Verwenden Sie den Namen der Systemsteuerung, ohne den Ausdruck, die Systemsteuerung, hinzuzufügen.

### <a name="spoke-pages"></a>Sprachseiten

**Allgemein**

-   **Verwenden Sie Aufgabenseiten für häufig verwendete oder wichtige Aufgaben, bei denen Benutzer mehr Anleitungen und Erläuterungen benötigen.**
-   **Verwenden Sie Formular Seiten für Funktionen mit vielen Einstellungen, und profitieren Sie von einer direkten Darstellung mit einer einzelnen Seite.** Die idealen Aufgaben für solche Seiten umfassen in der Regel offensichtliche Änderungen an einigen einfachen Eigenschaften.
-   **Verwenden Sie keine Aufgabenbereiche in den Sprachseiten.**

**Interaktion**

-   **Versuchen Sie, die Hauptaufgaben auf eine einzelne Seite zu beschränken.** Wenn mehr als eine Seite erforderlich ist, können Sie folgende Aktionen ausführen:
    -   **Verwenden Sie für zusätzliche oder optionale Schritte zwischen Sprachseiten.** Für zwischengeschaltete Seiten wird von der abschließenden Seite "gesprochen" ein Commit ausgeführt
    -   **Verwenden Sie unabhängige Fenster für unabhängige hilfsanstellungen.** Unabhängige Fenster werden eigenständig und unabhängig von der Hauptaufgabe bereitgestellt.

Dadurch wird die Bedeutung der commitschaltflächen für die Hauptaufgabe klar und eindeutig. Benutzer sollten immer sicher sein, dass Sie wissen, wofür Sie einen Commit ausführen.

-   **Verwenden Sie nicht die Option "Siehe auch Links" innerhalb eines Aufgaben Flusses.** Diese sind mit Verwandten, aber unterschiedlichen System Steuerungselementen verknüpft. Obwohl das Navigieren zu einem anderen Element in Hub-Seiten zulässig ist, befindet es sich nicht in den Wort Seiten, da die Aufgabe dadurch unterbrochen wird.
-   **Verwenden Sie keine Sprachseiten für einfache Eingabe oder Bestätigungen.** Verwenden Sie stattdessen modale Dialogfelder.

**Interaktion (zwischenwort Seiten)**

-   **Verwenden Sie Aufgaben Verknüpfungen oder eine Schaltfläche "weiter", um zur nächsten Seite zu navigieren.** Die Möglichkeit, mit dem nächsten Schritt fortzufahren, sollte immer offensichtlich sein.
-   **Sie können Navigationslinks zu optionalen Task Schritten haben.** Um Verwirrung zu vermeiden, wenn Benutzer einen Commit für die Aufgabe ausführen, sollten diese zusätzlichen Seiten zwischen Seiten innerhalb desselben System Steuerungs Elements sein. Sie sollten keine Commit-Schaltflächen haben, sondern sollten ausgeführt werden, wenn ein Commit für die Hauptaufgabe ausgeführt wird.

**Interaktion (abschließende Sprachseiten)**

-   **Verwenden Sie Commit-Schaltflächen, um eine Aufgabe abzuschließen.** Verwenden Sie ein [Verzögertes commitmodell](glossary.md) für das Schreiben von Seiten, sodass Änderungen erst vorgenommen werden, wenn explizit ein Commit ausgeführt wird (wenn Benutzer mit der Rückseite, dem Schließen oder der Adressleiste navigieren, werden die Änderungen abgebrochen). Die Schaltflächen "Commit" sind ein visueller Hinweis darauf, dass der Benutzer eine Aufgabe durchführen soll. Verwenden Sie für diesen Zweck keine Verknüpfungen.
-   **Bestätigen Sie die Commit-Schaltflächen (einschließlich Abbrechen) nicht.** Dies kann ärgerlich sein. Ausnahmen:
    -   Die Aktion hat bedeutende Konsequenzen und ist, falls falsch, nicht leicht zu fixieren.
    -   Die Aktion kann zu einem erheblichen Verlust der Zeit oder des Aufwands des Benutzers führen.
    -   Die Aktion ist mit anderen Aktionen eindeutig inkonsistent.
-   Vergewissern Sie sich nicht, dass **Benutzer Änderungen** verwerfen, indem Sie mit der Rückseite, dem Schließen oder der Adressleiste navigieren. Allerdings können Sie überprüfen, ob eine potenziell unbeabsichtigte Navigation zu einem erheblichen Verlust der Zeit oder des Aufwands des Benutzers führen kann.
-   **Verwenden Sie weder Befehls-noch Navigationslinks** (siehe auch Links). Auf den letzten Sprachseiten sollten Benutzer den Task explizit ausführen oder Abbrechen. Benutzer sollten nicht aufgefordert werden, an einer anderen Stelle zu navigieren, da dadurch die Aufgabe wahrscheinlich implizit abgebrochen wird.
-   **Wenn Benutzer eine Aufgabe beenden oder Abbrechen, sollten Sie zurück an die Hub-Seite gesendet werden, von der aus die Aufgabe gestartet wurde.** Wenn keine solche Seite vorhanden ist, schließen Sie stattdessen das Fenster "Systemsteuerung". Gehen Sie nicht davon aus, dass die Sprachseiten immer von einer anderen Seite gestartet werden.
-   **Entfernen Sie die veralteten "Commit"-Seiten aus dem Windows-Explorer-Back-Stack** , wenn Sie die Benutzer zurück zu der Seite zurückgeben, von der aus der Task gestartet wurde. Benutzern sollten nie die Seiten angezeigt werden, für die Sie bereits ein Commit ausgeführt haben, wenn Sie auf die Schaltfläche Zurück klicken Benutzer sollten immer zusätzliche Änderungen vornehmen, indem Sie die Aufgabe vollständig wiederholen, anstatt auf zurück zum Ändern veralteter Seiten zu klicken.
    -   **Entwickler:** Sie können diese veralteten Seiten mithilfe der APIs itravellog:: findtravelentry () und itravellogex::D eleteentry () entfernen.

**Commit-Schaltflächen**

**Hinweis:** Schaltflächen Abbrechen gelten als Commit-Schaltflächen.

-   **Bestätigen Sie Aufgaben mithilfe von Commit-Schaltflächen, bei denen es sich um spezifische Antworten auf die Haupt Anweisung handelt, anstelle von generischen Bezeichnungen wie OK** Die Beschriftungen auf den Commit-Schaltflächen sollten selbst sinnvoll sein. Vermeiden Sie die Verwendung von "OK", da es sich nicht um eine bestimmte Antwort auf die Haupt Anweisung handelt und daher leichter zu verstehen ist. Außerdem wird in der Regel OK mit modalen Dialogfeldern verwendet, und es wird fälschlicherweise impliziert, das Fenster der System Steuerungselemente zu schließen.
    -   **Ausnahmen:**
        -   Verwenden Sie OK für Seiten, die keine Einstellungen haben.
        -   Verwenden Sie OK, wenn die jeweilige Antwort immer noch generisch ist, z. b. speichern, auswählen oder auswählen, als ob Sie eine bestimmte Einstellung oder eine Auflistung von Einstellungen ändern möchten.
        -   Verwenden Sie die Schaltfläche OK, wenn die Seite Options Felder enthält, die Antworten auf die Haupt Anweisung sind. Um das verzögerte Commit-Modell beizubehalten, können Sie keine Aufgaben Verknüpfungen auf einer abschließenden Seite "sprechen" verwenden.

            ![Screenshot der Webeinschränkungen mit der Schaltfläche "OK" ](images/winenv-ctrl-panels-image10.png)

            In diesem Beispiel sind die Options Felder, nicht die Commit-Schaltflächen, Antworten auf die main-Anweisung.
-   **Geben Sie eine Schaltfläche Abbrechen an, damit Benutzer Änderungen explizit verwerfen können.** Obwohl Benutzer eine Aufgabe implizit abbrechen können, indem Sie Ihre Änderungen nicht bestätigen, ermöglicht Ihnen die Bereitstellung einer Schaltfläche "Abbrechen" eine höhere Vertrauenswürdigkeit.
    -   **Ausnahme:** Geben Sie für Aufgaben, bei denen Benutzer keine Änderungen vornehmen können, keine Schaltfläche Abbrechen an. Die Schaltfläche OK hat denselben Effekt wie Abbrechen in diesem Fall.
-   **Verwenden Sie nicht die Schaltflächen schließen, fertig oder Fertigstellen.** Diese Schaltflächen werden in der Regel mit modalen Dialogfeldern verwendet und implizieren fälschlicherweise, das Fenster der System Steuerungselemente zu schließen. Benutzer können das Fenster mithilfe der Schaltfläche Schließen auf der Titelleiste schließen. Außerdem sind "Fertig" und "Fertigstellen" irreführend, da Benutzer zu der Seite zurückkehren, von der aus die Aufgabe gestartet wurde, sodass Sie nicht wirklich fertig sind.
-   **Deaktivieren Sie keine Commit-Schaltflächen.** Andernfalls müssen Benutzer ableiten, warum die Commit-Schaltflächen deaktiviert werden. Es ist besser, die Commit-Schaltflächen aktiviert zu lassen und eine hilfreiche Fehlermeldung zu erhalten, wenn ein Problem vorliegt.
-   **Stellen Sie sicher, dass die Schaltflächen Commit auf der Seite ohne Bildlauf angezeigt werden.** Wenn die Seite lang ist, können Sie die Commit-Schaltflächen immer sichtbar machen, indem Sie Sie in einen [Befehlsbereich](glossary.md)anstatt im Inhalts Bereich platzieren.

    ![Screenshot des Dialog Felds "Automatische Wiedergabe" ](images/winenv-ctrl-panels-image11.png)

    In diesem Beispiel ist die Größe des Inhalts Bereichs unbegrenzt, sodass die Commit-Schaltflächen im Befehlsbereich abgelegt werden.

-   Richten Sie die Commit-Schaltflächen rechtsbündig ein, und verwenden Sie diese Reihenfolge (von links nach rechts): positive Commit-Schaltflächen, Abbrechen und anwenden.

**Vorschau Schaltflächen**

-   Stellen Sie sicher **, dass die Schaltfläche Vorschau die ausstehenden Änderungen jetzt anwendet, aber die aktuellen Einstellungen wiederherstellen, wenn Benutzer von der Seite weg navigieren, ohne die Änderungen zu übernehmen.**
-   **Sie können die Schaltflächen "Vorschau" auf jeder beliebigen Seite verwenden.** Hub-Seiten benötigen keine Vorschau Schaltflächen, da Sie ein [sofortiges Commit-Modell](glossary.md)verwenden.
-   **Verwenden Sie die Schaltfläche "Vorschau" anstelle einer Schaltfläche "anwenden" für System Steuerungs Seiten.** Vorschau Schaltflächen sind für Benutzer leichter zu verstehen und können auf jeder beliebigen Seite verwendet werden.
-   **Geben Sie nur dann eine Vorschau Schaltfläche an, wenn auf der Seite Einstellungen (mindestens eine) mit Effekten angezeigt werden, die Benutzern angezeigt werden.** Benutzer sollten in der Lage sein, eine Änderung in der Vorschau anzuzeigen, die Änderung zu evaluieren und auf der Grundlage dieser Auswertung weitere Änderungen vorzunehmen.
-   **Aktivieren Sie immer die Schaltfläche Vorschau.**

**Live Vorschau**

Ein System Steuerungselement verfügt über eine Live Vorschau, wenn die Auswirkungen von Änderungen auf einer sprach Seite sofort angezeigt werden können.

-   **Verwenden Sie die Live Vorschau für Anzeigeeinstellungen in folgenden Situationen:**
    -   Der Effekt ist offensichtlich, in der Regel, weil er für den gesamten Monitor gilt.
    -   Der Effekt kann ohne erhebliche Verzögerung angewendet werden.
    -   Der Effekt ist sicher und kann problemlos rückgängig gemacht werden.

        ![Screenshot des Dialog Felds "Farbeinstellungen ändern" ](images/winenv-ctrl-panels-image12.png)

        In diesem Beispiel werden die Auswirkungen der Einstellungen für die Windows-Farbe und-Darstellung sofort angezeigt. Auf diese Weise können Benutzer mit minimalem Aufwand Änderungen vornehmen.

-   **Verwenden Sie für die Commit-Schaltflächen die Schaltflächen Speichern und Abbrechen.** "Änderungen speichern" behält die aktuellen Einstellungen bei, während "Abbrechen" auf die ursprünglichen Einstellungen zurückgesetzt wird. "Änderungen speichern" wird anstelle von "OK" verwendet, um zu überprüfen, ob alle in der Vorschau angezeigten Änderungen noch nicht angewendet wurden.
-   **Geben Sie keine Apply-Schaltfläche an.** Die Live Vorschau macht Apply unnötig.
-   Stellen Sie **alle Änderungen wieder her, wenn Benutzer** mit der Rückseite, dem Schließen oder der Adressleiste navigieren. Zum Beibehalten von Änderungen müssen Benutzer diese explizit übertragen.

**Schaltflächen anwenden**

-   Stellen Sie sicher **, dass die Schaltfläche übernehmen die ausstehenden Änderungen anwendet (die seit dem Start der Aufgabe oder der letzten Anwendung vorgenommen wurden), aber auf der aktuellen Seite bleiben.** Auf diese Weise können Benutzer die Änderungen auswerten, bevor Sie mit anderen Aufgaben fortfahren.
-   **Verwenden Sie die Schaltflächen anwenden nur auf der Seite abschließende Sprachausgabe.** Apply-Schaltflächen sollten nicht auf zwischengeschalteten Seiten verwendet werden, um ein sofortiges Commit-Modell beizubehalten.
    -   **Ausnahme:** Wenn eine Einstellung geändert werden muss, können Sie die Schaltflächen anwenden auf einer hybriden Hub Seite [verwenden.](glossary.md) Weitere Informationen finden Sie unter [Interaktion](#hub-pages)mit der Hub-Seite.
-   **Geben Sie die Schaltfläche Anwenden nur dann an, wenn die Seite über Einstellungen (mindestens eine) mit Effekten verfügt, die Benutzer auf sinnvolle Weise auswerten können.** Normalerweise werden Schaltflächen anwenden verwendet, wenn Einstellungen sichtbare Änderungen vornehmen. Benutzer sollten in der Lage sein, eine Änderung anzuwenden, die Änderung zu evaluieren und auf der Grundlage dieser Auswertung weitere Änderungen vorzunehmen.
-   **Aktivieren Sie die Schaltfläche Anwenden nur, wenn ausstehende Änderungen vorhanden sind.** Andernfalls deaktivieren Sie Sie.
-   **Weisen Sie als Zugriffsschlüssel "A" zu.**

### <a name="control-panel-integration"></a>Integration der Systemsteuerung

Wenn Sie Ihr System Steuerungselement in Windows integrieren möchten, können Sie folgende Aktionen ausführen:

-   **Registrieren Sie Ihr System Steuerungselement (einschließlich Name, Beschreibung und Symbol)**, damit Windows es kennt.
-   Wenn das System Steuerungselement die oberste Ebene hat (siehe unten):
    -   Ordnen Sie Sie der entsprechenden **Kategorieseite** zu.
    -   **Stellen Sie Aufgaben Verknüpfungen (einschließlich Name, Beschreibung, Schlüsselwörter und Befehlszeile) bereit** , um primäre Aufgaben anzugeben, und ermöglichen Sie den Benutzern, direkt zu den Aufgaben zu navigieren.
-   **Geben Sie Suchbegriffe** an, um Benutzern zu helfen, ihre Aufgaben Verknüpfungen mithilfe der System Steuerungs Suchfunktion zu finden.

    Beachten Sie, dass Sie diese Informationen nur für einzelne System Steuerungselemente bereitstellen können, die Sie für vorhandene System Steuerungselemente, die Sie erweitern, nicht hinzufügen oder ändern können.

**Kategorieseiten**

-   **Fügen Sie das System Steuerungselement nur dann zu einer Kategorieseite hinzu, wenn:**

    -   Die meisten Benutzer benötigen Sie. Beispiel: Netzwerk-und Freigabe Center
    -   Es wird mehrmals verwendet. Beispiel: System
    -   Sie bietet wichtige Funktionen, die nicht an anderer Stelle verfügbar gemacht werden. Beispiel: Drucker

    System Steuerungselemente, die diese Kriterien erfüllen, werden als oberste Ebene bezeichnet.

-   **Fügen Sie das System Steuerungselement nicht zu einer Kategorieseite hinzu, wenn:**

    -   Sie wird nur selten verwendet oder für einmalige Setups verwendet. Beispiel: Welcome Center
    -   Es richtet sich an fortgeschrittene Benutzer oder IT-Experten. Beispiel: Farbverwaltung
    -   Dies gilt nicht für die aktuelle Hardware-oder Softwarekonfiguration. Beispiel: Windows SideShow (wenn von der aktuellen Hardware nicht unterstützt).

    Wenn Sie solche System Steuerungselemente aus den Kategorieseiten entfernen, werden die Elemente der obersten Ebene leichter zu finden. Wenn Sie Ihre Nutzung verwenden, sind diese System Steuerungselemente durchsuchen oder kontextabhängige Einstiegspunkte ausreichend auffindbar.

-   **Ordnen Sie das System Steuerungselement der obersten Ebene der Kategorie zu, in der die Benutzer wahrscheinlich nach dem Element suchen.** Diese Entscheidung sollte auf Benutzer Tests basieren.
-   **Sie sollten das System Steuerungselement der obersten Ebene auch der zweit wahrscheinlichsten Kategorie zuordnen.** Sie sollten einem System Steuerungselement zwei Kategorien zuordnen, wenn Benutzer wahrscheinlich in mehr als einem Ort nach den Hauptaufgaben suchen.
-   **Ordnen Sie das System Steuerungselement nicht mehr als zwei Kategorien zu.** Der Wert der Kategorisierung wird unterminiert, wenn System Steuerungselemente in verschiedenen Kategorien angezeigt werden.

**Aufgaben Verknüpfungen**

-   **Ordnen Sie das System Steuerungselement seinen primären Aufgaben zu.** Sie können bis zu fünf Aufgaben auf einer Kategorieseite anzeigen, für die Suche nach der Systemsteuerung werden jedoch zusätzliche Tasks verwendet. Verwenden Sie denselben Ausdruck wie für Aufgaben Verknüpfungen, und entfernen Sie ggf. einige Wörter, um die Verknüpfung der Aufgabe zu erhöhen.
-   **Wenn Sie Aufgaben Verknüpfungen bevorzugen, können Sie in Ihrem System Steuerungselement zu unterschiedlichen Stellen führen.** Es kann verwirrend sein, mehrere Verknüpfungen zum gleichen Ort zu haben.

**Suchbegriffe**

-   **Registrieren Sie Suchbegriffe für das System Steuerungselement, das Benutzer wahrscheinlich zur Beschreibung verwenden.** Diese Suchbegriffe sollten Folgendes umfassen:

    -   Die konfigurierten Features oder Objekte.
    -   Die primären Tasks.

    Diese Suchbegriffe sollten auf Benutzer Tests basieren.

-   **Fügen Sie auch gängige Synonyme für diese Suchbegriffe ein.** Beispielsweise sind "Monitor" und "Display" Synonyme, daher sollten beide Wörter eingeschlossen werden.
-   **Schließt Alternative rechtschreibweisen oder Wort Umbrüche ein.** Beispielsweise können Benutzer entweder nach Website und Website suchen. Sie sollten auch allgemeine fehlerhafte rechtschreibweisen bereitstellen.
-   **Sie können Singular-und Plural-nominale Formulare in Erwägung gezogen.** Das Such Feature der Systemsteuerung sucht nicht automatisch nach beiden Formularen. Geben Sie die Formulare an, für die Benutzer wahrscheinlich suchen.
-   **Verwenden Sie einfache, angespannte Verben.** Wenn Sie Connect als Suchbegriff registrieren, sucht die Suchfunktion nicht automatisch nach Verbindungen, Verbindung und Verbindung.
-   **Machen Sie sich keine Gedanken über den Fall** Bei der Suchfunktion wird die Groß-/Kleinschreibung nicht beachtet.

### <a name="standard-users-and-protected-administrators"></a>Standard Benutzer und geschützte Administratoren

**Viele Einstellungen erfordern Administratorrechte, damit Sie geändert werden können.** Wenn ein Prozess Administratorrechte erfordert, erfordert Windows Vista und höher, dass [Standard Benutzer](glossary.md) und [geschützte Administratoren](glossary.md) Ihre Berechtigungen explizit erhöhen. Dadurch wird verhindert, dass bösartiger Code mit Administratorrechten ausgeführt wird.

Weitere Informationen und Beispiele finden Sie unter [Benutzerkontensteuerung](winenv-uac.md).

### <a name="schemes-and-themes"></a>Schemas und Designs

Ein Schema ist eine benannte Auflistung von visuellen Einstellungen. Ein Design ist eine benannte Auflistung von Einstellungen im gesamten System. Beispiele für Schemas und Designs sind Anzeige, Maus, Telefon und Modem, Energieoptionen und Sound-und Audiooptionen.

-   **Benutzern das Erstellen von Schemas gestatten, wenn:**

    -   **Benutzer müssen die Einstellungen wahrscheinlich ändern.**
    -   **Benutzer haben die Wahrscheinlichkeit, dass die Einstellungen als Sammlung geändert werden.**

    Schemas sind nützlich, wenn sich Benutzer in einer anderen Umgebung befinden, z. b. in einem anderen physischen Standort (Land/Region, Zeitzone). Verwenden Ihres Computers in einer anderen Situation (bei Akkus, angedockt/nicht angedockt); oder verwenden Sie Ihren Computer für eine andere Funktion (Präsentationen, Videowiedergabe).

-   **Geben Sie mindestens ein Standardschema an.** Das Standardschema sollte in den meisten Fällen gut benannt und für die meisten Benutzer gelten. Benutzer müssen kein eigenes Schema erstellen.
-   **Stellen Sie eine Vorschau oder einen** anderen Mechanismus bereit, damit Benutzer die Einstellungen innerhalb des Schemas sehen können.

    ![Screenshot des Personalisierungs Dialogfelds ](images/winenv-ctrl-panels-image13.png)

    In diesem Beispiel zeigt das Element Personalisierungs-Systemsteuerung eine Vorschau der Desktop-und Darstellungs Einstellungen an.

-   **Stellen Sie Befehle zum Speichern und löschen bereit.** Ein RENAME-Befehl ist nicht erforderlich, wenn Benutzer Schemas umbenennen können, indem Sie unter dem gewünschten Namen speichern und das ursprüngliche Schema löschen.
-   Wenn die Einstellungen nicht ohne Schema angewendet werden können, dürfen **Benutzer nicht alle Schemas löschen.** Benutzer müssen kein eigenes Schema erstellen.
-   Wenn die Schemas nicht vollständig unabhängig sind (z. b. sind Energie Schemas vom aktuellen Laptop Modus abhängig), **Stellen Sie sicher, dass es eine einfache Möglichkeit gibt, die Einstellungen zu ändern, die für alle Schemas gelten.** Stellen Sie z. b. mit Energie Schemas sicher, dass Benutzer festlegen können, was geschieht, wenn der Deckel eines tragbaren Computers an einem einzigen Speicherort geschlossen wird.

### <a name="miscellaneous"></a>Verschiedenes

-   **Verwenden Sie die System Steuerungs Erweiterungen für Funktionen, die vorhandene Windows-Funktionen ersetzen oder erweitern.** Die folgenden System Steuerungselemente sind erweiterbar: Bluetooth-Geräte, Anzeige, Internet, Tastatur, Maus, Netzwerk, Strom, System, drahtlos (Infrarot).

### <a name="default-values"></a>Standardwerte

-   **Die Einstellungen in einem System Steuerungselement müssen den aktuellen Status des Features widerspiegeln.** Andernfalls wäre es irreführend, was zu unerwünschten Ergebnissen führen könnte. Wenn die Einstellungen z. b. die Empfehlungen, aber nicht den aktuellen Status widerspiegeln, können Benutzer auf Abbrechen klicken, anstatt Änderungen vorzunehmen. es wird also nicht geändert, dass keine Änderungen erforderlich sind.
-   **Wählen Sie den sichersten (um den Verlust von Daten oder den System Zugriff zu verhindern) und den sichersten Anfangszustand.** Nehmen Sie an, dass die meisten Benutzer die Einstellungen nicht ändern.
-   **Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie den anfänglichen Status aus, der höchstwahrscheinlich oder praktisch ist.**

## <a name="text"></a>Text

### <a name="item-names"></a>Elementnamen

-   **Wählen Sie einen beschreibenden Namen aus, der die Funktionsweise des System Steuerungs Elements eindeutig kommuniziert und unterscheidet.** Die meisten Namen beschreiben das Windows-Feature oder-Objekt, das konfiguriert wird, und werden in der klassischen Ansicht der System Steuerungs-Startseite angezeigt.
-   **Schließen Sie die Wörter "Settings", "Options", "Properties" oder "Configuration" nicht in den Namen ein.** Dies wird impliziert, und wenn Sie Sie deaktivieren, ist es für Benutzer einfacher, Sie zu scannen.

    **Falsch:**

    Barrierefreiheits Optionen

    Modem Einstellungen

    Energieoptionen

    Regions- und Sprachoptionen

    **Richtig:**

    Eingabehilfen

    Modem

    Leistung

    Regionale Formate und Sprachen

    In den richtigen Beispielen werden unnötige Wörter entfernt.

-   **Wenn das System Steuerungselement verwandte Funktionen konfiguriert, Listen Sie nur die Features auf, die zum Identifizieren des Elements erforderlich sind, und Listen Sie die Features auf, die am wahrscheinlichsten erkannt oder zuerst verwendet werden.**

    **Falsch:**

    Ordneroptionen

    Telefon-und Modem Optionen

    **Richtig:**

    Dateien und Ordner

    Modem

    In den richtigen Beispielen erhalten die primären Elemente der System Steuerungselemente einen Schwerpunkt.

-   Verwenden Sie die groß [-](glossary.md)/Kleinschreibung.

### <a name="page-titles"></a>Seitentitel

**Hinweis:** Wie bei allen Explorer-Fenstern werden die Seitentitel der Systemsteuerung in der [Adressleiste](glossary.md), jedoch nicht in der Titelleiste angezeigt.

-   **Verwenden Sie für Hub-Seiten den Elementnamen der Systemsteuerung.**
-   **Verwenden Sie für Sprachseiten eine kurze Zusammenfassung des Zwecks der Seite.** Verwenden Sie die Haupt Anweisung der Seite, wenn Sie präzise ist. Verwenden Sie andernfalls eine präzise neuanweisung der Main-Anweisung.

    ![Screenshot des Dialog Felds "Energieoptionen" ](images/winenv-ctrl-panels-image6.png)

    In diesem Beispiel werden Energieoptionen für den Seitentitel anstelle der Main-Anweisung verwendet.

-   Verwenden Sie die Groß-/Kleinschreibung.

### <a name="task-link-text"></a>Task Linktext

Die folgenden Richtlinien gelten für Links zu Aufgabenseiten, wie z. b. Aufgaben Verknüpfungen für Kategorieseiten und siehe auch Links.

-   **Wählen Sie präzise Aufgaben Namen aus, die die Aufgabe eindeutig kommunizieren und unterscheiden.** Benutzer müssen nicht ermitteln, was die Aufgabe wirklich bedeutet, oder wie Sie sich von anderen Aufgaben unterscheidet.

    **Falsch:**

    Anzeigeeinstellungen anpassen

    **Richtig:**

    Bildschirmauflösung

    Im richtigen Beispiel stellt der Wortlaut mehr Genauigkeit dar.

-   **Beibehalten einer ähnlichen Sprache zwischen Aufgaben Verknüpfungen und den Seiten, auf die Sie zeigen.** Benutzer sollten von der Seite, die von einem Link angezeigt wird, nicht überrascht sein.
-   **Entwerfen Sie für Aufgabenseiten die Haupt Anweisung, die Commit-Schaltflächen und die Aufgaben Verknüpfungen als verknüpften Textzeile.**

    **Beispiele:**

    

    |                              |                                                       |
    |------------------------------|-------------------------------------------------------|
    | Aufgaben Verknüpfung:<br/>        | Herstellen der Verbindung mit einem WLAN<br/>              |
    | Main-Anweisung:<br/> | Netzwerk auswählen, mit dem eine Verbindung hergestellt werden soll<br/>             |
    | Commit-Schaltfläche:<br/>    | Verbinden<br/>                                    |
    | Aufgaben Verknüpfung:<br/>        | Einrichten von Eltern Steuerelementen<br/>                   |
    | Main-Anweisung:<br/> | Auswählen eines Benutzers und Einrichten von Eltern Steuerelementen<br/> |
    | Commit-Schaltfläche:<br/>    | Eltern Steuerelement anwenden<br/>                     |
    | Aufgaben Verknüpfung:<br/>        | Beheben von Synchronisierungs Konflikten<br/>                |
    | Main-Anweisung:<br/> | Wie möchten Sie diesen Konflikt beheben?<br/>  |
    | Commit-Schaltfläche:<br/>    | Beheben<br/>                                    |

    

     

    Diese Beispiele zeigen die Beziehung zwischen dem Text des Aufgaben Links, der Haupt Anweisung und dem Commit-Schaltflächen Text.

-   Während Aufgaben oft mit Verben beginnen, **sollten Sie das Verb auf Kategorieseiten auslassen, wenn es sich um ein allgemeines, Konfigurations bezogenes Verb handelt, das nicht zur Kommunikation der Aufgabe beiträgt.**

    **Bestimmte, hilfreiche Verben:**

    Hinzufügen

    Azure Functions

    Verbinden

    Kopieren

    Erstellen

    Löschen

    Trennen

    Installieren

    Entfernen

    Einrichten

    Start

    Stop

    Problembehandlung

    **Generische, nicht hilfreiche Verben:**

    Anpassen

    Änderung

    Choose

    Konfigurieren

    Bearbeiten

    Verwalten

    Öffnen

    Auswählen

    Set

    Select

    Anzeigen

    Sicht

-   **Wenn der Task mehrere verwandte Features konfiguriert, Listen Sie nur die Features auf, die für die Gruppe repräsentativ sind.** Lassen Sie Details aus, die leicht abgeleitet werden können.

    **Falsch:**

    Lautstärke Symbol, stumm Schaltung, Volumesymbol

    Sprecher, Mikrofon, MIDI und Sound Schemas

    **Richtig:**

    Lautstärke

    Referenten und Mikrofon

    In den richtigen Beispielen werden nur die repräsentativen Features in der Aufgaben Verknüpfung angegeben.

-   **Sie sollten Aufgaben nur in Bezug auf Technologie formulieren, wenn Ziel Benutzer dies auch tun würden.**

    **Falsch:**

    Connectoids

    Pixel Tiefe

    dpi

    **Richtig:**

    Drucker

    Scanner

    Maus

    Die richtigen Beispiele sind technologische Begriffe, die Ziel Benutzer wahrscheinlich verwenden, während die falschen Beispiele nicht sind.

-   Verwenden Sie nur Plural Nomen, wenn das System mehr als eine Unterstützung unterstützen kann.
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Verwenden Sie keine Interpunktion am Ende.

### <a name="main-instructions"></a>Haupt Anleitung

-   **Verwenden Sie für die Hub-Seite die main-Anweisung, um das Ziel des Benutzers mit dem System Steuerungselement zu erläutern.** Die Haupt Anweisung soll Benutzern helfen, zu bestimmen, ob Sie das richtige System Steuerungselement ausgewählt haben. Beachten Sie, dass Benutzer das System Steuerungselement möglicherweise als fehlerhaft ausgewählt haben und tatsächlich nach Einstellungen suchen, die Teil eines anderen System Steuerungs Elements sind.

    **Beispiele:**

    Sorgen Sie dafür, dass der Computer sicher und auf dem neuesten Stand ist

    Optimieren Sie Ihren Computer, damit er einfacher zu erkennen, zu hören und zu steuern ist.

-   **Verwenden Sie für die Seiten des Spokes die Haupt Anweisung, um zu erläutern, was auf der Seite zu tun ist.** Die Anweisung sollte eine bestimmte Anweisung, eine imperative Richtung oder eine Frage sein. Gute Anweisungen vermitteln das Ziel des Benutzers mit der Seite, anstatt sich ausschließlich auf die Mechanismen der Bearbeitung zu konzentrieren.

    **Falsch:**

    Benachrichtigungs Aufgabe auswählen

    **Richtig:**

    Angeben, wie eingehende Informationen behandelt werden sollen

    Die richtige Version kommuniziert besser mit dem Ziel, das von der Seite erreicht wurde.

-   **Verwenden Sie nach Möglichkeit bestimmte Verben.** Bestimmte Verben sind für Benutzer aussagekräftiger als generische.
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   **Schließen Sie keine abschließenden Zeiträume ein, wenn die Anweisung eine-Anweisung ist.** Wenn die Anweisung eine Frage ist, müssen Sie ein endgültiges Fragezeichen einschließen.

### <a name="supplemental-instructions"></a>Ergänzende Anweisungen

-   **Verwenden Sie für die Hub-Seite die optionale ergänzende Anweisung, um den Zweck des System Steuerungs Elements weiter zu erläutern.**
-   **Verwenden Sie für Sprachseiten die optionale ergänzende Anweisung, um zusätzliche Informationen zu präsentieren, die hilfreich sind, um die Seite zu verstehen oder zu verwenden.** Sie können ausführlichere Informationen bereitstellen und die Terminologie definieren.
-   Verwenden Sie vollständige Sätze und Groß-/Kleinschreibung im [Satz](glossary.md).

### <a name="page-text"></a>Seiten Text

-   **Geben Sie die Haupt Anweisung im Inhalts Bereich nicht erneut an.**
-   **Verwenden Sie das Wort "page", um auf die Seite selbst zu verweisen.**
-   **Verwenden Sie die zweite Person (Sie, ihre), um den Benutzern mitzuteilen, was** in der Haupt Anweisung und im Inhalts Bereich zu tun ist. Häufig wird die zweite Person impliziert.

    **Beispiel:**

    Wählen Sie die Bilder aus, die Sie drucken möchten.

-   **Verwenden Sie die erste Person (I, me, my), damit Benutzer dem System Steuerungselement mitteilen können, was** im Inhalts Bereich geschehen soll, der auf die Haupt Anweisung antwortet.

    **Beispiel:**

    Drucken Sie die Fotos auf meiner Kamera.

### <a name="task-links"></a>Aufgaben Verknüpfungen

-   **Wählen Sie einen präzisen Linktext aus, der eindeutig kommuniziert und die Funktionsweise der Aufgabe unterscheidet.** Es sollte selbsterklärend sein und der Haupt Anweisung entsprechen. Benutzer müssen nicht ermitteln, was der Link wirklich bedeutet, oder wie er sich von anderen Links unterscheidet.
-   **Starten Sie Aufgaben Verknüpfungen immer mit einem Verb.**
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Verwenden Sie keine Interpunktion am Ende.
-   **Wenn der Link für die Aufgabe eine weitere Erläuterung erfordert, stellen Sie die Erläuterung in einem separaten Text Steuer** Element mithilfe vollständiger Sätze und Interpunktions Zeichen bereit. Fügen Sie diese Erklärungen jedoch nur hinzu, wenn Sie benötigt werden, um allen Aufgaben Verknüpfungen keine Erläuterungen hinzuzufügen, da ein anderer Aufgaben Link einen benötigt

Weitere Informationen und Beispiele finden Sie unter [Links](ctrl-command-links.md).

### <a name="commit-buttons"></a>Commit-Schaltflächen

-   **Verwenden Sie spezifische Commit-Schaltflächen Bezeichnungen, die selbst sinnvoll sind und der Main-Anweisung entsprechen.** Im Idealfall sollten Benutzer nichts anderes lesen müssen, um die Bezeichnung zu verstehen. Benutzer sind viel wahrscheinlicher, dass Befehlszeilen Bezeichnungen als statischer Text gelesen werden.
-   **Startet immer Commit-Schaltflächen Bezeichnungen mit einem Verb.**
-   **Verwenden Sie nicht schließen, fertig oder Fertigstellen.** Diese Schaltflächen Bezeichnungen eignen sich besser für andere Windows-Typen.
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Verwenden Sie keine Interpunktion am Ende.
-   Weisen Sie einen eindeutigen [Zugriffsschlüssel](glossary.md)zu.
    -   **Ausnahme:** Weisen Sie den Schaltflächen Abbrechen keine Zugriffstasten zu, da ESC der Zugriffsschlüssel ist. Dadurch können die anderen Zugriffsschlüssel leichter zugewiesen werden.

## <a name="documentation"></a>Dokumentation

Beim Verweis auf die Startseite oder die Kategorieseiten der Systemsteuerung:

-   In der Benutzerdokumentation finden Sie in der Systemsteuerung unter Verwendung der Titel-/schreibungsformatierung und Weglassen eines vorangehenden, eindeutigen Artikels.

    **Beispiel:**

    Öffnen Sie in der Systemsteuerung **Security Center**.

-   Informationen zur Programmierung und zur anderen technischen Dokumentation finden Sie auf der System Steuerungs Seite und auf der Kategorie der System Steuerungs Kategorie, ohne dass die Wörter groß geschrieben werden. Ein vorheriger, genauer Artikel ist optional.

Für System Steuerungselemente:

-   Wenn Sie auf ein einzelnes System Steuerungselement verweisen, verwenden Sie " \[ System Steuerungselement Name \] in der Systemsteuerung" oder im allgemeinen "System Steuerungselement" in der Benutzerdokumentation. Verwenden Sie das Applet, das Programm oder die Systemsteuerung nicht, um auf einzelne System Steuerungselemente zu verweisen.
-   Wenn Sie auf die Hub Seite eines System Steuerungs Elements verweisen, verwenden Sie die Seite "Haupt \[ System Steuerungselement-Elementname \] ".
-   Formatieren Sie den Namen der Systemsteuerung, wenn möglich, mit fett formatiertem Text. Andernfalls sollten Sie den Namen nur dann in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiele:

-   Öffnen Sie in der Systemsteuerung die Option **Eltern Steuerelemente**.
-   Kehren Sie zur Hauptseite für **Eltern Steuerelemente** zurück.

