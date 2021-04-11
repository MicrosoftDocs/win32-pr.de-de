---
description: 'Weitere Informationen finden Sie hier: JET_INDEXCREATE Member'
title: Mitglieder JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_members(v=EXCHG.10)
ms:contentKeyID: 55103641
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: cbe9ce962221db30c8cdae90461fa55fc0baea19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217861"
---
# <a name="jet_indexcreate-members"></a><span data-ttu-id="babf3-103">Mitglieder JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="babf3-103">JET_INDEXCREATE members</span></span>

<span data-ttu-id="babf3-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="babf3-104">Include protected members</span></span>  
<span data-ttu-id="babf3-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="babf3-105">Include inherited members</span></span>  

<span data-ttu-id="babf3-106">Enthält die Informationen, die erforderlich sind, um einen Index über Daten in einer ESE-Datenbank zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="babf3-106">Contains the information needed to create an index over data in an ESE database.</span></span> <span data-ttu-id="babf3-107">Enthält die Informationen, die erforderlich sind, um einen Index über Daten in einer ESE-Datenbank zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="babf3-107">Contains the information needed to create an index over data in an ESE database.</span></span>

<span data-ttu-id="babf3-108">Der [JET_INDEXCREATE](./jet-indexcreate-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="babf3-108">The [JET_INDEXCREATE](./jet-indexcreate-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="babf3-109">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="babf3-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="babf3-110">Name</span><span class="sxs-lookup"><span data-stu-id="babf3-110">Name</span></span></th>
<th><span data-ttu-id="babf3-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="babf3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="babf3-113"><a href="dn335115(v=exchg.10).md">JET_INDEXCREATE</a></span><span class="sxs-lookup"><span data-stu-id="babf3-113"><a href="dn335115(v=exchg.10).md">JET_INDEXCREATE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="babf3-114">Oben</span><span class="sxs-lookup"><span data-stu-id="babf3-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="babf3-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="babf3-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="babf3-116">Name</span><span class="sxs-lookup"><span data-stu-id="babf3-116">Name</span></span></th>
<th><span data-ttu-id="babf3-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="babf3-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="babf3-119"><a href="dn335122(v=exchg.10).md">cbKey</a></span><span class="sxs-lookup"><span data-stu-id="babf3-119"><a href="dn335122(v=exchg.10).md">cbKey</a></span></span></td>
<td><span data-ttu-id="babf3-120">Ruft die Länge von szkey (in Zeichen) ab, einschließlich der beiden abschließenden Nullen, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="babf3-120">Gets or sets the length, in characters, of szKey including the two terminating nulls.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="babf3-122"><a href="dn335156(v=exchg.10).md">cbkeymost</a></span><span class="sxs-lookup"><span data-stu-id="babf3-122"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="babf3-123">Ruft die maximal zulässige Größe (in Bytes) für Schlüssel im Index ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="babf3-123">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="babf3-124">Die unterstützte Mindestschlüsselgröße ist JET_cbKeyMostMin (255). Dies ist die maximale maximale Schlüsselgröße.</span><span class="sxs-lookup"><span data-stu-id="babf3-124">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="babf3-125">Die maximale Schlüsselgröße hängt von der Datenbankseiten Größe <a href="hh596135(v=exchg.10).md">databasepagesize</a>ab.</span><span class="sxs-lookup"><span data-stu-id="babf3-125">The maximum key size is dependent on the database page size <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="babf3-126">Die maximale Schlüsselgröße kann mit <a href="dn351156(v=exchg.10).md">keymost</a>abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="babf3-126">The maximum key size can be retrieved with <a href="dn351156(v=exchg.10).md">KeyMost</a>.</span></span> <span data-ttu-id="babf3-127">Dieser Parameter wird unter Windows XP und Windows Server 2003 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="babf3-127">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="babf3-128">Anders als bei der nicht verwalteten API ist <strong>indexkeymost ()</strong> (JET_bitIndexKeyMost) nicht erforderlich, sondern wird automatisch hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="babf3-128">Unlike the unmanaged API, <strong>IndexKeyMost()</strong> (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="babf3-130"><a href="dn335158(v=exchg.10).md">cbvarsegmac</a></span><span class="sxs-lookup"><span data-stu-id="babf3-130"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="babf3-131">Ruft die maximale Länge (in Byte) der einzelnen Spalten ab, die im Index gespeichert werden sollen, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="babf3-131">Gets or sets the maximum length, in bytes, of each column to store in the index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="babf3-133"><a href="dn335118(v=exchg.10).md">cconditionalcolumn</a></span><span class="sxs-lookup"><span data-stu-id="babf3-133"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span></span></td>
<td><span data-ttu-id="babf3-134">Ruft die Anzahl der bedingten Spalten ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="babf3-134">Gets or sets the number of conditional columns.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="babf3-136"><a href="dn335157(v=exchg.10).md">irre</a></span><span class="sxs-lookup"><span data-stu-id="babf3-136"><a href="dn335157(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="babf3-137">Ruft den Fehlercode ab, der den Index erstellt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="babf3-137">Gets or sets the error code from creating this index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="babf3-139"><a href="dn335119(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="babf3-139"><a href="dn335119(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="babf3-140">Ruft Index Erstellungs Optionen ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="babf3-140">Gets or sets index creation options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="babf3-142"><a href="dn335159(v=exchg.10).md">pidxunicode</a></span><span class="sxs-lookup"><span data-stu-id="babf3-142"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span></span></td>
<td><span data-ttu-id="babf3-143">Ruft die optionalen Unicode-Vergleichs Optionen ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="babf3-143">Gets or sets the optional unicode comparison options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="babf3-145"><a href="dn335120(v=exchg.10).md">pspacehints</a></span><span class="sxs-lookup"><span data-stu-id="babf3-145"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span></span></td>
<td><span data-ttu-id="babf3-146">Ruft Speicherplatz Zuordnung, Wartung und Verwendungs Hinweise ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="babf3-146">Gets or sets space allocation, maintenance, and usage hints.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="babf3-148"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span><span class="sxs-lookup"><span data-stu-id="babf3-148"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span></span></td>
<td><span data-ttu-id="babf3-149">Ruft die optionalen bedingten Spalten ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="babf3-149">Gets or sets the optional conditional columns.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="babf3-151"><a href="dn335121(v=exchg.10).md">szindexname</a></span><span class="sxs-lookup"><span data-stu-id="babf3-151"><a href="dn335121(v=exchg.10).md">szIndexName</a></span></span></td>
<td><span data-ttu-id="babf3-152">Ruft den Namen des zu erstellenden Indexes ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="babf3-152">Gets or sets the name of the index to create.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="babf3-154"><a href="dn335161(v=exchg.10).md">szkey</a></span><span class="sxs-lookup"><span data-stu-id="babf3-154"><a href="dn335161(v=exchg.10).md">szKey</a></span></span></td>
<td><span data-ttu-id="babf3-155">Ruft die Beschreibung des Index Schlüssels ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="babf3-155">Gets or sets the description of the index key.</span></span> <span data-ttu-id="babf3-156">Dies ist eine Double-NULL-terminierte Zeichenfolge mit durch Null getrennten Token.</span><span class="sxs-lookup"><span data-stu-id="babf3-156">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="babf3-157">Jedes Token hat das Format [Direction-specifier] [Spaltenname], wobei Direction-Specification entweder &quot; + &quot; oder ist &quot; - &quot; .</span><span class="sxs-lookup"><span data-stu-id="babf3-157">Each token is of the form [direction-specifier][column-name], where direction-specification is either &quot;+&quot; or &quot;-&quot;.</span></span> <span data-ttu-id="babf3-158">Beispielsweise wird ein szkey von &quot; + abc\0-def\0 + ghi\0 &quot; über die drei Spalten &quot; ABC &quot; (in aufsteigender Reihenfolge), &quot; DEF &quot; (in absteigender Reihenfolge) und &quot; ghi &quot; (in aufsteigender Reihenfolge) indiziert.</span><span class="sxs-lookup"><span data-stu-id="babf3-158">for example, a szKey of &quot;+abc\0-def\0+ghi\0&quot; will index over the three columns &quot;abc&quot; (in ascending order), &quot;def&quot; (in descending order), and &quot;ghi&quot; (in ascending order).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="babf3-160"><a href="dn335162(v=exchg.10).md">uldensity</a></span><span class="sxs-lookup"><span data-stu-id="babf3-160"><a href="dn335162(v=exchg.10).md">ulDensity</a></span></span></td>
<td><span data-ttu-id="babf3-161">Ruft die Dichte des Indexes ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="babf3-161">Gets or sets the density of the index.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="babf3-162">Oben</span><span class="sxs-lookup"><span data-stu-id="babf3-162">Top</span></span>

## <a name="methods"></a><span data-ttu-id="babf3-163">Methoden</span><span class="sxs-lookup"><span data-stu-id="babf3-163">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="babf3-164">Name</span><span class="sxs-lookup"><span data-stu-id="babf3-164">Name</span></span></th>
<th><span data-ttu-id="babf3-165">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="babf3-165">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="babf3-167"><a href="dn335116(v=exchg.10).md">Contentequals</a></span><span class="sxs-lookup"><span data-stu-id="babf3-167"><a href="dn335116(v=exchg.10).md">ContentEquals</a></span></span></td>
<td><span data-ttu-id="babf3-168">Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="babf3-168">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="babf3-170"><a href="dn335153(v=exchg.10).md">Deepclone</a></span><span class="sxs-lookup"><span data-stu-id="babf3-170"><a href="dn335153(v=exchg.10).md">DeepClone</a></span></span></td>
<td><span data-ttu-id="babf3-171">Gibt eine tiefe Kopie des-Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="babf3-171">Returns a deep copy of the object.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="babf3-173"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></span><span class="sxs-lookup"><span data-stu-id="babf3-173"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="babf3-174">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="babf3-174">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="babf3-176"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="babf3-176"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="babf3-177">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="babf3-177">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="babf3-179"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="babf3-179"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="babf3-180">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="babf3-180">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="babf3-182"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="babf3-182"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="babf3-183">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="babf3-183">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="babf3-185"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></span><span class="sxs-lookup"><span data-stu-id="babf3-185"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="babf3-186">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="babf3-186">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="babf3-188"><a href="dn335154(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="babf3-188"><a href="dn335154(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="babf3-189">Generiert eine Zeichen folgen Darstellung der-Instanz.</span><span class="sxs-lookup"><span data-stu-id="babf3-189">Generate a string representation of the instance.</span></span> <span data-ttu-id="babf3-190">(Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="babf3-190">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="babf3-191">Oben</span><span class="sxs-lookup"><span data-stu-id="babf3-191">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="babf3-192">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="babf3-192">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="babf3-193">Referenz</span><span class="sxs-lookup"><span data-stu-id="babf3-193">Reference</span></span>

[<span data-ttu-id="babf3-194">JET_INDEXCREATE-Klasse</span><span class="sxs-lookup"><span data-stu-id="babf3-194">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="babf3-195">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="babf3-195">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
