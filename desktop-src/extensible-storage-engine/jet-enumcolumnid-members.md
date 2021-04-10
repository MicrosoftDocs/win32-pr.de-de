---
description: 'Weitere Informationen finden Sie hier: JET_ENUMCOLUMNID Member'
title: Mitglieder JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_members(v=EXCHG.10)
ms:contentKeyID: 55103504
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f852541d8e16a1a9edfd87afe59a0a8a4c4c4af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041600"
---
# <a name="jet_enumcolumnid-members"></a><span data-ttu-id="1bf0f-103">Mitglieder JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="1bf0f-103">JET_ENUMCOLUMNID members</span></span>

<span data-ttu-id="1bf0f-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="1bf0f-104">Include protected members</span></span>  
<span data-ttu-id="1bf0f-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="1bf0f-105">Include inherited members</span></span>  

<span data-ttu-id="1bf0f-106">Listet einen bestimmten Satz von Spalten und optional einen bestimmten Satz von mehreren Werten für diese Spalten auf, wenn die jetenumeratecolumns-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1bf0f-106">Enumerates a specific set of columns and, optionally, a specific set of multiple values for those columns when the JetEnumerateColumns function is used.</span></span> <span data-ttu-id="1bf0f-107">Jetenumschlag-atecolrens nimmt optional ein Array von JET_ENUMCOLUMNID Strukturen an.</span><span class="sxs-lookup"><span data-stu-id="1bf0f-107">JetEnumerateColumns optionally takes an array of JET_ENUMCOLUMNID structures.</span></span>

<span data-ttu-id="1bf0f-108">Der [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1bf0f-108">The [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="1bf0f-109">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="1bf0f-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="1bf0f-110">Name</span><span class="sxs-lookup"><span data-stu-id="1bf0f-110">Name</span></span></th>
<th><span data-ttu-id="1bf0f-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bf0f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="1bf0f-113"><a href="dn335140(v=exchg.10).md">JET_ENUMCOLUMNID</a></span><span class="sxs-lookup"><span data-stu-id="1bf0f-113"><a href="dn335140(v=exchg.10).md">JET_ENUMCOLUMNID</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1bf0f-114">Oben</span><span class="sxs-lookup"><span data-stu-id="1bf0f-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="1bf0f-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1bf0f-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="1bf0f-116">Name</span><span class="sxs-lookup"><span data-stu-id="1bf0f-116">Name</span></span></th>
<th><span data-ttu-id="1bf0f-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bf0f-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="1bf0f-119"><a href="dn335141(v=exchg.10).md">ColumnID</a></span><span class="sxs-lookup"><span data-stu-id="1bf0f-119"><a href="dn335141(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="1bf0f-120">Ruft die aufzuzählenden Spalten-ID ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="1bf0f-120">Gets or sets the columnid ID to enumerate.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="1bf0f-122"><a href="dn335092(v=exchg.10).md">ctagsequence</a></span><span class="sxs-lookup"><span data-stu-id="1bf0f-122"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span></span></td>
<td><span data-ttu-id="1bf0f-123">Ruft die Anzahl der Spaltenwerte (durch einen einbasierten Index) ab, die für die angegebene Spalten-ID aufgelistet werden sollen, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="1bf0f-123">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="1bf0f-124">Wenn ctagsequence gleich 0 (null) ist, wird rgtagsequence ignoriert, und alle Spaltenwerte für die angegebene Spalten-ID werden aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1bf0f-124">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="1bf0f-126"><a href="dn335093(v=exchg.10).md">rgtagsequence</a></span><span class="sxs-lookup"><span data-stu-id="1bf0f-126"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span></span></td>
<td><span data-ttu-id="1bf0f-127">Ruft das Array von einbasierten Indizes in das Array von Spaltenwerten für eine angegebene Spalte ab oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="1bf0f-127">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="1bf0f-128">Bei einem einzelnen Element handelt es sich um eine in JET_RETRIEVECOLUMN definierte itagsequence.</span><span class="sxs-lookup"><span data-stu-id="1bf0f-128">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="1bf0f-129">Eine itagsequence-Wert von 0 (null) bedeutet &quot; Skip &quot; .</span><span class="sxs-lookup"><span data-stu-id="1bf0f-129">An itagSequence of 0 (zero) means &quot;skip&quot;.</span></span> <span data-ttu-id="1bf0f-130">Eine itagsequence von 1 bedeutet, dass der erste Spaltenwert der Spalte zurückgegeben wird, der Wert 2 für den zweiten Wert usw.</span><span class="sxs-lookup"><span data-stu-id="1bf0f-130">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1bf0f-131">Oben</span><span class="sxs-lookup"><span data-stu-id="1bf0f-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="1bf0f-132">Methoden</span><span class="sxs-lookup"><span data-stu-id="1bf0f-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="1bf0f-133">Name</span><span class="sxs-lookup"><span data-stu-id="1bf0f-133">Name</span></span></th>
<th><span data-ttu-id="1bf0f-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bf0f-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="1bf0f-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></span><span class="sxs-lookup"><span data-stu-id="1bf0f-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="1bf0f-137">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="1bf0f-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="1bf0f-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="1bf0f-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="1bf0f-140">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="1bf0f-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="1bf0f-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="1bf0f-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="1bf0f-143">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="1bf0f-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="1bf0f-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="1bf0f-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="1bf0f-146">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="1bf0f-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="1bf0f-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></span><span class="sxs-lookup"><span data-stu-id="1bf0f-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="1bf0f-149">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="1bf0f-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="1bf0f-151"><a href="dn335091(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="1bf0f-151"><a href="dn335091(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="1bf0f-152">Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die den aktuellen <a href="dn335139(v=exchg.10).md">JET_ENUMCOLUMNID</a>darstellt.</span><span class="sxs-lookup"><span data-stu-id="1bf0f-152">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335139(v=exchg.10).md">JET_ENUMCOLUMNID</a>.</span></span> <span data-ttu-id="1bf0f-153">(Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="1bf0f-153">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1bf0f-154">Oben</span><span class="sxs-lookup"><span data-stu-id="1bf0f-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="1bf0f-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1bf0f-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1bf0f-156">Referenz</span><span class="sxs-lookup"><span data-stu-id="1bf0f-156">Reference</span></span>

[<span data-ttu-id="1bf0f-157">JET_ENUMCOLUMNID-Klasse</span><span class="sxs-lookup"><span data-stu-id="1bf0f-157">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="1bf0f-158">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="1bf0f-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
