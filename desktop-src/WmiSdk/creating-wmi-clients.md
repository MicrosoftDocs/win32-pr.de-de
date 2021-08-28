---
description: WMI bietet eine standardisierte Systemverwaltungsinfrastruktur, die von einer Reihe verschiedener Clients genutzt werden kann.
ms.assetid: 7aa0ead7-010c-4ad2-b6ba-0ef84263d5c6
ms.tgt_platform: multiple
title: Erstellen von WMI-Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95123d4462408a25591df2babb8b1ddd83942e5e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883052"
---
# <a name="creating-wmi-clients"></a>Erstellen von WMI-Clients

WMI bietet eine standardisierte Systemverwaltungsinfrastruktur, die von einer Reihe verschiedener Clients genutzt werden kann. Diese Clients reichen vom befehlszeilentool wmic.exe bis zu System Center Operations Manager. Sie können Ihre eigenen WMI-Clients schreiben, indem Sie entweder die WMI-Skripterstellungs-API, die native C++-API oder die Typen im System.Management .NET Framework Klassenbibliotheksnamespace verwenden.

## <a name="how-to-create-a-wmi-client"></a>Erstellen eines WMI-Clients

Die Kernfunktionalität von WMI besteht aus dem Abrufen von Objekten aus dem WMI-Repository und dem Untersuchen der Eigenschaften dieser Objekte. Sie können diese Eigenschaften auch aktualisieren oder Methoden für diese Eigenschaften aufrufen. Die folgenden Beispiele zeigen, wie Sie eine einfache WMI-Verwaltungsaufgabe ausführen: abrufen des Namens des lokalen Computers.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Begriff</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Erstellen eines Clients mit PowerShell<br/></td>
<td>WMI und PowerShell sind eng integriert. Daher muss beim Abrufen von WMI-Objekten mit PowerShell einfach das cmdlet Get-WmiObject aufgerufen werden. Beachten Sie, dass im ersten Codeausschnitt aus Konsistenzgründen viele der Standardwerte explizit angegeben werden. Bei der zweiten wird davon ausgegangen, dass die Standardwerte korrekt sind.<br/> <span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#explicitly states many of the default parameters
$myComputer = Get-WmiObject -ComputerName &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Query &quot;SELECT * FROM Win32_ComputerSystem&quot;
foreach ($computer in $myComputer)
{ &quot;System Name: &quot; + $computer.name }

#assumes the default values are correct
Get-WmiObject Win32_ComputerSystem | Format-Table &quot;Name&quot;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><p><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Erstellen eines Clients mit VBScript</p></td>
<td><p>VBScript war die ursprüngliche Skriptsprache, die häufig mit WMI verwendet wurde. Obwohl PowerShell immer beliebter wurde, sind viele der vorhandenen Codebeispiele in dieser Dokumentation in VBScript geschrieben. Beachten Sie, dass in diesem vbscript-Beispiel sowohl der Pfad des lokalen Computers als auch die Identitätswechselebene explizit festgelegt werden. dies ist nicht erforderlich, aber häufig eine bewährte Methode.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Computer Name: &quot; & objItem.Name
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><p><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Erstellen eines Clients mit C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a>)</p></td>
<td><p>Dieser Namespace enthält die aktuelle Lösung für den Zugriff auf WMI mit verwaltetem Code und wird als Windows Management Infrastructure (MI, oder WMIv2) bezeichnet. Mi ist derzeit die unterstützte Technologie zum Erstellen verwalteter Verwaltungsclients. Weitere Informationen finden Sie unter <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">How to Implement a Managed MI Client (Implementieren eines verwalteten MI-Clients)</a> und How to Implement a Native MI Client <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">(Implementieren eines nativen MI-Clients).</a></p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C#</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable&lt;CimInstance&gt; queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Name&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Erstellen eines Clients mit C# (<a href="/dotnet/api/system.management">System.Management</a>)</p></td>
<td><p>Dieser Namespace enthält die ursprüngliche Projektmappe für den Zugriff auf WMI mit verwaltetem Code. Obwohl die <a href="/dotnet/api/system.management">System.Management-Klassen</a> weiterhin verfügbar sind, sind die <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure-Klassen</a> im Allgemeinen effizienter und besser skaliert. Daher wird empfohlen, anstelle der ursprünglichen WMI-Klassen die MI-Klassen zu verwenden.</p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C#</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable&lt;CimInstance&gt; queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Name&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle sind die themen aufgeführt, die in diesem Abschnitt behandelt werden.



| Thema                                                                                                        | Beschreibung                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Herstellen einer Verbindung mit WMI auf einem Remotecomputer](connecting-to-wmi-on-a-remote-computer.md)                         | Beschreibt eine Reihe von Problemen, die auftreten, wenn Clients die WMI-Infrastruktur auf einem Remotecomputer verwenden.                                                                                          |
| [WMI-Aufgaben für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md)                         | Zeigt WMI-Beispielclientcode an.                                                                                                                                                                 |
| [Erstellen einer WMI-Anwendung oder eines WMI-Skripts](creating-a-wmi-application-or-script.md)                             | Stellt Informationen zum Erstellen verschiedener WMI-Clients bereit.                                                                                                                                       |
| [Überwachen von Leistungsdaten](monitoring-performance-data.md)                                               | Beschreibt die Verwendung von WMI zum Überwachen von Leistungsdaten.                                                                                                                                          |
| [Empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md)                                                           | Beschreibt, wie WMI-Ereignisse angezeigt werden.                                                                                                                                                              |
| [Überwachen von Ereignissen](monitoring-events.md)                                                                   | Beschreibt, wie WMI-Ereignisse überwacht werden.                                                                                                                                                           |
| [Abfragen mit WQL](querying-with-wql.md)                                                                   | Führt die WMI Query Language (WQL) ein.                                                                                                                                                       |
| [Abfragen des Status optionaler Features](querying-the-status-of-optional-features.md)                     | In Windows 7 hat WMI die [**Win32 \_ OptionalFeature-Klasse**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) implementiert. Diese Klasse ruft den Status der optionalen Features ab, die auf einem Computer vorhanden sind. |
| [Beschreiben des Speicherorts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md)                       | Konzentriert sich auf die Syntax zum Beschreiben des Speicherorts einer verwalteten WMI-Entität.                                                                                                                     |
| [Zugreifen auf andere Betriebssystemfeatures mit WMI](accessing-other-operating-system-features-with-wmi.md) | Beschreibt, wie WMI-Clients geschrieben werden, die auf Gerätetreiber, Active Directory und SNMP-Geräte zugreifen.                                                                                             |
| [Zugreifen auf Daten im Interop-Namespace](accessing-data-in-the-interop-namespace.md)                       | Zuordnungsanbieter ermöglichen Windows Management Instrumentation(WMI)-Clients das Durchlaufen und Abrufen von Profilen und zugeordneten Klasseninstanzen aus verschiedenen Namespaces.                      |
| [Bearbeiten von Klassen- und Instanzinformationen](manipulating-class-and-instance-information.md)               | Beschreibt die allgemeinen Aufgaben, die WMI-Clients ausführen müssen.                                                                                                                                      |
| [Verknüpfen von Klassen](linking-classes-together.md)                                                     | Erläutert den Ansichtsanbieter und wie er verwendet werden kann, um Informationen aus mehreren WMI-Klassen zusammenzuführen.                                                                                    |
| [Ändern der Systemregistrierung](modifying-the-system-registry.md)                                           | Beschreibt, wie WMI-Clients WMI zum Verwalten von Systemregistrierungsinformationen verwenden können.                                                                                                                   |



 

