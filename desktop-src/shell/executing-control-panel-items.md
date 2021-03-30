---
description: Erläutert die Methoden zum Öffnen eines System Steuerungs Elements für Windows Vista und spätere Systeme sowie zum abdecken von Legacy-System Steuerungs Befehlen.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Ausführen von System Steuerungselementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaaac4b782273e0b4444fb2b5b6d3cab0b3599ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994934"
---
# <a name="executing-control-panel-items"></a><span data-ttu-id="61485-103">Ausführen von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="61485-103">Executing Control Panel Items</span></span>

> [!Note]  
> <span data-ttu-id="61485-104">Wenn Sie die Liste der kanonischen und Modulnamen für System Steuerungselemente suchen, finden Sie weitere Informationen unter [kanonische Namen von System Steuerungselementen](controlpanel-canonical-names.md).</span><span class="sxs-lookup"><span data-stu-id="61485-104">If you are looking for the list of canonical and module names for Control Panel items, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

 

<span data-ttu-id="61485-105">Es gibt zwei Möglichkeiten zum Öffnen eines System Steuerungs Elements:</span><span class="sxs-lookup"><span data-stu-id="61485-105">There are two ways to open a Control Panel item:</span></span>

-   <span data-ttu-id="61485-106">Der Benutzer kann die Systemsteuerung öffnen und dann ein Element öffnen, indem Sie auf das Element Symbol klicken oder doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="61485-106">The user can open Control Panel and then open an item by clicking or double-clicking the item's icon.</span></span>
-   <span data-ttu-id="61485-107">Der Benutzer oder eine Anwendung kann ein System Steuerungselement starten, indem es direkt über die Eingabeaufforderung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61485-107">The user or an application can start a Control Panel item by executing it directly from the command line prompt.</span></span>

<span data-ttu-id="61485-108">Eine Anwendung kann die Systemsteuerung Programm gesteuert mithilfe der [**winexec**](/windows/win32/api/winbase/nf-winbase-winexec) -Funktion öffnen.</span><span class="sxs-lookup"><span data-stu-id="61485-108">An application can open the Control Panel programmatically by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



<span data-ttu-id="61485-109">Im folgenden Beispiel wird gezeigt, wie eine Anwendung das System Steuerungselement mit dem Namen **MyCpl.cpl** mit der [**winexec**](/windows/win32/api/winbase/nf-winbase-winexec) -Funktion starten kann.</span><span class="sxs-lookup"><span data-stu-id="61485-109">The following example shows how an application can start the Control Panel item named **MyCpl.cpl** by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



<span data-ttu-id="61485-110">Wenn ein System Steuerungselement über eine Befehlszeile geöffnet wird, können Sie es anweisen, eine bestimmte Registerkarte im Element zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="61485-110">When a Control Panel item is opened through a command line, you can instruct it to open to a particular tab in the item.</span></span> <span data-ttu-id="61485-111">Aufgrund des Hinzufügens und Entfernens bestimmter Registerkarten in einigen Windows Vista-System Steuerungselementen hat sich die Nummerierung der Registerkarten in Windows XP möglicherweise geändert.</span><span class="sxs-lookup"><span data-stu-id="61485-111">Due to the addition and removal of certain tabs in some Windows Vista Control Panel items, the numbering of the tabs might have changed from that in Windows XP.</span></span> <span data-ttu-id="61485-112">Im folgenden Beispiel wird z. b. die vierte Registerkarte im System Element unter Windows XP und die dritte Registerkarte unter Windows Vista gestartet.</span><span class="sxs-lookup"><span data-stu-id="61485-112">For instance, the following example launches the fourth tab in the System item on Windows XP and the third tab on Windows Vista.</span></span>


```
control.exe sysdm.cpl,,3
```



<span data-ttu-id="61485-113">In diesem Thema wird Folgendes erörtert:</span><span class="sxs-lookup"><span data-stu-id="61485-113">This topic discusses the following:</span></span>

-   [<span data-ttu-id="61485-114">Kanonische Windows Vista-Namen</span><span class="sxs-lookup"><span data-stu-id="61485-114">Windows Vista Canonical Names</span></span>](#windows-vista-canonical-names)
-   [<span data-ttu-id="61485-115">Neue Befehle für Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61485-115">New Commands for Windows Vista</span></span>](#new-commands-for-windows-vista)
-   [<span data-ttu-id="61485-116">Ältere System Steuerungsbefehle</span><span class="sxs-lookup"><span data-stu-id="61485-116">Legacy Control Panel Commands</span></span>](#legacy-control-panel-commands)
-   [<span data-ttu-id="61485-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="61485-117">Related topics</span></span>](#related-topics)

## <a name="windows-vista-canonical-names"></a><span data-ttu-id="61485-118">Kanonische Windows Vista-Namen</span><span class="sxs-lookup"><span data-stu-id="61485-118">Windows Vista Canonical Names</span></span>

<span data-ttu-id="61485-119">In Windows Vista und höher ist die bevorzugte Methode zum Starten eines System Steuerungs Elements über eine Befehlszeile die Verwendung des kanonischen Namens des System Steuerungs Elements.</span><span class="sxs-lookup"><span data-stu-id="61485-119">In Windows Vista and later, the preferred method of launching a Control Panel item from a command line is to use the Control Panel item's canonical name.</span></span> <span data-ttu-id="61485-120">Ein kanonischer Name ist eine nicht lokalisierte Zeichenfolge, die das System Steuerungselement in der Registrierung deklariert.</span><span class="sxs-lookup"><span data-stu-id="61485-120">A canonical name is a non-localized string that the Control Panel item declares in the registry.</span></span> <span data-ttu-id="61485-121">Der Wert der Verwendung eines kanonischen Namens besteht darin, dass der Modulname des System Steuerungs Elements abstrahiert wird.</span><span class="sxs-lookup"><span data-stu-id="61485-121">The value of using a canonical name is that it abstracts the module name of the Control Panel item.</span></span> <span data-ttu-id="61485-122">Ein Element kann in einer DLL-Version implementiert und später als exe-Version neu implementiert werden oder dessen Modulname ändern.</span><span class="sxs-lookup"><span data-stu-id="61485-122">An item can be implemented in a .dll and later be reimplemented as a .exe or change its module name.</span></span> <span data-ttu-id="61485-123">Solange der kanonische Name unverändert bleibt, muss jedes Programm, das es mithilfe dieses kanonischen Namens öffnet, nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="61485-123">As long as the canonical name remains the same, then any program that opens it by using that canonical name does not need to be updated.</span></span>

<span data-ttu-id="61485-124">Gemäß der Konvention wird der kanonische Name als "corporationname. controlpanelitemname" formatiert.</span><span class="sxs-lookup"><span data-stu-id="61485-124">By convention, the canonical name is formed as "CorporationName.ControlPanelItemName".</span></span>

<span data-ttu-id="61485-125">Im folgenden Beispiel wird gezeigt, wie eine Anwendung das System Steuerungselement **Windows Update** mit [**winexec**](/windows/win32/api/winbase/nf-winbase-winexec)starten kann.</span><span class="sxs-lookup"><span data-stu-id="61485-125">The following example shows how an application can start the Control Panel item **Windows Update** with [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).</span></span>


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



<span data-ttu-id="61485-126">Wenn Sie ein System Steuerungselement mit dem kanonischen Namen starten möchten, verwenden Sie Folgendes: "% SystemRoot% \\ system32 \\control.exe/Name *CanonicalName*"</span><span class="sxs-lookup"><span data-stu-id="61485-126">To start a Control Panel item with its canonical name, use: "%systemroot%\\system32\\control.exe /name *canonicalName*"</span></span>

<span data-ttu-id="61485-127">Verwenden Sie Folgendes, um eine bestimmte Unterseite in einem Element zu öffnen oder mit zusätzlichen Parametern zu öffnen: "% SystemRoot% \\ system32 \\control.exe/Name **CanonicalName** /Seite **pagename**"</span><span class="sxs-lookup"><span data-stu-id="61485-127">To open a specific sub-page in an item, or to open it with additional parameters, use: "%systemroot%\\system32\\control.exe /name **canonicalName** /page **pageName**"</span></span>

<span data-ttu-id="61485-128">Eine Anwendung kann auch die [**iopencontrolpanel:: Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) -Methode implementieren, um System Steuerungselemente zu starten, einschließlich der Fähigkeit, eine bestimmte Unterseite zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="61485-128">An application can also implement the [**IOpenControlPanel::Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) method to launch Control Panel items, including the ability to open a specific sub-page.</span></span>

<span data-ttu-id="61485-129">Eine komplette Liste der kanonischen Namen von System Steuerungselementen finden Sie unter [kanonische Namen von System Steuerungselementen](controlpanel-canonical-names.md).</span><span class="sxs-lookup"><span data-stu-id="61485-129">For a complete list of Control Panel item canonical names, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

## <a name="new-commands-for-windows-vista"></a><span data-ttu-id="61485-130">Neue Befehle für Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61485-130">New Commands for Windows Vista</span></span>

<span data-ttu-id="61485-131">Unter Windows Vista sind einige Optionen, auf die von einem cpl-Modul unter Windows XP zugegriffen wurde, jetzt als exe-Dateien implementiert.</span><span class="sxs-lookup"><span data-stu-id="61485-131">On Windows Vista, some options that were accessed by a .cpl module on Windows XP are now implemented as .exe files.</span></span> <span data-ttu-id="61485-132">Dies bietet zusätzliche Sicherheit, da Standardbenutzer aufgefordert werden, Administrator Anmelde Informationen anzugeben, wenn versucht wird, die Dateien zu starten.</span><span class="sxs-lookup"><span data-stu-id="61485-132">This provides added security by allowing standard users to be prompted to provide administrator credentials when trying to launch the files.</span></span> <span data-ttu-id="61485-133">Optionen, die keine zusätzliche Sicherheit erfordern, werden über dieselben Befehlszeilen wie in Windows XP aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="61485-133">Options that do not require extra security are accessed by the same command lines that were used in Windows XP.</span></span> <span data-ttu-id="61485-134">Im folgenden finden Sie eine Liste der Befehle, die in Windows Vista verwendet werden, um auf bestimmte Registerkarten von System Steuerungselementen zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="61485-134">The following is a list of commands used in Windows Vista to access specific tabs of Control Panel items:</span></span>

### <a name="personalization"></a><span data-ttu-id="61485-135">Personalization</span><span class="sxs-lookup"><span data-stu-id="61485-135">Personalization</span></span>

-   <span data-ttu-id="61485-136">Schriftgröße und dpi:% windir% \\ system32 \\DpiScaling.exe</span><span class="sxs-lookup"><span data-stu-id="61485-136">Font size and DPI: %windir%\\system32\\DpiScaling.exe</span></span>
-   <span data-ttu-id="61485-137">Bildschirmauflösung:% windir% \\ system32 \\control.exe desk.cpl, Einstellungen,@Settings</span><span class="sxs-lookup"><span data-stu-id="61485-137">Screen resolution: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="61485-138">Anzeigeeinstellungen:% windir% \\ system32 \\control.exe desk.cpl, Einstellungen,@Settings</span><span class="sxs-lookup"><span data-stu-id="61485-138">Display settings: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="61485-139">Themen:% windir% \\ system32 \\control.exe desk.cpl, Designs,@Themes</span><span class="sxs-lookup"><span data-stu-id="61485-139">Themes: %windir%\\system32\\control.exe desk.cpl,Themes,@Themes</span></span>
-   <span data-ttu-id="61485-140">Bildschirmschoner:% windir% \\ system32 \\control.exe desk.cpl, Bildschirmschoner,@screensaver</span><span class="sxs-lookup"><span data-stu-id="61485-140">Screensaver: %windir%\\system32\\control.exe desk.cpl,screensaver,@screensaver</span></span>
-   <span data-ttu-id="61485-141">Multimonitor:% windir% \\ system32 \\control.exe desk.cpl, Monitor,@Monitor</span><span class="sxs-lookup"><span data-stu-id="61485-141">Multi-monitor: %windir%\\system32\\control.exe desk.cpl,Monitor,@Monitor</span></span>
-   <span data-ttu-id="61485-142">Farbschema:% windir% \\ system32 \\control.exe/Name Microsoft. Personalization/Seite pagefarbige zation</span><span class="sxs-lookup"><span data-stu-id="61485-142">Color Scheme: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageColorization</span></span>
-   <span data-ttu-id="61485-143">Desktop Hintergrund:% windir% \\ system32 \\control.exe/Name Microsoft. Personalization/Seite pgewallpaper</span><span class="sxs-lookup"><span data-stu-id="61485-143">Desktop background: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageWallpaper</span></span>

> [!Note]  
> <span data-ttu-id="61485-144">Starter-und Basic-Editionen unterstützen nicht control.exe/Name Microsoft. Personalization-Befehl.</span><span class="sxs-lookup"><span data-stu-id="61485-144">Starter and Basic Editions do not support control.exe /name Microsoft.Personalization command.</span></span>

 

### <a name="system"></a><span data-ttu-id="61485-145">System</span><span class="sxs-lookup"><span data-stu-id="61485-145">System</span></span>

-   <span data-ttu-id="61485-146">Leistung:% windir% \\ system32 \\SystemPropertiesPerformance.exe</span><span class="sxs-lookup"><span data-stu-id="61485-146">Performance: %windir%\\system32\\SystemPropertiesPerformance.exe</span></span>
-   <span data-ttu-id="61485-147">Remote Zugriff:% windir% \\ system32 \\SystemPropertiesRemote.exe</span><span class="sxs-lookup"><span data-stu-id="61485-147">Remote access: %windir%\\system32\\SystemPropertiesRemote.exe</span></span>
-   <span data-ttu-id="61485-148">Computer Name:% windir% \\ system32 \\SystemPropertiesComputerName.exe</span><span class="sxs-lookup"><span data-stu-id="61485-148">Computer name: %windir%\\system32\\SystemPropertiesComputerName.exe</span></span>
-   <span data-ttu-id="61485-149">System Schutz:% windir% \\ system32 \\SystemPropertiesProtection.exe</span><span class="sxs-lookup"><span data-stu-id="61485-149">System protection: %windir%\\system32\\SystemPropertiesProtection.exe</span></span>
-   <span data-ttu-id="61485-150">Erweiterte Systemeigenschaften:% windir% \\ system32 \\SystemPropertiesAdvanced.exe</span><span class="sxs-lookup"><span data-stu-id="61485-150">Advanced system properties: %windir%\\system32\\SystemPropertiesAdvanced.exe</span></span>

### <a name="programs-and-features"></a><span data-ttu-id="61485-151">Programme und Funktionen</span><span class="sxs-lookup"><span data-stu-id="61485-151">Programs and Features</span></span>

-   <span data-ttu-id="61485-152">Software hinzufügen oder entfernen:% windir% \\ system32 \\control.exe/Name Microsoft. Program Sand Features</span><span class="sxs-lookup"><span data-stu-id="61485-152">Add or remove programs: %windir%\\system32\\control.exe /name Microsoft.ProgramsAndFeatures</span></span>
-   <span data-ttu-id="61485-153">Windows-Features:% windir% \\ system32 \\OptionalFeatures.exe</span><span class="sxs-lookup"><span data-stu-id="61485-153">Windows features: %windir%\\system32\\OptionalFeatures.exe</span></span>

### <a name="regional-and-language-options"></a><span data-ttu-id="61485-154">Regions- und Sprachoptionen</span><span class="sxs-lookup"><span data-stu-id="61485-154">Regional and Language Options</span></span>

-   <span data-ttu-id="61485-155">Tastatur:% systemroot% \\ system32 \\control.exe/Name Microsoft. regionandlanguageoptions/Seite/p: "Keyboard"</span><span class="sxs-lookup"><span data-stu-id="61485-155">Keyboard: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"</span></span>
-   <span data-ttu-id="61485-156">Speicherort:% systemroot% \\ system32 \\control.exe/Name Microsoft. regionandlanguageoptions/Seite/p: "Location"</span><span class="sxs-lookup"><span data-stu-id="61485-156">Location: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"</span></span>
-   <span data-ttu-id="61485-157">Verwaltung:% systemroot% \\ system32 \\control.exe/Name Microsoft. regionandlanguageoptions/Seite/p: "administrative"</span><span class="sxs-lookup"><span data-stu-id="61485-157">Administrative: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"</span></span>

### <a name="folder-options"></a><span data-ttu-id="61485-158">Ordneroptionen</span><span class="sxs-lookup"><span data-stu-id="61485-158">Folder Options</span></span>

-   <span data-ttu-id="61485-159">Ordner Suche:% windir% \\ system32 \\rundll32.exe shell32.dll, options \_ Rundung 2</span><span class="sxs-lookup"><span data-stu-id="61485-159">Folder searching: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 2</span></span>
-   <span data-ttu-id="61485-160">Dateizuordnungen:% windir% \\ system32 \\control.exe/Name Microsoft. defaultprograms/Seite pagefileassoc</span><span class="sxs-lookup"><span data-stu-id="61485-160">File associations: %windir%\\system32\\control.exe /name Microsoft.DefaultPrograms /page pageFileAssoc</span></span>
-   <span data-ttu-id="61485-161">Ansicht:% windir% \\ system32 \\rundll32.exe shell32.dll, options \_ Rundung 7</span><span class="sxs-lookup"><span data-stu-id="61485-161">View: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 7</span></span>
-   <span data-ttu-id="61485-162">Allgemein:% windir% \\ system32 \\rundll32.exe shell32.dll, options \_ Rundung 0</span><span class="sxs-lookup"><span data-stu-id="61485-162">General: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 0</span></span>

### <a name="power-options"></a><span data-ttu-id="61485-163">Energieoptionen</span><span class="sxs-lookup"><span data-stu-id="61485-163">Power Options</span></span>

-   <span data-ttu-id="61485-164">Aktuelle Plan Einstellungen bearbeiten:% windir% \\ system32 \\control.exe/Name Microsoft. poweroptions/Seite pagePlanSettings</span><span class="sxs-lookup"><span data-stu-id="61485-164">Edit current plan settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pagePlanSettings</span></span>
-   <span data-ttu-id="61485-165">System Einstellungen:% windir% \\ system32 \\control.exe/Name Microsoft. poweroptions/Seite pageglobalsettings</span><span class="sxs-lookup"><span data-stu-id="61485-165">System settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageGlobalSettings</span></span>
-   <span data-ttu-id="61485-166">Erstellen Sie einen Energie Sparplan:% windir% \\ system32 \\control.exe/Name Microsoft. poweroptions/Seite pagekreatenewplan</span><span class="sxs-lookup"><span data-stu-id="61485-166">Create a power plan: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageCreateNewPlan</span></span>
-   <span data-ttu-id="61485-167">Es ist kein kanonischer Befehl für die Seite Erweiterte Einstellungen vorhanden. der Zugriff erfolgt auf ältere Weise:% windir% \\ system32 \\control.exe powercfg.cpl,, 3</span><span class="sxs-lookup"><span data-stu-id="61485-167">There is no canonical command for the Advanced Settings page, it is accessed in the older manner: %windir%\\system32\\control.exe powercfg.cpl,,3</span></span>

## <a name="legacy-control-panel-commands"></a><span data-ttu-id="61485-168">Ältere System Steuerungsbefehle</span><span class="sxs-lookup"><span data-stu-id="61485-168">Legacy Control Panel Commands</span></span>

<span data-ttu-id="61485-169">Wenn Sie die [**winexec**](/windows/win32/api/winbase/nf-winbase-winexec) -Funktion verwenden, kann das System spezielle System Steuerungsbefehle erkennen.</span><span class="sxs-lookup"><span data-stu-id="61485-169">When you use the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function, the system can recognize special Control Panel commands.</span></span> <span data-ttu-id="61485-170">Mit diesen Befehlen wird Windows Vista vorab angezeigt.</span><span class="sxs-lookup"><span data-stu-id="61485-170">These commands predate Windows Vista.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61485-171">control.exe Desktop</span><span class="sxs-lookup"><span data-stu-id="61485-171">control.exe desktop</span></span></td>
<td><span data-ttu-id="61485-172">Öffnet das Fenster <strong>Eigenschaften anzeigen</strong> .</span><span class="sxs-lookup"><span data-stu-id="61485-172">Launches the <strong>Display Properties</strong> window.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="61485-173">Dieser Befehl wird von den Starter-und Basic-Editionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="61485-173">Starter and Basic Editions do not support this command.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61485-174">control.exe Farbe</span><span class="sxs-lookup"><span data-stu-id="61485-174">control.exe color</span></span></td>
<td><span data-ttu-id="61485-175">Öffnet das Fenster <strong>Anzeigeeigenschaften</strong> <strong>mit der vorab</strong> ausgewählten Registerkarte Darstellung.</span><span class="sxs-lookup"><span data-stu-id="61485-175">Launches the <strong>Display Properties</strong> window with the <strong>Appearance</strong> tab preselected.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61485-176">control.exe Datum/-Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="61485-176">control.exe date/time</span></span></td>
<td><span data-ttu-id="61485-177">Öffnet das Fenster mit den <strong>Eigenschaften für Datum und Uhrzeit</strong> .</span><span class="sxs-lookup"><span data-stu-id="61485-177">Launches the <strong>Date and Time Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61485-178">control.exe International</span><span class="sxs-lookup"><span data-stu-id="61485-178">control.exe international</span></span></td>
<td><span data-ttu-id="61485-179">Öffnet das Fenster Regions <strong>-und Sprachoptionen</strong> .</span><span class="sxs-lookup"><span data-stu-id="61485-179">Launches the <strong>Regional and Language Options</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61485-180">control.exe Maus</span><span class="sxs-lookup"><span data-stu-id="61485-180">control.exe mouse</span></span></td>
<td><span data-ttu-id="61485-181">Öffnet das Fenster mit den <strong>Maus Eigenschaften</strong> .</span><span class="sxs-lookup"><span data-stu-id="61485-181">Launches the <strong>Mouse Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61485-182">control.exe Tastatur</span><span class="sxs-lookup"><span data-stu-id="61485-182">control.exe keyboard</span></span></td>
<td><span data-ttu-id="61485-183">Öffnet das Fenster <strong>Tastatur Eigenschaften</strong> .</span><span class="sxs-lookup"><span data-stu-id="61485-183">Launches the <strong>Keyboard Properties</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61485-184">control.exe Drucker</span><span class="sxs-lookup"><span data-stu-id="61485-184">control.exe printers</span></span></td>
<td><span data-ttu-id="61485-185">Zeigt den Ordner <strong>Drucker und Faxe</strong> an.</span><span class="sxs-lookup"><span data-stu-id="61485-185">Displays the <strong>Printers and Faxes</strong> folder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61485-186">control.exe Schriftarten</span><span class="sxs-lookup"><span data-stu-id="61485-186">control.exe fonts</span></span></td>
<td><span data-ttu-id="61485-187">Zeigt den Ordner " <strong>Fonts</strong> " an.</span><span class="sxs-lookup"><span data-stu-id="61485-187">Displays the <strong>Fonts</strong> folder.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="61485-188">Für Windows 2000-Systeme und spätere Systeme:</span><span class="sxs-lookup"><span data-stu-id="61485-188">For Windows 2000 and later systems:</span></span>



|                            |                                                          |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="61485-189">control.exe Ordner</span><span class="sxs-lookup"><span data-stu-id="61485-189">control.exe folders</span></span>        | <span data-ttu-id="61485-190">Öffnet das Fenster **Ordneroptionen** .</span><span class="sxs-lookup"><span data-stu-id="61485-190">Launches the **Folder Options** window.</span></span>                  |
| <span data-ttu-id="61485-191">control.exe NetWare</span><span class="sxs-lookup"><span data-stu-id="61485-191">control.exe netware</span></span>        | <span data-ttu-id="61485-192">Hiermit wird das **Novell NetWare** -Fenster (sofern installiert) gestartet.</span><span class="sxs-lookup"><span data-stu-id="61485-192">Launches the **Novell NetWare** window (if installed).</span></span>   |
| <span data-ttu-id="61485-193">control.exe Telefonie</span><span class="sxs-lookup"><span data-stu-id="61485-193">control.exe telephony</span></span>      | <span data-ttu-id="61485-194">Öffnet das Fenster " **Telefon-und Modem Optionen** ".</span><span class="sxs-lookup"><span data-stu-id="61485-194">Launches the **Phone and Modem Options** window.</span></span>         |
| <span data-ttu-id="61485-195">control.exe admintools</span><span class="sxs-lookup"><span data-stu-id="61485-195">control.exe admintools</span></span>     | <span data-ttu-id="61485-196">Zeigt den Ordner **Verwaltung** an.</span><span class="sxs-lookup"><span data-stu-id="61485-196">Displays the **Administrative Tools** folder.</span></span>            |
| <span data-ttu-id="61485-197">control.exe schedtasks</span><span class="sxs-lookup"><span data-stu-id="61485-197">control.exe schedtasks</span></span>     | <span data-ttu-id="61485-198">Zeigt den Ordner " **geplante Aufgaben** " an.</span><span class="sxs-lookup"><span data-stu-id="61485-198">Displays the **Scheduled Tasks** folder.</span></span>                 |
| <span data-ttu-id="61485-199">control.exe netconnections</span><span class="sxs-lookup"><span data-stu-id="61485-199">control.exe netconnections</span></span> | <span data-ttu-id="61485-200">Zeigt den Ordner **Netzwerkverbindungen** an.</span><span class="sxs-lookup"><span data-stu-id="61485-200">Displays the **Network Connections** folder.</span></span>             |
| <span data-ttu-id="61485-201">control.exe Infrarot</span><span class="sxs-lookup"><span data-stu-id="61485-201">control.exe infrared</span></span>       | <span data-ttu-id="61485-202">Hiermit wird das Fenster des **Infrarot Monitors** (sofern installiert) gestartet.</span><span class="sxs-lookup"><span data-stu-id="61485-202">Launches the **Infrared Monitor** window (if installed).</span></span> |
| <span data-ttu-id="61485-203">control.exe Benutzer Kennwörter</span><span class="sxs-lookup"><span data-stu-id="61485-203">control.exe userpasswords</span></span>  | <span data-ttu-id="61485-204">Öffnet das Fenster **Benutzerkonten** .</span><span class="sxs-lookup"><span data-stu-id="61485-204">Launches the **User Accounts** window.</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="61485-205">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="61485-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61485-206">System Steuerungselemente</span><span class="sxs-lookup"><span data-stu-id="61485-206">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="61485-207">Richtlinien zur Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="61485-207">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="61485-208">System Steuerungselemente werden registriert</span><span class="sxs-lookup"><span data-stu-id="61485-208">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="61485-209">Verwenden von CPlApplet</span><span class="sxs-lookup"><span data-stu-id="61485-209">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="61485-210">Nachrichtenverarbeitung in der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="61485-210">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="61485-211">Erweitern von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="61485-211">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="61485-212">Zuweisen von System Steuerungs Kategorien</span><span class="sxs-lookup"><span data-stu-id="61485-212">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="61485-213">Erstellen von durchsuchbaren Aufgaben Verknüpfungen für ein System Steuerungselement</span><span class="sxs-lookup"><span data-stu-id="61485-213">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="61485-214">Zugreifen auf die Systemsteuerung im abgesicherten Modus unter Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61485-214">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
