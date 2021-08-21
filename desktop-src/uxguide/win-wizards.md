---
title: Assistenten
description: Trotz dieses hervorragenden, einfachen Namens sind Assistenten keine besondere Form der Benutzeroberfläche und verfügen nur über einen bestimmten Hilfsbereich.
ms.assetid: 122d6e65-92f0-4e8a-92f7-ecd7e90665c8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 31a9a0b4ed0c114dbdeadce7fe894bdd7da9cc099960f6ce2291e073ffdf3ef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119029062"
---
# <a name="wizards"></a>Assistenten

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Trotz dieses hervorragenden, einfachen Namens sind Assistenten keine besondere Form der Benutzeroberfläche und verfügen nur über einen bestimmten Hilfsbereich.

Assistenten werden zum Ausführen von mehrstufigen Aufgaben verwendet.

![Screenshot: Assistent "Drucker hinzufügen" mit "Welchen Druckertyp möchten Sie installieren?" an.](images/win-wizards-image1.png)

![Screenshot: Assistent "Drucker hinzufügen" bei der Suche nach verfügbaren Druckern](images/win-wizards-image2.png)

![Screenshot des Assistenten zum Hinzufügen von Druckern ](images/win-wizards-image3.png)

Mehrere Schritte eines Assistenten werden als Folge von Seiten dargestellt.

Assistenten enthalten in der Regel die folgenden Seitentypen:

-   Auswahlseiten werden verwendet, um Informationen zu sammeln und Benutzern das Treffen von Entscheidungen zu ermöglichen.
-   Die Seite Commit wird verwendet, um eine Aktion auszuführen, die nicht rückgängig zu machen ist, indem Sie auf Zurück oder Abbrechen klicken.
-   Die Seite Status wird verwendet, um den Fortschritt eines längeren Vorgangs anzuzeigen.

Der moderne Assistentenentwurf setzt auf Effizienz, sodass die Seite Status für kürzere Vorgänge optional ist und häufig auf die herkömmliche [Willkommensseite](glossary.md) und [die Seite Herzlichen Glückwunsch](glossary.md) am Anfang und Ende verzichten.

Alle Assistentenseiten verfügen über die folgenden Komponenten:

-   Eine Titelleiste zum Identifizieren des Namens des Assistenten mit einem Schaltfläche "Zurück" in der oberen linken Ecke und einer Schaltfläche Schließen mit optionalen Schaltflächen Minimieren/Maximieren und Wiederherstellen. Beachten Sie, dass die Titelleiste auch ein Symbol enthält, um es auf der Taskleiste zu identifizieren.
-   Eine Hauptanweisung, um das Ziel des Benutzers mit der Seite zu erklären.
-   Ein Inhaltsbereich mit optionalem Text und möglicherweise anderen Steuerelementen.
-   Ein Befehlsbereich mit mindestens einer Commitschaltfläche, um einen Commit für die Aufgabe durchzuführen oder mit dem nächsten Schritt fortzufahren.

Obwohl ein Assistent über mehrere Schritte verfügt, müssen diese Schritte aus Sicht des Benutzers zu einer einzelnen Aufgabe addiert werden. Dies ist das grundlegende Assistentenentwurfsprinzip von "ein Assistent, eine Aufgabe".

Daher ist in diesem Artikel eine Aufgabe die grundlegende Funktion eines Assistenten (die Aufgabe eines Setup-Assistenten ist z. B. die Installation eines Programms). Untergeordnete Aufgaben sind Aspekte der größeren Aufgabe (z. B. kann eine Untergeordnete Aufgabe eines Setup-Assistenten darin bestehen, das zu installierende Programm zu konfigurieren). Schließlich wird jede Assistentenseite als Schritt in einer bestimmten Unteraufgabe oder Aufgabe betrachtet (z. B. kann es zwei oder drei Schritte geben, die an der Konfiguration des Programms beteiligt sind).

**Hinweis:** Richtlinien zum [Einrichten](exper-setup.md)von , [Dialogfeldern](win-dialog-box.md)und [Statusleisten](progress-bars.md) werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Ein Assistent kann für jede Aufgabe verwendet werden, die mehrere Eingabeschritte erfordert. Effektive Assistenten haben jedoch zusätzliche Anforderungen:

-   **Führt der Assistent eine einzelne atomare Aufgabe aus?** Verwenden Sie keine Interaktionen, bei denen es sich nicht um einzelne Aufgaben handelt (ein ganzes Programm sollte niemals ein Assistent sein, es sei denn, es wird eine einzelne Aufgabe ausgeführt). Verwenden Sie keine Assistenten, um unabhängige Aufgaben oder größtenteils nicht verbundene Schritte zu kombinieren.
-   **Kann die Anzahl der erforderlichen Fragen reduziert werden? Gibt es akzeptable Standardwerte, die in den meisten Fällen gut funktionieren oder später bei Bedarf angepasst werden können? Kann daher die Anzahl der Seiten reduziert werden?** Wenn ja, versuchen Sie, die Aufgabe so zu vereinfachen, dass sie auf einer einzelnen Seite (z. B. einem Dialogfeld) angezeigt werden kann, oder beseitigen Sie die Notwendigkeit einer vollständigen Eingabe (sodass die Aufgabe direkt ausgeführt werden kann).
-   **Müssen die erforderlichen Fragen sequenziell bereitgestellt werden? Gibt es mehrere wahrscheinliche, aber optionale Fragen?** In diesem Falle sollten Sie ein Dialogfeld oder ein Dialogfeld im Registerkartenbett in Betracht ziehen.

    **Richtig:**

    ![Screenshot des Dialogfelds "Druckoptionen" ](images/win-wizards-image4.png)

    Das Dialogfeld Microsoft PowerPoint Druckoptionen enthält viele Benutzereingabeoptionen, sodass Sie sie in einem Assistenten präsentieren können. Es ist jedoch nicht erforderlich, sie sequenziell bereitzustellen, daher ist ein Dialogfeld eine bessere Wahl.

Assistenten sind eine relativ umfangreiche Form der Benutzeroberfläche. Wenn eine geeignete, schlankere Lösung verfügbar ist, verwenden Sie sie!

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="overuse-of-wizards"></a>Übermäßige Nutzung von Assistenten

In der Vergangenheit unterschieden sich Assistenten von der normalen Benutzeroberfläche darin, dass sie so entworfen wurden, dass sie Benutzern dabei helfen, besonders komplexe Aufgaben auszuführen (mit Schritten, die sich an unterschiedlichen Standorten befinden) und häufig über integrierte Intelligenz verfügten, um Benutzern den Erfolg zu erleichtern. Heute sollte die gesamte Benutzeroberfläche so konzipiert sein, dass Aufgaben so einfach wie möglich sind, sodass keine spezielle Benutzeroberfläche nur für diesen Zweck erforderlich ist.

Dennoch bleibt der Merken, dass Assistenten eine besondere Benutzeroberfläche sind– größtenteils, weil sie als "Assistenten" bezeichnet werden (viel kreativer als z.B. "Dialoge" und "Eigenschaftenfenster"). Stattdessen ist es besser, sie als mehrstufige Aufgaben zu betrachten und nicht besondere Aufmerksamkeit auf diese Tatsache zu lenken.

Überlegen Sie vor dem Erstellen eines Assistenten, ob Benutzer wirklich vom Hauptfluss des Programms unterbrochen werden müssen. Möglicherweise gibt es eine einfachere, inline kontextbezogene Lösung, die sich für Benutzer letztendlich hilfreicher und effizienter anfühlt. Ein schlecht entworfenes Feature in einem Programm erfordert z. B. keinen Assistenten, um es zu erklären und zu vereinfachen. Es ist erforderlich, das Feature selbst neu zu gestalten. Ein Assistent sollte nicht als Bandhilfe verwendet werden, um ein grundlegenderes Problem mit dem Programm zu beheben.

### <a name="wizards-do-have-appropriate-functions"></a>Assistenten verfügen über geeignete Funktionen.

Assistenten sind einer der Schlüssel zur Vereinfachung der Benutzerfreundlichkeit. Sie ermöglichen es Ihnen, einen komplexen Vorgang wie die Konfiguration eines Programms zu übernehmen und in eine Reihe einfacher Schritte aufzugliedern. An jedem Punkt des Prozesses können Sie eine Erläuterung der benötigten Informationen bereitstellen und Steuerelemente anzeigen, die es dem Benutzer ermöglichen, Eine Auswahl zu treffen und Text einzugeben.

Bestimmte Arten von mehrstufigen Aufgaben eignen sich für das Assistentenformular. Beispielsweise umfassen in Windows mehrere Assistenten Konnektivitätsfunktionen (mit dem Internet oder Unternehmensnetzwerk oder mit Peripheriegeräten wie Druckern und Faxcomputern).

![Screenshot des Verbindungs-Assistenten ](images/win-wizards-image5.png)

Das Herstellen einer Verbindung mit einem Netzwerk ist eine typische Aufgabe in Windows geeignet für einen Assistenten.

Hier besteht die Funktion des Assistenten darin, zwischen etwas Bekanntem und Stabilem (dem out-of-box-Betriebssystem) und etwas Unbekanntem und Variablem (Konnektivitätsvereinbarungen mit einem Telefonunternehmen oder Internetdienstanbieter) zu vermitteln. Die Komplexität von Computingökosystemen ist jetzt so wichtig, dass es wirklich hilfreich ist, Assistenten zu verwenden, um diese Komplexität zu reduzieren.

Andere Arten von Aufgaben, die sowie Windows Assistenten funktionieren, umfassen High-End-Funktionen (z. B. Sprach- und Handschrifterkennung) und Rich Media-Funktionen (z. B. das Konfigurieren von Optionen zum Drehen und Veröffentlichen von Filmen). Assistenten können auch für einfachere mehrstufige Aufgaben wie die Problembehandlung bereitgestellt werden. Kurz gesagt: Wenn verschiedene Benutzer Ihr Programm wahrscheinlich auf sehr unterschiedliche Weise erleben möchten, kann dies auf die Notwendigkeit eines Assistenten und seine Kapazität für mehrere Benutzereingabepunkte hinweisen.

Für Ihr Programm ist es im Voraus ein wenig Entwurfszeit wert, zu bestimmen, welche Funktion der Assistent bereitstellt und ob diese Funktion tatsächlich auf den Grad der Bereitstellung eines Assistenten steigt.

### <a name="wizard-length"></a>Länge des Assistenten

Designfragen stellen sich auf natürliche Weise zur Anzahl und Organisation von Seiten und Optionen. Beispiel:

-   Gibt es eine optimale Anzahl von Seiten für einen Assistenten? Oder zumindest ein gewünschter Bereich?
-   Sollte der Assistent präzise und optimiert sein, damit Benutzer ihn so schnell wie möglich abschließen können?
-   Sollten mehr Seiten vorhanden sein, für die weniger Auswahlmöglichkeiten erforderlich sind? Oder weniger Seiten mit mehr Komplexität? Welcher Entwurf gilt als besser verwendbar?
-   Können Sie schnellere Assistentenfunktionen entwickeln, indem Sie Benutzeroberflächenkonventionen wie Seiten im Registerkartenbereich anwenden?

Microsoft hat empfohlen, Assistenten mit maximal drei Seiten als einfache Assistenten zu entwerfen, und die Assistenten von vier oder mehr Seiten verwenden einen erweiterten Assistentenentwurf (siehe richtlinien für [die Windows Benutzerfreundlichkeit](/previous-versions/ms997609(v=msdn.10)) von 1999). Die aktuellen Assistentenentwurfsstandards unterscheiden sich jedoch von einem der wichtigsten Unterschiede zwischen den einfachen und erweiterten Formularen (die Verwendung der Seiten Willkommen und Herzlichen Glückwunsch), sodass diese Kategorien nun unzureichend sind und die Anzahl der Seiten, die die Entwurfsauswahl bestimmen, willkürlich erscheint.

Der Assistent sollte so lang oder kurz sein, wie die Aufgabe erfordert. Es gibt keine feste Richtlinie für ihre Länge. Ein einseitiger Assistent sollte wirklich als Dialogfeld angezeigt werden, sodass zwei Seiten wahrscheinlich die kompakteste Form für einen Assistenten sind.

**Richtig:**

![Screenshot des Dialogfelds "Datenträger erstellen" ](images/win-wizards-image6.png)

Diese Aufgabe verfügt über so wenige Optionen, dass die Darstellung als Assistent unnötig wäre. Ein Dialogfeld ist das geeignete Formular für diese Benutzeroberfläche.

Wenn Sie am anderen Ende des Spektrums über einen Assistenten verfügen, der mehrere Entscheidungspunkte und Verzweigungen enthält und häufig dazu führt, dass Benutzer ihren Navigationspfad verlieren, haben Sie einen praktischen Grenzwert überschritten und sollten die Länge des Assistenten verringern. Alternativ können Sie den Assistenten in mehrere unterschiedliche Aufgaben untergliedern.

Achten Sie bei der Ermittlung der am besten geeigneten Länge für Den Assistenten besonders auf Die Zielbenutzer. Programme für Endbenutzer wie Heimbenutzer und Büromitarbeiter verwenden tendenziell Assistenten, um die Komplexität auszublenden. Die Assistenten sind so kurz wie möglich, mit einem sauberen, einfachen Seitenentwurf und vorab ausgewählten Standardwerten für so viele Optionen wie möglich. Im Gegensatz dazu sind Server-Assistenten oder -Programme, die für IT-Experten vorgesehen sind, in der Regel länger und komplexer. Diese Gruppe von Zielbenutzern verfügt über eine viel höhere Toleranz für Konfigurationsentscheidungen und kann tatsächlich verdächtig werden, wenn zu viel Komplexität verborgen ist.

Wenn ein Assistent von Natur aus eine komplexe Aufgabe vereinfacht, sollte er dies relativ minimal für eine technisch anspruchsvolle Zielgruppe und relativ aggressiv für eine ungenannte Benutzerbasis tun.

**Richtig:**

![Screenshot des Assistenten zum Anzeigen von Sprachen ](images/win-wizards-image7.png)

Diese Assistentenseite ist gut für Endbenutzer konzipiert, da sie ein potenziell komplexes Subjekt durch eine einfache, logische binäre Auswahl reduziert: Entweder installieren oder deinstallieren.

**Richtig:**

![Screenshot: Seite "Featureauswahl" des Assistenten "SQL Server Setup"](images/win-wizards-image8.png)

Im Setup-Assistenten für Microsoft SQL Server 2008 ist der Seitenentwurf viel komplexer, und die zahlreichen Auswahlmöglichkeiten erfordern mehr Überlegungen, aber die Zielgruppe sind Datenbankadministratoren, die eine strenge Kontrolle über die Funktionsauswahl erwarten.

Achten Sie abschließend darauf, wie häufig die jeweilige Aufgabe ausgeführt werden kann. Eine selten ausgeführte Aufgabe kann einen längeren Assistenten bereitstellen, wohingegen häufige Aufgaben auf jeden Fall die Kürze bevorzugen sollten.

### <a name="branching"></a>Verzweigung

Bei längeren Assistenten müssen Sie möglicherweise Branches des Taskflusses erstellen, in denen sich die Seitensequenz je nach bereitgestellter Benutzereingabe "upstream" unterscheiden kann. Verzweigungen sind für Benutzer grundsätzlich nicht mehr zu finden, daher müssen Sie die Benutzeroberfläche so entwerfen, dass Stabilität vermittelt wird. Es wird empfohlen, nicht mehr als zwei Entscheidungspunkte, die Verzweigung im gesamten Assistenten verursachen, und nicht mehr als einen geschachtelten Branch innerhalb eines einzelnen Branchs zu verwenden.

Richtlinien zum Erstellen einer stabilen Benutzeroberfläche innerhalb eines Verzweigungs-Assistenten finden Sie unter [Verzweigungen](#branching) im Abschnitt Richtlinien dieses Artikels.

### <a name="providing-a-navigation-guide"></a>Bereitstellen eines Navigationshandbuchs

Navigationsleitfäden können nützlich sein, wenn die Aufgabe viele Schritte auft, und Benutzer möglicherweise ihre Stelle in der Sequenz verlieren oder einfach wissen möchten, wie viel Zeit benötigt wird.

Navigationshandbücher werden häufig als Liste von Seiten oder Abschnitten des Assistenten angezeigt und sehen ein wenig wie ein Inhaltsverzeichnis in einer Spalte oder einem Bereich auf der linken Seite jeder Seite aus. Obwohl die Liste im gesamten Assistenten beibehalten wird (die gleiche Liste von Seiten wird auf jeder Seite angezeigt), gibt es einige visuelle Möglichkeiten, um anzuzeigen, wo sich der Benutzer derzeit in der Sequenz befindet (z. B. fett formatiert, um die aktive Seite oder den aktiven Abschnitt zu unterscheiden).

Navigationshandbücher können sequenziell oder nicht sequenziell sein. Der sequenzielle Typ stellt die vergangenen Seiten zusammen mit den bekannten zukünftigen Seiten vor. Sie können die Zukunft in Bezug auf Schritte anstelle von Seiten präsentieren, wenn die Schritte bekannt sind und Seiten abhängig sind. Sie können Seiten dann dynamisch auffüllen, sobald sie bekannt werden. Da die Navigationssequenz fest ist, ist die Navigationsanleitung nicht interaktiv.

Nicht sequenzielle Navigationshandbücher sind interaktiv, sodass Benutzer zuvor angezeigte Seiten direkt erneut besuchen können. Sie können auch die Navigationssequenz für Seiten überspringen, die optional sind. Optionale Seiten müssen über Standardwerte verfügen, die in den meisten Fällen akzeptabel sind. Mit dieser Art von Leitfaden:

-   Zuvor angezeigte Seiten können immer direkt angezeigt werden.
-   Zukünftige Seiten werden möglicherweise nicht angezeigt, wenn sie über Voraussetzungen verfügen.
-   Seiten, die besucht werden können, sollten sichtbar von Seiten unterschieden werden, die nicht möglich sind (z. B. durch Die Verwendung von aktiven oder deaktivierten Links) sowie von Seiten, die erforderlich oder optional sind.

Benutzer können sich über die Bedeutung der Schaltfläche "Zurück" in diesem Szenario verwirren. Führt das Klicken auf Zurück zur vorherigen Seite oder zum vorherigen Abschnitt im Navigationshandbuch oder zur letzten angezeigten Seite oder zum letzten angezeigten Abschnitt? Da Windows Assistenten jetzt die Schaltfläche "Zurück" in der oberen linken Ecke der Assistentenseiten platzieren, anstatt in der unteren rechten Ecke mit den anderen Commitschaltflächen, denken Benutzer an back-Funktionen wie im Web. Die beste Lösung besteht also in der Bedeutung Schaltfläche "Zurück" der Webnavigation (wenn Sie auf Zurück klicken, um zur letzten seite oder zum letzten angezeigten Abschnitt zu führen), und den Navigationsleitfaden des Assistenten für die sequenzielle Navigation zu verwenden.

### <a name="page-integrity"></a>Seitenintegrität

Der Entwurf des Assistenten umfasst nicht nur Entscheidungen in Bezug auf den gesamten Aufgabenfluss, z. B. die Behandlung der Navigation und der Verzweigungserfahrung, sondern auch entscheidungen zu den einzelnen Seiten, aus denen der Assistent besteht. **Das wichtigste Prinzip beim Entwerfen guter Assistentenseiten ist die Integrität: Der Inhalt einer Seite sollte zusammengehören.**

Assistentenseiten sind deutlich nutzbarer, wenn jede Seite konzeptionell zusammenhängt und nur einen Aspekt der Gesamtaufgabe betrifft. Die [Hauptanweisung](glossary.md) ist die primäre Möglichkeit, dies zu erreichen. Identifizieren Sie das Ziel oder den Zweck der Seite für Benutzer eindeutig. [Zusätzliche Anweisungen](glossary.md)und alle Steuerelemente auf der Seite beziehen sich alle direkt auf die Hauptanweisung. Obwohl Assistentenseiten Benutzern Optionen bieten sollten, für die einige Gedanken erforderlich sind, sieht dieser Aufwand nicht wie eine Arbeit aus, da er eng auf die Integrität der Seite selbst ausgerichtet ist.

Leider machen Designer von Assistenten häufig einen Fehler, wenn Benutzer schnell auf die Schaltfläche Weiter klicken, um die Benutzerfreundlichkeit, Einfachheit und Integrität ihrer Seiten zu belegen. Die endgültige Assistentenerfahrung ist nicht Weiter, Weiter, Weiter, Weiter, Fertig stellen. Obwohl eine solche Erfahrung darauf hindeutet, dass die Standardwerte gut ausgewählt wurden, deutet dies auch darauf hin, dass der Assistent nicht wirklich notwendig war, da alle Optionen optional sind.

In Bezug auf Visuals und Text sollten Sie diese Elemente auf die grundlegenden Elemente ausdrungen. Widersetzen Sie sich der Bitte, mehrere untergeordnete Aufgaben auf einer einzelnen Seite (dem "assistenten" genannten Assistenten) zu bündeln oder auf Registerkarten zurück zu greifen, um komplexe Eingabeanforderungen zu präsentieren. Eine einzelne Seite sollte eine einzelne Unteraufgabe der Gesamtaufgabe des Assistenten abdecken.

**Falsch:**

![Screenshot des SQL Server-Setup-Assistenten ](images/win-wizards-image9.png)

Da drei Registerkarten mit ziemlich dichten Benutzereingaben erforderlich sind, versucht diese Assistentenseite zu viel zu erreichen.

In den meisten Fällen sollten Sie die Größe jeder Seite im assistentenweiten Bereich behalten, um ein einheitliches Aussehen und Einheitlichen zu fördern. Obwohl Windows Assistenten die Größe von Seiten zulassen, sodass die Größe einer Seite der Inhaltsmenge entspricht, nutzen nur wenige diese Option.

Und schließlich verwalten Sie strukturelle Elemente jeder Assistentenseite durch die Sequenz. Verschieben Sie z. B. den Schaltfläche "Zurück" aus der oberen linken Ecke nicht wieder nach unten in den Bereich mit den Commitschaltflächen für ein oder zwei Seiten. Diese Ebene der Layoutkonsistenz hilft Benutzern, sich innerhalb des Assistenten stabil zu fühlen. Stellen Sie sich dies als Baseline für die visuelle Integrität einer Seite vor.

### <a name="finding-the-right-level-of-communication"></a>Auffinden der richtigen Kommunikationsebene

Benutzer haben eine geringe Toleranz für das Lesen großer Textblöcke auf dem Bildschirm und noch weniger innerhalb einer Benutzeroberflächenoberfläche, deren ausdrücklicher Zweck darin besteht, sich schnell durch eine Aufgabe zu bewegen.

Assistenten neigen zu einer Über kommunizieren. Sie nehmen viel Platz auf dem Bildschirm in Dies scheint ein Laufwerk zu ermutigen, den Platz zu füllen. Es ist wie eine Variation des Texts zum Gesetz: Benutzeroberfläche wird erweitert, um den verfügbaren Platz zu füllen.

Ein Grund für diese Überschreitung ist die Redundanz. Aufgrund der Vorlagen, die im frühen Entwurf des Assistenten verwendet wurden, kann dieselbe Sprache an mehreren Stellen auf einer Seite angezeigt werden, z. B. in der Titelleiste, überschriften, text text, control labels und so weiter.

Es lohnt sich, einen professionellen Editor zu verwenden, um den Text Des Assistenten unnötig zu beschneiden. Vermeiden Sie unnötige Fragen und Optionen auf einzelnen Seiten, und beseitigen Sie ganze Seiten aus dem Assistenten als Ganzes (z. B. die herkömmlichen Seiten Willkommen und Herzlichen Glückwunsch). Machen Sie sich mit einer präzisen Hauptanweisung auf den Punkt der Seite, indem Sie die Sprache verwenden, die Ihre Zielgruppe zum Beschreiben der Aufgabe verwendet, und nicht den Jargon der Technologie oder des Features, die Sie oder Ihr Team intern verwenden. Dieser benutzerorientierte Ansatz ist entscheidend, um die Kommunikation der Assistenten Ihres Programms zu verbessern.

Achten Sie besonders auf den Ton Ihres Assistenten: Manchmal sind die dauerhaftsten Bilder Ihres Programms nicht das Ergebnis, was Sie sagen, sondern wie Sie es sagen! In Assistenten sind Benutzer mit einem benutzerfreundlichen, konversationsorientierten Ton und der verwendung des Pronomens der zweiten Person ("Sie") gut, wenn das Programm um Eingaben bittet. Weitere Richtlinien finden Sie unter [Stil und Ton.](text-style-tone.md)

Das Reduzieren der Wortanzahl auf der Assistentenseite ist im Allgemeinen ersetzbar, aber achten Sie darauf, nicht zu weit zu gehen. Wenn die Aufgabe wichtig ist und einen Assistenten zusichert, schätzen Die Benutzer, dass sie über genügend Informationen zum Treffen von sinnvollen Entscheidungen versiert sind. Das folgende Beispiel zeigt, wie Der Text des Assistenten ohne Bedeutungseinbußen komprimiert werden kann.

**Vorher:**

![Screenshot des Cleartype-Assistenten, Entwurf ](images/win-wizards-image10.png)

**Nachher:**

![Screenshot des Cleartype-Assistenten, überarbeitet ](images/win-wizards-image11.png)

Die bearbeitete Version dieser Assistentenseite stellt eine aufgabenorientierte Hauptanweisung zur Verfügung, entfernt den unnötigen erläuternden Absatz unter der Hauptanweisung und überarbeitet die Kontrollkästchenbezeichnung, um den Zweck des Kontrollkästchens zu verdeutlichen.

**Wenn Sie nur drei Dinge tun...**

1. Ordnen Sie die Aufgabe, die Sie ausführen möchten, mit der entsprechenden Benutzeroberfläche zu, um die Aufgabe auszuführen. Verwenden Sie nicht einfach standardmäßig einen Assistenten, wenn Sie der Meinung sind, dass Sie viele Eingaben von Benutzern sammeln müssen.

2. Denken Sie sorgfältig über die Länge und Struktur des Assistenten nach. bevorzugen kurze Assistenten ohne Verzweigung, um die Benutzererfahrung so einfach wie möglich zu halten, damit Benutzer wieder zur primären Aufgabe oder zum Interesse an Ihrem Programm zurückkommen können.

3. Stellen Sie die Integrität jeder Seite im Assistenten sicher: Der Inhalt einer Seite sollte eindeutig zusammengehören.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Ziehen Sie zunächst einfache Alternativen in Betracht, z. B. Dialogfelder, Aufgabenbereiche oder einzelne Seiten.** Sie müssen keine Assistenten verwenden. Sie können hilfreiche Informationen und Unterstützung auf jeder Benutzeroberfläche bereitstellen.
-   **Verwenden Sie Assistenten für mehrstufige Aufgaben.** Verwenden Sie mehrseitige Dialogfelder für Aufgaben mit nur einem Schritt mit Feedback. Weitere Richtlinien finden Sie unter [Dialogfelder](win-dialog-box.md).

    **Richtig:**

    ![Screenshot des Dialogfelds "Diagnose" ](images/win-wizards-image12.png)

    ![Screenshot des Feedbacks zum Diagnosedialogfeld ](images/win-wizards-image13.png)

    In diesem Beispiel besteht Windows Netzwerkdiagnose aus Fortschritts- und Ergebnisseiten. Da es sich bei der Aufgabe nur um einen einzelnen Schritt handelt, sind die Navigationsschaltflächen, die Benutzer in einem Assistenten benötigen, nicht erforderlich. Sie wird effektiv als mehrseitiges Dialogfeld dargestellt.

### <a name="window-size"></a>Fenstergröße

-   **Wählen Sie eine Fenstergröße aus, die alle Assistentenseiten ohne vertikales oder horizontales Seitenscrolling anzeigen kann.** Während die Steuerelemente auf der Seite möglicherweise einen Bildlauf erfordern, dürfen die Assistentenseiten selbst nicht scrollen.
-   **Größe der Fenster groß genug, um ihre Aufgaben bequem auszuführen.** Das Seitenlayout sollte nicht überrollt werden oder erfordert, dass Benutzer übermäßig scrollen oder die Größe ändern.
-   **Aber machen Sie Fenster nicht übermäßig groß.** Größere Fenster machen die Aufgabe komplexer und erfordern zusätzliche Bewegungen für die Interaktion.
-   **Verwenden Sie größenvergrößerbare Fenster für einen Assistenten, der von mehr Bildschirmfläche profitieren kann, dies aber nicht erfordert.** Weisen Sie eine geeignete Mindestgröße zu. Fenster, die die Größe ändern können, sind hilfreich, wenn Seiten eine Interaktion mit inhalt erfordern, deren Größe geändert werden kann, z. B. große Listenansichten.

    **Richtig:**

    ![Screenshot des Visual Studio-Setups, Teilliste ](images/win-wizards-image14.png)

    **Besser:**

    ![Screenshot des Visual Studio-Setups, vollständige Liste ](images/win-wizards-image15.png)

    In diesem Beispiel können Benutzer durch ändern der Größe des Fensters die vollständige Liste anzeigen.

-   **Erwägen Sie die Verwendung von Assistenten mit dynamischer Größe, deren Seitengröße sich nach Bedarf für den Inhalt ändert.** Auf diese Weise kann ein Assistent Seitenlayouts mit einer Vielzahl von Inhalten aufnehmen.
-   **Bevorzugen Sie die statische Größenanpassung gegenüber der dynamischen, wenn Benutzer die Änderungen möglicherweise als fehlende Stabilität in ihrer Erfahrung mit dem Assistenten betrachten.** Die visuelle Stabilität lädt häufig die Aufnahme von Inhalten ein. Die meisten Assistenten sollten standardmäßige, statische Fenstergrößen übernehmen, wobei die dynamische Größe für Sonderfälle reserviert ist.

### <a name="wizard-length"></a>Länge des Assistenten

-   **Sorgen Sie dafür, dass Der Assistent so präzise und optimiert wie möglich ist.** Entfernen Sie unnötige Optionen und Fragen, und verwenden Sie intelligente Standardwerte, um die Anzahl der Seiten zu reduzieren, die für Benutzereingaben erforderlich sind.
    -   **Ausnahme:** IT-Experten und andere technische Benutzer verfügen über eine höhere Toleranz für längere Assistenten und detaillierte Eingabeanforderungen.
-   **Legen Sie den Assistenten auf mindestens zwei Seiten an.** Ein einseitiger Assistent sollte stattdessen als Dialogfeld umgestaltet werden.
-   **Reduzieren Sie die Seitenanzahl des Assistenten nicht einfach, indem Sie die Komplexität der einzelnen Seiten erhöhen.** Beispielsweise sollte eine Assistentenseite, die drei Registerkarten enthält, die Benutzereingaben erfordern, als drei separate Seiten neu gestaltet werden.
-   **Erhöhen Sie nicht die Seitenanzahl des Assistenten, indem Sie jede Seite so einfach gestalten, dass Benutzer unbenannt durch die gesamte Sequenz auf Weiter klicken.** Dies ist ein gängiger Entwurfsfehler des Assistenten. Wenn eine Assistentenseite nicht mindestens ein gewisses Maß an Überlegungen erfordert, muss sie sich wahrscheinlich überhaupt nicht im Assistenten befinden.

### <a name="branching"></a>Verzweigung

-   **Der Entwurf des Assistenten ohne Verzweigung wird der Verzweigung vorgezogen.** Assistenten ohne Verzweigung sind in der Regel einfacher, kürzer und leicht zu navigieren. Verzweigungs-Assistenten erschweren es Benutzern, zu bestimmen, wie viele Schritte in der Aufgabe ausgeführt werden und wo sie sich in der Sequenz befinden.
-   **Wenn Sie verzweigen müssen, helfen Sie Benutzern, sich mit einer der folgenden Verfahren zu orientieren:**
    -   **Aufzählen von Seiten.** Eine gängige Methode besteht darin, den Speicherort des Benutzers in der Sequenz auf jeder Seite anzugeben, z. B. mit dem Ausdruck Schritt X von Y. Stellen Sie sicher, dass der Endpunkt (Y) stabil ist. Wenn sich der Wert ändert, beeinträchtigt dies die Zuverlässigkeit der Benutzer.
    -   **Schließen Sie die Unterschritte** ein (z. B. Schritt 2a von 6).
    -   **Machen Sie Schritte seitenunabhängig, wobei jeder Schritt mehrere Seiten umfassen kann.** Beispielsweise kann ein Reisedienst eine Assistentenorganisation basierend auf bewährten E-Commerce-Konventionen für die Branche einsetzen.

        **Richtig:**

        ![Screenshot der schrittbasierten Assistentenorganisation ](images/win-wizards-image16.png)

        Logische Bezeichnungen können benutzern eines Verzweigungs-Assistenten eine angemessene Ausrichtung bieten.

    -   **Optionale Schritte werden in der Enumerationssequenz als persistent behandelt.** Wenn ein Branch beispielsweise nur einige optionale Schritte überspringt, überspringen Sie einfach auch die Schritte im Feedback, anstatt erneut zu nummerieren. Wenn ein Benutzer also auf Seite 2 eine Auswahl trifft, die dazu führt, dass die Seiten 3 und 4 optional sind, zeigen Sie die Schritte 1, 2, 5 und 6 von 6 an. Geben Sie die Schritte 5 und 6 nicht neu an.
    -   **Wenn der Assistent einen einzelnen Branch verwendet und der Branch früh in der Aufgabe auftritt, starten Sie die Sequenz an diesem Punkt, und verwenden Sie dann einfach den Nichtverzweigungsansatz.** Das heißt, ab dem Punkt des Branchs wird der Fortschritt nacheinander bis zum Ende des Branchs ausgeführt.

-   **Wenn Sie eine Verzweigung ausführen müssen, beschränken Sie die Anzahl der Verzweigungen innerhalb eines einzelnen Assistenten auf ein oder zwei.** Schließen Sie niemals mehr als einen Branch in einen Branch ein (eine "geschachtelte" Verzweigung).

### <a name="commit-buttons"></a>Commitschaltflächen

-   **Wenn Benutzer einen Commit für eine Aufgabe ausführen, verwenden Sie eine Commitschaltfläche, die eine bestimmte Antwort auf die Hauptanweisung ist** (z. B. Drucken, Verbinden oder Starten). Verwenden Sie keine generischen Bezeichnungen wie Next (was keine Verpflichtung impliziert) oder Finish (was nicht spezifisch ist) zum Committen einer Aufgabe. Die Bezeichnungen auf diesen Commitschaltflächen sollten für sich allein sinnvoll sein. Starten Sie immer Commit-Schaltflächenbezeichnungen mit einem Verb. **Ausnahmen:**
    -   Verwenden Sie Fertig stellen, wenn die spezifischen Antworten noch generisch sind, z. B. Speichern, Auswählen, Auswählen oder Abrufen.
    -   Verwenden Sie Fertig stellen, um eine bestimmte Einstellung oder eine Sammlung von Einstellungen zu ändern.
-   **Ein einzelner Assistent kann über mehrere Commitpunkte verfügen, aber ein einzelner Punkt wird bevorzugt.**
-   **Bei Bedarf können Sie Commitschaltflächen auf einer Seite umbenennen oder ausblenden.** Diese Flexibilität ist ein Vorteil des neuen Assistentenentwurfs in Windows, der in älteren Assistenten nicht verfügbar war. Beachten Sie, dass sich das Ausblenden einer Commitschaltfläche von der Deaktivierung unterscheidet.
-   **Deaktivieren Sie keine Positive Commit-Schaltfläche.** Andernfalls müssen Benutzer ableiten, warum die Commitschaltflächen deaktiviert sind. Es ist besser, commit-Schaltflächen aktiviert zu lassen und immer dann eine hilfreiche Fehlermeldung zu geben, wenn ein Problem auftritt. Das Deaktivieren der Schaltfläche ist nur akzeptabel, wenn der Grund dafür offensichtlich und eindeutig ist.
-   **Verwechseln Sie Navigationsschaltflächen (Weiter und Zurück) nicht mit Commitschaltflächen.** Als Nächstes bedeutet, dass der Assistent ohne Verpflichtung ausgeführt wird. Zurück sollte immer auf der nächsten Seite verfügbar sein, und wenn Sie auf Zurück klicken, sollte die Auswirkung der letzten Schaltfläche Weiter rückgängig werden. Wenn dies nicht möglich ist, leisten Benutzer eine Verpflichtung, und dies wird durch eine bestimmte Bezeichnung auf der Commitschaltfläche angezeigt. Weitere Richtlinien zu den Schaltflächen Weiter und Zurück finden Sie unter [Navigation](#providing-a-navigation-guide).

### <a name="cancel-buttons"></a>Schaltflächen "Abbrechen"

-   **Bitten Sie Die Benutzer nicht, zu bestätigen, ob sie wirklich einen Abbruch beabsichtigen.** Dies kann mühsam sein. **Ausnahmen:**
    -   Die Aktion hat erhebliche Folgen und ist, wenn sie falsch ist, nicht ohne weiteres behebbar.
    -   Die Aktion kann zu einem erheblichen Verlust der Zeit oder des Aufwands des Benutzers führen.
    -   Die Aktion ist eindeutig inkonsistent mit anderen Aktionen.
-   **Benutzern das Neustarten von Assistenten für den Fall gestatten, dass sie versehentlich abgebrochen wurden.**
-   **Deaktivieren Sie nicht die Schaltfläche Abbrechen. Ausnahmen:**
    -   Wenn das Abbrechen schädlich ist, kann dies beim Ausführen einer Aufgabe in eigenständigen Assistenten der Fall sein.
    -   Wenn das Abbrechen nicht möglich ist, kann dies der Fall sein, wenn der Assistent nicht über die Kontrolle über alle Schritte verfügt.

### <a name="close-buttons"></a>Schaltflächen schließen

-   **Verwenden Sie Schließen für Follow-Up- und Vervollständigungsseiten.** Verwenden Sie nicht Abbrechen, da durch das Schließen des Fensters keine Änderungen oder Aktionen abgebrochen werden, die an diesem Punkt vorgenommen wurden. Verwenden Sie Done nicht, da es sich nicht um ein imperatives Verb handelt.
-   **Sobald die Aufgabe ausgeführt wurde, sollte Abbrechen zu Schließen (für eigenständige Assistenten) werden.** Die Auswirkung von Schließen besteht einfach darin, das Fenster zu schließen.

### <a name="other-controls"></a>Weitere Steuermöglichkeiten

-   **Verwenden Sie Befehlslinks nur für Auswahlmöglichkeiten, nicht für Verpflichtungen.** Bestimmte Commitschaltflächen zeigen die Verpflichtung deutlich besser an als Befehlslinks in einem Assistenten.
-   **Wenn Sie Befehlslinks verwenden, blenden Sie die Schaltfläche Weiter aus, lassen Sie jedoch die Schaltfläche Abbrechen.**

### <a name="using-pages-vs-dialog-boxes-or-inline-ui"></a>Verwenden von Seiten (im Vergleich zu Dialogfeldern oder der Inline-Benutzeroberfläche)

-   **Im Allgemeinen bevorzugen Sie Seiten Dialogfeldern.** Benutzer erwarten, dass Assistenten seitenbasiert sind.
-   **Verwenden Sie Dialogfelder, um** Seiten zu vervollständigen, z. B. mit Objektauswahl und Browsern.
-   **Verwenden Sie Dialogfelder, um Fehlermeldungen zu erhalten, die für die gesamte Seite gelten und sich aus dem Klicken auf eine Commitschaltfläche ergeben.**
-   **Verwenden Sie die Inlinedarstellung für einfache dynamische Verhaltensweisen,** z. B. progressive Offenlegung und kontextbezogene Benutzeroberfläche.
-   **Verwenden Sie die Inlinepräsentation für Fehlermeldungen, die für bestimmte Steuerelemente gelten.**

### <a name="wizard-pages"></a>Seiten des Assistenten

-   **Konzentrieren Sie sich auf die effiziente Entscheidungsfindung.** Reduzieren Sie die Anzahl der Seiten, um sich auf das Wesentliche zu konzentrieren. Konsolidieren Sie verwandte Seiten, und nehmen Sie optionale Seiten aus dem Hauptflow. Wenn Benutzer im Assistenten vollständig auf Weiter klicken, scheint dies zunächst eine gute Erfahrung zu sein, aber wenn Benutzer die Standardwerte nie ändern müssen, sind die Seiten wahrscheinlich unnötig.
-   **Entwerfen Sie jede Seite so, dass sie einen zweck- und visuellen Zweck hat.** Weitere Informationen finden Sie unter [Seitenintegrität.](#page-integrity)
-   **Verwenden Sie keine Willkommensseiten, damit die erste Seite nach Möglichkeit funktionsfähig ist.** Verwenden Sie eine optionale Erste Schritte Seite nur in den:

    -   Der Assistent verfügt über Voraussetzungen, die erforderlich sind, um den Assistenten erfolgreich abzuschließen.
    -   Benutzer verstehen den Zweck des Assistenten möglicherweise nicht basierend auf der ersten Auswahlseite, und es gibt keinen Platz für eine weitere Erläuterung.
    -   Die Hauptanweisung für Erste Schritte Seiten lautet "Before you begin:".

    **Falsch:**

    ![Screenshot der Willkommensseite des Mappoint-Setups ](images/win-wizards-image17.png)

-   Moderne Assistenten entscheiden sich für funktionale erste Seiten. Hier ist nichts zu tun, aber klicken Sie auf Weiter. Warum erzwingen Sie, dass Benutzer diese Tokensteuer für ihre wertvolle Zeit zahlen?
-   **Auf Seiten, auf denen Benutzer aufgefordert werden, Entscheidungen zu treffen, optimieren Sie für die wahrscheinlichsten Fälle.** Diese Seitentypen sollten tatsächliche Auswahlmöglichkeiten bieten, nicht nur Anweisungen.
    -   Wenn Sie keine Erste Schritte Seite verwenden, erläutern Sie oben auf der ersten Seite der Auswahl den Zweck des Assistenten.
-   **Verwenden Sie Commitseiten, um zu verdeutlichen, wann Benutzer einen Commit für die Aufgabe ausführen.** In der Regel ist die Seite Commit die letzte Auswahlseite, und die Schaltfläche Weiter wird neu bezeichnet, um anzugeben, dass für die Aufgabe ein Commit ausgeführt wird.
    -   Verwenden Sie keine Zusammenfassungsseiten, die lediglich die vorherige Auswahl des Benutzers zusammenfassen, es sei denn, die Aufgabe ist riskant (mit Sicherheit oder Zeit- oder Geldverlust) oder es besteht eine gute Wahrscheinlichkeit, dass Benutzer ihre Auswahl überprüfen müssen.
-   **Verwenden Sie Statusseiten, um den Status eines längeren Vorgangs anzuzeigen.** Nach erfolgreichem Abschluss sollte die Statusseite automatisch mit dem nächsten Schritt fortschreiten. Sie sollte nur dann auf der Statusseite bleiben, wenn ein Problem vorliegt, das der Benutzer sehen muss. Das Klicken auf Zurück zu einer Statusseite sollte keine Nebeneffekte haben.
    -   **Verwenden Sie eine einzelne, bestimmende Statusanzeige.** Befolgen Sie die Richtlinien für die [statusbestimmte Statusanzeige,](progress-bars.md)einschließlich:
        -   Geben Sie die Vervollständigung eindeutig an. Lassen Sie eine Statusanzeige nur dann auf 100 Prozent zu, wenn der Vorgang abgeschlossen wurde.
        -   Starten Sie den Fortschritt nicht neu. Eine Statusanzeige verliert ihren Wert, wenn sie neu gestartet wird (möglicherweise weil ein Schritt im Vorgang abgeschlossen wird), da Benutzer nicht wissen können, wann der Vorgang abgeschlossen wird. Lassen Sie stattdessen alle Schritte im Vorgang einen Teil des Fortschritts teilen, und lassen Sie die Statusanzeige einmal abgeschlossen werden.
    -   **Geben Sie eine kurze Beschreibung des aktuellen Schritts oberhalb der Statusanzeige an.** Für schnelle Vorgänge ist dieser Text nicht erforderlich. die Statusanzeige allein ist ausreichend. Bei Vorgängen, die eine Minute oder länger erfordern, kann Text hilfreich sein.
        -   Verwenden Sie Satzfragmente, die in der Regel mit einem Verb beginnen und mit auslassungszeichen enden. Beispiele: Kopieren von Dateien..., Installieren der erforderlichen Komponenten...
        -   Platzieren Sie Text über der Leiste, nicht darunter.
        -   **Falsch:**
        -   ![Screenshot der Statusanzeige mit folgendem Text ](images/win-wizards-image18.png)
        -   In diesem Beispiel sollte der erläuternde Text über der Statusleiste angezeigt werden.
        -   Vermeiden Sie es, die Statusseite mit unnötigen Details zu überladen. Diese Seite ist nicht für technischen Support vorgesehen. sie ist für Benutzer vorgesehen.
        -   **Falsch:**
        -   ![Screenshot der Statusanzeige mit zu vielen Details ](images/win-wizards-image19.png)
        -   In diesem Beispiel sind technische Details wie GUIDs für Benutzer bedeutungslos.
-   **Verwenden Sie keine Herzlichen Glückwunschseiten, die nur den Assistenten beenden.** Wenn die Ergebnisse des Assistenten für Benutzer deutlich sichtbar sind, schließen Sie den Assistenten einfach auf der endgültigen Commitschaltfläche.
    -   Verwenden Sie Follow-Up Seiten, wenn es verwandte Aufgaben gibt, die Benutzer wahrscheinlich als Nachverfolgung ausführen. Vermeiden Sie vertraute Nachverfolgungsaufgaben, z. B. "E-Mail senden".
    -   Verwenden Sie Vervollständigungsseiten nur, wenn die Ergebnisse nicht sichtbar sind und es keine bessere Möglichkeit gibt, Feedback für den Taskabschluss bereitzustellen.
    -   Assistenten mit Statusseiten müssen eine Seite "Abschluss" oder Follow-Up Seite verwenden, um den Abschluss der Aufgabe anzugeben. Schließen Sie bei Aufgaben mit langer Ausführungslaufzeit den Assistenten auf der Seite Commit, und verwenden Sie Benachrichtigungen, um Feedback zu geben.
-   **Verwenden Sie Zusammenfassungsseiten nur, wenn die Eingabe komplex ist und Benutzer überprüfen müssen, ob die Aufgabe ein erhebliches Risiko mit sich bringt (z. B. ein finanzieller Übergang), oder wenn der Assistent basierend auf Benutzereingaben Maßnahmen ergreifen wird, die nicht offensichtlich sind (um Vertrauen durch Transparenz aufzubauen).** Häufig erfüllen Zusammenfassungsseiten diese Relevanzleiste nicht und können ausgelassen werden.
-   **Verwenden Sie Fehlerseiten, wenn der Assistent aufgrund eines Problems, bei dem keine Wiederherstellung möglich ist, nicht abgeschlossen werden kann.** Erläutern Sie auf dieser Seite, was das Problem in einer eindeutigen Sprache ist, ohne dass benutzer den technischen Jargon nicht verstehen. Stellen Sie außerdem praktische Schritte bereit, die Benutzer ausführen können, um das Problem zu lösen. Weitere Richtlinien finden Sie unter [Fehlermeldungen.](mess-error.md)
    -   **Ausnahme:** Wenn der Assistent mit einem kleineren Problem abgeschlossen wird, bei dem eine Wiederherstellung möglich ist, stellen Sie das Problem als zusätzliche Aufgabe anstelle eines Fehlers dar. Verwenden Sie positive, erfolgsorientierte, fördernde Sprache, nicht Begriffe wie Fehler, Fehler oder Problem. Verwenden Sie kein Fehlersymbol.

### <a name="navigation"></a>Navigation

-   **Verwenden Sie Next nur, wenn Sie ohne Verpflichtung zur nächsten Seite wechseln.** Das Wechseln zur nächsten Seite wird als Verpflichtung betrachtet, wenn deren Auswirkung nicht rückgängig machen kann, indem Sie auf Zurück oder Abbrechen klicken.
-   **Verwenden Sie Nur Zurück, um Fehler zu korrigieren.** Abgesehen von der Behebung von Fehlern sollten Benutzer nicht auf Zurück klicken müssen, um in einer Aufgabe Fortschritte zu machen.
-   **Beibehalten der Benutzerauswahl über die Navigation.** Wenn der Benutzer z. B. Änderungen vornimmt, auf Zurück und dann auf Weiter klickt, sollten diese Änderungen beibehalten werden. Benutzer erwarten nicht, dass sie Änderungen erneut eingeben müssen, es sei denn, sie haben sich explizit dafür entschieden, sie zu löschen.
-   **Deaktivieren Sie die Schaltfläche "Zurück" nur, wenn das Wiederholen der Schritte schädlich ist.**
-   **Benutzern das Durchsuchen oder Überarbeiten von Optionen in den folgenden Navigationsszenarien gestatten:**
    -   Der Benutzer gibt eine Eingabe ein, klickt auf die Schaltfläche "Commit", klickt auf Zurück, um vorherige Änderungen zu überprüfen, ändert nichts und klickt dann erneut auf die Schaltfläche "Commit". Normalerweise sollte dies möglich sein, und der zweite Commit sollte einfach zur nächsten Seite übergehen (da die Aufgabe bereits ausgeführt wurde).
    -   Der Benutzer gibt eine Eingabe ein, klickt auf die Schaltfläche "Commit", klickt auf Zurück, um vorherige Änderungen zu überprüfen, ändert etwas, und klickt dann erneut auf die Schaltfläche "Commit". Normalerweise sollte dies möglich sein, und der zweite Commit sollte die Aufgabe mit der geänderten Eingabe wiederholen (ersetzen oder rückgängig machen).

### <a name="help"></a>Hilfe

-   **Entwurfs-Assistentenseiten, um genügend Informationen bereitzustellen, sodass der Verweis auf die Dokumentation in der Programmhilfe nicht erforderlich ist.** Ein Assistent entfernt Benutzer bereits von ihrer gewünschten direkten Interaktion mit dem Programm. Wenn Benutzer nach externer Hilfe suchen müssen, werden sie noch weiter aus diesem Zustand entfernt. Hilfe sollte die Ausnahme und nicht die Regel sein.
-   **Wenn Sie einen Zugriffspunkt für Hilfe bereitstellen müssen, verwenden Sie einen Link im unteren linken Bereich des Inhaltsbereichs der Seite (oberhalb des Befehlsbereichs).** Dieser Link sollte kurz sein und in der Regel in Form einer Frage formuliert werden, die Benutzer am wahrscheinlichsten beantworten möchten.
-   **Richtig:**
-   ![Screenshot der Assistentenseite mit Hilfelink ](images/win-wizards-image5.png)
-   Dieser Link zur Hilfe ist geeignet, da grundlegende Hintergrundinformationen wie diese die Assistentenseite zu überladen würden.

## <a name="text"></a>Text

### <a name="general"></a>Allgemein

-   Verwenden Sie Sie und Ihre , um auf den Benutzer und den Computer, das Dokument, die Einstellungen usw. des Benutzers zu verweisen. Verwenden Sie nicht die erste Person (I, my), um auf den Computer oder den Assistenten zu verweisen. Es ist jedoch akzeptabel, die erste Person in optionen zu verwenden, die der Benutzer auswählt. **Beispiel: Kontrollkästchen Nur meine Verwendung.**
-   Jede Assistentenseite muss über eine [Hauptanweisung verfügen.](glossary.md)

### <a name="titles"></a>Titel

-   Geben Sie den Namen des Assistenten in die Titelleiste ein. Verwenden Sie [die Groß-/Großschreibung im Titelformat.](glossary.md)
-   Titel dürfen keine Interpunktion enthalten, mit Ausnahme von Titeln mit Fragezeichen.
-   Schließen Sie das Wort Assistent nicht in Assistententitel ein. Verwenden Sie beispielsweise Verbinden zu einem Netzwerk anstelle von Network Setup-Assistant.

### <a name="buttons"></a>Schaltflächen

-   Fügen Sie keinen Text in die Schaltfläche "Zurück" ein. Verwenden Sie stattdessen das Pfeilsymbol ohne Bezeichnung.
-   Fügen Sie Text in die Schaltfläche Weiter ein. Verwenden Sie neben dem Wort Weiter keine Glyphen (z. B. > oder >>).
-   Verwenden Sie bestimmte Commitschaltflächenbezeichnungen, die eigenständig sinnvoll sind und eine Antwort auf die Hauptanweisung sind. Im Idealfall sollten Benutzer nichts anderes lesen müssen, um die Bezeichnung zu verstehen. Die Wahrscheinlichkeit, dass Benutzer Befehlsschaltflächenbezeichnungen lesen, ist weitaus wahrscheinlicher als statischer Text.
-   Verwenden Sie nach Möglichkeit nicht das Wort Fertig stellen für die Bezeichnung der Commitschaltfläche, da es in der Regel eine bessere, spezifischere Commitschaltfläche gibt:
    -   Wenn durch Klicken auf die Schaltfläche ein Commit für die Aufgabe ausgeführt wird (sodass die Aufgabe noch nicht ausgeführt wurde), verwenden Sie eine bestimmte Bezeichnung, die mit einem Verb beginnt, das eine Antwort auf die Hauptanweisung ist (Beispiele: Drucken, Verbinden, Starten).
    -   Wenn die Aufgabe bereits im Assistenten ausgeführt wurde, verwenden Sie stattdessen Schließen.

        **Ausnahmen:**

        -   Sie können Fertig stellen verwenden, wenn die bestimmte Bezeichnung noch generisch ist, z. B. Speichern, Auswählen, Auswählen oder Abrufen.
        -   Sie können Fertig stellen verwenden, wenn die Aufgabe das Ändern einer Einstellung oder sammlung von Einstellungen umfasst.

-   Starten Sie Commit-Schaltflächenbezeichnungen mit einem Verb. Ausnahmen sind OK, Ja und Nein.
-   Verwenden Sie [die Groß-/Großschreibung im Satzformat.](glossary.md)
-   Verwenden Sie keine Interpunktion am Ende.

## <a name="documentation"></a>Dokumentation

-   Obwohl die meisten Windows Assistenten nicht mehr das Wort Assistent im Titel haben, ist es akzeptabel, Assistenten in der Dokumentation als Assistenten zu bezeichnen. Dieser Verweis sollte in Kleinbuchstaben geschrieben werden.
-   **Richtig:**
-   Wenn Sie ein Netzwerk zum ersten Mal einrichten, können Sie hilfe erhalten, indem Sie die **Verbinden zu einem Netzwerk-Assistenten** verwenden.
-   Einige Legacy-Assistenten aus früheren Versionen von Windows enthalten möglicherweise den Assistenten im Titel . Wenn Sie auf einen dieser Assistenten verweisen, ist es akzeptabel, den \[ \] X-Assistenten zu verwenden, um zu vermeiden, dass der \[ \] X-Assistent gesagt wird.
-   Verweisen Sie auf einen einzelnen Bildschirm in einem Assistenten als Seite.

 

 