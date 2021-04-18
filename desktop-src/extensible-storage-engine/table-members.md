---
description: 'Weitere Informationen finden Sie hier: Tabellen Elemente'
title: 'Tabellenmember '
TOCTitle: Table members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Table
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table_members(v=EXCHG.10)
ms:contentKeyID: 55104054
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: b4e5bd09cf1c450197978e3126dc63fe96ec6425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571194"
---
# <a name="table-members"></a><span data-ttu-id="2ba2b-103">Tabellenmember </span><span class="sxs-lookup"><span data-stu-id="2ba2b-103">Table members</span></span>

<span data-ttu-id="2ba2b-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="2ba2b-104">Include protected members</span></span>  
<span data-ttu-id="2ba2b-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="2ba2b-105">Include inherited members</span></span>  

<span data-ttu-id="2ba2b-106">Eine Klasse, die eine JET_TABLEID in einem verwerfbaren Objekt kapselt.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-106">A class that encapsulates a JET_TABLEID in a disposable object.</span></span> <span data-ttu-id="2ba2b-107">Dadurch wird eine vorhandene Tabelle geöffnet.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-107">This opens an existing table.</span></span> <span data-ttu-id="2ba2b-108">Verwenden Sie zum Erstellen einer Tabelle die jetkreatetable-Methode.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-108">To create a table use the JetCreateTable method.</span></span>

<span data-ttu-id="2ba2b-109">Der [Tabellentyp](./table-class.md) macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-109">The [Table](./table-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="2ba2b-110">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="2ba2b-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2ba2b-111">Name</span><span class="sxs-lookup"><span data-stu-id="2ba2b-111">Name</span></span></th>
<th><span data-ttu-id="2ba2b-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ba2b-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="2ba2b-114"><a href="dn351234(v=exchg.10).md">Table</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-114"><a href="dn351234(v=exchg.10).md">Table</a></span></span></td>
<td><span data-ttu-id="2ba2b-115">Initialisiert eine neue Instanz der Table-Klasse.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-115">Initializes a new instance of the Table class.</span></span> <span data-ttu-id="2ba2b-116">Die Tabelle wird aus der angegebenen Datenbank geöffnet.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-116">The table is opened from the given database.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ba2b-117">Oben</span><span class="sxs-lookup"><span data-stu-id="2ba2b-117">Top</span></span>

## <a name="properties"></a><span data-ttu-id="2ba2b-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2ba2b-118">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2ba2b-119">Name</span><span class="sxs-lookup"><span data-stu-id="2ba2b-119">Name</span></span></th>
<th><span data-ttu-id="2ba2b-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ba2b-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Geschützte Eigenschaft" alt="Protected property" /></td>
<td><span data-ttu-id="2ba2b-122"><a href="dn350578(v=exchg.10).md">Hasresource</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-122"><a href="dn350578(v=exchg.10).md">HasResource</a></span></span></td>
<td><span data-ttu-id="2ba2b-123">Ruft einen Wert ab, der angibt, ob die zugrunde liegende Ressource zurzeit zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-123">Gets a value indicating whether the underlying resource is currently allocated.</span></span> <span data-ttu-id="2ba2b-124">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="2ba2b-124">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="2ba2b-126"><a href="dn351171(v=exchg.10).md">Jettableid</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-126"><a href="dn351171(v=exchg.10).md">JetTableid</a></span></span></td>
<td><span data-ttu-id="2ba2b-127">Ruft den JET_TABLEID ab, der in dieser Tabelle enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-127">Gets the JET_TABLEID that this table contains.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="2ba2b-129"><a href="dn351170(v=exchg.10).md">Name</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-129"><a href="dn351170(v=exchg.10).md">Name</a></span></span></td>
<td><span data-ttu-id="2ba2b-130">Ruft den Namen dieser Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-130">Gets the name of this table.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ba2b-131">Oben</span><span class="sxs-lookup"><span data-stu-id="2ba2b-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="2ba2b-132">Methoden</span><span class="sxs-lookup"><span data-stu-id="2ba2b-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2ba2b-133">Name</span><span class="sxs-lookup"><span data-stu-id="2ba2b-133">Name</span></span></th>
<th><span data-ttu-id="2ba2b-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ba2b-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="2ba2b-136"><a href="dn350541(v=exchg.10).md">Checkobjectisnotverworfen</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="2ba2b-137">Löst eine Ausnahme aus, wenn dieses Objekt verworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-137">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="2ba2b-138">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="2ba2b-138">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="2ba2b-140"><a href="dn351235(v=exchg.10).md">Schließen</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-140"><a href="dn351235(v=exchg.10).md">Close</a></span></span></td>
<td><span data-ttu-id="2ba2b-141">Schließen Sie die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-141">Close the table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="2ba2b-143"><a href="dn350553(v=exchg.10).md">Verwerfen ()</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-143"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="2ba2b-144">Löschen Sie dieses Objekt, und veröffentlichen Sie die zugrunde liegende ESENT-Ressource.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-144">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="2ba2b-145">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="2ba2b-145">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="2ba2b-147"><a href="dn350543(v=exchg.10).md">Verwerfen (Boolean)</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-147"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="2ba2b-148">Wird von verwerfen und dem Finalizer aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-148">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="2ba2b-149">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="2ba2b-149">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="2ba2b-151"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-151"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="2ba2b-152">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="2ba2b-152">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="2ba2b-154"><a href="dn350552(v=exchg.10).md">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-154"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="2ba2b-155">Schließt eine Instanz der esentresource-Klasse ab.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-155">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="2ba2b-156">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="2ba2b-156">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="2ba2b-158"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-158"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="2ba2b-159">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="2ba2b-159">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="2ba2b-161"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-161"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="2ba2b-162">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="2ba2b-162">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="2ba2b-164"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-164"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="2ba2b-165">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="2ba2b-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="2ba2b-167"><a href="dn351168(v=exchg.10).md">Releaseresource</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-167"><a href="dn351168(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="2ba2b-168">Freigeben der zugrunde liegenden JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-168">Free the underlying JET_TABLEID.</span></span> <span data-ttu-id="2ba2b-169">(Überschreibt <a href="dn350545(v=exchg.10).md">esentresource. releaseresource ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="2ba2b-169">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="2ba2b-171"><a href="dn350576(v=exchg.10).md">Resourcewaszugewiesen</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-171"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="2ba2b-172">Wird von einer Unterklasse aufgerufen, wenn eine Ressource zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-172">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="2ba2b-173">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="2ba2b-173">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="2ba2b-175"><a href="dn350577(v=exchg.10).md">Resourcewasreleased</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-175"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="2ba2b-176">Wird von einer Unterklasse aufgerufen, wenn eine Ressource freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-176">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="2ba2b-177">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="2ba2b-177">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="2ba2b-179"><a href="dn351237(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-179"><a href="dn351237(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="2ba2b-180">Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die die aktuelle <a href="dn351163(v=exchg.10).md">Tabelle</a>darstellt.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-180">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351163(v=exchg.10).md">Table</a>.</span></span> <span data-ttu-id="2ba2b-181">(Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="2ba2b-181">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ba2b-182">Oben</span><span class="sxs-lookup"><span data-stu-id="2ba2b-182">Top</span></span>

## <a name="operators"></a><span data-ttu-id="2ba2b-183">Operatoren</span><span class="sxs-lookup"><span data-stu-id="2ba2b-183">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2ba2b-184">Name</span><span class="sxs-lookup"><span data-stu-id="2ba2b-184">Name</span></span></th>
<th><span data-ttu-id="2ba2b-185">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ba2b-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Öffentlicher Operator" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="2ba2b-188"><a href="dn351239(v=exchg.10).md">Implizit (zu JET_TABLEID Tabelle)</a></span><span class="sxs-lookup"><span data-stu-id="2ba2b-188"><a href="dn351239(v=exchg.10).md">Implicit(Table to JET_TABLEID)</a></span></span></td>
<td><span data-ttu-id="2ba2b-189">Impliziter Konvertierungs Operator aus einer Tabelle in einen JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-189">Implicit conversion operator from a Table to a JET_TABLEID.</span></span> <span data-ttu-id="2ba2b-190">Dadurch kann eine Tabelle mit APIs verwendet werden, die eine JET_TABLEID erwarten.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-190">This allows a Table to be used with APIs which expect a JET_TABLEID.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ba2b-191">Oben</span><span class="sxs-lookup"><span data-stu-id="2ba2b-191">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="2ba2b-192">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ba2b-192">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2ba2b-193">Referenz</span><span class="sxs-lookup"><span data-stu-id="2ba2b-193">Reference</span></span>

[<span data-ttu-id="2ba2b-194">Table-Klasse</span><span class="sxs-lookup"><span data-stu-id="2ba2b-194">Table class</span></span>](./table-class.md)

[<span data-ttu-id="2ba2b-195">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="2ba2b-195">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
