---
description: 'Weitere Informationen finden Sie hier: JET_OPENTEMPORARYTABLE Member'
title: JET_OPENTEMPORARYTABLE Mitglieder (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: JET_OPENTEMPORARYTABLE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_members(v=EXCHG.10)
ms:contentKeyID: 55104223
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af149ecba6858aca4b4877fc9446872386406838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104551253"
---
# <a name="jet_opentemporarytable-members"></a><span data-ttu-id="adf35-103">Mitglieder JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="adf35-103">JET_OPENTEMPORARYTABLE members</span></span>

<span data-ttu-id="adf35-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="adf35-104">Include protected members</span></span>  
<span data-ttu-id="adf35-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="adf35-105">Include inherited members</span></span>  

<span data-ttu-id="adf35-106">Eine Auflistung von Parametern für die jetopertemporarytable-Methode.</span><span class="sxs-lookup"><span data-stu-id="adf35-106">A collection of parameters for the JetOpenTemporaryTable method.</span></span>

<span data-ttu-id="adf35-107">Der [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="adf35-107">The [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="adf35-108">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="adf35-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="adf35-109">Name</span><span class="sxs-lookup"><span data-stu-id="adf35-109">Name</span></span></th>
<th><span data-ttu-id="adf35-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="adf35-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="adf35-112"><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></span><span class="sxs-lookup"><span data-stu-id="adf35-112"><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="adf35-113">Oben</span><span class="sxs-lookup"><span data-stu-id="adf35-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="adf35-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="adf35-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="adf35-115">Name</span><span class="sxs-lookup"><span data-stu-id="adf35-115">Name</span></span></th>
<th><span data-ttu-id="adf35-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="adf35-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="adf35-118"><a href="dn335290(v=exchg.10).md">cbkeymost</a></span><span class="sxs-lookup"><span data-stu-id="adf35-118"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="adf35-119">Ruft die maximale Größe für einen Schlüssel ab, der eine angegebene Zeile darstellt, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="adf35-119">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="adf35-120">Die maximale Schlüsselgröße kann festgelegt werden, um zu steuern, wie Schlüssel abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="adf35-120">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="adf35-121">Das Abschneiden von Schlüsseln ist wichtig, da sich dies auf den Fall auswirkt, dass Zeilen als verschieden betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="adf35-121">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="adf35-122">Wenn dieser Parameter auf 0 oder 255 festgelegt ist, bleiben die maximale Schlüsselgröße und ihre Semantik identisch mit der maximalen Schlüsselgröße, die von Windows Server 2003 unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="adf35-122">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="adf35-123">Dieser Parameter kann auch auf einen größeren Wert als Funktion der Datenbankseiten Größe für die Instanz <a href="hh596135(v=exchg.10).md">databasepagesize</a>festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="adf35-123">This parameter may also be set to a larger value as a function of the database page size for the instance <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="adf35-124">Weitere Informationen finden Sie unter <a href="dn335292(v=exchg.10).md">keymost</a> .</span><span class="sxs-lookup"><span data-stu-id="adf35-124">See <a href="dn335292(v=exchg.10).md">KeyMost</a> for more information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="adf35-126"><a href="dn351219(v=exchg.10).md">cbvarsegmac</a></span><span class="sxs-lookup"><span data-stu-id="adf35-126"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="adf35-127">Ruft die maximale Datenmenge ab oder legt Sie fest, die von einer beliebigen Variablen Längen Spalte verwendet wird, um einen Schlüssel für eine bestimmte Zeile zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="adf35-127">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="adf35-128">Dieser Parameter kann verwendet werden, um die Menge des von einer bestimmten Schlüssel Spalte genutzten schlüsselplatzes zu steuern.</span><span class="sxs-lookup"><span data-stu-id="adf35-128">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="adf35-129">Dieser Grenzwert ist in Bytes.</span><span class="sxs-lookup"><span data-stu-id="adf35-129">This limit is in bytes.</span></span> <span data-ttu-id="adf35-130">Wenn dieser Parameter 0 (null) ist oder mit der <a href="dn335290(v=exchg.10).md">cbkeymost</a> -Eigenschaft identisch ist, ist kein Limit wirksam.</span><span class="sxs-lookup"><span data-stu-id="adf35-130">If this parameter is zero or is the same as the <a href="dn335290(v=exchg.10).md">cbKeyMost</a> property then no limit is in effect.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="adf35-132"><a href="dn335287(v=exchg.10).md">CColumn</a></span><span class="sxs-lookup"><span data-stu-id="adf35-132"><a href="dn335287(v=exchg.10).md">ccolumn</a></span></span></td>
<td><span data-ttu-id="adf35-133">Ruft die Anzahl der Spalten in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="adf35-133">Gets or sets the number of columns in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="adf35-135"><a href="dn351232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="adf35-135"><a href="dn351232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="adf35-136">Ruft Optionen für die temporäre Tabelle ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="adf35-136">Gets or sets options for the temp table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="adf35-138"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span><span class="sxs-lookup"><span data-stu-id="adf35-138"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span></span></td>
<td><span data-ttu-id="adf35-139">Ruft die Gebiets Schema-ID und normalisierungs Flags ab, die zum Vergleichen von Unicode-Schlüssel Spaltendaten in der temporären Tabelle verwendet werden, oder legt diese fest</span><span class="sxs-lookup"><span data-stu-id="adf35-139">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="adf35-140">Wenn dieser Parameter NULL ist, wird die Standard-LCID verwendet, um alle Unicode-Schlüssel Spalten in der temporären Tabelle zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="adf35-140">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="adf35-141">Die Standard-LCID ist das US-englische Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="adf35-141">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="adf35-142">Wenn dieser Parameter NULL ist, werden die standardnormalisierungs-Flags verwendet, um alle Unicode-Schlüssel Spaltendaten in der temporären Tabelle zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="adf35-142">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="adf35-143">Die standardnormalisierungs-Flags lauten: NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="adf35-143">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="adf35-145"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span><span class="sxs-lookup"><span data-stu-id="adf35-145"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span></span></td>
<td><span data-ttu-id="adf35-146">Ruft die Spaltendefinitionen für die in der temporären Tabelle erstellten Spalten ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="adf35-146">Gets or sets the column definitions for the columns created in the temporary table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="adf35-148"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="adf35-148"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span></span></td>
<td><span data-ttu-id="adf35-149">Ruft den Ausgabepuffer ab, der das Array der Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="adf35-149">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="adf35-150">Die Spalten-IDs in diesem Array entsprechen exakt dem Eingabe Array von Spaltendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="adf35-150">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="adf35-151">Folglich muss die Größe dieses Puffers der Größe von <a href="dn351228(v=exchg.10).md">prgcolumndef</a>entsprechen.</span><span class="sxs-lookup"><span data-stu-id="adf35-151">As a result, the size of this buffer must correspond to the size of <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="adf35-153"><a href="dn335293(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="adf35-153"><a href="dn335293(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="adf35-154">Ruft das Tabellen Handle für die temporäre Tabelle ab, die als Ergebnis eines erfolgreichen jetopumtemporarytable-Aufrufes erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="adf35-154">Gets the table handle for the temporary table created as a result of a successful call to JetOpenTemporaryTable.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="adf35-155">Oben</span><span class="sxs-lookup"><span data-stu-id="adf35-155">Top</span></span>

## <a name="methods"></a><span data-ttu-id="adf35-156">Methoden</span><span class="sxs-lookup"><span data-stu-id="adf35-156">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="adf35-157">Name</span><span class="sxs-lookup"><span data-stu-id="adf35-157">Name</span></span></th>
<th><span data-ttu-id="adf35-158">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="adf35-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="adf35-160"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></span><span class="sxs-lookup"><span data-stu-id="adf35-160"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="adf35-161">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="adf35-161">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="adf35-163"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="adf35-163"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="adf35-164">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="adf35-164">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="adf35-166"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="adf35-166"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="adf35-167">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="adf35-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="adf35-169"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="adf35-169"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="adf35-170">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="adf35-170">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="adf35-172"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></span><span class="sxs-lookup"><span data-stu-id="adf35-172"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="adf35-173">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="adf35-173">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="adf35-175"><a href="dn335286(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="adf35-175"><a href="dn335286(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="adf35-176">Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die den aktuellen <a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>darstellt.</span><span class="sxs-lookup"><span data-stu-id="adf35-176">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>.</span></span> <span data-ttu-id="adf35-177">(Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="adf35-177">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="adf35-178">Oben</span><span class="sxs-lookup"><span data-stu-id="adf35-178">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="adf35-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adf35-179">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="adf35-180">Referenz</span><span class="sxs-lookup"><span data-stu-id="adf35-180">Reference</span></span>

[<span data-ttu-id="adf35-181">JET_OPENTEMPORARYTABLE-Klasse</span><span class="sxs-lookup"><span data-stu-id="adf35-181">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="adf35-182">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="adf35-182">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
