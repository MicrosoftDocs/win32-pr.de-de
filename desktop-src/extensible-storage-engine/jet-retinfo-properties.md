---
description: 'Weitere Informationen finden Sie hier: JET_RETINFO-Eigenschaften'
title: Eigenschaften von JET_RETINFO
TOCTitle: JET_RETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103867
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4724651b0184bae0b4acca049a8a16653282ce85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564798"
---
# <a name="jet_retinfo-properties"></a><span data-ttu-id="58a32-103">Eigenschaften von JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="58a32-103">JET_RETINFO properties</span></span>

<span data-ttu-id="58a32-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="58a32-104">Include protected members</span></span>  
<span data-ttu-id="58a32-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="58a32-105">Include inherited members</span></span>  

<span data-ttu-id="58a32-106">Der [JET_RETINFO](./jet-retinfo-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="58a32-106">The [JET_RETINFO](./jet-retinfo-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="58a32-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58a32-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="58a32-108">Name</span><span class="sxs-lookup"><span data-stu-id="58a32-108">Name</span></span></th>
<th><span data-ttu-id="58a32-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58a32-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="58a32-111"><a href="dn335221(v=exchg.10).md">columnidnexttaging</a></span><span class="sxs-lookup"><span data-stu-id="58a32-111"><a href="dn335221(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="58a32-112">Ruft das ColumnID der abgerufenen Spalte mit mehreren Werten oder geringer Dichte ab, wenn alle markierten Spalten abgerufen werden, indem 0 als ColumnID an jetretrievecolbin übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="58a32-112">Gets the columnid of the retrieved tagged, multi-valued or sparse, column when all tagged columns are retrieved by passing 0 as the columnid to JetRetrieveColumn.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="58a32-114"><a href="dn335220(v=exchg.10).md">iblongvalue</a></span><span class="sxs-lookup"><span data-stu-id="58a32-114"><a href="dn335220(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="58a32-115">Ruft den Offset auf das erste Byte ab, das aus einer Spalte vom Typ <a href="hh577895(v=exchg.10).md">LONGBINARY</a>oder <a href="hh577895(v=exchg.10).md">LONGTEXT</a>abgerufen werden soll, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="58a32-115">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a>, or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="58a32-117"><a href="dn351035(v=exchg.10).md">itagsequence</a></span><span class="sxs-lookup"><span data-stu-id="58a32-117"><a href="dn351035(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="58a32-118">Ruft die Sequenznummer des Werts in einer mehrwertigen Spalte ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="58a32-118">Gets or sets the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="58a32-119">Das Array von Werten ist 1-basiert.</span><span class="sxs-lookup"><span data-stu-id="58a32-119">The array of values is one-based.</span></span> <span data-ttu-id="58a32-120">Der erste Wert ist Sequenz 1, nicht 0.</span><span class="sxs-lookup"><span data-stu-id="58a32-120">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="58a32-121">Wenn die Daten Satz Spalte nur über einen Wert verfügt, sollte 1 als itagsequence übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="58a32-121">If the record column has only one value then 1 should be passed as the itagSequence.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="58a32-122">Oben</span><span class="sxs-lookup"><span data-stu-id="58a32-122">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="58a32-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58a32-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="58a32-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="58a32-124">Reference</span></span>

[<span data-ttu-id="58a32-125">JET_RETINFO-Klasse</span><span class="sxs-lookup"><span data-stu-id="58a32-125">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="58a32-126">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="58a32-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
