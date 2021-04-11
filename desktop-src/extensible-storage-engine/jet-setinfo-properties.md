---
description: 'Weitere Informationen finden Sie hier: JET_SETINFO-Eigenschaften'
title: Eigenschaften von JET_SETINFO
TOCTitle: JET_SETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103917
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af54ddfc09cce0a9c9498dea2060fb83baa0d6f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128648"
---
# <a name="jet_setinfo-properties"></a><span data-ttu-id="fc33e-103">Eigenschaften von JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="fc33e-103">JET_SETINFO properties</span></span>

<span data-ttu-id="fc33e-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="fc33e-104">Include protected members</span></span>  
<span data-ttu-id="fc33e-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="fc33e-105">Include inherited members</span></span>  

<span data-ttu-id="fc33e-106">Der [JET_SETINFO](./jet-setinfo-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fc33e-106">The [JET_SETINFO](./jet-setinfo-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="fc33e-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fc33e-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="fc33e-108">Name</span><span class="sxs-lookup"><span data-stu-id="fc33e-108">Name</span></span></th>
<th><span data-ttu-id="fc33e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc33e-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="fc33e-111"><a href="dn351064(v=exchg.10).md">iblongvalue</a></span><span class="sxs-lookup"><span data-stu-id="fc33e-111"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="fc33e-112">Ruft den Offset bis zum ersten Byte ab, das in einer Spalte vom Typ <a href="hh577895(v=exchg.10).md">LONGBINARY</a> oder <a href="hh577895(v=exchg.10).md">LONGTEXT</a>festgelegt werden soll, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="fc33e-112">Gets or sets offset to the first byte to be set in a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="fc33e-114"><a href="dn351037(v=exchg.10).md">itagsequence</a></span><span class="sxs-lookup"><span data-stu-id="fc33e-114"><a href="dn351037(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="fc33e-115">Ruft die Sequenznummer des Werts in einer mehrwertigen Spalte ab, die festgelegt werden soll, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="fc33e-115">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="fc33e-116">Das Array von Werten ist 1-basiert.</span><span class="sxs-lookup"><span data-stu-id="fc33e-116">The array of values is one-based.</span></span> <span data-ttu-id="fc33e-117">Der erste Wert ist Sequenz 1, nicht 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fc33e-117">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="fc33e-118">Wenn die Daten Satz Spalte nur über einen Wert verfügt, sollte 1 als itagsequence übergeben werden, wenn dieser Wert ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="fc33e-118">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="fc33e-119">Der Wert 0 (null) bedeutet, dass am Ende der Sequenz der Spaltenwerte eine neue Spaltenwert Instanz hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="fc33e-119">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fc33e-120">Oben</span><span class="sxs-lookup"><span data-stu-id="fc33e-120">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="fc33e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc33e-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fc33e-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="fc33e-122">Reference</span></span>

[<span data-ttu-id="fc33e-123">JET_SETINFO-Klasse</span><span class="sxs-lookup"><span data-stu-id="fc33e-123">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="fc33e-124">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="fc33e-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
