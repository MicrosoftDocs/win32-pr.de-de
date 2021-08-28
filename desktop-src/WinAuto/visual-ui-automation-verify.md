---
title: Visual Benutzeroberflächenautomatisierung Verify
description: Visual Benutzeroberflächenautomatisierung Verify (Visual UIA Verify) ist ein Windows \32; GUI-Treiber für die UIA-Testbibliothek, die für manuelle Tests der Benutzeroberflächenautomatisierung konzipiert ist.
ms.assetid: 8AEB083E-785E-4F15-B708-2098A9A41B4E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e8c6118914c791e04226dfa11d2c3bd9548368
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466847"
---
# <a name="visual-ui-automation-verify"></a>Visual Benutzeroberflächenautomatisierung Verify

Visual Benutzeroberflächenautomatisierung Verify (Visual UIA Verify) ist ein Windows GUI-Treiber für die UIA-Testbibliothek, der für manuelle Tests der Benutzeroberflächenautomatisierung entwickelt wurde. Es stellt eine Schnittstelle zur UIA-Testbibliotheksfunktionalität bereit, die den Codierungsaufwand eines Befehlszeilentools beseitigt.

-   [Menübefehle](#menu-commands)
-   [Funktionsbereiche](#functional-panes)
    -   [Strukturbereich "Automation-Elemente"](#automation-elements-tree-pane)
    -   [Testbereich](#tests-pane)
    -   [Bereich „Testergebnisse“](#test-results-pane)
    -   [Eigenschaftenbereich](#properties-pane)

Visual UIA Verify unterstützt nur die UIA Verify XML logger (WUIALoggerXml.dll) nativ. Vom Benutzer auswählbare XML-Transformationen werden in Visual UIA Verify integriert, um verschiedene Ansichten des XML-Protokollierungsberichts im Testergebnisse **anzuzeigen.**

Standardmäßig lädt Visual UIA Verify den Benutzeroberflächenautomatisierung clientseitigen Anbieter, der mit dem ursprünglichen Release der Benutzeroberflächenautomatisierung. Sie können diesen Anbieter nicht laden, indem Sie **/NOCLIENTSIDEPROVIDER** in der Befehlszeilenoption von VisualUIVerifyNative.exe.

Der folgende Screenshot zeigt die wichtigsten Funktionsbereiche der Visual UIA Verify-Benutzeroberfläche.

![Hauptfunktionsbereiche der grafischen Uia-Überprüfungsbenutzeroberfläche](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a>Menübefehle

In der folgenden Tabelle werden die Befehle im Menü Visual UIA Verify (Visual UIA-Überprüfung) beschrieben.




| Menü | Befehl | BESCHREIBUNG | 
|------|---------|-------------|
| <strong>File</strong> | <strong>Beenden</strong> | Beenden Sie Visual UIA Verify. | 
| <strong>Ansicht</strong> | <strong>Hervorhebung</strong> | Markieren Sie das umgebundene Rechteck des ausgewählten Elements im <strong>Bereich Automation-Elementstruktur.</strong> Die folgenden Optionen sind verfügbar.<ul><li><strong>Rechteck</strong>: Eine durchstrichene rote Linie.</li><li><strong>Fading Rectangle –Eine</strong>durchdrungene rote Linie, die nach einigen Sekunden nicht mehr angezeigt wird.</li><li><strong>Lichtstrahl und Rechteck</strong>– Eine durchdrungsrote Linie mit zusätzlichen blauen Hervorhebungslinien, die von jeder Ecke des umgebundenen Rechtecks enumerieren.</li><li><strong>Keine</strong>– Keine sichtbare Hervorhebung.</li></ul> | 
| <strong>Automation Elements Tree</strong>${REMOVE}$<br /> | <strong>Ausgewähltes Element aktualisieren</strong> | Aktualisieren Sie die unteren Elemente des ausgewählten Elements im <strong>Bereich Automation-Elementstruktur.</strong> Die Liste der Elemente ist statisch und wird nicht dynamisch (automatisch) aktualisiert, wenn sich die Elementstruktur ändert. | 
| <strong>Navigation</strong> | Navigieren Sie durch die Elementstrukturhierarchie zu einem der folgenden Elemente.<ul><li><strong>Übergeordnetes</strong>Element – Zum übergeordneten Element wechseln.</li><li><strong>Erstes untergeordnetes</strong>Element : Wechseln Sie zum ersten untergeordneten Element.</li><li><strong>Nächstes gleichgeordnetes</strong>Element : Wechseln Sie zum ersten gleichgeordneten Element.</li><li><strong>Vorheriges gleichgeordnetes</strong>Element – Zum vorherigen gleichgeordneten Element wechseln.</li><li><strong>Letztes untergeordnetes</strong>Element – Zum letzten untergeordneten Element wechseln.</li></ul> | 
| <strong>Modus</strong>${REMOVE}$<br /> | <strong>Always On Oben</strong> | Das Fenster Visual UIA Verify (Visual UIA-Überprüfung) verbleibt am oberen Ende der Desktop-Z-Reihenfolge. | 
| <strong>Hovermodus (STRG verwenden)</strong> | Wenn die STRG-TASTE gedrückt wird, wird das Element unter dem Mauszeiger als das element von Interesse identifiziert. Der <strong>Bereich Automation Elements Tree</strong> (Automatisierungselementstruktur) wird aktualisiert, und das entsprechende Element in der Elementliste wird hervorgehoben. | 
| <strong>Fokusverfolgung</strong> | Wenn sich der Fokus ändert, wird das Element mit dem Fokus als das element von Interesse identifiziert. Der <strong>Bereich Automation Elements Tree</strong> (Automatisierungselementstruktur) wird aktualisiert, und das entsprechende Element in der Elementliste wird hervorgehoben. | 
| <strong>Tests</strong>${REMOVE}$<br /> | <strong>Nach links wechseln</strong> | Verschieben Sie einen Knoten in der <strong>Teststruktur nach</strong> links. | 
| <strong>Nach oben</strong> | Verschieben Sie einen Knoten in der <strong>Teststruktur</strong> nach oben. | 
| <strong>Nach unten</strong> | Verschieben Sie einen Knoten in der <strong>Teststruktur</strong> nach unten. | 
| <strong>Nach rechts wechseln</strong> | Verschieben Sie einen Knoten in der <strong>Teststruktur</strong> nach rechts. | 
| <strong>Ausführen ausgewählter Tests für ausgewähltes Element</strong> | Führen Sie die ausgewählten Tests in der <strong>Teststruktur</strong> für das ausgewählte Element aus. | 
| <strong>Filtern bekannter Probleme</strong> | Filtern Sie bekannte Benutzeroberflächenautomatisierung fehler aus den Testergebnissen. | 
| <strong>Hilfe</strong> | <strong>Informationen zu Visual Benutzeroberflächenautomatisierung Verify</strong> | Anzeigen der Softwareversion und copyright-Informationen für Visual UIA Verify. | 




 

## <a name="functional-panes"></a>Funktionsbereiche

In diesem Abschnitt werden die Funktionsbereiche der Visual UIA Verify-Benutzeroberfläche beschrieben.

-   [Strukturbereich "Automation-Elemente"](#automation-elements-tree-pane)
-   [Testbereich](#tests-pane)
-   [Bereich „Testergebnisse“](#test-results-pane)
-   [Eigenschaftenbereich](#properties-pane)

### <a name="automation-elements-tree-pane"></a>Strukturbereich "Automation-Elemente"

Der **Bereich Automatisierungselementstruktur** enthält eine hierarchische Momentaufnahme von Automatisierungselementobjekten, die zum Testen verfügbar sind. Das oberste Element in der Struktur stellt den Desktop dar.

Diese Ansicht ist eine statische Sammlung, die kompiliert wird, wenn Visual UIA Verify gestartet wird. Um die Ansicht auf dem ausgewählten Knoten zu aktualisieren, verwenden Sie den Menübefehl **Ausgewähltes Element aktualisieren** oder die Symbolleistenschaltfläche.

Der folgende Screenshot zeigt den Bereich **Automation-Elementstruktur.**

![Strukturbereich der Automatisierungselemente von visual uia verify](images/automation-elements-tree-pane.png)

Ein abgeblendeter (nicht  verfügbarer) Knoten in der Automatisierungselementstruktur gibt an, dass das Element ein Element der unformatierten Benutzeroberflächenautomatisierung-Ansicht ist, aber nicht die Bedingungen erfüllt, die erforderlich sind, um als Member der Inhaltsansicht oder Steuerelementansicht angesehen zu werden. Das -Element kann jedoch weiterhin von Visual Benutzeroberflächenautomatisierung überprüft werden. Weitere Informationen finden Sie in der Übersicht [Benutzeroberflächenautomatisierung Struktur](uiauto-treeoverview.md).

Auf der Symbolleiste der **Automatisierungselementestruktur sind** folgende Befehle verfügbar:

-   **Aktualisieren :** Aktualisiert den ausgewählten Knoten und seine unteren Elemente. Mit diesem Befehl wird die gesamte Elementstruktur nur aktualisiert, wenn der Stammknoten ausgewählt ist.
-   **Übergeordnetes Element (STRG+UMSCHALT+F6):** Wechseln Sie zum übergeordneten Element des aktuellen Knotens.
-   **Erstes untergeordnetes (STRG+UMSCHALT+F7)**– Zum ersten untergeordneten Knoten des aktuellen Knotens wechseln.
-   **Next Sibling (STRG+UMSCHALT+F8) –** Zum nächsten gleichgeordneten untergeordneten Knoten des aktuellen Knotens wechseln.
-   **Previous Sibling (STRG+UMSCHALT+F9) –** Zum vorherigen gleichgeordneten Knoten des aktuellen Knotens wechseln.
-   **Last Child (STRG+UMSCHALT+F10) –** Zum letzten untergeordneten Knoten des aktuellen Knotens wechseln.
-   **Fokusnachverfolgung**– Umschalten der Knotenauswahl basierend auf der Fokusnachverfolgung.

### <a name="tests-pane"></a>Testbereich

Der **Bereich** Tests enthält eine Liste der Benutzeroberflächenautomatisierung-Tests, die nach Testtyp (**Automation-Element,** **Steuerelement** und Muster **)** und Priorität (**Buildüberprüfung,** Priorität **0,** Priorität **1,** **Priorität 2** und **Priorität 3**) organisiert sind. Diese Liste wird basierend auf dem Steuerelementtyp des ausgewählten Elements im Bereich **Automatisierungselementstruktur** generiert. Weitere Informationen finden Sie unter [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

Der folgende Screenshot zeigt den **Bereich Tests.**

![Testbereich](images/test-pane.png)

Folgende Befehle sind auf der Symbolleiste **Tests** verfügbar:

-   **Show**– Gibt die anzuzeigenden Benutzeroberflächenautomatisierung Tests an. Das bedeutet, dass alle Tests oder nur Tests angezeigt werden, die für den Steuerelementtyp des ausgewählten Elements in der **Automation Elements Tree** (Standard) geeignet sind.
-   **Typ**: Gibt die anzuzeigenden Testtypen an: **Automation-Element,** **Muster** oder **Steuerelement.**
-   **Prioritäten**– Gibt die anzuzeigenden Testprioritäten an: **Buildüberprüfung,** **Priorität 0,** **Priorität 1,** **Priorität 2** oder **Priorität 3.**
-   **Gehe nach links**– Gehe zum übergeordneten Element des aktuellen Knotens.
-   **Nach oben**– Wechseln Sie zum vorherigen gleichgeordneten Element des aktuellen Knotens.
-   **Nach unten**: Wechseln Sie zum nächsten nebengeordneten Element des aktuellen Knotens.
-   **Nach rechts**: Wechseln Sie zum ersten untergeordneten Element des aktuellen Knotens.
-   **Ausgewählte Tests ausführen**– Führt die Tests für das in der **Automation-Elementstruktur** ausgewählte Element aus.

### <a name="test-results-pane"></a>Bereich „Testergebnisse“

Der **bereich Testergebnisse** enthält die Protokollierungsfunktion "Visual UIA Verify". Der folgende Screenshot zeigt den **bereich Testergebnisse.**

![Testergebnisbereich](images/test-results-pane.png)

Befehle, die über die Symbolleiste **Testergebnisse** verfügbar sind, umfassen Folgendes:

-   **Zurück**– Seite rückwärts im Berichtsanzeigeverlauf.
-   **Vorwärts**– Seitenvorschau im Berichtsanzeigeverlauf.
-   **Insgesamt**– Zeigt eine Zusammenfassung der Testergebnisse an (**Erfolgreich,** **Fehler** und **Unerwarteter Fehler**). Das Testergebnis ist mit der Ansicht **Alle Ergebnisse** verknüpft. Der Befehl **Overall** zeigt eine Tabelle wie die folgende an.

    ![Testergebnistabelle gesamt](images/overall-test-results.png)

-   **Alle Ergebnisse**: Zeigt ein ausführliches Protokoll für jedes Testergebnis an, wie in den folgenden Tabellen gezeigt.

    ![Beispielprotokollergebnisdetails aus der Ansicht "Alle Ergebnisse"](images/all-results-log.png)

    Der Testname in der Tabelle **Alle Ergebnisse** ist wie in der folgenden Tabelle mit einer Testfallbeschreibung für das -Element verknüpft.

    ![Testfalldetails](images/test-case-detail.png)

-   **Vollständiges Protokoll**– Zeigt eine alternative Ansicht des detaillierten Protokolls für jedes Testergebnis an, wie im folgenden Screenshot gezeigt.

    ![Alternative Ansicht eines Testfalldetails](images/alt-view-of-test-case-detail.png)

-   **XML**– Zeigt den von der XML-Protokollierung generierten unformatierten XML-Code an.
-   **Schnellsuche**– Einfache Textsuche der aktuellen Ansicht im **Testergebnisse** Bereich.
-   **In neuem Fenster öffnen**: Öffnet die aktuelle Ansicht in einer neuen Instanz von Internet Explorer.

### <a name="properties-pane"></a>Eigenschaftenbereich

Der Bereich **Eigenschaften** enthält eine Liste der Benutzeroberflächenautomatisierung Eigenschaften und Eigenschaftswerte, die nach Eigenschaftstyp organisiert sind: **Allgemeine Barrierefreiheit,** **Identifikation,** **Muster** (Steuerelementmuster), **Zustand** und **Sichtbarkeit.** Die Eigenschaftswerte werden basierend auf dem Steuerelementtyp des im Bereich **Automation Elements Tree (Automatisierungselementstruktur)** ausgewählten Objekts dynamisch aufgefüllt. Der folgende Screenshot zeigt den **Bereich Eigenschaften.**

![Eigenschaftenbereich](images/properties-pane.png)

Wenn das ausgewählte Steuerelement ein bestimmtes Steuerelementmuster unterstützt, bietet Visual UIA Verify die Möglichkeit, Methoden aufzurufen, die von diesem Steuerelementmuster unterstützt werden. Der [Steuerelementtyp Fenster](uiauto-supportwindowcontroltype.md) unterstützt z. B. das [Fenster-Steuerelementmuster](uiauto-implementingwindow.md), das über eine [**Close-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) verfügt, die über den **Eigenschaftenbereich** aufgerufen werden kann, wie im folgenden Screenshot gezeigt. Weitere Informationen finden Sie unter [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

![close-Methode des Fenstersteuerelementmusters, das über den Eigenschaftenbereich aufgerufen wird](images/close-invoked-from-properties-pane.png)

Folgende Befehle sind auf der **Eigenschaftensymbolleiste** verfügbar:

-   **Aktualisieren**: Aktualisieren Sie die **Eigenschaftenstruktur.**
-   **Alle erweitern**– Erweitert alle Knoten in der **Eigenschaftenstruktur.**

 

 




