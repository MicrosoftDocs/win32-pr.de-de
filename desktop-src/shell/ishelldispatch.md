---
description: Stellt ein -Objekt in der Shell dar.
title: IShellDispatch-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9B429C03-7F80-45db-B8CD-58D19FAD2E61
ms.openlocfilehash: 02fbead4b2d40a91ec6dab70f536d1ea3241ee84
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840891"
---
# <a name="ishelldispatch-object"></a><span data-ttu-id="dcc12-103">IShellDispatch-Objekt</span><span class="sxs-lookup"><span data-stu-id="dcc12-103">IShellDispatch object</span></span>

<span data-ttu-id="dcc12-104">Stellt ein -Objekt in der Shell dar.</span><span class="sxs-lookup"><span data-stu-id="dcc12-104">Represents an object in the Shell.</span></span> <span data-ttu-id="dcc12-105">Methoden werden bereitgestellt, um die Shell zu steuern und Befehle in der Shell auszuführen.</span><span class="sxs-lookup"><span data-stu-id="dcc12-105">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="dcc12-106">Es gibt auch Methoden, um andere Shell-bezogene Objekte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="dcc12-106">There are also methods to obtain other Shell-related objects.</span></span>

> [!Note]  
> <span data-ttu-id="dcc12-107">**IShellDispatch wird** implementiert und über das [**Shell-Objekt aufgerufen.**](shell.md)</span><span class="sxs-lookup"><span data-stu-id="dcc12-107">**IShellDispatch** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="dcc12-108">Member</span><span class="sxs-lookup"><span data-stu-id="dcc12-108">Members</span></span>

<span data-ttu-id="dcc12-109">Das **IShellDispatch-Objekt** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="dcc12-109">The **IShellDispatch** object has these types of members:</span></span>

-   [<span data-ttu-id="dcc12-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="dcc12-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="dcc12-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dcc12-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dcc12-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="dcc12-112">Methods</span></span>

<span data-ttu-id="dcc12-113">Das **IShellDispatch-Objekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="dcc12-113">The **IShellDispatch** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="dcc12-114">Methode</span><span class="sxs-lookup"><span data-stu-id="dcc12-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="dcc12-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dcc12-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="dcc12-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-117">Erstellt ein Dialogfeld, in dem der Benutzer einen Ordner auswählen und dann das Ordnerobjekt des ausgewählten <a href="folder.md"><strong>Ordners zurückgibt.</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-117">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="dcc12-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-119">Kaskadiert alle Fenster auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="dcc12-119">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="dcc12-120">Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Kaskadieren von Fenstern.</strong></span><span class="sxs-lookup"><span data-stu-id="dcc12-120">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="dcc12-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-122">Führt die angegebene Systemsteuerung aus.</span><span class="sxs-lookup"><span data-stu-id="dcc12-122">Runs the specified Control Panel application.</span></span> <span data-ttu-id="dcc12-123">Wenn die Anwendung bereits geöffnet ist, wird die ausgeführte Instanz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="dcc12-123">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="dcc12-124">Ab Windows Vista sind die meisten Systemsteuerung Shell-Elemente und können mit dieser Funktion nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="dcc12-124">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="dcc12-125">Um diese anwendungen Systemsteuerung öffnen, übergeben Sie den kanonischen Namen an control.exe.</span><span class="sxs-lookup"><span data-stu-id="dcc12-125">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="dcc12-126">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="dcc12-126">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="dcc12-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-128">Wirft den Computer von seiner Andockstation aus.</span><span class="sxs-lookup"><span data-stu-id="dcc12-128">Ejects the computer from its docking station.</span></span> <span data-ttu-id="dcc12-129">Dies entspricht dem Klicken auf das <strong>Startmenü</strong> und dem Auswählen von <strong>PC auswerfen,</strong>wenn ihr Computer diesen Befehl unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dcc12-129">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="dcc12-130"><a href="ishelldispatch-explore.md"><strong>Erkunden</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-130"><a href="ishelldispatch-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-131">Öffnet einen angegebenen Ordner in einem Windows-Explorer Fenster.</span><span class="sxs-lookup"><span data-stu-id="dcc12-131">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="dcc12-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-133">Zeigt das Dialogfeld <strong>Ausführen</strong> für den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="dcc12-133">Displays the <strong>Run</strong> dialog to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="dcc12-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-135">Zeigt das Dialogfeld <strong>Suchergebnisse: Computer an.</strong></span><span class="sxs-lookup"><span data-stu-id="dcc12-135">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="dcc12-136">Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dcc12-136">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="dcc12-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-138">Zeigt das Dialogfeld <strong>Suchen: Alle Dateien</strong> an.</span><span class="sxs-lookup"><span data-stu-id="dcc12-138">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="dcc12-139">Dies entspricht dem Klicken auf das <strong>Menü Start</strong> und anschließender Auswahl von <strong>Suchen.</strong></span><span class="sxs-lookup"><span data-stu-id="dcc12-139">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="dcc12-140"><a href="ishelldispatch-help.md"><strong>Hilfe</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-140"><a href="ishelldispatch-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-141">Zeigt das Fenster Hilfe und Support von Windows an.</span><span class="sxs-lookup"><span data-stu-id="dcc12-141">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="dcc12-142">Diese Methode hat die gleiche Auswirkung wie das Klicken auf das <strong>Startmenü</strong> und das Auswählen von <strong>Hilfe und Support.</strong></span><span class="sxs-lookup"><span data-stu-id="dcc12-142">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="dcc12-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimierenAlle</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-144">Minimiert alle Fenster auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="dcc12-144">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="dcc12-145">Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Minimieren aller Windows-Fenster</strong> auf älteren Systemen oder Klicken auf das Symbol <strong>Desktop anzeigen</strong> auf der Taskleiste.</span><span class="sxs-lookup"><span data-stu-id="dcc12-145">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon on the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="dcc12-146"><a href="ishelldispatch-namespace.md"><strong>Namespace</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-146"><a href="ishelldispatch-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-147">Erstellt ein <a href="folder.md"><strong>Folder-Objekt</strong></a> für den angegebenen Ordner und gibt es zurück.</span><span class="sxs-lookup"><span data-stu-id="dcc12-147">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="dcc12-148"><a href="ishelldispatch-open.md"><strong>Öffnen</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-148"><a href="ishelldispatch-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-149">Öffnet den angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="dcc12-149">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="dcc12-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-151">Aktualisiert den Inhalt des <strong>Startmenüs.</strong></span><span class="sxs-lookup"><span data-stu-id="dcc12-151">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="dcc12-152">Wird nur mit Systemen vor Windows XP verwendet.</span><span class="sxs-lookup"><span data-stu-id="dcc12-152">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="dcc12-153"><a href="ishelldispatch-settime.md"><strong>Settime</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-154">Zeigt das <strong>Dialogfeld Datum und Uhrzeit</strong> an.</span><span class="sxs-lookup"><span data-stu-id="dcc12-154">Displays the <strong>Date and Time</strong> dialog box.</span></span> <span data-ttu-id="dcc12-155">Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Uhr im Statusbereich der Taskleiste und das Auswählen von <strong>Datum/Uhrzeit anpassen.</strong></span><span class="sxs-lookup"><span data-stu-id="dcc12-155">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust date/time</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="dcc12-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-157">Zeigt das <strong>Dialogfeld Windows herunterfahren</strong> an.</span><span class="sxs-lookup"><span data-stu-id="dcc12-157">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="dcc12-158">Dies ist identisch mit dem Klicken auf das <strong>Startmenü</strong> und dem Auswählen <strong>von Herunterfahren.</strong></span><span class="sxs-lookup"><span data-stu-id="dcc12-158">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="dcc12-159"><a href="ishelldispatch-suspend.md"><strong>Auszusetzen</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-159"><a href="ishelldispatch-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="dcc12-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-161">Kacheln aller Fenster auf dem Desktop horizontal.</span><span class="sxs-lookup"><span data-stu-id="dcc12-161">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="dcc12-162">Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen <strong>von Fenstern gestapelt anzeigen.</strong></span><span class="sxs-lookup"><span data-stu-id="dcc12-162">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows stacked</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="dcc12-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-164">Kacheln aller Fenster auf dem Desktop vertikal.</span><span class="sxs-lookup"><span data-stu-id="dcc12-164">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="dcc12-165">Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Fenstern nebeneinander anzeigen.</strong></span><span class="sxs-lookup"><span data-stu-id="dcc12-165">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows side by side</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="dcc12-166"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-166"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-167">Zeigt das <strong>Dialogfeld Taskleiste und Eigenschaften des Startmenüs</strong> an.</span><span class="sxs-lookup"><span data-stu-id="dcc12-167">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="dcc12-168">Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Eigenschaften.</strong></span><span class="sxs-lookup"><span data-stu-id="dcc12-168">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="dcc12-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-170">Stellt alle Desktopfenster in dem Zustand wieder her, in dem sie sich vor dem letzten <a href="shell-minimizeall.md"><strong>MinimizeAll-Befehl</strong></a> befanden.</span><span class="sxs-lookup"><span data-stu-id="dcc12-170">Restores all desktop windows to the state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="dcc12-171">Diese Methode hat den gleichen Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Alle Fenster minimieren</strong> rückgängig (auf älteren Systemen) oder ein zweites Klicken auf das Symbol Desktop <strong>anzeigen</strong> in der Taskleiste.</span><span class="sxs-lookup"><span data-stu-id="dcc12-171">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> (on older systems) or a second clicking of the <strong>Show Desktop</strong> icon in the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="dcc12-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcc12-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="dcc12-173">Erstellt ein <a href="shellwindows.md"><strong>ShellWindows-Objekt</strong></a> und gibt es zurück.</span><span class="sxs-lookup"><span data-stu-id="dcc12-173">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="dcc12-174">Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.</span><span class="sxs-lookup"><span data-stu-id="dcc12-174">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="dcc12-175">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dcc12-175">Properties</span></span>

<span data-ttu-id="dcc12-176">Das **IShellDispatch-Objekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dcc12-176">The **IShellDispatch** object has these properties.</span></span>



| <span data-ttu-id="dcc12-177">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dcc12-177">Property</span></span>                                                     | <span data-ttu-id="dcc12-178">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="dcc12-178">Access type</span></span>          | <span data-ttu-id="dcc12-179">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dcc12-179">Description</span></span>                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="dcc12-180">**Application**</span><span class="sxs-lookup"><span data-stu-id="dcc12-180">**Application**</span></span>](ishelldispatch-application.md)<br/> | <span data-ttu-id="dcc12-181">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dcc12-181">Read-only</span></span><br/> | <span data-ttu-id="dcc12-182">Enthält ein -Objekt, das eine Anwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcc12-182">Contains an object that represents an application.</span></span><br/>                    |
| [<span data-ttu-id="dcc12-183">**Parent**</span><span class="sxs-lookup"><span data-stu-id="dcc12-183">**Parent**</span></span>](ishelldispatch-parent.md)<br/>           | <span data-ttu-id="dcc12-184">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dcc12-184">Read-only</span></span><br/> | <span data-ttu-id="dcc12-185">Ruft ein -Objekt ab, das das übergeordnete Element des aktuellen -Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcc12-185">Retrieves an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dcc12-186">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dcc12-186">Requirements</span></span>



| <span data-ttu-id="dcc12-187">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dcc12-187">Requirement</span></span> | <span data-ttu-id="dcc12-188">Wert</span><span class="sxs-lookup"><span data-stu-id="dcc12-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcc12-189">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dcc12-189">Minimum supported client</span></span><br/> | <span data-ttu-id="dcc12-190">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dcc12-190">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dcc12-191">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dcc12-191">Minimum supported server</span></span><br/> | <span data-ttu-id="dcc12-192">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dcc12-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dcc12-193">Header</span><span class="sxs-lookup"><span data-stu-id="dcc12-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcc12-194"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="dcc12-194"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="dcc12-195">Idl</span><span class="sxs-lookup"><span data-stu-id="dcc12-195">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dcc12-196"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="dcc12-196"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="dcc12-197">DLL</span><span class="sxs-lookup"><span data-stu-id="dcc12-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcc12-198"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="dcc12-198"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcc12-199">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcc12-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc12-200">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="dcc12-200">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="dcc12-201">**Shell-Objekt**</span><span class="sxs-lookup"><span data-stu-id="dcc12-201">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 
