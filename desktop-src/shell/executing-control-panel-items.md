---
description: Erläutert Methoden zum Öffnen eines Systemsteuerung Elements für Windows Vista- und höhere Systeme sowie zum Abdecken von Legacybefehlen Systemsteuerung.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Ausführen von Systemsteuerung Elementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cb6ae2fa08231d3876e1a5a636e404f519f4a6
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581758"
---
# <a name="executing-control-panel-items"></a><span data-ttu-id="1fb54-103">Ausführen von Systemsteuerung Elementen</span><span class="sxs-lookup"><span data-stu-id="1fb54-103">Executing Control Panel Items</span></span>

> [!Note]  
> <span data-ttu-id="1fb54-104">Wenn Sie nach der Liste der kanonischen und Modulnamen für Systemsteuerung Elemente suchen, finden Sie weitere Informationen unter [Kanonische Namen von Systemsteuerung Elementen.](controlpanel-canonical-names.md)</span><span class="sxs-lookup"><span data-stu-id="1fb54-104">If you are looking for the list of canonical and module names for Control Panel items, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

 

<span data-ttu-id="1fb54-105">Es gibt zwei Möglichkeiten, ein Systemsteuerung Element zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="1fb54-105">There are two ways to open a Control Panel item:</span></span>

-   <span data-ttu-id="1fb54-106">Der Benutzer kann Systemsteuerung öffnen und dann ein Element öffnen, indem er auf das Symbol des Elements klickt oder doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="1fb54-106">The user can open Control Panel and then open an item by clicking or double-clicking the item's icon.</span></span>
-   <span data-ttu-id="1fb54-107">Der Benutzer oder eine Anwendung kann ein Systemsteuerung Element starten, indem er es direkt über die Eingabeaufforderung ausführt.</span><span class="sxs-lookup"><span data-stu-id="1fb54-107">The user or an application can start a Control Panel item by executing it directly from the command line prompt.</span></span>

<span data-ttu-id="1fb54-108">Eine Anwendung kann die Systemsteuerung programmgesteuert mithilfe der [**WinExec-Funktion**](/windows/win32/api/winbase/nf-winbase-winexec) öffnen.</span><span class="sxs-lookup"><span data-stu-id="1fb54-108">An application can open the Control Panel programmatically by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



<span data-ttu-id="1fb54-109">Das folgende Beispiel zeigt, wie eine Anwendung das Systemsteuerung Element namens **MyCpl.cpl** mithilfe der [**WinExec-Funktion**](/windows/win32/api/winbase/nf-winbase-winexec) starten kann.</span><span class="sxs-lookup"><span data-stu-id="1fb54-109">The following example shows how an application can start the Control Panel item named **MyCpl.cpl** by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



<span data-ttu-id="1fb54-110">Wenn ein Systemsteuerung Element über eine Befehlszeile geöffnet wird, können Sie es anweisen, eine bestimmte Registerkarte im Element zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1fb54-110">When a Control Panel item is opened through a command line, you can instruct it to open to a particular tab in the item.</span></span> <span data-ttu-id="1fb54-111">Aufgrund des Hinzufügens und Entfernens bestimmter Registerkarten in einigen Windows Vista Systemsteuerung Elementen hat sich die Nummerierung der Registerkarten möglicherweise von der Nummerierung in Windows XP geändert.</span><span class="sxs-lookup"><span data-stu-id="1fb54-111">Due to the addition and removal of certain tabs in some Windows Vista Control Panel items, the numbering of the tabs might have changed from that in Windows XP.</span></span> <span data-ttu-id="1fb54-112">Im folgenden Beispiel wird beispielsweise die vierte Registerkarte im Element System auf Windows XP und die dritte Registerkarte auf Windows Vista gestartet.</span><span class="sxs-lookup"><span data-stu-id="1fb54-112">For instance, the following example launches the fourth tab in the System item on Windows XP and the third tab on Windows Vista.</span></span>


```
control.exe sysdm.cpl,,3
```



<span data-ttu-id="1fb54-113">In diesem Thema wird Folgendes erörtert:</span><span class="sxs-lookup"><span data-stu-id="1fb54-113">This topic discusses the following:</span></span>

-   [<span data-ttu-id="1fb54-114">Windows Kanonische Vista-Namen</span><span class="sxs-lookup"><span data-stu-id="1fb54-114">Windows Vista Canonical Names</span></span>](#windows-vista-canonical-names)
-   [<span data-ttu-id="1fb54-115">Neue Befehle für Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1fb54-115">New Commands for Windows Vista</span></span>](#new-commands-for-windows-vista)
-   [<span data-ttu-id="1fb54-116">Legacybefehle für Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="1fb54-116">Legacy Control Panel Commands</span></span>](#legacy-control-panel-commands)
-   [<span data-ttu-id="1fb54-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1fb54-117">Related topics</span></span>](#related-topics)

## <a name="windows-vista-canonical-names"></a><span data-ttu-id="1fb54-118">Windows Kanonische Vista-Namen</span><span class="sxs-lookup"><span data-stu-id="1fb54-118">Windows Vista Canonical Names</span></span>

<span data-ttu-id="1fb54-119">In Windows Vista und höher besteht die bevorzugte Methode zum Starten eines Systemsteuerung Elements über eine Befehlszeile darin, den kanonischen Namen des Systemsteuerung Elements zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1fb54-119">In Windows Vista and later, the preferred method of launching a Control Panel item from a command line is to use the Control Panel item's canonical name.</span></span> <span data-ttu-id="1fb54-120">Ein kanonischer Name ist eine nicht lokalisierte Zeichenfolge, die vom Systemsteuerung Element in der Registrierung deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="1fb54-120">A canonical name is a non-localized string that the Control Panel item declares in the registry.</span></span> <span data-ttu-id="1fb54-121">Der Wert der Verwendung eines kanonischen Namens ist, dass der Modulname des Systemsteuerung Elements abstrahiert wird.</span><span class="sxs-lookup"><span data-stu-id="1fb54-121">The value of using a canonical name is that it abstracts the module name of the Control Panel item.</span></span> <span data-ttu-id="1fb54-122">Ein Element kann in einem .dll implementiert und später als .exe erneut implementiert oder sein Modulname geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1fb54-122">An item can be implemented in a .dll and later be reimplemented as a .exe or change its module name.</span></span> <span data-ttu-id="1fb54-123">Solange der kanonische Name gleich bleibt, muss jedes Programm, das ihn mit diesem kanonischen Namen öffnet, nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1fb54-123">As long as the canonical name remains the same, then any program that opens it by using that canonical name does not need to be updated.</span></span>

<span data-ttu-id="1fb54-124">Gemäß der Konvention wird der kanonische Name als "CorporationName.ControlPanelItemName" gebildet.</span><span class="sxs-lookup"><span data-stu-id="1fb54-124">By convention, the canonical name is formed as "CorporationName.ControlPanelItemName".</span></span>

<span data-ttu-id="1fb54-125">Das folgende Beispiel zeigt, wie eine Anwendung das Systemsteuerung Element **Windows Update** mit [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec)starten kann.</span><span class="sxs-lookup"><span data-stu-id="1fb54-125">The following example shows how an application can start the Control Panel item **Windows Update** with [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).</span></span>


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



<span data-ttu-id="1fb54-126">Verwenden Sie "%systemroot% \\ system32control.exe \\ /name *canonicalName",* um ein Systemsteuerung Element mit seinem kanonischen Namen zu starten.</span><span class="sxs-lookup"><span data-stu-id="1fb54-126">To start a Control Panel item with its canonical name, use: "%systemroot%\\system32\\control.exe /name *canonicalName*"</span></span>

<span data-ttu-id="1fb54-127">Verwenden Sie "%systemroot% \\ system32control.exe \\ /name **canonicalName** /page **pageName",** um eine bestimmte Unterseite in einem Element zu öffnen oder sie mit zusätzlichen Parametern zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1fb54-127">To open a specific sub-page in an item, or to open it with additional parameters, use: "%systemroot%\\system32\\control.exe /name **canonicalName** /page **pageName**"</span></span>

<span data-ttu-id="1fb54-128">Eine Anwendung kann auch die [**IOpenControlPanel::Open-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) implementieren, um Systemsteuerung Elemente zu starten, einschließlich der Möglichkeit, eine bestimmte Unterseite zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1fb54-128">An application can also implement the [**IOpenControlPanel::Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) method to launch Control Panel items, including the ability to open a specific sub-page.</span></span>

<span data-ttu-id="1fb54-129">Eine vollständige Liste der kanonischen Namen Systemsteuerung Elements finden Sie unter [Kanonische Namen von Systemsteuerung Items](controlpanel-canonical-names.md).</span><span class="sxs-lookup"><span data-stu-id="1fb54-129">For a complete list of Control Panel item canonical names, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

## <a name="new-commands-for-windows-vista"></a><span data-ttu-id="1fb54-130">Neue Befehle für Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1fb54-130">New Commands for Windows Vista</span></span>

<span data-ttu-id="1fb54-131">Auf Windows Vista werden einige Optionen, auf die von einem .cpl-Modul auf Windows XP zugegriffen wurde, jetzt als .exe-Dateien implementiert.</span><span class="sxs-lookup"><span data-stu-id="1fb54-131">On Windows Vista, some options that were accessed by a .cpl module on Windows XP are now implemented as .exe files.</span></span> <span data-ttu-id="1fb54-132">Dies bietet zusätzliche Sicherheit, da Standardbenutzer beim Versuch, die Dateien zu starten, aufgefordert werden, Administratoranmeldeinformationen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1fb54-132">This provides added security by allowing standard users to be prompted to provide administrator credentials when trying to launch the files.</span></span> <span data-ttu-id="1fb54-133">Auf Optionen, die keine zusätzliche Sicherheit erfordern, wird über die gleichen Befehlszeilen zugegriffen, die in Windows XP verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="1fb54-133">Options that do not require extra security are accessed by the same command lines that were used in Windows XP.</span></span> <span data-ttu-id="1fb54-134">Es folgt eine Liste der Befehle, die in Windows Vista verwendet werden, um auf bestimmte Registerkarten von Systemsteuerung Elementen zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="1fb54-134">The following is a list of commands used in Windows Vista to access specific tabs of Control Panel items:</span></span>

### <a name="personalization"></a><span data-ttu-id="1fb54-135">Personalization</span><span class="sxs-lookup"><span data-stu-id="1fb54-135">Personalization</span></span>

-   <span data-ttu-id="1fb54-136">Schriftgrad und DPI: %windir% \\ system32 \\DpiScaling.exe</span><span class="sxs-lookup"><span data-stu-id="1fb54-136">Font size and DPI: %windir%\\system32\\DpiScaling.exe</span></span>
-   <span data-ttu-id="1fb54-137">Bildschirmauflösung: %windir% \\ system32 \\control.exe desk.cpl,Einstellungen,@Settings</span><span class="sxs-lookup"><span data-stu-id="1fb54-137">Screen resolution: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="1fb54-138">Anzeigeeinstellungen: %windir% \\ system32 \\control.exe desk.cpl,Einstellungen,@Settings</span><span class="sxs-lookup"><span data-stu-id="1fb54-138">Display settings: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="1fb54-139">Designs: %windir% \\ system32 \\control.exe desk.cpl,Themes,@Themes</span><span class="sxs-lookup"><span data-stu-id="1fb54-139">Themes: %windir%\\system32\\control.exe desk.cpl,Themes,@Themes</span></span>
-   <span data-ttu-id="1fb54-140">Bildschirmschoner: %windir% \\ system32 \\control.exe desk.cpl,screensaver,@screensaver</span><span class="sxs-lookup"><span data-stu-id="1fb54-140">Screensaver: %windir%\\system32\\control.exe desk.cpl,screensaver,@screensaver</span></span>
-   <span data-ttu-id="1fb54-141">Multimonitor: %windir% \\ system32 \\control.exe desk.cpl,Monitor,@Monitor</span><span class="sxs-lookup"><span data-stu-id="1fb54-141">Multi-monitor: %windir%\\system32\\control.exe desk.cpl,Monitor,@Monitor</span></span>
-   <span data-ttu-id="1fb54-142">Farbschema: %windir% \\ system32 \\control.exe /name Microsoft.Personalization /pageColorization</span><span class="sxs-lookup"><span data-stu-id="1fb54-142">Color Scheme: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageColorization</span></span>
-   <span data-ttu-id="1fb54-143">Desktophintergrund: %windir% \\ system32 \\control.exe /name Microsoft.Personalization /pageWallpaper</span><span class="sxs-lookup"><span data-stu-id="1fb54-143">Desktop background: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageWallpaper</span></span>

> [!Note]  
> <span data-ttu-id="1fb54-144">Starter- und Basic-Editionen unterstützen control.exe Befehl /name Microsoft.Personalization nicht.</span><span class="sxs-lookup"><span data-stu-id="1fb54-144">Starter and Basic Editions do not support control.exe /name Microsoft.Personalization command.</span></span>

 

### <a name="system"></a><span data-ttu-id="1fb54-145">System</span><span class="sxs-lookup"><span data-stu-id="1fb54-145">System</span></span>

-   <span data-ttu-id="1fb54-146">Leistung: %windir% \\ system32 \\SystemPropertiesPerformance.exe</span><span class="sxs-lookup"><span data-stu-id="1fb54-146">Performance: %windir%\\system32\\SystemPropertiesPerformance.exe</span></span>
-   <span data-ttu-id="1fb54-147">Remotezugriff: %windir% \\ system32 \\SystemPropertiesRemote.exe</span><span class="sxs-lookup"><span data-stu-id="1fb54-147">Remote access: %windir%\\system32\\SystemPropertiesRemote.exe</span></span>
-   <span data-ttu-id="1fb54-148">Computername: %windir% \\ system32 \\SystemPropertiesComputerName.exe</span><span class="sxs-lookup"><span data-stu-id="1fb54-148">Computer name: %windir%\\system32\\SystemPropertiesComputerName.exe</span></span>
-   <span data-ttu-id="1fb54-149">Systemschutz: %windir% \\ system32 \\SystemPropertiesProtection.exe</span><span class="sxs-lookup"><span data-stu-id="1fb54-149">System protection: %windir%\\system32\\SystemPropertiesProtection.exe</span></span>
-   <span data-ttu-id="1fb54-150">Erweiterte Systemeigenschaften: %windir% \\ system32 \\SystemPropertiesAdvanced.exe</span><span class="sxs-lookup"><span data-stu-id="1fb54-150">Advanced system properties: %windir%\\system32\\SystemPropertiesAdvanced.exe</span></span>

### <a name="programs-and-features"></a><span data-ttu-id="1fb54-151">Programme und Features</span><span class="sxs-lookup"><span data-stu-id="1fb54-151">Programs and Features</span></span>

-   <span data-ttu-id="1fb54-152">Hinzufügen oder Entfernen von Programmen: %windir% \\ system32 \\control.exe /name Microsoft.ProgramsAndFeatures</span><span class="sxs-lookup"><span data-stu-id="1fb54-152">Add or remove programs: %windir%\\system32\\control.exe /name Microsoft.ProgramsAndFeatures</span></span>
-   <span data-ttu-id="1fb54-153">Windows Features: %windir% \\ system32 \\OptionalFeatures.exe</span><span class="sxs-lookup"><span data-stu-id="1fb54-153">Windows features: %windir%\\system32\\OptionalFeatures.exe</span></span>

### <a name="regional-and-language-options"></a><span data-ttu-id="1fb54-154">Regions- und Sprachoptionen</span><span class="sxs-lookup"><span data-stu-id="1fb54-154">Regional and Language Options</span></span>

-   <span data-ttu-id="1fb54-155">Tastatur: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"</span><span class="sxs-lookup"><span data-stu-id="1fb54-155">Keyboard: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"</span></span>
-   <span data-ttu-id="1fb54-156">Speicherort: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"</span><span class="sxs-lookup"><span data-stu-id="1fb54-156">Location: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"</span></span>
-   <span data-ttu-id="1fb54-157">Administrator: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"</span><span class="sxs-lookup"><span data-stu-id="1fb54-157">Administrative: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"</span></span>

### <a name="folder-options"></a><span data-ttu-id="1fb54-158">Ordneroptionen</span><span class="sxs-lookup"><span data-stu-id="1fb54-158">Folder Options</span></span>

-   <span data-ttu-id="1fb54-159">Ordnersuche: %windir% \\ system32 \\rundll32.exe shell32.dll,Optionen \_ RunDLL 2</span><span class="sxs-lookup"><span data-stu-id="1fb54-159">Folder searching: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 2</span></span>
-   <span data-ttu-id="1fb54-160">Dateizuordnungen: %windir% \\ system32 \\control.exe /name Microsoft.DefaultPrograms /pagefileAssoc</span><span class="sxs-lookup"><span data-stu-id="1fb54-160">File associations: %windir%\\system32\\control.exe /name Microsoft.DefaultPrograms /page pageFileAssoc</span></span>
-   <span data-ttu-id="1fb54-161">Ansicht: %windir% \\ system32 \\rundll32.exe shell32.dll,Optionen \_ RunDLL 7</span><span class="sxs-lookup"><span data-stu-id="1fb54-161">View: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 7</span></span>
-   <span data-ttu-id="1fb54-162">Allgemein: %windir% \\ system32 \\rundll32.exe shell32.dll,Optionen \_ RunDLL 0</span><span class="sxs-lookup"><span data-stu-id="1fb54-162">General: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 0</span></span>

### <a name="power-options"></a><span data-ttu-id="1fb54-163">Energieoptionen</span><span class="sxs-lookup"><span data-stu-id="1fb54-163">Power Options</span></span>

-   <span data-ttu-id="1fb54-164">Aktuelle Planeinstellungen bearbeiten: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /pagePlanSettings</span><span class="sxs-lookup"><span data-stu-id="1fb54-164">Edit current plan settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pagePlanSettings</span></span>
-   <span data-ttu-id="1fb54-165">Systemeinstellungen: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /page pageGlobalSettings</span><span class="sxs-lookup"><span data-stu-id="1fb54-165">System settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageGlobalSettings</span></span>
-   <span data-ttu-id="1fb54-166">Erstellen eines Energiesparplans: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /pageCreateNewPlan</span><span class="sxs-lookup"><span data-stu-id="1fb54-166">Create a power plan: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageCreateNewPlan</span></span>
-   <span data-ttu-id="1fb54-167">Es gibt keinen kanonischen Befehl für die Seite Advanced Einstellungen, auf die in der älteren Weise zugegriffen wird: %windir% \\ system32 \\control.exe powercfg.cpl,,3</span><span class="sxs-lookup"><span data-stu-id="1fb54-167">There is no canonical command for the Advanced Settings page, it is accessed in the older manner: %windir%\\system32\\control.exe powercfg.cpl,,3</span></span>

## <a name="legacy-control-panel-commands"></a><span data-ttu-id="1fb54-168">Legacybefehle für Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="1fb54-168">Legacy Control Panel Commands</span></span>

<span data-ttu-id="1fb54-169">Wenn Sie die [**WinExec-Funktion**](/windows/win32/api/winbase/nf-winbase-winexec) verwenden, kann das System spezielle Systemsteuerung Befehle erkennen.</span><span class="sxs-lookup"><span data-stu-id="1fb54-169">When you use the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function, the system can recognize special Control Panel commands.</span></span> <span data-ttu-id="1fb54-170">Diese Befehle stellen Windows Vista voraus.</span><span class="sxs-lookup"><span data-stu-id="1fb54-170">These commands predate Windows Vista.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1fb54-171">control.exe Desktop</span><span class="sxs-lookup"><span data-stu-id="1fb54-171">control.exe desktop</span></span></td>
<td><span data-ttu-id="1fb54-172">Startet das <strong>fenster Anzeigeeigenschaften.</strong></span><span class="sxs-lookup"><span data-stu-id="1fb54-172">Launches the <strong>Display Properties</strong> window.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="1fb54-173">Starter- und Basic-Editionen unterstützen diesen Befehl nicht.</span><span class="sxs-lookup"><span data-stu-id="1fb54-173">Starter and Basic Editions do not support this command.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fb54-174">control.exe Farbe</span><span class="sxs-lookup"><span data-stu-id="1fb54-174">control.exe color</span></span></td>
<td><span data-ttu-id="1fb54-175">Startet das <strong>fenster Anzeigeeigenschaften,</strong> in dem die Registerkarte <strong>Darstellung</strong> vorab ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="1fb54-175">Launches the <strong>Display Properties</strong> window with the <strong>Appearance</strong> tab preselected.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fb54-176">Datum/Uhrzeit control.exe</span><span class="sxs-lookup"><span data-stu-id="1fb54-176">control.exe date/time</span></span></td>
<td><span data-ttu-id="1fb54-177">Öffnet das Fenster <strong>Datums- und Uhrzeiteigenschaften.</strong></span><span class="sxs-lookup"><span data-stu-id="1fb54-177">Launches the <strong>Date and Time Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fb54-178">control.exe international</span><span class="sxs-lookup"><span data-stu-id="1fb54-178">control.exe international</span></span></td>
<td><span data-ttu-id="1fb54-179">Öffnet das Fenster <strong>Regions- und Sprachoptionen.</strong></span><span class="sxs-lookup"><span data-stu-id="1fb54-179">Launches the <strong>Regional and Language Options</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fb54-180">control.exe Maus</span><span class="sxs-lookup"><span data-stu-id="1fb54-180">control.exe mouse</span></span></td>
<td><span data-ttu-id="1fb54-181">Öffnet das Fenster <strong>Mauseigenschaften.</strong></span><span class="sxs-lookup"><span data-stu-id="1fb54-181">Launches the <strong>Mouse Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fb54-182">control.exe Tastatur</span><span class="sxs-lookup"><span data-stu-id="1fb54-182">control.exe keyboard</span></span></td>
<td><span data-ttu-id="1fb54-183">Öffnet das Fenster <strong>Tastatureigenschaften.</strong></span><span class="sxs-lookup"><span data-stu-id="1fb54-183">Launches the <strong>Keyboard Properties</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fb54-184">control.exe Drucker</span><span class="sxs-lookup"><span data-stu-id="1fb54-184">control.exe printers</span></span></td>
<td><span data-ttu-id="1fb54-185">Zeigt den Ordner <strong>Drucker und Faxe</strong> an.</span><span class="sxs-lookup"><span data-stu-id="1fb54-185">Displays the <strong>Printers and Faxes</strong> folder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fb54-186">control.exe Schriftarten</span><span class="sxs-lookup"><span data-stu-id="1fb54-186">control.exe fonts</span></span></td>
<td><span data-ttu-id="1fb54-187">Zeigt den Ordner <strong>Schriftarten an.</strong></span><span class="sxs-lookup"><span data-stu-id="1fb54-187">Displays the <strong>Fonts</strong> folder.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1fb54-188">Für Windows Systeme ab 2000:</span><span class="sxs-lookup"><span data-stu-id="1fb54-188">For Windows 2000 and later systems:</span></span>



| <span data-ttu-id="1fb54-189">Get-Help</span><span class="sxs-lookup"><span data-stu-id="1fb54-189">Command</span></span>                    | <span data-ttu-id="1fb54-190">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1fb54-190">Description</span></span>                                              |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="1fb54-191">control.exe Ordner</span><span class="sxs-lookup"><span data-stu-id="1fb54-191">control.exe folders</span></span>        | <span data-ttu-id="1fb54-192">Öffnet das Fenster **Ordneroptionen.**</span><span class="sxs-lookup"><span data-stu-id="1fb54-192">Launches the **Folder Options** window.</span></span>                  |
| <span data-ttu-id="1fb54-193">control.exe Netware</span><span class="sxs-lookup"><span data-stu-id="1fb54-193">control.exe netware</span></span>        | <span data-ttu-id="1fb54-194">Startet das **NetWare-Fenster (sofern** installiert).</span><span class="sxs-lookup"><span data-stu-id="1fb54-194">Launches the **Novell NetWare** window (if installed).</span></span>   |
| <span data-ttu-id="1fb54-195">control.exe Telefonie</span><span class="sxs-lookup"><span data-stu-id="1fb54-195">control.exe telephony</span></span>      | <span data-ttu-id="1fb54-196">Öffnet das Fenster **Telefon und Modemoptionen.**</span><span class="sxs-lookup"><span data-stu-id="1fb54-196">Launches the **Phone and Modem Options** window.</span></span>         |
| <span data-ttu-id="1fb54-197">control.exe admintools</span><span class="sxs-lookup"><span data-stu-id="1fb54-197">control.exe admintools</span></span>     | <span data-ttu-id="1fb54-198">Zeigt den Ordner **Verwaltung an.**</span><span class="sxs-lookup"><span data-stu-id="1fb54-198">Displays the **Administrative Tools** folder.</span></span>            |
| <span data-ttu-id="1fb54-199">control.exe schedtasks</span><span class="sxs-lookup"><span data-stu-id="1fb54-199">control.exe schedtasks</span></span>     | <span data-ttu-id="1fb54-200">Zeigt den Ordner **Geplante Aufgaben** an.</span><span class="sxs-lookup"><span data-stu-id="1fb54-200">Displays the **Scheduled Tasks** folder.</span></span>                 |
| <span data-ttu-id="1fb54-201">control.exe netconnections</span><span class="sxs-lookup"><span data-stu-id="1fb54-201">control.exe netconnections</span></span> | <span data-ttu-id="1fb54-202">Zeigt den **Ordner Netzwerkverbindungen** an.</span><span class="sxs-lookup"><span data-stu-id="1fb54-202">Displays the **Network Connections** folder.</span></span>             |
| <span data-ttu-id="1fb54-203">control.exe</span><span class="sxs-lookup"><span data-stu-id="1fb54-203">control.exe infrared</span></span>       | <span data-ttu-id="1fb54-204">Öffnet das **Fenster "Überwachung des Monitors"** (sofern installiert).</span><span class="sxs-lookup"><span data-stu-id="1fb54-204">Launches the **Infrared Monitor** window (if installed).</span></span> |
| <span data-ttu-id="1fb54-205">control.exe von Benutzerpasswörtern</span><span class="sxs-lookup"><span data-stu-id="1fb54-205">control.exe userpasswords</span></span>  | <span data-ttu-id="1fb54-206">Öffnet das **Fenster Benutzerkonten.**</span><span class="sxs-lookup"><span data-stu-id="1fb54-206">Launches the **User Accounts** window.</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="1fb54-207">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1fb54-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fb54-208">Systemsteuerung Elemente</span><span class="sxs-lookup"><span data-stu-id="1fb54-208">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="1fb54-209">Richtlinien zur Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="1fb54-209">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="1fb54-210">Registrieren Systemsteuerung Elementen</span><span class="sxs-lookup"><span data-stu-id="1fb54-210">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="1fb54-211">Verwenden von CPLApplet</span><span class="sxs-lookup"><span data-stu-id="1fb54-211">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="1fb54-212">Systemsteuerung Nachrichtenverarbeitung</span><span class="sxs-lookup"><span data-stu-id="1fb54-212">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="1fb54-213">Erweitern von Systemsteuerung Elementen</span><span class="sxs-lookup"><span data-stu-id="1fb54-213">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="1fb54-214">Zuweisen Systemsteuerung Kategorien</span><span class="sxs-lookup"><span data-stu-id="1fb54-214">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="1fb54-215">Erstellen durchsuchbarer Aufgabenlinks für Systemsteuerung Element</span><span class="sxs-lookup"><span data-stu-id="1fb54-215">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="1fb54-216">Zugreifen auf die Systemsteuerung im Tresor-Modus unter Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1fb54-216">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
