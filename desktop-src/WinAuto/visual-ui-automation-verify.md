---
title: Visual Benutzeroberflächenautomatisierung Verify
description: Visual Benutzeroberflächenautomatisierung Verify (Visual UIA Verify) ist ein Windows \ 32; GUI-Treiber für die UIA-Testbibliothek, die für manuelle Tests der Benutzeroberflächenautomatisierung konzipiert ist.
ms.assetid: 8AEB083E-785E-4F15-B708-2098A9A41B4E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c50fdd123d24c8a6ef4215ae2451cf49b854b60b26c5d741db1921c42f6f7aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563654"
---
# <a name="visual-ui-automation-verify"></a>Visual Benutzeroberflächenautomatisierung Verify

Visual Benutzeroberflächenautomatisierung Verify (Visual UIA Verify) ist ein Windows GUI-Treiber für die UIA-Testbibliothek, der für manuelle Tests der Benutzeroberflächenautomatisierung entwickelt wurde. Es stellt eine Schnittstelle zur UIA-Testbibliotheksfunktion bereit, die den Codierungsaufwand eines Befehlszeilentools entfällt.

-   [Menübefehle](#menu-commands)
-   [Funktionsbereich](#functional-panes)
    -   [Strukturbereich "Automation-Elemente"](#automation-elements-tree-pane)
    -   [Testbereich](#tests-pane)
    -   [Bereich „Testergebnisse“](#test-results-pane)
    -   [Eigenschaftenbereich](#properties-pane)

Visual UIA Verify unterstützt nur die UIA Verify XML-Protokollierung (WUIALoggerXml.dll) nativ. Vom Benutzer auswählbare XML-Transformationen werden in Visual UIA Verify integriert, um verschiedene Ansichten des XML-Protokollierungsberichts im **bereich Testergebnisse** darzustellen.

Standardmäßig lädt Visual UIA Verify den Benutzeroberflächenautomatisierung clientseitigen Anbieter, der mit der ursprünglichen Version von Benutzeroberflächenautomatisierung ausgeliefert wurde. Sie können diesen Anbieter nicht laden, indem Sie **/NOCLIENTSIDEPROVIDER** in der Befehlszeilenoption von VisualUIVerifyNative.exe hinzufügen.

Der folgende Screenshot zeigt die Hauptfunktionsbereiche der Benutzeroberfläche "Visual UIA Verify".

![Hauptfunktionsbereiche der grafischen Benutzeroberfläche "uia verify"](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a>Menübefehle

In der folgenden Tabelle werden die Befehle im Menü Visual UIA Verify (Visual UIA-Überprüfung) beschrieben.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Menü</th>
<th>Befehl</th>
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
<td>Markieren Sie das umgrenzende Rechteck des ausgewählten Elements im Bereich <strong>Automation Elements Tree (Automatisierungselementstruktur).</strong> Die folgenden Optionen sind verfügbar.
<ul>
<li><strong>Rechteck</strong>: Eine durchgezogene rote Linie.</li>
<li><strong>Verblassendes Rechteck</strong>: Eine durchgezogene rote Linie, die nach einigen Sekunden nicht mehr angezeigt wird.</li>
<li><strong>Lichtstrahl und Rechteck</strong>: Eine durchgehende rote Linie mit zusätzlichen blauen Hervorhebungslinien, die von jeder Ecke des umschließenden Rechtecks stammen.</li>
<li><strong>None</strong>– Keine sichtbare Hervorhebung.</li>
</ul></td>
</tr>
<tr class="odd">
<td rowspan="2"><strong>Automation Elements Tree</strong>${REMOVE}$<br />
</td>
<td><strong>Ausgewähltes Element aktualisieren</strong></td>
<td>Aktualisieren Sie die untergeordneten Elemente des ausgewählten Elements im Bereich <strong>Automation-Elementstruktur.</strong> Die Liste der Elemente ist statisch und wird nicht dynamisch (automatisch) aktualisiert, wenn sich die Elementstruktur ändert.</td>
</tr>
<tr class="even">
<td><strong>Navigation</strong></td>
<td>Navigieren Sie durch die Elementstrukturhierarchie zu einem der folgenden Elemente.
<ul>
<li><strong>Übergeordnetes</strong>Element : Wechseln Sie zum übergeordneten Element.</li>
<li><strong>First Child</strong>– Wechseln Sie zum ersten untergeordneten Element.</li>
<li><strong>Next Sibling</strong>– Wechseln Sie zum ersten nebengeordneten Element.</li>
<li><strong>Previous Sibling</strong>– Wechseln Sie zum vorherigen nebengeordneten Element.</li>
<li><strong>Letztes untergeordnetes</strong>Element : Wechseln Sie zum letzten untergeordneten Element.</li>
</ul></td>

</tr>
<tr class="odd">
<td rowspan="3"><strong>Modus</strong>${REMOVE}$<br />
</td>
<td><strong>Always On Top</strong></td>
<td>Das Fenster Visual UIA Verify (Visual UIA-Überprüfung) bleibt oben in der Z-Reihenfolge des Desktops.</td>
</tr>
<tr class="even">
<td><strong>Hovermodus (Strg drücken)</strong></td>
<td>Wenn die STRG-TASTE gedrückt wird, wird das Element unter dem Mauscursor als das element von Interesse identifiziert. Der Bereich <strong>Automation Elements Tree (Automation-Elementstruktur)</strong> wird aktualisiert, und das entsprechende Element in der Elementliste wird hervorgehoben.</td>

</tr>
<tr class="odd">
<td><strong>Fokusnachverfolgung</strong></td>
<td>Wenn sich der Fokus ändert, wird das Element mit dem Fokus als das element of interest identifiziert. Der Bereich <strong>Automation Elements Tree (Automation-Elementstruktur)</strong> wird aktualisiert, und das entsprechende Element in der Elementliste wird hervorgehoben.</td>

</tr>
<tr class="even">
<td rowspan="6"><strong>Tests</strong>${REMOVE}$<br />
</td>
<td><strong>Nach links wechseln</strong></td>
<td>Verschieben Sie einen Knoten in der <strong>Teststruktur</strong> nach links.</td>
</tr>
<tr class="odd">
<td><strong>Nach oben</strong></td>
<td>Verschieben Sie einen Knoten in der <strong>Teststruktur</strong> nach oben.</td>

</tr>
<tr class="even">
<td><strong>Nach unten</strong></td>
<td>Verschieben Sie einen Knoten in der <strong>Teststruktur</strong> nach unten.</td>

</tr>
<tr class="odd">
<td><strong>Nach rechts wechseln</strong></td>
<td>Verschieben Sie einen Knoten in der <strong>Teststruktur</strong> nach rechts.</td>

</tr>
<tr class="even">
<td><strong>Ausführen ausgewählter Tests für ausgewähltes Element</strong></td>
<td>Führen Sie die ausgewählten Tests aus der <strong>Teststruktur</strong> für das ausgewählte Element aus.</td>

</tr>
<tr class="odd">
<td><strong>Filtern bekannter Probleme</strong></td>
<td>Filtern Sie bekannte Benutzeroberflächenautomatisierung Fehler aus den Testergebnissen.</td>

</tr>
<tr class="even">
<td><strong>Hilfe</strong></td>
<td><strong>Informationen zur Überprüfung von Visual Benutzeroberflächenautomatisierung</strong></td>
<td>Anzeigen der Softwareversion und der Copyrightinformationen für Die Visual UIA-Überprüfung.</td>
</tr>
</tbody>
</table>



 

## <a name="functional-panes"></a>Funktionsbereich

In diesem Abschnitt werden die Funktionbereiche auf der Benutzeroberfläche visual UIA Verify beschrieben.

-   [Strukturbereich "Automation-Elemente"](#automation-elements-tree-pane)
-   [Testbereich](#tests-pane)
-   [Bereich „Testergebnisse“](#test-results-pane)
-   [Eigenschaftenbereich](#properties-pane)

### <a name="automation-elements-tree-pane"></a>Strukturbereich "Automation-Elemente"

Der Bereich **Automation Elements Tree** enthält eine hierarchische Momentaufnahme von Automatisierungselementobjekten, die zum Testen verfügbar sind. Das oberste Element in der Struktur stellt den Desktop dar.

Diese Ansicht ist eine statische Auflistung, die kompiliert wird, wenn Visual UIA Verify gestartet wird. Um die Ansicht auf dem ausgewählten Knoten zu aktualisieren, verwenden Sie den Menübefehl **Ausgewähltes Element aktualisieren** oder die Symbolleistenschaltfläche.

Der folgende Screenshot zeigt den Bereich **"Automation Elements Tree".**

![Automatisierungselement-Strukturbereich der visuellen UIA-Überprüfung](images/automation-elements-tree-pane.png)

Ein abgeblendeter (nicht verfügbarer) Knoten in der **Automation Elements Tree** gibt an, dass das Element ein Element der Benutzeroberflächenautomatisierung Rohansicht ist, aber nicht die Bedingungen erfüllt, die erforderlich sind, um als Mitglied der Inhaltsansicht oder Steuerelementansicht angesehen zu werden. Das Element kann jedoch weiterhin über Visual Benutzeroberflächenautomatisierung Verify getestet werden. Weitere Informationen finden Sie in der [Übersicht über Benutzeroberflächenautomatisierung-Struktur.](uiauto-treeoverview.md)

Befehle, die über die **Symbolleiste der Automation Elements Tree** verfügbar sind, umfassen Folgendes:

-   **Aktualisieren**: Aktualisieren Sie den ausgewählten Knoten und seine untergeordneten Elemente. Dieser Befehl aktualisiert nur dann die gesamte Elementstruktur, wenn der Stammknoten ausgewählt ist.
-   **Parent (STRG+UMSCHALT+F6):** Wechseln Sie zum übergeordneten Element des aktuellen Knotens.
-   **Erstes untergeordnetes Element (STRG+UMSCHALT+F7):** Wechseln Sie zum ersten untergeordneten Element des aktuellen Knotens.
-   **Next Sibling (STRG+UMSCHALT+F8):** Wechseln Sie zum nächsten nebengeordneten untergeordneten Element des aktuellen Knotens.
-   **Previous Sibling (STRG+UMSCHALT+F9):** Wechseln Sie zum vorherigen gleichgeordneten Element des aktuellen Knotens.
-   **Letztes untergeordnetes Element (STRG+UMSCHALT+F10):** Wechseln Sie zum letzten untergeordneten Element des aktuellen Knotens.
-   **Fokusnachverfolgung**: Umschalten der Knotenauswahl basierend auf der Fokusnachverfolgung

### <a name="tests-pane"></a>Testbereich

Der Bereich **Tests** enthält eine Liste der Benutzeroberflächenautomatisierung Tests, die nach Testtyp **(Automation-Element,** **Steuerelement** und **Muster)** und Priorität **(Buildüberprüfung,** **Priorität 0,** **Priorität 1,** **Priorität 2** und **Priorität 3)** organisiert sind. Diese Liste wird basierend auf dem Steuerelementtyp des ausgewählten Elements im **Bereich Automation-Elementstruktur** generiert. Weitere Informationen finden Sie unter [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

Der folgende Screenshot zeigt den **Bereich Tests.**

![Testbereich](images/test-pane.png)

Auf der Symbolleiste **Tests sind unter anderem folgende** Befehle verfügbar:

-   **Anzeigen**: Gibt die Benutzeroberflächenautomatisierung anzuzeigenden Tests an. Das bedeutet, dass alle Tests oder nur Tests angezeigt werden, die für den Steuerelementtyp des ausgewählten Elements in der **Automation-Elementstruktur** (Standard) geeignet sind.
-   **Typ**: Gibt die anzuzeigenden Testtypen an: **Automation-Element,** **Muster** oder **Steuerelement**.
-   **Prioritäten**– Gibt die anzuzeigenden Testprioritäten an: **Buildüberprüfung,** Priorität **0,** Priorität **1,** Priorität **2** oder **Priorität 3.**
-   **Nach links** wechseln – Wechseln Sie zum übergeordneten Element des aktuellen Knotens.
-   **Nach oben**: Wechseln Sie zum vorherigen gleichgeordneten Knoten des aktuellen Knotens.
-   **Nach unten**: Wechseln Sie zum nächsten gleichgeordneten Knoten des aktuellen Knotens.
-   **Gehe nach rechts**– Gehe zum ersten untergeordneten Knoten des aktuellen Knotens.
-   **Ausgewählte Tests ausführen – Führt** die Tests für das in der Automation-Elementstruktur ausgewählte Element **aus.**

### <a name="test-results-pane"></a>Bereich „Testergebnisse“

Der **Testergebnisse** bereich enthält die Protokollierungsfunktion Visual UIA Verify (Visual UIA Verify). Der folgende Screenshot zeigt **den** Testergebnisse Bereich.

![Bereich "Testergebnisse"](images/test-results-pane.png)

Folgende Befehle sind auf der **Symbolleiste Testergebnisse** verfügbar:

-   **Zurück**– Rückwärts im Berichtsanzeigeverlauf.
-   **Vorwärts –** Vorwärtsseiten im Berichtsanzeigeverlauf.
-   **Gesamt**– Zeigt eine Zusammenfassung der Testergebnisse an (**Erfolgreich,** **Fehler** und **unerwarteter Fehler**). Das Testergebnis ist mit der Ansicht **Alle Ergebnisse** verknüpft. Der **Befehl Overall** zeigt eine Tabelle wie die folgende an.

    ![Allgemeine Testergebnistabelle](images/overall-test-results.png)

-   **Alle Ergebnisse–** Zeigt ein detailliertes Protokoll für jedes Testergebnis an, wie in den folgenden Tabellen gezeigt.

    ![Beispielprotokollergebnisdetail aus der Ansicht "Alle Ergebnisse"](images/all-results-log.png)

    Der Testname in der **Tabelle Alle** Ergebnisse ist mit einer Testfallbeschreibung für das Element verknüpft, wie in der folgenden Tabelle dargestellt.

    ![Testfalldetails](images/test-case-detail.png)

-   **Vollständiges** Protokoll – Zeigt eine alternative Ansicht des detaillierten Protokolls für jedes Testergebnis an, wie im folgenden Screenshot gezeigt.

    ![Alternative Ansicht eines Testfalldetails](images/alt-view-of-test-case-detail.png)

-   **XML**– Zeigt den unformatierten XML-Code an, der von der XML-Protokollierung generiert wurde.
-   **Schnellsuche –** Einfache Textsuche der aktuellen Ansicht im **Testergebnisse** Bereich.
-   **In neuem Fenster öffnen**– Öffnet die aktuelle Ansicht in einer neuen Instanz von Internet Explorer.

### <a name="properties-pane"></a>Eigenschaftenbereich

Der **Bereich** Eigenschaften enthält eine Liste Benutzeroberflächenautomatisierung Eigenschaften und Eigenschaftswerte, die nach Eigenschaftentyp organisiert sind: **Allgemeine** Barrierefreiheit, **Identifikation,** **Muster** (Steuerelementmuster), **Status** und **Sichtbarkeit.** Die Eigenschaftswerte werden basierend auf dem Steuerelementtyp des im Bereich Automatisierungselementestruktur ausgewählten Objekts **dynamisch aufgefüllt.** Der folgende Screenshot zeigt den **Bereich Eigenschaften.**

![Eigenschaftenbereich](images/properties-pane.png)

Wenn das ausgewählte Steuerelement ein bestimmtes Steuerelementmuster unterstützt, bietet Visual UIA Verify die Möglichkeit zum Aufrufen von Methoden, die von diesem Steuerelementmuster unterstützt werden. Der Steuerelementtyp [Fenster](uiauto-supportwindowcontroltype.md) unterstützt z. B. das [Fenster-Steuerelementmuster,](uiauto-implementingwindow.md)das  über eine [**Close-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) verfügt, die über den Eigenschaftenbereich aufgerufen werden kann, wie im folgenden Screenshot gezeigt. Weitere Informationen finden Sie unter [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

![close-Methode des Fenstersteuermusters, das über den Eigenschaftenbereich aufgerufen wird](images/close-invoked-from-properties-pane.png)

Auf der Symbolleiste Eigenschaften **sind folgende Befehle** verfügbar:

-   **Aktualisieren :** Aktualisieren Sie die **Eigenschaftenstruktur.**
-   **Alle erweitern**– Erweitert alle Knoten in der **Eigenschaftenstruktur.**

 

 




