---
title: Steuerungspanels
description: Verwenden Sie Systemsteuerungselemente, um Benutzer beim Konfigurieren von Features auf Systemebene und beim Ausführen verwandter Aufgaben zu unterstützen. Programme, die über eine Benutzeroberfläche verfügen, sollten stattdessen direkt über ihre Benutzeroberfläche konfiguriert werden.
ms.assetid: 845325ef-9f1d-4aa7-a5b0-685fac74a9f8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 86226e3643f741d277c0e2864870a7e81c25614a6dd5ba2e01a05c67729c26d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117853548"
---
# <a name="control-panels"></a>Steuerungspanels

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Verwenden Sie Systemsteuerungselemente, um Benutzer beim Konfigurieren von Features auf Systemebene und beim Ausführen verwandter Aufgaben zu unterstützen. Programme, die über eine Benutzeroberfläche verfügen, sollten stattdessen direkt über ihre Benutzeroberfläche konfiguriert werden.

Mit Systemsteuerung in Microsoft Windows können Benutzer Features auf Systemebene konfigurieren und zugehörige Aufgaben ausführen. Beispiele für die Featurekonfiguration auf Systemebene sind Hardware- und Softwareeinrichtung und -konfiguration, Sicherheit, Systemwartung und Benutzerkontenverwaltung.

Der Begriff Systemsteuerung bezieht sich auf das gesamte feature Windows Systemsteuerung. Einzelne Steuerungspanels werden als Systemsteuerungselemente bezeichnet. Ein Systemsteuerungselement gilt als oberste Ebene, wenn es direkt über die Startseite der Systemsteuerung oder eine Kategorieseite zugänglich ist.

![Screenshot der Sprachkategorie der Systemsteuerung ](images/winenv-ctrl-panels-image1.png)

Ein typisches Systemsteuerungselement.

Die Startseite der Systemsteuerung ist der Haupteinstiegspunkt für alle Systemsteuerungselemente. Sie listet die Elemente nach ihrer Kategorie sowie die häufigsten Aufgaben auf. Sie wird angezeigt, wenn Benutzer im Startmenü auf Systemsteuerung klicken.

Auf einer Seite mit der Systemsteuerungskategorie werden die Elemente in einer einzelnen Kategorie zusammen mit den gängigsten Aufgaben aufgelistet. Sie wird angezeigt, wenn Benutzer auf der Startseite auf einen Kategorienamen klicken.

Systemsteuerungselemente werden mithilfe von [Aufgabenflüssen](glossary.md) oder Eigenschaftenblättern implementiert. Für Windows Vista und höher sind Taskflows die bevorzugte Benutzeroberfläche(UI).

**Entwickler:** Informationen zum Erstellen von Systemsteuerungselementen finden Sie unter [Systemsteuerung Items](/previous-versions//bb776838(v=vs.85)).

**Hinweis:** Richtlinien im Zusammenhang mit [Eigenschaftenblättern](win-property-win.md) werden in einem separaten Artikel vorgestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Sollen Features auf Systemebene konfiguriert werden?** Falls nicht, verwenden Sie einen anderen Integrationspunkt. Konfigurieren Sie Ihre Anwendungsfeatures direkt über die Benutzeroberfläche mithilfe von Dialogfeldern mit Optionen, anstatt Systemsteuerung zu verwenden. Verwenden Sie für Hilfsprogramme, die nicht für Setup-, Konfigurations- oder zugehörige Aufgaben (z. B. Problembehandlung) verwendet werden, die Startmenü als Integrationspunkt.
-   **Verfügt das Feature auf Systemebene über eine eigene Benutzeroberfläche?** Wenn ja, sollten Benutzer auf dieser Benutzeroberfläche Änderungen vornehmen. Beispielsweise sollte ein Hilfsprogramm für die Systemsicherung nicht über Systemsteuerung, sondern über seine Programmoptionen konfiguriert werden.
-   **Müssen Benutzer die Konfiguration häufig ändern?** In diesem Falle (z. B. mehrmals pro Woche) sollten Sie alternative Lösungen in Betracht ziehen, möglicherweise zusätzlich zur Verwendung von Systemsteuerung. Beispielsweise kann die Einstellung Windows Mastervolume direkt über das Symbol im Benachrichtigungsbereich konfiguriert werden. Einige Einstellungen können automatisch konfiguriert werden. In Windows Explorer ermöglicht die Registerkarte Kompatibilität für Anwendungseigenschaften beispielsweise die Ausführung einer Anwendung im Farbmodus 256, anstatt dass Benutzer den Videomodus manuell ändern müssen.
-   **Sind die ZIELbenutzer IT-Experten?** Verwenden Sie in diesem Falle stattdessen ein MMC-Snap-In [(Microsoft Management Console),](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) das speziell für Systemverwaltungsaufgaben entwickelt wurde. In einigen Fällen besteht die beste Lösung darin, sowohl ein Systemsteuerungselement für allgemeine Benutzer als auch ein MMC-Snap-In für IT-Experten zu verwenden.

    ![Screenshot des Computerverwaltungsfensters ](images/winenv-ctrl-panels-image2.png)

    In diesem Beispiel ermöglicht das MMC-Snap-In "Lokale Benutzer und Gruppen" die Benutzerverwaltung für IT-Experten. Andere Benutzer verwenden das Element Benutzerkonten wahrscheinlicher in Systemsteuerung.

-   **Ist das Feature ein OEM-Feature, das nur während der anfänglichen Systemkonfiguration verwendet wird?** Verwenden Sie in diesem Falle die Windows Begrüßungscenter als Integrationspunkt.

Systemsteuerungselemente sind erforderlich, da viele Features auf Systemebene keinen offensichtlicheren oder direkteren Integrationspunkt haben. Systemsteuerung sollte jedoch nicht als "ein Ort" für alle Konfigurationseinstellungen angezeigt werden. **Programme, die über eine Benutzeroberfläche verfügen, sollten direkt über ihre Benutzeroberfläche konfiguriert werden, anstatt Systemsteuerungselemente zu verwenden.**

**Falsch:**

![Screenshot des Elements "Internetoptionen" der Systemsteuerung ](images/winenv-ctrl-panels-image3.png)

In diesem Beispiel sollte Windows Internet Explorer nicht in Systemsteuerung dargestellt werden, da die eigene Benutzeroberfläche ein besserer Integrationspunkt ist.

### <a name="create-a-new-control-panel-item-or-extend-an-existing-one"></a>Erstellen Sie ein neues Systemsteuerungselement, oder erweitern Sie ein vorhandenes Element?

Orientieren Sie sich an folgenden Fragen:

-   **Kann die Funktionalität als Aufgaben ausgedrückt werden, die in ein vorhandenes, erweiterbares Systemsteuerungselement integriert werden können?** Die folgenden Systemsteuerungselemente sind erweiterbar: Bluetooth Geräte, Anzeige, Internet, Tastatur, Maus, Netzwerk, Energie, System, Drahtlos (Mobilfunk).
-   **Ersetzen die Eigenschaften und Aufgaben die Funktionen des vorhandenen erweiterbaren Systemsteuerungselements?** Wenn ja, sollten Sie das vorhandene Systemsteuerungselement erweitern, da dies zu einer einfacheren Benutzererfahrung führt. Falls nicht, erstellen Sie ein neues Systemsteuerungselement.

## <a name="design-concepts"></a>Entwurfskonzepte

**Das Systemsteuerung Konzept basiert auf einer realen Metapher.** Eine reale Systemsteuerung ist eine Sammlung von Steuerelementen (Knöpfe, Schalter, Messgeräte und Anzeigen), die zum Überwachen und Steuern eines Geräts verwendet werden. Benutzer solcher Kontrollpanels benötigen häufig Schulungen, um zu verstehen, wie sie verwendet werden.

Im Gegensatz zu ihren realen Entsprechungen **sind Windows Systemsteuerungsentwürfe für Erstbenutzer optimiert.** Benutzer führen die meisten Systemsteuerungsaufgaben nicht sehr oft aus, weshalb sie sich in der Regel nicht erinnern, wie sie sie ausführen müssen, und sie müssen sie jedes Mal neu verleerben.

So entwerfen Sie ein Systemsteuerungselement, das nützlich und einfach zu verwenden ist:

-   Stellen Sie sicher, dass die Eigenschaften erforderlich sind.
-   Darstellen von Eigenschaften im Hinblick auf Benutzerziele anstelle von Technologie.
-   Zeigen Sie Eigenschaften auf der richtigen Ebene an.
-   Entwurfsseiten für bestimmte Aufgaben.
-   Entwurfsseiten für Standardbenutzer und geschützte Administratoren.

Bestimmen Sie beim Entwerfen und Auswerten von Elementen, die in Systemsteuerung eingeschlossen werden sollen, die allgemeinen Aufgaben, die Benutzer ausführen, und stellen Sie sicher, dass ein eindeutiger Pfad zum Ausführen dieser Aufgaben vorhanden ist. Benutzer führen in der Regel die folgenden Arten von Aufgaben mit Systemsteuerungselementen aus:

-   Anfängliche Konfiguration
-   Selten vorgenommene Änderungen (für die meisten Einstellungen)
-   Häufige Änderungen (für einige wichtige Einstellungen)
-   Zurücksetzen der Einstellungen auf einen ursprünglichen oder vorherigen Zustand
-   Problembehandlung

**Wenn Sie nur eine Sache durchführen...**

Entwerfen Sie Systemsteuerungsseiten für bestimmte Aufgaben, und stellen Sie sie im Hinblick auf Benutzerziele statt auf Technologie dar.

## <a name="usage-patterns"></a>Verwendungsmuster

Für Systemsteuerungselemente können Sie einen Aufgabenfluss oder ein Eigenschaftenblatt verwenden. Im Folgenden finden Sie ihre Verwendungsmuster:

### <a name="task-flow-patterns"></a>Aufgabenflussmuster

Aufgabenflusselemente verwenden eine Hubseite, um die übergeordneten Optionen darzustellen, und Spoke-Seiten, um die eigentliche Konfiguration auszuführen.

**Hubseiten**

-   Aufgabenbasierte Hubseiten. Diese Hubseiten stellen die am häufigsten verwendeten Aufgaben dar. Sie eignen sich am besten für einige häufig verwendete oder wichtige Aufgaben, bei denen Benutzer mehr Anleitung und Erklärung benötigen. Hubseiten verfügen nicht über Commitschaltflächen. Hybridtaskbasierte Hubseiten verfügen auch über einige Eigenschaften oder Befehle direkt darauf. Hybrid Hub-Seiten werden dringend empfohlen, wenn Benutzer höchstwahrscheinlich Systemsteuerung verwenden, um auf diese Eigenschaften und Befehle zuzugreifen.
-   Objektbasierte Hubseiten. Diese Hubseiten stellen die verfügbaren Objekte mithilfe eines Listenansicht-Steuerelements dar. Sie werden am besten verwendet, wenn es mehrere Objekte geben kann. Hubseiten verfügen nicht über Commitschaltflächen.

**Spoke-Seiten**

-   Aufgabenseiten. Diese Spoke-Seiten stellen eine Aufgabe oder einen Schritt in einer Aufgabe mit einer bestimmten aufgabenbasierten Hauptanweisung dar. Sie eignen sich am besten für Aufgaben, die von zusätzlichen Anleitungen und Erläuterungen profitieren.
-   Formularseiten. Diese Spoke-Seiten stellen eine Sammlung verwandter Eigenschaften und Aufgaben basierend auf einer allgemeinen Hauptanweisung vor. Sie werden am besten für Features verwendet, die über viele Eigenschaften verfügen und von einer direkten Single-Page-Präsentation wie erweiterten Eigenschaften profitieren.

### <a name="property-sheet-patterns"></a>Eigenschaftenblattmuster

-   Eigenschaftenblätter werden am besten in älteren Elementen mit vielen Einstellungen für fortgeschrittene Benutzer verwendet. Neue Elemente können den gleichen Effekt erzielen, wenn ein Taskfluss das Formularseitenmuster verwendet.

## <a name="guidelines"></a>Richtlinien

### <a name="property-sheet-control-panel-items"></a>Systemsteuerungselemente für Eigenschaftenblätter

-   **Verwenden Sie keine Eigenschaftenblätter für neue Systemsteuerungselemente.** Verwenden Sie stattdessen Aufgabenflüsse, um eine nahtlose Erfahrung zu schaffen und die Kategorisierungs- und Suchfunktionen der Startseite der Systemsteuerung vollständig zu nutzen.

### <a name="task-flow-control-panel-items"></a>Elemente der Taskflusssteuerung

**Allgemein**

-   **Halten Sie die wichtigsten Inhalte und Steuerelemente sichtbar, ohne zu scrollen.** Benutzer scrollen nicht, um Seiteninhalte anzuzeigen, es sei denn, sie haben einen Grund dafür. Sie können Commitschaltflächen immer sichtbar machen, indem Sie sie in einem [Befehlsbereich statt](glossary.md) im Inhaltsbereich platzieren. Unterbricht Seiten nicht nur, um Bildlauf zu vermeiden.
    -   **Sie können lange Seiten vertikal scrollen,** solange die wichtigsten Steuerelemente sichtbar sind, ohne zu scrollen.
    -   **Verwenden Sie kein horizontales Scrollen.** Gestalten Sie stattdessen den Seiteninhalt neu, und verwenden Sie vertikales Scrollen. Seiten können nur dann horizontale Bildlaufleisten enthalten, wenn sie sehr schmal sind.
-   **So navigieren Sie zwischen Seiten:**
    -   Verwenden [Sie Aufgabenlinks,](glossary.md) um eine Aufgabe zu starten.
    -   Verwenden Sie Aufgabenlinks oder eine Schaltfläche Weiter, um zur nächsten Seite in einer mehrstufigen Aufgabe zu navigieren.
    -   Verwenden Sie Commitschaltflächen, um eine Aufgabe auszuführen.
    -   Verwenden Sie Schaltfläche "Zurück" in der Menüleiste, um zu zuvor angezeigten Seiten zurückzukehren. Fügen Sie dem Befehlsbereich keine Schaltfläche "Zurück" hinzu.
    -   Verwenden Sie die Adressleiste, um direkt zur Startseite der Systemsteuerung zurückzukehren.
    -   Verwenden Sie auch Links im Aufgabenbereich, um zu Seiten in anderen Systemsteuerungselementen zu navigieren. Andernfalls sollte die Navigation innerhalb eines einzelnen Systemsteuerungselements bleiben.
-   **Legen Sie nur die Startseite der Systemsteuerung in der Adressleiste ab.** Wenn Sie auf diesen Link klicken, wird die Startseite der Systemsteuerung wieder angezeigt, und alle in Bearbeitungen arbeitenden Arbeiten werden ohne Bestätigung [verabsendet.](https://msdn.microsoft.com/library/windows/desktop/aa511273.aspx)
-   **Legen Sie auf den Systemsteuerungsseiten keine Befehlsschaltfläche Schließen ab.** Benutzer können ein Systemsteuerungsfenster mithilfe der Schaltfläche Schließen auf der Titelleiste schließen.

**Aufgabenlinks und Schaltflächen**

-   **Wenn eine Seite über einen kleinen Satz fester Optionen verfügt, verwenden Sie Aufgabenlinks anstelle einer Kombination aus Optionsfeldern und einer Schaltfläche Weiter.** Dadurch können Benutzer mit nur einem Klick eine Antwort auswählen.
-   Sie können Aufgabenlinks und Schaltflächen an den folgenden Stellen (in der Reihenfolge der Aufholbarkeit) platziert werden:
    -   Der [Befehlsbereich](glossary.md) (nur für Befehlsschaltflächen auf Spoke-Seiten).
    -   Der [Inhaltsbereich:](glossary.md)
        -   Befehlsschaltflächen
        -   Aufgabenlinks
        -   Weitere Links
    -   Links im [Aufgabenbereich](glossary.md) (nur Hubseiten).
-   **Legen Sie die Position von Aufgabenlinks und Schaltflächen auf der Wichtigkeit und der Notwendigkeit der Aufserfbarkeit fest.**
    -   **Legen Sie nur Commitschaltflächen im Befehlsbereich ab.**
    -   **Legen Sie wichtige Aufgaben im Inhaltsbereich ab.** Befehlsschaltflächen ziehen in der Regel die meiste Aufmerksamkeit auf sich, daher reservieren Sie sie für Befehle, die Benutzern angezeigt werden müssen. Aufgabenlinks ziehen auch Aufmerksamkeit, aber weniger als Befehlsschaltflächen.
    -   **Reservieren Sie den Aufgabenbereich und einfache Links für sekundäre (weniger wichtige) Aufgaben.** Der Aufgabenbereich ist der am wenigsten erkennbare Bereich einer Aufgabenseite, und einfache Links sind nicht so sichtbar wie Befehlsschaltflächen und Aufgabenlinks.
-   Für Aufgabenlinks, die im Inhaltsbereich dargestellt werden:
    -   **Wenn mehr als sieben Links enthalten sind, gruppen Sie die Links in Kategorien.** Geben Sie Überschriften für jede der Gruppen an.
    -   **Stellen Sie die Links für weniger als sieben Links in einer einzelnen Gruppe ohne Überschrift vor.**
-   **Stellen Sie Aufgabenlinks und Schaltflächen in einer logischen Reihenfolge vor.** Aufgabenlinks vertikal auflisten, Befehlsschaltflächen horizontal.
-   Unterteilen Sie **die Befehle innerhalb von Kategorien in verknüpfte Gruppen.** Stellen Sie die Aufgabengruppen vor, indem Sie die am häufigsten verwendeten zuerst platzieren und innerhalb jeder Gruppe die am häufigsten verwendeten Aufgaben an erster Stelle platzieren. **Die resultierende Reihenfolge sollte ungefähr der Wahrscheinlichkeit der Verwendung folgen, aber auch einen logischen Fluss haben.**
    -   **Ausnahme:** Aufgabenlinks, die dazu führen, dass alles gemacht wird, sollten zuerst platziert werden.
-   **Wenn viele Aufgabenlinks** zur Verfügung stehen, sollten Sie den wichtigsten Aufgaben ein 24 x 24 Pixel großes Symbol und zwei Textzeilen verwenden. Verwenden Sie für weniger wichtige Aufgaben ein 16 x 16 Pixel großes Symbol oder kein Symbol und eine einzelne Zeile mit Linktext.

    ![Screenshot von Elementen mit großen und kleinen Symbolen ](images/winenv-ctrl-panels-image4.png)

    In diesem Beispiel erhalten wichtige Befehle eine wichtigere Darstellung.

-   **Eine klare physische Trennung zwischen häufig verwendeten Befehlen und destruktiven Befehlen.** Andernfalls können Benutzer versehentlich auf destruktive Befehle klicken. Möglicherweise müssen Sie Ihre Befehle neu anordnen, um destruktive Befehle zusammenzubringen.
-   **Stellen Sie den Mechanismus zum Rückgängig machen von Befehlen direkt auf der Seite zur Verfügung.** Benutzer sollten nicht an einer anderen Stelle navigieren müssen, um einen Fehler rückgängig zu machen.
-   **Verwenden Sie für Aufgabenlinks entweder alle Standardsymbole für Aufgabenlinks oder alle benutzerdefinierten Symbole.** Mischen Sie sie nicht. Erwägen Sie die Verwendung benutzerdefinierter Symbole nur, wenn Folgendes zu beachten ist:
    -   Sie unterstützen Benutzer dabei, die Aufgaben zu verstehen.
    -   Sie entsprechen den [Symbolstandards von Icon.](vis-icons.md)
    -   Sie haben eine unaufdringliche Darstellung.

**Dialogfelder**

Bei der Verwendung von Aufgabenflüssen möchten Sie in der Regel, dass eine Aufgabe innerhalb eines einzelnen Fensters von Seite zu Seite fließen soll, aber die folgenden Umstände sind Ausnahmen. Verwenden Sie Dialogfelder unter den folgenden Umständen:

-   Zum Auffordern von Benutzern zur Eingabe eines Administratorbenutzernamens und -kennworts. Verwenden Sie zu diesem Zweck immer das Dialogfeld Anmeldeinformations-Manager. (Sollte modal [sein.)](glossary.md)
-   Um einen befehlsbasierten Befehl mithilfe eines Aufgabendialogfelds oder eines Meldungsfelds zu bestätigen. (Sollte modal sein.)
-   So erhalten Sie Eingaben für die Befehle "Neu", "Hinzufügen", "Speichern unter", "Umbenennen" und "Drucken".

    ![Screenshot des Dialogfelds "Netzwerkstandorte löschen" ](images/winenv-ctrl-panels-image5.png)

    In diesem Beispiel wird der Befehl Löschen in einem Dialogfeld anstelle einer separaten Seite ausgeführt.

-   Zum Ausführen sekundärer, eigenständiger Aufgaben. Mithilfe [eines moduslosen sekundären](glossary.md)Fensters können solche Aufgaben unabhängig und außerhalb des Hauptaufgabenflusses ausgeführt werden.

### <a name="hub-pages"></a>Hubseiten

**Allgemein**

-   Verwenden Sie aufgabenbasierte Hubseiten, wenn:
    -   **Es gibt eine kleine Anzahl häufig verwendeter oder wichtiger Aufgaben.**
    -   **Die Konfiguration umfasst ein oder zwei Objekte** (Beispiele: Monitore, Tastatur, Maus, Gamecontroller).
    -   **Die Konfiguration wird systemweit angewendet** (Beispiele: Datum und Uhrzeit, Sicherheit, Energieoptionen).
-   Verwenden Sie objektbasierte Hubseiten in folgenden Folgenden:
    -   **Die Konfiguration kann mehrere Objekte umfassen** (Beispiele: Benutzerkonten, Netzwerkverbindungen, Drucker).
    -   **Die Konfiguration gilt nur für das ausgewählte Objekt**.
-   **Verwenden Sie keine Hubseite,** wenn das Systemsteuerungselement über eine einzelne Seite verfügt, die alle beteiligten Aufgaben und Eigenschaften enthält.

**Objektlisten**

-   **Listen Sie Elemente in logischer Reihenfolge auf.** Sortiert benannte Objekte in alphabetischer Reihenfolge, Zahlen in numerischer Reihenfolge und Datumsangaben in chronologischer Reihenfolge.
-   Geben Sie für objektbasierte **Hubs Objektansichtsbefehle im Aufgabenbereich an, wenn die Möglichkeit zum Ändern der Ansicht für die Aufgaben wichtig ist.** Die Möglichkeit zum Ändern von Ansichten ist wichtig, wenn viele Objekte vorhanden sind und die Standardpräsentation nicht für alle Szenarien gut funktioniert. Benutzer können die Listenansicht auch dann ändern, wenn keine expliziten Befehle über das Kontextmenü der Listenansicht vorhanden sind, aber weniger auffindbar sind.

Weitere Richtlinien zum Darstellen von Objektlisten finden Sie unter [Listenansichten.](ctrl-list-views.md)

**Interaktion**

-   **Legen Sie keine Commitschaltflächen auf Hubseiten ab.** Hubseiten sind grundsätzlich Startpunkte. Benutzer "committen" niemals Hubseiten, die sie nie mit ihnen erledigt haben. Und Commitschaltflächen auf Hubseiten machen alle von einem Hub initiierten Aufgaben verwirrend (Benutzer fragen sich, ob für diese Aufgaben ein Commit ausgeführt werden muss).
    -   **Ausnahme:** Wenn zum Ändern einer Einstellung [erhöhte Rechte](glossary.md)erforderlich sind, geben Sie eine Schaltfläche Anwenden mit einem [Sicherheitsschildsymbol an.](winenv-uac.md) Deaktivieren Sie die Commitschaltfläche, nachdem die Änderungen angewendet wurden.
-   **Erwägen Sie, die nützlichsten Eigenschaften direkt auf Hubseiten zu verwenden.** Solche Hybrid Hub-Seiten werden dringend empfohlen, wenn Benutzer höchstwahrscheinlich Systemsteuerung verwenden, um auf diese Eigenschaften zuzugreifen.

    ![Screenshot der Hubseite "Energieoptionen" ](images/winenv-ctrl-panels-image6.png)

    In diesem Beispiel enthält das Energieoptionen Systemsteuerungselement direkt auf der Hubseite die nützlichsten Einstellungen.

-   **Verwenden Sie ein Modell mit sofortigem Commit für alle Einstellungen auf Hybrid Hub-Seiten, damit Änderungen sofort vorgenommen werden.** Auch hier committen Benutzer nie eine Hubseite. Wenn für eine Einstellung eine Commitschaltfläche erforderlich ist, legen Sie sie nicht auf einer Hubseite ab.
-   **Erwägen Sie, einfache Befehle mit einem Schritt direkt auf Hubseiten zu verwenden, anstatt Navigationslinks zu verwenden.**
-   **Bestätigen Sie die befehle an Ort und Stelle, deren Auswirkungen nicht einfach rückgängig zu werden sind.** Verwenden Sie ein [Aufgabendialogfeld](win-dialog-box.md) oder [ein Meldungsfeld.](glossary.md)

    ![Screenshot des Dialogfelds "Löschen bestätigen" ](images/winenv-ctrl-panels-image7.png)

    In diesem Beispiel wird der Befehl Löschen mit einem Dialogfeld bestätigt.

-   **Identifizieren Sie für aufgabenbasierte Hubseiten jede Aufgabe mit einem Aufgabenlink und einem Symbol.** Sie können auch eine optionale Beschreibung für jeden Link angeben. Versuchen Sie jedoch, die Aufgabenlinks selbsterklärend zu gestalten und optionale Beschreibungen nur für Links bereitzustellen, die sie wirklich benötigen.

    ![Screenshot der Seite "Computerleistungshub" ](images/winenv-ctrl-panels-image8.png)

    In diesem Beispiel verfügt jede Aufgabe über einen Aufgabenlink und ein Symbol.

-   **Bei objektbasierten Hubseiten wählt ein Einzelklick Objekte aus, und durch Doppelklicken wird ein Objekt ausgewählt, und es wird zur Standardseite navigiert.** Die Standardseite ist in der Regel eine Eigenschaftenseite oder eine aufgabenbasierte Hubseite.
-   **Eine objektbasierte Hubseite kann zu einem aufgabenbasierten Hub für die ausgewählten Objekte navigieren.** Solche sekundären Hubs sollten jedoch vermieden werden, da sie ein Systemsteuerungselement zu indirekt wirken lassen.

**Aufgabenbereiche**

Verwenden Sie Aufgabenbereiche, um Links zu Befehlen, Ansichten und verwandten Systemsteuerungselementen anzuzeigen.

-   Für Aufgabenbereiche in aufgabenbasierten Hubs zeigen Sie Links in der folgenden Reihenfolge an:
    -   **Sekundäre Befehle.** Stellen Sie primäre Aufgaben nur im Inhaltsbereich dar. Verwenden Sie den Aufgabenbereich für sekundäre, optionale Aufgaben. Stellen Sie sich eine aufgabe primäre Aufgabe vor, wenn Benutzer sie in wichtigen Szenarien ermitteln müssen. sekundär, wenn es für Benutzer akzeptabel ist, sie nicht zu ermitteln.
    -   **Siehe auch**. Die optionalen Links, die zu verwandten Systemsteuerungselementen navigieren.
-   Für Aufgabenbereiche in objektbasierten Hubs werden Links in der folgenden Reihenfolge angezeigt:
    -   **Objektansichten**. Die optionalen Links, die zum Steuern der Darstellung der Objekte verwendet werden.
    -   **Die Befehle wurden korrigiert.** Die Befehle, die unabhängig von den derzeit ausgewählten Objekten sind.
    -   **Kontextbezogene Befehle.** Die Befehle, die von den derzeit ausgewählten Objekten abhängen und daher nicht immer angezeigt werden.
    -   **Siehe auch**. Die optionalen Links, die zu verwandten Systemsteuerungselementen navigieren.
-   **Verwenden Sie keine Aufgabenbereiche auf Spoke-Seiten.** Im Gegensatz zu Hubseiten sollten sich Spoke-Seiten auf das Abschließen der Aufgabe konzentrieren. Sie möchten die Benutzer nicht dazu auffordern, vor abschluss zu navigieren.

**Siehe auch Links.**

-   **Geben Sie links im Aufgabenbereich anzeigen an, um Benutzern zu helfen, verwandte Systemsteuerungselemente oder das richtige Systemsteuerungselement zu finden, wenn sie das falsche Element haben.** Link zu Elementen, die Benutzer ihrem Systemsteuerungselement wahrscheinlich zuordnen.

    ![Screenshot Info-Center Links zu "Siehe auch" ](images/winenv-ctrl-panels-image9.png)

    In diesem Beispiel ist das Element der Action Center-Systemsteuerung mit verwandten Systemsteuerungselementen verknüpft.

-   **Link zu einer bestimmten Aufgabenseite, wenn benutzer dies eher erkennen.** Andernfalls verknüpfen Sie mit dem gesamten Systemsteuerungselement. Verwenden Sie den Namen der Systemsteuerung, ohne den Ausdruck (Systemsteuerung) hinzuzufügen.

### <a name="spoke-pages"></a>Spoke-Seiten

**Allgemein**

-   **Verwenden Sie Aufgabenseiten für häufig verwendete oder wichtige Aufgaben, bei denen Benutzer weitere Anleitungen und Erläuterungen benötigen.**
-   **Verwenden Sie Formularseiten für Features, die viele Einstellungen aufweisen und von einer direkten, einseitigen Darstellung profitieren.** Die idealen Aufgaben für solche Seiten umfassen in der Regel offensichtliche Änderungen an einigen einfachen Eigenschaften.
-   **Verwenden Sie keine Aufgabenbereiche auf Spoke-Seiten.**

**Interaktion**

-   **Versuchen Sie, die Hauptaufgaben auf eine einzelne Seite zu beschränken.** Wenn mehr als eine Seite erforderlich ist, haben Sie die möglichkeit:
    -   **Verwenden Sie Spoke-Zwischenseiten für zusätzliche oder optionale Schritte.** Zwischen-Spoke-Seiten werden von der letzten Spoke-Seite ausgeführt.
    -   **Verwenden Sie unabhängige Fenster für unabhängige Hilfsaufgaben.** Unabhängige Fenster werden eigenständig und unabhängig von der Hauptaufgabe ausgeführt.

Dadurch wird die Bedeutung der Commitschaltflächen für die Hauptaufgabe klar und eindeutig. Benutzer sollten immer sicher sein, dass sie verstehen, wozu sie sich committen.

-   **Verwenden Sie keine Links anzeigen innerhalb eines Taskflows.** Diese links zu verwandten, aber unterschiedlichen Systemsteuerungselementen. Obwohl das Navigieren zu einem anderen Element auf Hubseiten akzeptabel ist, befindet es sich nicht auf Spoke-Seiten, da dies die Aufgabe unterbricht.
-   **Verwenden Sie keine Spoke-Seiten für einfache Eingaben oder Bestätigungen.** Verwenden Sie stattdessen modale Dialogfelder.

**Interaktion (Spoke-Zwischenseiten)**

-   **Verwenden Sie Aufgabenlinks oder die Schaltfläche Weiter, um zur nächsten Seite zu navigieren.** Der Weg zum nächsten Schritt sollte immer offensichtlich sein.
-   **Sie können Navigationslinks zu optionalen Aufgabenschritten haben.** Um Verwirrung zu vermeiden, wenn Benutzer sich an die Aufgabe committen, sollten diese zusätzlichen Seiten Zwischenseiten innerhalb desselben Systemsteuerungselements sein. Sie dürfen keine Commitschaltflächen haben, sollten aber committet werden, wenn für die Hauptaufgabe ein Commit ausgeführt wird.

**Interaktion (letzte Spoke-Seiten)**

-   **Verwenden Sie Commitschaltflächen, um eine Aufgabe abzuschließen.** Verwenden Sie ein [verzögertes Commitmodell](glossary.md) für Spoke-Seiten, sodass Änderungen erst vorgenommen werden, wenn ein expliziter Commit ausgeführt wird (wenn Benutzer mithilfe von Zurück, Schließen oder der Adressleiste weg navigieren, werden Änderungen abgebrochen). Die Commitschaltflächen sind ein visueller Hinweis darauf, dass der Benutzer eine Aufgabe abschließen wird. Verwenden Sie für diesen Zweck keine Links.
-   **Bestätigen Sie keine Commitschaltflächen (einschließlich Abbrechen).** Dies kann mühsam sein. Ausnahmen:
    -   Die Aktion hat erhebliche Folgen und kann, falls falsch, nicht sofort behoben werden.
    -   Die Aktion kann zu einem erheblichen Verlust der Zeit oder des Aufwands des Benutzers führen.
    -   Die Aktion ist eindeutig inkonsistent mit anderen Aktionen.
-   **Bestätigen Sie nicht, ob Benutzer Änderungen verwerfen,** indem Sie mit "Zurück", "Schließen" oder der Adressleiste weg navigieren. Sie können jedoch bestätigen, dass eine potenziell unbeabsichtigte Navigation zu einem erheblichen Verlust der Zeit oder des Aufwands des Benutzers führen kann.
-   **Verwenden Sie keine Befehls- oder Navigationslinks** (einschließlich Siehe auch Links). Auf den letzten Spoke-Seiten sollten Benutzer die Aufgabe explizit abschließen oder abbrechen. Benutzern sollte nicht empfohlen werden, an einer anderen Stelle zu navigieren, da dies die Aufgabe wahrscheinlich implizit abbrechen würde.
-   **Wenn Benutzer eine Aufgabe abschließen oder abbrechen, sollten sie zurück an die Hubseite gesendet werden, von der die Aufgabe gestartet wurde.** Wenn keine solche Seite verfügbar ist, schließen Sie stattdessen das Systemsteuerungsfenster. Gehen Sie nicht davon aus, dass Spoke-Seiten immer von einer anderen Seite gestartet werden.
-   **Entfernen Sie die veralteten "committed"-Seiten** aus dem Back-Stack des Windows-Explorers, wenn Sie Benutzer auf die Seite zurückführen, von der die Aufgabe gestartet wurde. Benutzer sollten nie die Seiten sehen, für die sie beim Klicken auf die Schaltfläche "Zurück". Benutzer sollten immer zusätzliche Änderungen vornehmen, indem sie die Aufgabe vollständig wiederholen, anstatt auf Zurück zu klicken, um veraltete Seiten zu ändern.
    -   **Entwickler:** Sie können diese veralteten Seiten mithilfe der APIs ITravelLog::FindTravelEntry() und ITravelLogEx::D eleteEntry() entfernen.

**Commitschaltflächen**

**Hinweis:** Schaltflächen zum Abbrechen werden als Commitschaltflächen betrachtet.

-   **Bestätigen Sie Aufgaben mithilfe von Commitschaltflächen, bei denen es sich um spezifische Antworten auf die Hauptanweisung handelt, anstatt mit generischen Bezeichnungen wie OK.** Die Bezeichnungen auf commit-Schaltflächen sollten selbst sinnvoll sein. Vermeiden Sie die Verwendung von OK, da es sich nicht um eine bestimmte Antwort auf die Main-Anweisung handelt und daher leichter falsch verstanden werden kann. Darüber hinaus wird OK in der Regel mit modalen Dialogfeldern verwendet und impliziert fälschlicherweise das Schließen des Fensters des Systemsteuerungselements.
    -   **Ausnahmen:**
        -   Verwenden Sie OK für Seiten ohne Einstellungen.
        -   Verwenden Sie OK, wenn die spezifische Antwort immer noch generisch ist, z. B. Speichern, Auswählen oder Auswählen, z. B. beim Ändern einer bestimmten Einstellung oder einer Sammlung von Einstellungen.
        -   Verwenden Sie OK, wenn die Seite Optionsfelder enthält, die Antworten auf die Main-Anweisung sind. Um das Modell mit verzögerten Commits zu verwalten, können Sie keine Aufgabenlinks auf einer abschließenden Spoke-Seite verwenden.

            ![Screenshot der Webeinschränkungen mit der Schaltfläche "OK" ](images/winenv-ctrl-panels-image10.png)

            In diesem Beispiel sind die Optionsfelder, nicht die Commitschaltflächen, Antworten auf die Main-Anweisung.
-   **Geben Sie die Schaltfläche Abbrechen an, damit Benutzer Änderungen explizit abbrechen können.** Während Benutzer eine Aufgabe implizit abbrechen können, indem sie ihre Änderungen nicht bestätigen, können sie dies mit größerer Sicherheit über die Schaltfläche Abbrechen tun.
    -   **Ausnahme:** Geben Sie keine Schaltfläche Abbrechen für Aufgaben an, bei denen Benutzer keine Änderungen vornehmen können. Die Schaltfläche OK hat in diesem Fall die gleiche Wirkung wie Abbrechen.
-   **Verwenden Sie die Commitschaltflächen Schließen, Fertig oder Fertig stellen nicht.** Diese Schaltflächen werden in der Regel mit modalen Dialogfeldern verwendet und implizieren fälschlicherweise das Schließen des Systemsteuerungselementfensters. Benutzer können das Fenster mithilfe der Schaltfläche Schließen auf der Titelleiste schließen. Außerdem sind Fertig und Fertig stellen irreführend, da Benutzer auf die Seite zurückgegeben werden, auf der die Aufgabe gestartet wurde, sodass sie nicht wirklich fertig sind.
-   **Deaktivieren Sie keine Commitschaltflächen.** Andernfalls müssen Benutzer die Gründe für die Deaktivierung der Commitschaltflächen ableiten. Es ist besser, commit-Schaltflächen aktiviert zu lassen und bei jedem Problem eine hilfreiche Fehlermeldung zu geben.
-   **Stellen Sie sicher, dass die Commitschaltflächen auf der Seite angezeigt werden, ohne zu scrollen.** Wenn die Seite lang ist, können Sie Commitschaltflächen [](glossary.md)immer sichtbar machen, indem Sie sie in einem Befehlsbereich statt im Inhaltsbereich platzieren.

    ![Screenshot des Dialogfelds "Automatische Wiedergabe" ](images/winenv-ctrl-panels-image11.png)

    In diesem Beispiel ist die Größe des Inhaltsbereichs ungebunden, sodass die Commitschaltflächen im Befehlsbereich platziert werden.

-   Richten Sie die Commitschaltflächen rechts aus, und verwenden Sie diese Reihenfolge (von links nach rechts): Schaltflächen für positive Commits, Abbrechen und Anwenden.

**Vorschauschaltflächen**

-   Stellen Sie sicher, dass die Schaltfläche Vorschau bedeutet, dass die ausstehenden Änderungen jetzt angewendet werden, aber die aktuellen Einstellungen wiederhergestellt werden, wenn Benutzer von der Seite weg navigieren, ohne die Änderungen **zu übernehmen.**
-   **Sie können Vorschauschaltflächen auf jeder Spoke-Seite verwenden.** Hubseiten benötigen keine Vorschauschaltflächen, da sie ein [Direkt-Commit-Modell verwenden.](glossary.md)
-   **Erwägen Sie die Verwendung einer Vorschauschaltfläche anstelle einer Schaltfläche Anwenden für Systemsteuerungsseiten.** Vorschauschaltflächen sind für Benutzer einfacher zu verstehen und können auf jeder Spoke-Seite verwendet werden.
-   **Geben Sie nur dann eine Vorschauschaltfläche an, wenn die Seite über Einstellungen (mindestens eine) mit Auswirkungen verfügt, die Benutzern angezeigt werden können.** Benutzer sollten in der Lage sein, eine Vorschau einer Änderung anzuzeigen, die Änderung zu bewerten und weitere Änderungen basierend auf dieser Auswertung vorzunehmen.
-   **Aktivieren Sie immer die Schaltfläche Vorschau.**

**Livevorschauen**

Ein Systemsteuerungselement verfügt über eine Livevorschau, wenn die Auswirkungen von Änderungen auf einer Spoke-Seite sofort angezeigt werden.

-   **Erwägen Sie die Verwendung der Livevorschau für Anzeigeeinstellungen, wenn Folgendes zu beachten ist:**
    -   Der Effekt ist offensichtlich, da er in der Regel für den gesamten Monitor gilt.
    -   Der Effekt kann ohne erhebliche Verzögerung angewendet werden.
    -   Der Effekt ist sicher und kann problemlos rückgängig gemacht werden.

        ![Screenshot des Dialogfelds "Farbeinstellungen ändern" ](images/winenv-ctrl-panels-image12.png)

        In diesem Beispiel werden die Auswirkungen der Windows Farb- und Darstellungseinstellungen sofort angezeigt. Dadurch können Benutzer änderungen mit minimalem Aufwand vornehmen.

-   **Verwenden Sie Änderungen speichern und Abbrechen für die Commitschaltflächen.** "Änderungen speichern" behält die aktuellen Einstellungen bei, während Abbrechen auf die ursprünglichen Einstellungen zurückwechselt. "Änderungen speichern" wird anstelle von OK verwendet, um deutlich zu machen, dass noch keine Änderungen in der Vorschau angewendet wurden.
-   **Geben Sie keine Schaltfläche Anwenden an.** Die Livevorschau macht Anwenden überflüssig.
-   **Stellen Sie alle Änderungen wieder auf, wenn Benutzer mithilfe von** Zurück, Schließen oder der Adressleiste weg navigieren. Um Änderungen zu erhalten, müssen Benutzer diese explizit commiten.

**Schaltflächen anwenden**

-   Stellen Sie sicher, dass die Schaltfläche Anwenden bedeutet, dass die ausstehenden Änderungen (seit dem Start der Aufgabe oder der letzten Anwendung vorgenommen) angewendet werden, aber auf **der aktuellen Seite bleiben.** Auf diese Weise können Benutzer die Änderungen auswerten, bevor sie mit anderen Aufgaben arbeiten.
-   **Verwenden Sie Schaltflächen nur auf endgültigen Spoke-Seiten anwenden.** Schaltflächen anwenden sollten nicht auf Spoke-Zwischenseiten verwendet werden, um ein Direkt-Commit-Modell zu verwalten.
    -   **Ausnahme:** Sie können Schaltflächen anwenden auf einer Hybrid Hub-Seite verwenden, wenn das Ändern einer Einstellung eine Erhöhung [von erfordert.](glossary.md) Weitere Informationen finden Sie unter [Hub-Seiteninteraktion.](#hub-pages)
-   **Geben Sie nur dann eine Schaltfläche Anwenden an, wenn die Seite einstellungen (mindestens eine) mit Effekten enthält, die Benutzer auf sinnvolle Weise auswerten können.** In der Regel werden Schaltflächen anwenden verwendet, wenn Einstellungen sichtbare Änderungen vornehmen. Benutzer sollten in der Lage sein, eine Änderung anzuwenden, die Änderung zu bewerten und weitere Änderungen basierend auf dieser Auswertung vorzunehmen.
-   **Aktivieren Sie die Schaltfläche Anwenden nur, wenn Änderungen ausstehen.** Andernfalls deaktivieren Sie es.
-   **Weisen Sie "A" als Zugriffsschlüssel zu.**

### <a name="control-panel-integration"></a>Integration der Systemsteuerung

Zum Integrieren Ihres Systemsteuerungselements in Windows haben Sie dies:

-   **Registrieren Sie Ihr Systemsteuerungselement (einschließlich Name,** Beschreibung und Symbol), damit Windows es kennt.
-   Wenn Sich ihr Systemsteuerungselement auf der obersten Ebene befindet (siehe unten):
    -   Ordnen Sie sie der entsprechenden **Kategorieseite zu.**
    -   **Stellen Sie Aufgabenlinks (einschließlich Name, Beschreibung,** Schlüsselwörter und Befehlszeile) zur Verfügung, um primäre Aufgaben anzugeben und Benutzern zu ermöglichen, direkt zu den Aufgaben zu navigieren.
-   **Geben Sie Suchbegriffe** an, mit deren Hilfe Benutzer ihre Aufgabenlinks mithilfe Systemsteuerung suchen können.

    Beachten Sie, dass Sie diese Informationen nur für einzelne Systemsteuerungselemente bereitstellen können, die Sie für vorhandene Systemsteuerungselemente, die Sie erweitern, nicht hinzufügen oder ändern können.

**Kategorieseiten**

-   **Fügen Sie Ihr Systemsteuerungselement einer Kategorieseite nur hinzu, wenn:**

    -   Die meisten Benutzer benötigen sie. Beispiel: Netzwerk- und Freigabecenter
    -   Sie wird häufig verwendet. Beispiel: System
    -   Sie bietet wichtige Funktionen, die nicht an anderer Stelle verfügbar gemacht werden. Beispiel: Drucker

    Systemsteuerungselemente, die diese Kriterien erfüllen, werden als oberste Ebene bezeichnet.

-   **Fügen Sie Ihr Systemsteuerungselement nicht zu einer Kategorieseite hinzu, wenn:**

    -   Es wird selten für einmaliges Setup verwendet oder verwendet. Beispiel: Begrüßungscenter
    -   Sie richtet sich an fortgeschrittene Benutzer oder IT-Experten. Beispiel: Farbverwaltung
    -   Dies gilt nicht für die aktuelle Hardware- oder Softwarekonfiguration. Beispiel: Windows SideShow (falls nicht von der aktuellen Hardware unterstützt).

    Wenn Sie solche Systemsteuerungselemente von den Kategorieseiten entfernen, sind die Elemente der obersten Ebene leichter zu finden. Aufgrund ihrer Verwendung sind diese Systemsteuerungselemente über Such- oder kontextbezogene Einstiegspunkte ausreichend erkennbar.

-   **Ordnen Sie Ihr Systemsteuerungselement der obersten Ebene der Kategorie zu, unter der Benutzer am wahrscheinlichsten nach ihm suchen.** Diese Entscheidung sollte auf Benutzertests basieren.
-   **Erwägen Sie, ihr Systemsteuerungselement der obersten Ebene auch der zweitwahrscheinlichsten Kategorie zu zuordnen.** Sie sollten ein Systemsteuerungselement zwei Kategorien zuordnen, wenn Benutzer wahrscheinlich an mehr als einem Ort nach seinen Hauptaufgaben suchen.
-   **Ordnen Sie Ihr Systemsteuerungselement nicht mehr als zwei Kategorien zu.** Der Wert der Kategorisierung wird verfeinert, wenn Systemsteuerungselemente in mehreren Kategorien angezeigt werden.

**Aufgabenlinks**

-   **Ordnen Sie ihr Systemsteuerungselement den primären Aufgaben zu.** Sie können bis zu fünf Aufgaben auf einer Kategorieseite anzeigen, für die Systemsteuerungssuche werden jedoch zusätzliche Aufgaben verwendet. Verwenden Sie denselben Ausdruck wie für Aufgabenlinks, und entfernen Sie möglicherweise einige Wörter, um die Aufgabenlinks prägnanter zu machen.
-   **Es wird bevorzugt, dass Aufgabenlinks zu unterschiedlichen Stellen in Ihrem Systemsteuerungselement führen.** Mehrere Links zum gleichen Ort können verwirrend sein.

**Suchbegriffe**

-   **Registrieren Sie Suchbegriffe für Ihr Systemsteuerungselement, das Benutzer wahrscheinlich verwenden, um es zu beschreiben.** Diese Suchbegriffe sollten Folgendes umfassen:

    -   Die konfigurierten Features oder Objekte.
    -   Die primären Aufgaben.

    Diese Suchbegriffe sollten auf Benutzertests basieren.

-   **Schließen Sie auch allgemeine Synonyme für diese Suchbegriffe ein.** Monitor und Anzeige sind beispielsweise Synonyme, daher sollten beide Wörter eingeschlossen werden.
-   **Fügen Sie alternative Schreibweisen oder Wörterumbrüche ein.** Beispielsweise können Benutzer entweder nach Website und Website suchen. Erwägen Sie auch die Bereitstellung häufiger Falschschreibfehler.
-   **Betrachten Sie Singular- und Plural nomen-Formen.** Das Suchfeature der Systemsteuerung sucht nicht automatisch nach beiden Formularen. stellt die Formulare zur Verfügung, nach denen Benutzer wahrscheinlich suchen werden.
-   **Verwenden Sie einfache Gegenwärtigkeitsverben.** Wenn Sie connect als Suchbegriff registrieren, sucht das Suchfeature nicht automatisch nach Verbindungen, Verbindungen und Verbunden.
-   **Machen Sie sich keine Gedanken über den Fall.** Bei der Suchfunktion wird die Kleinschreibung nicht beachtet.

### <a name="standard-users-and-protected-administrators"></a>Standardbenutzer und geschützte Administratoren

**Viele Einstellungen erfordern Administratorrechte, um sich zu ändern.** Wenn ein Prozess Administratorrechte erfordert, Windows Vista und höher [Standardbenutzer](glossary.md) und [geschützte](glossary.md) Administratoren ihre Berechtigungen explizit erhöhen. Dadurch wird verhindert, dass schädlicher Code mit Administratorrechten ausgeführt wird.

Weitere Informationen und Beispiele finden Sie unter [Benutzerkontensteuerung.](winenv-uac.md)

### <a name="schemes-and-themes"></a>Schemas und Designs

Ein Schema ist eine benannte Sammlung visueller Einstellungen. Ein Design ist eine benannte Sammlung von Einstellungen im gesamten System. Beispiele für Schemas und Designs sind Display, Mouse, Telefon und Modem, Energieoptionen sowie Sound- und Audiooptionen.

-   **Benutzern das Erstellen von Schemas erlauben, wenn:**

    -   **Benutzer werden wahrscheinlich die Einstellungen ändern.**
    -   **Benutzer ändern die Einstellungen höchstwahrscheinlich als Sammlung.**

    Schemas sind nützlich, wenn sich Benutzer in einer anderen Umgebung befinden, z. B. an einem anderen physischen Standort (Land/Region, Zeitzone). verwendung ihres Computers in einer anderen Situation (auf Akkus, angedockt/angedockt); oder verwenden sie ihren Computer für eine andere Funktion (Präsentationen, Videowiedergabe).

-   **Geben Sie mindestens ein Standardschema an.** Das Standardschema sollte gut benannt sein und in den meisten Fällen für die meisten Benutzer gelten. Benutzer sollten kein eigenes Schema erstellen müssen.
-   **Stellen Sie eine Vorschau** oder einen anderen Mechanismus zur Verfügung, damit Benutzer die Einstellungen innerhalb des Schemas sehen können.

    ![Screenshot des Dialogfelds "Personalisierung" ](images/winenv-ctrl-panels-image13.png)

    In diesem Beispiel zeigt das Element Personalisierungssteuerung eine Vorschau der Desktop- und Darstellungseinstellungen an.

-   **Geben Sie die Befehle Speichern unter und Löschen an.** Ein Umbenennungsbefehl ist nicht erforderlich, benutzer können Schemas umbenennen, indem sie unter dem gewünschten Namen speichern und das ursprüngliche Schema löschen.
-   Wenn die Einstellungen nicht ohne Schema angewendet werden können, dürfen Benutzer nicht alle **Schemas löschen.** Benutzer sollten kein eigenes Schema erstellen müssen.
-   Wenn die Schemas nicht vollständig unabhängig sind (z. B. sind Energieschemas vom aktuellen Laptopmodus abhängig), stellen Sie sicher, dass es eine einfache Möglichkeit gibt, Einstellungen zu ändern, die für alle **Schemas gelten.** Stellen Sie beispielsweise bei Energieschemas sicher, dass Benutzer festlegen können, was geschieht, wenn die Deckel eines portablen Computers an einem einzigen Ort geschlossen werden.

### <a name="miscellaneous"></a>verschiedene gefährliche Stoffe

-   **Verwenden Systemsteuerung Erweiterungen für Features, die vorhandene Funktionen ersetzen Windows erweitern.** Die folgenden Systemsteuerungselemente sind erweiterbar: Bluetooth Devices, Display, Internet, Keyboard, Mouse, Network, Power, System, Wireless (Wireless).

### <a name="default-values"></a>Standardwerte

-   **Die Einstellungen in einem Systemsteuerungselement müssen den aktuellen Zustand des Features widerspiegeln.** Andernfalls wäre dies irreführend und kann zu unerwünschten Ergebnissen führen. Wenn die Einstellungen beispielsweise die Empfehlungen, aber nicht den aktuellen Status widerspiegeln, können Benutzer auf Abbrechen klicken, anstatt Änderungen vorzunehmen, da sie denken, dass keine Änderungen erforderlich sind.
-   **Wählen Sie den sichersten (um Datenverlust oder Systemzugriff zu verhindern) und den sichersten Anfangszustand aus.** Angenommen, die meisten Benutzer ändern die Einstellungen nicht.
-   **Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie den Anfangszustand aus, der wahrscheinlich oder praktisch ist.**

## <a name="text"></a>Text

### <a name="item-names"></a>Elementnamen

-   **Wählen Sie einen beschreibenden Namen aus, der eindeutig kommuniziert und unterscheidet, was das Systemsteuerungselement tut.** Die meisten Namen beschreiben Windows konfigurierten Features oder Objekte und werden in der klassischen Ansicht der Startseite der Systemsteuerung angezeigt.
-   **Schließen Sie die Wörter "Einstellungen", "Optionen", "Eigenschaften" oder "Konfiguration" nicht in den Namen ein.** Dies ist impliziert, und das Deaktivieren erleichtert benutzern das Scannen.

    **Falsch:**

    Barrierefreiheitsoptionen

    Modem Einstellungen

    Energieoptionen

    Regions- und Sprachoptionen

    **Richtig:**

    Zugriff

    Modem

    Power

    Regionale Formate und Sprachen

    In den richtigen Beispielen werden unnötige Wörter entfernt.

-   **Wenn das Systemsteuerungselement verwandte Features konfiguriert, listen Sie nur die Features auf, die zum Identifizieren des Elements erforderlich sind, und listen Sie zuerst die Features auf, die am wahrscheinlichsten erkannt oder verwendet werden.**

    **Falsch:**

    Ordneroptionen

    Telefon und Modemoptionen

    **Richtig:**

    Dateien und Ordner

    Modem

    In den richtigen Beispielen werden die Features des primären Systemsteuerungselements hervorgehoben.

-   Verwenden Sie [die Groß-/Groß-/Groß-/Formatvorlage](glossary.md).

### <a name="page-titles"></a>Seitentitel

**Hinweis:** Wie bei allen Explorer-Fenstern werden titel der Systemsteuerungsseite auf der Adressleiste [angezeigt,](glossary.md)jedoch nicht in der Titelleiste.

-   **Verwenden Sie für Hubseiten den Elementnamen der Systemsteuerung.**
-   **Verwenden Sie für Spoke-Seiten eine präzise Zusammenfassung des Zwecks der Seite.** Verwenden Sie die Hauptanweisung der Seite, wenn sie präzise ist. verwenden Sie andernfalls eine präzise Neuformtierung der Main-Anweisung.

    ![Screenshot des Dialogfelds "Energieoptionen" ](images/winenv-ctrl-panels-image6.png)

    In diesem Beispiel wird Energieoptionen für den Seitentitel anstelle der main-Anweisung verwendet.

-   Verwenden Sie die Groß-/Großschreibung im Titelstil.

### <a name="task-link-text"></a>Text des Aufgabenlinks

Die folgenden Richtlinien gelten für Links zu Aufgabenseiten, z. B. Aufgabenlinks für Kategorieseiten und Links zu "Siehe auch".

-   **Wählen Sie präzise Aufgabennamen aus, die die Aufgabe eindeutig kommunizieren und unterscheiden.** Benutzer sollten nicht herausfinden müssen, was die Aufgabe wirklich bedeutet oder wie sie sich von anderen Aufgaben unterscheidet.

    **Falsch:**

    Anpassen der Anzeigeeinstellungen

    **Richtig:**

    Bildschirmauflösung

    Im richtigen Beispiel vermittelt die Formulierung mehr Genauigkeit.

-   **Behalten Sie eine ähnliche Sprache zwischen Aufgabenlinks und den Seiten bei, auf die sie verweisen.** Benutzer sollten sich nicht von der Seite, die durch einen Link angezeigt wird, nicht überrumpeln lassen.
-   **Entwerfen Sie für Aufgabenseiten die Hauptanweisung, Commitschaltflächen und Aufgabenlinks als verwandten Textsatz.**
    

    | Beispiel                             |    Anweisung                                                   |
    |------------------------------|-------------------------------------------------------|
    | Aufgabenlink:<br/>        | Herstellen der Verbindung mit einem WLAN<br/>              |
    | Hauptanweisung:<br/> | Auswählen eines Netzwerks, mit dem eine Verbindung hergestellt werden soll<br/>             |
    | Schaltfläche "Commit":<br/>    | Verbinden<br/>                                    |
    | Aufgabenlink:<br/>        | Einrichten der Jugendschutzmechanismen<br/>                   |
    | Hauptanweisung:<br/> | Auswählen eines Benutzers und Einrichten der Jugendschutzmechanismen<br/> |
    | Schaltfläche "Commit":<br/>    | Anwenden der Jugendschutz<br/>                     |
    | Aufgabenlink:<br/>        | Lösen von Synchronisierungskonflikten<br/>                |
    | Hauptanweisung:<br/> | Wie möchten Sie diesen Konflikt lösen?<br/>  |
    | Schaltfläche "Commit":<br/>    | Beheben<br/>                                    |

    

     

    Diese Beispiele zeigen die Beziehung zwischen dem Tasklinktext, der Hauptanweisung und dem Text der Commitschaltfläche.

-   Während Aufgaben häufig mit Verben beginnen, **sollten Sie das Verb auf Kategorieseiten weglassen, wenn es sich um ein generisches, konfigurationsbezogenes Verb handelt, das die Kommunikation der Aufgabe nicht unterstützt.**

    **Spezifische, hilfreiche Verben:**

    Add

    Azure Functions

    Verbinden

    Kopieren

    Erstellen

    Löschen

    Trennen

    Installieren

    Entfernen

    Einrichten

    Starten

    Beenden

    Problembehandlung

    **Generische, nicht hilfreiche Verben:**

    Anpassen

    Change

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

-   **Wenn der Task mehrere verwandte Features konfiguriert, listen Sie nur die Features auf, die für den Satz repräsentativ sind.** Lassen Sie Details aus, die leicht abgeleitet werden können.

    **Falsch:**

    Lautstärke des Lautsprechers, Stummschalten, Lautstärkesymbol

    Lautsprecher, Mikrofone, PARTS und Soundschemas

    **Richtig:**

    Lautstärke des Lautsprechers

    Lautsprecher und Mikrofone

    In den richtigen Beispielen werden nur die repräsentativen Features im Aufgabenlink angegeben.

-   **Sie sollten Aufgaben nur in Bezug auf die Technologie formulieren, wenn dies auch für Zielbenutzer derFall ist.**

    **Falsch:**

    Connectoids

    Pixeltiefe

    dpi

    **Richtig:**

    Drucker

    Scanner

    Maus

    Die richtigen Beispiele sind technologiebasierte Begriffe, die zielorientierte Benutzer wahrscheinlich verwenden, während dies nicht der Richtige ist.

-   Verwenden Sie Plural nomen nur, wenn das System mehr als eins unterstützen kann.
-   Verwenden Sie [die Groß-/Großschreibung im Satzformat.](glossary.md)
-   Verwenden Sie keine Interpunktion am Ende.

### <a name="main-instructions"></a>Hauptanweisungen

-   **Verwenden Sie für die Hubseite die Hauptanweisung, um das Ziel des Benutzers mit dem Systemsteuerungselement zu erläutern.** Die Hauptanweisung sollte Benutzern helfen, zu bestimmen, ob sie das richtige Systemsteuerungselement ausgewählt haben. Beachten Sie, dass Benutzer möglicherweise ihr Systemsteuerungselement mit einem Fehler ausgewählt haben und tatsächlich nach Einstellungen suchen, die Teil eines anderen Systemsteuerungselements sind.

    **Beispiele:**

    Halten Sie Ihren Computer sicher und auf dem neuesten Stand.

    Optimieren Sie Ihren Computer, damit er leichter zu sehen, zu hören und zu steuern ist.

-   **Verwenden Sie für Spoke-Seiten die Hauptanweisung, um zu erläutern, was auf der Seite zu tun ist.** Die Anweisung sollte eine bestimmte Anweisung, imperative Richtung oder Frage sein. Gute Anweisungen kommunizieren das Ziel des Benutzers mit der Seite, anstatt sich ausschließlich auf die Mechanismen der Bearbeitung zu konzentrieren.

    **Falsch:**

    Auswählen einer Benachrichtigungsaufgabe

    **Richtig:**

    Angeben des Umgangs mit eingehenden Informationen

    Die richtige Version kommuniziert das von der Seite erreichten Ziel besser.

-   **Verwenden Sie nach Möglichkeit bestimmte Verben.** Bestimmte Verben sind für Benutzer aussagekräftiger als generische Verben.
-   Verwenden Sie [die Groß-/Großschreibung im Satzformat.](glossary.md)
-   **Schließen Sie keine abschließenden Zeiträume ein, wenn die Anweisung eine -Anweisung ist.** Wenn die Anweisung eine Frage ist, fügen Sie ein abschließendes Fragezeichen ein.

### <a name="supplemental-instructions"></a>Zusätzliche Anweisungen

-   **Verwenden Sie für die Hubseite die optionale zusätzliche Anweisung, um den Zweck des Systemsteuerungselements näher zu erläutern.**
-   **Verwenden Sie für Spoke-Seiten die optionale ergänzende Anweisung, um zusätzliche Informationen anzuzeigen, die hilfreich sind, um die Seite zu verstehen oder zu verwenden.** Sie können ausführlichere Informationen bereitstellen und Terminologie definieren.
-   Verwenden Sie vollständige Sätze und Großbuchstaben im [Satzstil.](glossary.md)

### <a name="page-text"></a>Seitentext

-   **Geben Sie die Hauptanweisung nicht im Inhaltsbereich an.**
-   **Verwenden Sie das Wort "page", um auf die Seite selbst zu verweisen.**
-   **Verwenden Sie die zweite Person (Sie, Ihre), um Benutzern mitzuteilen, was** im Hauptbereich für Anweisungen und Inhalte zu tun ist. Häufig wird die zweite Person impliziert.

    **Beispiel:**

    Wählen Sie die Bilder aus, die Sie drucken möchten.

-   **Verwenden Sie die erste Person (I, me, my), damit Benutzer dem Systemsteuerungselement mitteilen können, was** im Inhaltsbereich zu tun ist, der auf die Hauptanweisung reagiert.

    **Beispiel:**

    Drucken Sie die Fotos auf meiner Kamera.

### <a name="task-links"></a>Aufgabenlinks

-   **Wählen Sie präzisen Linktext aus, der klar kommuniziert und unterscheidet, was der Tasklink macht.** Sie sollte selbsterklärend sein und der Hauptanweisung entsprechen. Benutzer sollten nicht herausfinden müssen, was der Link wirklich bedeutet oder wie er sich von anderen Links unterscheidet.
-   **Tasklinks immer mit einem Verb starten.**
-   Verwenden Sie [die Groß-/Großschreibung im Satzformat.](glossary.md)
-   Verwenden Sie keine Interpunktion am Ende.
-   **Wenn der Aufgabenlink eine weitere Erläuterung erfordert, geben Sie die Erklärung in einem separaten Textsteuerelement** an, indem Sie vollständige Sätze und endende Interpunktion verwenden. Fügen Sie solche Erklärungen jedoch nur bei Bedarf hinzu, und fügen Sie nicht allen Aufgabenlinks Erklärungen hinzu, da eine andere Aufgabenverbindung benötigt wird.

Weitere Informationen und Beispiele finden Sie unter [Links](ctrl-command-links.md).

### <a name="commit-buttons"></a>Commitschaltflächen

-   **Verwenden Sie bestimmte Commitschaltflächenbezeichnungen, die eigenständig sinnvoll sind und mit der Hauptanweisung übereinstimmen.** Im Idealfall sollten Benutzer nichts anderes lesen müssen, um die Bezeichnung zu verstehen. Die Wahrscheinlichkeit, dass Benutzer Befehlsschaltflächenbezeichnungen lesen, ist weitaus wahrscheinlicher als statischer Text.
-   **Starten Sie immer Commit-Schaltflächenbezeichnungen mit einem Verb.**
-   **Verwenden Sie nicht Schließen, Fertig oder Fertig stellen.** Diese Schaltflächenbezeichnungen eignen sich besser für andere Fenstertypen.
-   Verwenden Sie [die Groß-/Großschreibung im Satzformat.](glossary.md)
-   Verwenden Sie keine Interpunktion am Ende.
-   Weisen Sie einen eindeutigen [Zugriffsschlüssel zu.](glossary.md)
    -   **Ausnahme:** Weisen Sie Den Schaltflächen "Abbrechen" keine Zugriffsschlüssel zu, da es sich bei ESC um den Zugriffsschlüssel handelt. Auf diese Weise können die anderen Zugriffsschlüssel einfacher zugewiesen werden.

## <a name="documentation"></a>Dokumentation

Wenn Sie auf die Startseite oder Kategorieseiten der Systemsteuerung verweisen:

-   Lesen Sie in der Benutzerdokumentation Systemsteuerung, indem Sie großgeschriebene Titel verwenden und einen vorangehenden eindeutigen Artikel auslassen.

    **Beispiel:**

    Öffnen Sie in Systemsteuerung **Security Center**.

-   In der Programmierung und anderen technischen Dokumentationen finden Sie auf der Startseite der Systemsteuerung und auf der Seite mit der Systemsteuerungskategorie weitere Informationen, ohne die Wörter groß zu machen. Ein vorheriger bestimmter Artikel ist optional.

Für Systemsteuerungselemente:

-   Wenn Sie auf ein einzelnes Systemsteuerungselement verweisen, verwenden Sie \[ "Systemsteuerungselementname \] in Systemsteuerung" oder im Allgemeinen "Systemsteuerung Element" in der Benutzerdokumentation. Verwenden Sie applet, program oder control panel nicht, um auf einzelne Systemsteuerungselemente zu verweisen.
-   Wenn Sie auf die Hubseite eines Systemsteuerungselements verweisen, verwenden Sie "Main \[ Control Panel Item Name \] Page".
-   Formatieren Sie den Systemsteuerungsnamen nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie den Namen nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

Beispiele:

-   Öffnen Sie in Systemsteuerung **Die Jugendschutzelemente.**
-   Kehren Sie zur Hauptseite **Der Jugendschutz** zurück.

