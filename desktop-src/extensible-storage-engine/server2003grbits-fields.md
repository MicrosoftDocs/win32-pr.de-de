---
description: 'Weitere Informationen finden Sie hier: Server2003Grbits Fields'
title: Server2003Grbits-Felder (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: Server2003Grbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104210
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: ed7a99118674d955fc6a882ac08407e45837af77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571005"
---
# <a name="server2003grbits-fields"></a><span data-ttu-id="fc3c4-103">Server2003Grbits-Felder</span><span class="sxs-lookup"><span data-stu-id="fc3c4-103">Server2003Grbits fields</span></span>

<span data-ttu-id="fc3c4-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="fc3c4-104">Include protected members</span></span>  
<span data-ttu-id="fc3c4-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="fc3c4-105">Include inherited members</span></span>  

<span data-ttu-id="fc3c4-106">Der [Server2003Grbits](./server2003grbits-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fc3c4-106">The [Server2003Grbits](./server2003grbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="fc3c4-107">Felder</span><span class="sxs-lookup"><span data-stu-id="fc3c4-107">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="fc3c4-108">Name</span><span class="sxs-lookup"><span data-stu-id="fc3c4-108">Name</span></span></th>
<th><span data-ttu-id="fc3c4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc3c4-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="fc3c4-112"><a href="dn351203(v=exchg.10).md">Enumerateignoreuserdefineddefault</a></span><span class="sxs-lookup"><span data-stu-id="fc3c4-112"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span></span></td>
<td><span data-ttu-id="fc3c4-113">Wenn eine bestimmte Spalte nicht im Datensatz vorhanden ist und über einen benutzerdefinierten Standardwert verfügt, wird kein Spaltenwert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fc3c4-113">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="fc3c4-114">Mit dieser Option wird verhindert, dass der Rückruf, der den benutzerdefinierten Standardwert für die Spalte berechnet, beim Auflisten der Werte für diese Spalte aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fc3c4-114">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="fc3c4-117"><a href="dn351284(v=exchg.10).md">Nur Weiterleitung</a></span><span class="sxs-lookup"><span data-stu-id="fc3c4-117"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span></span></td>
<td><span data-ttu-id="fc3c4-118">Mit dieser Option wird angefordert, dass die temporäre Tabelle nur erstellt wird, wenn der temporäre Tabellen-Manager die für zwischen Abfrageergebnisse optimierte-Implementierung verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="fc3c4-118">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="fc3c4-119">Wenn ein beliebiges Merkmal der temporären Tabelle die Verwendung dieser Optimierung verhindern würde, schlägt der Vorgang mit JET_errCannotMaterializeForwardOnlySort fehl.</span><span class="sxs-lookup"><span data-stu-id="fc3c4-119">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span> <span data-ttu-id="fc3c4-120">Ein Nebeneffekt dieser Option besteht darin, zuzulassen, dass die temporäre Tabelle Datensätze mit doppelten Index Schlüsseln enthält.</span><span class="sxs-lookup"><span data-stu-id="fc3c4-120">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="fc3c4-121">Weitere Informationen finden Sie unter <a href="hh558517(v=exchg.10).md">Unique</a> .</span><span class="sxs-lookup"><span data-stu-id="fc3c4-121">See <a href="hh558517(v=exchg.10).md">Unique</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="fc3c4-124"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span><span class="sxs-lookup"><span data-stu-id="fc3c4-124"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span></span></td>
<td><span data-ttu-id="fc3c4-125">Alle Transaktionen, für die zuvor von einer Sitzung ein Commit ausgeführt wurde und die noch nicht in die Transaktionsprotokoll Datei geleert wurden, werden sofort geleert.</span><span class="sxs-lookup"><span data-stu-id="fc3c4-125">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="fc3c4-126">Diese API wartet, bis die Transaktionen geleert wurden, bevor Sie an den Aufrufer zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fc3c4-126">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="fc3c4-127">Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</span><span class="sxs-lookup"><span data-stu-id="fc3c4-127">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="fc3c4-128">Diese Option kann nicht in Kombination mit anderen Optionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc3c4-128">This option cannot be used in combination with any other option.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fc3c4-129">Oben</span><span class="sxs-lookup"><span data-stu-id="fc3c4-129">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="fc3c4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc3c4-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fc3c4-131">Referenz</span><span class="sxs-lookup"><span data-stu-id="fc3c4-131">Reference</span></span>

[<span data-ttu-id="fc3c4-132">Server2003Grbits-Klasse</span><span class="sxs-lookup"><span data-stu-id="fc3c4-132">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="fc3c4-133">Microsoft. ISAM. ESENT. Interop. Server2003-Namespace</span><span class="sxs-lookup"><span data-stu-id="fc3c4-133">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
