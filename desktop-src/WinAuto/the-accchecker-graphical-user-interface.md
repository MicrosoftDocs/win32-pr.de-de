---
title: Die grafische Benutzeroberfläche der Zugriffs Überprüfung
description: In diesem Thema werden die Elemente beschrieben, aus denen die Benutzeroberfläche für die Zugriffs Prüfung besteht.
ms.assetid: C8C156F6-AB29-4011-9DCD-74261AC17404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26d847d1bc198958ca28dd77d67b0e99b9d7745
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "104562106"
---
# <a name="the-accchecker-graphical-user-interface"></a><span data-ttu-id="5125f-103">Die grafische Benutzeroberfläche der Zugriffs Überprüfung</span><span class="sxs-lookup"><span data-stu-id="5125f-103">The AccChecker Graphical User Interface</span></span>

<span data-ttu-id="5125f-104">In diesem Thema werden die Elemente beschrieben, aus denen die Benutzeroberfläche für die Zugriffs Prüfung besteht.</span><span class="sxs-lookup"><span data-stu-id="5125f-104">This topic describes the elements that make up the AccChecker GUI.</span></span>

-   [<span data-ttu-id="5125f-105">Registerkarte Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="5125f-105">Verifications Tab</span></span>](#verifications-tab)
-   [<span data-ttu-id="5125f-106">Registerkarte „Ergebnisse“</span><span class="sxs-lookup"><span data-stu-id="5125f-106">Results Tab</span></span>](#results-tab)
-   [<span data-ttu-id="5125f-107">MSAA-und UIA-Bildschirm Lese Registerkarten</span><span class="sxs-lookup"><span data-stu-id="5125f-107">MSAA and UIA Screen Reader Tabs</span></span>](#msaa-and-uia-screen-reader-tabs)
-   [<span data-ttu-id="5125f-108">Registerkarten für MSAA und UIA-Struktur</span><span class="sxs-lookup"><span data-stu-id="5125f-108">MSAA and UIA Tree Tabs</span></span>](#msaa-and-uia-tree-tabs)
-   [<span data-ttu-id="5125f-109">Menü "Datei"</span><span class="sxs-lookup"><span data-stu-id="5125f-109">File Menu</span></span>](#file-menu)
-   [<span data-ttu-id="5125f-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5125f-110">Related topics</span></span>](#related-topics)

## <a name="verifications-tab"></a><span data-ttu-id="5125f-111">Registerkarte Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="5125f-111">Verifications Tab</span></span>

<span data-ttu-id="5125f-112">Die Zugriffs Prüfung wird mit der Standardansicht der Registerkarte über **Prüfungen** gestartet:</span><span class="sxs-lookup"><span data-stu-id="5125f-112">AccChecker starts with the default view of the **Verifications** tab:</span></span>

![Screenshot, der die Registerkarte "verifications" in der eingabezugriffsüberprüfung von U I anzeigt](images/accchecker-verifications-tab.png)

<span data-ttu-id="5125f-114">Die Registerkarte über **Prüfungen** enthält die folgenden Komponenten.</span><span class="sxs-lookup"><span data-stu-id="5125f-114">The **Verifications** tab contains the following components.</span></span>

-   <span data-ttu-id="5125f-115">**Überprüfungs Zielauswahl** Bietet die folgenden Optionen für die Auswahl einer Zielanwendung oder eines-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="5125f-115">**Verification target selector** Offers the following options for selecting a target application or control.</span></span>
    -   <span data-ttu-id="5125f-116">Wählen Sie ein Ziel aus der vordefinierten Dropdown Liste aus.</span><span class="sxs-lookup"><span data-stu-id="5125f-116">Choose a target from the pre-populated drop-down list.</span></span> <span data-ttu-id="5125f-117">Diese Liste enthält alle HWNDs der obersten Ebene, die beim Start identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="5125f-117">This list contains all top-level HWNDs identified at start-up.</span></span>
    -   <span data-ttu-id="5125f-118">Wählen Sie ein HWND basierend auf der Position des Mauszeigers aus (auswählbare Steuerelemente werden mit einem roten Rechteck hervorgehoben).</span><span class="sxs-lookup"><span data-stu-id="5125f-118">Choose an HWND based on the location of the mouse cursor (selectable controls are highlighted with a red rectangle).</span></span> <span data-ttu-id="5125f-119">Mit dieser Option können Sie ein beliebiges sichtbares Objekt auswählen, das über ein HWND verfügt.</span><span class="sxs-lookup"><span data-stu-id="5125f-119">This option lets you select any visible object that has an HWND.</span></span>
    -   <span data-ttu-id="5125f-120">Geben Sie ein bestimmtes HWND ein.</span><span class="sxs-lookup"><span data-stu-id="5125f-120">Enter a particular HWND.</span></span>
-   <span data-ttu-id="5125f-121">**Checkliste für Überprüfungs Routinen** Bietet die Möglichkeit, die gewünschte Überprüfungs Routine auszuwählen, die für eine Anwendung oder ein Steuerelement ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5125f-121">**Verification routines checklist** Provides the ability to select the desired verification routine to be performed against an application or control.</span></span> <span data-ttu-id="5125f-122">Weitere Informationen finden Sie unter Überprüfungs Routinen.</span><span class="sxs-lookup"><span data-stu-id="5125f-122">See Verification Routines for more information.</span></span>
-   <span data-ttu-id="5125f-123">**Fehler-und Warnungs Unterdrückungs Dateiauswahl** Unterdrückungs Dateien werden auf der Registerkarte Überprüfungs **Ergebnisse** generiert. Wenn Sie mit der rechten Maustaste auf einen Fehler oder eine Warnmeldung Klicken und im Kontextmenü unter **drücken** auswählen, wird für diese Nachricht ein Flag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5125f-123">**Error and warning suppression file selector** Suppression files are generated from the verification **Results** tab. By right-clicking an error or warning message and selecting **Suppress** from the context menu, a flag is set for that message.</span></span> <span data-ttu-id="5125f-124">Wenn das Kontrollkästchen **Unterdrückungen** aktiviert ist, werden unterdrückte Einträge in der Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5125f-124">If the **Suppressions** check box is checked, suppressed entries appear in the list.</span></span> <span data-ttu-id="5125f-125">Ein unterdrückter Eintrag kann unterdrückt werden, indem das gleiche Kontextmenü verwendet wird, um ihn zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="5125f-125">A suppressed entry can be unsuppressed by using the same context menu used to suppress it.</span></span>

    <span data-ttu-id="5125f-126">Eine Unterdrückungs Datei wird im XML-Format gespeichert, indem im Menü **Datei** die Option **Unterdrückung speichern** ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="5125f-126">A suppression file is saved in XML format by selecting **Save Suppression** from the **File** menu.</span></span> <span data-ttu-id="5125f-127">Diese Datei wird bei nachfolgenden Überprüfungs Läufen verwendet, bei denen die Nachrichten ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="5125f-127">This file is consumed on subsequent verification runs where the messages will be hidden.</span></span> <span data-ttu-id="5125f-128">Um die Unterdrückungs Datei zu entfernen, klicken Sie auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="5125f-128">To remove the suppression file, click **Clear**.</span></span> <span data-ttu-id="5125f-129">Informationen zu bestimmten Nachrichten finden Sie unter Verifizierungsprotokoll Meldungen.</span><span class="sxs-lookup"><span data-stu-id="5125f-129">For information on specific messages, see Verification Log Messages.</span></span> <span data-ttu-id="5125f-130">Verwenden Sie im Menü **Datei** die Option **Protokoll speichern** , um die gesamte Liste als Protokolldatei in XML oder als formatierte Textdatei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5125f-130">Use **Save Log** from the **File** menu to save the entire list as a log file in XML or as a formatted text file.</span></span>

    ![Registerkarte "accchecker-Ergebnisse" mit hervorgehobenem Kontext Element](images/accchecker-results-tab-with-suppress.png)

    <span data-ttu-id="5125f-132">Das folgende Beispiel zeigt den Inhalt einer Unterdrückungs Datei, die durch Ausführen der **Eigenschaften** Überprüfungen in der System Steuerungsanwendung der Windows-Firewall generiert wird.</span><span class="sxs-lookup"><span data-stu-id="5125f-132">The following example shows the content of a suppression file generated by running the **Properties** verifications on the Windows Firewall control panel application.</span></span> <span data-ttu-id="5125f-133">Der Fehler mit der ID "elementhasnoname" wurde in diesem Beispiel zur Unterdrückung ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="5125f-133">The error with an ID of "ElementHasNoName" was chosen for suppression in this example.</span></span>

    ```XML
    <?xml version="1.0" encoding="utf-8"?><ArrayOfLogEvent xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema">
      <LogEvent>
        <EventID>ElementHasNoName</EventID>
        <Text>Element has no name</Text>
        <ParentChain>Windows Firewall.Windows Firewall</ParentChain>
        <VerificationRoutine>VerificationRoutines.CheckName</VerificationRoutine>
        <Classname>ATL:BUTTON</Classname>
        <AccName />
        <AccRole>PushButton</AccRole>
      </LogEvent>
    </ArrayOfLogEvent>
    ```

    

-   <span data-ttu-id="5125f-134">**Priorisierte Ergebnisse anzeigen** Bietet die folgenden Optionen zum Filtern der Überprüfungs Ergebnisse nach Priorität.</span><span class="sxs-lookup"><span data-stu-id="5125f-134">**Show prioritized results** Offers the following options for filtering the verification results by priority.</span></span>
    -   <span data-ttu-id="5125f-135">**Alle** Alle Ergebnisse unabhängig von der Priorität einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="5125f-135">**All** Include all all results regardless of priority.</span></span>
    -   <span data-ttu-id="5125f-136">**Nur P1** Nur Ergebnisse mit Priorität 0 und Priorität 1 einschließen.</span><span class="sxs-lookup"><span data-stu-id="5125f-136">**P1 only** Include only priority 0 and priority 1 results.</span></span>
    -   <span data-ttu-id="5125f-137">**Nur P1 P2** Ergebnisse mit Priorität 0 und Priorität 2 einschließen.</span><span class="sxs-lookup"><span data-stu-id="5125f-137">**P1   P2 only** Include priority 0 through priority 2 results.</span></span>
-   <span data-ttu-id="5125f-138">**Ausgewählte Verifizierungen ausführen** Stellt die Schaltfläche über **Prüfungen ausführen** zum Starten des Überprüfungsprozesses bereit.</span><span class="sxs-lookup"><span data-stu-id="5125f-138">**Run selected verifications** Provides the **Run Verifications** button for starting the verification process.</span></span> <span data-ttu-id="5125f-139">Während die Überprüfung ausgeführt wird, ändert sich die Schaltfläche, um über **Prüfungen abzubrechen** , und kann verwendet werden, um die Überprüfungen zu beenden, nachdem der aktuelle abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="5125f-139">While verifications are running, the button changes to **Cancel Verifications** and can be used to stop the verifications after the current one completes.</span></span>

## <a name="results-tab"></a><span data-ttu-id="5125f-140">Registerkarte "Ergebnisse"</span><span class="sxs-lookup"><span data-stu-id="5125f-140">Results Tab</span></span>

<span data-ttu-id="5125f-141">Die Registerkarte **Ergebnisse** wird aufgefüllt, nachdem die ausgewählten Überprüfungs Aufgaben fertiggestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="5125f-141">The **Results** tab is populated after the selected verification tasks are complete.</span></span> <span data-ttu-id="5125f-142">Sie besteht aus den folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="5125f-142">It consists of the following components.</span></span>

-   <span data-ttu-id="5125f-143">Die Meldungs Liste, in der die Fehler-, Warnungs-und Informationsmeldungen angezeigt werden, die von den ausgewählten Überprüfungs Tasks generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="5125f-143">The message list, which displays the error, warning, and informational messages generated by the selected verification tasks.</span></span> <span data-ttu-id="5125f-144">Die angezeigten Meldungen können mithilfe der Kontrollkästchen oberhalb der Meldungs Liste nach Typ gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="5125f-144">The messages displayed can be filtered by type using the checkboxes above the message list.</span></span>
-   <span data-ttu-id="5125f-145">Die Nachrichten Details und eine Bildschirmaufnahme des Überprüfungs Ziels.</span><span class="sxs-lookup"><span data-stu-id="5125f-145">The message details and a screen capture of the verification target.</span></span> <span data-ttu-id="5125f-146">Wenn Sie eine Meldung aus der Liste Nachricht auswählen, werden weitere Details angezeigt, und das entsprechende Element wird im Bereich Bildschirmaufnahme hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="5125f-146">Selecting a message from the message list displays further details and highlights the corresponding element in the screen capture pane.</span></span> <span data-ttu-id="5125f-147">Die Schaltfläche **visualisieren** , schaltet die Zugriffstaste auf die Registerkarte **MSAA** -Struktur. Wenn ein Fehler auf der Registerkarte **Ergebnisse** hervorgehoben ist, wird das entsprechende Element auf der Registerkarte **MSAA** -Struktur hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="5125f-147">The **Visualize** button, switches AccChecker to the **MSAA Tree** tab. If an error is highlighted on the **Results** tab, the corresponding element is highlighted on the **MSAA Tree** tab.</span></span>

<span data-ttu-id="5125f-148">Wenn Sie mit der rechten Maustaste auf eine Nachricht klicken, wird ein Kontextmenü mit den folgenden Elementen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5125f-148">Right-clicking on a message exposes a context menu with the following items.</span></span>

-   <span data-ttu-id="5125f-149">Unter **drücken** Fügt die Meldung der Unterdrückungs Liste hinzu.</span><span class="sxs-lookup"><span data-stu-id="5125f-149">**Suppress** Adds the message to the suppression list.</span></span>
-   <span data-ttu-id="5125f-150">**In Zwischenablage kopieren** Kopiert die Nachrichten Details in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="5125f-150">**Copy to clipboard** Copies the message details to the clipboard.</span></span>
-   <span data-ttu-id="5125f-151">**Visualisieren** Schaltet die Zugriffstaste auf die Registerkarte **MSAA** -Struktur. Das Element, das dem ausgewählten Fehler entspricht, wird hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="5125f-151">**Visualize** Switches AccChecker to the **MSAA Tree** tab. The element that corresponds to the selected error is highlighted.</span></span>
-   <span data-ttu-id="5125f-152">**Hilfe** Zeigt zusätzliche Informationen zur Meldung an.</span><span class="sxs-lookup"><span data-stu-id="5125f-152">**Help** Displays additional information about the message.</span></span>

## <a name="msaa-and-uia-screen-reader-tabs"></a><span data-ttu-id="5125f-153">MSAA-und UIA-Bildschirm Lese Registerkarten</span><span class="sxs-lookup"><span data-stu-id="5125f-153">MSAA and UIA Screen Reader Tabs</span></span>

<span data-ttu-id="5125f-154">Die Registerkarten "MSAA Screen Reader" und "UIA Screen Reader" ähneln einander.</span><span class="sxs-lookup"><span data-stu-id="5125f-154">The MSAA Screen reader and the UIA Screen reader tabs are similar.</span></span> <span data-ttu-id="5125f-155">Beide zeigen eine Aufzeichnung von Elementen an, die in einem simulierten Durchlauf des Überprüfungs Ziels durch eine Bildschirm Sprachausgabe gefunden wurden, mit dem Unterschied, dass die MSAA-Implementierung und die andere die UIA-Implementierung anzeigt.</span><span class="sxs-lookup"><span data-stu-id="5125f-155">Both display a transcript of elements encountered in a simulated traversal of the verification target by a screen reader, except that one shows the MSAA implementation, and the other shows the UIA implemention.</span></span>

<span data-ttu-id="5125f-156">Elemente werden navigiert und protokolliert, so wie Sie von einer Bildschirmausgabe gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="5125f-156">Elements are navigated and logged just as a screen reader would read them.</span></span> <span data-ttu-id="5125f-157">Die auf dieser Registerkarte dargestellten Informationen sind wichtig, um zu bestätigen, dass nur nützliche und relevante Informationen angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="5125f-157">The information presented on this tab is essential to confirm that only useful and relevant information is being announced.</span></span> <span data-ttu-id="5125f-158">Beispielsweise ist ein normaler Name eines Steuer Elements, z. b. "MenuItem Edit" oder "Push Button Close", zulässig. ein Steuerelement Name, der nicht sinnvoll ist, z. b. "CPNavPanel22" oder "DefaultValue1", ist jedoch nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="5125f-158">For example, a normal-sounding control name such as "MenuItem Edit" or "PushButton Close" is acceptable; however, a control name that doesn't make sense, such as "CPNavPanel22" or "DefaultValue1", is not acceptable.</span></span> <span data-ttu-id="5125f-159">Die Schaltfläche **visualisieren** bewirkt, dass die Zugriffs Prüfung zur Registerkarte **MSAA** -Struktur oder **UIA** -Struktur wechselt. Wenn ein Element auf der Registerkarte **Bildschirmleser** hervorgehoben ist, wird das entsprechende Element auf der Registerkarte **MSAA** -Struktur oder **UIA** -Struktur hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="5125f-159">The **Visualize** button, causes AccChecker to switch to the **MSAA Tree** or **UIA Tree** tab. If an element is highlighted on the **Screen Reader** tab, the corresponding element is highlighted on the **MSAA Tree** or **UIA Tree** tab.</span></span>

<span data-ttu-id="5125f-160">Die **Screenreader** -Überprüfungs Routine **muss auf** der Registerkarte über **Prüfungen** ausgewählt sein, damit die **Registerkarte "MSAA-Bildschirmleser** " angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5125f-160">The **ScreenReader** verification routine under **Consistence** must be selected in the **Verifications** tab for the **MSAA Screen reader tab** to be displayed.</span></span> <span data-ttu-id="5125f-161">Ebenso muss die **uiaskreeinreader** -Überprüfungs Routine ausgewählt werden, damit die Registerkarte " **UIA-Bildschirmleser** " angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5125f-161">Similarly, the **UiaScreenReader** verification routine must be selected for the **UIA Screen reader** tab to be displayed.</span></span>

<span data-ttu-id="5125f-162">Der folgende Screenshot zeigt die Registerkarte "User Screen Reader" (UIA) mit einer Beispiel Überprüfung von Notepad.</span><span class="sxs-lookup"><span data-stu-id="5125f-162">The following screen shot shows the UIA Screen reader tab with a sample verification of Notepad.</span></span>

![Bildschirm Lese Registerkarte "accchecker" zeigt Beispiel Überprüfungs Ergebnisse an](images/accchecker-screen-reader-tab.png)

## <a name="msaa-and-uia-tree-tabs"></a><span data-ttu-id="5125f-164">Registerkarten für MSAA und UIA-Struktur</span><span class="sxs-lookup"><span data-stu-id="5125f-164">MSAA and UIA Tree Tabs</span></span>

<span data-ttu-id="5125f-165">Das Ausführen einer Überprüfungs Routine bewirkt, dass accchecker alle sichtbaren Elemente im Überprüfungs Ziel kompiliert und hierarchisch auf der Registerkarte " **MSAA** -Struktur" und der Registerkarte " **UIA** -Struktur" anzeigt. Der folgende Screenshot zeigt die Registerkarte MSAA-Struktur mit der Hierarchie der Elemente für Notepad.</span><span class="sxs-lookup"><span data-stu-id="5125f-165">Running any verification routine causes AccChecker to compile all visible elements in the verification target and display them hierarchically on the **MSAA Tree** tab and the **UIA Tree** tab. The following screen shot shows the MSAA Tree tab with the hierarchy of elements for Notepad.</span></span>

![Registerkarte "accchecker-Struktur"](images/accchecker-tree-tab.png)

## <a name="file-menu"></a><span data-ttu-id="5125f-167">Menü „Datei“</span><span class="sxs-lookup"><span data-stu-id="5125f-167">File Menu</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5125f-168">Menü</span><span class="sxs-lookup"><span data-stu-id="5125f-168">Menu</span></span></th>
<th><span data-ttu-id="5125f-169">Get-Help</span><span class="sxs-lookup"><span data-stu-id="5125f-169">Command</span></span></th>
<th><span data-ttu-id="5125f-170">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5125f-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="5"><span data-ttu-id="5125f-171"><strong>Datei</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="5125f-171"><strong>File</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="5125f-172"><strong>Öffnen</strong></span><span class="sxs-lookup"><span data-stu-id="5125f-172"><strong>Open</strong></span></span></td>
<td><span data-ttu-id="5125f-173">Bietet die folgenden Optionen.</span><span class="sxs-lookup"><span data-stu-id="5125f-173">Provides the following options.</span></span><br/>
<ul>
<li><span data-ttu-id="5125f-174"><strong>Verifications-dll</strong> Öffnet eine Überprüfungs-dll.</span><span class="sxs-lookup"><span data-stu-id="5125f-174"><strong>Verifications DLL</strong> Opens a verification DLL.</span></span> <span data-ttu-id="5125f-175">Native accchecker-Verifizierungen werden in einer eigenständigen dll (VerificationRoutines.dll) gekapselt.</span><span class="sxs-lookup"><span data-stu-id="5125f-175">Native AccChecker verifications are encapsulated in a standalone DLL (VerificationRoutines.dll).</span></span> <span data-ttu-id="5125f-176">Mit diesem Entwurf können Testteams basierend auf der UI-Plattform, die getestet wird, ihren eigenen Satz von Überprüfungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="5125f-176">This design allows test teams to create their own set of verifications based on the UI platform being tested.</span></span></li>
<li><span data-ttu-id="5125f-177"><strong>Protokolldatei</strong> Ermöglicht das Auswählen einer zu öffnenden Überprüfungsprotokoll Datei.</span><span class="sxs-lookup"><span data-stu-id="5125f-177"><strong>Log file</strong> Lets you choose a verification log file to open.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5125f-178"><strong>Verfügbare Überprüfungen automatisch laden</strong></span><span class="sxs-lookup"><span data-stu-id="5125f-178"><strong>Automatically load available verifications</strong></span></span></td>
<td><span data-ttu-id="5125f-179">Alle verfügbaren accessüberprüfungs Überprüfungen werden automatisch geladen.</span><span class="sxs-lookup"><span data-stu-id="5125f-179">Automatically loads all available AccChecker verifications.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5125f-180"><strong>Protokoll speichern</strong></span><span class="sxs-lookup"><span data-stu-id="5125f-180"><strong>Save Log</strong></span></span></td>
<td><span data-ttu-id="5125f-181">Speichern Sie das Überprüfungsprotokoll als XML oder als Klartext.</span><span class="sxs-lookup"><span data-stu-id="5125f-181">Save the verification log as XML or as plain text.</span></span> <span data-ttu-id="5125f-182">Nur-Text ist besser lesbar.</span><span class="sxs-lookup"><span data-stu-id="5125f-182">Plain text is more readable.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5125f-183"><strong>Unterdrückung speichern</strong></span><span class="sxs-lookup"><span data-stu-id="5125f-183"><strong>Save Suppression</strong></span></span></td>
<td><span data-ttu-id="5125f-184">Speichern Sie das Unterdrückungs Protokoll als XML.</span><span class="sxs-lookup"><span data-stu-id="5125f-184">Save the suppression log as XML.</span></span> <span data-ttu-id="5125f-185">Diese Datei gibt die Überprüfungs Meldungen an, die bei Regressionstests ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="5125f-185">This file specifies the verification messages to ignore in regression testing.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5125f-186"><strong>Beenden</strong></span><span class="sxs-lookup"><span data-stu-id="5125f-186"><strong>Exit</strong></span></span></td>
<td><span data-ttu-id="5125f-187">Schließt das accchecker-Tool.</span><span class="sxs-lookup"><span data-stu-id="5125f-187">Closes the AccChecker tool.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="5125f-188"><strong>Verifizierungen</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="5125f-188"><strong>Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="5125f-189"><strong>Run Now</strong></span><span class="sxs-lookup"><span data-stu-id="5125f-189"><strong>Run Now</strong></span></span></td>
<td><span data-ttu-id="5125f-190">Führen Sie die Überprüfungs Routinen aus, die für das ausgewählte Überprüfungs Ziel angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="5125f-190">Run the verification routines as specified for the chosen verification target.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5125f-191"><strong>Alle aktivieren</strong></span><span class="sxs-lookup"><span data-stu-id="5125f-191"><strong>Enable All</strong></span></span></td>
<td><span data-ttu-id="5125f-192">Aktivieren Sie die Kontrollkästchen Alle Überprüfungs Routine.</span><span class="sxs-lookup"><span data-stu-id="5125f-192">Check all verification routine check boxes.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5125f-193"><strong>Alle deaktivieren</strong></span><span class="sxs-lookup"><span data-stu-id="5125f-193"><strong>Disable All</strong></span></span></td>
<td><span data-ttu-id="5125f-194">Deaktivieren Sie die Kontrollkästchen Alle Überprüfungs Routine.</span><span class="sxs-lookup"><span data-stu-id="5125f-194">Uncheck all verification routine check boxes.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5125f-195"><strong>Optionen</strong></span><span class="sxs-lookup"><span data-stu-id="5125f-195"><strong>Options</strong></span></span></td>
<td><span data-ttu-id="5125f-196"><strong>Always on oben</strong></span><span class="sxs-lookup"><span data-stu-id="5125f-196"><strong>Always On Top</strong></span></span></td>
<td><span data-ttu-id="5125f-197">Erstellen Sie das oberste Fenster in der z-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="5125f-197">Make AccChecker the topmost window in the z-order.</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="5125f-198"><strong>Hilfe</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="5125f-198"><strong>Help</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="5125f-199"><strong>Hilfe</strong></span><span class="sxs-lookup"><span data-stu-id="5125f-199"><strong>Help</strong></span></span></td>
<td><span data-ttu-id="5125f-200">Anzeigen von Hilfe Informationen.</span><span class="sxs-lookup"><span data-stu-id="5125f-200">Display help information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5125f-201"><strong>Info</strong></span><span class="sxs-lookup"><span data-stu-id="5125f-201"><strong>About</strong></span></span></td>
<td><span data-ttu-id="5125f-202">Anzeigen der accchecker-Version und einer e-Mail-Adresse für die Kontaktaufnahme mit Microsoft zur Zugriffs Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="5125f-202">Display the AccChecker version and an email address for contacting Microsoft about AccChecker.</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="5125f-203">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5125f-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5125f-204">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="5125f-204">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 





