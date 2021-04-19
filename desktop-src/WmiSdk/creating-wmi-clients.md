---
description: WMI stellt eine standardisierte System Verwaltungsinfrastruktur bereit, die von einer Reihe verschiedener Clients genutzt werden kann.
ms.assetid: 7aa0ead7-010c-4ad2-b6ba-0ef84263d5c6
ms.tgt_platform: multiple
title: Erstellen von WMI-Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd6d89c63218ffd20ef66b2115e581bdb9c4373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350590"
---
# <a name="creating-wmi-clients"></a>Erstellen von WMI-Clients

WMI stellt eine standardisierte System Verwaltungsinfrastruktur bereit, die von einer Reihe verschiedener Clients genutzt werden kann. Diese Clients reichen vom wmic.exe Befehlszeilen Tool bis System Center Operations Manager. Sie können eigene WMI-Clients schreiben, indem Sie entweder die WMI-Skript-API, die native C++-API oder die Typen im Namespace System. Management .NET Framework Klassenbibliothek verwenden.

## <a name="how-to-create-a-wmi-client"></a>Erstellen eines WMI-Clients

Die Kernfunktionen von WMI bestehen aus dem Abrufen von Objekten aus dem WMI-Repository und dem untersuchen der Eigenschaften dieser Objekte. Sie können diese Eigenschaften auch aktualisieren oder Methoden für diese Eigenschaften aufzurufen. In den folgenden Beispielen wird gezeigt, wie eine grundlegende WMI-Verwaltungsaufgabe durchgeführt wird: Abrufen des Namens des lokalen Computers.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Begriff</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Erstellen eines Clients mit PowerShell<br/></td>
<td>WMI und PowerShell sind eng integriert. Daher ist das Abrufen von WMI-Objekten mit PowerShell lediglich eine Frage des Aufrufs des Get-WmiObject Cmdlets. Beachten Sie, dass der erste Code Ausschnitt aus Gründen der Konsistenz viele der Standardwerte explizit angibt. bei der zweiten wird davon ausgegangen, dass die Standardwerte richtig sind.<br/> <span data-codelanguage="PowerShell"></span>
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
<td><p>VBScript war die ursprüngliche Skriptsprache, die häufig mit WMI verwendet wurde. Obwohl PowerShell beliebter geworden ist, sind viele der vorhandenen Codebeispiele in dieser Dokumentation in VBScript geschrieben. Beachten Sie, dass in diesem speziellen VBScript-Beispiel explizit sowohl der Pfad des lokalen Computers als auch die Ebene des Identitäts Wechsels angegeben wird. Dies ist nicht erforderlich, wird jedoch häufig als bewährte Vorgehensweise empfohlen.</p>
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
<td><p><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Erstellen eines Clients mit c# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a>)</p></td>
<td><p>Dieser Namespace enthält die aktuelle Lösung für den Zugriff auf WMI mit verwaltetem Code und wird als Windows-Verwaltungsinfrastruktur (Mi oder WMIv2) bezeichnet. Derzeit ist Mi die unterstützte Technologie zum Erstellen von verwalteten Verwaltungs Clients. Weitere Informationen finden Sie unter Gewusst <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">wie: Implementieren eines verwalteten Mi-Clients</a> und Gewusst wie: <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">Implementieren eines nativen Mi-Clients</a>.</p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
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
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

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
<td><p><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Erstellen eines Clients mit c# (<a href="/dotnet/api/system.management">System. Management</a>)</p></td>
<td><p>Dieser Namespace enthält die ursprüngliche Lösung für den Zugriff auf WMI mit verwaltetem Code. Während die <a href="/dotnet/api/system.management">System. Management</a> -Klassen weiterhin verfügbar sind, sind die <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a> -Klassen in der Regel effizienter und skalierbar. Daher wird empfohlen, anstelle der ursprünglichen WMI-Klassen die Mi-Klassen zu verwenden.</p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
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
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

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



 

In der folgenden Tabelle sind die in diesem Abschnitt behandelten Themen aufgeführt.



| Thema                                                                                                        | BESCHREIBUNG                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md)                         | Beschreibt eine Reihe von Problemen, die auftreten, wenn die WMI-Infrastruktur von Clients auf einem Remote Computer verwendet wird.                                                                                          |
| [WMI-Tasks für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md)                         | Zeigt Beispielcode für WMI-Client.                                                                                                                                                                 |
| [Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md)                             | Bietet Informationen zum Erstellen verschiedener WMI-Clients.                                                                                                                                       |
| [Überwachen von Leistungsdaten](monitoring-performance-data.md)                                               | Beschreibt die Verwendung von WMI zum Überwachen von Leistungsdaten.                                                                                                                                          |
| [Empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md)                                                           | Beschreibt, wie WMI-Ereignisse angezeigt werden.                                                                                                                                                              |
| [Überwachen von Ereignissen](monitoring-events.md)                                                                   | Hier wird beschrieben, wie WMI-Ereignisse überwacht werden.                                                                                                                                                           |
| [Abfragen mit WQL](querying-with-wql.md)                                                                   | Führt die WMI Query Language (WQL) ein.                                                                                                                                                       |
| [Abfragen des Status optionaler Funktionen](querying-the-status-of-optional-features.md)                     | In Windows 7 implementierte WMI die [**Win32 \_ optionalfeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) -Klasse. Diese Klasse ruft den Status der optionalen Features auf, die auf einem Computer vorhanden sind. |
| [Beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md)                       | Konzentriert sich auf die Syntax, um den Speicherort einer verwalteten WMI-Entität zu beschreiben.                                                                                                                     |
| [Zugreifen auf andere Betriebs System Funktionen mit WMI](accessing-other-operating-system-features-with-wmi.md) | Beschreibt das Schreiben von WMI-Clients, die auf Gerätetreiber, Active Directory und SNMP-Geräte zugreifen.                                                                                             |
| [Zugreifen auf Daten im Interop-Namespace](accessing-data-in-the-interop-namespace.md)                       | Mithilfe von Zuordnungs Anbietern können Windows-Verwaltungsinstrumentation (WMI)-Clients Profile und zugehörige Klassen Instanzen aus unterschiedlichen Namespaces durchlaufen und abrufen.                      |
| [Manipulieren von Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md)               | Beschreibt die allgemeinen Aufgaben, die von WMI-Clients ausgeführt werden müssen.                                                                                                                                      |
| [Verknüpfen von Klassen](linking-classes-together.md)                                                     | Erläutert den Ansichts Anbieter und wie er zum Zusammenführen von Informationen aus mehreren WMI-Klassen verwendet werden kann.                                                                                    |
| [Ändern der System Registrierung](modifying-the-system-registry.md)                                           | Beschreibt, wie WMI-Clients WMI zum Verwalten von System Registrierungsinformationen verwenden können.                                                                                                                   |



 

