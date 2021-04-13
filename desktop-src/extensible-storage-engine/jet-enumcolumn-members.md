---
description: 'Weitere Informationen finden Sie hier: JET_ENUMCOLUMN Member'
title: Mitglieder JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103614
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: a1281d7d81fc4e0db476c4ca0f9ac688a7a7b055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561021"
---
# <a name="jet_enumcolumn-members"></a><span data-ttu-id="6a9e1-103">Mitglieder JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="6a9e1-103">JET_ENUMCOLUMN members</span></span>

<span data-ttu-id="6a9e1-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="6a9e1-104">Include protected members</span></span>  
<span data-ttu-id="6a9e1-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="6a9e1-105">Include inherited members</span></span>  

<span data-ttu-id="6a9e1-106">Listet die Spaltenwerte eines Datensatzes mithilfe der jetenumeratecolumns-Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="6a9e1-106">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="6a9e1-107">Jetenreeratecolenns gibt ein Array von JET_ENUMCOLUMNVALUE Strukturen zurück.</span><span class="sxs-lookup"><span data-stu-id="6a9e1-107">JetEnumerateColumns returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="6a9e1-108">Das Array wird im Arbeitsspeicher zurückgegeben, der mithilfe des Rückrufs zugewiesen wurde, der für diese Funktion angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6a9e1-108">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

<span data-ttu-id="6a9e1-109">Der [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6a9e1-109">The [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="6a9e1-110">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="6a9e1-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="6a9e1-111">Name</span><span class="sxs-lookup"><span data-stu-id="6a9e1-111">Name</span></span></th>
<th><span data-ttu-id="6a9e1-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a9e1-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="6a9e1-114"><a href="dn335131(v=exchg.10).md">JET_ENUMCOLUMN</a></span><span class="sxs-lookup"><span data-stu-id="6a9e1-114"><a href="dn335131(v=exchg.10).md">JET_ENUMCOLUMN</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6a9e1-115">Oben</span><span class="sxs-lookup"><span data-stu-id="6a9e1-115">Top</span></span>

## <a name="properties"></a><span data-ttu-id="6a9e1-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6a9e1-116">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="6a9e1-117">Name</span><span class="sxs-lookup"><span data-stu-id="6a9e1-117">Name</span></span></th>
<th><span data-ttu-id="6a9e1-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a9e1-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="6a9e1-120"><a href="dn335137(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="6a9e1-120"><a href="dn335137(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="6a9e1-121">Ruft die Größe des Werts ab, der für die Spalte aufgelistet wurde.</span><span class="sxs-lookup"><span data-stu-id="6a9e1-121">Gets the size of the value that was enumerated for the column.</span></span> <span data-ttu-id="6a9e1-122">Dieser Member wird nur verwendet, wenn <a href="dn335086(v=exchg.10).md">Err</a> gleich <a href="hh557250(v=exchg.10).md">columnsinglevalue</a>ist.</span><span class="sxs-lookup"><span data-stu-id="6a9e1-122">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is equal to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="6a9e1-124"><a href="dn335085(v=exchg.10).md">cenenumcolumnvalue</a></span><span class="sxs-lookup"><span data-stu-id="6a9e1-124"><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></span></span></td>
<td><span data-ttu-id="6a9e1-125">Ruft die Anzahl der für die Spalte aufgelisteten Spaltenwerte ab.</span><span class="sxs-lookup"><span data-stu-id="6a9e1-125">Gets the number of column values enumerated for the column.</span></span> <span data-ttu-id="6a9e1-126">Dieser Member wird nur verwendet, wenn <a href="dn335086(v=exchg.10).md">Err</a> nicht <a href="hh557250(v=exchg.10).md">columnsinglevalue</a>ist.</span><span class="sxs-lookup"><span data-stu-id="6a9e1-126">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is not <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="6a9e1-128"><a href="dn335135(v=exchg.10).md">ColumnID</a></span><span class="sxs-lookup"><span data-stu-id="6a9e1-128"><a href="dn335135(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="6a9e1-129">Ruft die aufgelistete ColumnID-ID ab.</span><span class="sxs-lookup"><span data-stu-id="6a9e1-129">Gets the columnid ID that was enumerated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="6a9e1-131"><a href="dn335086(v=exchg.10).md">irre</a></span><span class="sxs-lookup"><span data-stu-id="6a9e1-131"><a href="dn335086(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="6a9e1-132">Ruft den Spalten Statuscode ab, der sich aus der-Enumeration ergibt.</span><span class="sxs-lookup"><span data-stu-id="6a9e1-132">Gets the column status code that results from the enumeration.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="6a9e1-134"><a href="dn335087(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="6a9e1-134"><a href="dn335087(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="6a9e1-135">Ruft den Wert ab, der für die Spalte aufgelistet wurde.</span><span class="sxs-lookup"><span data-stu-id="6a9e1-135">Gets the value that was enumerated for the column.</span></span> <span data-ttu-id="6a9e1-136">Dieser Member wird nur verwendet, wenn <a href="dn335086(v=exchg.10).md">Err</a> gleich <a href="hh557250(v=exchg.10).md">columnsinglevalue</a>ist.</span><span class="sxs-lookup"><span data-stu-id="6a9e1-136">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is equal to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span> <span data-ttu-id="6a9e1-137">Dies verweist auf den Arbeitsspeicher, der mit dem an <a href="dn292148(v=exchg.10).md">jetenumeratecolumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, enumeratecolumnsgrbit)</a>weiter gegebenen Rückruf für den <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> Zuweisung zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="6a9e1-137">This points to memory allocated with the <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> allocator callback passed to <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>.</span></span> <span data-ttu-id="6a9e1-138">Vergessen Sie nicht, den Arbeitsspeicher zu veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="6a9e1-138">Remember to release the memory when finished.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="6a9e1-140"><a href="dn335089(v=exchg.10).md">rgenenumcolumnvalue</a></span><span class="sxs-lookup"><span data-stu-id="6a9e1-140"><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></span></span></td>
<td><span data-ttu-id="6a9e1-141">Ruft die enumerationsspaltenwerte für die Spalte ab.</span><span class="sxs-lookup"><span data-stu-id="6a9e1-141">Gets the enumerated column values for the column.</span></span> <span data-ttu-id="6a9e1-142">Dieser Member wird nur verwendet, wenn <a href="dn335086(v=exchg.10).md">Err</a> nicht <a href="hh557250(v=exchg.10).md">columnsinglevalue</a>ist.</span><span class="sxs-lookup"><span data-stu-id="6a9e1-142">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is not <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6a9e1-143">Oben</span><span class="sxs-lookup"><span data-stu-id="6a9e1-143">Top</span></span>

## <a name="methods"></a><span data-ttu-id="6a9e1-144">Methoden</span><span class="sxs-lookup"><span data-stu-id="6a9e1-144">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="6a9e1-145">Name</span><span class="sxs-lookup"><span data-stu-id="6a9e1-145">Name</span></span></th>
<th><span data-ttu-id="6a9e1-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a9e1-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="6a9e1-148"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></span><span class="sxs-lookup"><span data-stu-id="6a9e1-148"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="6a9e1-149">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="6a9e1-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="6a9e1-151"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="6a9e1-151"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="6a9e1-152">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="6a9e1-152">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="6a9e1-154"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="6a9e1-154"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="6a9e1-155">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="6a9e1-155">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="6a9e1-157"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="6a9e1-157"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="6a9e1-158">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="6a9e1-158">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="6a9e1-160"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></span><span class="sxs-lookup"><span data-stu-id="6a9e1-160"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="6a9e1-161">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="6a9e1-161">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="6a9e1-163"><a href="dn335132(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="6a9e1-163"><a href="dn335132(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="6a9e1-164">Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die den aktuellen <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a>darstellt.</span><span class="sxs-lookup"><span data-stu-id="6a9e1-164">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a>.</span></span> <span data-ttu-id="6a9e1-165">(Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="6a9e1-165">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6a9e1-166">Oben</span><span class="sxs-lookup"><span data-stu-id="6a9e1-166">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="6a9e1-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a9e1-167">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6a9e1-168">Referenz</span><span class="sxs-lookup"><span data-stu-id="6a9e1-168">Reference</span></span>

[<span data-ttu-id="6a9e1-169">JET_ENUMCOLUMN-Klasse</span><span class="sxs-lookup"><span data-stu-id="6a9e1-169">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="6a9e1-170">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="6a9e1-170">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
