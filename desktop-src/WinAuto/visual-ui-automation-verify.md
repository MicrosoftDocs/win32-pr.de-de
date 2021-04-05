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
# <a name="visual-ui-automation-verify"></a><span data-ttu-id="810d6-103">Überprüfen der Visual UI-Automatisierung</span><span class="sxs-lookup"><span data-stu-id="810d6-103">Visual UI Automation Verify</span></span>

<span data-ttu-id="810d6-104">Visual UI Automation Verify (Visual UIA Verify) ist ein Windows GUI-Treiber für die UIA-Test Bibliothek, die für manuelle Tests der Benutzeroberflächen Automatisierung konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="810d6-104">Visual UI Automation Verify (Visual UIA Verify) is a Windows GUI driver for the UIA Test Library that is designed for manual testing of UI automation.</span></span> <span data-ttu-id="810d6-105">Es stellt eine Schnittstelle für die Funktionalität der UIA-Test Bibliothek bereit, mit der der Codierungsaufwand eines Befehlszeilen Tools entfällt.</span><span class="sxs-lookup"><span data-stu-id="810d6-105">It provides an interface to UIA Test Library functionality that eliminates the coding overhead of a command-line tool.</span></span>

-   [<span data-ttu-id="810d6-106">Menübefehle</span><span class="sxs-lookup"><span data-stu-id="810d6-106">Menu Commands</span></span>](#menu-commands)
-   [<span data-ttu-id="810d6-107">Funktionale Bereiche</span><span class="sxs-lookup"><span data-stu-id="810d6-107">Functional Panes</span></span>](#functional-panes)
    -   [<span data-ttu-id="810d6-108">Bereich "Automatisierungselemente-Struktur"</span><span class="sxs-lookup"><span data-stu-id="810d6-108">Automation Elements Tree Pane</span></span>](#automation-elements-tree-pane)
    -   [<span data-ttu-id="810d6-109">Bereich "Tests"</span><span class="sxs-lookup"><span data-stu-id="810d6-109">Tests Pane</span></span>](#tests-pane)
    -   [<span data-ttu-id="810d6-110">Bereich „Testergebnisse“</span><span class="sxs-lookup"><span data-stu-id="810d6-110">Test Results Pane</span></span>](#test-results-pane)
    -   [<span data-ttu-id="810d6-111">Eigenschaften Bereich</span><span class="sxs-lookup"><span data-stu-id="810d6-111">Properties Pane</span></span>](#properties-pane)

<span data-ttu-id="810d6-112">Visual UIA Verify unterstützt nur die systemeigene UIA-Überprüfung-XML-Protokollierung (WUIALoggerXml.dll).</span><span class="sxs-lookup"><span data-stu-id="810d6-112">Visual UIA Verify supports only the UIA Verify XML logger (WUIALoggerXml.dll) natively.</span></span> <span data-ttu-id="810d6-113">Benutzer auswählbare XML-Transformationen sind in Visual UIA-Überprüfung integriert, um verschiedene Ansichten des XML-Protokollierungs Berichts im **Testergebnisse** Bereich darzustellen.</span><span class="sxs-lookup"><span data-stu-id="810d6-113">User-selectable XML transformations are incorporated into Visual UIA Verify to present various views of the XML logger report in the **Test Results** pane.</span></span>

<span data-ttu-id="810d6-114">Standardmäßig lädt Visual UIA Verify den Client seitigen Benutzeroberflächenautomatisierungs-Anbieter, der mit der ursprünglichen Version der Benutzeroberflächen Automatisierung ausgeliefert wurde.</span><span class="sxs-lookup"><span data-stu-id="810d6-114">By default, Visual UIA Verify loads the UI Automation client-side provider that shipped with the original release of UI Automation.</span></span> <span data-ttu-id="810d6-115">Sie können auswählen, dass dieser Anbieter nicht geladen werden soll, indem Sie **/NOCLIENTSIDEPROVIDER** in der Befehlszeilenoption von VisualUIVerifyNative.exe hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="810d6-115">You can choose not to load this provider by adding **/NOCLIENTSIDEPROVIDER** in the command-line option of VisualUIVerifyNative.exe.</span></span>

<span data-ttu-id="810d6-116">Der folgende Screenshot zeigt die Haupt Funktionsbereiche der Benutzeroberfläche der Visual UIA-Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="810d6-116">The following screen shot shows the main functional areas of the Visual UIA Verify user interface.</span></span>

![Haupt Funktionsbereiche der Benutzeroberfläche der Visual UIA-Überprüfung](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a><span data-ttu-id="810d6-118">Menübefehle</span><span class="sxs-lookup"><span data-stu-id="810d6-118">Menu Commands</span></span>

<span data-ttu-id="810d6-119">In der folgenden Tabelle werden die Befehle im Menü der Visual UIA-Überprüfung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="810d6-119">The following table describes the commands in the Visual UIA Verify menu.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="810d6-120">Menü</span><span class="sxs-lookup"><span data-stu-id="810d6-120">Menu</span></span></th>
<th><span data-ttu-id="810d6-121">Get-Help</span><span class="sxs-lookup"><span data-stu-id="810d6-121">Command</span></span></th>
<th><span data-ttu-id="810d6-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="810d6-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="810d6-123"><strong>File</strong></span><span class="sxs-lookup"><span data-stu-id="810d6-123"><strong>File</strong></span></span></td>
<td><span data-ttu-id="810d6-124"><strong>Beenden</strong></span><span class="sxs-lookup"><span data-stu-id="810d6-124"><strong>Exit</strong></span></span></td>
<td><span data-ttu-id="810d6-125">Beenden Sie Visual UIA Verify.</span><span class="sxs-lookup"><span data-stu-id="810d6-125">Exit Visual UIA Verify.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="810d6-126"><strong>Ansicht</strong></span><span class="sxs-lookup"><span data-stu-id="810d6-126"><strong>View</strong></span></span></td>
<td><span data-ttu-id="810d6-127"><strong>Hervorhebung</strong></span><span class="sxs-lookup"><span data-stu-id="810d6-127"><strong>Highlighting</strong></span></span></td>
<td><span data-ttu-id="810d6-128">Markieren Sie das umgebende Rechteck des ausgewählten Elements im Strukturbereich <strong>Automation-Elemente</strong> .</span><span class="sxs-lookup"><span data-stu-id="810d6-128">Highlight the bounding rectangle of the selected element in the <strong>Automation Elements Tree</strong> pane.</span></span> <span data-ttu-id="810d6-129">Die folgenden Optionen sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="810d6-129">The following options are available.</span></span>
<ul>
<li><span data-ttu-id="810d6-130"><strong>Rechteck</strong>– eine solide rote Linie.</span><span class="sxs-lookup"><span data-stu-id="810d6-130"><strong>Rectangle</strong>—A solid red line.</span></span></li>
<li><span data-ttu-id="810d6-131"><strong>Ausblenden des Rechtecks</strong>– eine rote Linie, die nach einigen Sekunden verschwindet.</span><span class="sxs-lookup"><span data-stu-id="810d6-131"><strong>Fading Rectangle</strong>—A solid red line that disappears after a few seconds.</span></span></li>
<li><span data-ttu-id="810d6-132"><strong>Rays und Rechteck</strong>– eine durchgezogen rote Linie mit zusätzlichen blauen Hervorhebungs Linien, die aus jeder Ecke des umgebenden Rechtecks heraus Strahlen.</span><span class="sxs-lookup"><span data-stu-id="810d6-132"><strong>Rays and Rectangle</strong>—A solid red line with additional blue highlight lines that radiate from each corner of the bounding rectangle.</span></span></li>
<li><span data-ttu-id="810d6-133"><strong>None</strong>– keine sichtbare Hervorhebung.</span><span class="sxs-lookup"><span data-stu-id="810d6-133"><strong>None</strong>—No visible highlight.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="810d6-134"><strong>Automation-Element</strong>Struktur $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="810d6-134"><strong>Automation Elements Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="810d6-135"><strong>Ausgewähltes Element aktualisieren</strong></span><span class="sxs-lookup"><span data-stu-id="810d6-135"><strong>Refresh Selected Element</strong></span></span></td>
<td><span data-ttu-id="810d6-136">Aktualisieren Sie die untergeordneten Elemente des ausgewählten Elements im Strukturbereich <strong>Automation-Elemente</strong> .</span><span class="sxs-lookup"><span data-stu-id="810d6-136">Refresh the children of the selected element in the <strong>Automation Elements Tree</strong> pane.</span></span> <span data-ttu-id="810d6-137">Die Liste der Elemente ist statisch und wird nicht dynamisch (automatisch) aktualisiert, wenn sich die Elementstruktur ändert.</span><span class="sxs-lookup"><span data-stu-id="810d6-137">The list of elements is static and does not refresh dynamically (automatically) if the element tree changes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="810d6-138"><strong>Navigation</strong></span><span class="sxs-lookup"><span data-stu-id="810d6-138"><strong>Navigation</strong></span></span></td>
<td><span data-ttu-id="810d6-139">Navigieren Sie durch die Elementstruktur Hierarchie zu einem der folgenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="810d6-139">Navigate through the element tree hierarchy to one of the following elements.</span></span>
<ul>
<li><span data-ttu-id="810d6-140">Über <strong>geordnetes</strong>Element – gehe zu übergeordnetem Element.</span><span class="sxs-lookup"><span data-stu-id="810d6-140"><strong>Parent</strong>—Go to parent element.</span></span></li>
<li><span data-ttu-id="810d6-141"><strong>First Child</strong>– gehe zum ersten untergeordneten Element.</span><span class="sxs-lookup"><span data-stu-id="810d6-141"><strong>First Child</strong>—Go to first child element.</span></span></li>
<li><span data-ttu-id="810d6-142"><strong>Nächstes</strong>gleich geordnetes Element – gehe zum ersten neben geordneten Element.</span><span class="sxs-lookup"><span data-stu-id="810d6-142"><strong>Next Sibling</strong>—Go to first sibling element.</span></span></li>
<li><span data-ttu-id="810d6-143"><strong>Vorheriges</strong>gleich geordnetes Element – gehe zum vorangehenden neben geordneten Element.</span><span class="sxs-lookup"><span data-stu-id="810d6-143"><strong>Previous Sibling</strong>—Go to previous sibling element.</span></span></li>
<li><span data-ttu-id="810d6-144"><strong>Last Child</strong>– gehe zum letzten untergeordneten Element.</span><span class="sxs-lookup"><span data-stu-id="810d6-144"><strong>Last Child</strong>—Go to last child element.</span></span></li>
</ul></td>

</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="810d6-145"><strong>Modus</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="810d6-145"><strong>Mode</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="810d6-146"><strong>Always on oben</strong></span><span class="sxs-lookup"><span data-stu-id="810d6-146"><strong>Always On Top</strong></span></span></td>
<td><span data-ttu-id="810d6-147">Das Fenster "Visual UIA verify" bleibt am Anfang der z-Reihenfolge des Desktops.</span><span class="sxs-lookup"><span data-stu-id="810d6-147">The Visual UIA Verify window remains at the top of the desktop z-order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="810d6-148"><strong>Hover-Modus (STRG verwenden)</strong></span><span class="sxs-lookup"><span data-stu-id="810d6-148"><strong>Hover Mode (Use Ctrl)</strong></span></span></td>
<td><span data-ttu-id="810d6-149">Wenn die STRG-Taste gedrückt wird, wird das-Element unter dem Maus Cursor als interessantes Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="810d6-149">When the Ctrl key is pressed, the element under the mouse cursor is identified as the element of interest.</span></span> <span data-ttu-id="810d6-150">Der Bereich <strong>Automatisierungs Element</strong> Struktur wird aktualisiert, und das entsprechende Element in der Elementliste wird hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="810d6-150">The <strong>Automation Elements Tree</strong> pane is refreshed and the corresponding item in the element list is highlighted.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="810d6-151"><strong>Fokusverfolgung</strong></span><span class="sxs-lookup"><span data-stu-id="810d6-151"><strong>Focus Tracking</strong></span></span></td>
<td><span data-ttu-id="810d6-152">Wenn sich der Fokus ändert, wird das Element mit dem Fokus als interessantes Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="810d6-152">As the focus changes, the element with the focus is identified as the element of interest.</span></span> <span data-ttu-id="810d6-153">Der Bereich <strong>Automatisierungs Element</strong> Struktur wird aktualisiert, und das entsprechende Element in der Elementliste wird hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="810d6-153">The <strong>Automation Elements Tree</strong> pane is refreshed and the corresponding item in the element list is highlighted.</span></span></td>

</tr>
<tr class="even">
<td rowspan="6"><span data-ttu-id="810d6-154"><strong>Tests</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="810d6-154"><strong>Tests</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="810d6-155"><strong>Nach links</strong></span><span class="sxs-lookup"><span data-stu-id="810d6-155"><strong>Go Left</strong></span></span></td>
<td><span data-ttu-id="810d6-156">Verschieben Sie einen Knoten nach links in der <strong>Test</strong> Struktur.</span><span class="sxs-lookup"><span data-stu-id="810d6-156">Move one node left in the <strong>Tests</strong> tree.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="810d6-157"><strong>Nach oben</strong></span><span class="sxs-lookup"><span data-stu-id="810d6-157"><strong>Go Up</strong></span></span></td>
<td><span data-ttu-id="810d6-158">Verschieben Sie einen Knoten in der <strong>Test</strong> Struktur nach oben.</span><span class="sxs-lookup"><span data-stu-id="810d6-158">Move one node up in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="810d6-159"><strong>Nach unten</strong></span><span class="sxs-lookup"><span data-stu-id="810d6-159"><strong>Go Down</strong></span></span></td>
<td><span data-ttu-id="810d6-160">Verschieben Sie einen Knoten in der <strong>Test</strong> Struktur nach unten.</span><span class="sxs-lookup"><span data-stu-id="810d6-160">Move one node down in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="810d6-161"><strong>Nach rechts</strong></span><span class="sxs-lookup"><span data-stu-id="810d6-161"><strong>Go Right</strong></span></span></td>
<td><span data-ttu-id="810d6-162">Verschieben Sie einen Knoten nach rechts in der <strong>Test</strong> Struktur.</span><span class="sxs-lookup"><span data-stu-id="810d6-162">Move one node right in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="810d6-163"><strong>Ausgewählte (r) Test (e) auf ausgewähltem Element ausführen</strong></span><span class="sxs-lookup"><span data-stu-id="810d6-163"><strong>Run Selected Test(s) On Selected Element</strong></span></span></td>
<td><span data-ttu-id="810d6-164">Führt die ausgewählten Tests aus der <strong>Test</strong> Struktur für das ausgewählte Element aus.</span><span class="sxs-lookup"><span data-stu-id="810d6-164">Run the selected tests from the <strong>Tests</strong> tree on the selected element.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="810d6-165"><strong>Bekannte Probleme Filtern</strong></span><span class="sxs-lookup"><span data-stu-id="810d6-165"><strong>Filter Known Problems</strong></span></span></td>
<td><span data-ttu-id="810d6-166">Filtern bekannter Benutzeroberflächenautomatisierungs-Fehler aus den Testergebnissen.</span><span class="sxs-lookup"><span data-stu-id="810d6-166">Filter known UI Automation bugs from the test results.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="810d6-167"><strong>Hilfe</strong></span><span class="sxs-lookup"><span data-stu-id="810d6-167"><strong>Help</strong></span></span></td>
<td><span data-ttu-id="810d6-168"><strong>Informationen zur Überprüfung der Benutzeroberflächen Automatisierung</strong></span><span class="sxs-lookup"><span data-stu-id="810d6-168"><strong>About Visual UI Automation Verify</strong></span></span></td>
<td><span data-ttu-id="810d6-169">Zeigen Sie die Softwareversion und die Copyright Informationen für Visual UIA-Überprüfung an.</span><span class="sxs-lookup"><span data-stu-id="810d6-169">Display the software version and copyright information for Visual UIA Verify.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="functional-panes"></a><span data-ttu-id="810d6-170">Funktionale Bereiche</span><span class="sxs-lookup"><span data-stu-id="810d6-170">Functional Panes</span></span>

<span data-ttu-id="810d6-171">In diesem Abschnitt werden die Funktionsbereiche in der Benutzeroberfläche der Visual UIA-Überprüfung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="810d6-171">This section describes the functional panes in the Visual UIA Verify user interface.</span></span>

-   [<span data-ttu-id="810d6-172">Bereich "Automatisierungselemente-Struktur"</span><span class="sxs-lookup"><span data-stu-id="810d6-172">Automation Elements Tree Pane</span></span>](#automation-elements-tree-pane)
-   [<span data-ttu-id="810d6-173">Bereich "Tests"</span><span class="sxs-lookup"><span data-stu-id="810d6-173">Tests Pane</span></span>](#tests-pane)
-   [<span data-ttu-id="810d6-174">Bereich „Testergebnisse“</span><span class="sxs-lookup"><span data-stu-id="810d6-174">Test Results Pane</span></span>](#test-results-pane)
-   [<span data-ttu-id="810d6-175">Eigenschaften Bereich</span><span class="sxs-lookup"><span data-stu-id="810d6-175">Properties Pane</span></span>](#properties-pane)

### <a name="automation-elements-tree-pane"></a><span data-ttu-id="810d6-176">Bereich "Automatisierungselemente-Struktur"</span><span class="sxs-lookup"><span data-stu-id="810d6-176">Automation Elements Tree Pane</span></span>

<span data-ttu-id="810d6-177">Der Bereich **Automatisierungselemente** -Struktur enthält eine hierarchische Momentaufnahme von Automation-Element Objekten, die für Tests verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="810d6-177">The **Automation Elements Tree** pane contains a hierarchical snapshot of automation element objects that are available for testing.</span></span> <span data-ttu-id="810d6-178">Das oberste Element in der Struktur stellt den Desktop dar.</span><span class="sxs-lookup"><span data-stu-id="810d6-178">The top element in the tree represents the desktop.</span></span>

<span data-ttu-id="810d6-179">Diese Sicht ist eine statische Auflistung, die kompiliert wird, wenn die Überprüfung der visuellen benutzerdefinierte Funktion gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="810d6-179">This view is a static collection that is compiled when Visual UIA Verify starts.</span></span> <span data-ttu-id="810d6-180">Zum Aktualisieren der Ansicht auf dem ausgewählten Knoten verwenden Sie den Menübefehl " **ausgewähltes Element aktualisieren** " oder die Symbolleisten Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="810d6-180">To refresh the view at the selected node, use the **Refresh Selected Element** menu command or toolbar button.</span></span>

<span data-ttu-id="810d6-181">Der folgende Screenshot zeigt den Strukturbereich **Automation-Elemente** .</span><span class="sxs-lookup"><span data-stu-id="810d6-181">The following screen shot shows the **Automation Elements Tree** pane.</span></span>

![Bereich "Automatisierungselemente" der visuellen UIA-Überprüfung](images/automation-elements-tree-pane.png)

<span data-ttu-id="810d6-183">Ein abgeblichter (nicht verfügbarer) Knoten in der **Automatisierungs Element** Struktur zeigt an, dass das Element ein Member der Benutzeroberflächenautomatisierungs-rohansicht ist, aber nicht den Bedingungen entspricht, die als Member der Inhaltsansicht oder Steuerelement Ansicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="810d6-183">A dimmed (unavailable) node in the **Automation Elements Tree** indicates that the element is a member of the UI Automation raw view, but does not meet the conditions necessary to be considered a member of the content view or control view.</span></span> <span data-ttu-id="810d6-184">Das-Element kann jedoch weiterhin über die Visual UI-Automatisierungs Überprüfung getestet werden.</span><span class="sxs-lookup"><span data-stu-id="810d6-184">However, the element can still be tested from Visual UI Automation Verify.</span></span> <span data-ttu-id="810d6-185">Weitere Informationen finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="810d6-185">For more information, see the [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

<span data-ttu-id="810d6-186">Folgende Befehle sind in der Struktur Symbolleiste der **Automatisierungselemente** verfügbar:</span><span class="sxs-lookup"><span data-stu-id="810d6-186">Commands available from the **Automation Elements Tree** toolbar include:</span></span>

-   <span data-ttu-id="810d6-187">**Aktualisieren**– den ausgewählten Knoten und seine untergeordneten Elemente aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="810d6-187">**Refresh**—Refresh the selected node and its children.</span></span> <span data-ttu-id="810d6-188">Dieser Befehl aktualisiert nicht die gesamte Elementstruktur, es sei denn, der Stamm Knoten ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="810d6-188">This command does not refresh the entire element tree unless the root node is selected.</span></span>
-   <span data-ttu-id="810d6-189">**Parent (STRG + UMSCHALT + F6)**– wechselt zum übergeordneten Element des aktuellen Knotens.</span><span class="sxs-lookup"><span data-stu-id="810d6-189">**Parent (Ctrl+Shift+F6)**—Go to parent of the current node.</span></span>
-   <span data-ttu-id="810d6-190">**First Child (STRG + UMSCHALT + F7)**– wechselt zum ersten untergeordneten Element des aktuellen Knotens.</span><span class="sxs-lookup"><span data-stu-id="810d6-190">**First Child (Ctrl+Shift+F7)**—Go to first child of the current node..</span></span>
-   <span data-ttu-id="810d6-191">**Nächstes neben geordnetes Element (STRG + UMSCHALT + F8)**– wechselt zum nächsten neben geordneten Element des aktuellen Knotens.</span><span class="sxs-lookup"><span data-stu-id="810d6-191">**Next Sibling (Ctrl+Shift+F8)**—Go to next sibling child of the current node.</span></span>
-   <span data-ttu-id="810d6-192">**Vorheriges gleich geordnetes Element (STRG + UMSCHALT + F9)**– wechselt zum vorherigen gleich geordneten Element des aktuellen Knotens.</span><span class="sxs-lookup"><span data-stu-id="810d6-192">**Previous Sibling (Ctrl+Shift+F9)**—Go to previous sibling of the current node.</span></span>
-   <span data-ttu-id="810d6-193">**Last Child (STRG + UMSCHALT + F10)**– wechselt zum letzten untergeordneten Element des aktuellen Knotens.</span><span class="sxs-lookup"><span data-stu-id="810d6-193">**Last Child (Ctrl+Shift+F10)**—Go to last child of the current node.</span></span>
-   <span data-ttu-id="810d6-194">**Fokusverfolgung**– aktivieren oder deaktivieren Sie die Knoten Auswahl basierend auf der Fokusverfolgung.</span><span class="sxs-lookup"><span data-stu-id="810d6-194">**Focus Tracking**—Toggle node selection on or off based on focus tracking.</span></span>

### <a name="tests-pane"></a><span data-ttu-id="810d6-195">Bereich "Tests"</span><span class="sxs-lookup"><span data-stu-id="810d6-195">Tests Pane</span></span>

<span data-ttu-id="810d6-196">Der Bereich **Tests** enthält eine Liste von Tests der Benutzeroberflächen Automatisierung, geordnet nach Testtyp (**Automatisierungs Element**, **Steuer** Element und **Muster**) und Priorität (**Buildüberprüfung**, **Priorität 0**, **Priorität 1**, **Priorität 2** und **Priorität 3**).</span><span class="sxs-lookup"><span data-stu-id="810d6-196">The **Tests** pane contains a list of UI Automation tests organized by test type (**Automation Element**, **Control**, and **Pattern**) and priority (**Build Verification**, **Priority 0**, **Priority 1**, **Priority 2**, and **Priority 3**).</span></span> <span data-ttu-id="810d6-197">Diese Liste wird basierend auf dem Steuer Elementtyp des ausgewählten Elements im Strukturbereich **Automation-Elemente** generiert.</span><span class="sxs-lookup"><span data-stu-id="810d6-197">This list is generated based on the control type of the selected element in the **Automation Elements Tree** pane.</span></span> <span data-ttu-id="810d6-198">Weitere Informationen finden Sie unter [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="810d6-198">For more information, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

<span data-ttu-id="810d6-199">Der folgende Screenshot zeigt den Bereich **Tests** .</span><span class="sxs-lookup"><span data-stu-id="810d6-199">The following screen shot shows the **Tests** pane.</span></span>

![Testbereich](images/test-pane.png)

<span data-ttu-id="810d6-201">Folgende Befehle sind auf der Symbolleiste " **Tests** " verfügbar:</span><span class="sxs-lookup"><span data-stu-id="810d6-201">Commands available from the **Tests** toolbar include:</span></span>

-   <span data-ttu-id="810d6-202">Show – gibt die **anzuzeigenden** Benutzeroberflächenautomatisierungs-Tests an; Das heißt, alle Tests oder nur Tests, die für den Steuer Elementtyp des ausgewählten Elements in der Struktur der **Automatisierungselemente** geeignet sind (Standard).</span><span class="sxs-lookup"><span data-stu-id="810d6-202">**Show**—Specifies the UI Automation tests to display; that is, display all tests or only tests suited to the control type of the selected element in the **Automation Elements Tree** (default).</span></span>
-   <span data-ttu-id="810d6-203">Type – gibt die **anzuzeigenden** Testtypen an: **Automation-Element**,- **Muster** oder- **Steuer** Element.</span><span class="sxs-lookup"><span data-stu-id="810d6-203">**Type**—Specifies the test types to display: **Automation Element**, **Pattern**, or **Control**.</span></span>
-   <span data-ttu-id="810d6-204">**Prioritäten**– gibt die anzuzeigenden Test Prioritäten an: **Buildüberprüfung**, **Priorität 0**, **Priorität 1**, **Priorität 2** oder **Priorität 3**.</span><span class="sxs-lookup"><span data-stu-id="810d6-204">**Priorities**—Specifies the test priorities to display: **Build Verification**, **Priority 0**, **Priority 1**, **Priority 2**, or **Priority 3**.</span></span>
-   <span data-ttu-id="810d6-205">**Gehe zu Links**– wechselt zum übergeordneten Knoten des aktuellen Knotens.</span><span class="sxs-lookup"><span data-stu-id="810d6-205">**Go Left**—Go to the parent of the current node.</span></span>
-   <span data-ttu-id="810d6-206">Nach **oben**– wechselt zum vorherigen gleich geordneten Element des aktuellen Knotens.</span><span class="sxs-lookup"><span data-stu-id="810d6-206">**Go Up**—Go to the previous sibling of the current node.</span></span>
-   <span data-ttu-id="810d6-207">Nach **unten**– gehe zum nächsten neben geordneten Element des aktuellen Knotens.</span><span class="sxs-lookup"><span data-stu-id="810d6-207">**Go Down**—Go to the next sibling of the current node.</span></span>
-   <span data-ttu-id="810d6-208">**Go Right**– wechselt zum ersten untergeordneten Element des aktuellen Knotens.</span><span class="sxs-lookup"><span data-stu-id="810d6-208">**Go Right**—Go to the first child of the current node.</span></span>
-   <span data-ttu-id="810d6-209">**Ausgewählte Test (e) ausführen**– führt die Tests für das in der Struktur der **Automatisierungselemente** ausgewählte Element aus.</span><span class="sxs-lookup"><span data-stu-id="810d6-209">**Run Selected Test(s)**—Runs the tests on the element selected in the **Automation Elements Tree**.</span></span>

### <a name="test-results-pane"></a><span data-ttu-id="810d6-210">Bereich „Testergebnisse“</span><span class="sxs-lookup"><span data-stu-id="810d6-210">Test Results Pane</span></span>

<span data-ttu-id="810d6-211">Der Bereich **Testergebnisse** enthält die Funktion zur Überprüfung der Visual UIA-Protokollierung.</span><span class="sxs-lookup"><span data-stu-id="810d6-211">The **Test Results** pane contains the Visual UIA Verify logging functionality.</span></span> <span data-ttu-id="810d6-212">Der folgende Screenshot zeigt den **Testergebnisse** Bereich.</span><span class="sxs-lookup"><span data-stu-id="810d6-212">The following screen shot shows the **Test Results** pane.</span></span>

![Bereich "Testergebnisse"](images/test-results-pane.png)

<span data-ttu-id="810d6-214">Folgende Befehle sind in der **Testergebnis** Symbolleiste verfügbar:</span><span class="sxs-lookup"><span data-stu-id="810d6-214">Commands available from the **Tests Results** toolbar include:</span></span>

-   <span data-ttu-id="810d6-215">**Zurück**– Seiten rückwärts in Berichts Anzeige Verlauf.</span><span class="sxs-lookup"><span data-stu-id="810d6-215">**Back**—Page backward in report viewing history.</span></span>
-   <span data-ttu-id="810d6-216">**Forward**– Seiten vorwärts im Berichts Anzeige Verlauf.</span><span class="sxs-lookup"><span data-stu-id="810d6-216">**Forward**—Page forward in report viewing history.</span></span>
-   <span data-ttu-id="810d6-217">**Insgesamt**– zeigt eine Zusammenfassung der Testergebnisse an(bestanden **,** Fehler und **unerwarteter Fehler**).</span><span class="sxs-lookup"><span data-stu-id="810d6-217">**Overall**—Displays a summary of the test results (**Passed**, **Failed**, and **Unexpected Error**).</span></span> <span data-ttu-id="810d6-218">Das Testergebnis ist mit der Ansicht **alle Ergebnisse** verknüpft.</span><span class="sxs-lookup"><span data-stu-id="810d6-218">The test result is linked to the **All Results** view.</span></span> <span data-ttu-id="810d6-219">Der Befehl " **Gesamt** " zeigt eine Tabelle wie die folgende an.</span><span class="sxs-lookup"><span data-stu-id="810d6-219">The **Overall** command displays a table like the following one.</span></span>

    ![Tabelle für allgemeine Testergebnisse](images/overall-test-results.png)

-   <span data-ttu-id="810d6-221">**Alle Ergebnisse**– zeigt ein detailliertes Protokoll für jedes Testergebnis an, wie in den folgenden Tabellen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="810d6-221">**All Results**— Displays a detailed log for each test result, as shown in the following tables.</span></span>

    ![Beispiel für Protokoll Ergebnis Details aus der Ansicht "alle Ergebnisse"](images/all-results-log.png)

    <span data-ttu-id="810d6-223">Der Testname in der Tabelle **alle Ergebnisse** wird mit einer Test Fallbeschreibung für das-Element verknüpft, wie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="810d6-223">The test name in the **All Results** table is linked to a test case description for the element, as in the following table.</span></span>

    ![Test Fall Details](images/test-case-detail.png)

-   <span data-ttu-id="810d6-225">**Full Log**– zeigt eine Alternative Ansicht des detaillierten Protokolls für jedes Testergebnis an, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="810d6-225">**Full Log**—Displays an alternate view of the detailed log for each test result, as shown in the following screen shot.</span></span>

    ![Alternative Ansicht eines Test Fall Details](images/alt-view-of-test-case-detail.png)

-   <span data-ttu-id="810d6-227">**XML**– zeigt das von der XML-Protokollierung generierte unformatierte XML an.</span><span class="sxs-lookup"><span data-stu-id="810d6-227">**XML**—Displays the raw XML generated by the XML logger.</span></span>
-   <span data-ttu-id="810d6-228">**Schnell** Suche – einfache Text Suche der aktuellen Ansicht im **Testergebnisse** Bereich.</span><span class="sxs-lookup"><span data-stu-id="810d6-228">**Quick Find**—Simple text search of the current view in the **Test Results** pane.</span></span>
-   <span data-ttu-id="810d6-229">**In neuem Fenster öffnen**– öffnet die aktuelle Ansicht in einer neuen Instanz von Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="810d6-229">**Open in New Window**—Opens the current view in a new instance of Internet Explorer.</span></span>

### <a name="properties-pane"></a><span data-ttu-id="810d6-230">Eigenschaftenbereich</span><span class="sxs-lookup"><span data-stu-id="810d6-230">Properties Pane</span></span>

<span data-ttu-id="810d6-231">Der **Eigenschaften** Bereich enthält eine Liste der Benutzeroberflächenautomatisierungs-Eigenschaften und Eigenschaftswerte, geordnet nach Eigenschaftentyp: **Allgemeine Barrierefreiheit**, **Identifikation**, **Muster** (Steuerelement Muster), **Status** und **Sichtbarkeit**.</span><span class="sxs-lookup"><span data-stu-id="810d6-231">The **Properties** pane contains a list of UI Automation properties and property values organized by property type: **General Accessibility**, **Identification**, **Patterns** (control patterns), **State**, and **Visibility**.</span></span> <span data-ttu-id="810d6-232">Die Eigenschaftswerte werden basierend auf dem Steuerelement des im Strukturbereich **Automation-Elemente** ausgewählten Objekts dynamisch aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="810d6-232">The property values are dynamically populated based on the control type of the object selected in the **Automation Elements Tree** pane.</span></span> <span data-ttu-id="810d6-233">Der folgende Screenshot zeigt den Bereich **Eigenschaften** .</span><span class="sxs-lookup"><span data-stu-id="810d6-233">The following screen shot shows the **Properties** pane.</span></span>

![Eigenschaften Bereich](images/properties-pane.png)

<span data-ttu-id="810d6-235">Wenn das ausgewählte Steuerelement ein bestimmtes Steuerelement Muster unterstützt, bietet Visual UIA Verify die Möglichkeit, Methoden aufzurufen, die von diesem Steuerelement Muster unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="810d6-235">If the selected control supports a specific control pattern, Visual UIA Verify provides the ability to call methods that are supported by that control pattern.</span></span> <span data-ttu-id="810d6-236">Beispielsweise unterstützt der [Fenster Steuer](uiauto-supportwindowcontroltype.md) Element-Typ das [Window-Steuerelement Muster](uiauto-implementingwindow.md), das über eine [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) -Methode verfügt, die im Bereich **Eigenschaften** aufgerufen werden kann, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="810d6-236">For example, the [Window control type](uiauto-supportwindowcontroltype.md) supports the [Window control pattern](uiauto-implementingwindow.md), which has a [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) method that can be invoked from the **Properties** pane, as shown in the following screen shot.</span></span> <span data-ttu-id="810d6-237">Weitere Informationen finden Sie unter [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="810d6-237">For more information, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

![Close-Methode des Window-Steuerelement Musters, das im Bereich "Eigenschaften" aufgerufen wird](images/close-invoked-from-properties-pane.png)

<span data-ttu-id="810d6-239">Folgende Befehle sind auf der **Eigenschaften** Symbolleiste verfügbar:</span><span class="sxs-lookup"><span data-stu-id="810d6-239">Commands available from the **Properties** toolbar include:</span></span>

-   <span data-ttu-id="810d6-240">**Aktualisieren**– aktualisieren Sie die **Eigenschaften** Struktur.</span><span class="sxs-lookup"><span data-stu-id="810d6-240">**Refresh**—Refresh the **Properties** tree.</span></span>
-   <span data-ttu-id="810d6-241">**Alle erweitern**– erweitert alle Knoten in der **Eigenschaften** Struktur.</span><span class="sxs-lookup"><span data-stu-id="810d6-241">**Expand All**—Expands all nodes in the **Properties** tree.</span></span>

 

 




