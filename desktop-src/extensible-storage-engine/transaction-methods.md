---
description: 'Weitere Informationen finden Sie hier: Transaction-Methoden'
title: 'Transaktionsmethoden '
TOCTitle: Transaction methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Transaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction_methods(v=EXCHG.10)
ms:contentKeyID: 55104163
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c926d00f785aab3a63cd8ebc7eebaf74ea5f0e23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104552736"
---
# <a name="transaction-methods"></a><span data-ttu-id="bfa89-103">Transaktionsmethoden </span><span class="sxs-lookup"><span data-stu-id="bfa89-103">Transaction methods</span></span>

<span data-ttu-id="bfa89-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="bfa89-104">Include protected members</span></span>  
<span data-ttu-id="bfa89-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="bfa89-105">Include inherited members</span></span>  

<span data-ttu-id="bfa89-106">Der [Transaktionstyp](./transaction-class.md) macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bfa89-106">The [Transaction](./transaction-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="bfa89-107">Methoden</span><span class="sxs-lookup"><span data-stu-id="bfa89-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="bfa89-108">Name</span><span class="sxs-lookup"><span data-stu-id="bfa89-108">Name</span></span></th>
<th><span data-ttu-id="bfa89-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bfa89-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="bfa89-111"><a href="dn351172(v=exchg.10).md">Starten</a></span><span class="sxs-lookup"><span data-stu-id="bfa89-111"><a href="dn351172(v=exchg.10).md">Begin</a></span></span></td>
<td><span data-ttu-id="bfa89-112">Beginnen Sie eine Transaktion.</span><span class="sxs-lookup"><span data-stu-id="bfa89-112">Begin a transaction.</span></span> <span data-ttu-id="bfa89-113">Dieses Objekt sollte sich zurzeit nicht in einer Transaktion befinden.</span><span class="sxs-lookup"><span data-stu-id="bfa89-113">This object should not currently be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="bfa89-115"><a href="dn350541(v=exchg.10).md">Checkobjectisnotverworfen</a></span><span class="sxs-lookup"><span data-stu-id="bfa89-115"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="bfa89-116">Löst eine Ausnahme aus, wenn dieses Objekt verworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="bfa89-116">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="bfa89-117">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="bfa89-117">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="bfa89-119"><a href="dn351179(v=exchg.10).md">Commit (committransaktiongrbit)</a></span><span class="sxs-lookup"><span data-stu-id="bfa89-119"><a href="dn351179(v=exchg.10).md">Commit(CommitTransactionGrbit)</a></span></span></td>
<td><span data-ttu-id="bfa89-120">Commit für eine Transaktion durchsetzen.</span><span class="sxs-lookup"><span data-stu-id="bfa89-120">Commit a transaction.</span></span> <span data-ttu-id="bfa89-121">Dieses Objekt sollte sich in einer Transaktion befinden.</span><span class="sxs-lookup"><span data-stu-id="bfa89-121">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="bfa89-123"><a href="dn351243(v=exchg.10).md">Commit (committransaktiongrbit, TimeSpan, JET_COMMIT_ID)</a></span><span class="sxs-lookup"><span data-stu-id="bfa89-123"><a href="dn351243(v=exchg.10).md">Commit(CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span></span></td>
<td><span data-ttu-id="bfa89-124">Commit für eine Transaktion durchsetzen.</span><span class="sxs-lookup"><span data-stu-id="bfa89-124">Commit a transaction.</span></span> <span data-ttu-id="bfa89-125">Dieses Objekt sollte sich in einer Transaktion befinden.</span><span class="sxs-lookup"><span data-stu-id="bfa89-125">This object should be in a transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="bfa89-127"><a href="dn350553(v=exchg.10).md">Verwerfen ()</a></span><span class="sxs-lookup"><span data-stu-id="bfa89-127"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="bfa89-128">Löschen Sie dieses Objekt, und veröffentlichen Sie die zugrunde liegende ESENT-Ressource.</span><span class="sxs-lookup"><span data-stu-id="bfa89-128">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="bfa89-129">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="bfa89-129">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="bfa89-131"><a href="dn350543(v=exchg.10).md">Verwerfen (Boolean)</a></span><span class="sxs-lookup"><span data-stu-id="bfa89-131"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="bfa89-132">Wird von verwerfen und dem Finalizer aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="bfa89-132">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="bfa89-133">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="bfa89-133">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="bfa89-135"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></span><span class="sxs-lookup"><span data-stu-id="bfa89-135"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="bfa89-136">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="bfa89-136">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="bfa89-138"><a href="dn350552(v=exchg.10).md">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="bfa89-138"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="bfa89-139">Schließt eine Instanz der esentresource-Klasse ab.</span><span class="sxs-lookup"><span data-stu-id="bfa89-139">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="bfa89-140">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="bfa89-140">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="bfa89-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="bfa89-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="bfa89-143">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="bfa89-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="bfa89-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="bfa89-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="bfa89-146">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="bfa89-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="bfa89-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></span><span class="sxs-lookup"><span data-stu-id="bfa89-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="bfa89-149">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="bfa89-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="bfa89-151"><a href="dn351176(v=exchg.10).md">Releaseresource</a></span><span class="sxs-lookup"><span data-stu-id="bfa89-151"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="bfa89-152">Wird aufgerufen, wenn die Transaktion entfernt wird, während Sie aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="bfa89-152">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="bfa89-153">Dadurch sollte für die Transaktion ein Rollback ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bfa89-153">This should rollback the transaction.</span></span> <span data-ttu-id="bfa89-154">(Überschreibt <a href="dn350545(v=exchg.10).md">esentresource. releaseresource ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="bfa89-154">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="bfa89-156"><a href="dn350576(v=exchg.10).md">Resourcewaszugewiesen</a></span><span class="sxs-lookup"><span data-stu-id="bfa89-156"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="bfa89-157">Wird von einer Unterklasse aufgerufen, wenn eine Ressource zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="bfa89-157">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="bfa89-158">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="bfa89-158">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="bfa89-160"><a href="dn350577(v=exchg.10).md">Resourcewasreleased</a></span><span class="sxs-lookup"><span data-stu-id="bfa89-160"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="bfa89-161">Wird von einer Unterklasse aufgerufen, wenn eine Ressource freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bfa89-161">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="bfa89-162">(Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</span><span class="sxs-lookup"><span data-stu-id="bfa89-162">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="bfa89-164"><a href="dn351244(v=exchg.10).md">Rollback</a></span><span class="sxs-lookup"><span data-stu-id="bfa89-164"><a href="dn351244(v=exchg.10).md">Rollback</a></span></span></td>
<td><span data-ttu-id="bfa89-165">Rollback einer Transaktion.</span><span class="sxs-lookup"><span data-stu-id="bfa89-165">Rollback a transaction.</span></span> <span data-ttu-id="bfa89-166">Dieses Objekt sollte sich in einer Transaktion befinden.</span><span class="sxs-lookup"><span data-stu-id="bfa89-166">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="bfa89-168"><a href="dn351181(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="bfa89-168"><a href="dn351181(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="bfa89-169">Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die die aktuelle <a href="dn351174(v=exchg.10).md">Transaktion</a>darstellt.</span><span class="sxs-lookup"><span data-stu-id="bfa89-169">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351174(v=exchg.10).md">Transaction</a>.</span></span> <span data-ttu-id="bfa89-170">(Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="bfa89-170">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bfa89-171">Oben</span><span class="sxs-lookup"><span data-stu-id="bfa89-171">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="bfa89-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfa89-172">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bfa89-173">Referenz</span><span class="sxs-lookup"><span data-stu-id="bfa89-173">Reference</span></span>

[<span data-ttu-id="bfa89-174">Transaktionsklasse</span><span class="sxs-lookup"><span data-stu-id="bfa89-174">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="bfa89-175">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="bfa89-175">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
