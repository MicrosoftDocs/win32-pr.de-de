---
description: 'Weitere Informationen finden Sie hier: JET_INDEXCREATE-Eigenschaften'
title: Eigenschaften von JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103645
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 66b6ada105e6f6d12cb754f288478e85d75a07e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960595"
---
# <a name="jet_indexcreate-properties"></a><span data-ttu-id="02e88-103">Eigenschaften von JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="02e88-103">JET_INDEXCREATE properties</span></span>

<span data-ttu-id="02e88-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="02e88-104">Include protected members</span></span>  
<span data-ttu-id="02e88-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="02e88-105">Include inherited members</span></span>  

<span data-ttu-id="02e88-106">Der [JET_INDEXCREATE](./jet-indexcreate-class.md) -Typ macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="02e88-106">The [JET_INDEXCREATE](./jet-indexcreate-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="02e88-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02e88-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="02e88-108">Name</span><span class="sxs-lookup"><span data-stu-id="02e88-108">Name</span></span></th>
<th><span data-ttu-id="02e88-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02e88-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="02e88-111"><a href="dn335122(v=exchg.10).md">cbKey</a></span><span class="sxs-lookup"><span data-stu-id="02e88-111"><a href="dn335122(v=exchg.10).md">cbKey</a></span></span></td>
<td><span data-ttu-id="02e88-112">Ruft die Länge von szkey (in Zeichen) ab, einschließlich der beiden abschließenden Nullen, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="02e88-112">Gets or sets the length, in characters, of szKey including the two terminating nulls.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="02e88-114"><a href="dn335156(v=exchg.10).md">cbkeymost</a></span><span class="sxs-lookup"><span data-stu-id="02e88-114"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="02e88-115">Ruft die maximal zulässige Größe (in Bytes) für Schlüssel im Index ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="02e88-115">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="02e88-116">Die unterstützte Mindestschlüsselgröße ist JET_cbKeyMostMin (255). Dies ist die maximale maximale Schlüsselgröße.</span><span class="sxs-lookup"><span data-stu-id="02e88-116">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="02e88-117">Die maximale Schlüsselgröße hängt von der Datenbankseiten Größe <a href="hh596135(v=exchg.10).md">databasepagesize</a>ab.</span><span class="sxs-lookup"><span data-stu-id="02e88-117">The maximum key size is dependent on the database page size <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="02e88-118">Die maximale Schlüsselgröße kann mit <a href="dn351156(v=exchg.10).md">keymost</a>abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="02e88-118">The maximum key size can be retrieved with <a href="dn351156(v=exchg.10).md">KeyMost</a>.</span></span> <span data-ttu-id="02e88-119">Dieser Parameter wird unter Windows XP und Windows Server 2003 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="02e88-119">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="02e88-120">Anders als bei der nicht verwalteten API ist <strong>indexkeymost ()</strong> (JET_bitIndexKeyMost) nicht erforderlich, sondern wird automatisch hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="02e88-120">Unlike the unmanaged API, <strong>IndexKeyMost()</strong> (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="02e88-122"><a href="dn335158(v=exchg.10).md">cbvarsegmac</a></span><span class="sxs-lookup"><span data-stu-id="02e88-122"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="02e88-123">Ruft die maximale Länge (in Byte) der einzelnen Spalten ab, die im Index gespeichert werden sollen, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="02e88-123">Gets or sets the maximum length, in bytes, of each column to store in the index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="02e88-125"><a href="dn335118(v=exchg.10).md">cconditionalcolumn</a></span><span class="sxs-lookup"><span data-stu-id="02e88-125"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span></span></td>
<td><span data-ttu-id="02e88-126">Ruft die Anzahl der bedingten Spalten ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="02e88-126">Gets or sets the number of conditional columns.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="02e88-128"><a href="dn335157(v=exchg.10).md">irre</a></span><span class="sxs-lookup"><span data-stu-id="02e88-128"><a href="dn335157(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="02e88-129">Ruft den Fehlercode ab, der den Index erstellt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="02e88-129">Gets or sets the error code from creating this index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="02e88-131"><a href="dn335119(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="02e88-131"><a href="dn335119(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="02e88-132">Ruft Index Erstellungs Optionen ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="02e88-132">Gets or sets index creation options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="02e88-134"><a href="dn335159(v=exchg.10).md">pidxunicode</a></span><span class="sxs-lookup"><span data-stu-id="02e88-134"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span></span></td>
<td><span data-ttu-id="02e88-135">Ruft die optionalen Unicode-Vergleichs Optionen ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="02e88-135">Gets or sets the optional unicode comparison options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="02e88-137"><a href="dn335120(v=exchg.10).md">pspacehints</a></span><span class="sxs-lookup"><span data-stu-id="02e88-137"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span></span></td>
<td><span data-ttu-id="02e88-138">Ruft Speicherplatz Zuordnung, Wartung und Verwendungs Hinweise ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="02e88-138">Gets or sets space allocation, maintenance, and usage hints.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="02e88-140"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span><span class="sxs-lookup"><span data-stu-id="02e88-140"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span></span></td>
<td><span data-ttu-id="02e88-141">Ruft die optionalen bedingten Spalten ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="02e88-141">Gets or sets the optional conditional columns.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="02e88-143"><a href="dn335121(v=exchg.10).md">szindexname</a></span><span class="sxs-lookup"><span data-stu-id="02e88-143"><a href="dn335121(v=exchg.10).md">szIndexName</a></span></span></td>
<td><span data-ttu-id="02e88-144">Ruft den Namen des zu erstellenden Indexes ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="02e88-144">Gets or sets the name of the index to create.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="02e88-146"><a href="dn335161(v=exchg.10).md">szkey</a></span><span class="sxs-lookup"><span data-stu-id="02e88-146"><a href="dn335161(v=exchg.10).md">szKey</a></span></span></td>
<td><span data-ttu-id="02e88-147">Ruft die Beschreibung des Index Schlüssels ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="02e88-147">Gets or sets the description of the index key.</span></span> <span data-ttu-id="02e88-148">Dies ist eine Double-NULL-terminierte Zeichenfolge mit durch Null getrennten Token.</span><span class="sxs-lookup"><span data-stu-id="02e88-148">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="02e88-149">Jedes Token hat das Format [Direction-specifier] [Spaltenname], wobei Direction-Specification entweder &quot; + &quot; oder ist &quot; - &quot; .</span><span class="sxs-lookup"><span data-stu-id="02e88-149">Each token is of the form [direction-specifier][column-name], where direction-specification is either &quot;+&quot; or &quot;-&quot;.</span></span> <span data-ttu-id="02e88-150">Beispielsweise wird ein szkey von &quot; + abc\0-def\0 + ghi\0 &quot; über die drei Spalten &quot; ABC &quot; (in aufsteigender Reihenfolge), &quot; DEF &quot; (in absteigender Reihenfolge) und &quot; ghi &quot; (in aufsteigender Reihenfolge) indiziert.</span><span class="sxs-lookup"><span data-stu-id="02e88-150">for example, a szKey of &quot;+abc\0-def\0+ghi\0&quot; will index over the three columns &quot;abc&quot; (in ascending order), &quot;def&quot; (in descending order), and &quot;ghi&quot; (in ascending order).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="02e88-152"><a href="dn335162(v=exchg.10).md">uldensity</a></span><span class="sxs-lookup"><span data-stu-id="02e88-152"><a href="dn335162(v=exchg.10).md">ulDensity</a></span></span></td>
<td><span data-ttu-id="02e88-153">Ruft die Dichte des Indexes ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="02e88-153">Gets or sets the density of the index.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="02e88-154">Oben</span><span class="sxs-lookup"><span data-stu-id="02e88-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="02e88-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02e88-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="02e88-156">Referenz</span><span class="sxs-lookup"><span data-stu-id="02e88-156">Reference</span></span>

[<span data-ttu-id="02e88-157">JET_INDEXCREATE-Klasse</span><span class="sxs-lookup"><span data-stu-id="02e88-157">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="02e88-158">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="02e88-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
