---
description: 'Weitere Informationen finden Sie hier: JET_OPENTEMPORARYTABLE-Eigenschaften'
title: JET_OPENTEMPORARYTABLE Eigenschaften (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: JET_OPENTEMPORARYTABLE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_properties(v=EXCHG.10)
ms:contentKeyID: 55104127
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e9c55afddd1128a517c27f6a86466b488e6924a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104566607"
---
# <a name="jet_opentemporarytable-properties"></a><span data-ttu-id="55c71-103">Eigenschaften von JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="55c71-103">JET_OPENTEMPORARYTABLE properties</span></span>

<span data-ttu-id="55c71-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="55c71-104">Include protected members</span></span>  
<span data-ttu-id="55c71-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="55c71-105">Include inherited members</span></span>  

<span data-ttu-id="55c71-106">Der [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="55c71-106">The [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="55c71-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55c71-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="55c71-108">Name</span><span class="sxs-lookup"><span data-stu-id="55c71-108">Name</span></span></th>
<th><span data-ttu-id="55c71-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55c71-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="55c71-111"><a href="dn335290(v=exchg.10).md">cbkeymost</a></span><span class="sxs-lookup"><span data-stu-id="55c71-111"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="55c71-112">Ruft die maximale Größe für einen Schlüssel ab, der eine angegebene Zeile darstellt, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="55c71-112">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="55c71-113">Die maximale Schlüsselgröße kann festgelegt werden, um zu steuern, wie Schlüssel abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="55c71-113">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="55c71-114">Das Abschneiden von Schlüsseln ist wichtig, da sich dies auf den Fall auswirkt, dass Zeilen als verschieden betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="55c71-114">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="55c71-115">Wenn dieser Parameter auf 0 oder 255 festgelegt ist, bleiben die maximale Schlüsselgröße und ihre Semantik identisch mit der maximalen Schlüsselgröße, die von Windows Server 2003 unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="55c71-115">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="55c71-116">Dieser Parameter kann auch auf einen größeren Wert als Funktion der Datenbankseiten Größe für die Instanz <a href="hh596135(v=exchg.10).md">databasepagesize</a>festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="55c71-116">This parameter may also be set to a larger value as a function of the database page size for the instance <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="55c71-117">Weitere Informationen finden Sie unter <a href="dn335292(v=exchg.10).md">keymost</a> .</span><span class="sxs-lookup"><span data-stu-id="55c71-117">See <a href="dn335292(v=exchg.10).md">KeyMost</a> for more information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="55c71-119"><a href="dn351219(v=exchg.10).md">cbvarsegmac</a></span><span class="sxs-lookup"><span data-stu-id="55c71-119"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="55c71-120">Ruft die maximale Datenmenge ab oder legt Sie fest, die von einer beliebigen Variablen Längen Spalte verwendet wird, um einen Schlüssel für eine bestimmte Zeile zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="55c71-120">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="55c71-121">Dieser Parameter kann verwendet werden, um die Menge des von einer bestimmten Schlüssel Spalte genutzten schlüsselplatzes zu steuern.</span><span class="sxs-lookup"><span data-stu-id="55c71-121">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="55c71-122">Dieser Grenzwert ist in Bytes.</span><span class="sxs-lookup"><span data-stu-id="55c71-122">This limit is in bytes.</span></span> <span data-ttu-id="55c71-123">Wenn dieser Parameter 0 (null) ist oder mit der <a href="dn335290(v=exchg.10).md">cbkeymost</a> -Eigenschaft identisch ist, ist kein Limit wirksam.</span><span class="sxs-lookup"><span data-stu-id="55c71-123">If this parameter is zero or is the same as the <a href="dn335290(v=exchg.10).md">cbKeyMost</a> property then no limit is in effect.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="55c71-125"><a href="dn335287(v=exchg.10).md">CColumn</a></span><span class="sxs-lookup"><span data-stu-id="55c71-125"><a href="dn335287(v=exchg.10).md">ccolumn</a></span></span></td>
<td><span data-ttu-id="55c71-126">Ruft die Anzahl der Spalten in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="55c71-126">Gets or sets the number of columns in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="55c71-128"><a href="dn351232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="55c71-128"><a href="dn351232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="55c71-129">Ruft Optionen für die temporäre Tabelle ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="55c71-129">Gets or sets options for the temp table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="55c71-131"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span><span class="sxs-lookup"><span data-stu-id="55c71-131"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span></span></td>
<td><span data-ttu-id="55c71-132">Ruft die Gebiets Schema-ID und normalisierungs Flags ab, die zum Vergleichen von Unicode-Schlüssel Spaltendaten in der temporären Tabelle verwendet werden, oder legt diese fest</span><span class="sxs-lookup"><span data-stu-id="55c71-132">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="55c71-133">Wenn dieser Parameter NULL ist, wird die Standard-LCID verwendet, um alle Unicode-Schlüssel Spalten in der temporären Tabelle zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="55c71-133">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="55c71-134">Die Standard-LCID ist das US-englische Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="55c71-134">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="55c71-135">Wenn dieser Parameter NULL ist, werden die standardnormalisierungs-Flags verwendet, um alle Unicode-Schlüssel Spaltendaten in der temporären Tabelle zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="55c71-135">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="55c71-136">Die standardnormalisierungs-Flags lauten: NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="55c71-136">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="55c71-138"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span><span class="sxs-lookup"><span data-stu-id="55c71-138"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span></span></td>
<td><span data-ttu-id="55c71-139">Ruft die Spaltendefinitionen für die in der temporären Tabelle erstellten Spalten ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="55c71-139">Gets or sets the column definitions for the columns created in the temporary table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="55c71-141"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="55c71-141"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span></span></td>
<td><span data-ttu-id="55c71-142">Ruft den Ausgabepuffer ab, der das Array der Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="55c71-142">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="55c71-143">Die Spalten-IDs in diesem Array entsprechen exakt dem Eingabe Array von Spaltendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="55c71-143">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="55c71-144">Folglich muss die Größe dieses Puffers der Größe von <a href="dn351228(v=exchg.10).md">prgcolumndef</a>entsprechen.</span><span class="sxs-lookup"><span data-stu-id="55c71-144">As a result, the size of this buffer must correspond to the size of <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="55c71-146"><a href="dn335293(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="55c71-146"><a href="dn335293(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="55c71-147">Ruft das Tabellen Handle für die temporäre Tabelle ab, die als Ergebnis eines erfolgreichen jetopumtemporarytable-Aufrufes erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="55c71-147">Gets the table handle for the temporary table created as a result of a successful call to JetOpenTemporaryTable.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="55c71-148">Oben</span><span class="sxs-lookup"><span data-stu-id="55c71-148">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="55c71-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55c71-149">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="55c71-150">Referenz</span><span class="sxs-lookup"><span data-stu-id="55c71-150">Reference</span></span>

[<span data-ttu-id="55c71-151">JET_OPENTEMPORARYTABLE-Klasse</span><span class="sxs-lookup"><span data-stu-id="55c71-151">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="55c71-152">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="55c71-152">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
