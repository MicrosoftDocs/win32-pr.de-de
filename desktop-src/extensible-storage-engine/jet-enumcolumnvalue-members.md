---
description: 'Weitere Informationen finden Sie hier: JET_ENUMCOLUMNVALUE Member'
title: Mitglieder JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue_members(v=EXCHG.10)
ms:contentKeyID: 55103510
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2950caf527af07312f4f27c9464ee4088830fe1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104552854"
---
# <a name="jet_enumcolumnvalue-members"></a><span data-ttu-id="ed766-103">Mitglieder JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="ed766-103">JET_ENUMCOLUMNVALUE members</span></span>

<span data-ttu-id="ed766-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="ed766-104">Include protected members</span></span>  
<span data-ttu-id="ed766-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="ed766-105">Include inherited members</span></span>  

<span data-ttu-id="ed766-106">Listet die Spaltenwerte eines Datensatzes mithilfe der jetenumeratecolumns-Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="ed766-106">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="ed766-107">[Jetenumeratecolumns (JET_SESID, JET_TABLEID, Int32, \[ \] , Int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, enumeratecolumnsgrbit)](./api.jetenumeratecolumns-method.md) gibt ein Array mit JET_ENUMCOLUMNVALUE Strukturen zurück.</span><span class="sxs-lookup"><span data-stu-id="ed766-107">[JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[\], Int32, \[\], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="ed766-108">Das Array wird im Arbeitsspeicher zurückgegeben, der mithilfe des Rückrufs zugewiesen wurde, der für diese Funktion angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ed766-108">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

<span data-ttu-id="ed766-109">Der [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ed766-109">The [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="ed766-110">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="ed766-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ed766-111">Name</span><span class="sxs-lookup"><span data-stu-id="ed766-111">Name</span></span></th>
<th><span data-ttu-id="ed766-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed766-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ed766-114"><a href="dn335095(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a></span><span class="sxs-lookup"><span data-stu-id="ed766-114"><a href="dn335095(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ed766-115">Oben</span><span class="sxs-lookup"><span data-stu-id="ed766-115">Top</span></span>

## <a name="properties"></a><span data-ttu-id="ed766-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed766-116">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ed766-117">Name</span><span class="sxs-lookup"><span data-stu-id="ed766-117">Name</span></span></th>
<th><span data-ttu-id="ed766-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed766-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="ed766-120"><a href="dn335097(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="ed766-120"><a href="dn335097(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="ed766-121">Ruft die Größe des Spaltenwerts für die Spalte ab.</span><span class="sxs-lookup"><span data-stu-id="ed766-121">Gets the size of the column value for the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="ed766-123"><a href="dn335144(v=exchg.10).md">irre</a></span><span class="sxs-lookup"><span data-stu-id="ed766-123"><a href="dn335144(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="ed766-124">Ruft den Spalten Statuscode ab, der sich aus der Enumeration des Spaltenwerts ergibt.</span><span class="sxs-lookup"><span data-stu-id="ed766-124">Gets the column status code resulting from the enumeration of the column value.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="ed766-126"><a href="dn335102(v=exchg.10).md">itagsequence</a></span><span class="sxs-lookup"><span data-stu-id="ed766-126"><a href="dn335102(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="ed766-127">Ruft den Spaltenwert (durch einen einbasierten Index) ab, der aufgelistet wurde.</span><span class="sxs-lookup"><span data-stu-id="ed766-127">Gets the column value (by one-based index) that was enumerated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="ed766-129"><a href="dn335149(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="ed766-129"><a href="dn335149(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="ed766-130">Ruft den Wert ab, der für die Spalte aufgelistet wurde.</span><span class="sxs-lookup"><span data-stu-id="ed766-130">Gets the value that was enumerated for the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ed766-131">Oben</span><span class="sxs-lookup"><span data-stu-id="ed766-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="ed766-132">Methoden</span><span class="sxs-lookup"><span data-stu-id="ed766-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ed766-133">Name</span><span class="sxs-lookup"><span data-stu-id="ed766-133">Name</span></span></th>
<th><span data-ttu-id="ed766-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed766-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ed766-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></span><span class="sxs-lookup"><span data-stu-id="ed766-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="ed766-137">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="ed766-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="ed766-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="ed766-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="ed766-140">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="ed766-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ed766-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="ed766-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="ed766-143">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="ed766-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ed766-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="ed766-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="ed766-146">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="ed766-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="ed766-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></span><span class="sxs-lookup"><span data-stu-id="ed766-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="ed766-149">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="ed766-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ed766-151"><a href="dn335096(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="ed766-151"><a href="dn335096(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="ed766-152">Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die den aktuellen <a href="dn335142(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>darstellt.</span><span class="sxs-lookup"><span data-stu-id="ed766-152">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335142(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="ed766-153">(Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="ed766-153">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ed766-154">Oben</span><span class="sxs-lookup"><span data-stu-id="ed766-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="ed766-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed766-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ed766-156">Referenz</span><span class="sxs-lookup"><span data-stu-id="ed766-156">Reference</span></span>

[<span data-ttu-id="ed766-157">JET_ENUMCOLUMNVALUE-Klasse</span><span class="sxs-lookup"><span data-stu-id="ed766-157">JET_ENUMCOLUMNVALUE class</span></span>](./jet-enumcolumnvalue-class.md)

[<span data-ttu-id="ed766-158">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ed766-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
