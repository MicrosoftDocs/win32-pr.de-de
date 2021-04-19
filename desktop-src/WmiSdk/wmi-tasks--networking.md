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
# <a name="wmi-tasks-networking"></a>WMI-Tasks: Netzwerk

WMI-Tasks für Netzwerke verwalten und Abrufen von Informationen zu Verbindungen und IP-oder Mac-Adressen. Weitere Beispiele finden Sie im technet scriptcenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

In den in diesem Thema gezeigten Skript Beispielen werden nur Daten vom lokalen Computer abgerufen. Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remote Computern finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).


Im folgenden Verfahren wird die Vorgehensweise zum Ausführen eines Skripts beschrieben.

**So führen Sie ein Skript aus**

1.  Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung. vb, z. b. *filename.vbs*. Stellen Sie sicher, dass der Text-Editor der Datei keine Erweiterung ". txt" hinzufügt.
2.  Öffnen Sie ein Eingabe Aufforderungs Fenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.
3.  Geben Sie **cscript-filename.vbs** an der Eingabeaufforderung ein.
4.  Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie von einer Eingabeaufforderung mit erhöhten Rechten ausführen. Einige Ereignisprotokolle, z. b. das Sicherheits Ereignisprotokoll, werden möglicherweise durch die Benutzer Zugriffs Steuerung (User Access Control, UAC) geschützt.

> [!Note]  
> Cscript zeigt standardmäßig die Ausgabe eines Skripts im Eingabe Aufforderungs Fenster an. Da WMI-Skripts große Mengen an Ausgaben verursachen können, empfiehlt es sich, die Ausgabe in eine Datei umzuleiten. Geben Sie an der Eingabeaufforderung **cscript filename.vbs > outfile.txt** ein, um die Ausgabe des *filename.vbs* Skripts in *outfile.txt* umzuleiten.

 

In der folgenden Tabelle sind Skript Beispiele aufgelistet, die zum Abrufen verschiedener Datentypen auf dem lokalen Computer verwendet werden können.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vorgehensweisen</th>
<th>WMI-Klassen oder-Methoden</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... eine Netzwerkverbindung mithilfe von WMI deaktivieren?</td>
<td>Wenn Sie DHCP verwenden, verwenden Sie den <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> und die <a href="/windows/desktop/CIMWin32Prov/releasedhcplease-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLease</strong></a> -Methode, um die IP-Adresse freizugeben. Wenn Sie DHCP nicht verwenden, können Sie WMI nicht zum Deaktivieren einer Netzwerkverbindung verwenden. Verwenden Sie zum erneuten Aktivieren der Netzwerkverbindung <a href="/windows/desktop/CIMWin32Prov/renewdhcplease-method-in-class-win32-networkadapterconfiguration"><strong>objnetcard. erneudhcplease</strong></a>. Mithilfe der <a href="/windows/desktop/CIMWin32Prov/releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLeaseAll</strong></a> -Methode und der <a href="/windows/desktop/CIMWin32Prov/renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>erneuerdhcpleaseall</strong></a> -Methode können Sie auch alle DHCP-Leases freigeben oder erneuern.<br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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
<th>PowerShell</th>
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
<td>... Deaktivieren oder Aktivieren einer NIC</td>
<td><p>Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> -Klasse und die Methoden zum <a href="/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter"><strong>Deaktivieren</strong></a> oder <a href="/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter"><strong>aktivieren</strong></a> .</p></td>
</tr>
<tr class="odd">
<td>... bestimmen Sie, welche IP-Adresse einer bestimmten Netzwerkverbindung zugewiesen wurde?</td>
<td><p>Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> -Klasse und die <strong>NetConnectionID</strong> -Eigenschaft, um die Mac-Adresse der Netzwerkverbindung zu ermitteln. Verwenden Sie dann die <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> -Klasse, um die IP-Adresse zu ermitteln, die der Mac-Adresse zugeordnet ist.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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
<th>VB</th>
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
<td>... Bestimmen der Mac-Adresse eines Netzwerkadapters</td>
<td><p>Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> -Klasse, und überprüfen Sie den Wert der <strong>macaddress</strong> -Eigenschaft.</p></td>
</tr>
<tr class="odd">
<td>... bestimmen Sie die IP-Adresse eines Computers?</td>
<td><p>Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> -Klasse, und überprüfen Sie den Wert der <strong>IPAddress</strong> -Eigenschaft. Dies wird als Array zurückgegeben. verwenden Sie daher eine For-Each Schleife, um den Wert zu erhalten.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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
<th>PowerShell</th>
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
<td>...configSie einen Computer, damit er seine IP-Adresse über DHCP erhält?</td>
<td><p>Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> -Klasse und die <a href="/windows/desktop/CIMWin32Prov/enabledhcp-method-in-class-win32-networkadapterconfiguration"><strong>EnableDHCP</strong></a> -Methode.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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
<td>... einem Computer eine statische IP-Adresse zuweisen?</td>
<td><p>Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> -Klasse und die <a href="/windows/desktop/CIMWin32Prov/enablestatic-method-in-class-win32-networkadapterconfiguration"><strong>EnableStatic</strong></a> -Methode.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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
<td>... Abrufen von Informationen zu Netzwerkadaptern, ohne auch Informationen zu Dingen wie RAS-und VPN-Verbindungen abzurufen?</td>
<td><p>Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> -Klasse. Verwenden Sie in Ihrer <a href="querying-with-wql.md">WQL</a> -Abfrage diese Klausel: Where <strong>ipabled</strong>  =  <strong>true</strong>.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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
<td>... Pingen eines Computers, ohne Ping.exe zu verwenden?</td>
<td><p>Verwenden Sie die <a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> -Klasse.</p>
<p><a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> können Daten für Computer zurückgeben, die sowohl IPv4-als auch IPv6-Adressen haben.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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
<th>VB</th>
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



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Tasks für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[WMI C++ Anwendungsbeispiele](wmi-c---application-examples.md)
</dt> <dt>

[Technet scriptcenter](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

