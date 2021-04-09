---
title: Assistenten
description: Trotz dieses wunderbaren namens sind die Assistenten nicht wirklich eine besondere Form der Benutzeroberfläche, und Sie verfügen nur über einen bestimmten Bereich von Hilfsprogramm.
ms.assetid: 122d6e65-92f0-4e8a-92f7-ecd7e90665c8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6455c38228606932e9144c744dd217d0a7fa67e8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103869356"
---
# <a name="wizards"></a>Assistenten

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Trotz dieses wunderbaren namens sind die Assistenten nicht wirklich eine besondere Form der Benutzeroberfläche, und Sie verfügen nur über einen bestimmten Bereich von Hilfsprogramm.

Assistenten werden verwendet, um Aufgaben mit mehreren Schritten auszuführen.

![Screenshot, der den Assistenten zum Hinzufügen von Druckern mit der Art des Druckers anzeigt, den Sie installieren möchten. an.](images/win-wizards-image1.png)

![Screenshot mit dem Assistenten zum Hinzufügen von Druckern bei der Suche nach verfügbaren Druckern.](images/win-wizards-image2.png)

![Screenshot des Assistenten zum Hinzufügen von Druckern ](images/win-wizards-image3.png)

Mehrere Schritte eines Assistenten werden als Sequenz von Seiten angezeigt.

Assistenten enthalten in der Regel die folgenden Seiten Typen:

-   Auswahl Seiten werden verwendet, um Informationen zu erfassen und Benutzern das Treffen von Optionen zu ermöglichen.
-   Die Seite Commit wird verwendet, um eine Aktion auszuführen, die nicht rückgängig gemacht werden kann, indem Sie auf zurück oder Abbrechen klicken.
-   Die Seite Status wird verwendet, um den Fortschritt eines langwierigen Vorgangs anzuzeigen.

Beim modern Wizard Design wird eine Premium-Effizienz erzielt, bei der die Statusseite für kürzere Vorgänge optional ist und häufig mit der herkömmlichen [Willkommensseite](glossary.md) und der [Herzlichen Glückwunsch Seite](glossary.md) am Anfang und Ende ausgegeben wird.

Alle Assistenten Seiten enthalten folgende Komponenten:

-   Eine Titelleiste, um den Namen des Assistenten zu identifizieren, mit der Schaltfläche zurück in der oberen linken Ecke und der Schaltfläche Schließen mit optionalen Schaltflächen zum minimieren, maximieren und wiederherstellen. Beachten Sie, dass die Titelleiste auch ein Symbol für die Identifizierung auf der Taskleiste enthält.
-   Eine Haupt Anweisung, um das Ziel des Benutzers mit der Seite zu erläutern.
-   Ein Inhalts Bereich mit optionalem Text und möglicherweise anderen Steuerelementen.
-   Einen Befehlsbereich mit mindestens einer Commit-Schaltfläche, um den Task zu übertragen oder mit dem nächsten Schritt fortzufahren.

Obwohl ein Assistent mehrere Schritte umfasst, müssen diese Schritte alle aus der Sicht des Benutzers zu einer einzelnen Aufgabe hinzugefügt werden. Dies ist das grundlegende Entwurfs Prinzip des Assistenten für "ein Assistent, eine Aufgabe".

Daher ist in diesem Artikel die grundlegende Funktion eines Assistenten (z. b. die Aufgabe eines Setup-Assistenten, ein Programm zu installieren). Untergeordnete Aufgaben sind Aspekte der größeren Aufgabe (z. b. besteht eine Unteraufgabe eines Setup-Assistenten darin, das zu installierende Programm zu konfigurieren). Schließlich wird jede Seite des Assistenten als Schritt in einer bestimmten Unteraufgabe oder Aufgabe betrachtet (es können z. b. zwei oder drei Schritte erforderlich sein, um das Programm zu konfigurieren).

**Hinweis:** Richtlinien im Zusammenhang mit [Setup](exper-setup.md), [Dialogfeldern](win-dialog-box.md)und Status [leisten](progress-bars.md) werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Ein Assistent kann für alle Aufgaben verwendet werden, für die mehrere Eingabe Schritte erforderlich sind. Effektive Assistenten haben jedoch zusätzliche Anforderungen:

-   **Führt der Assistent eine einzelne atomarische Aufgabe aus?** Verwenden Sie keine Interaktionen, die keine einzelnen Aufgaben sind (ein gesamtes Programm sollte nie ein Assistent sein, es sei denn, es wird eine einzelne Aufgabe ausgeführt). Verwenden Sie Assistenten nicht, um unabhängige Aufgaben oder größtenteils nicht verknüpfte Schritte zu kombinieren.
-   **Kann die Anzahl der erforderlichen Fragen reduziert werden? Gibt es akzeptable Standardwerte, die in den meisten Fällen gut funktionieren oder später nach Bedarf angepasst werden können? Kann die Anzahl der Seiten folglich reduziert werden?** Wenn dies der Fall ist, versuchen Sie, die Aufgabe so zu vereinfachen, dass Sie auf einer einzelnen Seite (z. b. in einem Dialogfeld) angezeigt werden kann, oder dass die Eingabe nicht vollständig erforderlich ist (sodass die Aufgabe direkt ausgeführt werden kann).
-   **Müssen die erforderlichen Fragen sequenziell bereitgestellt werden? Gibt es mehrere wahrscheinliche, aber optionale Fragen?** Wenn dies der Fall ist, sollten Sie ein Dialogfeld oder ein Dialogfeld im Registerkarten Format

    **Richtig:**

    ![Screenshot des Dialog Felds "Druckoptionen" ](images/win-wizards-image4.png)

    Das Microsoft PowerPoint-Dialogfeld "Druckoptionen" enthält viele Benutzereingabe Optionen, sodass Sie Sie in einem Assistenten präsentieren können. Es ist jedoch nicht notwendig, Sie sequenziell bereitzustellen, sodass ein Dialogfeld besser geeignet ist.

Assistenten sind eine relativ hohe Form der Benutzeroberfläche. Wenn eine geeignete Lösung mit leichterem Gewicht verfügbar ist, verwenden Sie Sie!

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="overuse-of-wizards"></a>Über Verwendung von Assistenten

In der Vergangenheit unterscheiden sich die Assistenten von der normalen Benutzeroberfläche dahin, dass Sie so konzipiert wurden, dass Benutzer besonders komplexe Aufgaben ausführen können (mit Schritten, die sich an unterschiedlichen Standorten befinden) und häufig über integrierte Intelligenz verfügten, damit Benutzer erfolgreich Heute sollten alle Benutzeroberflächen so entworfen werden, dass Aufgaben so einfach wie möglich ausgeführt werden, sodass es nicht erforderlich ist, nur für diesen Zweck eine spezielle Benutzeroberfläche zu erstellen.

Der Gedanke bleibt jedoch bestehen, wenn die Assistenten eine spezielle Benutzeroberfläche sind – größtenteils, weil Sie als "Assistenten" bezeichnet werden (viel kreativer als "Dialoge" und "Eigenschaften Fenster"). Es ist vielmehr besser, Sie als mehrstufige Aufgaben zu berücksichtigen und keine besondere Aufmerksamkeit auf diese Tatsache zu ziehen.

Berücksichtigen Sie vor dem Erstellen eines Assistenten, ob Benutzer wirklich vom Hauptprogramm Ablauf unterbrochen werden müssen. Möglicherweise gibt es eine leichtere, Inline-und kontextabhängige Lösung, die letztendlich für Benutzer hilfreicher und effizienter ist. Beispielsweise ist es in einem Programm nicht möglich, einen Assistenten zu erläutern und zu vereinfachen. Er erfordert eine Umgestaltung der Funktion selbst. Ein Assistent sollte nicht als Band Hilfe verwendet werden, um ein grundlegendes Problem mit dem Programm zu beheben.

### <a name="wizards-do-have-appropriate-functions"></a>Assistenten verfügen über entsprechende Funktionen

Assistenten sind einer der Schlüssel zum Vereinfachen der Benutzer Leistung. Sie ermöglichen es Ihnen, einen komplexen Vorgang auszuführen, z. b. die Konfiguration eines Programms, und ihn in eine Reihe einfacher Schritte zu unterbrechen. An jedem Punkt des Vorgangs können Sie eine Erläuterung dazu bereitstellen, was erforderlich ist, und Steuerelemente anzeigen, die es dem Benutzer ermöglichen, eine Auswahl vorzunehmen und Text einzugeben.

Bestimmte Arten von Tasks mit mehreren Schritten eignen sich für das Formular des Assistenten. In Windows umfassen mehrere Assistenten z. b. Konnektivitätsfunktionen (für das Internet oder das Unternehmensnetzwerk oder für Peripheriegeräte wie Drucker und faxcomputer).

![Screenshot des Verbindungs-Assistenten ](images/win-wizards-image5.png)

Das Herstellen einer Verbindung mit einem Netzwerk ist eine typische Aufgabe in Windows, die für einen Assistenten geeignet ist.

Hier besteht die Funktion des Assistenten darin, zwischen etwas bekanntem und stabiler (dem Out-of-Box-Betriebssystem) und unbekannten und Variablen (konnektivitätsanordnungen mit einem Telefonunternehmen oder einem Internet Dienstanbieter) zu vermitteln. Die Komplexität der computingresssourcen ist erheblich genug, da es nun wirklich hilfreich ist, diese Komplexität mit Assistenten zu verringern.

Andere Arten von Aufgaben, die gut als Windows-Assistenten funktionieren, umfassen High-End-Funktionen (z. b. Spracherkennung und Handschrifterkennung) und Rich-Media-Umgebungen (z. b. das Konfigurieren von Optionen zum Erstellen und Veröffentlichen von Assistenten können auch für weitere grundlegende mehrstufige Aufgaben bereitgestellt werden, z. b. für die Problembehandlung. Kurz gesagt, wenn verschiedene Benutzer Ihr Programm wahrscheinlich auf vielfältige Weise erleben möchten, kann dies auf den Bedarf an einem Assistenten und seine Kapazität für mehrere Benutzereingabe Punkte hinweisen.

Für Ihr Programm lohnt es sich, eine gewisse Entwurfszeit zu bestimmen, um zu bestimmen, welche Funktion der Assistent verwendet, und ob diese Funktion tatsächlich auf die Ebene der Bereitstellung eines Assistenten ansteigt.

### <a name="wizard-length"></a>Assistenten Länge

Entwurfs Fragen werden natürlich um die Anzahl und die Organisation von Seiten und Optionen herum entstehen. Beispiel:

-   Gibt es eine optimale Anzahl von Seiten für einen Assistenten? Oder zumindest ein wünschenswert?
-   Sollte der Assistent präzise und optimiert werden, damit Benutzer ihn so schnell wie möglich vervollständigen können?
-   Sollten mehr Seiten vorhanden sein, die weniger Optionen erfordern? Oder weniger Seiten mit höherer Komplexität? Welches Design gilt als besser verwendbar?
-   Können Sie mithilfe von Benutzeroberflächen Konventionen, z. b. Seiten im Registerkarten Format, schnellere Assistenten-Erfahrungen entwickeln

Microsoft hat empfohlen, dass Assistenten mit drei Seiten oder weniger als einfache Assistenten entworfen werden, und für die von vier oder mehr Seiten wird ein erweiterter Assistent entworfen (siehe Windows-Richtlinien für [Benutzer](/previous-versions/ms997609(v=msdn.10)) Oberflächen von 1999). Doch die aktuellen Entwurfs Standards des Assistenten verzichten darauf, was einer der wesentlichen Unterschiede zwischen den einfachen und erweiterten Formularen war (die Verwendung der Seiten willkommen und herzlichen Glückwunsch). diese Kategorien sind nun nicht mehr ausreichend, und die Anzahl der Seiten, die die Entwurfs Auswahl bestimmen, scheint willkürlich.

Der Assistent sollte so lang oder kurz sein, wie dies für die Aufgabe erforderlich ist. Es gibt keine fixed-Richtlinie für seine Länge. Ein unidirektionaler Assistent sollte wirklich als Dialogfeld angezeigt werden, sodass zwei Seiten wahrscheinlich die möglichst komprimierte Form für einen Assistenten darstellen.

**Richtig:**

![Screenshot des Dialog Felds "Disc erstellen" ](images/win-wizards-image6.png)

Diese Aufgabe verfügt über so wenige Optionen, wie Sie als Assistent dargestellt werden kann. Ein Dialogfeld ist das geeignete Formular für diese Benutzeroberfläche.

Wenn Sie am anderen Ende des Spektrums über einen Assistenten verfügen, der mehrere Entscheidungspunkte und Verzweigungen umfasst, und die Benutzer häufig die Spur Ihres Navigations Pfads verlieren, haben Sie ein praktisches Limit überschritten und sollten die Länge des Assistenten verringern. Alternativ dazu können Sie den Assistenten möglicherweise in mehrere unterschiedliche Aufgaben unterteilen.

Wenn Sie die am besten geeignete Länge für Ihren Assistenten ermitteln, achten Sie besonders auf die Ziel Benutzer. Programme für Endbenutzer, wie z. b. Heimanwender und Office-Worker, verwenden Assistenten, um die Komplexität zu verbergen. die Assistenten sind so kurz wie möglich, mit einfachem, einfachem Seiten Entwurf und vorab ausgewählten Standardwerten für so viele Optionen wie möglich. Im Gegensatz dazu sind Server-Assistenten oder Programme, die für IT-Experten vorgesehen sind, tendenziell länger und komplexer. Diese Gruppe von Ziel Benutzern hat eine viel höhere Toleranz für die Durchführung von Konfigurations Entscheidungen und kann sogar verdächtig werden, wenn zu viel Komplexität verborgen ist.

Wenn ein Assistent nach Natur eine komplexe Aufgabe vereinfacht, sollte dies relativ minimal für eine technisch ausgereifte Zielgruppe und relativ aggressiv für eine Anfänger-Benutzerbasis Vorgehen.

**Richtig:**

![Screenshot des Assistenten zum Anzeigen von Sprachen ](images/win-wizards-image7.png)

Diese Assistenten Seite ist gut für Endbenutzer konzipiert, da Sie einen potenziell komplexen Unterschied zu einer einfachen, logischen binären Auswahl reduziert: entweder installieren oder deinstallieren.

**Richtig:**

![Screenshot, der die Seite "Funktionsauswahl" des Assistenten "SQL Server Setup" anzeigt.](images/win-wizards-image8.png)

Im Setup-Assistenten für Microsoft SQL Server 2008 ist der Seiten Entwurf ausgelastet, und die zahlreichen Optionen erfordern mehr Meinung, aber die Zielgruppe ist Datenbankadministratoren, die eine strenge Kontrolle über die Funktionsauswahl erwarten.

Achten Sie schließlich darauf, wie häufig die jeweilige Aufgabe ausgeführt werden kann. Bei einer seltenen Aufgabe kann ein längerer Assistent bereitgestellt werden, während häufige Aufgaben die über-und-Zeit endgültig bevorzugen sollten.

### <a name="branching"></a>Verzweigung

Für längere Assistenten müssen Sie möglicherweise Verzweigungen des Aufgaben Flusses erstellen, in denen sich die Sequenz der Seiten abhängig von der bereitgestellten Benutzereingabe "Upstream" unterscheiden kann. Verzweigungen werden grundsätzlich von Benutzern getrennt, sodass Sie die Benutzer Darstellung entwerfen müssen, um die Stabilität zu vermitteln. Es werden nicht mehr als zwei Entscheidungspunkte empfohlen, die eine Verzweigung im gesamten Assistenten verursachen, und nicht mehr als eine geschachtelte Verzweigung innerhalb einer einzelnen Verzweigung.

Richtlinien zum Erstellen eines stabilen Benutzer Erlebnisses innerhalb eines [Verzweigungs-Assistenten finden Sie](#branching) im Abschnitt "Richtlinien" in diesem Artikel.

### <a name="providing-a-navigation-guide"></a>Bereitstellen eines Navigations Handbuchs

Navigationshandbücher können nützlich sein, wenn es viele Schritte in der Aufgabe gibt, und Benutzer können Ihre Position in der Sequenz verlieren oder einfach wissen möchten, wie viel länger Sie dauert.

Navigationshandbücher werden häufig als Liste der Seiten oder Abschnitte des Assistenten angezeigt. Sie sehen ein wenig wie ein Inhaltsverzeichnis, in einer Spalte oder in einem Bereich auf der linken Seite der einzelnen Seiten. Obwohl die Liste im Assistenten weiterhin vorhanden ist (dieselbe Liste von Seiten wird auf jeder Seite angezeigt), gibt es einige visuelle Mittel, um anzugeben, wo sich der Benutzer zurzeit in der Sequenz befindet (z. b. mit Fettdruck, um die aktive Seite oder den Abschnitt zu unterscheiden).

Navigationshandbücher können sequenziell oder nicht sequenziell sein. Der sequenzielle Typ zeigt die vergangenen Seiten zusammen mit den bekannten zukünftigen Seiten an. Sie können die Zukunft in Form von Schritten anstelle von Seiten darstellen, wenn die Schritte bekannt sind und die Seiten abhängig sind. Sie können Seiten dann dynamisch auffüllen, sobald Sie bekannt werden. Da die Navigations Sequenz korrigiert ist, ist das Navigationshandbuch nicht interaktiv.

Nicht sequenzielle navigationshandbücher sind interaktiv, sodass Benutzer die zuvor angezeigten Seiten direkt überprüfen können. Sie können auch vor der Navigations Sequenz für Seiten springen, die als optional entworfen wurden. Optionale Seiten müssen Standardwerte aufweisen, die in den meisten Fällen zulässig sind. Mit dieser Art von Leitfaden:

-   Zuvor angezeigte Seiten können immer direkt angezeigt werden.
-   Zukünftige Seiten werden möglicherweise nicht angezeigt, wenn Sie über erforderliche Komponenten verfügen.
-   Seiten, die besucht werden können, sollten sich sichtbar von denjenigen unterscheiden, die nicht möglich sind (z. b. durch die Verwendung aktiver oder deaktivierter Links), zusammen mit den erforderlichen oder optionalen Seiten.

Benutzer können in diesem Szenario mit der Bedeutung der Schaltfläche "zurück" verwechselt werden. Wenn Sie auf "zurück" klicken, werden Sie zur vorherigen Seite oder zum vorherigen Abschnitt im Navigationshandbuch geleitet, oder die letzte Seite oder der letzte Abschnitt wird angezeigt? Da Windows-Assistenten jetzt die Schaltfläche "zurück" in der linken oberen Ecke der Assistenten Seiten ablegen, und nicht in der unteren rechten Ecke mit den anderen Commit-Schaltflächen, stellen die Benutzer die Back-Funktionalität wie im Web dar. Die beste Lösung besteht also darin, Ihre Schaltfläche "zurück" für die Webnavigation anzugeben (durch Klicken auf "zurück" sollte die letzte Seite oder der letzte Abschnitt angezeigt werden), und die Navigations Anleitung des Assistenten für die sequenzielle Navigation zu verwenden.

### <a name="page-integrity"></a>Seiten Integrität

Der Assistent-Entwurf umfasst nicht nur Entscheidungen bezüglich des gesamten Aufgaben Flusses, sondern auch die Navigation und die Verzweigungs Darstellung, aber auch die, die sich auf die einzelnen Seiten beziehen, die den Assistenten bilden. **Das wichtigste Prinzip für das Entwerfen von guten Assistenten Seiten ist die Integrität: der Inhalt einer Seite sollte gleich sein.**

Assistenten Seiten können erheblich besser verwendet werden, wenn Sie konzeptionell zusammenhängen, wobei nur ein Aspekt der gesamten Aufgabe behandelt wird. Die [Haupt Anweisung](glossary.md) ist das primäre Mittel, dies zu erreichen. Identifizieren Sie das Ziel oder den Zweck der Seite für Benutzer eindeutig. [Ergänzende Anweisungen](glossary.md)und alle Steuerelemente auf der Seite beziehen sich auf die Haupt Anweisung. Obwohl den Seiten des Assistenten Benutzer mit Optionen angezeigt werden sollen, für die ein bestimmter Gedanke erforderlich ist, kann dieser Aufwand nicht wie die Arbeit aussehen, da er sich stark von der Integrität der Seite selbst unterscheidet.

Leider täuschen die Assistenten-Designer oft das schnelle klicken auf die Schaltfläche "weiter" des Benutzers als Beleg für die Benutzerfreundlichkeit, Einfachheit und Integrität Ihrer Seiten. Der ultimative Assistent ist nicht weiter als nächstes, Nächster, nächster Vorgang, Fertigstellen. Eine solche Vorgehensweise deutet darauf hin, dass die Standardwerte gut ausgewählt wurden, aber auch, dass der Assistent nicht wirklich notwendig war, da alle Optionen optional sind.

Im Hinblick auf visuelle Elemente und Text werden diese Elemente auf den Grundlagen der Grundlagen angezeigt. Halten Sie sich gegen die Möglichkeit, mehrere untergeordnete Aufgaben auf einer einzelnen Seite (dem "Burrito"-Assistenten) zu bündeln oder auf Registerkarten zur Darstellung komplexer Eingabe Anforderungen zurückzugreifen. Eine einzelne Seite sollte eine einzelne Unteraufgabe der gesamten Aufgabe des Assistenten abdecken.

**Falsch:**

![Screenshot des SQL Server-Setup-Assistenten ](images/win-wizards-image9.png)

Wenn drei Registerkarten mit einer ziemlich dichten Benutzereingabe erforderlich sind, versucht die Seite des Assistenten zu viel zu tun.

In den meisten Fällen sollten Sie die Größe jeder Seite im gesamten Assistenten behalten, um ein konsistentes Erscheinungsbild zu fördern. Obwohl Windows-Assistenten die Größe der Größe ändern können, sodass die Größe einer Seite mit der Menge an Inhalten übereinstimmt, verwenden nur einige wenige diese Option.

Behalten Sie schließlich die strukturellen Elemente der einzelnen Assistenten Seiten durch die Sequenz bei. Verschieben Sie z. b. die Schaltfläche "zurück" nicht von der linken oberen Ecke zurück in den Bereich für die Commit-Schaltflächen für eine Seite oder zwei. Diese Ebene der layoutkonsistenz hilft Benutzern, die Stabilität innerhalb des Assistenten zu erhalten. Stellen Sie sich dies als Grundlage für die visuelle Integrität einer Seite vor.

### <a name="finding-the-right-level-of-communication"></a>Ermitteln der richtigen Kommunikationsebene

Die Benutzer verfügen über eine geringe Toleranz für das Lesen großer Textblöcke auf dem Bildschirm und sogar weniger auf der Oberfläche einer Benutzeroberfläche, deren Express Zweck es ist, eine Aufgabe beschleunigt zu verschieben.

Assistenten haben eine Tendenz zur über-Kommunikation. Sie belegen viel Platz auf dem Bildschirm, was ein Laufwerk zum Auffüllen des Speicherplatzes anregen könnte. Das ist wie eine Variation des Parkinson-Gesetzes: der Benutzeroberflächen Text wird erweitert, um den verfügbaren Speicherplatz auszufüllen.

Ein unterliegt in diesem überschreiten ist Redundanz. Aufgrund von Vorlagen, die im frühen Assistenten Design verwendet werden, wird die gleiche Sprache möglicherweise an mehreren Positionen auf einer Seite angezeigt, z. b. in der Titelleiste, in Überschriften, im TextText, in Steuerelement Bezeichnungen usw.

Es lohnt sich, einen professionellen Editor zu beauftragen, um den Assistenten Text rücksichtslos zu löschen. Vermeiden Sie unnötige Fragen und Optionen auf den einzelnen Seiten, und entfernen Sie alle Seiten des Assistenten als Ganzes (z. b. die herkömmlichen Willkommens-und Begrüßungs Seiten). Gelangen Sie direkt zum Punkt der Seite mit einer kurz geschriebenen Haupt Anweisung. verwenden Sie die Sprache, die die Zielgruppe verwendet, um die Aufgabe zu beschreiben, nicht den Jargon der Technologie oder des Features, die bzw. das Sie oder Ihr teamintern verwenden. Dieser Benutzer zentrierte Ansatz ist wichtig, um die Kommunikation der Assistenten des Programms zu verbessern.

Achten Sie besonders auf den Ton Ihres Assistenten: Manchmal sind die nachhaltigsten Eindrücke Ihres Programms das Ergebnis, das Sie sagen, aber wie Sie es sagen. In den Assistenten sind die Benutzer mit einem benutzerfreundlichen, Konversations Ton vertraut, der die zweite Person ("Du") verwendet, wenn das Programmeingaben anfordert. Weitere Richtlinien finden Sie unter [Style und Tone](text-style-tone.md).

Das Reduzieren der Anzahl von Wörtern auf der Seite des Assistenten ist im allgemeinen empfehlenswert, aber seien Sie vorsichtig, wenn Sie nicht zu weit gehen. Wenn die Aufgabe wichtig ist und einen Assistenten erfordert, schätzen die Benutzer genug Informationen, um die Auswahl zu treffen. Im folgenden Beispiel wird gezeigt, wie der Text des Assistenten ohne Einbußen bei der Bedeutung komprimiert werden kann.

**Vorher:**

![Screenshot des ClearType-Assistenten, Entwurf ](images/win-wizards-image10.png)

**Nachher:**

![Screenshot des ClearType-Assistenten, überarbeitet ](images/win-wizards-image11.png)

Die bearbeitete Version dieser Assistenten Seite stellt eine aufgabenorientierte Haupt Anweisung bereit, entfernt den unnötigen Abschnitt unter der Main-Anweisung und überprüft die Kontrollkästchen Bezeichnung, um den Zweck des Kontrollkästchens zu verdeutlichen.

**Wenn Sie nur drei Dinge tun...**

1. Ordnen Sie die Aufgabe, die Sie ausführen möchten, mit der entsprechenden Benutzeroberfläche zu, um den Auftrag auszuführen. Wenn Sie glauben, dass Sie viele Eingaben von Benutzern erfassen müssen, ist es nicht einfach, auf einen Assistenten zu verzichten.

2. Überprüfen Sie sorgfältig die Länge und die Struktur des Assistenten. bevorzugen Sie kurze, nicht verzweigende Assistenten, um die Benutzeroberflächen so einfach wie möglich zu halten, damit Benutzer zu Ihrer primären Aufgabe oder zum Interesse an Ihrem Programm zurückkehren können.

3. Stellen Sie sicher, dass die Integrität jeder Seite im Assistenten besteht: der Inhalt einer Seite sollte eindeutig zueinander gehören.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Sie sollten zuerst einfache Alternativen in Erwägung gezogen werden, z. b. Dialogfelder, Aufgabenbereiche oder einzelne Seiten.** Sie müssen keine Assistenten verwenden – Sie können hilfreiche Informationen und Unterstützung in jeder beliebigen Benutzeroberfläche bereitstellen.
-   **Verwenden Sie Assistenten für Aufgaben mit mehreren Schritten.** Verwenden Sie mehrseitige Dialogfelder für Einzelschritt-Aufgaben mit Feedback. Weitere Richtlinien finden Sie unter [Dialog Felder](win-dialog-box.md).

    **Richtig:**

    ![Screenshot des Dialog Felds "Diagnose" ](images/win-wizards-image12.png)

    ![Screenshot des Dialogs mit dem Diagnose Dialogfeld ](images/win-wizards-image13.png)

    In diesem Beispiel besteht die Windows-Netzwerk Diagnose aus den Seiten für Fortschritt und Ergebnisse. Da es sich bei der Aufgabe nur um einen einzigen Schritt handelt, sind die Navigations Schaltflächen, die Benutzer in einem Assistenten benötigen, nicht erforderlich. Sie wird als mehrseitiges Dialogfeld dargestellt.

### <a name="window-size"></a>Fenstergröße

-   **Wählen Sie eine Fenstergröße, in der alle Assistenten Seiten ohne vertikalen oder horizontalen Seiten Bildlauf angezeigt werden können.** Die Steuerelemente auf der Seite erfordern möglicherweise einen Bildlauf, aber die Seiten des Assistenten dürfen nicht selbst ausgeführt werden.
-   **Die Größe von Fenstern ist groß genug, um Ihre Aufgaben komfortabel auszuführen.** Das Seitenlayout sollte nicht verkrampft sein oder einen Bildlauf oder eine Größenänderung der Benutzer erfordern.
-   **Machen Sie Windows aber nicht übermäßig groß.** Größere Fenster sorgen dafür, dass der Task komplexer ist und zusätzliche Verschiebungen für die Interaktion erforderlich ist.
-   **Verwenden Sie für einen Assistenten, der in der Größe geändert werden kann** Weisen Sie eine entsprechende Mindestgröße zu. Fenster mit Größenänderung sind hilfreich, wenn für Seiten eine Interaktion mit Inhalten mit Größenänderung erforderlich ist, wie z. b. große Listen

    **Richtig:**

    ![Screenshot von Visual Studio-Setup, partielle Liste ](images/win-wizards-image14.png)

    **Besserer**

    ![Screenshot von Visual Studio-Setup, vollständige Liste ](images/win-wizards-image15.png)

    In diesem Beispiel unterstützt die Größe des Fensters Benutzern das Anzeigen der vollständigen Liste.

-   **Verwenden Sie dynamisch Größen-Assistenten, deren Seitengröße je nach Bedarf für den Inhalt geändert wird.** Auf diese Weise kann ein Assistent Seitenlayouts mit einem breiten Spektrum an Inhalten aufnehmen.
-   **Bevorzugen Sie die statische Größenänderung gegenüber Dynamic, wenn Benutzer die Änderungen möglicherweise als fehlende Stabilität im Assistenten erkennen.** Bei der visuellen Stabilität wird die Inhalts Inhalte häufig nicht angezeigt. Die meisten Assistenten sollten eine standardmäßige, statische Fenstergröße übernehmen, bei der die dynamische Größe in besonderen Fällen reserviert ist.

### <a name="wizard-length"></a>Assistenten Länge

-   **Sorgen Sie dafür, dass der Assistent möglichst präzise und optimiert wird.** Entfernen Sie unnötige Optionen und Fragen, und verwenden Sie Smart defaults, um die Anzahl der für die Benutzereingaben erforderlichen Seiten zu verringern.
    -   **Ausnahme:** IT-Experten und andere technische Benutzer haben eine höhere Toleranz für längere Assistenten und ausführliche Eingabe Anforderungen.
-   **Legen Sie den Assistenten auf mindestens zwei Seiten.** Ein einseitiger Assistent sollte stattdessen als Dialogfeld neu gestaltet werden.
-   **Reduzieren Sie die Seitenanzahl des Assistenten nicht, indem Sie einfach die Komplexität der einzelnen Seiten erhöhen.** Eine Assistenten Seite, die drei Registerkarten mit Benutzereingaben enthält, sollte beispielsweise als drei separate Seiten umgestaltet werden.
-   **Erhöhen Sie die Seitenanzahl des Assistenten nicht, indem Sie für jede Seite so einfach sind, dass Benutzer mit der ganzen Sequenz einfach auf Weiter klicken.** Dies ist ein gängiger Entwurfs Fehler im Assistenten. Wenn eine Assistenten Seite nicht zumindest einen gewissen Grad an Gedanken erfordert, muss Sie wahrscheinlich nicht im Assistenten vorliegen.

### <a name="branching"></a>Verzweigung

-   **Bevorzugen des Entwurfs von nicht Verzweigungs-Assistenten über Verzweigungen.** Nicht verzweigende Assistenten sind tendenziell einfacher, kürzer und leicht zu navigieren. Mit Verzweigungs-Assistenten können Benutzer leichter feststellen, wie viele Schritte in der Aufgabe ausgeführt werden und wo Sie sich in der Sequenz befinden.
-   **Wenn Sie Verzweigungen müssen, helfen Sie den Benutzern, sich mit einer der folgenden Verfahren zu orientieren:**
    -   **Listet Seiten auf.** Eine gängige Methode besteht darin, den Speicherort des Benutzers in der Sequenz auf jeder Seite anzugeben, z. b. mit dem Ausdruck Schritt X von Y. Stellen Sie sicher, dass der Endpunkt (y) stabil ist. Wenn der Wert geändert wird, untergräbt dies das Vertrauen der Benutzer.
    -   **Schließen Sie das Konzept der untergeordneten Schritte** ein (z. b. Schritt 2a von 6).
    -   **Erstellen Sie Schritte unabhängig von Seiten, wobei jeder Schritt mehrere Seiten umfassen kann.** Ein Reisedienst könnte z. b. die Assistenten Organisation basierend auf bewährten e-Commerce-Konventionen für die Branche einsetzen.

        **Richtig:**

        ![Screenshot der schrittbasierten Assistenten Organisation ](images/win-wizards-image16.png)

        Logische Bezeichnungen können für Benutzer eines Verzweigungs-Assistenten eine angemessene Ausrichtung bereitstellen.

    -   **Behandeln Sie optionale Schritte als persistent in der enumerationssequenz.** Wenn z. b. eine Verzweigung nur einige optionale Schritte überspringt, überspringen Sie einfach die Schritte im Feedback, anstatt Sie neu zu Rendering. Wenn ein Benutzer auf Seite 2 eine Auswahl treffen kann, die dazu führt, dass die Seiten 3 und 4 optional sind, zeigen Sie die Schritte 1, 2, 5 und 6 von 6 an. Die Schritte 5 und 6 werden nicht umbenennt.
    -   **Wenn der Assistent einen einzelnen Branch verwendet und die Verzweigung frühzeitig in der Aufgabe auftritt, starten Sie die Sequenz an diesem Punkt, und verwenden Sie dann einfach den nicht Verzweigungs Ansatz.** Das heißt, dass beginnend an der Stelle der Verzweigung der Fortschritt in der Sequenz bis zum Ende der Verzweigung erfolgt.

-   **Wenn Sie Verzweigungen müssen, begrenzen Sie die Anzahl der Verzweigungen in einem einzelnen Assistenten auf einen oder zwei.** Fügen Sie niemals mehr als eine Verzweigung in eine Verzweigung ein (eine "geschachtelte" Verzweigung).

### <a name="commit-buttons"></a>Commit-Schaltflächen

-   **Wenn Benutzer ein Commit für eine Aufgabe ausführen, verwenden Sie eine Commit-Schaltfläche, die eine bestimmte Antwort auf die Haupt Anweisung ist** (z. b. Print, Connect oder Start). Verwenden Sie keine generischen Bezeichnungen wie Next (was keine Verpflichtung impliziert) oder Fertigstellen (was nicht spezifisch ist) zum Ausführen eines Commits für eine Aufgabe. Die Bezeichnungen auf diesen Commit-Schaltflächen sollten selbst sinnvoll sein. Startet immer Commit-Schaltflächen Bezeichnungen mit einem Verb. **Ausnahmen:**
    -   Verwenden Sie Fertigstellen, wenn die spezifischen Antworten weiterhin generisch sind, z. b. speichern, auswählen, auswählen oder Get.
    -   Verwenden Sie "Fertigstellen", um eine bestimmte Einstellung oder eine Sammlung von Einstellungen zu ändern.
-   **Ein einzelner Assistent kann mehrere Commit-Punkte enthalten, es wird jedoch ein einzelner Punkt bevorzugt.**
-   **Bei Bedarf können Sie die Commit-Schaltflächen auf einer Seite umbenennen oder ausblenden.** Diese Flexibilität ist ein Vorteil des neuen Assistenten Design in Windows, das in älteren Assistenten nicht verfügbar war. Beachten Sie, dass das Ausblenden einer Commit-Schaltfläche von der Deaktivierung abweicht.
-   **Vermeiden Sie die Deaktivierung einer positiven Commit-Schaltfläche.** Andernfalls müssen Benutzer ableiten, warum die Commit-Schaltflächen deaktiviert werden. Es ist besser, die Commit-Schaltflächen aktiviert zu lassen und eine hilfreiche Fehlermeldung zu erhalten, wenn ein Problem auftritt. Das Deaktivieren der Schaltfläche ist nur akzeptabel, wenn der Grund dafür offensichtlich und eindeutig ist.
-   **Verwechseln Sie Navigations Schaltflächen ("weiter" und "zurück") nicht mit Commit** Das nächste bedeutet, dass der Assistent ohne Verpflichtung fortgeführt werden soll. "Zurück" sollte auf der nächsten Seite immer verfügbar sein. Wenn Sie auf "zurück" klicken, sollte die Auswirkung der letzten Schaltfläche rückgängig gemacht werden. Wenn dies nicht möglich ist, nehmen die Benutzer eine Verpflichtung auf, und dies wird über eine bestimmte Bezeichnung auf der Schaltfläche "Commit" angegeben. Weitere Richtlinien zu den Schaltflächen "weiter" und "zurück" finden Sie unter [Navigation](#providing-a-navigation-guide).

### <a name="cancel-buttons"></a>Schaltflächen Abbrechen

-   **Bitten Sie die Benutzer nicht, zu bestätigen, ob Sie wirklich abbrechen möchten.** Dies kann ärgerlich sein. **Ausnahmen:**
    -   Die Aktion hat bedeutende Konsequenzen und ist, falls falsch, nicht sofort fixierbar.
    -   Die Aktion kann zu einem erheblichen Verlust der Zeit oder des Aufwands des Benutzers führen.
    -   Die Aktion ist mit anderen Aktionen eindeutig inkonsistent.
-   **Ermöglicht Benutzern das Neustarten von Assistenten für den Fall, dass Sie versehentlich abgebrochen wurden.**
-   **Deaktivieren Sie die Schaltfläche Abbrechen nicht. Ausnahmen**
    -   Wenn das Abbrechen schädlich ist, kann dies der Fall sein, wenn eine Aufgabe in eigenständigen Assistenten ausgeführt wird.
    -   Wenn das Abbrechen nicht möglich ist, kann dies der Fall sein, wenn der Assistent keine Kontrolle über alle Schritte hat.

### <a name="close-buttons"></a>Schließen von Schaltflächen

-   **Verwenden Sie Close für Follow-Up-und Abschluss Seiten.** Verwenden Sie Cancel nicht, da das Schließen des Fensters Änderungen oder Aktionen, die zu diesem Zeitpunkt durchgeführt wurden, nicht verwerfen kann. Verwenden Sie done nicht, da es sich nicht um ein Imperatives Verb handelt.
-   **Nachdem die Aufgabe ausgeführt wurde, sollte Abbrechen (für eigenständige Assistenten) geschlossen werden.** Die Auswirkung von Close besteht lediglich darin, das Fenster zu schließen.

### <a name="other-controls"></a>Weitere Steuermöglichkeiten

-   **Verwenden Sie Befehls Verknüpfungen nur für Auswahlmöglichkeiten, keine Verpflichtungen.** Bestimmte Commit-Schaltflächen weisen auf eine wesentlich bessere Verpflichtung als Befehls Verknüpfungen in einem Assistenten hin.
-   **Wenn Sie Befehls Verknüpfungen verwenden, blenden Sie die Schaltfläche weiter aus, aber lassen Sie die Schaltfläche Abbrechen.**

### <a name="using-pages-vs-dialog-boxes-or-inline-ui"></a>Verwenden von Seiten (im Vergleich zu Dialogfeldern oder der Inline Benutzeroberfläche)

-   **Im allgemeinen bevorzugen Sie Seiten für Dialogfelder.** Benutzer erwarten, dass Assistenten Seiten basiert sind.
-   **Verwenden Sie Dialogfelder, um das Abschließen von Seiten zu unterstützen,** z. b. mit objektpickern und Browsern
-   **Verwenden Sie Dialogfelder, um Fehlermeldungen anzugeben, die auf die gesamte Seite angewendet werden, und führen Sie das Klicken auf die Schaltfläche Commit aus.**
-   **Verwenden Sie die Inline Präsentation für einfaches dynamisches Verhalten,** z. b. Progressive Offenlegung und kontextbezogene Benutzeroberfläche.
-   **Verwenden Sie die Inline Präsentation für Fehlermeldungen, die für bestimmte Steuerelemente gelten.**

### <a name="wizard-pages"></a>Seiten des Assistenten

-   **Konzentrieren Sie sich auf die effiziente Entscheidungsfindung.** Reduzieren Sie die Anzahl der Seiten, um sich auf Essentials zu konzentrieren. Konsolidieren Sie verwandte Seiten, und verwenden Sie optionale Seiten aus dem Hauptflow. Wenn Benutzer die vollständige Durchführung des Assistenten auf Weiter klicken, erscheint Ihnen möglicherweise zunächst ein guter Eindruck, aber wenn Benutzer die Standardeinstellungen nicht ändern müssen, sind die Seiten wahrscheinlich unnötig.
-   **Entwerfen Sie jede Seite so, dass Sie nur einen Zweck und eine visuelle Konsistenz hat.** Weitere Informationen finden Sie unter [Seiten Integrität](#page-integrity).
-   **Verwenden Sie keine Willkommens Seiten – erstellen Sie die erste Seite immer, wenn dies möglich ist.** Verwenden Sie nur dann eine optionale Seite mit den ersten Schritten, wenn:

    -   Der Assistent verfügt über erforderliche Komponenten, die erforderlich sind, um den Assistenten erfolgreich abzuschließen.
    -   Benutzer können den Zweck des Assistenten aufgrund der ersten Auswahl Seite nicht verstehen, und es gibt keinen Platz für weitere Erläuterungen.
    -   Die Haupt Anweisung für die Seite "erste Schritte" lautet "Vorbereitung:".

    **Falsch:**

    ![Screenshot der Willkommensseite für das MapPoint-Setup ](images/win-wizards-image17.png)

-   Moderne Assistenten entscheiden sich für funktionale erste Seiten. Hier ist nichts zu tun, aber klicken Sie auf Weiter. Warum müssen Benutzer diese tokensteuern für Ihre wertvolle Zeit bezahlen?
-   **Auf Seiten, bei denen Benutzer aufgefordert werden, Entscheidungen zu treffen, optimieren Sie in den wahrscheinlichsten Fällen.** Diese Seiten Typen sollten tatsächliche Optionen, nicht nur Anweisungen, darstellen.
    -   Wenn Sie keine Seite "erste Schritte" verwenden, erläutern Sie den Zweck des Assistenten am Anfang der ersten Seite der Auswahl.
-   **Verwenden Sie Commit Pages, um den Benutzer zu bestätigen, wenn Benutzer einen Commit für die Aufgabe ausführen.** In der Regel ist die commitseite die letzte Seite der Auswahl, und die Schaltfläche Weiter wird neu klassifiziert, um die Aufgabe anzugeben, für die ein Commit ausgeführt wird.
    -   Verwenden Sie keine Zusammenfassungs Seiten, die nur die vorherige Auswahl des Benutzers zusammenfassen, es sei denn, die Aufgabe ist riskant (bei der Sicherheit oder dem Verlust der Zeit oder des Geldes), oder es besteht eine gute Wahrscheinlichkeit, dass Benutzer Ihre Auswahl überprüfen müssen.
-   **Verwenden Sie Statusseiten, um den Status eines langwierigen Vorgangs anzuzeigen.** Nach erfolgreichem Abschluss sollte die Statusseite automatisch mit dem nächsten Schritt fortfahren. Sie sollte auf der Seite "Status" nur dann bleiben, wenn ein Problem vorliegt, das der Benutzer sehen muss. Das Klicken auf eine Statusseite sollte keinen Nebeneffekt haben.
    -   **Verwenden Sie eine einzelne, bestimmte Statusanzeige.** Befolgen Sie die [Richtlinien für die bestimmte der Statusleiste](progress-bars.md), einschließlich:
        -   Geben Sie den Abschluss eindeutig an. Lassen Sie eine Statusanzeige nicht zu 100 Prozent wechseln, es sei denn, der Vorgang wurde abgeschlossen.
        -   Starten Sie den Fortschritt nicht. Eine Statusanzeige verliert ihren Wert, wenn Sie neu gestartet wird (möglicherweise weil ein Schritt im Vorgang abgeschlossen ist), da Benutzer nicht wissen, wann der Vorgang abgeschlossen wird. Nehmen Sie stattdessen an, dass alle Schritte des Vorgangs einen Teil des Fortschritts aufweisen und die Statusanzeige einmal abgeschlossen werden soll.
    -   **Geben Sie eine kurze Beschreibung des aktuellen Schritts oberhalb der Statusanzeige an.** Bei schnellen Vorgängen ist dieser Text unnötig. die Statusanzeige ist ausreichend. Bei Vorgängen, die eine Minute oder länger erfordern, kann Text hilfreich sein.
        -   Verwenden Sie Satzfragmente, die in der Regel mit einem Verb beginnen und mit einem Auslassungs Zeichen enden. Beispiele: Dateien werden kopiert..., erforderliche Komponenten werden installiert...
        -   Platzieren Sie Text oberhalb der Leiste, nicht weiter unten.
        -   **Falsch:**
        -   ![Screenshot der Statusanzeige mit folgendem Text ](images/win-wizards-image18.png)
        -   In diesem Beispiel sollte der erläuternde Text oberhalb der Statusanzeige angezeigt werden.
        -   Verzichten Sie darauf, die Statusseite mit unnötigen Details zu gruppieren. Diese Seite ist kein technischer Support. Das ist für Benutzer.
        -   **Falsch:**
        -   ![Screenshot der Statusanzeige mit zu vielen Details ](images/win-wizards-image19.png)
        -   In diesem Beispiel sind technische Details wie GUIDs für Benutzer bedeutungslos.
-   **Verwenden Sie keine Herzlichen Glückwunsch Seiten, die nichts tun, sondern den Assistenten beenden.** Wenn den Benutzern die Ergebnisse offensichtlich offensichtlich sind, schließen Sie einfach den Assistenten auf der Schaltfläche letztes Commit.
    -   Verwenden Sie Follow-Up Seiten, wenn Verwandte Aufgaben vorhanden sind, die Benutzer wahrscheinlich als Nachverfolgung ausführen. Vermeiden Sie vertraute nach Verfolgungs Aufgaben, wie z. b. "Senden einer e-Mail-Nachricht".
    -   Verwenden Sie Vervollständigungs Seiten nur dann, wenn die Ergebnisse nicht angezeigt werden und keine bessere Möglichkeit zum Bereitstellen von Feedback für den Abschluss der Aufgabe vorliegt.
    -   Assistenten, die Statusseiten haben, müssen eine Vervollständigungs Seite oder Follow-Up Seite verwenden, um den Abschluss der Aufgabe anzuzeigen. Schließen Sie für Aufgaben mit langer Ausführungszeit den Assistenten auf der Seite Commit, und verwenden Sie Benachrichtigungen, um Feedback zu geben.
-   **Verwenden Sie Zusammenfassungs Seiten nur dann, wenn die Eingabe Komplex ist und die Benutzer überprüfen müssen, wenn der Task ein erhebliches Risiko (z. b. einen Finanz Übergang) umfasst oder wenn der Assistent auf der Grundlage von Benutzereingaben, die nicht offensichtlich sind, Aktionen durchführt** Häufig werden die Zusammenfassungs Seiten nicht dieser relevanzleiste entsprechen und können ausgelassen werden.
-   **Verwenden Sie Fehlerseiten, wenn der Assistent aufgrund eines Problems, von dem die Wiederherstellung nicht möglich ist, nicht abgeschlossen werden kann.** Erläutern Sie auf dieser Seite, worum es sich bei dem Problem um eine klare Sprache handelt, und zwar ohne technischen Fachjargon. Stellen Sie außerdem praktische Schritte bereit, mit denen Benutzer das Problem lösen können. Weitere Richtlinien finden Sie unter [Fehlermeldungen](mess-error.md).
    -   **Ausnahme:** Wenn der Assistent mit einem geringfügigen Problem abgeschlossen ist, von dem eine Wiederherstellung möglich ist, stellen Sie das Problem als zusätzliche Aufgabe dar, anstatt einen Fehler zu beheben. Verwenden Sie positive, erfolgsorientierte, ermutigende Sprache, keine Begriffe wie Fehler, Fehler oder Problem. Verwenden Sie kein Fehler Symbol.

### <a name="navigation"></a>Navigation

-   **Verwenden Sie Next nur, wenn Sie ohne Verpflichtung zur nächsten Seite übergehen.** Der Fortschritt der nächsten Seite wird als Verpflichtung betrachtet, wenn der Effekt nicht rückgängig gemacht werden kann, indem Sie auf zurück oder Abbrechen klicken.
-   **Verwenden Sie zurück, um Fehler zu beheben.** Abgesehen von der Behebung von Fehlern dürfen Benutzer nicht auf "zurück" klicken, um den Fortschritt in einer Aufgabe fortzusetzen.
-   **Beibehalten der Benutzer Auswahl durch Navigation.** Wenn der Benutzer z. b. Änderungen vornimmt, auf zurück und dann auf Weiter klickt, sollten diese Änderungen beibehalten werden. Benutzer erwarten nicht, dass die Änderungen erneut eingegeben werden müssen, es sei denn, Sie haben explizit entschieden, Sie zu löschen.
-   **Deaktivieren Sie die Schaltfläche zurück, es sei denn, die Schritte sind schädlich.**
-   **Ermöglicht Benutzern das Durchsuchen oder Überprüfen von Optionen in den folgenden Navigations Szenarien:**
    -   Der Benutzer gibt Eingaben aus, klickt auf die Schaltfläche "Commit" und klickt auf "zurück", um die vorherigen Änderungen zu überprüfen Normalerweise sollte dies möglich sein, und der zweite Commit sollte nur zur nächsten Seite wechseln (weil die Aufgabe bereits abgeschlossen wurde).
    -   Der Benutzer gibt Eingaben aus, klickt auf die Schaltfläche "Commit" und klickt auf "zurück", um die vorherigen Änderungen zu überprüfen Normalerweise sollte dies möglich sein, und der zweite Commit sollte die Aufgabe mit der geänderten Eingabe wiederholen (durch ersetzen oder rückgängig machen der Auswirkungen der ersten).

### <a name="help"></a>Hilfe

-   **Die Seiten des Entwurfs-Assistenten, um genügend Informationen bereitzustellen, sodass das verweisen auf die Dokumentation in Programm Hilfe unnötig ist.** Ein Assistent entfernt Benutzer bereits von der gewünschten direkten Interaktion mit dem Programm. Wenn Sie möchten, dass die Benutzer externe Hilfe benötigen, entfernen Sie Sie noch weiter aus diesem Zustand. Hilfe sollte die Ausnahme sein, nicht die Regel.
-   **Wenn Sie einen Zugriffspunkt zur Unterstützung von angeben müssen, verwenden Sie einen Link im unteren linken Bereich des Inhalts Bereichs der Seite (oberhalb des Befehls Bereichs).** Dieser Link sollte kurz sein und in der Regel in der Form einer Frage formuliert sein, dass die Benutzer höchstwahrscheinlich antworten möchten.
-   **Richtig:**
-   ![Screenshot der Assistenten Seite mit Hilfe Verknüpfung ](images/win-wizards-image5.png)
-   Dieser Link zur Hilfe ist geeignet, da grundlegende Hintergrundinformationen wie diese die Seite des Assistenten zu stark überladen würden.

## <a name="text"></a>Text

### <a name="general"></a>Allgemein

-   Verwenden Sie und ihren, um auf den Benutzer und den Computer, das Dokument, die Einstellungen usw. des Benutzers zu verweisen. Verwenden Sie nicht die erste Person (I, my), um auf den Computer oder den Assistenten zu verweisen. Es ist jedoch akzeptabel, dass Sie die erste Person in Optionen verwenden, die der Benutzer auswählt. **Beispiel:** das Kontrollkästchen nur verwenden.
-   Jede Assistenten Seite muss über eine [Haupt Anweisung](glossary.md)verfügen.

### <a name="titles"></a>Titel

-   Legen Sie den Namen des Assistenten in der Titelleiste ab. Verwenden Sie die groß [-](glossary.md)/Kleinschreibung.
-   Titel sollten keine Interpunktions Zeichen enthalten, mit Ausnahme derjenigen mit Fragezeichen.
-   Schließen Sie den Word-Assistenten nicht in die Titel des Assistenten ein. Verwenden Sie beispielsweise Verbindung mit einem Netzwerk statt mit dem Netzwerksetup-Assistenten.

### <a name="buttons"></a>Schaltflächen

-   Fügen Sie Text nicht auf die Schaltfläche zurück ein. Verwenden Sie stattdessen das Pfeilsymbol ohne Bezeichnung.
-   Fügen Sie Text auf der Schaltfläche weiter ein. Verwenden Sie neben dem Wort "Next" keine Symbole (z. b. > oder >>).
-   Verwenden Sie spezifische Commit-Schaltflächen Bezeichnungen, die selbst sinnvoll sind und eine Antwort auf die Haupt Anweisung sind. Im Idealfall sollten Benutzer nichts anderes lesen müssen, um die Bezeichnung zu verstehen. Benutzer sind viel wahrscheinlicher, dass Befehlszeilen Bezeichnungen als statischer Text gelesen werden.
-   Verwenden Sie nach Möglichkeit nicht die Wort Fertigstellung für die Schaltflächen Bezeichnung "Commit", da normalerweise eine bessere, spezifischere Commit-Schaltfläche vorliegt:
    -   Wenn Sie auf die Schaltfläche zum Ausführen eines Commits für die Aufgabe klicken (sodass die Aufgabe noch nicht ausgeführt wurde), verwenden Sie eine bestimmte Bezeichnung, die mit einem Verb beginnt, das eine Antwort auf die main-Anweisung ist (Beispiele: Print, Connect, Start).
    -   Wenn die Aufgabe bereits im Assistenten ausgeführt wurde, verwenden Sie stattdessen close.

        **Ausnahmen:**

        -   Sie können Fertigstellen verwenden, wenn die jeweilige Bezeichnung noch generisch ist, z. b. speichern, auswählen, auswählen oder Get.
        -   Sie können Fertigstellen verwenden, wenn die Aufgabe das Ändern einer Einstellung oder einer Sammlung von Einstellungen einschließt.

-   Starten Sie Commit-Schaltflächen Bezeichnungen mit einem Verb. Ausnahmen sind "OK", "yes" und "No".
-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.
-   Verwenden Sie keine Interpunktion am Ende.

## <a name="documentation"></a>Dokumentation

-   Obwohl die meisten Windows-Assistenten den Word-Assistenten im Titel nicht mehr haben, ist es akzeptabel, als Assistenten in der-Dokumentation auf Assistenten zu verweisen. Diese Referenz sollte in Kleinbuchstaben angegeben werden.
-   **Richtig:**
-   Wenn Sie ein Netzwerk zum ersten Mal einrichten, können Sie mithilfe des Assistenten **zum Herstellen einer Verbindung mit einem Netzwerk** Hilfe erhalten.
-   Einige ältere Assistenten aus früheren Versionen von Windows können den Assistenten im Titel enthalten. Wenn Sie auf einen dieser Assistenten verweisen, ist es akzeptabel, den \[ x- \] Assistenten zu verwenden, um den Assistenten zu vermeiden \[ \] .
-   Verweisen Sie auf einen einzelnen Bildschirm innerhalb eines Assistenten als Seite.

 

 