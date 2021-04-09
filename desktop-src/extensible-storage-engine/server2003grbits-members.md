---
description: 'Weitere Informationen finden Sie hier: Server2003Grbits Members'
title: Server2003Grbits-Member (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: Server2003Grbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_members(v=EXCHG.10)
ms:contentKeyID: 55107767
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 21008153606a6c35c76daf3c2758211f3fcdd42e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865612"
---
# <a name="server2003grbits-members"></a><span data-ttu-id="0e96a-103">Server2003Grbits-Member</span><span class="sxs-lookup"><span data-stu-id="0e96a-103">Server2003Grbits members</span></span>

<span data-ttu-id="0e96a-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="0e96a-104">Include protected members</span></span>  
<span data-ttu-id="0e96a-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="0e96a-105">Include inherited members</span></span>  

<span data-ttu-id="0e96a-106">Grbits, die der Windows Server 2003-Version von ESENT hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="0e96a-106">Grbits that have been added to the Windows Server 2003 version of ESENT.</span></span>

<span data-ttu-id="0e96a-107">Der [Server2003Grbits](./server2003grbits-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e96a-107">The [Server2003Grbits](./server2003grbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="0e96a-108">Felder</span><span class="sxs-lookup"><span data-stu-id="0e96a-108">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="0e96a-109">Name</span><span class="sxs-lookup"><span data-stu-id="0e96a-109">Name</span></span></th>
<th><span data-ttu-id="0e96a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e96a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="0e96a-113"><a href="dn351203(v=exchg.10).md">Enumerateignoreuserdefineddefault</a></span><span class="sxs-lookup"><span data-stu-id="0e96a-113"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span></span></td>
<td><span data-ttu-id="0e96a-114">Wenn eine bestimmte Spalte nicht im Datensatz vorhanden ist und über einen benutzerdefinierten Standardwert verfügt, wird kein Spaltenwert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0e96a-114">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="0e96a-115">Mit dieser Option wird verhindert, dass der Rückruf, der den benutzerdefinierten Standardwert für die Spalte berechnet, beim Auflisten der Werte für diese Spalte aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0e96a-115">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="0e96a-118"><a href="dn351284(v=exchg.10).md">Nur Weiterleitung</a></span><span class="sxs-lookup"><span data-stu-id="0e96a-118"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span></span></td>
<td><span data-ttu-id="0e96a-119">Mit dieser Option wird angefordert, dass die temporäre Tabelle nur erstellt wird, wenn der temporäre Tabellen-Manager die für zwischen Abfrageergebnisse optimierte-Implementierung verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="0e96a-119">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="0e96a-120">Wenn ein beliebiges Merkmal der temporären Tabelle die Verwendung dieser Optimierung verhindern würde, schlägt der Vorgang mit JET_errCannotMaterializeForwardOnlySort fehl.</span><span class="sxs-lookup"><span data-stu-id="0e96a-120">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span> <span data-ttu-id="0e96a-121">Ein Nebeneffekt dieser Option besteht darin, zuzulassen, dass die temporäre Tabelle Datensätze mit doppelten Index Schlüsseln enthält.</span><span class="sxs-lookup"><span data-stu-id="0e96a-121">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="0e96a-122">Weitere Informationen finden Sie unter <a href="hh558517(v=exchg.10).md">Unique</a> .</span><span class="sxs-lookup"><span data-stu-id="0e96a-122">See <a href="hh558517(v=exchg.10).md">Unique</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="0e96a-125"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span><span class="sxs-lookup"><span data-stu-id="0e96a-125"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span></span></td>
<td><span data-ttu-id="0e96a-126">Alle Transaktionen, für die zuvor von einer Sitzung ein Commit ausgeführt wurde und die noch nicht in die Transaktionsprotokoll Datei geleert wurden, werden sofort geleert.</span><span class="sxs-lookup"><span data-stu-id="0e96a-126">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="0e96a-127">Diese API wartet, bis die Transaktionen geleert wurden, bevor Sie an den Aufrufer zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0e96a-127">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="0e96a-128">Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</span><span class="sxs-lookup"><span data-stu-id="0e96a-128">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="0e96a-129">Diese Option kann nicht in Kombination mit anderen Optionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0e96a-129">This option cannot be used in combination with any other option.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0e96a-130">Oben</span><span class="sxs-lookup"><span data-stu-id="0e96a-130">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="0e96a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e96a-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0e96a-132">Referenz</span><span class="sxs-lookup"><span data-stu-id="0e96a-132">Reference</span></span>

[<span data-ttu-id="0e96a-133">Server2003Grbits-Klasse</span><span class="sxs-lookup"><span data-stu-id="0e96a-133">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="0e96a-134">Microsoft. ISAM. ESENT. Interop. Server2003-Namespace</span><span class="sxs-lookup"><span data-stu-id="0e96a-134">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
