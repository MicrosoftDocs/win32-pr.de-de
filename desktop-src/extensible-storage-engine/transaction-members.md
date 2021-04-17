---
description: 'Weitere Informationen finden Sie hier: Transaktions Elemente'
title: 'Transaktionsmember '
TOCTitle: Transaction members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Transaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction_members(v=EXCHG.10)
ms:contentKeyID: 55104159
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4a11aba5d3ffdc8a0e02bd166aa0a433d4860af5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561157"
---
# <a name="transaction-members"></a><span data-ttu-id="9f4d8-103">Transaktionsmember </span><span class="sxs-lookup"><span data-stu-id="9f4d8-103">Transaction members</span></span>

<span data-ttu-id="9f4d8-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="9f4d8-104">Include protected members</span></span>  
<span data-ttu-id="9f4d8-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="9f4d8-105">Include inherited members</span></span>  

<span data-ttu-id="9f4d8-106">Eine Klasse, die eine Transaktion für eine JET_SESID kapselt.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-106">A class that encapsulates a transaction on a JET_SESID.</span></span>

<span data-ttu-id="9f4d8-107">Der [Transaktionstyp](./transaction-class.md) macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-107">The [Transaction](./transaction-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="9f4d8-108">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="9f4d8-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="9f4d8-109">Name</span><span class="sxs-lookup"><span data-stu-id="9f4d8-109">Name</span></span></th>
<th><span data-ttu-id="9f4d8-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f4d8-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9f4d8-112"><a href="dn351177(v=exchg.10).md">Transaktion</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-112"><a href="dn351177(v=exchg.10).md">Transaction</a></span></span></td>
<td><span data-ttu-id="9f4d8-113">Initialisiert eine neue Instanz der Transaction-Klasse.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-113">Initializes a new instance of the Transaction class.</span></span> <span data-ttu-id="9f4d8-114">Dadurch wird automatisch eine Transaktion gestartet.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-114">This automatically begins a transaction.</span></span> <span data-ttu-id="9f4d8-115">Wenn nicht explizit ein Commit für die Transaktion ausgeführt wird, wird ein Rollback ausgeführt</span><span class="sxs-lookup"><span data-stu-id="9f4d8-115">The transaction will be rolled back if not explicitly committed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9f4d8-116">Oben</span><span class="sxs-lookup"><span data-stu-id="9f4d8-116">Top</span></span>

## <a name="properties"></a><span data-ttu-id="9f4d8-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9f4d8-117">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="9f4d8-118">Name</span><span class="sxs-lookup"><span data-stu-id="9f4d8-118">Name</span></span></th>
<th><span data-ttu-id="9f4d8-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f4d8-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Geschützte Eigenschaft" alt="Protected property" /></td>
<td><span data-ttu-id="9f4d8-121"><a href="dn350578(v=exchg.10).md">Hasresource</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-121"><a href="dn350578(v=exchg.10).md">HasResource</a></span></span></td>
<td><span data-ttu-id="9f4d8-122">Ruft einen Wert ab, der angibt, ob die zugrunde liegende Ressource zurzeit zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-122">Gets a value indicating whether the underlying resource is currently allocated.</span></span> <span data-ttu-id="9f4d8-123">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="9f4d8-123">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="9f4d8-125"><a href="dn351180(v=exchg.10).md">IsInTransaction</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-125"><a href="dn351180(v=exchg.10).md">IsInTransaction</a></span></span></td>
<td><span data-ttu-id="9f4d8-126">Ruft einen Wert ab, der angibt, ob dieses-Objekt derzeit in einer Transaktion ist.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-126">Gets a value indicating whether this object is currently in a transaction.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9f4d8-127">Oben</span><span class="sxs-lookup"><span data-stu-id="9f4d8-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="9f4d8-128">Methoden</span><span class="sxs-lookup"><span data-stu-id="9f4d8-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="9f4d8-129">Name</span><span class="sxs-lookup"><span data-stu-id="9f4d8-129">Name</span></span></th>
<th><span data-ttu-id="9f4d8-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f4d8-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9f4d8-132"><a href="dn351172(v=exchg.10).md">Starten</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-132"><a href="dn351172(v=exchg.10).md">Begin</a></span></span></td>
<td><span data-ttu-id="9f4d8-133">Beginnen Sie eine Transaktion.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-133">Begin a transaction.</span></span> <span data-ttu-id="9f4d8-134">Dieses Objekt sollte sich zurzeit nicht in einer Transaktion befinden.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-134">This object should not currently be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="9f4d8-136"><a href="dn350541(v=exchg.10).md">Checkobjectisnotverworfen</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="9f4d8-137">Löst eine Ausnahme aus, wenn dieses Objekt verworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-137">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="9f4d8-138">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="9f4d8-138">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9f4d8-140"><a href="dn351179(v=exchg.10).md">Commit (committransaktiongrbit)</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-140"><a href="dn351179(v=exchg.10).md">Commit(CommitTransactionGrbit)</a></span></span></td>
<td><span data-ttu-id="9f4d8-141">Commit für eine Transaktion durchsetzen.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-141">Commit a transaction.</span></span> <span data-ttu-id="9f4d8-142">Dieses Objekt sollte sich in einer Transaktion befinden.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-142">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9f4d8-144"><a href="dn351243(v=exchg.10).md">Commit (committransaktiongrbit, TimeSpan, JET_COMMIT_ID)</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-144"><a href="dn351243(v=exchg.10).md">Commit(CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span></span></td>
<td><span data-ttu-id="9f4d8-145">Commit für eine Transaktion durchsetzen.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-145">Commit a transaction.</span></span> <span data-ttu-id="9f4d8-146">Dieses Objekt sollte sich in einer Transaktion befinden.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-146">This object should be in a transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9f4d8-148"><a href="dn350553(v=exchg.10).md">Verwerfen ()</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-148"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="9f4d8-149">Löschen Sie dieses Objekt, und veröffentlichen Sie die zugrunde liegende ESENT-Ressource.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-149">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="9f4d8-150">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="9f4d8-150">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="9f4d8-152"><a href="dn350543(v=exchg.10).md">Verwerfen (Boolean)</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-152"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="9f4d8-153">Wird von verwerfen und dem Finalizer aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-153">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="9f4d8-154">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="9f4d8-154">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9f4d8-156"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-156"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="9f4d8-157">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9f4d8-157">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="9f4d8-159"><a href="dn350552(v=exchg.10).md">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-159"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="9f4d8-160">Schließt eine Instanz der esentresource-Klasse ab.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-160">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="9f4d8-161">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="9f4d8-161">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9f4d8-163"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-163"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="9f4d8-164">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9f4d8-164">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9f4d8-166"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-166"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="9f4d8-167">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9f4d8-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="9f4d8-169"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-169"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="9f4d8-170">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="9f4d8-170">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="9f4d8-172"><a href="dn351176(v=exchg.10).md">Releaseresource</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-172"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="9f4d8-173">Wird aufgerufen, wenn die Transaktion entfernt wird, während Sie aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-173">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="9f4d8-174">Dadurch sollte für die Transaktion ein Rollback ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-174">This should rollback the transaction.</span></span> <span data-ttu-id="9f4d8-175">(Überschreibt <a href="dn350545(v=exchg.10).md">esentresource. releaseresource ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="9f4d8-175">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="9f4d8-177"><a href="dn350576(v=exchg.10).md">Resourcewaszugewiesen</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-177"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="9f4d8-178">Wird von einer Unterklasse aufgerufen, wenn eine Ressource zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-178">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="9f4d8-179">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="9f4d8-179">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="9f4d8-181"><a href="dn350577(v=exchg.10).md">Resourcewasreleased</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-181"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="9f4d8-182">Wird von einer Unterklasse aufgerufen, wenn eine Ressource freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-182">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="9f4d8-183">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="9f4d8-183">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9f4d8-185"><a href="dn351244(v=exchg.10).md">Rollback</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-185"><a href="dn351244(v=exchg.10).md">Rollback</a></span></span></td>
<td><span data-ttu-id="9f4d8-186">Rollback einer Transaktion.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-186">Rollback a transaction.</span></span> <span data-ttu-id="9f4d8-187">Dieses Objekt sollte sich in einer Transaktion befinden.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-187">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="9f4d8-189"><a href="dn351181(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="9f4d8-189"><a href="dn351181(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="9f4d8-190">Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die die aktuelle <a href="dn351174(v=exchg.10).md">Transaktion</a>darstellt.</span><span class="sxs-lookup"><span data-stu-id="9f4d8-190">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351174(v=exchg.10).md">Transaction</a>.</span></span> <span data-ttu-id="9f4d8-191">(Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="9f4d8-191">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9f4d8-192">Oben</span><span class="sxs-lookup"><span data-stu-id="9f4d8-192">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="9f4d8-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f4d8-193">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9f4d8-194">Referenz</span><span class="sxs-lookup"><span data-stu-id="9f4d8-194">Reference</span></span>

[<span data-ttu-id="9f4d8-195">Transaktionsklasse</span><span class="sxs-lookup"><span data-stu-id="9f4d8-195">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="9f4d8-196">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="9f4d8-196">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
