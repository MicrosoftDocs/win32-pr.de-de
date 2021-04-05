---
description: 'Weitere Informationen finden Sie hier: JET_SETINFO Member'
title: Mitglieder JET_SETINFO
TOCTitle: JET_SETINFO members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_members(v=EXCHG.10)
ms:contentKeyID: 55103871
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c782eace916b3871ade67870b08e1766faeafd28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750489"
---
# <a name="jet_setinfo-members"></a><span data-ttu-id="92132-103">Mitglieder JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="92132-103">JET_SETINFO members</span></span>

<span data-ttu-id="92132-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="92132-104">Include protected members</span></span>  
<span data-ttu-id="92132-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="92132-105">Include inherited members</span></span>  

<span data-ttu-id="92132-106">Einstellungen für jetsetcolumn.</span><span class="sxs-lookup"><span data-stu-id="92132-106">Settings for JetSetColumn.</span></span>

<span data-ttu-id="92132-107">Der [JET_SETINFO](./jet-setinfo-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="92132-107">The [JET_SETINFO](./jet-setinfo-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="92132-108">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="92132-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="92132-109">Name</span><span class="sxs-lookup"><span data-stu-id="92132-109">Name</span></span></th>
<th><span data-ttu-id="92132-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92132-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="92132-112"><a href="dn351031(v=exchg.10).md">JET_SETINFO</a></span><span class="sxs-lookup"><span data-stu-id="92132-112"><a href="dn351031(v=exchg.10).md">JET_SETINFO</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="92132-113">Oben</span><span class="sxs-lookup"><span data-stu-id="92132-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="92132-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92132-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="92132-115">Name</span><span class="sxs-lookup"><span data-stu-id="92132-115">Name</span></span></th>
<th><span data-ttu-id="92132-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92132-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="92132-118"><a href="dn351064(v=exchg.10).md">iblongvalue</a></span><span class="sxs-lookup"><span data-stu-id="92132-118"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="92132-119">Ruft den Offset bis zum ersten Byte ab, das in einer Spalte vom Typ <a href="hh577895(v=exchg.10).md">LONGBINARY</a> oder <a href="hh577895(v=exchg.10).md">LONGTEXT</a>festgelegt werden soll, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="92132-119">Gets or sets offset to the first byte to be set in a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="92132-121"><a href="dn351037(v=exchg.10).md">itagsequence</a></span><span class="sxs-lookup"><span data-stu-id="92132-121"><a href="dn351037(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="92132-122">Ruft die Sequenznummer des Werts in einer mehrwertigen Spalte ab, die festgelegt werden soll, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="92132-122">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="92132-123">Das Array von Werten ist 1-basiert.</span><span class="sxs-lookup"><span data-stu-id="92132-123">The array of values is one-based.</span></span> <span data-ttu-id="92132-124">Der erste Wert ist Sequenz 1, nicht 0 (null).</span><span class="sxs-lookup"><span data-stu-id="92132-124">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="92132-125">Wenn die Daten Satz Spalte nur über einen Wert verfügt, sollte 1 als itagsequence übergeben werden, wenn dieser Wert ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="92132-125">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="92132-126">Der Wert 0 (null) bedeutet, dass am Ende der Sequenz der Spaltenwerte eine neue Spaltenwert Instanz hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="92132-126">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="92132-127">Oben</span><span class="sxs-lookup"><span data-stu-id="92132-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="92132-128">Methoden</span><span class="sxs-lookup"><span data-stu-id="92132-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="92132-129">Name</span><span class="sxs-lookup"><span data-stu-id="92132-129">Name</span></span></th>
<th><span data-ttu-id="92132-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92132-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="92132-132"><a href="dn351060(v=exchg.10).md">Contentequals</a></span><span class="sxs-lookup"><span data-stu-id="92132-132"><a href="dn351060(v=exchg.10).md">ContentEquals</a></span></span></td>
<td><span data-ttu-id="92132-133">Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="92132-133">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="92132-135"><a href="dn351032(v=exchg.10).md">Deepclone</a></span><span class="sxs-lookup"><span data-stu-id="92132-135"><a href="dn351032(v=exchg.10).md">DeepClone</a></span></span></td>
<td><span data-ttu-id="92132-136">Gibt eine tiefe Kopie des-Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="92132-136">Returns a deep copy of the object.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="92132-138"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></span><span class="sxs-lookup"><span data-stu-id="92132-138"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="92132-139">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="92132-139">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="92132-141"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="92132-141"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="92132-142">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="92132-142">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="92132-144"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="92132-144"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="92132-145">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="92132-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="92132-147"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="92132-147"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="92132-148">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="92132-148">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="92132-150"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></span><span class="sxs-lookup"><span data-stu-id="92132-150"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="92132-151">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="92132-151">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="92132-153"><a href="dn351062(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="92132-153"><a href="dn351062(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="92132-154">Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die den aktuellen <a href="dn351059(v=exchg.10).md">JET_SETINFO</a>darstellt.</span><span class="sxs-lookup"><span data-stu-id="92132-154">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351059(v=exchg.10).md">JET_SETINFO</a>.</span></span> <span data-ttu-id="92132-155">(Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="92132-155">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="92132-156">Oben</span><span class="sxs-lookup"><span data-stu-id="92132-156">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="92132-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92132-157">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="92132-158">Referenz</span><span class="sxs-lookup"><span data-stu-id="92132-158">Reference</span></span>

[<span data-ttu-id="92132-159">JET_SETINFO-Klasse</span><span class="sxs-lookup"><span data-stu-id="92132-159">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="92132-160">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="92132-160">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
