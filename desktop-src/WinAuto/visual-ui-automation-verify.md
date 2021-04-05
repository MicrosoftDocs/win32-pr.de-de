---
title: Überprüfen der Visual UI-Automatisierung
description: Visual UI Automation Verify (Visual UIA Verify) ist ein Windows \ 32; GUI-Treiber für die UIA-Test Bibliothek, die für Manuelles Testen der Benutzeroberflächen Automatisierung konzipiert ist.
ms.assetid: 8AEB083E-785E-4F15-B708-2098A9A41B4E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e224a52d243427af86c6cd27a3add3be03d9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713770"
---
# <a name="visual-ui-automation-verify"></a>Überprüfen der Visual UI-Automatisierung

Visual UI Automation Verify (Visual UIA Verify) ist ein Windows GUI-Treiber für die UIA-Test Bibliothek, die für manuelle Tests der Benutzeroberflächen Automatisierung konzipiert ist. Es stellt eine Schnittstelle für die Funktionalität der UIA-Test Bibliothek bereit, mit der der Codierungsaufwand eines Befehlszeilen Tools entfällt.

-   [Menübefehle](#menu-commands)
-   [Funktionale Bereiche](#functional-panes)
    -   [Bereich "Automatisierungselemente-Struktur"](#automation-elements-tree-pane)
    -   [Bereich "Tests"](#tests-pane)
    -   [Bereich „Testergebnisse“](#test-results-pane)
    -   [Eigenschaften Bereich](#properties-pane)

Visual UIA Verify unterstützt nur die systemeigene UIA-Überprüfung-XML-Protokollierung (WUIALoggerXml.dll). Benutzer auswählbare XML-Transformationen sind in Visual UIA-Überprüfung integriert, um verschiedene Ansichten des XML-Protokollierungs Berichts im **Testergebnisse** Bereich darzustellen.

Standardmäßig lädt Visual UIA Verify den Client seitigen Benutzeroberflächenautomatisierungs-Anbieter, der mit der ursprünglichen Version der Benutzeroberflächen Automatisierung ausgeliefert wurde. Sie können auswählen, dass dieser Anbieter nicht geladen werden soll, indem Sie **/NOCLIENTSIDEPROVIDER** in der Befehlszeilenoption von VisualUIVerifyNative.exe hinzufügen.

Der folgende Screenshot zeigt die Haupt Funktionsbereiche der Benutzeroberfläche der Visual UIA-Überprüfung.

![Haupt Funktionsbereiche der Benutzeroberfläche der Visual UIA-Überprüfung](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a>Menübefehle

In der folgenden Tabelle werden die Befehle im Menü der Visual UIA-Überprüfung beschrieben.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Menü</th>
<th>Get-Help</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>File</strong></td>
<td><strong>Beenden</strong></td>
<td>Beenden Sie Visual UIA Verify.</td>
</tr>
<tr class="even">
<td><strong>Ansicht</strong></td>
<td><strong>Hervorhebung</strong></td>
<td>Markieren Sie das umgebende Rechteck des ausgewählten Elements im Strukturbereich <strong>Automation-Elemente</strong> . Die folgenden Optionen sind verfügbar.
<ul>
<li><strong>Rechteck</strong>– eine solide rote Linie.</li>
<li><strong>Ausblenden des Rechtecks</strong>– eine rote Linie, die nach einigen Sekunden verschwindet.</li>
<li><strong>Rays und Rechteck</strong>– eine durchgezogen rote Linie mit zusätzlichen blauen Hervorhebungs Linien, die aus jeder Ecke des umgebenden Rechtecks heraus Strahlen.</li>
<li><strong>None</strong>– keine sichtbare Hervorhebung.</li>
</ul></td>
</tr>
<tr class="odd">
<td rowspan="2"><strong>Automation-Element</strong>Struktur $ {Remove} $<br />
</td>
<td><strong>Ausgewähltes Element aktualisieren</strong></td>
<td>Aktualisieren Sie die untergeordneten Elemente des ausgewählten Elements im Strukturbereich <strong>Automation-Elemente</strong> . Die Liste der Elemente ist statisch und wird nicht dynamisch (automatisch) aktualisiert, wenn sich die Elementstruktur ändert.</td>
</tr>
<tr class="even">
<td><strong>Navigation</strong></td>
<td>Navigieren Sie durch die Elementstruktur Hierarchie zu einem der folgenden Elemente.
<ul>
<li>Über <strong>geordnetes</strong>Element – gehe zu übergeordnetem Element.</li>
<li><strong>First Child</strong>– gehe zum ersten untergeordneten Element.</li>
<li><strong>Nächstes</strong>gleich geordnetes Element – gehe zum ersten neben geordneten Element.</li>
<li><strong>Vorheriges</strong>gleich geordnetes Element – gehe zum vorangehenden neben geordneten Element.</li>
<li><strong>Last Child</strong>– gehe zum letzten untergeordneten Element.</li>
</ul></td>

</tr>
<tr class="odd">
<td rowspan="3"><strong>Modus</strong>$ {Remove} $<br />
</td>
<td><strong>Always on oben</strong></td>
<td>Das Fenster "Visual UIA verify" bleibt am Anfang der z-Reihenfolge des Desktops.</td>
</tr>
<tr class="even">
<td><strong>Hover-Modus (STRG verwenden)</strong></td>
<td>Wenn die STRG-Taste gedrückt wird, wird das-Element unter dem Maus Cursor als interessantes Element identifiziert. Der Bereich <strong>Automatisierungs Element</strong> Struktur wird aktualisiert, und das entsprechende Element in der Elementliste wird hervorgehoben.</td>

</tr>
<tr class="odd">
<td><strong>Fokusverfolgung</strong></td>
<td>Wenn sich der Fokus ändert, wird das Element mit dem Fokus als interessantes Element identifiziert. Der Bereich <strong>Automatisierungs Element</strong> Struktur wird aktualisiert, und das entsprechende Element in der Elementliste wird hervorgehoben.</td>

</tr>
<tr class="even">
<td rowspan="6"><strong>Tests</strong>$ {Remove} $<br />
</td>
<td><strong>Nach links</strong></td>
<td>Verschieben Sie einen Knoten nach links in der <strong>Test</strong> Struktur.</td>
</tr>
<tr class="odd">
<td><strong>Nach oben</strong></td>
<td>Verschieben Sie einen Knoten in der <strong>Test</strong> Struktur nach oben.</td>

</tr>
<tr class="even">
<td><strong>Nach unten</strong></td>
<td>Verschieben Sie einen Knoten in der <strong>Test</strong> Struktur nach unten.</td>

</tr>
<tr class="odd">
<td><strong>Nach rechts</strong></td>
<td>Verschieben Sie einen Knoten nach rechts in der <strong>Test</strong> Struktur.</td>

</tr>
<tr class="even">
<td><strong>Ausgewählte (r) Test (e) auf ausgewähltem Element ausführen</strong></td>
<td>Führt die ausgewählten Tests aus der <strong>Test</strong> Struktur für das ausgewählte Element aus.</td>

</tr>
<tr class="odd">
<td><strong>Bekannte Probleme Filtern</strong></td>
<td>Filtern bekannter Benutzeroberflächenautomatisierungs-Fehler aus den Testergebnissen.</td>

</tr>
<tr class="even">
<td><strong>Hilfe</strong></td>
<td><strong>Informationen zur Überprüfung der Benutzeroberflächen Automatisierung</strong></td>
<td>Zeigen Sie die Softwareversion und die Copyright Informationen für Visual UIA-Überprüfung an.</td>
</tr>
</tbody>
</table>



 

## <a name="functional-panes"></a>Funktionale Bereiche

In diesem Abschnitt werden die Funktionsbereiche in der Benutzeroberfläche der Visual UIA-Überprüfung beschrieben.

-   [Bereich "Automatisierungselemente-Struktur"](#automation-elements-tree-pane)
-   [Bereich "Tests"](#tests-pane)
-   [Bereich „Testergebnisse“](#test-results-pane)
-   [Eigenschaften Bereich](#properties-pane)

### <a name="automation-elements-tree-pane"></a>Bereich "Automatisierungselemente-Struktur"

Der Bereich **Automatisierungselemente** -Struktur enthält eine hierarchische Momentaufnahme von Automation-Element Objekten, die für Tests verfügbar sind. Das oberste Element in der Struktur stellt den Desktop dar.

Diese Sicht ist eine statische Auflistung, die kompiliert wird, wenn die Überprüfung der visuellen benutzerdefinierte Funktion gestartet wird. Zum Aktualisieren der Ansicht auf dem ausgewählten Knoten verwenden Sie den Menübefehl " **ausgewähltes Element aktualisieren** " oder die Symbolleisten Schaltfläche.

Der folgende Screenshot zeigt den Strukturbereich **Automation-Elemente** .

![Bereich "Automatisierungselemente" der visuellen UIA-Überprüfung](images/automation-elements-tree-pane.png)

Ein abgeblichter (nicht verfügbarer) Knoten in der **Automatisierungs Element** Struktur zeigt an, dass das Element ein Member der Benutzeroberflächenautomatisierungs-rohansicht ist, aber nicht den Bedingungen entspricht, die als Member der Inhaltsansicht oder Steuerelement Ansicht erforderlich sind. Das-Element kann jedoch weiterhin über die Visual UI-Automatisierungs Überprüfung getestet werden. Weitere Informationen finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).

Folgende Befehle sind in der Struktur Symbolleiste der **Automatisierungselemente** verfügbar:

-   **Aktualisieren**– den ausgewählten Knoten und seine untergeordneten Elemente aktualisieren. Dieser Befehl aktualisiert nicht die gesamte Elementstruktur, es sei denn, der Stamm Knoten ist ausgewählt.
-   **Parent (STRG + UMSCHALT + F6)**– wechselt zum übergeordneten Element des aktuellen Knotens.
-   **First Child (STRG + UMSCHALT + F7)**– wechselt zum ersten untergeordneten Element des aktuellen Knotens.
-   **Nächstes neben geordnetes Element (STRG + UMSCHALT + F8)**– wechselt zum nächsten neben geordneten Element des aktuellen Knotens.
-   **Vorheriges gleich geordnetes Element (STRG + UMSCHALT + F9)**– wechselt zum vorherigen gleich geordneten Element des aktuellen Knotens.
-   **Last Child (STRG + UMSCHALT + F10)**– wechselt zum letzten untergeordneten Element des aktuellen Knotens.
-   **Fokusverfolgung**– aktivieren oder deaktivieren Sie die Knoten Auswahl basierend auf der Fokusverfolgung.

### <a name="tests-pane"></a>Bereich "Tests"

Der Bereich **Tests** enthält eine Liste von Tests der Benutzeroberflächen Automatisierung, geordnet nach Testtyp (**Automatisierungs Element**, **Steuer** Element und **Muster**) und Priorität (**Buildüberprüfung**, **Priorität 0**, **Priorität 1**, **Priorität 2** und **Priorität 3**). Diese Liste wird basierend auf dem Steuer Elementtyp des ausgewählten Elements im Strukturbereich **Automation-Elemente** generiert. Weitere Informationen finden Sie unter [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

Der folgende Screenshot zeigt den Bereich **Tests** .

![Testbereich](images/test-pane.png)

Folgende Befehle sind auf der Symbolleiste " **Tests** " verfügbar:

-   Show – gibt die **anzuzeigenden** Benutzeroberflächenautomatisierungs-Tests an; Das heißt, alle Tests oder nur Tests, die für den Steuer Elementtyp des ausgewählten Elements in der Struktur der **Automatisierungselemente** geeignet sind (Standard).
-   Type – gibt die **anzuzeigenden** Testtypen an: **Automation-Element**,- **Muster** oder- **Steuer** Element.
-   **Prioritäten**– gibt die anzuzeigenden Test Prioritäten an: **Buildüberprüfung**, **Priorität 0**, **Priorität 1**, **Priorität 2** oder **Priorität 3**.
-   **Gehe zu Links**– wechselt zum übergeordneten Knoten des aktuellen Knotens.
-   Nach **oben**– wechselt zum vorherigen gleich geordneten Element des aktuellen Knotens.
-   Nach **unten**– gehe zum nächsten neben geordneten Element des aktuellen Knotens.
-   **Go Right**– wechselt zum ersten untergeordneten Element des aktuellen Knotens.
-   **Ausgewählte Test (e) ausführen**– führt die Tests für das in der Struktur der **Automatisierungselemente** ausgewählte Element aus.

### <a name="test-results-pane"></a>Bereich „Testergebnisse“

Der Bereich **Testergebnisse** enthält die Funktion zur Überprüfung der Visual UIA-Protokollierung. Der folgende Screenshot zeigt den **Testergebnisse** Bereich.

![Bereich "Testergebnisse"](images/test-results-pane.png)

Folgende Befehle sind in der **Testergebnis** Symbolleiste verfügbar:

-   **Zurück**– Seiten rückwärts in Berichts Anzeige Verlauf.
-   **Forward**– Seiten vorwärts im Berichts Anzeige Verlauf.
-   **Insgesamt**– zeigt eine Zusammenfassung der Testergebnisse an(bestanden **,** Fehler und **unerwarteter Fehler**). Das Testergebnis ist mit der Ansicht **alle Ergebnisse** verknüpft. Der Befehl " **Gesamt** " zeigt eine Tabelle wie die folgende an.

    ![Tabelle für allgemeine Testergebnisse](images/overall-test-results.png)

-   **Alle Ergebnisse**– zeigt ein detailliertes Protokoll für jedes Testergebnis an, wie in den folgenden Tabellen dargestellt.

    ![Beispiel für Protokoll Ergebnis Details aus der Ansicht "alle Ergebnisse"](images/all-results-log.png)

    Der Testname in der Tabelle **alle Ergebnisse** wird mit einer Test Fallbeschreibung für das-Element verknüpft, wie in der folgenden Tabelle.

    ![Test Fall Details](images/test-case-detail.png)

-   **Full Log**– zeigt eine Alternative Ansicht des detaillierten Protokolls für jedes Testergebnis an, wie im folgenden Screenshot gezeigt.

    ![Alternative Ansicht eines Test Fall Details](images/alt-view-of-test-case-detail.png)

-   **XML**– zeigt das von der XML-Protokollierung generierte unformatierte XML an.
-   **Schnell** Suche – einfache Text Suche der aktuellen Ansicht im **Testergebnisse** Bereich.
-   **In neuem Fenster öffnen**– öffnet die aktuelle Ansicht in einer neuen Instanz von Internet Explorer.

### <a name="properties-pane"></a>Eigenschaftenbereich

Der **Eigenschaften** Bereich enthält eine Liste der Benutzeroberflächenautomatisierungs-Eigenschaften und Eigenschaftswerte, geordnet nach Eigenschaftentyp: **Allgemeine Barrierefreiheit**, **Identifikation**, **Muster** (Steuerelement Muster), **Status** und **Sichtbarkeit**. Die Eigenschaftswerte werden basierend auf dem Steuerelement des im Strukturbereich **Automation-Elemente** ausgewählten Objekts dynamisch aufgefüllt. Der folgende Screenshot zeigt den Bereich **Eigenschaften** .

![Eigenschaften Bereich](images/properties-pane.png)

Wenn das ausgewählte Steuerelement ein bestimmtes Steuerelement Muster unterstützt, bietet Visual UIA Verify die Möglichkeit, Methoden aufzurufen, die von diesem Steuerelement Muster unterstützt werden. Beispielsweise unterstützt der [Fenster Steuer](uiauto-supportwindowcontroltype.md) Element-Typ das [Window-Steuerelement Muster](uiauto-implementingwindow.md), das über eine [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) -Methode verfügt, die im Bereich **Eigenschaften** aufgerufen werden kann, wie im folgenden Screenshot gezeigt. Weitere Informationen finden Sie unter [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

![Close-Methode des Window-Steuerelement Musters, das im Bereich "Eigenschaften" aufgerufen wird](images/close-invoked-from-properties-pane.png)

Folgende Befehle sind auf der **Eigenschaften** Symbolleiste verfügbar:

-   **Aktualisieren**– aktualisieren Sie die **Eigenschaften** Struktur.
-   **Alle erweitern**– erweitert alle Knoten in der **Eigenschaften** Struktur.

 

 




