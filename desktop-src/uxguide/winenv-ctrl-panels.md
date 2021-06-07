---
title: Systemsteuerungen
description: Verwenden Sie Systemsteuerungselemente, um Benutzer beim Konfigurieren von Features auf Systemebene und beim Ausführen verwandter Aufgaben zu unterstützen. Programme mit einer Benutzeroberfläche sollten stattdessen direkt über ihre Benutzeroberfläche konfiguriert werden.
ms.assetid: 845325ef-9f1d-4aa7-a5b0-685fac74a9f8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 3b0e6fdf4e0c916f80ae3c1783e4e9e5fee920a8
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443311"
---
# <a name="control-panels"></a>Systemsteuerungen

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Verwenden Sie Systemsteuerungselemente, um Benutzer beim Konfigurieren von Features auf Systemebene und beim Ausführen verwandter Aufgaben zu unterstützen. Programme mit einer Benutzeroberfläche sollten stattdessen direkt über ihre Benutzeroberfläche konfiguriert werden.

Mit Systemsteuerung in Microsoft Windows können Benutzer Features auf Systemebene konfigurieren und verwandte Aufgaben ausführen. Beispiele für die Featurekonfiguration auf Systemebene sind Hardware- und Softwareeinrichtung und -konfiguration, Sicherheit, Systemwartung und Benutzerkontoverwaltung.

Der Begriff Systemsteuerung bezieht sich auf das gesamte Windows Systemsteuerung-Feature. Einzelne Systemsteuerungen werden als Systemsteuerungselemente bezeichnet. Ein Systemsteuerungselement gilt als element der obersten Ebene, wenn es direkt über die Startseite der Systemsteuerung oder eine Kategorieseite zugänglich ist.

![Screenshot der Sprachkategorie der Systemsteuerung ](images/winenv-ctrl-panels-image1.png)

Ein typisches Systemsteuerungselement.

Die Startseite der Systemsteuerung ist der Haupteinstiegspunkt für alle Systemsteuerungselemente. Es listet die Elemente nach ihrer Kategorie sowie die gängigsten Aufgaben auf. Sie wird angezeigt, wenn Benutzer im Systemsteuerung auf Startmenü.

Auf einer Kategorieseite der Systemsteuerung werden die Elemente innerhalb einer einzelnen Kategorie zusammen mit den gängigsten Aufgaben aufgeführt. Sie wird angezeigt, wenn Benutzer auf der Startseite auf einen Kategorienamen klicken.

Systemsteuerungselemente werden mithilfe von [Aufgabenflüssen oder](glossary.md) Eigenschaftenblättern implementiert. Für Windows Vista und höher sind Taskabläufe die bevorzugte Benutzeroberfläche ( User Interface, UI).

**Entwickler:** Informationen zum Erstellen von Systemsteuerungselementen finden Sie unter [Systemsteuerung Elemente](/previous-versions//bb776838(v=vs.85)).

**Hinweis:** Richtlinien im Zusammenhang [mit Eigenschaftenblättern](win-property-win.md) werden in einem separaten Artikel vorgestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Dient der Zweck zum Konfigurieren von Features auf Systemebene?** Falls nicht, verwenden Sie einen anderen Integrationspunkt. Konfigurieren Sie Ihre Anwendungsfeatures direkt über die Benutzeroberfläche mithilfe von Optionsdialogfeldern, anstatt Systemsteuerung. Verwenden Sie für Hilfsprogramme, die nicht für Setup-, Konfigurations- oder verwandte Aufgaben (z. B. Problembehandlung) verwendet werden, Startmenü als Integrationspunkt.
-   **Verfügt das Feature auf Systemebene über eine eigene Benutzeroberfläche?** Wenn ja, sollten Benutzer auf dieser Benutzeroberfläche Änderungen vornehmen. Beispielsweise sollte ein Hilfsprogramm für die Systemsicherung über die Programmoptionen konfiguriert werden, nicht über Systemsteuerung.
-   **Müssen Benutzer die Konfiguration häufig ändern?** Wenn dies der Meinung ist (z. B. mehrmals pro Woche), sollten Sie alternative Lösungen in Betracht ziehen, z. B. zusätzlich zur Systemsteuerung. Beispielsweise kann die Windows-Master-Volumeeinstellung direkt über das Symbol im Benachrichtigungsbereich konfiguriert werden. Einige Einstellungen können automatisch konfiguriert werden. In Windows-Explorer beispielweise ermöglicht die Registerkarte Kompatibilität für Anwendungseigenschaften die Ausführung einer Anwendung im 256-Farbmodus, anstatt dass Benutzer den Videomodus manuell ändern müssen.
-   **Sind die Zielbenutzer IT-Experten?** Verwenden Sie in diesem Microsoft Management Console stattdessen ein MMC-Snap-In [(](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) Microsoft Management Console), das speziell für Systemverwaltungsaufgaben entwickelt wurde. In einigen Fällen ist die beste Lösung sowohl ein Systemsteuerungselement für allgemeine Benutzer als auch ein MMC-Snap-In für IT-Experten.

    ![Screenshot des Fensters "Computerverwaltung" ](images/winenv-ctrl-panels-image2.png)

    In diesem Beispiel stellt das MMC-Snap-In Lokale Benutzer und Gruppen eine Benutzerverwaltung für IT-Experten zur Verfügung. Andere Benutzer verwenden das Element Benutzerkonten wahrscheinlicher in Systemsteuerung.

-   **Ist das Feature ein OEM-Feature, das nur während der anfänglichen Systemkonfiguration verwendet wird?** Wenn ja, verwenden Sie die Windows-Begrüßungscenter als Integrationspunkt.

Systemsteuerungselemente sind erforderlich, da viele Features auf Systemebene keinen offensichtlicheren oder direkteren Integrationspunkt haben. Allerdings Systemsteuerung nicht als "one place" für alle Konfigurationseinstellungen angezeigt werden. **Programme mit einer Benutzeroberfläche sollten direkt über ihre Benutzeroberfläche konfiguriert werden, anstatt Systemsteuerungselemente zu verwenden.**

**Falsch:**

![Screenshot des Internetoptionenelements der Systemsteuerung ](images/winenv-ctrl-panels-image3.png)

In diesem Beispiel sollte Windows Internet Explorer nicht in Systemsteuerung dargestellt werden, da eine eigene Benutzeroberfläche ein besserer Integrationspunkt ist.

### <a name="create-a-new-control-panel-item-or-extend-an-existing-one"></a>Erstellen Sie ein neues Systemsteuerungselement, oder erweitern Sie ein vorhandenes?

Orientieren Sie sich an folgenden Fragen:

-   **Kann die Funktionalität als Aufgaben ausgedrückt werden, die in ein vorhandenes, erweiterbares Systemsteuerungselement integriert werden können?** Die folgenden Systemsteuerungselemente sind erweiterbar: Bluetooth-Geräte, Anzeige, Internet, Tastatur, Maus, Netzwerk, Stromversorgung, System, Drahtlos (Darstellung).
-   **Ersetzen die Eigenschaften und Aufgaben die Features des vorhandenen erweiterbaren Systemsteuerungselements?** Wenn ja, sollten Sie das vorhandene Systemsteuerungselement erweitern, da dies zu einer einfacheren Benutzererfahrung führt. Falls nicht, erstellen Sie ein neues Systemsteuerungselement.

## <a name="design-concepts"></a>Entwurfskonzepte

**Das Systemsteuerung basiert auf einer realenMetapher.** Eine echte Systemsteuerung ist eine Sammlung von Steuerelementen (Regler, Schalter, Messgeräte und Anzeigen), die zum Überwachen und Steuern eines Geräts verwendet werden. Benutzer solcher Kontrollpanels benötigen häufig Schulungen, um ihre Verwendung zu verstehen.

Im Gegensatz zu ihren realen Entsprechungen sind **Windows-Systemsteuerungsentwürfe für Erstbenutzer optimiert.** Benutzer führen die meisten Systemsteuerungsaufgaben nicht sehr häufig aus, daher merken sie sich in der Regel nicht, wie sie dies tun, und müssen sie effektiv jedes Mal neu verleern.

So entwerfen Sie ein systemsteuerungselement, das nützlich und einfach zu verwenden ist:

-   Stellen Sie sicher, dass die Eigenschaften erforderlich sind.
-   Präsentieren Sie Eigenschaften in Bezug auf Benutzerziele anstelle von Technologie.
-   Präsentieren Sie Eigenschaften auf der rechten Ebene.
-   Entwurfsseiten für bestimmte Aufgaben.
-   Entwurfsseiten für Standardbenutzer und geschützte Administratoren.

Bestimmen Sie beim Entwerfen und Auswerten von Elementen, die in Systemsteuerung enthalten sein müssen, die allgemeinen Aufgaben, die Benutzer ausführen, und stellen Sie sicher, dass es einen eindeutigen Pfad zum Ausführen dieser Aufgaben gibt. Benutzer führen in der Regel die folgenden Arten von Aufgaben mit Systemsteuerungselementen aus:

-   Anfängliche Konfiguration
-   Selten vorgenommene Änderungen (für die meisten Einstellungen)
-   Häufige Änderungen (für einige wichtige Einstellungen)
-   Roll back settings to a initial or previous state (Zurücksetzen der Einstellungen auf einen ursprünglichen oder vorherigen Zustand)
-   Problembehandlung

**Wenn Sie nur eine Sache tun...**

Entwerfen Sie Systemsteuerungsseiten für bestimmte Aufgaben, und stellen Sie sie in Bezug auf Benutzerziele statt in Technologie vor.

## <a name="usage-patterns"></a>Verwendungsmuster

Für Systemsteuerungselemente können Sie einen Taskfluss oder ein Eigenschaftenblatt verwenden. Dies sind die Verwendungsmuster:

### <a name="task-flow-patterns"></a>Aufgabenflussmuster

Aufgabenflusselemente verwenden eine Hubseite, um die optionen auf hoher Ebene anzuzeigen, und Spokeseiten, um die eigentliche Konfiguration auszuführen.

**Hubseiten**

-   Aufgabenbasierte Hubseiten. Diese Hubseiten stellen die am häufigsten verwendeten Aufgaben vor. Sie werden am besten für einige häufig verwendete oder wichtige Aufgaben verwendet, bei denen Benutzer mehr Anleitungen und Erläuterungen benötigen. Hubseiten verfügen nicht über Commitschaltflächen. Hybride aufgabenbasierte Hubseiten verfügen auch über einige Eigenschaften oder Befehle direkt darauf. Hybrid Hub-Seiten werden dringend empfohlen, wenn Benutzer höchstwahrscheinlich Systemsteuerung verwenden, um auf diese Eigenschaften und Befehle zu zugreifen.
-   Objektbasierte Hubseiten. Diese Hubseiten stellen die verfügbaren Objekte mithilfe eines Listenansicht-Steuerelements dar. Sie werden am besten verwendet, wenn es mehrere Objekte geben könnte. Hubseiten verfügen nicht über Commitschaltflächen.

**Spoke-Seiten**

-   Aufgabenseiten. Diese Spoke-Seiten stellen eine Aufgabe oder einen Schritt in einer Aufgabe mit einer bestimmten aufgabenbasierten Hauptanweisung vor. Sie werden am besten für Aufgaben verwendet, die von zusätzlichen Anleitungen und Erläuterungen profitieren.
-   Formularseiten. Diese Spoke-Seiten stellen eine Auflistung verwandter Eigenschaften und Aufgaben dar, die auf einer allgemeinen Hauptanweisung basieren. Sie eignen sich am besten für Features mit vielen Eigenschaften und profitieren von einer direkten, einseitigen Darstellung, z. B. erweiterten Eigenschaften.

### <a name="property-sheet-patterns"></a>Eigenschaftenblattmuster

-   Eigenschaftenblätter werden am besten in Legacyelementen mit vielen Einstellungen für fortgeschrittene Benutzer verwendet. Neue Elemente können den gleichen Effekt mit einem Aufgabenfluss mithilfe des Formularseitenmusters erzielen.

## <a name="guidelines"></a>Richtlinien

### <a name="property-sheet-control-panel-items"></a>Elemente der Eigenschaftenblatt-Systemsteuerung

-   **Verwenden Sie keine Eigenschaftenblätter für neue Systemsteuerungselemente.** Verwenden Sie stattdessen Aufgabenflows, um eine nahtlose Benutzeroberfläche zu erstellen und die Kategorisierungs- und Suchfunktionen der Startseite der Systemsteuerung vollständig zu nutzen.

### <a name="task-flow-control-panel-items"></a>Elemente der Aufgabenflusssteuerung

**Allgemein**

-   **Lassen Sie die wichtigsten Inhalte und Steuerelemente sichtbar, ohne scrollen zu müssen.** Benutzer scrollen nicht, um Seiteninhalte anzuzeigen, es sei denn, sie haben einen Grund dafür. Sie können Commitschaltflächen immer sichtbar machen, indem Sie sie in einem [Befehlsbereich](glossary.md) statt im Inhaltsbereich platzieren. Zerlegen Sie Seiten nicht, nur um Scrollen zu vermeiden.
    -   **Sie können lange Seiten vertikal scrollen,** solange die wichtigsten Steuerelemente ohne Bildlauf sichtbar sind.
    -   **Verwenden Sie kein horizontales Scrollen.** Gestalten Sie stattdessen den Seiteninhalt neu, und verwenden Sie vertikales Scrollen. Seiten können nur dann über horizontale Scrollleisten verfügen, wenn sie sehr schmal sind.
-   **So navigieren Sie zwischen Seiten:**
    -   Verwenden Sie [Aufgabenlinks,](glossary.md) um eine Aufgabe zu starten.
    -   Verwenden Sie Aufgabenlinks oder die Schaltfläche Weiter, um in einer Aufgabe mit mehreren Schritten zur nächsten Seite zu navigieren.
    -   Verwenden Sie Commitschaltflächen, um eine Aufgabe abzuschließen.
    -   Verwenden Sie die Schaltfläche "Zurück" in der Menüleiste, um zu zuvor angezeigten Seiten zurückzukehren. Fügen Sie keine Schaltfläche "Zurück" zum Befehlsbereich hinzu.
    -   Verwenden Sie die Adressleiste, um direkt zur Startseite der Systemsteuerung zurückzukehren.
    -   Verwenden Sie links im Aufgabenbereich anzeigen, um zu Seiten in anderen Systemsteuerungselementen zu navigieren. Andernfalls sollte die Navigation innerhalb eines einzelnen Systemsteuerungselements bleiben.
-   **Legen Sie nur die Startseite der Systemsteuerung in die Adressleiste ein.** Wenn Sie auf diesen Link klicken, wird die Startseite der Systemsteuerung wieder angezeigt, und alle laufenden Arbeiten werden ohne [Bestätigung](https://msdn.microsoft.com/library/windows/desktop/aa511273.aspx)von verwerfen.
-   **Legen Sie keine Befehlsschaltfläche Schließen auf den Systemsteuerungsseiten ab.** Benutzer können ein Systemsteuerungsfenster mithilfe der Schaltfläche Schließen auf der Titelleiste schließen.

**Aufgabenlinks und Schaltflächen**

-   **Wenn eine Seite über einen kleinen Satz fester Optionen verfügt, verwenden Sie Aufgabenlinks anstelle einer Kombination aus Optionsfeldern und der Schaltfläche Weiter.** Dadurch können Benutzer eine Antwort mit einem einzigen Klick auswählen.
-   Sie können Aufgabenlinks und Schaltflächen an den folgenden Stellen anordnen (in der Reihenfolge der Auffindbarkeit):
    -   Der [Befehlsbereich](glossary.md) (nur für Befehlsschaltflächen auf Spoke-Seiten).
    -   Der [Inhaltsbereich](glossary.md):
        -   Befehlsschaltflächen
        -   Aufgabenlinks
        -   Weitere Links
    -   Links im [Aufgabenbereich](glossary.md) (nur Hubseiten).
-   **Legen Sie die Position von Aufgabenlinks und Schaltflächen auf Wichtigkeit und Notwendigkeit der Auffindbarkeit fest.**
    -   **Legen Sie nur Commitschaltflächen im Befehlsbereich ab.**
    -   **Legen Sie wichtige Aufgaben im Inhaltsbereich ab.** Befehlsschaltflächen zeichnen in der Regel die größte Aufmerksamkeit aus. Reservieren Sie sie daher für Befehle, die Benutzern angezeigt werden müssen. Aufgabenlinks zeichnen auch die Aufmerksamkeit auf, jedoch weniger als Befehlsschaltflächen.
    -   **Reservieren Sie den Aufgabenbereich und einfache Links für sekundäre (weniger wichtige) Aufgaben.** Der Aufgabenbereich ist der am wenigsten erkennbare Bereich einer Aufgabenseite, und einfache Links sind nicht so sichtbar wie Befehlsschaltflächen und Aufgabenlinks.
-   Für Aufgabenlinks, die im Inhaltsbereich angezeigt werden:
    -   **Wenn mehr als sieben Links vorhanden sind, gruppieren Sie die Links in Kategorien.** Geben Sie Überschriften für jede der Gruppen an.
    -   **Stellen Sie für weniger als sieben Links die Links in einer einzelnen Gruppe ohne Überschrift dar.**
-   **Stellen Sie Aufgabenlinks und Schaltflächen in einer logischen Reihenfolge dar.** Aufgabenverknüpfungen vertikal auflisten, Befehlsschaltflächen horizontal.
-   **Unterteilen Sie die Befehle innerhalb** von Kategorien in verwandte Gruppen. Stellen Sie die Aufgabengruppen vor, indem Sie die am häufigsten verwendeten zuerst platzieren und innerhalb jeder Gruppe zuerst die am häufigsten verwendeten Aufgaben platzieren. **Die resultierende Reihenfolge sollte ungefähr der Wahrscheinlichkeit der Verwendung entsprechen, aber auch einen logischen Ablauf aufweisen.**
    -   **Ausnahme:** Aufgabenlinks, die dazu führen, dass alles erledigt wird, sollten zuerst platziert werden.
-   **Wenn viele Aufgabenlinks vorhanden sind, stellen Sie die wichtigsten Aufgaben** mit einem 24 x 24-Pixel-Symbol und zwei Textzeilen in den Vordergrund. Verwenden Sie für weniger wichtige Aufgaben ein 16 x 16 Pixel großes Symbol oder kein Symbol und eine einzelne Zeile mit Linktext.

    ![Screenshot von Elementen mit großen und kleinen Symbolen ](images/winenv-ctrl-panels-image4.png)

    In diesem Beispiel erhalten wichtige Befehle eine wichtigere Darstellung.

-   **Eine klare physische Trennung zwischen häufig verwendeten befehlen und destruktiven Befehlen.** Andernfalls können Benutzer versehentlich auf destruktive Befehle klicken. Möglicherweise müssen Sie Ihre Befehle etwas neu anordnen, um destruktive Befehle zusammenzustellen.
-   **Stellen Sie den Mechanismus bereit, um Befehle direkt auf der Seite rückgängig zu machen.** Benutzer sollten nicht an einer anderen Stelle navigieren müssen, um einen Fehler rückgängig zu machen.
-   **Verwenden Sie für Aufgabenlinks entweder alle Standardsymbole für Aufgabenverknüpfung oder alle benutzerdefinierten Symbole.** Mischen Sie sie nicht. Verwenden Sie benutzerdefinierte Symbole nur, wenn:
    -   Sie helfen Benutzern, die Aufgaben zu verstehen.
    -   Sie entsprechen den Symbolstandards von [Symbolen](vis-icons.md).
    -   Sie haben eine unaufdringliche Darstellung.

**Dialogfelder**

Wenn Sie Taskflows verwenden, möchten Sie in der Regel, dass ein Task innerhalb eines einzelnen Fensters von Seite zu Seite verläuft. Die folgenden Umstände sind jedoch Ausnahmen. Verwenden Sie Dialogfelder unter den folgenden Umständen:

-   So fordern Sie Benutzer zur Eingabe eines Administratorbenutzernamens und -kennworts auf. Verwenden Sie zu diesem Zweck immer das Dialogfeld Anmeldeinformations-Manager. (Sollte [modal](glossary.md)sein.)
-   So bestätigen Sie einen in-place-Befehl mithilfe eines Aufgabendialogfelds oder Meldungsfelds. (Sollte modal sein.)
-   So erhalten Sie Eingaben für die Befehle "In-Place", z. B. für "Neu", "Hinzufügen", "Speichern unter", "Umbenennen" und "Drucken".

    ![Screenshot des Dialogfelds "Netzwerkspeicherorte löschen" ](images/winenv-ctrl-panels-image5.png)

    In diesem Beispiel wird der Befehl Löschen nicht in einer separaten Seite, sondern in einem Dialogfeld ausgeführt.

-   So führen Sie sekundäre, eigenständige Aufgaben aus. Mithilfe eines [moduslosen](glossary.md)sekundären Fensters können solche Aufgaben unabhängig und außerhalb des Haupttaskflows ausgeführt werden.

### <a name="hub-pages"></a>Hubseiten

**Allgemein**

-   Verwenden Sie aufgabenbasierte Hubseiten in folgenden Anwendungsfällen:
    -   **Es gibt eine kleine Anzahl häufig verwendeter oder wichtiger Aufgaben.**
    -   **Die Konfiguration umfasst ein oder zwei Objekte** (Beispiele: Monitore, Tastatur, Maus, Gamecontroller).
    -   **Die Konfiguration gilt systemweit** (Beispiele: Datum und Uhrzeit, Sicherheit, Energieoptionen).
-   Verwenden Sie objektbasierte Hubseiten in folgenden Anwendungsfällen:
    -   **Die Konfiguration kann mehrere Objekte umfassen** (z. B. Benutzerkonten, Netzwerkverbindungen, Drucker).
    -   **Die Konfiguration gilt nur für das ausgewählte Objekt.**
-   **Verwenden Sie keine Hubseite, wenn das Systemsteuerungselement über eine einzelne Seite** verfügt, die alle beteiligten Aufgaben und Eigenschaften enthält.

**Objektlisten**

-   **Listen Sie Elemente in einer logischen Reihenfolge auf.** Sortieren Sie benannte Objekte in alphabetischer Reihenfolge, Zahlen in numerischer Reihenfolge und Datumsangaben in chronologischer Reihenfolge.
-   Stellen Sie für objektbasierte Hubs Objektansichtsbefehle im Aufgabenbereich zur Verfügung, wenn die Möglichkeit zum Ändern der Ansicht **für die Aufgaben wichtig ist.** Die Möglichkeit zum Ändern von Ansichten ist wichtig, wenn viele Objekte enthalten sind und die Standardpräsentation nicht für alle Szenarien gut funktioniert. Benutzer können die Listenansicht auch dann ändern, wenn es keine expliziten Befehle über das Kontextmenü der Listenansicht gibt, dies ist jedoch weniger aufstellbar.

Weitere Richtlinien zum Präsentieren von Objektlisten finden Sie unter [Listenansichten](ctrl-list-views.md).

**Interaktion**

-   **Legen Sie keine Commitschaltflächen auf Hubseiten ab.** Hubseiten sind grundsätzlich Startpunkte. Benutzer "commiten" niemals Hubseiten, für die sie nie fertig sind. Und Commitschaltflächen auf Hubseiten machen alle aufgaben, die von einem Hub initiiert werden, verwirrend (Benutzer fragen sich, ob diese Aufgaben übertragen werden müssen).
    -   **Ausnahme:** Wenn für das Ändern einer Einstellung [eine Erhöhung erforderlich](glossary.md)ist, geben Sie eine Schaltfläche Anwenden mit einem Security [Shield-Symbol an.](winenv-uac.md) Deaktivieren Sie die Commitschaltfläche, nachdem Die Änderungen angewendet wurden.
-   **Erwägen Sie, die nützlichsten Eigenschaften direkt auf Hubseiten zu verwenden.** Solche Hybrid Hub-Seiten werden dringend empfohlen, wenn Benutzer höchstwahrscheinlich Systemsteuerung für den Zugriff auf diese Eigenschaften verwenden.

    ![Screenshot der Hubseite "Energieoptionen" ](images/winenv-ctrl-panels-image6.png)

    In diesem Beispiel verfügt Energieoptionen Systemsteuerungselement direkt auf der Hubseite über die nützlichsten Einstellungen.

-   **Verwenden Sie ein Direkt-Commit-Modell für alle Einstellungen auf Hybrid Hub-Seiten, damit Änderungen sofort vorgenommen werden.** Auch hier commiten Benutzer nie eine Hubseite. Wenn eine Einstellung eine Commitschaltfläche erfordert, legen Sie sie nicht auf einer Hubseite ab.
-   **Erwägen Sie, einfache Befehle mit nur einem Schritt direkt auf Hubseiten zu verwenden, anstatt Navigationslinks zu verwenden.**
-   **Bestätigen Sie befehle, deren Auswirkungen nicht einfach rückgängig gemacht werden können.** Verwenden Sie [ein Aufgabendialogfeld](win-dialog-box.md) oder [ein Meldungsfeld.](glossary.md)

    ![Screenshot des Dialogfelds "Löschen bestätigen" ](images/winenv-ctrl-panels-image7.png)

    In diesem Beispiel wird der Befehl Löschen mit einem Dialogfeld bestätigt.

-   **Identifizieren Sie für aufgabenbasierte Hubseiten jede Aufgabe mit einem Aufgabenlink und einem Symbol.** Sie können auch eine optionale Beschreibung für jeden Link bereitstellen. Versuchen Sie jedoch, die Aufgabenlinks selbsterklärend zu machen und optionale Beschreibungen nur für Links zur Verfügung zu stellen, die sie wirklich benötigen.

    ![Screenshot der Seite des Computerleistungshubs ](images/winenv-ctrl-panels-image8.png)

    In diesem Beispiel verfügt jede Aufgabe über einen Aufgabenlink und ein Symbol.

-   **Bei objektbasierten Hubseiten werden objekte durch Einfaches Klicken ausgewählt, und durch Doppelklicken wird ein Objekt ausgewählt, und es wird zu seiner Standardseite navigiert.** Die Standardseite ist in der Regel eine Eigenschaftenseite oder eine aufgabenbasierte Hubseite.
-   **Eine objektbasierte Hubseite kann zu einem aufgabenbasierten Hub für die ausgewählten Objekte navigieren.** Solche sekundären Hubs sollten jedoch vermieden werden, da sie ein Systemsteuerungselement zu indirekt anfühlen.

**Aufgabenbereiche**

Verwenden Sie Aufgabenbereiche, um Links zu Befehlen, Ansichten und zugehörigen Systemsteuerungselementen anzuzeigen.

-   Für Aufgabenbereiche in aufgabenbasierten Hubs müssen Links in der folgenden Reihenfolge angezeigt werden:
    -   **Sekundäre Befehle**. Primäre Aufgaben nur im Inhaltsbereich präsentieren. Verwenden Sie den Aufgabenbereich für sekundäre, optionale Aufgaben. Stellen Sie sich eine primäre Aufgabe vor, wenn Benutzer sie in wichtigen Szenarien entdecken müssen. sekundär, wenn es für Benutzer akzeptabel ist, es nicht zu entdecken.
    -   **Siehe auch**. Die optionalen Links, die zu verwandten Systemsteuerungselementen navigieren.
-   Für Aufgabenbereiche in objektbasierten Hubs müssen Links in der folgenden Reihenfolge angezeigt werden:
    -   **Objektansichten**. Die optionalen Links, die verwendet werden, um die Darstellung der -Objekte zu steuern.
    -   **Befehle wurden korrigiert.** Die Befehle, die unabhängig von den aktuell ausgewählten Objekten sind.
    -   **Kontextbezogene Befehle**. Die Befehle, die von den aktuell ausgewählten Objekten abhängen und daher nicht immer angezeigt werden.
    -   **Siehe auch**. Die optionalen Links, die zu verwandten Systemsteuerungselementen navigieren.
-   **Verwenden Sie keine Aufgabenbereiche auf Spoke-Seiten.** Im Gegensatz zu Hubseiten sollten sich Spoke-Seiten auf die Durchführung der Aufgabe konzentrieren. Sie möchten Benutzer nicht dazu ermutigen, vor dem Abschluss weg zu navigieren.

**Siehe auch Links.**

-   **Geben Sie auch Links im Aufgabenbereich an, um Benutzern zu helfen, verwandte Systemsteuerungselemente zu finden, oder das richtige Systemsteuerungselement, wenn sie die falschen haben.** Link zu Elementen, die Benutzer wahrscheinlich Ihrem Systemsteuerungselement zuordnen.

    ![Screenshot der Info-Center "siehe auch"-Links ](images/winenv-ctrl-panels-image9.png)

    In diesem Beispiel ist das Element der Aktionscenter-Systemsteuerung mit verwandten Systemsteuerungselementen verknüpft.

-   **Link zu einer bestimmten Aufgabenseite, wenn benutzer dies wahrscheinlicher erkennen.** Andernfalls wird ein Link zum gesamten Systemsteuerungselement angezeigt. Verwenden Sie den Systemsteuerungsnamen, ohne den Ausdruck Systemsteuerung hinzufügen zu müssen.

### <a name="spoke-pages"></a>Spoke-Seiten

**Allgemein**

-   **Verwenden Sie Aufgabenseiten für häufig verwendete oder wichtige Aufgaben, bei denen Benutzer weitere Anleitungen und Erläuterungen benötigen.**
-   **Verwenden Sie Formularseiten für Features, die viele Einstellungen haben und von einer direkten Single-Page-Präsentation profitieren.** Die idealen Aufgaben für solche Seiten umfassen in der Regel offensichtliche Änderungen an einigen wenigen einfachen Eigenschaften.
-   **Verwenden Sie keine Aufgabenbereiche auf Spoke-Seiten.**

**Interaktion**

-   **Versuchen Sie, die Hauptaufgaben auf eine einzelne Seite zu beschränken.** Wenn mehr als eine Seite erforderlich ist, können Sie:
    -   **Verwenden Sie zwischengeschaltete Spoke-Seiten für zusätzliche oder optionale Schritte.** Zwischen-Spoke-Seiten werden von der endgültigen Spoke-Seite gebunden.
    -   **Verwenden Sie unabhängige Fenster für unabhängige Hilfsaufgaben.** Unabhängige Fenster werden eigenständig und unabhängig von der Hauptaufgabe ausgeführt.

Dadurch bleibt die Bedeutung der Commitschaltflächen für die Hauptaufgabe klar und eindeutig. Benutzer sollten immer sicher sein, zu verstehen, was sie committen.

-   **Verwenden Sie in einem Taskfluss nicht die Links Siehe auch.** Diese links zu verwandten, aber unterschiedlichen Systemsteuerungselementen. Obwohl die Navigation zu einem anderen Element auf Hubseiten akzeptabel ist, befindet es sich nicht auf Spoke-Seiten, da dies die Aufgabe unterbricht.
-   **Verwenden Sie keine Spoke-Seiten für einfache Eingaben oder Bestätigungen.** Verwenden Sie stattdessen modale Dialogfelder.

**Interaktion (Spoke-Zwischenseiten)**

-   **Verwenden Sie Aufgabenlinks oder eine Schaltfläche Weiter, um zur nächsten Seite zu navigieren.** Die Vorgehensweise zum Fortfahren mit dem nächsten Schritt sollte immer offensichtlich sein.
-   **Sie können Navigationslinks zu optionalen Aufgabenschritten verwenden.** Um Verwechslungen zu vermeiden, wenn Benutzer die Aufgabe übernehmen, sollten diese zusätzlichen Seiten Zwischenseiten innerhalb desselben Systemsteuerungselements sein. Sie sollten keine Commitschaltflächen haben, aber beim Commit der Hauptaufgabe ein Commit für sie auszuführen.

**Interaktion (letzte Spoke-Seiten)**

-   **Verwenden Sie Commitschaltflächen, um eine Aufgabe auszuführen.** Verwenden [](glossary.md) Sie ein Modell mit verzögerten Commits für Spoke-Seiten, damit Änderungen erst vorgenommen werden, wenn explizit ein Commit erfolgt (wenn Benutzer mit "Zurück", "Schließen" oder der Adressleiste weg navigieren, werden die Änderungen abgebrochen). Die Commitschaltflächen sind ein visueller Hinweis darauf, dass der Benutzer eine Aufgabe abschließen wird. Verwenden Sie zu diesem Zweck keine Links.
-   **Bestätigen Sie keine Commitschaltflächen (einschließlich Abbrechen).** Dies kann lästig sein. Ausnahmen:
    -   Die Aktion hat erhebliche Konsequenzen und kann nicht sofort behoben werden, wenn sie falsch ist.
    -   Die Aktion kann zu einem erheblichen Verlust der Zeit oder des Aufwands des Benutzers führen.
    -   Die Aktion ist eindeutig inkonsistent mit anderen Aktionen.
-   **Bestätigen Sie nicht, ob Benutzer Änderungen verwerfen,** indem Sie mithilfe von Zurück, Schließen oder der Adressleiste weg navigieren. Sie können jedoch bestätigen, dass eine potenziell unbeabsichtigte Navigation zu einem erheblichen Verlust der Zeit oder des Aufwands des Benutzers führen kann.
-   **Verwenden Sie keine Befehls- oder Navigationslinks** (einschließlich Siehe auch Links). Auf den letzten Spoke-Seiten sollten Benutzer die Aufgabe explizit abschließen oder abbrechen. Benutzern sollte nicht empfohlen werden, an einer anderen Stelle zu navigieren, da dies die Aufgabe wahrscheinlich implizit abbrechen würde.
-   **Wenn Benutzer eine Aufgabe abschließen oder abbrechen, sollten sie zurück an die Hubseite gesendet werden, von der die Aufgabe gestartet wurde.** Wenn keine solche Seite verfügbar ist, schließen Sie stattdessen das Systemsteuerungsfenster. Gehen Sie nicht davon aus, dass Spoke-Seiten immer von einer anderen Seite gestartet werden.
-   **Entfernen Sie die veralteten "committed"-Seiten** aus dem Windows-Explorer Back-Stapel, wenn Sie Benutzer auf die Seite zurückkehren, von der die Aufgabe gestartet wurde. Benutzer sollten nie die Seiten sehen, für die sie beim Klicken auf die Schaltfläche "Zurück". Benutzer sollten immer zusätzliche Änderungen vornehmen, indem sie die Aufgabe vollständig wiederholen, anstatt auf Zurück zu klicken, um veraltete Seiten zu ändern.
    -   **Entwickler:** Sie können diese veralteten Seiten mithilfe der APIs ITravelLog::FindTravelEntry() und ITravelLogEx::D eleteEntry() entfernen.

**Commitschaltflächen**

**Hinweis:** Schaltflächen zum Abbrechen werden als Commitschaltflächen betrachtet.

-   **Bestätigen Sie Aufgaben mithilfe von Commitschaltflächen, bei denen es sich um spezifische Antworten auf die Hauptanweisung handelt, anstatt mit generischen Bezeichnungen wie OK.** Die Bezeichnungen auf Den Commitschaltflächen sollten selbst sinnvoll sein. Vermeiden Sie die Verwendung von OK, da es sich nicht um eine bestimmte Antwort auf die Main-Anweisung handelt und daher leichter falsch verstanden werden kann. Darüber hinaus wird OK in der Regel mit modalen Dialogfeldern verwendet und impliziert fälschlicherweise das Schließen des Fensters des Systemsteuerungselements.
    -   **Ausnahmen:**
        -   Verwenden Sie OK für Seiten ohne Einstellungen.
        -   Verwenden Sie OK, wenn die spezifische Antwort immer noch generisch ist, z. B. Speichern, Auswählen oder Auswählen, wie beim Ändern einer bestimmten Einstellung oder einer Sammlung von Einstellungen.
        -   Verwenden Sie OK, wenn die Seite Optionsfelder enthält, die Antworten auf die Main-Anweisung sind. Um das Modell mit verzögerten Commits zu verwalten, können Sie keine Aufgabenlinks auf einer abschließenden Spoke-Seite verwenden.

            ![Screenshot der Webeinschränkungen mit der Schaltfläche "OK" ](images/winenv-ctrl-panels-image10.png)

            In diesem Beispiel sind die Optionsfelder, nicht die Commitschaltflächen, Antworten auf die Main-Anweisung.
-   **Geben Sie die Schaltfläche Abbrechen an, damit Benutzer Änderungen explizit abbrechen können.** Während Benutzer eine Aufgabe implizit abbrechen können, indem sie ihre Änderungen nicht bestätigen, können sie dies mit größerer Sicherheit über die Schaltfläche Abbrechen tun.
    -   **Ausnahme:** Geben Sie keine Schaltfläche Abbrechen für Aufgaben an, bei denen Benutzer keine Änderungen vornehmen können. Die Schaltfläche OK hat in diesem Fall die gleiche Wirkung wie Abbrechen.
-   **Verwenden Sie die Commitschaltflächen Schließen, Fertig oder Fertig stellen nicht.** Diese Schaltflächen werden in der Regel mit modalen Dialogfeldern verwendet und implizieren fälschlicherweise das Schließen des Elementfensters der Systemsteuerung. Benutzer können das Fenster mithilfe der Schaltfläche Schließen auf der Titelleiste schließen. Außerdem sind Fertig und Fertig stellen irreführend, da Benutzer auf die Seite zurückgegeben werden, auf der die Aufgabe gestartet wurde, sodass sie nicht wirklich fertig sind.
-   **Deaktivieren Sie keine Commitschaltflächen.** Andernfalls müssen Benutzer die Gründe für die Deaktivierung der Commitschaltflächen ableiten. Es ist besser, commit-Schaltflächen aktiviert zu lassen und bei jedem Problem eine hilfreiche Fehlermeldung zu erhalten.
-   **Stellen Sie sicher, dass die Commitschaltflächen auf der Seite angezeigt werden, ohne zu scrollen.** Wenn die Seite lang ist, können Sie Commitschaltflächen [](glossary.md)immer sichtbar machen, indem Sie sie in einem Befehlsbereich statt im Inhaltsbereich platzieren.

    ![Screenshot des Dialogfelds "Automatische Wiedergabe" ](images/winenv-ctrl-panels-image11.png)

    In diesem Beispiel ist die Größe des Inhaltsbereichs ungebunden, sodass die Commitschaltflächen im Befehlsbereich platziert werden.

-   Richten Sie die Commitschaltflächen rechts aus, und verwenden Sie diese Reihenfolge (von links nach rechts): Schaltflächen für positive Commits, Abbrechen und Anwenden.

**Vorschauschaltflächen**

-   Stellen Sie sicher, dass die Schaltfläche Vorschau bedeutet, dass die ausstehenden Änderungen jetzt angewendet werden, aber die aktuellen Einstellungen wiederhergestellt werden, wenn Benutzer von der Seite weg navigieren, ohne die Änderungen **zu übernehmen.**
-   **Sie können Vorschauschaltflächen auf jeder Spoke-Seite verwenden.** Hubseiten benötigen keine Vorschauschaltflächen, da sie ein [Direkt-Commit-Modell verwenden.](glossary.md)
-   **Erwägen Sie die Verwendung einer Vorschauschaltfläche anstelle einer Schaltfläche Anwenden für Systemsteuerungsseiten.** Vorschauschaltflächen sind für Benutzer einfacher zu verstehen und können auf jeder Spoke-Seite verwendet werden.
-   **Geben Sie nur dann eine Vorschauschaltfläche an, wenn die Seite einstellungen (mindestens eine) mit Auswirkungen auf die Benutzer hat.** Benutzer sollten in der Lage sein, eine Vorschau einer Änderung anzuzeigen, die Änderung zu bewerten und weitere Änderungen basierend auf dieser Auswertung vorzunehmen.
-   **Aktivieren Sie immer die Schaltfläche Vorschau.**

**Livevorschauen**

Ein Systemsteuerungselement verfügt über eine Livevorschau, wenn die Auswirkungen von Änderungen auf einer Spoke-Seite sofort angezeigt werden.

-   **Erwägen Sie die Verwendung der Livevorschau für Anzeigeeinstellungen, wenn Folgendes zu beachten ist:**
    -   Der Effekt ist offensichtlich, da er in der Regel für den gesamten Monitor gilt.
    -   Der Effekt kann ohne erhebliche Verzögerung angewendet werden.
    -   Der Effekt ist sicher und kann problemlos rückgängig gemacht werden.

        ![Screenshot des Dialogfelds "Farbeinstellungen ändern" ](images/winenv-ctrl-panels-image12.png)

        In diesem Beispiel werden die Auswirkungen der Windows-Einstellungen für Farbe und Darstellung sofort angezeigt. Dadurch können Benutzer änderungen mit minimalem Aufwand vornehmen.

-   **Verwenden Sie Änderungen speichern und Abbrechen für die Commitschaltflächen.** "Änderungen speichern" behält die aktuellen Einstellungen bei, während Abbrechen auf die ursprünglichen Einstellungen zurückwechselt. "Änderungen speichern" wird anstelle von OK verwendet, um deutlich zu machen, dass noch keine Änderungen in der Vorschau angewendet wurden.
-   **Geben Sie keine Schaltfläche Anwenden an.** Die Livevorschau macht Anwenden überflüssig.
-   **Stellen Sie alle Änderungen wieder auf, wenn Benutzer mithilfe von** Zurück, Schließen oder der Adressleiste weg navigieren. Um Änderungen zu erhalten, müssen Benutzer diese explizit commiten.

**Schaltflächen anwenden**

-   Stellen Sie sicher, dass die Schaltfläche Anwenden bedeutet, dass die ausstehenden Änderungen (seit dem Start der Aufgabe oder der letzten Apply-Aufgabe) angewendet werden, aber auf **der aktuellen Seite bleiben.** Auf diese Weise können Benutzer die Änderungen auswerten, bevor sie mit anderen Aufgaben arbeiten.
-   **Verwenden Sie Schaltflächen nur auf endgültigen Spoke-Seiten anwenden.** Schaltflächen anwenden sollten nicht auf Spoke-Zwischenseiten verwendet werden, um ein Direkt-Commit-Modell zu verwalten.
    -   **Ausnahme:** Sie können Schaltflächen anwenden auf einer Hybrid Hub-Seite verwenden, wenn das Ändern einer Einstellung eine Erhöhung [von erfordert.](glossary.md) Weitere Informationen finden Sie unter [Hub-Seiteninteraktion.](#hub-pages)
-   **Geben Sie nur dann eine Schaltfläche Anwenden an, wenn die Seite einstellungen (mindestens eine) mit Effekten enthält, die Benutzer auf sinnvolle Weise auswerten können.** In der Regel werden Schaltflächen anwenden verwendet, wenn Einstellungen sichtbare Änderungen vornehmen. Benutzer sollten in der Lage sein, eine Änderung anzuwenden, die Änderung zu bewerten und weitere Änderungen basierend auf dieser Auswertung vorzunehmen.
-   **Aktivieren Sie die Schaltfläche Anwenden nur, wenn Änderungen ausstehen.** Andernfalls deaktivieren Sie es.
-   **Weisen Sie "A" als Zugriffsschlüssel zu.**

### <a name="control-panel-integration"></a>Integration der Systemsteuerung

So integrieren Sie Ihr Systemsteuerungselement in Windows:

-   **Registrieren Sie Ihr Systemsteuerungselement (einschließlich Name, Beschreibung** und Symbol), damit Windows es kennt.
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
    -   Dies gilt nicht für die aktuelle Hardware- oder Softwarekonfiguration. Beispiel: Windows SideShow (sofern nicht von der aktuellen Hardware unterstützt).

    Das Entfernen solcher Systemsteuerungselemente aus den Kategorieseiten erleichtert die Suche nach Elementen der obersten Ebene. Aufgrund ihrer Verwendung sind diese Systemsteuerungselemente über Such- oder kontextbezogene Einstiegspunkte ausreichend auffindbar.

-   **Ordnen Sie das Element der Systemsteuerung der obersten Ebene der Kategorie zu, unter der Benutzer am wahrscheinlichsten danach suchen.** Diese Entscheidung sollte auf Benutzertests basieren.
-   **Erwägen Sie auch, Ihr Systemsteuerungselement der obersten Ebene der kategorie mit der zweitwahrscheinlichsten Zusicherung zuzuordnen.** Sie sollten ein Systemsteuerungselement zwei Kategorien zuordnen, wenn Benutzer wahrscheinlich an mehreren Stellen nach den Hauptaufgaben suchen.
-   **Ordnen Sie Ihr Systemsteuerungselement nicht mehr als zwei Kategorien zu.** Der Wert der Kategorisierung wird beeinträchtigt, wenn Systemsteuerungselemente in mehreren Kategorien angezeigt werden.

**Aufgabenlinks**

-   **Ordnen Sie das Systemsteuerungselement den primären Aufgaben zu.** Sie können bis zu fünf Aufgaben auf einer Kategorieseite anzeigen, aber zusätzliche Aufgaben werden für die Systemsteuerungssuche verwendet. Verwenden Sie den gleichen Ausdruck wie für Aufgabenlinks, und entfernen Sie möglicherweise einige Wörter, um die Aufgabenlinks prägnanter zu gestalten.
-   **Verwenden Sie lieber Aufgabenlinks, die zu verschiedenen Stellen in Ihrem Systemsteuerungselement führen.** Es kann verwirrend sein, mehrere Links zu demselben Ort zu haben.

**Suchbegriffe**

-   **Registrieren Sie Suchbegriffe für Ihr Systemsteuerungselement, das Benutzer höchstwahrscheinlich verwenden, um es zu beschreiben.** Diese Suchbegriffe sollten Folgendes enthalten:

    -   Die konfigurierten Features oder Objekte.
    -   Die primären Aufgaben.

    Diese Suchbegriffe sollten auf Benutzertests basieren.

-   **Schließen Sie auch allgemeine Synonyme für diese Suchbegriffe ein.** Monitor und Anzeige sind beispielsweise Synonyme, sodass beide Wörter eingeschlossen werden sollten.
-   **Fügen Sie alternative Schreibweisen oder Wortumbrüche ein.** Benutzer können z. B. nach Website und Website suchen. Erwägen Sie auch, häufige Rechtschreibfehler bereitzustellen.
-   **Betrachten Sie Singular- und Plural nomenformen.** Das Suchfeature der Systemsteuerung sucht nicht automatisch nach beiden Formularen. Stellen Sie die Formulare bereit, nach denen Benutzer wahrscheinlich suchen.
-   **Verwenden Sie einfache aktuelle Tense-Verben.** Wenn Sie connect als Suchbegriff registrieren, sucht das Suchfeature nicht automatisch nach Verbindungen, Verbindungen und Verbindungen.
-   **Machen Sie sich keine Gedanken über den Fall.** Bei der Suchfunktion wird die Groß-/Kleinschreibung nicht beachtet.

### <a name="standard-users-and-protected-administrators"></a>Standardbenutzer und geschützte Administratoren

**Viele Einstellungen erfordern Administratorrechte, um geändert werden zu können.** Wenn für einen Prozess Administratorrechte erforderlich sind, müssen [Standardbenutzer](glossary.md) und [geschützte Administratoren](glossary.md) unter Windows Vista und höher ihre Berechtigungen explizit erhöhen. Auf diese Weise wird verhindert, dass bösartiger Code mit Administratorrechten ausgeführt wird.

Weitere Informationen und Beispiele finden Sie unter [Benutzerkontensteuerung.](winenv-uac.md)

### <a name="schemes-and-themes"></a>Schemas und Designs

Ein Schema ist eine benannte Auflistung visueller Einstellungen. Ein Design ist eine benannte Sammlung von Einstellungen im gesamten System. Beispiele für Schemas und Designs sind Display, Mouse, Phone and Modem, Energieoptionen und Sound and Audio Options.

-   **Benutzern das Erstellen von Schemas erlauben, wenn:**

    -   **Benutzer ändern wahrscheinlich die Einstellungen.**
    -   **Benutzer ändern die Einstellungen höchstwahrscheinlich als Sammlung.**

    Schemas sind nützlich, wenn sich Benutzer in einer anderen Umgebung befinden, z. B. an einem anderen physischen Standort (Land/Region, Zeitzone). verwendung ihres Computers in einer anderen Situation (bei Akkus, angedockt/abgedockt); oder den Computer für eine andere Funktion (Präsentationen, Videowiedergabe) verwenden.

-   **Geben Sie mindestens ein Standardschema an.** Das Standardschema sollte gut benannt sein und in den meisten Fällen für die meisten Benutzer gelten. Benutzer sollten kein eigenes Schema erstellen müssen.
-   **Stellen Sie eine Vorschau** oder einen anderen Mechanismus bereit, damit Benutzer die Einstellungen innerhalb des Schemas sehen können.

    ![Screenshot des Dialogfelds "Personalisierung" ](images/winenv-ctrl-panels-image13.png)

    In diesem Beispiel zeigt das Systemsteuerungselement Personalisierung eine Vorschau der Desktop- und Darstellungseinstellungen an.

-   **Geben Sie die Befehle Speichern unter und Löschen an.** Ein Umbenennungsbefehl ist nicht erforderlich. Benutzer können Schemas nicht umbenennen, indem sie unter dem gewünschten Namen speichern und das ursprüngliche Schema löschen.
-   Wenn die Einstellungen nicht ohne Schema angewendet werden können, **dürfen Benutzer nicht alle Schemas löschen.** Benutzer sollten kein eigenes Schema erstellen müssen.
-   Wenn die Schemas nicht vollständig unabhängig sind (z. B. hängen Energieschemas vom aktuellen Laptopmodus ab), **stellen Sie sicher, dass es eine einfache Möglichkeit gibt, Einstellungen zu ändern, die für alle Schemas gelten.** Stellen Sie beispielsweise bei Energieschemas sicher, dass Benutzer festlegen können, was geschieht, wenn der Deckel eines tragbaren Computers an einem einzigen Ort geschlossen wird.

### <a name="miscellaneous"></a>Sonstiges

-   **Verwenden Sie Systemsteuerung Erweiterungen für Features, die vorhandene Windows-Funktionen ersetzen oder erweitern.** Die folgenden Systemsteuerungselemente sind erweiterbar: Bluetooth-Geräte, Anzeige, Internet, Tastatur, Maus, Netzwerk, Energie, System, Drahtlos (Mobilfunk).

### <a name="default-values"></a>Standardwerte

-   **Die Einstellungen in einem Systemsteuerungselement müssen den aktuellen Status des Features widerspiegeln.** Andernfalls wäre dies irreführend und würde möglicherweise zu unerwünschten Ergebnissen führen. Wenn Einstellungen beispielsweise die Empfehlungen, aber nicht den aktuellen Zustand widerspiegeln, können Benutzer auf Abbrechen klicken, anstatt Änderungen vorzunehmen, da sie denken, dass keine Änderungen erforderlich sind.
-   **Wählen Sie den sichersten (um Daten- oder Systemzugriffsverluste zu verhindern) und den sichersten Anfangszustand aus.** Angenommen, die meisten Benutzer ändern die Einstellungen nicht.
-   **Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie den Anfangszustand aus, der am wahrscheinlichsten oder praktischsten ist.**

## <a name="text"></a>Text

### <a name="item-names"></a>Elementnamen

-   **Wählen Sie einen beschreibenden Namen aus, der klar kommuniziert und unterscheidet, was das Systemsteuerungselement macht.** Die meisten Namen beschreiben das Zu konfigurierende Windows-Feature oder -Objekt und werden in der klassischen Ansicht der Startseite der Systemsteuerung angezeigt.
-   **Schließen Sie die Wörter "Einstellungen", "Optionen", "Eigenschaften" oder "Konfiguration" nicht in den Namen ein.** Dies ist impliziert, und wenn sie deaktiviert wird, ist es für Benutzer einfacher zu überprüfen.

    **Falsch:**

    Barrierefreiheitsoptionen

    Modemeinstellungen

    Energieoptionen

    Regions- und Sprachoptionen

    **Richtig:**

    Zugriff

    Modem

    Power

    Regionale Formate und Sprachen

    In den richtigen Beispielen werden unnötige Wörter entfernt.

-   **Wenn das Systemsteuerungselement verwandte Features konfiguriert, listen Sie nur die Features auf, die zum Identifizieren des Elements erforderlich sind, und listen Sie die Features auf, die am wahrscheinlichsten zuerst erkannt oder verwendet werden.**

    **Falsch:**

    Ordneroptionen

    Telefon- und Modemoptionen

    **Richtig:**

    Dateien und Ordner

    Modem

    In den richtigen Beispielen werden die primären Systemsteuerungselementfeatures hervorgehoben.

-   Verwenden Sie [die Groß-/Großschreibung im Titelformat.](glossary.md)

### <a name="page-titles"></a>Seitentitel

**Hinweis:** Wie bei allen Explorer-Fenstern werden die Titel der Systemsteuerungsseite in der [Adressleiste](glossary.md)angezeigt, jedoch nicht in der Titelleiste.

-   **Verwenden Sie für Hubseiten den Namen des Systemsteuerungselements.**
-   **Verwenden Sie für Spoke-Seiten eine kurze Zusammenfassung des Seitenzwecks.** Verwenden Sie die Hauptanweisung der Seite, wenn sie präzise ist. verwenden Sie andernfalls eine präzise Neuanordnung der Hauptanweisung.

    ![Screenshot des Dialogfelds "Energieoptionen" ](images/winenv-ctrl-panels-image6.png)

    In diesem Beispiel wird Energieoptionen anstelle der Hauptanweisung für den Seitentitel verwendet.

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

    

     

    Diese Beispiele zeigen die Beziehung des Aufgabenlinktexts, der Hauptanweisung und des Commitschaltflächentexts.

-   Während Aufgaben häufig mit Verben beginnen, **sollten Sie das Verb auf Kategorieseiten weglassen, wenn es sich um ein generisches, konfigurationsbezogenes Verb handelt, das die Kommunikation der Aufgabe nicht unterstützt.**

    **Spezifische, hilfreiche Verben:**

    Hinzufügen

    Prüfen

    Verbinden

    Kopieren

    Erstellen

    Löschen

    Trennen

    Installieren

    Entfernen

    Einrichten

    Start

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

    Sprecherlautstärke, Stummschaltung, Lautstärkesymbol

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

-   **Verwenden Sie für die Hubseite die Hauptanweisung, um das Ziel des Benutzers mit dem Systemsteuerungselement zu erläutern.** Die Hauptanweisung sollte Benutzern helfen, zu bestimmen, ob sie das richtige Systemsteuerungselement ausgewählt haben. Beachten Sie, dass Benutzer möglicherweise ihr Systemsteuerungselement fehlerhaft ausgewählt haben und tatsächlich nach Einstellungen suchen, die Teil eines anderen Systemsteuerungselements sind.

    **Beispiele:**

    Halten Sie Ihren Computer sicher und auf dem neuesten Stand.

    Optimieren Sie Ihren Computer, damit er leichter zu sehen, zu hören und zu steuern ist.

-   **Verwenden Sie für Spoke-Seiten die Hauptanweisung, um zu erläutern, was auf der Seite zu tun ist.** Die Anweisung sollte eine bestimmte Anweisung, imperative Richtung oder Frage sein. Gute Anweisungen kommunizieren das Ziel des Benutzers mit der Seite, anstatt sich ausschließlich auf die Mechanismen der Bearbeitung zu konzentrieren.

    **Falsch:**

    Auswählen einer Benachrichtigungsaufgabe

    **Richtig:**

    Angeben, wie eingehende Informationen behandelt werden sollen

    Die richtige Version kommuniziert das von der Seite erreichten Ziel besser.

-   **Verwenden Sie nach Möglichkeit bestimmte Verben.** Bestimmte Verben sind für Benutzer sinnvoller als generische Verben.
-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)
-   **Schließen Sie keine abschließenden Zeiträume ein, wenn die Anweisung eine -Anweisung ist.** Wenn es sich bei der Anweisung um eine Frage handelt, fügen Sie ein abschließendes Fragezeichen ein.

### <a name="supplemental-instructions"></a>Zusätzliche Anweisungen

-   **Verwenden Sie für die Hubseite die optionale zusätzliche Anweisung, um den Zweck des Systemsteuerungselements weiter zu erläutern.**
-   **Verwenden Sie für Spoke-Seiten die optionale ergänzende Anweisung, um zusätzliche Informationen anzuzeigen, die für das Verständnis oder die Verwendung der Seite hilfreich sind.** Sie können ausführlichere Informationen bereitstellen und Terminologie definieren.
-   Verwenden Sie vollständige Sätze und [die Groß-/Groß-/Formatvorlage.](glossary.md)

### <a name="page-text"></a>Seitentext

-   **Geben Sie die Hauptanweisung nicht im Inhaltsbereich neu.**
-   **Verwenden Sie das Wort "page", um auf die Seite selbst zu verweisen.**
-   **Verwenden Sie die zweite Person (Sie, Ihre),** um Benutzern zu sagen, was im Hauptanweisungs- und Inhaltsbereich zu tun ist. Häufig wird die zweite Person impliziert.

    **Beispiel:**

    Wählen Sie die Bilder aus, die Sie drucken möchten.

-   **Verwenden Sie die erste Person (I, me, my),** damit Benutzer dem Systemsteuerungselement mitteilen können, was im Inhaltsbereich zu tun ist, der auf die Hauptanweisung reagiert.

    **Beispiel:**

    Drucken Sie die Fotos auf meiner Kamera.

### <a name="task-links"></a>Aufgabenlinks

-   **Wählen Sie präzisen Linktext aus, der eindeutig kommuniziert und die Aufgabenverknüpfung unterscheidet.** Sie sollte selbsterklärend sein und der Main-Anweisung entsprechen. Benutzer sollten nicht herausfinden müssen, was der Link wirklich bedeutet oder wie er sich von anderen Links unterscheidet.
-   **Tasklinks werden immer mit einem Verb gestartet.**
-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)
-   Verwenden Sie keine Interpunktion am Ende.
-   **Wenn für den Aufgabenlink eine weitere Erläuterung erforderlich ist,** geben Sie die Erklärung in einem separaten Textsteuerfeld an, indem Sie vollständige Sätze und Satzzeichen beenden. Fügen Sie solche Erklärungen jedoch nur bei Bedarf hinzu, fügen Sie nicht allen Aufgabenlinks Erklärungen hinzu, da ein anderer Aufgabenlink eine solche benötigt.

Weitere Informationen und Beispiele finden Sie unter [Links](ctrl-command-links.md).

### <a name="commit-buttons"></a>Commitschaltflächen

-   **Verwenden Sie bestimmte Commitschaltflächenbezeichnungen, die für sich allein sinnvoll sind und mit der Main-Anweisung übereinstimmen.** Im Idealfall sollten Benutzer nichts anderes lesen müssen, um die Bezeichnung zu verstehen. Benutzer lesen die Bezeichnungen der Befehlsschaltfläche viel wahrscheinlicher als statischen Text.
-   **Starten Sie die Schaltflächenbezeichnungen für Commits immer mit einem Verb.**
-   **Verwenden Sie nicht Schließen, Fertig oder Fertig stellen.** Diese Schaltflächenbezeichnungen eignen sich besser für andere Fenstertypen.
-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)
-   Verwenden Sie keine Interpunktion am Ende.
-   Weisen Sie einen [eindeutigen Zugriffsschlüssel zu.](glossary.md)
    -   **Ausnahme:** Weisen Sie den Schaltflächen Abbrechen keine Zugriffsschlüssel zu, da esc sein Zugriffsschlüssel ist. Dadurch wird die Zuweisung der anderen Zugriffsschlüssel vereinfacht.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf die Startseite oder Kategorieseiten der Systemsteuerung:

-   Lesen Sie in der Benutzerdokumentation Systemsteuerung, indem Sie die Groß-/Formatvorlage verwenden und einen vorherigen bestimmten Artikel auslassen.

    **Beispiel:**

    Öffnen Systemsteuerung **in** Security Center .

-   Lesen Sie in der Programmierung und anderen technischen Dokumentationen die Startseite der Systemsteuerung und die Kategorieseite der Systemsteuerung, ohne eines der Wörter groß zu machen. Ein vorheriger definitiver Artikel ist optional.

Für Systemsteuerungselemente:

-   Wenn Sie auf ein einzelnes Systemsteuerungselement verweisen, verwenden Sie "Systemsteuerungselementname in Systemsteuerung" oder im Allgemeinen \[ \] "Systemsteuerung Element" in der Benutzerdokumentation. Verwenden Sie nicht Applet, Programm oder Systemsteuerung, um auf einzelne Systemsteuerungselemente zu verweisen.
-   Wenn Sie auf die Hubseite eines Systemsteuerungselements verweisen, verwenden Sie die "Hauptseite des \[ Elementnamens der \] Systemsteuerung".
-   Formatieren Sie den Namen der Systemsteuerung nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie den Namen nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiele:

-   Öffnen Systemsteuerung in der Datei **"Jugendschutz".**
-   Kehren Sie zur **Hauptseite Der Jugendschutz** zurück.

