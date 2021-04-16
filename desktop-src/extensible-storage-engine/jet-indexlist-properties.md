---
description: 'Weitere Informationen finden Sie hier: JET_INDEXLIST-Eigenschaften'
title: Eigenschaften von JET_INDEXLIST
TOCTitle: JET_INDEXLIST properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_properties(v=EXCHG.10)
ms:contentKeyID: 55103599
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 7a1f500f5d51c0487ea490d2051bfc5e4639afbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558697"
---
# <a name="jet_indexlist-properties"></a><span data-ttu-id="a0745-103">Eigenschaften von JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="a0745-103">JET_INDEXLIST properties</span></span>

<span data-ttu-id="a0745-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="a0745-104">Include protected members</span></span>  
<span data-ttu-id="a0745-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="a0745-105">Include inherited members</span></span>  

<span data-ttu-id="a0745-106">Der [JET_INDEXLIST](./jet-indexlist-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a0745-106">The [JET_INDEXLIST](./jet-indexlist-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="a0745-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a0745-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a0745-108">Name</span><span class="sxs-lookup"><span data-stu-id="a0745-108">Name</span></span></th>
<th><span data-ttu-id="a0745-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0745-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="a0745-111"><a href="dn335125(v=exchg.10).md">columnidccolumn</a></span><span class="sxs-lookup"><span data-stu-id="a0745-111"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span></span></td>
<td><span data-ttu-id="a0745-112">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Anzahl der Spalten im Index Schlüssel gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a0745-112">Gets the columnid of the column in the temporary table which stores the number of columns in the index key.</span></span> <span data-ttu-id="a0745-113">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a0745-113">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="a0745-115"><a href="dn335126(v=exchg.10).md">columnidcentry</a></span><span class="sxs-lookup"><span data-stu-id="a0745-115"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span></span></td>
<td><span data-ttu-id="a0745-116">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Anzahl der Einträge im Index gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a0745-116">Gets the columnid of the column in the temporary table which stores the number of entries in the index.</span></span> <span data-ttu-id="a0745-117">Dieser Wert ist nicht aktuell und wird nur von &quot; API. jetcomputestats aktualisiert &quot; .</span><span class="sxs-lookup"><span data-stu-id="a0745-117">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="a0745-118">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a0745-118">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="a0745-120"><a href="dn335127(v=exchg.10).md">columnidckey</a></span><span class="sxs-lookup"><span data-stu-id="a0745-120"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span></span></td>
<td><span data-ttu-id="a0745-121">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Anzahl der eindeutigen Schlüssel im Index gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a0745-121">Gets the columnid of the column in the temporary table which stores the number of unique keys in the index.</span></span> <span data-ttu-id="a0745-122">Dieser Wert ist nicht aktuell und wird nur von &quot; API. jetcomputestats aktualisiert &quot; .</span><span class="sxs-lookup"><span data-stu-id="a0745-122">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="a0745-123">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a0745-123">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="a0745-125"><a href="dn335129(v=exchg.10).md">columnidcolyp</a></span><span class="sxs-lookup"><span data-stu-id="a0745-125"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span></span></td>
<td><span data-ttu-id="a0745-126">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der der Spaltentyp der indizierten Spalte gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a0745-126">Gets the columnid of the column in the temporary table which stores the column type of the column being indexed.</span></span> <span data-ttu-id="a0745-127">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a0745-127">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="a0745-129"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="a0745-129"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span></span></td>
<td><span data-ttu-id="a0745-130">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der das ColumnID der indizierten Spalte gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a0745-130">Gets the columnid of the column in the temporary table which stores the columnid of the column being indexed.</span></span> <span data-ttu-id="a0745-131">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a0745-131">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="a0745-133"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span><span class="sxs-lookup"><span data-stu-id="a0745-133"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span></span></td>
<td><span data-ttu-id="a0745-134">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der das grbit gespeichert ist, das auf die indizierte Spalte angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a0745-134">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="a0745-135">Siehe <a href="hh579266(v=exchg.10).md">indexkeygrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="a0745-135">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="a0745-136">Die Spalte weist den Typ <a href="hh577895(v=exchg.10).md">Text</a>auf.</span><span class="sxs-lookup"><span data-stu-id="a0745-136">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="a0745-138"><a href="dn335168(v=exchg.10).md">columnidcp</a></span><span class="sxs-lookup"><span data-stu-id="a0745-138"><a href="dn335168(v=exchg.10).md">columnidCp</a></span></span></td>
<td><span data-ttu-id="a0745-139">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Codepage der indizierten Spalte gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a0745-139">Gets the columnid of the column in the temporary table which stores the code page of the indexed column.</span></span> <span data-ttu-id="a0745-140">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Short</a>.</span><span class="sxs-lookup"><span data-stu-id="a0745-140">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="a0745-142"><a href="dn335136(v=exchg.10).md">columnidcpage</a></span><span class="sxs-lookup"><span data-stu-id="a0745-142"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span></span></td>
<td><span data-ttu-id="a0745-143">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Anzahl der Seiten im Index gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a0745-143">Gets the columnid of the column in the temporary table which stores the number of pages in the index.</span></span> <span data-ttu-id="a0745-144">Dieser Wert ist nicht aktuell und wird nur von &quot; API. jetcomputestats aktualisiert &quot; .</span><span class="sxs-lookup"><span data-stu-id="a0745-144">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="a0745-145">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a0745-145">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="a0745-147"><a href="dn335169(v=exchg.10).md">columnidgrbitcolumn</a></span><span class="sxs-lookup"><span data-stu-id="a0745-147"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span></span></td>
<td><span data-ttu-id="a0745-148">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der das grbit gespeichert ist, das auf die indizierte Spalte angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a0745-148">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="a0745-149">Siehe <a href="hh579266(v=exchg.10).md">indexkeygrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="a0745-149">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="a0745-150">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a0745-150">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="a0745-152"><a href="dn335134(v=exchg.10).md">columnidgrbitindex</a></span><span class="sxs-lookup"><span data-stu-id="a0745-152"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span></span></td>
<td><span data-ttu-id="a0745-153">Ruft das ColumnID der Spalte in der temporären Tabelle ab, die die für den Index verwendeten grbits speichert.</span><span class="sxs-lookup"><span data-stu-id="a0745-153">Gets the columnid of the column in the temporary table which stores the grbits used on the index.</span></span> <span data-ttu-id="a0745-154">Siehe " <a href="hh578433(v=exchg.10).md">kreateingedexgrbit</a>".</span><span class="sxs-lookup"><span data-stu-id="a0745-154">See <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span></span> <span data-ttu-id="a0745-155">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a0745-155">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="a0745-157"><a href="dn335170(v=exchg.10).md">columnidicolumn</a></span><span class="sxs-lookup"><span data-stu-id="a0745-157"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span></span></td>
<td><span data-ttu-id="a0745-158">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der der Index von dieser Spalte im Index Schlüssel gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a0745-158">Gets the columnid of the column in the temporary table which stores the index of of this column in the index key.</span></span> <span data-ttu-id="a0745-159">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a0745-159">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="a0745-161"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span><span class="sxs-lookup"><span data-stu-id="a0745-161"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span></span></td>
<td><span data-ttu-id="a0745-162">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der der Name des Indexes gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a0745-162">Gets the columnid of the column in the temporary table which stores the name of the index.</span></span> <span data-ttu-id="a0745-163">Die Spalte weist den Typ <a href="hh577895(v=exchg.10).md">Text</a>auf.</span><span class="sxs-lookup"><span data-stu-id="a0745-163">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="a0745-165"><a href="dn335171(v=exchg.10).md">columnidlangid</a></span><span class="sxs-lookup"><span data-stu-id="a0745-165"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span></span></td>
<td><span data-ttu-id="a0745-166">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Sprachen-ID (LCID) des Indexes gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a0745-166">Gets the columnid of the column in the temporary table which stores the language id (LCID) of the index.</span></span> <span data-ttu-id="a0745-167">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Short</a>.</span><span class="sxs-lookup"><span data-stu-id="a0745-167">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="a0745-169"><a href="dn335172(v=exchg.10).md">columnidlcmapflags</a></span><span class="sxs-lookup"><span data-stu-id="a0745-169"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span></span></td>
<td><span data-ttu-id="a0745-170">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Unicode-normalisierungs Flags für den Index gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a0745-170">Gets the columnid of the column in the temporary table which stores the unicode normalization flags for the index.</span></span> <span data-ttu-id="a0745-171">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="a0745-171">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="a0745-173"><a href="dn335173(v=exchg.10).md">crecord</a></span><span class="sxs-lookup"><span data-stu-id="a0745-173"><a href="dn335173(v=exchg.10).md">cRecord</a></span></span></td>
<td><span data-ttu-id="a0745-174">Ruft die Anzahl der Datensätze in der temporären Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="a0745-174">Gets the number of records in the temporary table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="a0745-176"><a href="dn335174(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="a0745-176"><a href="dn335174(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="a0745-177">Ruft TableID der temporären Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="a0745-177">Gets tableid of the temporary table.</span></span> <span data-ttu-id="a0745-178">Dies sollte geschlossen werden, wenn die Tabelle nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="a0745-178">This should be closed when the table is no longer needed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a0745-179">Oben</span><span class="sxs-lookup"><span data-stu-id="a0745-179">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="a0745-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0745-180">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a0745-181">Referenz</span><span class="sxs-lookup"><span data-stu-id="a0745-181">Reference</span></span>

[<span data-ttu-id="a0745-182">JET_INDEXLIST-Klasse</span><span class="sxs-lookup"><span data-stu-id="a0745-182">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="a0745-183">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="a0745-183">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
