---
description: Um Daten aus WMI auf dem lokalen Computer oder einem Remote Computer zu erhalten, müssen Sie eine Verbindung mit dem WMI-Dienst herstellen, indem Sie eine Verbindung mit einem bestimmten Namespace herstellen.
ms.assetid: 71ff6b06-af7d-43ee-ae6e-1964ec249472
ms.tgt_platform: multiple
title: 'WMI-Tasks: Herstellen einer Verbindung mit dem WMI-Dienst'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 751c6c0802c30e113f4a2b7ddc646cdf5646b7dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358818"
---
# <a name="wmi-tasks-connecting-to-the-wmi-service"></a><span data-ttu-id="cf1f8-103">WMI-Tasks: Herstellen einer Verbindung mit dem WMI-Dienst</span><span class="sxs-lookup"><span data-stu-id="cf1f8-103">WMI Tasks: Connecting to the WMI Service</span></span>

<span data-ttu-id="cf1f8-104">Um Daten aus WMI auf dem lokalen Computer oder einem Remote Computer zu erhalten, müssen Sie eine Verbindung mit dem WMI-Dienst herstellen, indem Sie eine Verbindung mit einem bestimmten [*Namespace*](gloss-n.md)herstellen.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-104">To get data from WMI, either on the local computer or from a remote computer, you must connect to the WMI service by connecting to a specific [*namespace*](gloss-n.md).</span></span> <span data-ttu-id="cf1f8-105">Verwenden Sie in den meisten Fällen entweder die [Kurznamen-monikerverbindung](creating-a-wmi-script.md) oder die [**Locator**](swbemlocator-connectserver.md) -Verbindung.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-105">In most cases, use either the shorthand [moniker](creating-a-wmi-script.md) connection or the [**Locator**](swbemlocator-connectserver.md) connection.</span></span> <span data-ttu-id="cf1f8-106">Weitere Beispiele finden Sie im technet scriptcenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="cf1f8-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="cf1f8-107">Für Remote Verbindungen sind geeignete Einstellungen für die Windows-Firewall und die DCOM erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-107">Remote connections require proper settings for the Windows Firewall and DCOM.</span></span> <span data-ttu-id="cf1f8-108">Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md) und [Herstellen einer Verbindung über die Windows-Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span><span class="sxs-lookup"><span data-stu-id="cf1f8-108">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md) and [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span> <span data-ttu-id="cf1f8-109">Ab Windows Vista kann sich die Benutzerkontensteuerung (User Account Control, UAC) auf den WMI-Zugriff auswirken.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-109">Starting with Windows Vista, User Account Control (UAC) can affect WMI access.</span></span> <span data-ttu-id="cf1f8-110">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="cf1f8-110">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="cf1f8-111">In den in diesem Thema gezeigten Skript Beispielen werden nur Daten vom lokalen Computer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-111">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="cf1f8-112">Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remote Computern finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="cf1f8-112">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="cf1f8-113">Im folgenden Verfahren wird die Vorgehensweise zum Ausführen eines Skripts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-113">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="cf1f8-114">**So führen Sie ein Skript aus**</span><span class="sxs-lookup"><span data-stu-id="cf1f8-114">**To run a script**</span></span>

1.  <span data-ttu-id="cf1f8-115">Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung. vb, z. b. *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-115">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="cf1f8-116">Stellen Sie sicher, dass der Text-Editor der Datei keine Erweiterung ". txt" hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-116">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="cf1f8-117">Öffnen Sie ein Eingabe Aufforderungs Fenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-117">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="cf1f8-118">Geben Sie **cscript-filename.vbs** an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-118">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="cf1f8-119">Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie von einer Eingabeaufforderung mit erhöhten Rechten ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-119">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="cf1f8-120">Einige Ereignisprotokolle, z. b. das Sicherheits Ereignisprotokoll, werden möglicherweise durch die Benutzer Zugriffs Steuerung (User Access Control, UAC) geschützt.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-120">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="cf1f8-121">Cscript zeigt standardmäßig die Ausgabe eines Skripts im Eingabe Aufforderungs Fenster an.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-121">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="cf1f8-122">Da WMI-Skripts große Mengen an Ausgaben verursachen können, empfiehlt es sich, die Ausgabe in eine Datei umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-122">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="cf1f8-123">Geben Sie an der Eingabeaufforderung **cscript filename.vbs > outfile.txt** ein, um die Ausgabe des *filename.vbs* Skripts in *outfile.txt* umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-123">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="cf1f8-124">In der folgenden Tabelle sind Skript Beispiele aufgelistet, die zum Abrufen verschiedener Datentypen auf dem lokalen Computer verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-124">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf1f8-125">Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="cf1f8-125">How do I...</span></span></th>
<th><span data-ttu-id="cf1f8-126">WMI-Klassen oder-Methoden</span><span class="sxs-lookup"><span data-stu-id="cf1f8-126">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf1f8-127">... Herstellen einer Verbindung mit einem Remote Computer mithilfe von WMI</span><span class="sxs-lookup"><span data-stu-id="cf1f8-127">...connect to a remote computer using WMI?</span></span></td>
<td><span data-ttu-id="cf1f8-128">Geben Sie einen der folgenden als Teil der monikerverbindungszeichenfolge an: <a href="constructing-a-moniker-string.md"></a></span><span class="sxs-lookup"><span data-stu-id="cf1f8-128">Specify one of the following as part of your <a href="constructing-a-moniker-string.md">moniker</a> connection string:</span></span><br/>
<ul>
<li><span data-ttu-id="cf1f8-129">Einen NetBIOS-Computernamen, z. b. &quot; ATL-DC-01&quot;</span><span class="sxs-lookup"><span data-stu-id="cf1f8-129">A NetBIOS computer name, such as &quot;atl-dc-01&quot;</span></span></li>
<li><span data-ttu-id="cf1f8-130">Einen voll qualifizierten Domänen Namen, z. b. &quot; ATL-DC-01.fabrikam.com&quot;</span><span class="sxs-lookup"><span data-stu-id="cf1f8-130">A fully qualified domain name, such as &quot;atl-dc-01.fabrikam.com&quot;</span></span></li>
<li><span data-ttu-id="cf1f8-131">Eine IPv4-Adresse, z. b. &quot; 192.168.1.1&quot;</span><span class="sxs-lookup"><span data-stu-id="cf1f8-131">An IPv4 address, such as &quot;192.168.1.1&quot;</span></span></li>
<li><span data-ttu-id="cf1f8-132">Ab Windows Vista können Sie eine IPv6-Adresse angeben, wenn auf dem Zielcomputer und dem Computer, von dem aus Sie die Verbindung herstellen, IPv6 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-132">Starting with Windows Vista, you can specify an IPv6 address if the target computer and the computer from which you are making the connection both run IPv6.</span></span><br/></li>
</ul>
<span data-ttu-id="cf1f8-133">Weitere Informationen finden Sie unter <a href="connecting-to-wmi-on-a-remote-computer.md">Herstellen einer Verbindung mit WMI auf einem Remote Computer</a> und <a href="ipv6-and-ipv4-support-in-wmi.md">IPv6-und IPv4-Unterstützung in WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-133">For more information, see <a href="connecting-to-wmi-on-a-remote-computer.md">Connecting to WMI on a Remote Computer</a> and <a href="ipv6-and-ipv4-support-in-wmi.md">IPv6 and IPv4 Support in WMI</a>.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf1f8-134">VB</span><span class="sxs-lookup"><span data-stu-id="cf1f8-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
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
<th><span data-ttu-id="cf1f8-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="cf1f8-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf1f8-136">... Führen Sie ein WMI-Skript unter Alternative Anmelde Informationen aus?</span><span class="sxs-lookup"><span data-stu-id="cf1f8-136">...run a WMI script under alternate credentials?</span></span></td>
<td><p><span data-ttu-id="cf1f8-137">Verwenden Sie die Methode " <a href="swbemlocator-connectserver.md"><strong>mpbemlocator. ConnectServer</strong></a> " oder " <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWBEMLocator:: ConnectServer</strong></a> " in C++, und schließen Sie den entsprechenden Benutzernamen und das Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-137">Use the <a href="swbemlocator-connectserver.md"><strong>SWbemLocator.ConnectServer</strong></a> method, or <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator::ConnectServer</strong></a> in C++, and include the appropriate user name and password.</span></span> <span data-ttu-id="cf1f8-138">Beim Herstellen einer Verbindung mit dem lokalen Computer können die Anmelde Informationen nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-138">You cannot change credentials when connecting to the local computer.</span></span> <span data-ttu-id="cf1f8-139">Weitere Informationen finden Sie unter <a href="creating-a-wmi-script.md">Erstellen eines WMI-Skripts</a> und <a href="connecting-to-wmi-on-a-remote-computer.md">Herstellen einer Verbindung mit WMI auf einem Remote Computer</a>.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-139">For more information, see <a href="creating-a-wmi-script.md">Creating a WMI Script</a> and <a href="connecting-to-wmi-on-a-remote-computer.md">Connecting to WMI on a Remote Computer</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf1f8-140">VB</span><span class="sxs-lookup"><span data-stu-id="cf1f8-140">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objSWbemLocator = CreateObject(&quot;WbemScripting.SWbemLocator&quot;)
Set objSWbemServices = objSWbemLocator.ConnectServer (strComputer, &quot;root\cimv2&quot;, &quot;fabrikam\administrator&quot;, &quot;password&quot;)
Set colProcessList = objSWbemServices.ExecQuery(&quot;Select * From Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
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
<th><span data-ttu-id="cf1f8-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="cf1f8-141">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$StrComputer = &quot;atl-dc-01&quot;
$strCredentials = &quot;FABRIKAM\administrator&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; -credential $strCredentials `
   -Impersonation Impersonate | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="cf1f8-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cf1f8-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf1f8-143">WMI-Tasks für Skripts und Anwendungen</span><span class="sxs-lookup"><span data-stu-id="cf1f8-143">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="cf1f8-144">WMI C++ Anwendungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="cf1f8-144">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="cf1f8-145">Technet scriptcenter</span><span class="sxs-lookup"><span data-stu-id="cf1f8-145">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
