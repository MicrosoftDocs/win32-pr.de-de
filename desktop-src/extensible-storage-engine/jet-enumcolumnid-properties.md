---
description: 'Weitere Informationen finden Sie hier: JET_ENUMCOLUMNID-Eigenschaften'
title: Eigenschaften von JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_properties(v=EXCHG.10)
ms:contentKeyID: 55103627
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1e45574d7cabd937d6b2d7351a917ac62340f355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525028"
---
# <a name="jet_enumcolumnid-properties"></a><span data-ttu-id="5e933-103">Eigenschaften von JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="5e933-103">JET_ENUMCOLUMNID properties</span></span>

<span data-ttu-id="5e933-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="5e933-104">Include protected members</span></span>  
<span data-ttu-id="5e933-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="5e933-105">Include inherited members</span></span>  

<span data-ttu-id="5e933-106">Der [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5e933-106">The [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="5e933-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e933-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="5e933-108">Name</span><span class="sxs-lookup"><span data-stu-id="5e933-108">Name</span></span></th>
<th><span data-ttu-id="5e933-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e933-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="5e933-111"><a href="dn335141(v=exchg.10).md">ColumnID</a></span><span class="sxs-lookup"><span data-stu-id="5e933-111"><a href="dn335141(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="5e933-112">Ruft die aufzuzählenden Spalten-ID ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="5e933-112">Gets or sets the columnid ID to enumerate.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="5e933-114"><a href="dn335092(v=exchg.10).md">ctagsequence</a></span><span class="sxs-lookup"><span data-stu-id="5e933-114"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span></span></td>
<td><span data-ttu-id="5e933-115">Ruft die Anzahl der Spaltenwerte (durch einen einbasierten Index) ab, die für die angegebene Spalten-ID aufgelistet werden sollen, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="5e933-115">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="5e933-116">Wenn ctagsequence gleich 0 (null) ist, wird rgtagsequence ignoriert, und alle Spaltenwerte für die angegebene Spalten-ID werden aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5e933-116">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="5e933-118"><a href="dn335093(v=exchg.10).md">rgtagsequence</a></span><span class="sxs-lookup"><span data-stu-id="5e933-118"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span></span></td>
<td><span data-ttu-id="5e933-119">Ruft das Array von einbasierten Indizes in das Array von Spaltenwerten für eine angegebene Spalte ab oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="5e933-119">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="5e933-120">Bei einem einzelnen Element handelt es sich um eine in JET_RETRIEVECOLUMN definierte itagsequence.</span><span class="sxs-lookup"><span data-stu-id="5e933-120">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="5e933-121">Eine itagsequence-Wert von 0 (null) bedeutet &quot; Skip &quot; .</span><span class="sxs-lookup"><span data-stu-id="5e933-121">An itagSequence of 0 (zero) means &quot;skip&quot;.</span></span> <span data-ttu-id="5e933-122">Eine itagsequence von 1 bedeutet, dass der erste Spaltenwert der Spalte zurückgegeben wird, der Wert 2 für den zweiten Wert usw.</span><span class="sxs-lookup"><span data-stu-id="5e933-122">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5e933-123">Oben</span><span class="sxs-lookup"><span data-stu-id="5e933-123">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="5e933-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e933-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5e933-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="5e933-125">Reference</span></span>

[<span data-ttu-id="5e933-126">JET_ENUMCOLUMNID-Klasse</span><span class="sxs-lookup"><span data-stu-id="5e933-126">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="5e933-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="5e933-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
