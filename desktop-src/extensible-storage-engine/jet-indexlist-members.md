---
description: 'Weitere Informationen finden Sie hier: JET_INDEXLIST Member'
title: Mitglieder JET_INDEXLIST
TOCTitle: JET_INDEXLIST members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_members(v=EXCHG.10)
ms:contentKeyID: 55103660
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d7800ef911366bad40b2d02ee60e23b5d138d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050336"
---
# <a name="jet_indexlist-members"></a><span data-ttu-id="0ec6c-103">Mitglieder JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="0ec6c-103">JET_INDEXLIST members</span></span>

<span data-ttu-id="0ec6c-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="0ec6c-104">Include protected members</span></span>  
<span data-ttu-id="0ec6c-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="0ec6c-105">Include inherited members</span></span>  

<span data-ttu-id="0ec6c-106">Informationen zu einer temporären Tabelle, die Informationen zu allen Indizes für eine bestimmte Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-106">Information about a temporary table containing information about all indexes for a given table.</span></span>

<span data-ttu-id="0ec6c-107">Der [JET_INDEXLIST](./jet-indexlist-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-107">The [JET_INDEXLIST](./jet-indexlist-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="0ec6c-108">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="0ec6c-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="0ec6c-109">Name</span><span class="sxs-lookup"><span data-stu-id="0ec6c-109">Name</span></span></th>
<th><span data-ttu-id="0ec6c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ec6c-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="0ec6c-112"><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-112"><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0ec6c-113">Oben</span><span class="sxs-lookup"><span data-stu-id="0ec6c-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="0ec6c-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0ec6c-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="0ec6c-115">Name</span><span class="sxs-lookup"><span data-stu-id="0ec6c-115">Name</span></span></th>
<th><span data-ttu-id="0ec6c-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ec6c-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="0ec6c-118"><a href="dn335125(v=exchg.10).md">columnidccolumn</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-118"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span></span></td>
<td><span data-ttu-id="0ec6c-119">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Anzahl der Spalten im Index Schlüssel gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-119">Gets the columnid of the column in the temporary table which stores the number of columns in the index key.</span></span> <span data-ttu-id="0ec6c-120">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-120">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="0ec6c-122"><a href="dn335126(v=exchg.10).md">columnidcentry</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-122"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span></span></td>
<td><span data-ttu-id="0ec6c-123">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Anzahl der Einträge im Index gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-123">Gets the columnid of the column in the temporary table which stores the number of entries in the index.</span></span> <span data-ttu-id="0ec6c-124">Dieser Wert ist nicht aktuell und wird nur von &quot; API. jetcomputestats aktualisiert &quot; .</span><span class="sxs-lookup"><span data-stu-id="0ec6c-124">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="0ec6c-125">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-125">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="0ec6c-127"><a href="dn335127(v=exchg.10).md">columnidckey</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-127"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span></span></td>
<td><span data-ttu-id="0ec6c-128">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Anzahl der eindeutigen Schlüssel im Index gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-128">Gets the columnid of the column in the temporary table which stores the number of unique keys in the index.</span></span> <span data-ttu-id="0ec6c-129">Dieser Wert ist nicht aktuell und wird nur von &quot; API. jetcomputestats aktualisiert &quot; .</span><span class="sxs-lookup"><span data-stu-id="0ec6c-129">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="0ec6c-130">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-130">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="0ec6c-132"><a href="dn335129(v=exchg.10).md">columnidcolyp</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-132"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span></span></td>
<td><span data-ttu-id="0ec6c-133">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der der Spaltentyp der indizierten Spalte gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-133">Gets the columnid of the column in the temporary table which stores the column type of the column being indexed.</span></span> <span data-ttu-id="0ec6c-134">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-134">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="0ec6c-136"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-136"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span></span></td>
<td><span data-ttu-id="0ec6c-137">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der das ColumnID der indizierten Spalte gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-137">Gets the columnid of the column in the temporary table which stores the columnid of the column being indexed.</span></span> <span data-ttu-id="0ec6c-138">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-138">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="0ec6c-140"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-140"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span></span></td>
<td><span data-ttu-id="0ec6c-141">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der das grbit gespeichert ist, das auf die indizierte Spalte angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-141">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="0ec6c-142">Siehe <a href="hh579266(v=exchg.10).md">indexkeygrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-142">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="0ec6c-143">Die Spalte weist den Typ <a href="hh577895(v=exchg.10).md">Text</a>auf.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-143">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="0ec6c-145"><a href="dn335168(v=exchg.10).md">columnidcp</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-145"><a href="dn335168(v=exchg.10).md">columnidCp</a></span></span></td>
<td><span data-ttu-id="0ec6c-146">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Codepage der indizierten Spalte gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-146">Gets the columnid of the column in the temporary table which stores the code page of the indexed column.</span></span> <span data-ttu-id="0ec6c-147">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Short</a>.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-147">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="0ec6c-149"><a href="dn335136(v=exchg.10).md">columnidcpage</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-149"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span></span></td>
<td><span data-ttu-id="0ec6c-150">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Anzahl der Seiten im Index gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-150">Gets the columnid of the column in the temporary table which stores the number of pages in the index.</span></span> <span data-ttu-id="0ec6c-151">Dieser Wert ist nicht aktuell und wird nur von &quot; API. jetcomputestats aktualisiert &quot; .</span><span class="sxs-lookup"><span data-stu-id="0ec6c-151">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="0ec6c-152">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-152">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="0ec6c-154"><a href="dn335169(v=exchg.10).md">columnidgrbitcolumn</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-154"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span></span></td>
<td><span data-ttu-id="0ec6c-155">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der das grbit gespeichert ist, das auf die indizierte Spalte angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-155">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="0ec6c-156">Siehe <a href="hh579266(v=exchg.10).md">indexkeygrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-156">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="0ec6c-157">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-157">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="0ec6c-159"><a href="dn335134(v=exchg.10).md">columnidgrbitindex</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-159"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span></span></td>
<td><span data-ttu-id="0ec6c-160">Ruft das ColumnID der Spalte in der temporären Tabelle ab, die die für den Index verwendeten grbits speichert.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-160">Gets the columnid of the column in the temporary table which stores the grbits used on the index.</span></span> <span data-ttu-id="0ec6c-161">Siehe " <a href="hh578433(v=exchg.10).md">kreateingedexgrbit</a>".</span><span class="sxs-lookup"><span data-stu-id="0ec6c-161">See <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span></span> <span data-ttu-id="0ec6c-162">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-162">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="0ec6c-164"><a href="dn335170(v=exchg.10).md">columnidicolumn</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-164"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span></span></td>
<td><span data-ttu-id="0ec6c-165">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der der Index von dieser Spalte im Index Schlüssel gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-165">Gets the columnid of the column in the temporary table which stores the index of of this column in the index key.</span></span> <span data-ttu-id="0ec6c-166">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-166">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="0ec6c-168"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-168"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span></span></td>
<td><span data-ttu-id="0ec6c-169">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der der Name des Indexes gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-169">Gets the columnid of the column in the temporary table which stores the name of the index.</span></span> <span data-ttu-id="0ec6c-170">Die Spalte weist den Typ <a href="hh577895(v=exchg.10).md">Text</a>auf.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-170">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="0ec6c-172"><a href="dn335171(v=exchg.10).md">columnidlangid</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-172"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span></span></td>
<td><span data-ttu-id="0ec6c-173">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Sprachen-ID (LCID) des Indexes gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-173">Gets the columnid of the column in the temporary table which stores the language id (LCID) of the index.</span></span> <span data-ttu-id="0ec6c-174">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Short</a>.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-174">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="0ec6c-176"><a href="dn335172(v=exchg.10).md">columnidlcmapflags</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-176"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span></span></td>
<td><span data-ttu-id="0ec6c-177">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Unicode-normalisierungs Flags für den Index gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-177">Gets the columnid of the column in the temporary table which stores the unicode normalization flags for the index.</span></span> <span data-ttu-id="0ec6c-178">Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-178">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="0ec6c-180"><a href="dn335173(v=exchg.10).md">crecord</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-180"><a href="dn335173(v=exchg.10).md">cRecord</a></span></span></td>
<td><span data-ttu-id="0ec6c-181">Ruft die Anzahl der Datensätze in der temporären Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-181">Gets the number of records in the temporary table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="0ec6c-183"><a href="dn335174(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-183"><a href="dn335174(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="0ec6c-184">Ruft TableID der temporären Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-184">Gets tableid of the temporary table.</span></span> <span data-ttu-id="0ec6c-185">Dies sollte geschlossen werden, wenn die Tabelle nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-185">This should be closed when the table is no longer needed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0ec6c-186">Oben</span><span class="sxs-lookup"><span data-stu-id="0ec6c-186">Top</span></span>

## <a name="methods"></a><span data-ttu-id="0ec6c-187">Methoden</span><span class="sxs-lookup"><span data-stu-id="0ec6c-187">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="0ec6c-188">Name</span><span class="sxs-lookup"><span data-stu-id="0ec6c-188">Name</span></span></th>
<th><span data-ttu-id="0ec6c-189">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ec6c-189">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="0ec6c-191"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-191"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="0ec6c-192">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="0ec6c-192">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="0ec6c-194"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-194"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="0ec6c-195">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="0ec6c-195">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="0ec6c-197"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-197"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="0ec6c-198">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="0ec6c-198">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="0ec6c-200"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-200"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="0ec6c-201">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="0ec6c-201">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="0ec6c-203"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-203"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="0ec6c-204">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="0ec6c-204">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="0ec6c-206"><a href="dn335165(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="0ec6c-206"><a href="dn335165(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="0ec6c-207">Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die den aktuellen <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>darstellt.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-207">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>.</span></span> <span data-ttu-id="0ec6c-208">(Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="0ec6c-208">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0ec6c-209">Oben</span><span class="sxs-lookup"><span data-stu-id="0ec6c-209">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="0ec6c-210">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ec6c-210">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0ec6c-211">Referenz</span><span class="sxs-lookup"><span data-stu-id="0ec6c-211">Reference</span></span>

[<span data-ttu-id="0ec6c-212">JET_INDEXLIST-Klasse</span><span class="sxs-lookup"><span data-stu-id="0ec6c-212">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="0ec6c-213">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="0ec6c-213">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
