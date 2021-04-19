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
# <a name="creating-wmi-clients"></a><span data-ttu-id="ca817-103">Erstellen von WMI-Clients</span><span class="sxs-lookup"><span data-stu-id="ca817-103">Creating WMI Clients</span></span>

<span data-ttu-id="ca817-104">WMI stellt eine standardisierte System Verwaltungsinfrastruktur bereit, die von einer Reihe verschiedener Clients genutzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ca817-104">WMI provides a standardized system management infrastructure that can be leveraged by a number of different clients.</span></span> <span data-ttu-id="ca817-105">Diese Clients reichen vom wmic.exe Befehlszeilen Tool bis System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="ca817-105">These clients range from the wmic.exe command line tool to System Center Operations Manager.</span></span> <span data-ttu-id="ca817-106">Sie können eigene WMI-Clients schreiben, indem Sie entweder die WMI-Skript-API, die native C++-API oder die Typen im Namespace System. Management .NET Framework Klassenbibliothek verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca817-106">You can write your own WMI clients by using either the WMI Scripting API, the native C++ API or by using the types in the System.Management .NET Framework class library namespace.</span></span>

## <a name="how-to-create-a-wmi-client"></a><span data-ttu-id="ca817-107">Erstellen eines WMI-Clients</span><span class="sxs-lookup"><span data-stu-id="ca817-107">How to create a WMI client</span></span>

<span data-ttu-id="ca817-108">Die Kernfunktionen von WMI bestehen aus dem Abrufen von Objekten aus dem WMI-Repository und dem untersuchen der Eigenschaften dieser Objekte.</span><span class="sxs-lookup"><span data-stu-id="ca817-108">The core functionality of WMI consists of retrieving objects from the WMI repository and examining the properties of those objects.</span></span> <span data-ttu-id="ca817-109">Sie können diese Eigenschaften auch aktualisieren oder Methoden für diese Eigenschaften aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ca817-109">You can also choose to update those properties, or call methods on those properties.</span></span> <span data-ttu-id="ca817-110">In den folgenden Beispielen wird gezeigt, wie eine grundlegende WMI-Verwaltungsaufgabe durchgeführt wird: Abrufen des Namens des lokalen Computers.</span><span class="sxs-lookup"><span data-stu-id="ca817-110">The following examples show how to perform a basic WMI administration task: retrieving the name of the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca817-111">Begriff</span><span class="sxs-lookup"><span data-stu-id="ca817-111">Term</span></span></th>
<th><span data-ttu-id="ca817-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca817-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ca817-113"><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Erstellen eines Clients mit PowerShell</span><span class="sxs-lookup"><span data-stu-id="ca817-113"><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Creating a client with PowerShell</span></span><br/></td>
<td><span data-ttu-id="ca817-114">WMI und PowerShell sind eng integriert. Daher ist das Abrufen von WMI-Objekten mit PowerShell lediglich eine Frage des Aufrufs des Get-WmiObject Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="ca817-114">WMI and PowerShell are tightly integrated; as such, retrieving WMI objects with PowerShell is simply a matter of calling the Get-WmiObject cmdlet.</span></span> <span data-ttu-id="ca817-115">Beachten Sie, dass der erste Code Ausschnitt aus Gründen der Konsistenz viele der Standardwerte explizit angibt. bei der zweiten wird davon ausgegangen, dass die Standardwerte richtig sind.</span><span class="sxs-lookup"><span data-stu-id="ca817-115">Note that for consistency, the first code snippet explicitly states many of the default values; the second assumes that the default values are correct.</span></span><br/> <span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca817-116">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ca817-116">PowerShell</span></span></th>
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
<td><p><span data-ttu-id="ca817-117"><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Erstellen eines Clients mit VBScript</span><span class="sxs-lookup"><span data-stu-id="ca817-117"><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Creating a client with VBScript</span></span></p></td>
<td><p><span data-ttu-id="ca817-118">VBScript war die ursprüngliche Skriptsprache, die häufig mit WMI verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ca817-118">VBScript was the original scripting language that had common use with WMI.</span></span> <span data-ttu-id="ca817-119">Obwohl PowerShell beliebter geworden ist, sind viele der vorhandenen Codebeispiele in dieser Dokumentation in VBScript geschrieben.</span><span class="sxs-lookup"><span data-stu-id="ca817-119">While PowerShell has become more popular, many of the existing code samples in this documentation are written in VBScript.</span></span> <span data-ttu-id="ca817-120">Beachten Sie, dass in diesem speziellen VBScript-Beispiel explizit sowohl der Pfad des lokalen Computers als auch die Ebene des Identitäts Wechsels angegeben wird. Dies ist nicht erforderlich, wird jedoch häufig als bewährte Vorgehensweise empfohlen.</span><span class="sxs-lookup"><span data-stu-id="ca817-120">Note that this particular VBScript sample explicitly states both the local machine path as well as the impersonation level; this is not required, but is often a best practice.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca817-121">VB</span><span class="sxs-lookup"><span data-stu-id="ca817-121">VB</span></span></th>
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
<td><p><span data-ttu-id="ca817-122"><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Erstellen eines Clients mit c# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a>)</span><span class="sxs-lookup"><span data-stu-id="ca817-122"><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Creating a client with C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a>)</span></span></p></td>
<td><p><span data-ttu-id="ca817-123">Dieser Namespace enthält die aktuelle Lösung für den Zugriff auf WMI mit verwaltetem Code und wird als Windows-Verwaltungsinfrastruktur (Mi oder WMIv2) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ca817-123">This namespace contains the current solution for accessing WMI with managed code, and is known as the Windows Management Infrastructure (MI, or WMIv2).</span></span> <span data-ttu-id="ca817-124">Derzeit ist Mi die unterstützte Technologie zum Erstellen von verwalteten Verwaltungs Clients.</span><span class="sxs-lookup"><span data-stu-id="ca817-124">Currently, MI is the supported technology for creating managed management clients.</span></span> <span data-ttu-id="ca817-125">Weitere Informationen finden Sie unter Gewusst <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">wie: Implementieren eines verwalteten Mi-Clients</a> und Gewusst wie: <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">Implementieren eines nativen Mi-Clients</a>.</span><span class="sxs-lookup"><span data-stu-id="ca817-125">For more information, see <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">How to Implement a Managed MI Client</a> and <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">How to Implement a Native MI Client</a>.</span></span></p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca817-126">C#</span><span class="sxs-lookup"><span data-stu-id="ca817-126">C#</span></span></th>
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
<td><p><span data-ttu-id="ca817-127"><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Erstellen eines Clients mit c# (<a href="/dotnet/api/system.management">System. Management</a>)</span><span class="sxs-lookup"><span data-stu-id="ca817-127"><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Creating a client with C# (<a href="/dotnet/api/system.management">System.Management</a>)</span></span></p></td>
<td><p><span data-ttu-id="ca817-128">Dieser Namespace enthält die ursprüngliche Lösung für den Zugriff auf WMI mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="ca817-128">This namespace contains the original solution for accessing WMI with managed code.</span></span> <span data-ttu-id="ca817-129">Während die <a href="/dotnet/api/system.management">System. Management</a> -Klassen weiterhin verfügbar sind, sind die <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a> -Klassen in der Regel effizienter und skalierbar.</span><span class="sxs-lookup"><span data-stu-id="ca817-129">While the <a href="/dotnet/api/system.management">System.Management</a> classes are still available, the <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a> classes are generally more efficient and scale better.</span></span> <span data-ttu-id="ca817-130">Daher wird empfohlen, anstelle der ursprünglichen WMI-Klassen die Mi-Klassen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca817-130">As such, it is recommended that you use the MI classes, rather than the original WMI classes.</span></span></p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca817-131">C#</span><span class="sxs-lookup"><span data-stu-id="ca817-131">C#</span></span></th>
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



 

<span data-ttu-id="ca817-132">In der folgenden Tabelle sind die in diesem Abschnitt behandelten Themen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca817-132">The following table lists the topics covered in this section.</span></span>



| <span data-ttu-id="ca817-133">Thema</span><span class="sxs-lookup"><span data-stu-id="ca817-133">Topic</span></span>                                                                                                        | <span data-ttu-id="ca817-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca817-134">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca817-135">Herstellen einer Verbindung mit WMI auf einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="ca817-135">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)                         | <span data-ttu-id="ca817-136">Beschreibt eine Reihe von Problemen, die auftreten, wenn die WMI-Infrastruktur von Clients auf einem Remote Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ca817-136">Describes a number of issues that arise when clients use the WMI infrastructure on a remote computer.</span></span>                                                                                          |
| [<span data-ttu-id="ca817-137">WMI-Tasks für Skripts und Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ca817-137">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)                         | <span data-ttu-id="ca817-138">Zeigt Beispielcode für WMI-Client.</span><span class="sxs-lookup"><span data-stu-id="ca817-138">Shows example WMI client code.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="ca817-139">Erstellen einer WMI-Anwendung oder eines Skripts</span><span class="sxs-lookup"><span data-stu-id="ca817-139">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)                             | <span data-ttu-id="ca817-140">Bietet Informationen zum Erstellen verschiedener WMI-Clients.</span><span class="sxs-lookup"><span data-stu-id="ca817-140">Provides information about creating various WMI clients.</span></span>                                                                                                                                       |
| [<span data-ttu-id="ca817-141">Überwachen von Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="ca817-141">Monitoring Performance Data</span></span>](monitoring-performance-data.md)                                               | <span data-ttu-id="ca817-142">Beschreibt die Verwendung von WMI zum Überwachen von Leistungsdaten.</span><span class="sxs-lookup"><span data-stu-id="ca817-142">Describes how to use WMI to monitor performance data.</span></span>                                                                                                                                          |
| [<span data-ttu-id="ca817-143">Empfangen eines WMI-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="ca817-143">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)                                                           | <span data-ttu-id="ca817-144">Beschreibt, wie WMI-Ereignisse angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ca817-144">Describes how to view WMI events.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="ca817-145">Überwachen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="ca817-145">Monitoring Events</span></span>](monitoring-events.md)                                                                   | <span data-ttu-id="ca817-146">Hier wird beschrieben, wie WMI-Ereignisse überwacht werden.</span><span class="sxs-lookup"><span data-stu-id="ca817-146">Describes how to monitor WMI events.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="ca817-147">Abfragen mit WQL</span><span class="sxs-lookup"><span data-stu-id="ca817-147">Querying with WQL</span></span>](querying-with-wql.md)                                                                   | <span data-ttu-id="ca817-148">Führt die WMI Query Language (WQL) ein.</span><span class="sxs-lookup"><span data-stu-id="ca817-148">Introduces the WMI Query Language (WQL).</span></span>                                                                                                                                                       |
| [<span data-ttu-id="ca817-149">Abfragen des Status optionaler Funktionen</span><span class="sxs-lookup"><span data-stu-id="ca817-149">Querying the Status of Optional Features</span></span>](querying-the-status-of-optional-features.md)                     | <span data-ttu-id="ca817-150">In Windows 7 implementierte WMI die [**Win32 \_ optionalfeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="ca817-150">In Windows 7, WMI implemented the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class.</span></span> <span data-ttu-id="ca817-151">Diese Klasse ruft den Status der optionalen Features auf, die auf einem Computer vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ca817-151">This class retrieves the status of the optional features that are present on a computer.</span></span> |
| [<span data-ttu-id="ca817-152">Beschreiben des Speicher Orts eines WMI-Objekts</span><span class="sxs-lookup"><span data-stu-id="ca817-152">Describing the Location of a WMI Object</span></span>](describing-the-location-of-a-wmi-object.md)                       | <span data-ttu-id="ca817-153">Konzentriert sich auf die Syntax, um den Speicherort einer verwalteten WMI-Entität zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ca817-153">Focuses on the syntax for describing the location of a WMI managed entity.</span></span>                                                                                                                     |
| [<span data-ttu-id="ca817-154">Zugreifen auf andere Betriebs System Funktionen mit WMI</span><span class="sxs-lookup"><span data-stu-id="ca817-154">Accessing Other Operating System Features with WMI</span></span>](accessing-other-operating-system-features-with-wmi.md) | <span data-ttu-id="ca817-155">Beschreibt das Schreiben von WMI-Clients, die auf Gerätetreiber, Active Directory und SNMP-Geräte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ca817-155">Describes how to write WMI clients that access device drivers, Active Directory, and SNMP devices.</span></span>                                                                                             |
| [<span data-ttu-id="ca817-156">Zugreifen auf Daten im Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ca817-156">Accessing Data in the Interop Namespace</span></span>](accessing-data-in-the-interop-namespace.md)                       | <span data-ttu-id="ca817-157">Mithilfe von Zuordnungs Anbietern können Windows-Verwaltungsinstrumentation (WMI)-Clients Profile und zugehörige Klassen Instanzen aus unterschiedlichen Namespaces durchlaufen und abrufen.</span><span class="sxs-lookup"><span data-stu-id="ca817-157">Association providers enable Windows Management Instrumentation (WMI) clients to traverse and retrieve profiles and associated class instances from different namespaces.</span></span>                      |
| [<span data-ttu-id="ca817-158">Manipulieren von Klassen-und Instanzinformationen</span><span class="sxs-lookup"><span data-stu-id="ca817-158">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)               | <span data-ttu-id="ca817-159">Beschreibt die allgemeinen Aufgaben, die von WMI-Clients ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ca817-159">Describes the common tasks that WMI clients must perform.</span></span>                                                                                                                                      |
| [<span data-ttu-id="ca817-160">Verknüpfen von Klassen</span><span class="sxs-lookup"><span data-stu-id="ca817-160">Linking Classes Together</span></span>](linking-classes-together.md)                                                     | <span data-ttu-id="ca817-161">Erläutert den Ansichts Anbieter und wie er zum Zusammenführen von Informationen aus mehreren WMI-Klassen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ca817-161">Discusses the view provider and how it can be used to bring together information from multiple WMI classes.</span></span>                                                                                    |
| [<span data-ttu-id="ca817-162">Ändern der System Registrierung</span><span class="sxs-lookup"><span data-stu-id="ca817-162">Modifying the System Registry</span></span>](modifying-the-system-registry.md)                                           | <span data-ttu-id="ca817-163">Beschreibt, wie WMI-Clients WMI zum Verwalten von System Registrierungsinformationen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="ca817-163">Describes how WMI clients can use WMI to manage system registry information.</span></span>                                                                                                                   |



 

