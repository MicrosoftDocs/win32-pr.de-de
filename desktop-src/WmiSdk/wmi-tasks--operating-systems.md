---
description: WMI-Tasks für Betriebssysteme erhalten Informationen über das Betriebssystem, z. b. die Version, ob Sie aktiviert ist oder welche Hotfixes installiert sind.
ms.assetid: a216ad56-2650-4d93-86e1-449b56019361
ms.tgt_platform: multiple
title: 'WMI-Tasks: Betriebssysteme'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8d4dff83cebf5fd3336aeec2cc45ac4d8498cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350124"
---
# <a name="wmi-tasks-operating-systems"></a><span data-ttu-id="bd07d-103">WMI-Tasks: Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="bd07d-103">WMI Tasks: Operating Systems</span></span>

<span data-ttu-id="bd07d-104">WMI-Tasks für Betriebssysteme erhalten Informationen über das Betriebssystem, z. b. die Version, ob Sie aktiviert ist oder welche Hotfixes installiert sind.</span><span class="sxs-lookup"><span data-stu-id="bd07d-104">WMI tasks for operating systems obtain information about the operating system, such as version, whether it is activated, or which hotfixes are installed.</span></span>

<span data-ttu-id="bd07d-105">In den in diesem Thema gezeigten Skript Beispielen werden nur Daten vom lokalen Computer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="bd07d-105">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="bd07d-106">Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remote Computern finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="bd07d-106">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="bd07d-107">Im folgenden Verfahren wird die Vorgehensweise zum Ausführen eines Skripts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bd07d-107">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="bd07d-108">**So führen Sie ein Skript aus**</span><span class="sxs-lookup"><span data-stu-id="bd07d-108">**To run a script**</span></span>

1.  <span data-ttu-id="bd07d-109">Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung. vb, z. b. *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="bd07d-109">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="bd07d-110">Stellen Sie sicher, dass der Text-Editor der Datei keine Erweiterung ". txt" hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bd07d-110">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="bd07d-111">Öffnen Sie ein Eingabe Aufforderungs Fenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="bd07d-111">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="bd07d-112">Geben Sie **cscript-filename.vbs** an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="bd07d-112">Type **CScript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="bd07d-113">Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie von einer Eingabeaufforderung mit erhöhten Rechten ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd07d-113">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="bd07d-114">Einige Ereignisprotokolle, z. b. das Sicherheits Ereignisprotokoll, werden möglicherweise durch die Benutzer Zugriffs Steuerung (User Access Control, UAC) geschützt.</span><span class="sxs-lookup"><span data-stu-id="bd07d-114">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="bd07d-115">Cscript zeigt standardmäßig die Ausgabe eines Skripts im Eingabe Aufforderungs Fenster an.</span><span class="sxs-lookup"><span data-stu-id="bd07d-115">By default, CScript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="bd07d-116">Da WMI-Skripts große Mengen an Ausgaben verursachen können, empfiehlt es sich, die Ausgabe in eine Datei umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="bd07d-116">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="bd07d-117">Geben Sie an der Eingabeaufforderung **cscript filename.vbs > outfile.txt** ein, um die Ausgabe des *filename.vbs* Skripts in *outfile.txt* umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="bd07d-117">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="bd07d-118">In der folgenden Tabelle sind Skript Beispiele aufgelistet, die zum Abrufen verschiedener Datentypen auf dem lokalen Computer verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="bd07d-118">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd07d-119">Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="bd07d-119">How do I...</span></span></th>
<th><span data-ttu-id="bd07d-120">WMI-Klassen oder-Methoden</span><span class="sxs-lookup"><span data-stu-id="bd07d-120">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bd07d-121">... bestimmen, ob eine Service Pack auf einem Computer installiert wurde?</span><span class="sxs-lookup"><span data-stu-id="bd07d-121">...determine if a service pack has been installed on a computer?</span></span></td>
<td><span data-ttu-id="bd07d-122">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> -Klasse, und überprüfen Sie den Wert der Eigenschaften <strong>ServicePackMajorVersion</strong> und <strong>ServicePackMinorVersion</strong> .</span><span class="sxs-lookup"><span data-stu-id="bd07d-122">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and check the value of the <strong>ServicePackMajorVersion</strong> and <strong>ServicePackMinorVersion</strong> properties.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd07d-123">VB</span><span class="sxs-lookup"><span data-stu-id="bd07d-123">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo objOperatingSystem.ServicePackMajorVersion & &quot;.&quot; & objOperatingSystem.ServicePackMinorVersion
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd07d-124">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd07d-124">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | `
   format-list ServicePackMajorVersion, ServicePackMinorVersion</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd07d-125">... bestimmen, wann das Betriebssystem auf einem Computer installiert wurde?</span><span class="sxs-lookup"><span data-stu-id="bd07d-125">...determine when the operating system was installed on a computer?</span></span></td>
<td><p><span data-ttu-id="bd07d-126">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> -Klasse und die <strong>InstallDate</strong> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bd07d-126">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and the <strong>InstallDate</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd07d-127">VB</span><span class="sxs-lookup"><span data-stu-id="bd07d-127">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo &quot;Install Date: &quot; & objOperatingSystem.InstallDate 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd07d-128">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd07d-128">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | format-list InstallDate</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd07d-129">... bestimmen Sie, welche Version des Windows-Betriebssystems auf einem Computer installiert ist?</span><span class="sxs-lookup"><span data-stu-id="bd07d-129">...determine which version of the Windows operating system is installed on a computer?</span></span></td>
<td><p><span data-ttu-id="bd07d-130">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> -Klasse, und rufen Sie die Eigenschaften <strong>Name</strong> und <strong>Version</strong> ab.</span><span class="sxs-lookup"><span data-stu-id="bd07d-130">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class, and retrieve both the <strong>Name</strong> and <strong>Version</strong> properties.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd07d-131">VB</span><span class="sxs-lookup"><span data-stu-id="bd07d-131">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo objOperatingSystem.Caption & &quot;  &quot; & objOperatingSystem.Version
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd07d-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd07d-132">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | format-list Caption, Version</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd07d-133">... bestimmen Sie, welcher Ordner der Windows-Ordner ist (% windir%). auf einem Computer?</span><span class="sxs-lookup"><span data-stu-id="bd07d-133">...determine which folder is the Windows folder (%Windir%) on a computer?</span></span></td>
<td><p><span data-ttu-id="bd07d-134">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> -Klasse, und überprüfen Sie den Wert der <strong>WindowsDirectory</strong> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bd07d-134">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class, and check the value of the <strong>WindowsDirectory</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd07d-135">VB</span><span class="sxs-lookup"><span data-stu-id="bd07d-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo &quot;Windows Folder: &quot; & objOperatingSystem.WindowsDirectory
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd07d-136">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd07d-136">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | format-list WindowsDirectory</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd07d-137">... Legen Sie fest, welche Hotfixes auf einem Computer installiert wurden?</span><span class="sxs-lookup"><span data-stu-id="bd07d-137">...determine what hotfixes have been installed on a computer?</span></span></td>
<td><p><span data-ttu-id="bd07d-138">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-quickfixengineering"><strong>Win32_QuickFixEngineering</strong></a> -Klasse.</span><span class="sxs-lookup"><span data-stu-id="bd07d-138">Use the <a href="/windows/desktop/CIMWin32Prov/win32-quickfixengineering"><strong>Win32_QuickFixEngineering</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd07d-139">VB</span><span class="sxs-lookup"><span data-stu-id="bd07d-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colQuickFixes = objWMIService.ExecQuery (&quot;Select * from Win32_QuickFixEngineering&quot;)
For Each objQuickFix in colQuickFixes
    Wscript.Echo &quot;Description: &quot; & objQuickFix.Description
    Wscript.Echo &quot;Hotfix ID: &quot; & objQuickFix.HotFixID
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd07d-140">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd07d-140">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_QuickFixEngineering -Namespace &quot;root\cimv2&quot; | format-list Description, HotFixIDs</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd07d-141">... Stellen Sie fest, ob das Betriebssystem auf einem Computer aktiviert werden muss?</span><span class="sxs-lookup"><span data-stu-id="bd07d-141">...determine if I need to activate the operating system on a computer?</span></span></td>
<td><p><span data-ttu-id="bd07d-142">Verwenden Sie die <a href="/previous-versions/windows/desktop/legacy/aa394520(v=vs.85)"><strong>Win32_WindowsProductActivation</strong></a> -Klasse, und überprüfen Sie den Wert der <strong>ActivationRequired</strong> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bd07d-142">Use the <a href="/previous-versions/windows/desktop/legacy/aa394520(v=vs.85)"><strong>Win32_WindowsProductActivation</strong></a> class and check the value of the <strong>ActivationRequired</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd07d-143">VB</span><span class="sxs-lookup"><span data-stu-id="bd07d-143">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colWPA = objWMIService.ExecQuery (&quot;Select * from Win32_WindowsProductActivation&quot;)
For Each objWPA in colWPA
    Wscript.Echo &quot;Activation Required: &quot; & objWPA.ActivationRequired
    Wscript.Echo &quot;Remaining Evaluation Period: &quot; & objWPA.RemainingEvaluationPeriod
    Wscript.Echo &quot;Remaining Grace Period: &quot; & objWPA.RemainingGracePeriod
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd07d-144">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd07d-144">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_WindowsProductActivation -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | `
     format-list ActivationRequired, RemainingEvaluationPeriod, RemainingGracePeriod</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="bd07d-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bd07d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd07d-146">WMI-Tasks für Skripts und Anwendungen</span><span class="sxs-lookup"><span data-stu-id="bd07d-146">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="bd07d-147">WMI C++ Anwendungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="bd07d-147">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="bd07d-148">Technet scriptcenter</span><span class="sxs-lookup"><span data-stu-id="bd07d-148">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

