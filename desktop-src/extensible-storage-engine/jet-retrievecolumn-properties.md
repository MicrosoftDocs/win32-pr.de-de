---
description: 'Weitere Informationen finden Sie hier: JET_RETRIEVECOLUMN-Eigenschaften'
title: Eigenschaften von JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103808
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2a42337e361fc7cbef60db70662ab7388c678903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758508"
---
# <a name="jet_retrievecolumn-properties"></a><span data-ttu-id="f443c-103">Eigenschaften von JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="f443c-103">JET_RETRIEVECOLUMN properties</span></span>

<span data-ttu-id="f443c-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="f443c-104">Include protected members</span></span>  
<span data-ttu-id="f443c-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="f443c-105">Include inherited members</span></span>  

<span data-ttu-id="f443c-106">Der [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f443c-106">The [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="f443c-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f443c-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="f443c-108">Name</span><span class="sxs-lookup"><span data-stu-id="f443c-108">Name</span></span></th>
<th><span data-ttu-id="f443c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f443c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="f443c-111"><a href="dn335226(v=exchg.10).md">cbactual</a></span><span class="sxs-lookup"><span data-stu-id="f443c-111"><a href="dn335226(v=exchg.10).md">cbActual</a></span></span></td>
<td><span data-ttu-id="f443c-112">Ruft die Größe der Daten in Bytes ab, die durch einen Vorgang zum Abrufen einer Spalte abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f443c-112">Gets the size, in bytes, of data that is retrieved by a retrieve column operation.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="f443c-114"><a href="dn335228(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="f443c-114"><a href="dn335228(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="f443c-115">Ruft die Größe des <a href="dn351040(v=exchg.10).md">pvData</a> -Puffers in Bytes ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f443c-115">Gets or sets the size of the <a href="dn351040(v=exchg.10).md">pvData</a> buffer, in bytes.</span></span> <span data-ttu-id="f443c-116">Der Vorgang zum Abrufen von Spalten speichert keine weiteren Daten in pvData als cbData.</span><span class="sxs-lookup"><span data-stu-id="f443c-116">The retrieve column operation will not store more data in pvData than cbData.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="f443c-118"><a href="dn335230(v=exchg.10).md">ColumnID</a></span><span class="sxs-lookup"><span data-stu-id="f443c-118"><a href="dn335230(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="f443c-119">Ruft den Spalten Bezeichner für die abzurufende Spalte ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="f443c-119">Gets or sets the column identifier for the column to retrieve.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="f443c-121"><a href="dn335229(v=exchg.10).md">columnidnexttaging</a></span><span class="sxs-lookup"><span data-stu-id="f443c-121"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="f443c-122">Ruft das ColumnID der markierten Spalte mit mehreren Werten oder einer sparsespalte ab, wenn alle markierten Spalten abgerufen werden, indem 0 als ColumnID übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f443c-122">Gets the columnid of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the columnid.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="f443c-124"><a href="dn335231(v=exchg.10).md">irre</a></span><span class="sxs-lookup"><span data-stu-id="f443c-124"><a href="dn335231(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="f443c-125">Ruft die vom Abruf der Spalte zurückgegebene Warnung ab.</span><span class="sxs-lookup"><span data-stu-id="f443c-125">Gets the warning returned from the retrieval of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="f443c-127"><a href="dn335232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="f443c-127"><a href="dn335232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="f443c-128">Ruft die Optionen zum Abrufen von Spalten ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="f443c-128">Gets or sets the options for column retrieval.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="f443c-130"><a href="dn335233(v=exchg.10).md">ibdata</a></span><span class="sxs-lookup"><span data-stu-id="f443c-130"><a href="dn335233(v=exchg.10).md">ibData</a></span></span></td>
<td><span data-ttu-id="f443c-131">Ruft den Offset im Puffer ab, in dem Daten gespeichert werden, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="f443c-131">Gets or sets the offset in the buffer that data will be stored in.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="f443c-133"><a href="dn335234(v=exchg.10).md">iblongvalue</a></span><span class="sxs-lookup"><span data-stu-id="f443c-133"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="f443c-134">Ruft den Offset zum ersten Byte ab, das aus einer Spalte vom Typ <a href="hh577895(v=exchg.10).md">LONGBINARY</a> oder <a href="hh577895(v=exchg.10).md">LONGTEXT</a>abgerufen werden soll, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="f443c-134">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="f443c-136"><a href="dn351039(v=exchg.10).md">itagsequence</a></span><span class="sxs-lookup"><span data-stu-id="f443c-136"><a href="dn351039(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="f443c-137">Ruft die Sequenznummer der in einer mehrwertigen Spalte enthaltenen Werte ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="f443c-137">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="f443c-138">Wenn itagsequence den Wert 0 hat, wird anstelle von Spaltendaten die Anzahl der Instanzen einer mehrwertigen Spalte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f443c-138">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="f443c-140"><a href="dn351040(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="f443c-140"><a href="dn351040(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="f443c-141">Ruft den Puffer ab, in dem Daten gespeichert werden, die aus der Spalte abgerufen werden, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="f443c-141">Gets or sets the buffer that will store data that is retrieved from the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f443c-142">Oben</span><span class="sxs-lookup"><span data-stu-id="f443c-142">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="f443c-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f443c-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f443c-144">Referenz</span><span class="sxs-lookup"><span data-stu-id="f443c-144">Reference</span></span>

[<span data-ttu-id="f443c-145">JET_RETRIEVECOLUMN-Klasse</span><span class="sxs-lookup"><span data-stu-id="f443c-145">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="f443c-146">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f443c-146">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
