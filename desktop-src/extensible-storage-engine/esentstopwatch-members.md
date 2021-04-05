---
description: 'Erfahren Sie mehr über: esentstopwatch-Member'
title: Esentstopwatch-Member
TOCTitle: EsentStopwatch members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.EsentStopwatch
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstopwatch_members(v=EXCHG.10)
ms:contentKeyID: 55102990
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 36f9d619e104b7d271782c3765adea744beb950e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757987"
---
# <a name="esentstopwatch-members"></a><span data-ttu-id="200cc-103">Esentstopwatch-Member</span><span class="sxs-lookup"><span data-stu-id="200cc-103">EsentStopwatch members</span></span>

<span data-ttu-id="200cc-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="200cc-104">Include protected members</span></span>  
<span data-ttu-id="200cc-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="200cc-105">Include inherited members</span></span>  

<span data-ttu-id="200cc-106">Stellt eine Reihe von Methoden und Eigenschaften bereit, mit denen Sie die Arbeitsstatistik für einen Thread messen können.</span><span class="sxs-lookup"><span data-stu-id="200cc-106">Provides a set of methods and properties that you can use to measure ESENT work statistics for a thread.</span></span> <span data-ttu-id="200cc-107">Wenn die aktuelle Version von ESENT [jetgetthreadstats (JET_THREADSTATS)](./vistaapi.jetgetthreadstats-method.md) nicht unterstützt, sind alle ESENT-Statistiken 0.</span><span class="sxs-lookup"><span data-stu-id="200cc-107">If the current version of ESENT doesn't support [JetGetThreadStats(JET_THREADSTATS)](./vistaapi.jetgetthreadstats-method.md) then all ESENT statistics will be 0.</span></span>

<span data-ttu-id="200cc-108">Der [esentstopwatch](./esentstopwatch-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="200cc-108">The [EsentStopwatch](./esentstopwatch-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="200cc-109">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="200cc-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="200cc-110">Name</span><span class="sxs-lookup"><span data-stu-id="200cc-110">Name</span></span></th>
<th><span data-ttu-id="200cc-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="200cc-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="200cc-113"><a href="dn334872(v=exchg.10).md">Esentstopwatch</a></span><span class="sxs-lookup"><span data-stu-id="200cc-113"><a href="dn334872(v=exchg.10).md">EsentStopwatch</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="200cc-114">Oben</span><span class="sxs-lookup"><span data-stu-id="200cc-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="200cc-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="200cc-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="200cc-116">Name</span><span class="sxs-lookup"><span data-stu-id="200cc-116">Name</span></span></th>
<th><span data-ttu-id="200cc-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="200cc-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="200cc-119"><a href="dn334934(v=exchg.10).md">Verstrichene</a></span><span class="sxs-lookup"><span data-stu-id="200cc-119"><a href="dn334934(v=exchg.10).md">Elapsed</a></span></span></td>
<td><span data-ttu-id="200cc-120">Ruft die gesamte verstrichene Zeit ab, die von der aktuellen Instanz gemessen wurde.</span><span class="sxs-lookup"><span data-stu-id="200cc-120">Gets the total elapsed time measured by the current instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="200cc-122"><a href="dn334933(v=exchg.10).md">IsRunning</a></span><span class="sxs-lookup"><span data-stu-id="200cc-122"><a href="dn334933(v=exchg.10).md">IsRunning</a></span></span></td>
<td><span data-ttu-id="200cc-123">Ruft einen Wert ab, der angibt, ob der esentstopwatch-Timer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="200cc-123">Gets a value indicating whether the EsentStopwatch timer is running.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="200cc-125"><a href="dn334930(v=exchg.10).md">Threadstats</a></span><span class="sxs-lookup"><span data-stu-id="200cc-125"><a href="dn334930(v=exchg.10).md">ThreadStats</a></span></span></td>
<td><span data-ttu-id="200cc-126">Ruft die gesamte ESENT-Arbeitsstatistik ab, die von der aktuellen Instanz gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="200cc-126">Gets the total ESENT work stats measured by the current instance.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="200cc-127">Oben</span><span class="sxs-lookup"><span data-stu-id="200cc-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="200cc-128">Methoden</span><span class="sxs-lookup"><span data-stu-id="200cc-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="200cc-129">Name</span><span class="sxs-lookup"><span data-stu-id="200cc-129">Name</span></span></th>
<th><span data-ttu-id="200cc-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="200cc-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="200cc-132"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></span><span class="sxs-lookup"><span data-stu-id="200cc-132"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="200cc-133">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="200cc-133">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="200cc-135"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="200cc-135"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="200cc-136">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="200cc-136">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="200cc-138"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="200cc-138"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="200cc-139">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="200cc-139">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="200cc-141"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="200cc-141"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="200cc-142">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="200cc-142">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="200cc-144"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></span><span class="sxs-lookup"><span data-stu-id="200cc-144"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="200cc-145">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="200cc-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="200cc-147"><a href="dn334869(v=exchg.10).md">Zurücksetzen</a></span><span class="sxs-lookup"><span data-stu-id="200cc-147"><a href="dn334869(v=exchg.10).md">Reset</a></span></span></td>
<td><span data-ttu-id="200cc-148">Beendet die Zeitintervall Messung und setzt die Thread Statistik zurück.</span><span class="sxs-lookup"><span data-stu-id="200cc-148">Stops time interval measurement and resets the thread statistics.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="200cc-150"><a href="dn334931(v=exchg.10).md">Starten</a></span><span class="sxs-lookup"><span data-stu-id="200cc-150"><a href="dn334931(v=exchg.10).md">Start</a></span></span></td>
<td><span data-ttu-id="200cc-151">Beginnt mit dem Messen der ESENT-Arbeit.</span><span class="sxs-lookup"><span data-stu-id="200cc-151">Starts measuring ESENT work.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="200cc-154"><a href="dn334877(v=exchg.10).md">StartNew</a></span><span class="sxs-lookup"><span data-stu-id="200cc-154"><a href="dn334877(v=exchg.10).md">StartNew</a></span></span></td>
<td><span data-ttu-id="200cc-155">Initialisiert eine neue esentstopwatch-Instanz und beginnt mit der Messung der verstrichenen Zeit.</span><span class="sxs-lookup"><span data-stu-id="200cc-155">Initializes a new EsentStopwatch instance and starts measuring elapsed time.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="200cc-157"><a href="dn334932(v=exchg.10).md">Beenden</a></span><span class="sxs-lookup"><span data-stu-id="200cc-157"><a href="dn334932(v=exchg.10).md">Stop</a></span></span></td>
<td><span data-ttu-id="200cc-158">Beendet das Messen der ESENT-Arbeit.</span><span class="sxs-lookup"><span data-stu-id="200cc-158">Stops measuring ESENT work.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="200cc-160"><a href="dn334873(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="200cc-160"><a href="dn334873(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="200cc-161">Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die die aktuelle <a href="/dotnet/api/system.diagnostics.stopwatch">Stopwatch</a>darstellt.</span><span class="sxs-lookup"><span data-stu-id="200cc-161">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="/dotnet/api/system.diagnostics.stopwatch">Stopwatch</a>.</span></span> <span data-ttu-id="200cc-162">(Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="200cc-162">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="200cc-163">Oben</span><span class="sxs-lookup"><span data-stu-id="200cc-163">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="200cc-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="200cc-164">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="200cc-165">Referenz</span><span class="sxs-lookup"><span data-stu-id="200cc-165">Reference</span></span>

[<span data-ttu-id="200cc-166">Esentstopwatch-Klasse</span><span class="sxs-lookup"><span data-stu-id="200cc-166">EsentStopwatch class</span></span>](./esentstopwatch-class.md)

[<span data-ttu-id="200cc-167">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="200cc-167">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
