---
description: Stellt ein Objekt in der Shell dar.
title: Ishelldispatch-Objekt (Shldisp. h)
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
ms.openlocfilehash: 20c6cc9f0b3a2e2fde8f56311564d63bc1cc9c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978073"
---
# <a name="ishelldispatch-object"></a><span data-ttu-id="8f9f1-103">Ishelldispatch-Objekt</span><span class="sxs-lookup"><span data-stu-id="8f9f1-103">IShellDispatch object</span></span>

<span data-ttu-id="8f9f1-104">Stellt ein Objekt in der Shell dar.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-104">Represents an object in the Shell.</span></span> <span data-ttu-id="8f9f1-105">Es werden Methoden bereitgestellt, um die Shell zu steuern und um Befehle in der Shell auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-105">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="8f9f1-106">Es gibt auch Methoden zum Abrufen anderer shellbezogener Objekte.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-106">There are also methods to obtain other Shell-related objects.</span></span>

> [!Note]  
> <span data-ttu-id="8f9f1-107">**Ishelldispatch** wird implementiert und über das [**Shellobjekt**](shell.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-107">**IShellDispatch** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="8f9f1-108">Member</span><span class="sxs-lookup"><span data-stu-id="8f9f1-108">Members</span></span>

<span data-ttu-id="8f9f1-109">Das **ishelldispatch** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8f9f1-109">The **IShellDispatch** object has these types of members:</span></span>

-   [<span data-ttu-id="8f9f1-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="8f9f1-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8f9f1-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f9f1-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8f9f1-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="8f9f1-112">Methods</span></span>

<span data-ttu-id="8f9f1-113">Das **ishelldispatch** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-113">The **IShellDispatch** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="8f9f1-114">Methode</span><span class="sxs-lookup"><span data-stu-id="8f9f1-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="8f9f1-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f9f1-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8f9f1-116"><a href="ishelldispatch-browseforfolder.md"><strong>Browsorforfolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-117">Erstellt ein Dialogfeld, das dem Benutzer ermöglicht, einen Ordner auszuwählen, und gibt dann das <a href="folder.md"><strong>Ordner</strong></a> Objekt des ausgewählten Ordners zurück.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-117">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="8f9f1-118"><a href="ishelldispatch-cascadewindows.md"><strong>Cascade-Fenster</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-119">Alle Fenster auf dem Desktop werden kaskadiert.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-119">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="8f9f1-120">Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und <strong>kaskadierte Fenster</strong>auswählen.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-120">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8f9f1-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-122">Führt die angegebene System Steuerungsanwendung aus.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-122">Runs the specified Control Panel application.</span></span> <span data-ttu-id="8f9f1-123">Wenn die Anwendung bereits geöffnet ist, wird die laufende Instanz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-123">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="8f9f1-124">Ab Windows Vista sind die meisten System Steuerungsanwendungen shellelemente und können nicht mit dieser Funktion geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-124">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="8f9f1-125">Wenn Sie diese System Steuerungsanwendungen öffnen möchten, übergeben Sie den kanonischen Namen an control.exe.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-125">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="8f9f1-126">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8f9f1-126">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="8f9f1-127"><a href="ishelldispatch-ejectpc.md"><strong>Ejectpc</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-128">Der Computer wird von seiner Docking Station eingelesen.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-128">Ejects the computer from its docking station.</span></span> <span data-ttu-id="8f9f1-129">Dies ist das gleiche wie beim Klicken auf das <strong>Startmenü</strong> und beim Auswählen von <strong>ausgelösten PCs</strong>, wenn Ihr Computer diesen Befehl unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-129">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8f9f1-130"><a href="ishelldispatch-explore.md"><strong>Erkunden</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-130"><a href="ishelldispatch-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-131">Öffnet einen angegebenen Ordner in einem Windows-Explorer-Fenster.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-131">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="8f9f1-132"><a href="ishelldispatch-filerun.md"><strong>Filerun</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-133">Zeigt das Dialogfeld " <strong>Ausführen</strong> " für den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-133">Displays the <strong>Run</strong> dialog to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8f9f1-134"><a href="ishelldispatch-findcomputer.md"><strong>Findcomputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-135">Zeigt das Dialogfeld <strong>Suchergebnisse: Computer</strong> an.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-135">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="8f9f1-136">Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-136">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="8f9f1-137"><a href="ishelldispatch-findfiles.md"><strong>"Findfiles</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-138">Zeigt das Dialogfeld <strong>suchen: alle Dateien</strong> an.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-138">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="8f9f1-139">Dies ist das gleiche wie beim Klicken auf das <strong>Startmenü</strong> und anschließendes Auswählen von <strong>Suchen</strong>.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-139">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8f9f1-140"><a href="ishelldispatch-help.md"><strong>Hilfe</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-140"><a href="ishelldispatch-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-141">Zeigt das Fenster Hilfe und Support an.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-141">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="8f9f1-142">Diese Methode hat denselben Effekt wie das Klicken auf das <strong>Startmenü</strong> und das Auswählen von <strong>Hilfe und Support</strong>.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-142">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="8f9f1-143"><a href="ishelldispatch-minimizeall.md"><strong>Minimizeall</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-144">Minimiert alle Fenster auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-144">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="8f9f1-145">Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen der Option alle Fenster auf älteren Systemen <strong>minimieren</strong> oder klicken auf das Symbol <strong>Desktop anzeigen</strong> auf der Taskleiste.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-145">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon on the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8f9f1-146"><a href="ishelldispatch-namespace.md"><strong>Namespace</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-146"><a href="ishelldispatch-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-147">Erstellt ein <a href="folder.md"><strong>Ordner</strong></a> Objekt für den angegebenen Ordner und gibt dieses zurück.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-147">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="8f9f1-148"><a href="ishelldispatch-open.md"><strong>Eren</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-148"><a href="ishelldispatch-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-149">Öffnet den angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-149">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8f9f1-150"><a href="ishelldispatch-refreshmenu.md"><strong>Aktuerfrischendes Menü</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-151">Aktualisiert den Inhalt des <strong>Start</strong> Menüs.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-151">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="8f9f1-152">Wird nur mit Systemen vor Windows XP verwendet.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-152">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="8f9f1-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-154">Zeigt das Dialogfeld <strong>Datum und Uhrzeit</strong> an.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-154">Displays the <strong>Date and Time</strong> dialog box.</span></span> <span data-ttu-id="8f9f1-155">Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Uhr im Statusbereich der Taskleiste und das Auswählen von <strong>Datum/Uhrzeit anpassen</strong>.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-155">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust date/time</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8f9f1-156"><a href="ishelldispatch-shutdownwindows.md"><strong>Shutdownwindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-157">Zeigt das Dialogfeld <strong>Windows herunter</strong> fahren an.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-157">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="8f9f1-158">Dies ist das gleiche wie beim Klicken auf das <strong>Startmenü</strong> und beim Auswählen von " <strong>herunter</strong>fahren".</span><span class="sxs-lookup"><span data-stu-id="8f9f1-158">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="8f9f1-159"><a href="ishelldispatch-suspend.md"><strong>Angehalten</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-159"><a href="ishelldispatch-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8f9f1-160"><a href="ishelldispatch-tilehorizontally.md"><strong>Tilehorizontisch</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-161">Kachelt alle Fenster auf dem Desktop horizontal.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-161">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="8f9f1-162">Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Gestapeltes Fenster anzeigen</strong>.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-162">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows stacked</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="8f9f1-163"><a href="ishelldispatch-tilevertically.md"><strong>Tilevertikal</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-164">Kachelt alle Fenster auf dem Desktop vertikal.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-164">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="8f9f1-165">Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und <strong>Fenster nebeneinander anzeigen</strong>auswählen.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-165">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows side by side</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8f9f1-166"><a href="ishelldispatch-trayproperties.md"><strong>Trayproperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-166"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-167">Zeigt das Dialogfeld <strong>Eigenschaften von Taskleiste und Startmenü</strong> an.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-167">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="8f9f1-168">Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und <strong>Eigenschaften</strong>auswählen.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-168">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="8f9f1-169"><a href="ishelldispatch-undominimizeall.md"><strong>Undominimizeall</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-170">Stellt alle Desktop Fenster in dem Zustand wieder her, in dem Sie sich vor dem letzten <a href="shell-minimizeall.md"><strong>minimizeall</strong></a> -Befehl befanden.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-170">Restores all desktop windows to the state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="8f9f1-171">Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von " <strong>alle Fenster minimieren</strong> (auf älteren Systemen)" oder ein zweites klicken auf das Symbol " <strong>Desktop anzeigen</strong> " in der Taskleiste.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-171">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> (on older systems) or a second clicking of the <strong>Show Desktop</strong> icon in the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8f9f1-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f9f1-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8f9f1-173">Erstellt ein <a href="shellwindows.md"><strong>shellwindows</strong></a> -Objekt und gibt es zurück.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-173">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="8f9f1-174">Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-174">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="8f9f1-175">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f9f1-175">Properties</span></span>

<span data-ttu-id="8f9f1-176">Das **ishelldispatch** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-176">The **IShellDispatch** object has these properties.</span></span>



| <span data-ttu-id="8f9f1-177">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8f9f1-177">Property</span></span>                                                     | <span data-ttu-id="8f9f1-178">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="8f9f1-178">Access type</span></span>          | <span data-ttu-id="8f9f1-179">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f9f1-179">Description</span></span>                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="8f9f1-180">**Application**</span><span class="sxs-lookup"><span data-stu-id="8f9f1-180">**Application**</span></span>](ishelldispatch-application.md)<br/> | <span data-ttu-id="8f9f1-181">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f9f1-181">Read-only</span></span><br/> | <span data-ttu-id="8f9f1-182">Enthält ein-Objekt, das eine Anwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-182">Contains an object that represents an application.</span></span><br/>                    |
| [<span data-ttu-id="8f9f1-183">**Parent**</span><span class="sxs-lookup"><span data-stu-id="8f9f1-183">**Parent**</span></span>](ishelldispatch-parent.md)<br/>           | <span data-ttu-id="8f9f1-184">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f9f1-184">Read-only</span></span><br/> | <span data-ttu-id="8f9f1-185">Ruft ein-Objekt ab, das das übergeordnete Element des aktuellen-Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="8f9f1-185">Retrieves an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8f9f1-186">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8f9f1-186">Requirements</span></span>



| <span data-ttu-id="8f9f1-187">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f9f1-187">Requirement</span></span> | <span data-ttu-id="8f9f1-188">Wert</span><span class="sxs-lookup"><span data-stu-id="8f9f1-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f9f1-189">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f9f1-189">Minimum supported client</span></span><br/> | <span data-ttu-id="8f9f1-190">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f9f1-190">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8f9f1-191">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f9f1-191">Minimum supported server</span></span><br/> | <span data-ttu-id="8f9f1-192">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f9f1-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8f9f1-193">Header</span><span class="sxs-lookup"><span data-stu-id="8f9f1-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f9f1-194"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f9f1-194"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8f9f1-195">IDL</span><span class="sxs-lookup"><span data-stu-id="8f9f1-195">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8f9f1-196"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8f9f1-196"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8f9f1-197">DLL</span><span class="sxs-lookup"><span data-stu-id="8f9f1-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f9f1-198"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="8f9f1-198"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f9f1-199">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8f9f1-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f9f1-200">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="8f9f1-200">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="8f9f1-201">**Shellobjekt**</span><span class="sxs-lookup"><span data-stu-id="8f9f1-201">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 
