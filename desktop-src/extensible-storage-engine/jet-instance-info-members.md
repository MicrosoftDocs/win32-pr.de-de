---
description: 'Weitere Informationen finden Sie hier: JET_INSTANCE_INFO Member'
title: Mitglieder JET_INSTANCE_INFO
TOCTitle: JET_INSTANCE_INFO members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info_members(v=EXCHG.10)
ms:contentKeyID: 55103693
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 42d9bcd2c078766875fc8230eaf83dc07fdb4b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561312"
---
# <a name="jet_instance_info-members"></a><span data-ttu-id="78ee3-103">Mitglieder JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="78ee3-103">JET_INSTANCE_INFO members</span></span>

<span data-ttu-id="78ee3-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="78ee3-104">Include protected members</span></span>  
<span data-ttu-id="78ee3-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="78ee3-105">Include inherited members</span></span>  

<span data-ttu-id="78ee3-106">Empfängt Informationen über die Ausführung von Datenbankinstanzen, wenn Sie mit den Funktionen jetgetinstanceinfo und jedessnapshotfreeze verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78ee3-106">Receives information about running database instances when used with the JetGetInstanceInfo and JetOSSnapshotFreeze functions.</span></span>

<span data-ttu-id="78ee3-107">Der [JET_INSTANCE_INFO](./jet-instance-info-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="78ee3-107">The [JET_INSTANCE_INFO](./jet-instance-info-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="78ee3-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="78ee3-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="78ee3-109">Name</span><span class="sxs-lookup"><span data-stu-id="78ee3-109">Name</span></span></th>
<th><span data-ttu-id="78ee3-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78ee3-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="78ee3-112"><a href="dn335189(v=exchg.10).md">cdatenbanken</a></span><span class="sxs-lookup"><span data-stu-id="78ee3-112"><a href="dn335189(v=exchg.10).md">cDatabases</a></span></span></td>
<td><span data-ttu-id="78ee3-113">Ruft die Anzahl der Datenbanken ab, die an die Daten Bank Instanz angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="78ee3-113">Gets the number of databases that are attached to the database instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="78ee3-115"><a href="dn335190(v=exchg.10).md">hinstanceid</a></span><span class="sxs-lookup"><span data-stu-id="78ee3-115"><a href="dn335190(v=exchg.10).md">hInstanceId</a></span></span></td>
<td><span data-ttu-id="78ee3-116">Ruft den JET_INSTANCE der angegebenen-Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="78ee3-116">Gets the JET_INSTANCE of the given instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="78ee3-118"><a href="dn335193(v=exchg.10).md">szdatabasedateiname</a></span><span class="sxs-lookup"><span data-stu-id="78ee3-118"><a href="dn335193(v=exchg.10).md">szDatabaseFileName</a></span></span></td>
<td><span data-ttu-id="78ee3-119">Ruft eine Auflistung von Zeichen folgen ab, die jeweils den Dateinamen einer Datenbank enthält, die an die Daten Bank Instanz angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="78ee3-119">Gets a collection of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="78ee3-120">Das Array verfügt über cdatenbanken-Elemente.</span><span class="sxs-lookup"><span data-stu-id="78ee3-120">The array has cDatabases elements.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="78ee3-122"><a href="dn335194(v=exchg.10).md">szinstancename</a></span><span class="sxs-lookup"><span data-stu-id="78ee3-122"><a href="dn335194(v=exchg.10).md">szInstanceName</a></span></span></td>
<td><span data-ttu-id="78ee3-123">Ruft den Namen der Daten Bank Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="78ee3-123">Gets the name of the database instance.</span></span> <span data-ttu-id="78ee3-124">Dieser Wert kann NULL sein, wenn die Instanz keinen Namen hat.</span><span class="sxs-lookup"><span data-stu-id="78ee3-124">This value can be null if the instance does not have a name.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="78ee3-125">Oben</span><span class="sxs-lookup"><span data-stu-id="78ee3-125">Top</span></span>

## <a name="methods"></a><span data-ttu-id="78ee3-126">Methoden</span><span class="sxs-lookup"><span data-stu-id="78ee3-126">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="78ee3-127">Name</span><span class="sxs-lookup"><span data-stu-id="78ee3-127">Name</span></span></th>
<th><span data-ttu-id="78ee3-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78ee3-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="78ee3-130"><a href="dn335184(v=exchg.10).md">Ist gleich(Objekt)</a></span><span class="sxs-lookup"><span data-stu-id="78ee3-130"><a href="dn335184(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="78ee3-131">Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="78ee3-131">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="78ee3-132">(Überschreibt <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object. gleich(Objekt)</a>.)</span><span class="sxs-lookup"><span data-stu-id="78ee3-132">(Overrides <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="78ee3-134"><a href="dn335187(v=exchg.10).md">Ist gleich(JET_INSTANCE_INFO)</a></span><span class="sxs-lookup"><span data-stu-id="78ee3-134"><a href="dn335187(v=exchg.10).md">Equals(JET_INSTANCE_INFO)</a></span></span></td>
<td><span data-ttu-id="78ee3-135">Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="78ee3-135">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="78ee3-137"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="78ee3-137"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="78ee3-138">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="78ee3-138">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="78ee3-140"><a href="dn335191(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="78ee3-140"><a href="dn335191(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="78ee3-141">Gibt den Hashcode für diese Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="78ee3-141">Returns the hash code for this instance.</span></span> <span data-ttu-id="78ee3-142">(Überschreibt <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object. GetHashCode ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="78ee3-142">(Overrides <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="78ee3-144"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="78ee3-144"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="78ee3-145">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="78ee3-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="78ee3-147"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></span><span class="sxs-lookup"><span data-stu-id="78ee3-147"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="78ee3-148">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="78ee3-148">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="78ee3-150"><a href="dn335192(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="78ee3-150"><a href="dn335192(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="78ee3-151">Generiert eine Zeichen folgen Darstellung der-Instanz.</span><span class="sxs-lookup"><span data-stu-id="78ee3-151">Generate a string representation of the instance.</span></span> <span data-ttu-id="78ee3-152">(Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="78ee3-152">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="78ee3-153">Oben</span><span class="sxs-lookup"><span data-stu-id="78ee3-153">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="78ee3-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78ee3-154">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="78ee3-155">Referenz</span><span class="sxs-lookup"><span data-stu-id="78ee3-155">Reference</span></span>

[<span data-ttu-id="78ee3-156">JET_INSTANCE_INFO-Klasse</span><span class="sxs-lookup"><span data-stu-id="78ee3-156">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="78ee3-157">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="78ee3-157">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
