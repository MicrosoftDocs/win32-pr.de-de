---
description: Stellt die Objekte in der Shell dar. Methoden werden bereitgestellt, um die Shell zu steuern und Befehle in der Shell auszuführen. Es gibt auch Methoden, um andere Shell-bezogene Objekte zu erhalten.
title: 'Shellobjekt (Shldisp.h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 75fc151e-5b9e-476b-b4e5-b848917357a8
ms.openlocfilehash: 55f8062b71e553ec5ceefa413b45f439874744b8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841761"
---
# <a name="shell-object"></a><span data-ttu-id="694ea-105">Shellobjekt</span><span class="sxs-lookup"><span data-stu-id="694ea-105">Shell object</span></span>

<span data-ttu-id="694ea-106">Stellt die Objekte in der Shell dar.</span><span class="sxs-lookup"><span data-stu-id="694ea-106">Represents the objects in the Shell.</span></span> <span data-ttu-id="694ea-107">Methoden werden bereitgestellt, um die Shell zu steuern und Befehle in der Shell auszuführen.</span><span class="sxs-lookup"><span data-stu-id="694ea-107">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="694ea-108">Es gibt auch Methoden, um andere Shell-bezogene Objekte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="694ea-108">There are also methods to obtain other Shell-related objects.</span></span>

## <a name="members"></a><span data-ttu-id="694ea-109">Member</span><span class="sxs-lookup"><span data-stu-id="694ea-109">Members</span></span>

<span data-ttu-id="694ea-110">Das **Shell-Objekt** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="694ea-110">The **Shell** object has these types of members:</span></span>

-   [<span data-ttu-id="694ea-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="694ea-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="694ea-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="694ea-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="694ea-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="694ea-113">Methods</span></span>

<span data-ttu-id="694ea-114">Das **Shell-Objekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="694ea-114">The **Shell** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="694ea-115">Methode</span><span class="sxs-lookup"><span data-stu-id="694ea-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="694ea-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="694ea-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-118">Fügt der Liste der zuletzt verwendeten Dateien (MRU) eine Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="694ea-118">Adds a file to the most recently used (MRU) list.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-120">Erstellt ein Dialogfeld, in dem der Benutzer einen Ordner auswählen und dann das Ordnerobjekt des ausgewählten <a href="folder.md"><strong>Ordners zurückgibt.</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-120">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-122">Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und beenden kann.</span><span class="sxs-lookup"><span data-stu-id="694ea-122">Determines if the current user can start and stop the named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-124">Kaskadiert alle Fenster auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="694ea-124">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="694ea-125">Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Cascade Windows</strong>.</span><span class="sxs-lookup"><span data-stu-id="694ea-125">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade Windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-127">Führt die angegebene Systemsteuerung (\*.cpl)-Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="694ea-127">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="694ea-128">Wenn die Anwendung bereits geöffnet ist, wird die ausgeführte Instanz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="694ea-128">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="694ea-129">Ab Windows Vista sind die meisten Systemsteuerung Anwendungen Shell-Elemente und können nicht mit dieser Funktion geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="694ea-129">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="694ea-130">Um diese Systemsteuerung Anwendungen zu öffnen, übergeben Sie den kanonischen Namen an control.exe.</span><span class="sxs-lookup"><span data-stu-id="694ea-130">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="694ea-131">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="694ea-131">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-132"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-132"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-133">Wirft den Computer von seiner Andockstation aus.</span><span class="sxs-lookup"><span data-stu-id="694ea-133">Ejects the computer from its docking station.</span></span> <span data-ttu-id="694ea-134">Dies entspricht dem Klicken auf das <strong>Startmenü</strong> und der Auswahl von <strong>PC auswerfen,</strong>wenn Ihr Computer diesen Befehl unterstützt.</span><span class="sxs-lookup"><span data-stu-id="694ea-134">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-135"><a href="shell-explore.md"><strong>Erkunden</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-135"><a href="shell-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-136">Öffnet einen angegebenen Ordner in einem Windows-Explorer Fenster.</span><span class="sxs-lookup"><span data-stu-id="694ea-136">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-138">Ruft den Wert für eine angegebene Internet Explorer Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="694ea-138">Gets the value for a specified Internet Explorer policy.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-140">Zeigt das Dialogfeld <strong>Ausführen</strong> für den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="694ea-140">Displays the <strong>Run</strong> dialog to the user.</span></span> <span data-ttu-id="694ea-141">Diese Methode hat die gleiche Auswirkung wie das Klicken auf das <strong>Startmenü</strong> und das Auswählen <strong>von Ausführen.</strong></span><span class="sxs-lookup"><span data-stu-id="694ea-141">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Run</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-143">Zeigt das Dialogfeld <strong>Suchergebnisse: Computer</strong> an.</span><span class="sxs-lookup"><span data-stu-id="694ea-143">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="694ea-144">Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="694ea-144">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-145"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-145"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-146">Zeigt das Dialogfeld <strong>Suchen: Alle Dateien</strong> an.</span><span class="sxs-lookup"><span data-stu-id="694ea-146">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="694ea-147">Dies entspricht dem Klicken auf das <strong>Startmenü</strong> und der anschließenden Auswahl von <strong>Suchen</strong> (oder der entsprechenden Entsprechung unter Systemen vor Windows XP).</span><span class="sxs-lookup"><span data-stu-id="694ea-147">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong> (or its equivalent under systems earlier than Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-149">Zeigt das Dialogfeld <strong>Drucker suchen</strong> an.</span><span class="sxs-lookup"><span data-stu-id="694ea-149">Displays the <strong>Find Printer</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>Getsetting</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-151">Ruft eine globale Shelleinstellung ab.</span><span class="sxs-lookup"><span data-stu-id="694ea-151">Retrieves a global Shell setting.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-153">Ruft Systeminformationen ab.</span><span class="sxs-lookup"><span data-stu-id="694ea-153">Retrieves system information.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-154"><a href="shell-help.md"><strong>Hilfe</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-154"><a href="shell-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-155">Zeigt die Windows-Hilfe- und Supportcenter.</span><span class="sxs-lookup"><span data-stu-id="694ea-155">Displays the Windows Help and Support Center.</span></span> <span data-ttu-id="694ea-156">Diese Methode hat die gleiche Wirkung wie das Klicken auf das <strong>Startmenü</strong> und das Auswählen <strong>von Hilfe und Support.</strong></span><span class="sxs-lookup"><span data-stu-id="694ea-156">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>Isrestricted</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-158">Ruft die Einschränkungseinstellung einer Gruppe aus der Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="694ea-158">Retrieves a group's restriction setting from the registry.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-160">Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="694ea-160">Returns a value that indicates whether a particular service is running.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-162">Minimiert alle Fenster auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="694ea-162">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="694ea-163">Diese Methode hat die gleiche Wirkung wie das Klicken <strong></strong> mit der rechten Maustaste auf die Taskleiste und das Auswählen von Alle Fenster auf älteren Systemen minimieren oder auf das Symbol <strong>Desktop</strong> anzeigen im Schnellstart-Bereich der Taskleiste in Windows 2000 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="694ea-163">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-164"><a href="shell-namespace.md"><strong>Namespace</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-164"><a href="shell-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-165">Erstellt ein <a href="folder.md"><strong>Folder-Objekt für</strong></a> den angegebenen Ordner und gibt es zurück.</span><span class="sxs-lookup"><span data-stu-id="694ea-165">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-166"><a href="shell-open.md"><strong>Öffnen</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-166"><a href="shell-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-167">Öffnet den angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="694ea-167">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-169">Aktualisiert den Inhalt des <strong>Startmenüs.</strong></span><span class="sxs-lookup"><span data-stu-id="694ea-169">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="694ea-170">Wird nur mit Systemen vor Windows XP verwendet.</span><span class="sxs-lookup"><span data-stu-id="694ea-170">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-172">Zeigt den Bereich Apps-Suche an.</span><span class="sxs-lookup"><span data-stu-id="694ea-172">Displays the Apps Search pane.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-174">Startet einen benannten Dienst.</span><span class="sxs-lookup"><span data-stu-id="694ea-174">Starts a named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-176">Beendet einen benannten Dienst.</span><span class="sxs-lookup"><span data-stu-id="694ea-176">Stops a named service.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-177"><a href="shell-settime.md"><strong>Settime</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-178">Zeigt das Dialogfeld <strong>Datums- und Uhrzeiteigenschaften</strong> an.</span><span class="sxs-lookup"><span data-stu-id="694ea-178">Displays the <strong>Date and Time Properties</strong> dialog box.</span></span> <span data-ttu-id="694ea-179">Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Uhr im Taskleistenstatusbereich und das Auswählen <strong>von Datum/Uhrzeit anpassen.</strong></span><span class="sxs-lookup"><span data-stu-id="694ea-179">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust Date/Time</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-181">Führt einen angegebenen Vorgang für eine angegebene Datei aus.</span><span class="sxs-lookup"><span data-stu-id="694ea-181">Performs a specified operation on a specified file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-183">Zeigt eine Browserleiste an.</span><span class="sxs-lookup"><span data-stu-id="694ea-183">Displays a browser bar.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-185">Zeigt das Dialogfeld <strong>Windows herunterfahren</strong> an.</span><span class="sxs-lookup"><span data-stu-id="694ea-185">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="694ea-186">Dies entspricht dem Klicken auf das <strong>Menü Start</strong> und der Auswahl von <strong>Herunterfahren.</strong></span><span class="sxs-lookup"><span data-stu-id="694ea-186">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-187"><a href="shell-suspend.md"><strong>Auszusetzen</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-187"><a href="shell-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-189">Kachelt alle Fenster auf dem Desktop horizontal.</span><span class="sxs-lookup"><span data-stu-id="694ea-189">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="694ea-190">Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Fenster horizontal kacheln.</strong></span><span class="sxs-lookup"><span data-stu-id="694ea-190">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Horizontally</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-192">Kacheln aller Fenster auf dem Desktop vertikal.</span><span class="sxs-lookup"><span data-stu-id="694ea-192">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="694ea-193">Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen <strong>von Vertikales Kachelfenster.</strong></span><span class="sxs-lookup"><span data-stu-id="694ea-193">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Vertically</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-195">Zeigt den Desktop an oder blendet den Desktop aus.</span><span class="sxs-lookup"><span data-stu-id="694ea-195">Displays or hides the desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-196"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-196"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-197">Zeigt das <strong>Dialogfeld Taskleiste und Eigenschaften des Startmenüs</strong> an.</span><span class="sxs-lookup"><span data-stu-id="694ea-197">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="694ea-198">Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Eigenschaften.</strong></span><span class="sxs-lookup"><span data-stu-id="694ea-198">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-200">Stellt alle Desktopfenster in dem Zustand wieder wieder auf, den sie vor dem letzten <a href="shell-minimizeall.md"><strong>MinimizeAll-Befehl hatten.</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-200">Restores all desktop windows to the same state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="694ea-201">Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Alle</strong> Fenster auf älteren Systemen minimieren oder ein zweites Klicken auf das Symbol <strong>Desktop</strong> anzeigen im Schnellstart-Bereich der Taskleiste in Windows 2000 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="694ea-201">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> on older systems or a second clicking of the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-202"><a href="shell-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-202"><a href="shell-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-203">Erstellt ein <a href="shellwindows.md"><strong>ShellWindows-Objekt und gibt es</strong></a> zurück.</span><span class="sxs-lookup"><span data-stu-id="694ea-203">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="694ea-204">Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.</span><span class="sxs-lookup"><span data-stu-id="694ea-204">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="694ea-205"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-205"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-206">Zeigt das <strong>Windows-Sicherheit</strong> An.</span><span class="sxs-lookup"><span data-stu-id="694ea-206">Displays the <strong>Windows Security</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="694ea-207"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></span><span class="sxs-lookup"><span data-stu-id="694ea-207"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="694ea-208">Zeigt Ihre geöffneten Fenster in einem 3D-Stapel an, den Sie durchblättern können.</span><span class="sxs-lookup"><span data-stu-id="694ea-208">Displays your open windows in a 3D stack that you can flip through.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="694ea-209">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="694ea-209">Properties</span></span>

<span data-ttu-id="694ea-210">Das **Shell-Objekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="694ea-210">The **Shell** object has these properties.</span></span>



| <span data-ttu-id="694ea-211">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="694ea-211">Property</span></span>                                            | <span data-ttu-id="694ea-212">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="694ea-212">Access type</span></span>          | <span data-ttu-id="694ea-213">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="694ea-213">Description</span></span>                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="694ea-214">**Application**</span><span class="sxs-lookup"><span data-stu-id="694ea-214">**Application**</span></span>](shell-application.md)<br/> | <span data-ttu-id="694ea-215">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="694ea-215">Read-only</span></span><br/> | <span data-ttu-id="694ea-216">Enthält das Application-Objekt des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="694ea-216">Contains the object's Application object.</span></span><br/>                        |
| [<span data-ttu-id="694ea-217">**Parent**</span><span class="sxs-lookup"><span data-stu-id="694ea-217">**Parent**</span></span>](shell-parent.md)<br/>           | <span data-ttu-id="694ea-218">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="694ea-218">Read-only</span></span><br/> | <span data-ttu-id="694ea-219">Ruft ein -Objekt ab, das das übergeordnete Element des aktuellen -Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="694ea-219">Gets an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="694ea-220">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="694ea-220">Requirements</span></span>



| <span data-ttu-id="694ea-221">Anforderung</span><span class="sxs-lookup"><span data-stu-id="694ea-221">Requirement</span></span> | <span data-ttu-id="694ea-222">Wert</span><span class="sxs-lookup"><span data-stu-id="694ea-222">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="694ea-223">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="694ea-223">Minimum supported client</span></span><br/> | <span data-ttu-id="694ea-224">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="694ea-224">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="694ea-225">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="694ea-225">Minimum supported server</span></span><br/> | <span data-ttu-id="694ea-226">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="694ea-226">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="694ea-227">Header</span><span class="sxs-lookup"><span data-stu-id="694ea-227">Header</span></span><br/>                   | <dl> <span data-ttu-id="694ea-228"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="694ea-228"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="694ea-229">Idl</span><span class="sxs-lookup"><span data-stu-id="694ea-229">IDL</span></span><br/>                      | <dl> <span data-ttu-id="694ea-230"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="694ea-230"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="694ea-231">DLL</span><span class="sxs-lookup"><span data-stu-id="694ea-231">DLL</span></span><br/>                      | <dl> <span data-ttu-id="694ea-232"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="694ea-232"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
