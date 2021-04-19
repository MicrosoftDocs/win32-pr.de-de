---
description: 'Weitere Informationen finden Sie hier: JET_SPACEHINTS Struktur'
title: JET_SPACEHINTS Struktur
TOCTitle: JET_SPACEHINTS Structure
ms:assetid: 23328993-93c9-4a23-892b-e6a9f434d1d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269205(v=EXCHG.10)
ms:contentKeyID: 32765508
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf786d1f47b5eaae3f9540c8635853020f9b0521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344398"
---
# <a name="jet_spacehints-structure"></a><span data-ttu-id="46727-103">JET_SPACEHINTS Struktur</span><span class="sxs-lookup"><span data-stu-id="46727-103">JET_SPACEHINTS Structure</span></span>


<span data-ttu-id="46727-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="46727-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_spacehints-structure"></a><span data-ttu-id="46727-105">JET_SPACEHINTS Struktur</span><span class="sxs-lookup"><span data-stu-id="46727-105">JET_SPACEHINTS Structure</span></span>

<span data-ttu-id="46727-106">Die **JET_SPACEHINTS** Struktur enthält Informationen zu Speicherplatz Zuordnungs Mustern, wenn eine b-Struktur durch Anfüge-oder hotpointteilungen wächst.</span><span class="sxs-lookup"><span data-stu-id="46727-106">The **JET_SPACEHINTS** structure contains information about space allocation patterns when a b-tree grows through append or hotpoint splits.</span></span> <span data-ttu-id="46727-107">Anfüge Teilungen treten auf, wenn dem Ende einer b-Strukturdaten Sätze hinzugefügt werden und die hotpointteilungen durchgeführt werden, wenn der gleichen virtuellen Einfügemarke mehrere Datensätze hinzugefügt werden (z. b. "Marie", "Mark", "Martin", "Mary" in der Mitte einer in eine alphabetisch sortierten b-Struktur hinzufügen).</span><span class="sxs-lookup"><span data-stu-id="46727-107">Append splits happen when records are added to the end of a b-tree and hotpoint splits happen when multiple records are added to the same virtual insertion point (for example, adding 'Marie', 'Mark', 'Martin', 'Mary' to the middle of a b-tree that is sorted alphabetically).</span></span>

<span data-ttu-id="46727-108">**Windows 7:** Die **JET_SPACEHINTS** Struktur wird in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="46727-108">**Windows 7:** The **JET_SPACEHINTS** structure is introduced in Windows 7.</span></span>

```cpp
    typedef struct tagJET_SPACEHINTS {
      unsigned long cbStruct;
      unsigned long ulInitialDensity;
      unsigned long cbInitial;
      JET_GRBIT grbit;
      unsigned long ulMaintDensity;
      unsigned long ulGrowth;
      unsigned long cbMinExtent;
      unsigned long cbMaxExtent;
    } JET_SPACEHINTS;
```

### <a name="members"></a><span data-ttu-id="46727-109">Member</span><span class="sxs-lookup"><span data-stu-id="46727-109">Members</span></span>

<span data-ttu-id="46727-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="46727-110">**cbStruct**</span></span>

<span data-ttu-id="46727-111">Die Größe (in Bytes) dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="46727-111">The size, in bytes, of this structure.</span></span> <span data-ttu-id="46727-112">Legen Sie diesen Member auf sizeof (JET_SPACEHINTS) fest.</span><span class="sxs-lookup"><span data-stu-id="46727-112">Set this member to sizeof( JET_SPACEHINTS ).</span></span>

<span data-ttu-id="46727-113">**ulinitialdensity**</span><span class="sxs-lookup"><span data-stu-id="46727-113">**ulInitialDensity**</span></span>

<span data-ttu-id="46727-114">Die Dichte beim (Anfügen) Layout.</span><span class="sxs-lookup"><span data-stu-id="46727-114">The density at (append) layout.</span></span>

<span data-ttu-id="46727-115">**cbinitial**</span><span class="sxs-lookup"><span data-stu-id="46727-115">**cbInitial**</span></span>

<span data-ttu-id="46727-116">Die Anfangs Größe (in Bytes) des Objekts, das erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="46727-116">The initial size (in bytes) of the object being created.</span></span> <span data-ttu-id="46727-117">Dies muss ein Vielfaches der Seitengröße der Datenbank sein.</span><span class="sxs-lookup"><span data-stu-id="46727-117">This must be a multiple of the database page size.</span></span>

<span data-ttu-id="46727-118">**grbit**</span><span class="sxs-lookup"><span data-stu-id="46727-118">**grbit**</span></span>

<span data-ttu-id="46727-119">Eine Gruppe von Bits, die die für diese-Struktur zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="46727-119">A group of bits that contain the options to be used for this structure, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46727-120">Wert</span><span class="sxs-lookup"><span data-stu-id="46727-120">Value</span></span></p></th>
<th><p><span data-ttu-id="46727-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="46727-121">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46727-122">JET_bitSpaceHintsUtilizeParentSpace</span><span class="sxs-lookup"><span data-stu-id="46727-122">JET_bitSpaceHintsUtilizeParentSpace</span></span><br />
<span data-ttu-id="46727-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="46727-123">0x00000001</span></span></p></td>
<td><p><span data-ttu-id="46727-124">Ändert die interne Zuordnungs Richtlinie, um Speicherplatz auf der Grundlage des unmittelbar übergeordneten Elements einer b-Struktur zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="46727-124">Changes the internal allocation policy to get space heirarchically from the immediate parent of a b-tree.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46727-125">JET_bitCreateHintAppendSequential</span><span class="sxs-lookup"><span data-stu-id="46727-125">JET_bitCreateHintAppendSequential</span></span><br />
<span data-ttu-id="46727-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="46727-126">0x00000002</span></span></p></td>
<td><p><span data-ttu-id="46727-127">Ermöglicht das Anfügen von Split-Verhalten entsprechend der Wachstumsdynamik der Tabelle (festgelegt durch cbminblock, ulgrowth, cbmaxblock).</span><span class="sxs-lookup"><span data-stu-id="46727-127">Enables append split behavior to grow according to the growth dynamics of the table (set by cbMinExtent, ulGrowth, cbMaxExtent).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46727-128">JET_bitCreateHintHotpointSequential</span><span class="sxs-lookup"><span data-stu-id="46727-128">JET_bitCreateHintHotpointSequential</span></span><br />
<span data-ttu-id="46727-129">0x00000004</span><span class="sxs-lookup"><span data-stu-id="46727-129">0x00000004</span></span></p></td>
<td><p><span data-ttu-id="46727-130">Ermöglicht das Anwachsen des hotpointverhaltens entsprechend der Wachstumsdynamik der Tabelle (festgelegt durch cbminblock, ulgrowth, cbmaxblock).</span><span class="sxs-lookup"><span data-stu-id="46727-130">Enables hotpoint split behavior to grow according to the growth dynamics of the table (set by cbMinExtent, ulGrowth, cbMaxExtent).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46727-131">JET_bitRetrieveHintTableScanForward</span><span class="sxs-lookup"><span data-stu-id="46727-131">JET_bitRetrieveHintTableScanForward</span></span><br />
<span data-ttu-id="46727-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46727-132">0x00000010</span></span></p></td>
<td><p><span data-ttu-id="46727-133">Wenn dieser Wert festgelegt ist, gibt der Client an, dass der Forward-sequenzielle Scan das vorherrschende Verwendungs Muster dieser Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="46727-133">If set, the client indicates that forward sequential scan is the predominant usage pattern of this table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46727-134">JET_bitRetrieveHintTableScanBackward</span><span class="sxs-lookup"><span data-stu-id="46727-134">JET_bitRetrieveHintTableScanBackward</span></span><br />
<span data-ttu-id="46727-135">0x00000020</span><span class="sxs-lookup"><span data-stu-id="46727-135">0x00000020</span></span></p></td>
<td><p><span data-ttu-id="46727-136">Wenn festgelegt, gibt der Client an, dass die rückwärts sequenzielle Überprüfung das vorherrschende Verwendungs Muster dieser Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="46727-136">If set, the client indicates that backward sequential scan is the predominant usage pattern of this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46727-137">JET_bitDeleteHintTableSequential</span><span class="sxs-lookup"><span data-stu-id="46727-137">JET_bitDeleteHintTableSequential</span></span><br />
<span data-ttu-id="46727-138">0x00000100</span><span class="sxs-lookup"><span data-stu-id="46727-138">0x00000100</span></span></p></td>
<td><p><span data-ttu-id="46727-139">Wenn festgelegt, erwartet die Anwendung, dass diese Tabelle in sequenzieller Reihenfolge vom niedrigsten zum höchsten Schlüssel bereinigt wird.</span><span class="sxs-lookup"><span data-stu-id="46727-139">If set, the application expects this table to be cleaned up in sequential order, from lowest key to highest key.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="46727-140">**ulmaintdensity**</span><span class="sxs-lookup"><span data-stu-id="46727-140">**ulMaintDensity**</span></span>

<span data-ttu-id="46727-141">Dichte für mehrmaintdensity</span><span class="sxs-lookup"><span data-stu-id="46727-141">density to mulMaintDensity</span></span>

<span data-ttu-id="46727-142">Die zu verwaltende Dichte.</span><span class="sxs-lookup"><span data-stu-id="46727-142">Density to maintain at.</span></span> <span data-ttu-id="46727-143">Wenn die Speicherplatz Hinweise JET_bitRetrieveHintTableScanForward oder JET_bitRetrieveHintTableScanBackward angeben, wird die Tabellen Defragmentierung ausgelöst, wenn der verwendete Speicherplatz in der Tabelle unter diesen Schwellenwert fällt.</span><span class="sxs-lookup"><span data-stu-id="46727-143">If the space hints specify JET_bitRetrieveHintTableScanForward or JET_bitRetrieveHintTableScanBackward, table defragmentation will be triggered when the used space in the table drops below this threshold.</span></span> <span data-ttu-id="46727-144">Die Tabellen Defragmentierung kann deaktiviert werden, indem dieser Member auf NULL festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="46727-144">Table defragmentation can be disabled by setting this member to zero.</span></span> <span data-ttu-id="46727-145">Wenn dieser Member auf 100 festgelegt wird, wird die Tabellen Defragmentierung ausgeführt, sobald eine Seite freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="46727-145">Setting this member to 100 will cause table defragmentation to run as soon as a page is freed.</span></span>

<span data-ttu-id="46727-146">**ulgrowth**</span><span class="sxs-lookup"><span data-stu-id="46727-146">**ulGrowth**</span></span>

<span data-ttu-id="46727-147">Das prozentuale Wachstum von der letzten Vergrößerung oder anfangs Größe auf die nächste Native Jet-Zuordnungs Größe gerundet.</span><span class="sxs-lookup"><span data-stu-id="46727-147">The percent growth from the last growth or initial size, rounded to nearest native JET allocation size.</span></span>

<span data-ttu-id="46727-148">**cbminblock zu klein**</span><span class="sxs-lookup"><span data-stu-id="46727-148">**cbMinExtent too small**</span></span>

<span data-ttu-id="46727-149">Dies überschreibt ulgrowth, wenn zu klein.</span><span class="sxs-lookup"><span data-stu-id="46727-149">This overrides ulGrowth if too small.</span></span>

<span data-ttu-id="46727-150">**cbmaxblock**</span><span class="sxs-lookup"><span data-stu-id="46727-150">**cbMaxExtent**</span></span>

<span data-ttu-id="46727-151">Der maximale Wert für das Wachstum in Bytes.</span><span class="sxs-lookup"><span data-stu-id="46727-151">The maximum value for growth in bytes.</span></span> <span data-ttu-id="46727-152">Dies begrenzt ulgrowth.</span><span class="sxs-lookup"><span data-stu-id="46727-152">This caps ulGrowth.</span></span>

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a><span data-ttu-id="46727-153">Wenn eine b-Struktur durch Anfüge-oder hotpointteilungen wächst (im Gegensatz zu zufälligen Daten Satz Einfügungen), wird der von der Tabelle generierte Speicherplatz wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="46727-153">When a b-tree grows through append or hotpoint splits (as opposed to random record insertions), the amount of space the table will grow by is calculated as follows:</span></span>

1.  <span data-ttu-id="46727-154">Bei der Erstellung wird der b-Struktur cbinitial, immer, übergeben.</span><span class="sxs-lookup"><span data-stu-id="46727-154">At creation, we give the b-tree cbInitial, always.</span></span>

2.  <span data-ttu-id="46727-155">Während der ersten Zuordnung eines bestimmten Bereichs belegen wir Folgendes: cbinitial \* ulgrowth/100 (gerundet auf die Seitengröße der Datenbank) oder cbminblock, wenn größer.</span><span class="sxs-lookup"><span data-stu-id="46727-155">During the first allocation of a given area, we will allocate: cbInitial \* ulGrowth / 100 (rounded to the DB's page size), or cbMinExtent if larger.</span></span>

3.  <span data-ttu-id="46727-156">Bei der nächsten Zuordnung wird cblastalloc \* ulgrowth/100 (auf die Seitengröße der DB gerundet) oder cbminblock, wenn größer.</span><span class="sxs-lookup"><span data-stu-id="46727-156">During the next allocation, cbLastAlloc \* ulGrowth / 100 (rounded to the page size of the DB), or cbMinExtent if larger.</span></span>

4.  <span data-ttu-id="46727-157">Bei einer Zuordnungs Zuweisung (bei der es sich um die erste Zuordnung handeln kann), überschreitet die berechnete Größe den cbmaxblock, und dies ist die Vergrößerung.</span><span class="sxs-lookup"><span data-stu-id="46727-157">At some allocation (which could be the first allocation), the calculated size will exceed cbMaxExtent, and that will be the growth size thereafter.</span></span>

### <a name="requirements"></a><span data-ttu-id="46727-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46727-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46727-159"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="46727-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="46727-160">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="46727-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46727-161"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="46727-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="46727-162">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="46727-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46727-163"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="46727-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="46727-164">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="46727-164">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="46727-165">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="46727-165">See Also</span></span>

[<span data-ttu-id="46727-166">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="46727-166">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="46727-167">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="46727-167">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)
