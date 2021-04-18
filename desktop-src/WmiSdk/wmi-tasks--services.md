---
description: WMI-Tasks für Dienste erhalten Informationen zu Diensten, einschließlich abhängiger oder Vorgänger Dienste. Weitere Beispiele finden Sie im technet scriptcenter unter https://www.microsoft.com/technet .
ms.assetid: 1cd92981-c074-4ff7-a32c-ce492e6d6aa5
ms.tgt_platform: multiple
title: 'WMI-Tasks: Dienste'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b786ce0e358a59922728be4e90bc8cdeaa37a298
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351449"
---
# <a name="wmi-tasks-services"></a><span data-ttu-id="c48de-104">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="c48de-104">WMI Tasks: Services</span></span>

<span data-ttu-id="c48de-105">WMI-Tasks für Dienste erhalten Informationen zu Diensten, einschließlich abhängiger oder Vorgänger Dienste.</span><span class="sxs-lookup"><span data-stu-id="c48de-105">WMI tasks for services obtain information about services, including dependent or antecedent services.</span></span> <span data-ttu-id="c48de-106">Weitere Beispiele finden Sie im technet scriptcenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c48de-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="c48de-107">In den in diesem Thema gezeigten Skript Beispielen werden nur Daten vom lokalen Computer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c48de-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="c48de-108">Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remote Computern finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="c48de-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="c48de-109">Im folgenden Verfahren wird die Vorgehensweise zum Ausführen eines Skripts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c48de-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="c48de-110">**So führen Sie ein Skript aus**</span><span class="sxs-lookup"><span data-stu-id="c48de-110">**To run a script**</span></span>

1.  <span data-ttu-id="c48de-111">Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung. vb, z. b. *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="c48de-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="c48de-112">Stellen Sie sicher, dass der Text-Editor der Datei keine Erweiterung ". txt" hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="c48de-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="c48de-113">Öffnen Sie ein Eingabe Aufforderungs Fenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="c48de-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="c48de-114">Geben Sie **cscript-filename.vbs** an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="c48de-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="c48de-115">Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie von einer Eingabeaufforderung mit erhöhten Rechten ausführen.</span><span class="sxs-lookup"><span data-stu-id="c48de-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="c48de-116">Einige Ereignisprotokolle, z. b. das Sicherheits Ereignisprotokoll, werden möglicherweise durch die Benutzer Zugriffs Steuerung (User Access Control, UAC) geschützt.</span><span class="sxs-lookup"><span data-stu-id="c48de-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="c48de-117">Cscript zeigt standardmäßig die Ausgabe eines Skripts im Eingabe Aufforderungs Fenster an.</span><span class="sxs-lookup"><span data-stu-id="c48de-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="c48de-118">Da WMI-Skripts große Mengen an Ausgaben verursachen können, empfiehlt es sich, die Ausgabe in eine Datei umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="c48de-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="c48de-119">Geben Sie an der Eingabeaufforderung **cscript filename.vbs > outfile.txt** ein, um die Ausgabe des *filename.vbs* Skripts in *outfile.txt* umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="c48de-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="c48de-120">In der folgenden Tabelle sind Skript Beispiele aufgelistet, die zum Abrufen verschiedener Datentypen auf dem lokalen Computer verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c48de-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>




<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c48de-121">Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="c48de-121">How do I...</span></span></th>
<th><span data-ttu-id="c48de-122">WMI-Klassen oder-Methoden</span><span class="sxs-lookup"><span data-stu-id="c48de-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c48de-123">... bestimmen, welche Dienste ausgeführt werden und welche nicht?</span><span class="sxs-lookup"><span data-stu-id="c48de-123">...determine which services are running and which ones are not?</span></span></td>
<td><span data-ttu-id="c48de-124">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> -Klasse, um den Status aller Dienste zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c48de-124">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class to check the state of all of the services.</span></span> <span data-ttu-id="c48de-125">Mithilfe der State-Eigenschaft können Sie festzustellen, ob ein Dienst beendet oder ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c48de-125">The state property lets you know if a service is stopped or running.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c48de-126">VB</span><span class="sxs-lookup"><span data-stu-id="c48de-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\CIMV2&quot;) 
Set colItems = objWMIService.ExecQuery(&quot;SELECT * FROM Win32_Service&quot;,,48) 
For Each objItem in colItems 
    Wscript.Echo &quot;Service Name: &quot; & objItem.Name & VBNewLine & &quot;State: &quot; & objItem.State
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
<th><span data-ttu-id="c48de-127">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c48de-127">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | format-list Name, State</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c48de-128">... verhindern, dass Hauptbenutzer bestimmte Dienste starten?</span><span class="sxs-lookup"><span data-stu-id="c48de-128">...stop Power Users from starting certain services?</span></span></td>
<td><p><span data-ttu-id="c48de-129">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> -Klasse und die <a href="/windows/desktop/CIMWin32Prov/changestartmode-method-in-class-win32-service"><strong>ChangeStartMode</strong></a> -Methode, um die <strong>StartMode</strong> -Eigenschaft auf "deaktiviert" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c48de-129">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/changestartmode-method-in-class-win32-service"><strong>ChangeStartMode</strong></a> method to set the <strong>StartMode</strong> property to Disabled.</span></span> <span data-ttu-id="c48de-130">Deaktivierte Dienste können nicht gestartet werden, und Poweruser können den Start Modus eines Diensts standardmäßig nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="c48de-130">Disabled services cannot be started, and, by default, Power Users cannot change the start mode of a service.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c48de-131">VB</span><span class="sxs-lookup"><span data-stu-id="c48de-131">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = objWMIService.ExecQuery (&quot;Select * from Win32_Service where StartMode = &#39;Manual&#39;&quot;)
For Each objService in colServiceList
    errReturnCode = objService.Change( , , , , &quot;Disabled&quot;)
    WScript.Echo &quot;Changed manual service to disabled: &quot; & objService.Name   
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
<th><span data-ttu-id="c48de-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c48de-132">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | where {$_.startMode -eq &quot;Manual&quot;} | `
    foreach-object { [void]$_.changeStartMode(&#39;Disabled&#39;) }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c48de-133">... Dienste starten und Abbrechen?</span><span class="sxs-lookup"><span data-stu-id="c48de-133">...start and stop services?</span></span></td>
<td><p><span data-ttu-id="c48de-134">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> -Klasse und die <a href="/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service"><strong>Stop Service</strong></a> -Methode und die <a href="/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service"><strong>StartService</strong></a> -Methode.</span><span class="sxs-lookup"><span data-stu-id="c48de-134">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service"><strong>StopService</strong></a> and <a href="/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service"><strong>StartService</strong></a> methods.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c48de-135">VB</span><span class="sxs-lookup"><span data-stu-id="c48de-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colListOfServices = objWMIService.ExecQuery (&quot;Select * from Win32_Service Where Name =&#39;Alerter&#39;&quot;)
For Each objService in colListOfServices
    objService.StartService()
    Wscript.Echo &quot;Started Alerter service&quot;
Next
</code></pre></td>
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
<th><span data-ttu-id="c48de-136">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c48de-136">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | where {$_.Name -eq &quot;Alerter&quot;} | `
    foreach-object { [void]$_.StartService() }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c48de-137">... Dienst Konto Kennwörter mithilfe eines Skripts ändern?</span><span class="sxs-lookup"><span data-stu-id="c48de-137">...change service account passwords using a script?</span></span></td>
<td><p><span data-ttu-id="c48de-138">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> -Klasse und die- <a href="/windows/desktop/CIMWin32Prov/change-method-in-class-win32-service"><strong>Änderungs</strong></a> Methode.</span><span class="sxs-lookup"><span data-stu-id="c48de-138">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/change-method-in-class-win32-service"><strong>Change</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c48de-139">VB</span><span class="sxs-lookup"><span data-stu-id="c48de-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = objWMIService.ExecQuery (&quot;Select * from Win32_Service&quot;)
For Each objservice in colServiceList
    If objService.StartName = &quot;.\netsvc&quot; Then
        errReturn = objService.Change( , , , , , , , &quot;password&quot;)  
    End If 
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c48de-140">.. Legen Sie fest, welche Dienste ich unterbinden kann?</span><span class="sxs-lookup"><span data-stu-id="c48de-140">..determine which services I can stop?</span></span></td>
<td><p><span data-ttu-id="c48de-141">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> -Klasse, und überprüfen Sie den Wert der Eigenschaft " <strong>Accept-Stopps</strong> ".</span><span class="sxs-lookup"><span data-stu-id="c48de-141">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class, and check the value of the <strong>AcceptStop</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c48de-142">VB</span><span class="sxs-lookup"><span data-stu-id="c48de-142">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServices = objWMIService.ExecQuery (&quot;Select * from Win32_Service Where AcceptStop = True&quot;)
For Each objService in colServices
    Wscript.Echo objService.DisplayName 
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
<th><span data-ttu-id="c48de-143">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c48de-143">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | where {$_.AcceptStop -eq &quot;True&quot;} | `
     format-list DisplayName</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c48de-144">... Suchen Sie die Dienste, die ausgeführt werden müssen, bevor der DHCP-Dienst gestartet werden kann?</span><span class="sxs-lookup"><span data-stu-id="c48de-144">...find the services that must be running before I can start the DHCP service?</span></span></td>
<td><p><span data-ttu-id="c48de-145">Abfragen <a href="associators-of-statement.md">von assoziatoren der</a> <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> Klasse mit dem Namen "DHCP" &quot; , die &quot; sich in der <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> -Klasse befinden und &quot; von &quot; der <strong>Role</strong> -Eigenschaft abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="c48de-145">Query for <a href="associators-of-statement.md">ASSOCIATORS OF</a> the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class named &quot;DHCP&quot; that are in the <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> class and have &quot;Dependent&quot; in the <strong>Role</strong> property.</span></span> <span data-ttu-id="c48de-146"><strong>Role</strong> bezeichnet die Rolle des DHCP-Diensts: in diesem Fall hängt sie von den anderen Diensten ab, die gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="c48de-146"><strong>Role</strong> means the role of the DHCP service: in this case, it is dependent on the other services that are being started.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c48de-147">VB</span><span class="sxs-lookup"><span data-stu-id="c48de-147">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = objWMIService.ExecQuery(&quot;Associators Of &quot; _ 
    & &quot;{Win32_Service.Name=&#39;dhcp&#39;} Where &quot; _
    & &quot;AssocClass=Win32_DependentService &quot; _
    & &quot;Role=Dependent&quot;) 
For Each objService in colServiceList
Wscript.Echo objService.DisplayName 
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
<th><span data-ttu-id="c48de-148">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c48de-148">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$query = &quot;Associators Of {Win32_Service.Name=&#39;dhcp&#39;} Where AssocClass=Win32_DependentService Role=Dependent&quot;
Get-WmiObject -Query $query -Namespace &quot;root\cimv2&quot; | format-list DisplayName</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c48de-149">... Suchen Sie die Dienste, für die der WMI-Dienst (Winmgmt) ausgeführt werden muss, bevor der Dienst gestartet werden kann?</span><span class="sxs-lookup"><span data-stu-id="c48de-149">...find the services that require the WMI service (Winmgmt) service to be running before they can start?</span></span></td>
<td><p><span data-ttu-id="c48de-150">Abfragen <a href="associators-of-statement.md">von assoziatoren der</a> <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> Klasse mit dem Namen "DHCP" &quot; , die &quot; sich in der <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> -Klasse befinden und über &quot; Vorgänger &quot; in der <strong>Role</strong> -Eigenschaft verfügen.</span><span class="sxs-lookup"><span data-stu-id="c48de-150">Query for <a href="associators-of-statement.md">ASSOCIATORS OF</a> the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class named &quot;DHCP&quot; that are in the <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> class and have &quot;Antecendent&quot; in the <strong>Role</strong> property.</span></span> <span data-ttu-id="c48de-151"><strong>Role</strong> bezeichnet die Rolle des rasman-Diensts: in diesem Fall muss vor den abhängigen Diensten gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="c48de-151"><strong>Role</strong> means the role of the rasman service: in this case, it is antecedent to must be started before the dependent services.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c48de-152">VB</span><span class="sxs-lookup"><span data-stu-id="c48de-152">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\ & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = _
    objWMIService.ExecQuery(&quot;Associators of &quot; _
    & &quot;{Win32_Service.Name=&#39;winmgmt&#39;} Where &quot; _
    & &quot;AssocClass=Win32_DependentService &quot; _
    & &quot;Role=Antecedent&quot; )
For Each objService in colServiceList
Wscript.Echo &quot;Name: &quot; & objService.Name & VBTab & &quot;Display Name: &quot; & objService.DisplayName 
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
<th><span data-ttu-id="c48de-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c48de-153">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$query = &quot;Associators of {Win32_Service.Name=&#39;winmgmt&#39;} Where AssocClass=Win32_DependentService Role=Antecedent&quot;
Get-WmiObject -Query $query -Namespace &quot;root\cimv2&quot; | format-list Name, DisplayName</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c48de-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c48de-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c48de-155">WMI-Tasks für Skripts und Anwendungen</span><span class="sxs-lookup"><span data-stu-id="c48de-155">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="c48de-156">WMI C++ Anwendungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="c48de-156">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="c48de-157">Technet scriptcenter</span><span class="sxs-lookup"><span data-stu-id="c48de-157">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
