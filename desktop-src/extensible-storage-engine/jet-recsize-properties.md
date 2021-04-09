---
description: 'Weitere Informationen finden Sie hier: JET_RECSIZE-Eigenschaften'
title: JET_RECSIZE Eigenschaften (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: JET_RECSIZE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_properties(v=EXCHG.10)
ms:contentKeyID: 39513545
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4733e1d666bdf3f938c91f437c1764811fb10f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868944"
---
# <a name="jet_recsize-properties"></a><span data-ttu-id="3bb7b-103">Eigenschaften von JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="3bb7b-103">JET_RECSIZE properties</span></span>

<span data-ttu-id="3bb7b-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="3bb7b-104">Include protected members</span></span>  
<span data-ttu-id="3bb7b-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="3bb7b-105">Include inherited members</span></span>  

<span data-ttu-id="3bb7b-106">Der [JET_RECSIZE](./jet-recsize-structure2.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3bb7b-106">The [JET_RECSIZE](./jet-recsize-structure2.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="3bb7b-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3bb7b-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3bb7b-108">Name</span><span class="sxs-lookup"><span data-stu-id="3bb7b-108">Name</span></span></th>
<th><span data-ttu-id="3bb7b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3bb7b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="3bb7b-111"><a href="hh557581(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="3bb7b-111"><a href="hh557581(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="3bb7b-112">Ruft das Benutzer DataSet im Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="3bb7b-112">Gets the user data set in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="3bb7b-114"><a href="hh596280(v=exchg.10).md">cbdatacompressed</a></span><span class="sxs-lookup"><span data-stu-id="3bb7b-114"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span></span></td>
<td><span data-ttu-id="3bb7b-115">Ruft die komprimierte Größe der Benutzerdaten im Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="3bb7b-115">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="3bb7b-116">Dies ist das gleiche wie bei <a href="hh557581(v=exchg.10).md">cbData</a> , wenn keine systeminternen langen Werte komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="3bb7b-116">This is the same as <a href="hh557581(v=exchg.10).md">cbData</a> if no intrinsic long-values are compressed).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="3bb7b-118"><a href="hh557913(v=exchg.10).md">cblongvaluedata</a></span><span class="sxs-lookup"><span data-stu-id="3bb7b-118"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span></span></td>
<td><span data-ttu-id="3bb7b-119">Ruft das Benutzer DataSet im Datensatz ab, wird jedoch in der Struktur mit langem Wert gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3bb7b-119">Gets the user data set in the record, but stored in the long-value tree.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="3bb7b-121"><a href="hh566144(v=exchg.10).md">cblongvaluedatacompressed</a></span><span class="sxs-lookup"><span data-stu-id="3bb7b-121"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span></span></td>
<td><span data-ttu-id="3bb7b-122">Ruft die komprimierte Größe von Benutzerdaten in der Struktur mit langem Wert ab.</span><span class="sxs-lookup"><span data-stu-id="3bb7b-122">Gets the compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="3bb7b-123">Dies entspricht <a href="hh557913(v=exchg.10).md">cblongvaluedata</a> , wenn keine getrennten langen Werte komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="3bb7b-123">This is the same as <a href="hh557913(v=exchg.10).md">cbLongValueData</a> if no separated long values are compressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="3bb7b-125"><a href="hh558003(v=exchg.10).md">cblongvalueoverhead</a></span><span class="sxs-lookup"><span data-stu-id="3bb7b-125"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span></span></td>
<td><span data-ttu-id="3bb7b-126">Ruft den mehr Aufwand für die Daten des langen Werts ab.</span><span class="sxs-lookup"><span data-stu-id="3bb7b-126">Gets the overhead of the long-value data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="3bb7b-128"><a href="hh565836(v=exchg.10).md">cboverhead</a></span><span class="sxs-lookup"><span data-stu-id="3bb7b-128"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span></span></td>
<td><span data-ttu-id="3bb7b-129">Ruft den Aufwand der ESENT-Daten Satzstruktur für diesen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="3bb7b-129">Gets the overhead of the ESENT record structure for this record.</span></span> <span data-ttu-id="3bb7b-130">Dazu gehört auch die Schlüsselgröße des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="3bb7b-130">This includes the record's key size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="3bb7b-132"><a href="hh566154(v=exchg.10).md">ccompressedcolumns</a></span><span class="sxs-lookup"><span data-stu-id="3bb7b-132"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span></span></td>
<td><span data-ttu-id="3bb7b-133">Ruft die Gesamtzahl der Spalten im Datensatz ab, die komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="3bb7b-133">Gets the total number of columns in the record which are compressed.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="3bb7b-135"><a href="hh596288(v=exchg.10).md">clongvalues</a></span><span class="sxs-lookup"><span data-stu-id="3bb7b-135"><a href="hh596288(v=exchg.10).md">cLongValues</a></span></span></td>
<td><span data-ttu-id="3bb7b-136">Ruft die Gesamtzahl der Long-Werte ab, die in der Struktur mit dem langen Wert für diesen Datensatz gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="3bb7b-136">Gets the total number of long values stored in the long-value tree for this record.</span></span> <span data-ttu-id="3bb7b-137">Dies schließt keine systeminternen Long-Werte ein.</span><span class="sxs-lookup"><span data-stu-id="3bb7b-137">This does not include intrinsic long values.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="3bb7b-139"><a href="hh577486(v=exchg.10).md">cmultivalues</a></span><span class="sxs-lookup"><span data-stu-id="3bb7b-139"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span></span></td>
<td><span data-ttu-id="3bb7b-140">Ruft die Ansammlung der Gesamtzahl der Werte über den ersten für alle Spalten im Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="3bb7b-140">Gets the accumulation of the total number of values beyond the first for all columns in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="3bb7b-142"><a href="hh578172(v=exchg.10).md">cnontaggedcolumns</a></span><span class="sxs-lookup"><span data-stu-id="3bb7b-142"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span></span></td>
<td><span data-ttu-id="3bb7b-143">Ruft die Gesamtanzahl fester und variabler Spalten ab, die in diesem Datensatz festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="3bb7b-143">Gets the total number of fixed and variable columns set in this record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="3bb7b-145"><a href="hh566034(v=exchg.10).md">ctaggedcolumns</a></span><span class="sxs-lookup"><span data-stu-id="3bb7b-145"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span></span></td>
<td><span data-ttu-id="3bb7b-146">Ruft die Gesamtzahl der markierten Spalten ab, die in diesem Datensatz festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="3bb7b-146">Gets the total number of tagged columns set in this record.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3bb7b-147">Oben</span><span class="sxs-lookup"><span data-stu-id="3bb7b-147">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="3bb7b-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bb7b-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3bb7b-149">Referenz</span><span class="sxs-lookup"><span data-stu-id="3bb7b-149">Reference</span></span>

[<span data-ttu-id="3bb7b-150">JET_RECSIZE Struktur</span><span class="sxs-lookup"><span data-stu-id="3bb7b-150">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="3bb7b-151">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="3bb7b-151">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
