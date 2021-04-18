---
description: 'Weitere Informationen finden Sie hier: JET_RECSIZE Member'
title: JET_RECSIZE Mitglieder (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: JET_RECSIZE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_members(v=EXCHG.10)
ms:contentKeyID: 39510137
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 224d22b5dea0447297163fb6b5e1a70fe62a6396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557015"
---
# <a name="jet_recsize-members"></a><span data-ttu-id="607f3-103">Mitglieder JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="607f3-103">JET_RECSIZE members</span></span>

<span data-ttu-id="607f3-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="607f3-104">Include protected members</span></span>  
<span data-ttu-id="607f3-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="607f3-105">Include inherited members</span></span>  

<span data-ttu-id="607f3-106">Wird von [jetgetrecordsize (JET_SESID, JET_TABLEID, JET_RECSIZE, getrecordsizegrbit)](./vistaapi.jetgetrecordsize-method.md) verwendet, um Informationen über die Verwendungs Anforderungen eines Datensatzes im Benutzerdaten Bereich, die Anzahl der Mengen Spalten, die Anzahl der Werte und den mehr Aufwand für die ESENT-Daten Satzstruktur zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="607f3-106">Used by [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESENT record structure overhead space.</span></span>

<span data-ttu-id="607f3-107">Der [JET_RECSIZE](./jet-recsize-structure2.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="607f3-107">The [JET_RECSIZE](./jet-recsize-structure2.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="607f3-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="607f3-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="607f3-109">Name</span><span class="sxs-lookup"><span data-stu-id="607f3-109">Name</span></span></th>
<th><span data-ttu-id="607f3-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="607f3-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="607f3-112"><a href="hh557581(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="607f3-112"><a href="hh557581(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="607f3-113">Ruft das Benutzer DataSet im Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="607f3-113">Gets the user data set in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="607f3-115"><a href="hh596280(v=exchg.10).md">cbdatacompressed</a></span><span class="sxs-lookup"><span data-stu-id="607f3-115"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span></span></td>
<td><span data-ttu-id="607f3-116">Ruft die komprimierte Größe der Benutzerdaten im Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="607f3-116">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="607f3-117">Dies ist das gleiche wie bei <a href="hh557581(v=exchg.10).md">cbData</a> , wenn keine systeminternen langen Werte komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="607f3-117">This is the same as <a href="hh557581(v=exchg.10).md">cbData</a> if no intrinsic long-values are compressed).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="607f3-119"><a href="hh557913(v=exchg.10).md">cblongvaluedata</a></span><span class="sxs-lookup"><span data-stu-id="607f3-119"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span></span></td>
<td><span data-ttu-id="607f3-120">Ruft das Benutzer DataSet im Datensatz ab, wird jedoch in der Struktur mit langem Wert gespeichert.</span><span class="sxs-lookup"><span data-stu-id="607f3-120">Gets the user data set in the record, but stored in the long-value tree.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="607f3-122"><a href="hh566144(v=exchg.10).md">cblongvaluedatacompressed</a></span><span class="sxs-lookup"><span data-stu-id="607f3-122"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span></span></td>
<td><span data-ttu-id="607f3-123">Ruft die komprimierte Größe von Benutzerdaten in der Struktur mit langem Wert ab.</span><span class="sxs-lookup"><span data-stu-id="607f3-123">Gets the compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="607f3-124">Dies entspricht <a href="hh557913(v=exchg.10).md">cblongvaluedata</a> , wenn keine getrennten langen Werte komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="607f3-124">This is the same as <a href="hh557913(v=exchg.10).md">cbLongValueData</a> if no separated long values are compressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="607f3-126"><a href="hh558003(v=exchg.10).md">cblongvalueoverhead</a></span><span class="sxs-lookup"><span data-stu-id="607f3-126"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span></span></td>
<td><span data-ttu-id="607f3-127">Ruft den mehr Aufwand für die Daten des langen Werts ab.</span><span class="sxs-lookup"><span data-stu-id="607f3-127">Gets the overhead of the long-value data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="607f3-129"><a href="hh565836(v=exchg.10).md">cboverhead</a></span><span class="sxs-lookup"><span data-stu-id="607f3-129"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span></span></td>
<td><span data-ttu-id="607f3-130">Ruft den Aufwand der ESENT-Daten Satzstruktur für diesen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="607f3-130">Gets the overhead of the ESENT record structure for this record.</span></span> <span data-ttu-id="607f3-131">Dazu gehört auch die Schlüsselgröße des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="607f3-131">This includes the record's key size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="607f3-133"><a href="hh566154(v=exchg.10).md">ccompressedcolumns</a></span><span class="sxs-lookup"><span data-stu-id="607f3-133"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span></span></td>
<td><span data-ttu-id="607f3-134">Ruft die Gesamtzahl der Spalten im Datensatz ab, die komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="607f3-134">Gets the total number of columns in the record which are compressed.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="607f3-136"><a href="hh596288(v=exchg.10).md">clongvalues</a></span><span class="sxs-lookup"><span data-stu-id="607f3-136"><a href="hh596288(v=exchg.10).md">cLongValues</a></span></span></td>
<td><span data-ttu-id="607f3-137">Ruft die Gesamtzahl der Long-Werte ab, die in der Struktur mit dem langen Wert für diesen Datensatz gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="607f3-137">Gets the total number of long values stored in the long-value tree for this record.</span></span> <span data-ttu-id="607f3-138">Dies schließt keine systeminternen Long-Werte ein.</span><span class="sxs-lookup"><span data-stu-id="607f3-138">This does not include intrinsic long values.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="607f3-140"><a href="hh577486(v=exchg.10).md">cmultivalues</a></span><span class="sxs-lookup"><span data-stu-id="607f3-140"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span></span></td>
<td><span data-ttu-id="607f3-141">Ruft die Ansammlung der Gesamtzahl der Werte über den ersten für alle Spalten im Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="607f3-141">Gets the accumulation of the total number of values beyond the first for all columns in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="607f3-143"><a href="hh578172(v=exchg.10).md">cnontaggedcolumns</a></span><span class="sxs-lookup"><span data-stu-id="607f3-143"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span></span></td>
<td><span data-ttu-id="607f3-144">Ruft die Gesamtanzahl fester und variabler Spalten ab, die in diesem Datensatz festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="607f3-144">Gets the total number of fixed and variable columns set in this record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="607f3-146"><a href="hh566034(v=exchg.10).md">ctaggedcolumns</a></span><span class="sxs-lookup"><span data-stu-id="607f3-146"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span></span></td>
<td><span data-ttu-id="607f3-147">Ruft die Gesamtzahl der markierten Spalten ab, die in diesem Datensatz festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="607f3-147">Gets the total number of tagged columns set in this record.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="607f3-148">Oben</span><span class="sxs-lookup"><span data-stu-id="607f3-148">Top</span></span>

## <a name="methods"></a><span data-ttu-id="607f3-149">Methoden</span><span class="sxs-lookup"><span data-stu-id="607f3-149">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="607f3-150">Name</span><span class="sxs-lookup"><span data-stu-id="607f3-150">Name</span></span></th>
<th><span data-ttu-id="607f3-151">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="607f3-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="607f3-154"><a href="hh538879(v=exchg.10).md">Add (Hinzufügen)</a></span><span class="sxs-lookup"><span data-stu-id="607f3-154"><a href="hh538879(v=exchg.10).md">Add</a></span></span></td>
<td><span data-ttu-id="607f3-155">Fügen Sie die Größen in zwei JET_RECSIZE Strukturen hinzu.</span><span class="sxs-lookup"><span data-stu-id="607f3-155">Add the sizes in two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="607f3-157"><a href="hh558506(v=exchg.10).md">Ist gleich(Objekt)</a></span><span class="sxs-lookup"><span data-stu-id="607f3-157"><a href="hh558506(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="607f3-158">Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="607f3-158">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="607f3-159">(Überschreibt <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType. gleich (Object)</a>.)</span><span class="sxs-lookup"><span data-stu-id="607f3-159">(Overrides <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="607f3-161"><a href="hh577992(v=exchg.10).md">Ist gleich(JET_RECSIZE)</a></span><span class="sxs-lookup"><span data-stu-id="607f3-161"><a href="hh577992(v=exchg.10).md">Equals(JET_RECSIZE)</a></span></span></td>
<td><span data-ttu-id="607f3-162">Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="607f3-162">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="607f3-164"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="607f3-164"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="607f3-165">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="607f3-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="607f3-167"><a href="hh557078(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="607f3-167"><a href="hh557078(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="607f3-168">Gibt den Hashcode für diese Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="607f3-168">Returns the hash code for this instance.</span></span> <span data-ttu-id="607f3-169">(Überschreibt <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType. GetHashCode ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="607f3-169">(Overrides <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="607f3-171"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="607f3-171"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="607f3-172">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="607f3-172">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="607f3-174"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></span><span class="sxs-lookup"><span data-stu-id="607f3-174"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="607f3-175">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="607f3-175">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="607f3-178"><a href="hh579561(v=exchg.10).md">Subtrahieren</a></span><span class="sxs-lookup"><span data-stu-id="607f3-178"><a href="hh579561(v=exchg.10).md">Subtract</a></span></span></td>
<td><span data-ttu-id="607f3-179">Berechnen Sie den Unterschied in den Größen zwischen zwei JET_RECSIZE Strukturen.</span><span class="sxs-lookup"><span data-stu-id="607f3-179">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="607f3-181"><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></span><span class="sxs-lookup"><span data-stu-id="607f3-181"><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></span></span></td>
<td><span data-ttu-id="607f3-182">(Geerbt von <a href="/dotnet/api/system.valuetype">ValueType</a>.)</span><span class="sxs-lookup"><span data-stu-id="607f3-182">(Inherited from <a href="/dotnet/api/system.valuetype">ValueType</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="607f3-183">Oben</span><span class="sxs-lookup"><span data-stu-id="607f3-183">Top</span></span>

## <a name="operators"></a><span data-ttu-id="607f3-184">Operatoren</span><span class="sxs-lookup"><span data-stu-id="607f3-184">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="607f3-185">Name</span><span class="sxs-lookup"><span data-stu-id="607f3-185">Name</span></span></th>
<th><span data-ttu-id="607f3-186">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="607f3-186">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Öffentlicher Operator" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="607f3-189"><a href="hh578675(v=exchg.10).md">Zudem</a></span><span class="sxs-lookup"><span data-stu-id="607f3-189"><a href="hh578675(v=exchg.10).md">Addition</a></span></span></td>
<td><span data-ttu-id="607f3-190">Fügen Sie die Größen in zwei JET_RECSIZE Strukturen hinzu.</span><span class="sxs-lookup"><span data-stu-id="607f3-190">Add the sizes in two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Öffentlicher Operator" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="607f3-193"><a href="hh596362(v=exchg.10).md">Gleichheit</a></span><span class="sxs-lookup"><span data-stu-id="607f3-193"><a href="hh596362(v=exchg.10).md">Equality</a></span></span></td>
<td><span data-ttu-id="607f3-194">Bestimmt, ob zwei angegebene Instanzen von JET_RECSIZE gleich sind.</span><span class="sxs-lookup"><span data-stu-id="607f3-194">Determines whether two specified instances of JET_RECSIZE are equal.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Öffentlicher Operator" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="607f3-197"><a href="hh578809(v=exchg.10).md">Ungleichheit</a></span><span class="sxs-lookup"><span data-stu-id="607f3-197"><a href="hh578809(v=exchg.10).md">Inequality</a></span></span></td>
<td><span data-ttu-id="607f3-198">Bestimmt, ob zwei angegebene Instanzen von JET_RECSIZE nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="607f3-198">Determines whether two specified instances of JET_RECSIZE are not equal.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Öffentlicher Operator" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="607f3-201"><a href="hh596696(v=exchg.10).md">Subtraktion</a></span><span class="sxs-lookup"><span data-stu-id="607f3-201"><a href="hh596696(v=exchg.10).md">Subtraction</a></span></span></td>
<td><span data-ttu-id="607f3-202">Berechnen Sie den Unterschied in den Größen zwischen zwei JET_RECSIZE Strukturen.</span><span class="sxs-lookup"><span data-stu-id="607f3-202">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="607f3-203">Oben</span><span class="sxs-lookup"><span data-stu-id="607f3-203">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="607f3-204">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="607f3-204">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="607f3-205">Referenz</span><span class="sxs-lookup"><span data-stu-id="607f3-205">Reference</span></span>

[<span data-ttu-id="607f3-206">JET_RECSIZE Struktur</span><span class="sxs-lookup"><span data-stu-id="607f3-206">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="607f3-207">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="607f3-207">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
