---
description: WMI-Tasks für Netzwerke verwalten und Abrufen von Informationen zu Verbindungen und IP-oder Mac-Adressen. Weitere Beispiele finden Sie im technet scriptcenter unter https://www.microsoft.com/technet .
ms.assetid: 25da32c3-34bf-4c88-9b09-ff371f2cf8db
ms.tgt_platform: multiple
title: 'WMI-Tasks: Netzwerk'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31e8346a064fe2f6c7ab624897be8e789474f7b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356646"
---
# <a name="wmi-tasks-networking"></a><span data-ttu-id="f61ee-104">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="f61ee-104">WMI Tasks: Networking</span></span>

<span data-ttu-id="f61ee-105">WMI-Tasks für Netzwerke verwalten und Abrufen von Informationen zu Verbindungen und IP-oder Mac-Adressen.</span><span class="sxs-lookup"><span data-stu-id="f61ee-105">WMI tasks for networking manage and obtain information about connections and IP or MAC addresses.</span></span> <span data-ttu-id="f61ee-106">Weitere Beispiele finden Sie im technet scriptcenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f61ee-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="f61ee-107">In den in diesem Thema gezeigten Skript Beispielen werden nur Daten vom lokalen Computer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f61ee-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="f61ee-108">Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remote Computern finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="f61ee-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="f61ee-109">Im folgenden Verfahren wird die Vorgehensweise zum Ausführen eines Skripts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f61ee-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="f61ee-110">**So führen Sie ein Skript aus**</span><span class="sxs-lookup"><span data-stu-id="f61ee-110">**To run a script**</span></span>

1.  <span data-ttu-id="f61ee-111">Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung. vb, z. b. *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="f61ee-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="f61ee-112">Stellen Sie sicher, dass der Text-Editor der Datei keine Erweiterung ". txt" hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="f61ee-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="f61ee-113">Öffnen Sie ein Eingabe Aufforderungs Fenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="f61ee-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="f61ee-114">Geben Sie **cscript-filename.vbs** an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="f61ee-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="f61ee-115">Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie von einer Eingabeaufforderung mit erhöhten Rechten ausführen.</span><span class="sxs-lookup"><span data-stu-id="f61ee-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="f61ee-116">Einige Ereignisprotokolle, z. b. das Sicherheits Ereignisprotokoll, werden möglicherweise durch die Benutzer Zugriffs Steuerung (User Access Control, UAC) geschützt.</span><span class="sxs-lookup"><span data-stu-id="f61ee-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="f61ee-117">Cscript zeigt standardmäßig die Ausgabe eines Skripts im Eingabe Aufforderungs Fenster an.</span><span class="sxs-lookup"><span data-stu-id="f61ee-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="f61ee-118">Da WMI-Skripts große Mengen an Ausgaben verursachen können, empfiehlt es sich, die Ausgabe in eine Datei umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="f61ee-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="f61ee-119">Geben Sie an der Eingabeaufforderung **cscript filename.vbs > outfile.txt** ein, um die Ausgabe des *filename.vbs* Skripts in *outfile.txt* umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="f61ee-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="f61ee-120">In der folgenden Tabelle sind Skript Beispiele aufgelistet, die zum Abrufen verschiedener Datentypen auf dem lokalen Computer verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f61ee-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f61ee-121">Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="f61ee-121">How do I...</span></span></th>
<th><span data-ttu-id="f61ee-122">WMI-Klassen oder-Methoden</span><span class="sxs-lookup"><span data-stu-id="f61ee-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f61ee-123">... eine Netzwerkverbindung mithilfe von WMI deaktivieren?</span><span class="sxs-lookup"><span data-stu-id="f61ee-123">...disable a network connection using WMI?</span></span></td>
<td><span data-ttu-id="f61ee-124">Wenn Sie DHCP verwenden, verwenden Sie den <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> und die <a href="/windows/desktop/CIMWin32Prov/releasedhcplease-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLease</strong></a> -Methode, um die IP-Adresse freizugeben.</span><span class="sxs-lookup"><span data-stu-id="f61ee-124">If you are using DHCP, use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> and the <a href="/windows/desktop/CIMWin32Prov/releasedhcplease-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLease</strong></a> method to release the IP address.</span></span> <span data-ttu-id="f61ee-125">Wenn Sie DHCP nicht verwenden, können Sie WMI nicht zum Deaktivieren einer Netzwerkverbindung verwenden.</span><span class="sxs-lookup"><span data-stu-id="f61ee-125">If you are not using DHCP, you cannot use WMI to disable a network connection.</span></span> <span data-ttu-id="f61ee-126">Verwenden Sie zum erneuten Aktivieren der Netzwerkverbindung <a href="/windows/desktop/CIMWin32Prov/renewdhcplease-method-in-class-win32-networkadapterconfiguration"><strong>objnetcard. erneudhcplease</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f61ee-126">To re-enable the network connection, use <a href="/windows/desktop/CIMWin32Prov/renewdhcplease-method-in-class-win32-networkadapterconfiguration"><strong>objNetCard.RenewDHCPLease</strong></a>.</span></span> <span data-ttu-id="f61ee-127">Mithilfe der <a href="/windows/desktop/CIMWin32Prov/releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLeaseAll</strong></a> -Methode und der <a href="/windows/desktop/CIMWin32Prov/renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>erneuerdhcpleaseall</strong></a> -Methode können Sie auch alle DHCP-Leases freigeben oder erneuern.</span><span class="sxs-lookup"><span data-stu-id="f61ee-127">You can also release or renew all of the DHCP leases using the <a href="/windows/desktop/CIMWin32Prov/releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLeaseAll</strong></a> and <a href="/windows/desktop/CIMWin32Prov/renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>RenewDHCPLeaseAll</strong></a> methods.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f61ee-128">VB</span><span class="sxs-lookup"><span data-stu-id="f61ee-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNetCards = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapterConfiguration &quot; _
        & &quot;Where IPEnabled = True&quot;)
For Each objNetCard in colNetCards
    objNetCard.ReleaseDHCPLease()
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
<th><span data-ttu-id="f61ee-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f61ee-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;
$net = Get-WMIObject -class Win32_NetworkAdapterConfiguration -ComputerName $computer
$netenabled = $net | where {$_.IPenabled}
foreach ($NetCard in $netenabled) {
    &quot;Releasing lease on: {0}&quot; -f $netcard.caption
 $netcard.ReleaseDHCPLease()
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="f61ee-130">... Deaktivieren oder Aktivieren einer NIC</span><span class="sxs-lookup"><span data-stu-id="f61ee-130">...disable or enable a NIC?</span></span></td>
<td><p><span data-ttu-id="f61ee-131">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> -Klasse und die Methoden zum <a href="/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter"><strong>Deaktivieren</strong></a> oder <a href="/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter"><strong>aktivieren</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f61ee-131">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter"><strong>Disable</strong></a> or <a href="/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter"><strong>Enable</strong></a> methods.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f61ee-132">... bestimmen Sie, welche IP-Adresse einer bestimmten Netzwerkverbindung zugewiesen wurde?</span><span class="sxs-lookup"><span data-stu-id="f61ee-132">...determine which IP address has been assigned to a given network connection?</span></span></td>
<td><p><span data-ttu-id="f61ee-133">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> -Klasse und die <strong>NetConnectionID</strong> -Eigenschaft, um die Mac-Adresse der Netzwerkverbindung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="f61ee-133">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> class and the <strong>NetConnectionID</strong> property to determine the MAC address of the network connection.</span></span> <span data-ttu-id="f61ee-134">Verwenden Sie dann die <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> -Klasse, um die IP-Adresse zu ermitteln, die der Mac-Adresse zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f61ee-134">Then, use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class to find the IP address associated with the MAC address.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f61ee-135">VB</span><span class="sxs-lookup"><span data-stu-id="f61ee-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapter &quot; _
        & &quot;Where NetConnectionID = &quot; & _
        &quot;&#39;Local Area Connection 2&#39;&quot;)

For Each objItem in colItems
    strMACAddress = objItem.MACAddress
Next

Set colItems = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapterConfiguration&quot;)

For Each objItem in colItems
    If objItem.MACAddress = strMACAddress Then
        For Each strIPAddress in objItem.IPAddress
            Wscript.Echo &quot;IP Address: &quot; &  strIPAddress
        Next
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f61ee-136">VB</span><span class="sxs-lookup"><span data-stu-id="f61ee-136">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNics = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapter &quot; _
        & &quot;Where NetConnectionID = &quot; & _
        &quot;&#39;Local Area Connection&#39;&quot;)
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      (&quot;ASSOCIATORS OF &quot; _
          & &quot;{Win32_NetworkAdapter.DeviceID=&#39;&quot; & _
      objNic.DeviceID & &quot;&#39;}&quot; & _
      &quot; WHERE AssocClass=Win32_NetworkAdapterSetting&quot;)
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo &quot;IP Address: &quot; &  strIPAddress
        Next
    Next
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f61ee-137">... Bestimmen der Mac-Adresse eines Netzwerkadapters</span><span class="sxs-lookup"><span data-stu-id="f61ee-137">...determine the MAC address of a network adapter?</span></span></td>
<td><p><span data-ttu-id="f61ee-138">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> -Klasse, und überprüfen Sie den Wert der <strong>macaddress</strong> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f61ee-138">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class and check the value of the <strong>MACAddress</strong> property.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f61ee-139">... bestimmen Sie die IP-Adresse eines Computers?</span><span class="sxs-lookup"><span data-stu-id="f61ee-139">...determine the IP address of a computer?</span></span></td>
<td><p><span data-ttu-id="f61ee-140">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> -Klasse, und überprüfen Sie den Wert der <strong>IPAddress</strong> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f61ee-140">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class and check the value of the <strong>IPAddress</strong> property.</span></span> <span data-ttu-id="f61ee-141">Dies wird als Array zurückgegeben. verwenden Sie daher eine For-Each Schleife, um den Wert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f61ee-141">This is returned as an array, so use a For-Each loop to get the value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f61ee-142">VB</span><span class="sxs-lookup"><span data-stu-id="f61ee-142">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _ 
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set IPConfigSet = objWMIService.ExecQuery _
    (&quot;Select IPAddress from Win32_NetworkAdapterConfiguration &quot;)
 
For Each IPConfig in IPConfigSet
    If Not IsNull(IPConfig.IPAddress) Then 
        For i=LBound(IPConfig.IPAddress) _
            to UBound(IPConfig.IPAddress)
                WScript.Echo IPConfig.IPAddress(i)
        Next
    End If
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
<th><span data-ttu-id="f61ee-143">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f61ee-143">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;
$IPconfigset = Get-WmiObject Win32_NetworkAdapterConfiguration
  
# Iterate and get IP address
$count = 0
foreach ($IPConfig in $IPConfigSet) {
   if ($Ipconfig.IPaddress) {
      foreach ($addr in $Ipconfig.Ipaddress) {
   &quot;IP Address   : {0}&quot; -f  $addr;
   $count++ 
   }
   }
}
if ($count -eq 0) {&quot;No IP addresses found&quot;}
else {&quot;$Count IP addresses found on this system&quot;}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f61ee-144">...configSie einen Computer, damit er seine IP-Adresse über DHCP erhält?</span><span class="sxs-lookup"><span data-stu-id="f61ee-144">...configure a computer to start getting its IP address through DHCP?</span></span></td>
<td><p><span data-ttu-id="f61ee-145">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> -Klasse und die <a href="/windows/desktop/CIMWin32Prov/enabledhcp-method-in-class-win32-networkadapterconfiguration"><strong>EnableDHCP</strong></a> -Methode.</span><span class="sxs-lookup"><span data-stu-id="f61ee-145">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/enabledhcp-method-in-class-win32-networkadapterconfiguration"><strong>EnableDHCP</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f61ee-146">VB</span><span class="sxs-lookup"><span data-stu-id="f61ee-146">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNetAdapters = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NetworkAdapterConfiguration &quot; _
        & &quot;where IPEnabled=TRUE&quot;)
 
For Each objNetAdapter In colNetAdapters
    errEnable = objNetAdapter.EnableDHCP()
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f61ee-147">... einem Computer eine statische IP-Adresse zuweisen?</span><span class="sxs-lookup"><span data-stu-id="f61ee-147">...assign a computer a static IP address?</span></span></td>
<td><p><span data-ttu-id="f61ee-148">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> -Klasse und die <a href="/windows/desktop/CIMWin32Prov/enablestatic-method-in-class-win32-networkadapterconfiguration"><strong>EnableStatic</strong></a> -Methode.</span><span class="sxs-lookup"><span data-stu-id="f61ee-148">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/enablestatic-method-in-class-win32-networkadapterconfiguration"><strong>EnableStatic</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f61ee-149">VB</span><span class="sxs-lookup"><span data-stu-id="f61ee-149">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNetAdapters = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NetworkAdapterConfiguration &quot; _
        & &quot;where IPEnabled=TRUE&quot;)
strIPAddress = Array(&quot;192.168.1.141&quot;)
strSubnetMask = Array(&quot;255.255.255.0&quot;)
strGateway = Array(&quot;192.168.1.100&quot;)
strGatewayMetric = Array(1)
 
For Each objNetAdapter in colNetAdapters
    errEnable = objNetAdapter.EnableStatic( _
        strIPAddress, strSubnetMask)
    errGateways = objNetAdapter.SetGateways(_
        strGateway, strGatewaymetric)
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f61ee-150">... Abrufen von Informationen zu Netzwerkadaptern, ohne auch Informationen zu Dingen wie RAS-und VPN-Verbindungen abzurufen?</span><span class="sxs-lookup"><span data-stu-id="f61ee-150">...get information about network adapters without also retrieving information about things like RAS and VPN connections?</span></span></td>
<td><p><span data-ttu-id="f61ee-151">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f61ee-151">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class.</span></span> <span data-ttu-id="f61ee-152">Verwenden Sie in Ihrer <a href="querying-with-wql.md">WQL</a> -Abfrage diese Klausel: Where <strong>ipabled</strong>  =  <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="f61ee-152">In your <a href="querying-with-wql.md">WQL</a> query, use this clause: Where <strong>IPEnabled</strong> = <strong>True</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f61ee-153">VB</span><span class="sxs-lookup"><span data-stu-id="f61ee-153">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set IPConfigSet = objWMIService.ExecQuery _
    (&quot;Select IPAddress from Win32_NetworkAdapterConfiguration&quot; _
        & &quot; where IPEnabled=TRUE&quot;)
 
For Each IPConfig in IPConfigSet
    If Not IsNull(IPConfig.IPAddress) Then 
        For i=LBound(IPConfig.IPAddress) _
        to UBound(IPConfig.IPAddress)
            WScript.Echo IPConfig.IPAddress(i)
        Next
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f61ee-154">... Pingen eines Computers, ohne Ping.exe zu verwenden?</span><span class="sxs-lookup"><span data-stu-id="f61ee-154">...ping a computer without using Ping.exe?</span></span></td>
<td><p><span data-ttu-id="f61ee-155">Verwenden Sie die <a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f61ee-155">Use the <a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> class.</span></span></p>
<p><span data-ttu-id="f61ee-156"><a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> können Daten für Computer zurückgeben, die sowohl IPv4-als auch IPv6-Adressen haben.</span><span class="sxs-lookup"><span data-stu-id="f61ee-156"><a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> can return data for computers that have both IPv4 addresses and IPv6 addresses.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f61ee-157">VB</span><span class="sxs-lookup"><span data-stu-id="f61ee-157">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_ 
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colPings = objWMIService.ExecQuery _
    (&quot;Select * From Win32_PingStatus where Address = &#39;192.168.1.1&#39;&quot;)

For Each objStatus in colPings
    If IsNull(objStatus.StatusCode) _
        or objStatus.StatusCode<>0 Then 
        WScript.Echo &quot;Computer did not respond.&quot; 
    Else
        Wscript.Echo &quot;Computer responded.&quot;
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f61ee-158">VB</span><span class="sxs-lookup"><span data-stu-id="f61ee-158">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;client1&quot;
Set objShell = CreateObject(&quot;WScript.Shell&quot;)
Set objScriptExec = objShell.Exec( _
    &quot;ping -n 2 -w 1000 &quot; & strComputer)
strPingResults = LCase(objScriptExec.StdOut.ReadAll)
If InStr(strPingResults, &quot;reply from&quot;) Then
    If InStr(strPingResults, &quot;destination net unreachable&quot;) Then
        WScript.Echo strComputer & &quot;did not respond to ping.&quot;
    Else
        WScript.Echo strComputer & &quot; responded to ping.&quot;
    End If 
Else
    WScript.Echo strComputer & &quot; did not respond to ping.&quot;
End If
  </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f61ee-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f61ee-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f61ee-160">WMI-Tasks für Skripts und Anwendungen</span><span class="sxs-lookup"><span data-stu-id="f61ee-160">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="f61ee-161">WMI C++ Anwendungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="f61ee-161">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="f61ee-162">Technet scriptcenter</span><span class="sxs-lookup"><span data-stu-id="f61ee-162">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

