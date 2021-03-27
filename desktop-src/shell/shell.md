---
description: Stellt die-Objekte in der Shell dar. Es werden Methoden bereitgestellt, um die Shell zu steuern und um Befehle in der Shell auszuführen. Es gibt auch Methoden zum Abrufen anderer shellbezogener Objekte.
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
ms.openlocfilehash: 3e891278d98ca2eb51fca11054cba01947e03c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867744"
---
# <a name="shell-object"></a><span data-ttu-id="47cdd-105">Shellobjekt</span><span class="sxs-lookup"><span data-stu-id="47cdd-105">Shell object</span></span>

<span data-ttu-id="47cdd-106">Stellt die-Objekte in der Shell dar.</span><span class="sxs-lookup"><span data-stu-id="47cdd-106">Represents the objects in the Shell.</span></span> <span data-ttu-id="47cdd-107">Es werden Methoden bereitgestellt, um die Shell zu steuern und um Befehle in der Shell auszuführen.</span><span class="sxs-lookup"><span data-stu-id="47cdd-107">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="47cdd-108">Es gibt auch Methoden zum Abrufen anderer shellbezogener Objekte.</span><span class="sxs-lookup"><span data-stu-id="47cdd-108">There are also methods to obtain other Shell-related objects.</span></span>

## <a name="members"></a><span data-ttu-id="47cdd-109">Member</span><span class="sxs-lookup"><span data-stu-id="47cdd-109">Members</span></span>

<span data-ttu-id="47cdd-110">Das **Shellobjekt** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="47cdd-110">The **Shell** object has these types of members:</span></span>

-   [<span data-ttu-id="47cdd-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="47cdd-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="47cdd-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47cdd-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="47cdd-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="47cdd-113">Methods</span></span>

<span data-ttu-id="47cdd-114">Das **Shellobjekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="47cdd-114">The **Shell** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="47cdd-115">Methode</span><span class="sxs-lookup"><span data-stu-id="47cdd-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="47cdd-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47cdd-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>Addtor</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-118">Fügt der Liste der zuletzt verwendeten (MRU) eine Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="47cdd-118">Adds a file to the most recently used (MRU) list.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-119"><a href="shell-browseforfolder.md"><strong>Browsorforfolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-120">Erstellt ein Dialogfeld, das dem Benutzer ermöglicht, einen Ordner auszuwählen, und gibt dann das <a href="folder.md"><strong>Ordner</strong></a> Objekt des ausgewählten Ordners zurück.</span><span class="sxs-lookup"><span data-stu-id="47cdd-120">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>Canstartstopservice</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-122">Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und Abbrechen kann.</span><span class="sxs-lookup"><span data-stu-id="47cdd-122">Determines if the current user can start and stop the named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-123"><a href="shell-cascadewindows.md"><strong>Cascade-Fenster</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-124">Alle Fenster auf dem Desktop werden kaskadiert.</span><span class="sxs-lookup"><span data-stu-id="47cdd-124">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="47cdd-125">Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und <strong>kaskadierte Fenster</strong>auswählen.</span><span class="sxs-lookup"><span data-stu-id="47cdd-125">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade Windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-127">Führt die angegebene System Steuerungsanwendung (\*. cpl) aus.</span><span class="sxs-lookup"><span data-stu-id="47cdd-127">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="47cdd-128">Wenn die Anwendung bereits geöffnet ist, wird die laufende Instanz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="47cdd-128">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="47cdd-129">Ab Windows Vista sind die meisten System Steuerungsanwendungen shellelemente und können nicht mit dieser Funktion geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="47cdd-129">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="47cdd-130">Wenn Sie diese System Steuerungsanwendungen öffnen möchten, übergeben Sie den kanonischen Namen an control.exe.</span><span class="sxs-lookup"><span data-stu-id="47cdd-130">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="47cdd-131">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="47cdd-131">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-132"><a href="shell-ejectpc.md"><strong>Ejectpc</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-132"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-133">Der Computer wird von seiner Docking Station eingelesen.</span><span class="sxs-lookup"><span data-stu-id="47cdd-133">Ejects the computer from its docking station.</span></span> <span data-ttu-id="47cdd-134">Dies ist das gleiche wie beim Klicken auf das <strong>Startmenü</strong> und beim Auswählen von <strong>ausgelösten PCs</strong>, wenn Ihr Computer diesen Befehl unterstützt.</span><span class="sxs-lookup"><span data-stu-id="47cdd-134">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-135"><a href="shell-explore.md"><strong>Erkunden</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-135"><a href="shell-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-136">Öffnet einen angegebenen Ordner in einem Windows-Explorer-Fenster.</span><span class="sxs-lookup"><span data-stu-id="47cdd-136">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-137"><a href="shell-explorerpolicy.md"><strong>Explorerpolicy</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-138">Ruft den Wert für eine angegebene Internet Explorer-Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="47cdd-138">Gets the value for a specified Internet Explorer policy.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-139"><a href="shell-filerun.md"><strong>Filerun</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-140">Zeigt das Dialogfeld " <strong>Ausführen</strong> " für den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="47cdd-140">Displays the <strong>Run</strong> dialog to the user.</span></span> <span data-ttu-id="47cdd-141">Diese Methode hat denselben Effekt wie das Klicken auf das <strong>Startmenü</strong> und das Auswählen von <strong>Ausführen</strong>.</span><span class="sxs-lookup"><span data-stu-id="47cdd-141">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Run</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-142"><a href="shell-findcomputer.md"><strong>Findcomputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-143">Zeigt das Dialogfeld <strong>Suchergebnisse: Computer</strong> an.</span><span class="sxs-lookup"><span data-stu-id="47cdd-143">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="47cdd-144">Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="47cdd-144">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-145"><a href="shell-findfiles.md"><strong>"Findfiles</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-145"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-146">Zeigt das Dialogfeld <strong>suchen: alle Dateien</strong> an.</span><span class="sxs-lookup"><span data-stu-id="47cdd-146">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="47cdd-147">Dies ist das gleiche wie beim Klicken auf das <strong>Startmenü</strong> und anschließendes Auswählen von <strong>Suchen</strong> (oder der entsprechenden Entsprechung unter Systeme vor Windows XP).</span><span class="sxs-lookup"><span data-stu-id="47cdd-147">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong> (or its equivalent under systems earlier than Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>Findprinter</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-149">Zeigt das Dialogfeld <strong>Drucker suchen</strong> an.</span><span class="sxs-lookup"><span data-stu-id="47cdd-149">Displays the <strong>Find Printer</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-151">Ruft eine globale shelleinstellung ab.</span><span class="sxs-lookup"><span data-stu-id="47cdd-151">Retrieves a global Shell setting.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>Getsysteminformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-153">Ruft Systeminformationen ab.</span><span class="sxs-lookup"><span data-stu-id="47cdd-153">Retrieves system information.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-154"><a href="shell-help.md"><strong>Hilfe</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-154"><a href="shell-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-155">Zeigt das Windows-Hilfe-und Support Center an.</span><span class="sxs-lookup"><span data-stu-id="47cdd-155">Displays the Windows Help and Support Center.</span></span> <span data-ttu-id="47cdd-156">Diese Methode hat denselben Effekt wie das Klicken auf das <strong>Startmenü</strong> und das Auswählen von <strong>Hilfe und Support</strong>.</span><span class="sxs-lookup"><span data-stu-id="47cdd-156">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-158">Ruft die Einschränkungs Einstellung einer Gruppe aus der Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="47cdd-158">Retrieves a group's restriction setting from the registry.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>Isservicerunning</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-160">Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47cdd-160">Returns a value that indicates whether a particular service is running.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-161"><a href="shell-minimizeall.md"><strong>Minimizeall</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-162">Minimiert alle Fenster auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="47cdd-162">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="47cdd-163">Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von "alle Fenster auf älteren Systemen <strong>minimieren</strong> " oder das Klicken auf das Symbol " <strong>Desktop anzeigen</strong> " im Bereich "Schnellstart" der Taskleiste in Windows 2000 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="47cdd-163">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-164"><a href="shell-namespace.md"><strong>Namespace</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-164"><a href="shell-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-165">Erstellt ein <a href="folder.md"><strong>Ordner</strong></a> Objekt für den angegebenen Ordner und gibt dieses zurück.</span><span class="sxs-lookup"><span data-stu-id="47cdd-165">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-166"><a href="shell-open.md"><strong>Eren</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-166"><a href="shell-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-167">Öffnet den angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="47cdd-167">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-168"><a href="shell-refreshmenu.md"><strong>Aktuerfrischendes Menü</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-169">Aktualisiert den Inhalt des <strong>Start</strong> Menüs.</span><span class="sxs-lookup"><span data-stu-id="47cdd-169">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="47cdd-170">Wird nur mit Systemen vor Windows XP verwendet.</span><span class="sxs-lookup"><span data-stu-id="47cdd-170">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-171"><a href="shell-searchcommand.md"><strong>Searchcommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-172">Zeigt den Bereich apps-Suche an.</span><span class="sxs-lookup"><span data-stu-id="47cdd-172">Displays the Apps Search pane.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>Servicestart</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-174">Startet einen benannten Dienst.</span><span class="sxs-lookup"><span data-stu-id="47cdd-174">Starts a named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>Servicestop</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-176">Beendet einen benannten Dienst.</span><span class="sxs-lookup"><span data-stu-id="47cdd-176">Stops a named service.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-178">Zeigt das Dialogfeld <strong>Datums-und Uhrzeit Eigenschaften</strong> an.</span><span class="sxs-lookup"><span data-stu-id="47cdd-178">Displays the <strong>Date and Time Properties</strong> dialog box.</span></span> <span data-ttu-id="47cdd-179">Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Uhr im Statusbereich der Taskleiste und das Auswählen von <strong>Datum/Uhrzeit anpassen</strong>.</span><span class="sxs-lookup"><span data-stu-id="47cdd-179">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust Date/Time</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-181">Führt einen angegebenen Vorgang für eine angegebene Datei aus.</span><span class="sxs-lookup"><span data-stu-id="47cdd-181">Performs a specified operation on a specified file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>Showbrowserbar</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-183">Zeigt eine Browserleiste an.</span><span class="sxs-lookup"><span data-stu-id="47cdd-183">Displays a browser bar.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-184"><a href="shell-shutdownwindows.md"><strong>Shutdownwindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-185">Zeigt das Dialogfeld <strong>Windows herunter</strong> fahren an.</span><span class="sxs-lookup"><span data-stu-id="47cdd-185">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="47cdd-186">Dies ist das gleiche wie beim Klicken auf das <strong>Startmenü</strong> und beim Auswählen von " <strong>herunter</strong>fahren".</span><span class="sxs-lookup"><span data-stu-id="47cdd-186">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-187"><a href="shell-suspend.md"><strong>Angehalten</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-187"><a href="shell-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-188"><a href="shell-tilehorizontally.md"><strong>Tilehorizontisch</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-189">Kachelt alle Fenster auf dem Desktop horizontal.</span><span class="sxs-lookup"><span data-stu-id="47cdd-189">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="47cdd-190">Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und <strong>Fenster horizontal</strong>nebeneinander auswählen.</span><span class="sxs-lookup"><span data-stu-id="47cdd-190">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Horizontally</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-191"><a href="shell-tilevertically.md"><strong>Tilevertikal</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-192">Kachelt alle Fenster auf dem Desktop vertikal.</span><span class="sxs-lookup"><span data-stu-id="47cdd-192">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="47cdd-193">Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und nebeneinander <strong>Fenster</strong>nebeneinander auswählen.</span><span class="sxs-lookup"><span data-stu-id="47cdd-193">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Vertically</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-195">Zeigt den Desktop an oder blendet ihn aus.</span><span class="sxs-lookup"><span data-stu-id="47cdd-195">Displays or hides the desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-196"><a href="shell-trayproperties.md"><strong>Trayproperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-196"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-197">Zeigt das Dialogfeld <strong>Eigenschaften von Taskleiste und Startmenü</strong> an.</span><span class="sxs-lookup"><span data-stu-id="47cdd-197">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="47cdd-198">Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und <strong>Eigenschaften</strong>auswählen.</span><span class="sxs-lookup"><span data-stu-id="47cdd-198">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-199"><a href="shell-undominimizeall.md"><strong>Undominimizeall</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-200">Stellt alle Desktop Fenster in dem Zustand wieder her, in dem Sie vor dem letzten <a href="shell-minimizeall.md"><strong>minimizeall</strong></a> -Befehl standen.</span><span class="sxs-lookup"><span data-stu-id="47cdd-200">Restores all desktop windows to the same state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="47cdd-201">Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von "alle Fenster auf älteren Systemen <strong>minimieren</strong> " oder ein zweites klicken auf das Symbol " <strong>Desktop anzeigen</strong> " im Bereich "Schnellstart" der Taskleiste in Windows 2000 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="47cdd-201">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> on older systems or a second clicking of the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-202"><a href="shell-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-202"><a href="shell-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-203">Erstellt ein <a href="shellwindows.md"><strong>shellwindows</strong></a> -Objekt und gibt es zurück.</span><span class="sxs-lookup"><span data-stu-id="47cdd-203">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="47cdd-204">Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.</span><span class="sxs-lookup"><span data-stu-id="47cdd-204">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47cdd-205"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-205"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-206">Zeigt das Dialogfeld <strong>Windows-Sicherheit</strong> an.</span><span class="sxs-lookup"><span data-stu-id="47cdd-206">Displays the <strong>Windows Security</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47cdd-207"><a href="shell-windowswitcher.md"><strong>Windowswitcher</strong></a></span><span class="sxs-lookup"><span data-stu-id="47cdd-207"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="47cdd-208">Zeigt die geöffneten Fenster in einem 3D-Stapel an, den Sie durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="47cdd-208">Displays your open windows in a 3D stack that you can flip through.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="47cdd-209">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47cdd-209">Properties</span></span>

<span data-ttu-id="47cdd-210">Das **Shellobjekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="47cdd-210">The **Shell** object has these properties.</span></span>



| <span data-ttu-id="47cdd-211">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="47cdd-211">Property</span></span>                                            | <span data-ttu-id="47cdd-212">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="47cdd-212">Access type</span></span>          | <span data-ttu-id="47cdd-213">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47cdd-213">Description</span></span>                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="47cdd-214">**Application**</span><span class="sxs-lookup"><span data-stu-id="47cdd-214">**Application**</span></span>](shell-application.md)<br/> | <span data-ttu-id="47cdd-215">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47cdd-215">Read-only</span></span><br/> | <span data-ttu-id="47cdd-216">Enthält das Anwendungs Objekt des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="47cdd-216">Contains the object's Application object.</span></span><br/>                        |
| [<span data-ttu-id="47cdd-217">**Parent**</span><span class="sxs-lookup"><span data-stu-id="47cdd-217">**Parent**</span></span>](shell-parent.md)<br/>           | <span data-ttu-id="47cdd-218">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47cdd-218">Read-only</span></span><br/> | <span data-ttu-id="47cdd-219">Ruft ein-Objekt ab, das das übergeordnete Element des aktuellen-Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="47cdd-219">Gets an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="47cdd-220">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="47cdd-220">Requirements</span></span>



| <span data-ttu-id="47cdd-221">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47cdd-221">Requirement</span></span> | <span data-ttu-id="47cdd-222">Wert</span><span class="sxs-lookup"><span data-stu-id="47cdd-222">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47cdd-223">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47cdd-223">Minimum supported client</span></span><br/> | <span data-ttu-id="47cdd-224">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47cdd-224">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="47cdd-225">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47cdd-225">Minimum supported server</span></span><br/> | <span data-ttu-id="47cdd-226">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47cdd-226">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="47cdd-227">Header</span><span class="sxs-lookup"><span data-stu-id="47cdd-227">Header</span></span><br/>                   | <dl> <span data-ttu-id="47cdd-228"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="47cdd-228"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="47cdd-229">IDL</span><span class="sxs-lookup"><span data-stu-id="47cdd-229">IDL</span></span><br/>                      | <dl> <span data-ttu-id="47cdd-230"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="47cdd-230"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="47cdd-231">DLL</span><span class="sxs-lookup"><span data-stu-id="47cdd-231">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47cdd-232"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="47cdd-232"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
