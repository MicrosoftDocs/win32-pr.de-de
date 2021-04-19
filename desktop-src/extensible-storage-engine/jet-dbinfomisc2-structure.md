---
description: 'Weitere Informationen finden Sie hier: JET_DBINFOMISC2 Struktur'
title: JET_DBINFOMISC2-Struktur
TOCTitle: JET_DBINFOMISC2 Structure
ms:assetid: c62e87ca-c02c-4d6f-a1e6-f80d022c6aad
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294085(v=EXCHG.10)
ms:contentKeyID: 32765700
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
ms.openlocfilehash: 9cf47565a199bd17df47fb6962a1d174454dbe39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346681"
---
# <a name="jet_dbinfomisc2-structure"></a><span data-ttu-id="18853-103">JET_DBINFOMISC2-Struktur</span><span class="sxs-lookup"><span data-stu-id="18853-103">JET_DBINFOMISC2 Structure</span></span>


<span data-ttu-id="18853-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="18853-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfomisc2-structure"></a><span data-ttu-id="18853-105">JET_DBINFOMISC2-Struktur</span><span class="sxs-lookup"><span data-stu-id="18853-105">JET_DBINFOMISC2 Structure</span></span>

<span data-ttu-id="18853-106">Die **JET_DBINFOMISC2** -Struktur enthält verschiedene Informationen zu einer-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="18853-106">The **JET_DBINFOMISC2** structure holds miscellaneous information about a database.</span></span> <span data-ttu-id="18853-107">Dies sind die Informationen, die im Daten Bank Header enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="18853-107">This is the information that is contained in the database header.</span></span>

```cpp
    typedef struct {
      unsigned long ulVersion;
      unsigned long ulUpdate;
      JET_SIGNATURE signDb;
      unsigned long dbstate;
      JET_LGPOS lgposConsistent;
      JET_LOGTIME logtimeConsistent;
      JET_LOGTIME logtimeAttach;
      JET_LGPOS lgposAttach;
      JET_LOGTIME logtimeDetach;
      JET_LGPOS lgposDetach;
      JET_SIGNATURE signLog;
      JET_BKINFO bkinfoFullPrev;
      JET_BKINFO bkinfoIncPrev;
      JET_BKINFO bkinfoFullCur;
      unsigned long fShadowingDisabled;
      unsigned long fUpgradeDb;
      unsigned long dwMajorVersion;
      unsigned long dwMinorVersion;
      unsigned long dwBuildNumber;
      long lSPNumber;
      unsigned long cbPageSize;
      unsigned long genMinRequired;
      unsigned long genMaxRequired;
      JET_LOGTIME logtimeGenMaxCreate;
      unsigned long ulRepairCount;
      JET_LOGTIME logtimeRepair;
      unsigned long ulRepairCountOld;
      unsigned long ulECCFixSuccess;
      JET_LOGTIME logtimeECCFixSuccess;
      unsigned long ulECCFixSuccessOld;
      unsigned long ulECCFixFail;
      JET_LOGTIME logtimeECCFixFail;
      unsigned long ulECCFixFailOld;
      unsigned long ulBadChecksum;
      JET_LOGTIME logtimeBadChecksum;
      unsigned long ulBadChecksumOld;
    } JET_DBINFOMISC2;
```

### <a name="members"></a><span data-ttu-id="18853-108">Member</span><span class="sxs-lookup"><span data-stu-id="18853-108">Members</span></span>

<span data-ttu-id="18853-109">**ulversion**</span><span class="sxs-lookup"><span data-stu-id="18853-109">**ulVersion**</span></span>

<span data-ttu-id="18853-110">Die native Version der Datenbank-Engine, die die Datenbank erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="18853-110">The native version of the database engine that created the database.</span></span> <span data-ttu-id="18853-111">Informationen zum Abrufen der systemeigenen Version für die aktuelle Datenbank-Engine finden Sie unter [jetgetversion](./jetgetversion-function.md) .</span><span class="sxs-lookup"><span data-stu-id="18853-111">See [JetGetVersion](./jetgetversion-function.md) to retrieve the native version for the current database engine.</span></span>

<span data-ttu-id="18853-112">**ulupdate**</span><span class="sxs-lookup"><span data-stu-id="18853-112">**ulUpdate**</span></span>

<span data-ttu-id="18853-113">Verfolgt inkrementelle Datenbankformat Updates, die abwärts kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="18853-113">Tracks incremental database format updates that are backward compatible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18853-114">ulversion, ulupdate =</span><span class="sxs-lookup"><span data-stu-id="18853-114">ulVersion, ulUpdate =</span></span></p></th>
<th><p><span data-ttu-id="18853-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="18853-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18853-116">0x620, 0</span><span class="sxs-lookup"><span data-stu-id="18853-116">0x620,0</span></span></p></td>
<td><p><span data-ttu-id="18853-117">Ursprüngliches Betriebssystem-Beta Format (4/22/97).</span><span class="sxs-lookup"><span data-stu-id="18853-117">Original operating system Beta format (4/22/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18853-118">0x620, 1</span><span class="sxs-lookup"><span data-stu-id="18853-118">0x620,1</span></span></p></td>
<td><p><span data-ttu-id="18853-119">Fügen Sie im Katalog Spalten für die bedingte Indizierung und die alte (5/29/97) hinzu.</span><span class="sxs-lookup"><span data-stu-id="18853-119">Add columns in the catalog for conditional indexing and OLD (5/29/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18853-120">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="18853-120">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="18853-121">Fügen Sie das flocalizedtext-Flag in IDB (6/5/97) hinzu.</span><span class="sxs-lookup"><span data-stu-id="18853-121">Add the fLocalizedText flag in IDB (6/5/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18853-122">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="18853-122">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="18853-123">Fügen Sie den Stamm Seiten der Speicherplatz Struktur SPLIT_BUFFER hinzu (10/30/97).</span><span class="sxs-lookup"><span data-stu-id="18853-123">Add SPLIT_BUFFER to space tree root pages (10/30/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18853-124">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="18853-124">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="18853-125">Revision wiederherstellen, damit ESE97 vorwärts kompatibel bleibt (1/28/98).</span><span class="sxs-lookup"><span data-stu-id="18853-125">Revert revision in order for ESE97 to remain forward-compatible (1/28/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18853-126">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="18853-126">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="18853-127">Fügen Sie dem Katalog neue markierte Spalten hinzu ( &quot; callBackData &quot; und &quot; callbackdependen) &quot; .</span><span class="sxs-lookup"><span data-stu-id="18853-127">Add new tagged columns to catalog (&quot;CallbackData&quot; and &quot;CallbackDependencies&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18853-128">0x620, 4</span><span class="sxs-lookup"><span data-stu-id="18853-128">0x620,4</span></span></p></td>
<td><p><span data-ttu-id="18853-129">SLV-Unterstützung: signslv, fslvvorhanden in DB-Header (5/5/98).</span><span class="sxs-lookup"><span data-stu-id="18853-129">SLV support: signSLV, fSLVExists in db header (5/5/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18853-130">0x620, 5</span><span class="sxs-lookup"><span data-stu-id="18853-130">0x620,5</span></span></p></td>
<td><p><span data-ttu-id="18853-131">Neue SLV-Raumstruktur (5/29/98).</span><span class="sxs-lookup"><span data-stu-id="18853-131">New SLV space tree (5/29/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18853-132">0x620, 6</span><span class="sxs-lookup"><span data-stu-id="18853-132">0x620,6</span></span></p></td>
<td><p><span data-ttu-id="18853-133">SLV-Speicherplatz Zuordnung (10/12/98).</span><span class="sxs-lookup"><span data-stu-id="18853-133">SLV space map (10/12/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18853-134">0x620, 7</span><span class="sxs-lookup"><span data-stu-id="18853-134">0x620,7</span></span></p></td>
<td><p><span data-ttu-id="18853-135">4-Byte-idxsekunden (12/10/98).</span><span class="sxs-lookup"><span data-stu-id="18853-135">4-byte IDXSEG (12/10/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18853-136">0x620, 8</span><span class="sxs-lookup"><span data-stu-id="18853-136">0x620,8</span></span></p></td>
<td><p><span data-ttu-id="18853-137">Neues Vorlagen Spalten Format (1/25/99).</span><span class="sxs-lookup"><span data-stu-id="18853-137">New template column format (1/25/99).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18853-138">0x620, 9</span><span class="sxs-lookup"><span data-stu-id="18853-138">0x620,9</span></span></p></td>
<td><p><span data-ttu-id="18853-139">Sortierte Vorlagen Spalten (6/24/99).</span><span class="sxs-lookup"><span data-stu-id="18853-139">Sorted template columns (6/24/99).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18853-140">0x620, A</span><span class="sxs-lookup"><span data-stu-id="18853-140">0x620,A</span></span></p></td>
<td><p><span data-ttu-id="18853-141">Zusammengeführte Codebasis (3/26/2003).</span><span class="sxs-lookup"><span data-stu-id="18853-141">Merged code base (3/26/2003).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18853-142">0x620, B</span><span class="sxs-lookup"><span data-stu-id="18853-142">0x620,B</span></span></p></td>
<td><p><span data-ttu-id="18853-143">Neues Prüfsummen Format (1/08/2004).</span><span class="sxs-lookup"><span data-stu-id="18853-143">New checksum format (1/08/2004).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18853-144">0x620, C</span><span class="sxs-lookup"><span data-stu-id="18853-144">0x620,C</span></span></p></td>
<td><p><span data-ttu-id="18853-145">Erweiterte maximale Schlüssellänge auf 1000/2000 Bytes für 4/8-KB-Seiten (1/15/2004).</span><span class="sxs-lookup"><span data-stu-id="18853-145">Increased max key length to 1000/2000 bytes for 4/8kb pages (1/15/2004).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18853-146">0x620, D</span><span class="sxs-lookup"><span data-stu-id="18853-146">0x620,D</span></span></p></td>
<td><p><span data-ttu-id="18853-147">Katalog Speicher Hinweise, space_header. v2 (7/15/2007).</span><span class="sxs-lookup"><span data-stu-id="18853-147">Catalog space hints, space_header.v2 (7/15/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18853-148">0x620, E</span><span class="sxs-lookup"><span data-stu-id="18853-148">0x620,E</span></span></p></td>
<td><p><span data-ttu-id="18853-149">Fügen Sie dem Space Manager ein neues Knoten-/Block Format hinzu, und verwenden Sie es für reservierte Speicherplätze (8/9/2007).</span><span class="sxs-lookup"><span data-stu-id="18853-149">Add new node/extent format to space manager, use it for reserved pools of space (8/9/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18853-150">0x620, F</span><span class="sxs-lookup"><span data-stu-id="18853-150">0x620,F</span></span></p></td>
<td><p><span data-ttu-id="18853-151">Komprimierung für systeminterne lange Werte (10/30/2007).</span><span class="sxs-lookup"><span data-stu-id="18853-151">Compression for intrinsic long-values (10/30/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18853-152">0x620, 10</span><span class="sxs-lookup"><span data-stu-id="18853-152">0x620,10</span></span></p></td>
<td><p><span data-ttu-id="18853-153">Komprimierung für getrennte lange Werte (12/05/2007).</span><span class="sxs-lookup"><span data-stu-id="18853-153">Compression for separated long-values (12/05/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18853-154">0x620, 11</span><span class="sxs-lookup"><span data-stu-id="18853-154">0x620,11</span></span></p></td>
<td><p><span data-ttu-id="18853-155">Neue LV-Blockgröße für große Seiten (12/29/2007).</span><span class="sxs-lookup"><span data-stu-id="18853-155">New LV chunk size for large pages (12/29/2007).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="18853-156">**signdb**</span><span class="sxs-lookup"><span data-stu-id="18853-156">**signDb**</span></span>

<span data-ttu-id="18853-157">Signatur der Datenbank (einschließlich Erstellungszeit).</span><span class="sxs-lookup"><span data-stu-id="18853-157">Signature of the database (including creation time).</span></span> <span data-ttu-id="18853-158">Diese Struktur hat 28 bytes.</span><span class="sxs-lookup"><span data-stu-id="18853-158">This structure is 28 bytes.</span></span>

<span data-ttu-id="18853-159">**dbstate**</span><span class="sxs-lookup"><span data-stu-id="18853-159">**dbstate**</span></span>

<span data-ttu-id="18853-160">Dies ist der Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="18853-160">This is the database state.</span></span>

<span data-ttu-id="18853-161">Die folgenden Optionen sind für diesen Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="18853-161">The following options are available for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18853-162">Wert</span><span class="sxs-lookup"><span data-stu-id="18853-162">Value</span></span></p></th>
<th><p><span data-ttu-id="18853-163">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="18853-163">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18853-164">JET_dbstateJustCreated</span><span class="sxs-lookup"><span data-stu-id="18853-164">JET_dbstateJustCreated</span></span><br />
<span data-ttu-id="18853-165">1</span><span class="sxs-lookup"><span data-stu-id="18853-165">1</span></span></p></td>
<td><p><span data-ttu-id="18853-166">Die Datenbank wurde soeben erstellt.</span><span class="sxs-lookup"><span data-stu-id="18853-166">The database was just created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18853-167">JET_dbstateDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="18853-167">JET_dbstateDirtyShutdown</span></span><br />
<span data-ttu-id="18853-168">2</span><span class="sxs-lookup"><span data-stu-id="18853-168">2</span></span></p></td>
<td><p><span data-ttu-id="18853-169">Für die Datenbank muss eine harte oder weiche Wiederherstellung ausgeführt werden, damit Sie verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="18853-169">The database requires hard or soft recovery to be run in order to become usable or moveable.</span></span> <span data-ttu-id="18853-170">Es sollte nicht versucht werden, Datenbanken in diesem Zustand zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="18853-170">One should not try to move databases in this state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18853-171">JET_dbstateCleanShutdown</span><span class="sxs-lookup"><span data-stu-id="18853-171">JET_dbstateCleanShutdown</span></span><br />
<span data-ttu-id="18853-172">3</span><span class="sxs-lookup"><span data-stu-id="18853-172">3</span></span></p></td>
<td><p><span data-ttu-id="18853-173">Die Datenbank befindet sich in einem sauberen Zustand.</span><span class="sxs-lookup"><span data-stu-id="18853-173">The database is in a clean state.</span></span> <span data-ttu-id="18853-174">Die Datenbank kann ohne Protokolldateien angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="18853-174">The database can be attached without any log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18853-175">JET_dbstateBeingConverted</span><span class="sxs-lookup"><span data-stu-id="18853-175">JET_dbstateBeingConverted</span></span><br />
<span data-ttu-id="18853-176">4</span><span class="sxs-lookup"><span data-stu-id="18853-176">4</span></span></p></td>
<td><p><span data-ttu-id="18853-177">Die Datenbank wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="18853-177">The database is being upgraded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18853-178">JET_dbstateForceDetach</span><span class="sxs-lookup"><span data-stu-id="18853-178">JET_dbstateForceDetach</span></span><br />
<span data-ttu-id="18853-179">5</span><span class="sxs-lookup"><span data-stu-id="18853-179">5</span></span></p></td>
<td><p><span data-ttu-id="18853-180">Intern.</span><span class="sxs-lookup"><span data-stu-id="18853-180">Internal.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="18853-181">**lgposkonsistent**</span><span class="sxs-lookup"><span data-stu-id="18853-181">**lgposConsistent**</span></span>

<span data-ttu-id="18853-182">NULL, wenn sich die Datenbank in einem fehlerhaften Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="18853-182">Null if the database is in a dirty state.</span></span> <span data-ttu-id="18853-183">Dies ist die Protokoll Position, die verwendet wurde, als die Datenbank zuletzt in den Zustand "fehlerfreies Herunterfahren" gebracht wurde.</span><span class="sxs-lookup"><span data-stu-id="18853-183">This is the log position that was used when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="18853-184">**logtimekonsistent**</span><span class="sxs-lookup"><span data-stu-id="18853-184">**logtimeConsistent**</span></span>

<span data-ttu-id="18853-185">NULL, wenn sich die Datenbank in einem fehlerhaften Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="18853-185">Null if the database is in a dirty state.</span></span> <span data-ttu-id="18853-186">Dies ist der Zeitpunkt, zu dem die Datenbank zuletzt in den Zustand "sauberes Herunterfahren" versetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="18853-186">This is the time when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="18853-187">**logtimeattach**</span><span class="sxs-lookup"><span data-stu-id="18853-187">**logtimeAttach**</span></span>

<span data-ttu-id="18853-188">Der Zeitpunkt, zu dem die Datenbank zuletzt an [jetattachdatabase](./jetattachdatabase-function.md)angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="18853-188">The time when the database was last attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="18853-189">**lgposattach**</span><span class="sxs-lookup"><span data-stu-id="18853-189">**lgposAttach**</span></span>

<span data-ttu-id="18853-190">Die Protokoll Position, die beim letzten Anfügen der Datenbank mit [jetattachdatabase](./jetattachdatabase-function.md)verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="18853-190">The log position that was used the last time the database was attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="18853-191">**logtimedetach**</span><span class="sxs-lookup"><span data-stu-id="18853-191">**logtimeDetach**</span></span>

<span data-ttu-id="18853-192">Der Zeitpunkt, zu dem die Datenbank zuletzt mit [jetdetachdatabase](./jetdetachdatabase-function.md)getrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="18853-192">The time when the database was last detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="18853-193">**lgposdetach**</span><span class="sxs-lookup"><span data-stu-id="18853-193">**lgposDetach**</span></span>

<span data-ttu-id="18853-194">Die Protokoll Position, die beim letzten Trennen der Datenbank mit [jetdetachdatabase](./jetdetachdatabase-function.md)verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="18853-194">The log position that was used the last time the database was detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="18853-195">**signlog**</span><span class="sxs-lookup"><span data-stu-id="18853-195">**signLog**</span></span>

<span data-ttu-id="18853-196">Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18853-196">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="18853-197">**bkinfofullprev**</span><span class="sxs-lookup"><span data-stu-id="18853-197">**bkinfoFullPrev**</span></span>

<span data-ttu-id="18853-198">Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18853-198">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="18853-199">**bkinfoincprev**</span><span class="sxs-lookup"><span data-stu-id="18853-199">**bkinfoIncPrev**</span></span>

<span data-ttu-id="18853-200">Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18853-200">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="18853-201">**bkinfofullcur**</span><span class="sxs-lookup"><span data-stu-id="18853-201">**bkinfoFullCur**</span></span>

<span data-ttu-id="18853-202">Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18853-202">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="18853-203">**' f ' wingdeaktiviert**</span><span class="sxs-lookup"><span data-stu-id="18853-203">**fShadowingDisabled**</span></span>

<span data-ttu-id="18853-204">Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18853-204">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="18853-205">**FUpgrade DB**</span><span class="sxs-lookup"><span data-stu-id="18853-205">**fUpgradeDb**</span></span>

<span data-ttu-id="18853-206">Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18853-206">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="18853-207">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="18853-207">**dwMajorVersion**</span></span>

<span data-ttu-id="18853-208">Stellt die Windows NT-Versionsnummern beim Aktualisieren der Datenbankindizes dar.</span><span class="sxs-lookup"><span data-stu-id="18853-208">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="18853-209">Wird zum Aktualisieren von Indizes verwendet.</span><span class="sxs-lookup"><span data-stu-id="18853-209">Used for updating indexes.</span></span>

<span data-ttu-id="18853-210">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="18853-210">**dwMinorVersion**</span></span>

<span data-ttu-id="18853-211">Stellt die Windows NT-Versionsnummern beim Aktualisieren der Datenbankindizes dar.</span><span class="sxs-lookup"><span data-stu-id="18853-211">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="18853-212">Wird zum Aktualisieren von Indizes verwendet.</span><span class="sxs-lookup"><span data-stu-id="18853-212">Used for updating indexes.</span></span>

<span data-ttu-id="18853-213">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="18853-213">**dwBuildNumber**</span></span>

<span data-ttu-id="18853-214">Stellt die Windows NT-Versionsnummern beim Aktualisieren der Datenbankindizes dar.</span><span class="sxs-lookup"><span data-stu-id="18853-214">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="18853-215">Wird zum Aktualisieren von Indizes verwendet.</span><span class="sxs-lookup"><span data-stu-id="18853-215">Used for updating indexes.</span></span>

<span data-ttu-id="18853-216">**lspnumber**</span><span class="sxs-lookup"><span data-stu-id="18853-216">**lSPNumber**</span></span>

<span data-ttu-id="18853-217">Stellt die Windows NT-Versionsnummern beim Aktualisieren der Datenbankindizes dar.</span><span class="sxs-lookup"><span data-stu-id="18853-217">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="18853-218">Wird zum Aktualisieren von Indizes verwendet.</span><span class="sxs-lookup"><span data-stu-id="18853-218">Used for updating indexes.</span></span>

<span data-ttu-id="18853-219">**cbpagesize**</span><span class="sxs-lookup"><span data-stu-id="18853-219">**cbPageSize**</span></span>

<span data-ttu-id="18853-220">Größe der Datenbankseite.</span><span class="sxs-lookup"><span data-stu-id="18853-220">Database page size.</span></span> <span data-ttu-id="18853-221">0 bedeutet, dass die Seitengröße 4 KB beträgt.</span><span class="sxs-lookup"><span data-stu-id="18853-221">0 means the page size is 4 KB.</span></span>

<span data-ttu-id="18853-222">Dieser Wert wird nur abgerufen, wenn JET_DbInfoMisc an [jetgetdatabaseingefo](./jetgetdatabaseinfo-function.md) oder [jetgetdatabasefilinput Info](./jetgetdatabasefileinfo-function.md)übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="18853-222">This value is retrieved only if JET_DbInfoMisc was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span>

<span data-ttu-id="18853-223">**genminrequired**</span><span class="sxs-lookup"><span data-stu-id="18853-223">**genMinRequired**</span></span>

<span data-ttu-id="18853-224">Stellt die minimale Protokoll Generierung dar, die für die Wiedergabe der Protokolle erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="18853-224">Represents the minimum log generation required for replaying the logs.</span></span> <span data-ttu-id="18853-225">Dies wird in der Regel als Prüf Punkt Generierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="18853-225">This is typically used as the checkpoint generation.</span></span>

<span data-ttu-id="18853-226">**genmaxrequired**</span><span class="sxs-lookup"><span data-stu-id="18853-226">**genMaxRequired**</span></span>

<span data-ttu-id="18853-227">Stellt die maximale Protokoll Generierung dar, die für die Wiedergabe der Protokolle erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="18853-227">Represents the maximum log generation required for replaying the logs.</span></span>

<span data-ttu-id="18853-228">**logtimegenmaxcreate**</span><span class="sxs-lookup"><span data-stu-id="18853-228">**logtimeGenMaxCreate**</span></span>

<span data-ttu-id="18853-229">Stellt das Erstellungsdatum und den Erstellungs Zeitpunkt der genmax-Protokolldatei dar.</span><span class="sxs-lookup"><span data-stu-id="18853-229">Represents the creation date and time of the genMax log file.</span></span>

<span data-ttu-id="18853-230">**ulrepairren count**</span><span class="sxs-lookup"><span data-stu-id="18853-230">**ulRepairCount**</span></span>

<span data-ttu-id="18853-231">Gibt an, wie oft eine Reparatur für diese Datenbank aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="18853-231">The number of times a repair has been called on this database.</span></span>

<span data-ttu-id="18853-232">**logtimerepair**</span><span class="sxs-lookup"><span data-stu-id="18853-232">**logtimeRepair**</span></span>

<span data-ttu-id="18853-233">Stellt das Datum und die Uhrzeit der letzten Reparatur dar.</span><span class="sxs-lookup"><span data-stu-id="18853-233">Represents the date and time the last repair was run.</span></span>

<span data-ttu-id="18853-234">**ulrepaungräfin**</span><span class="sxs-lookup"><span data-stu-id="18853-234">**ulRepairCountOld**</span></span>

<span data-ttu-id="18853-235">Gibt an, wie oft die Reparatur für diese Datenbank ausgeführt wurde, bevor die letzte Defragmentierung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="18853-235">The number of times the repair had been run on this database before the last defragmentation.</span></span>

<span data-ttu-id="18853-236">**uleccfixsuccess**</span><span class="sxs-lookup"><span data-stu-id="18853-236">**ulECCFixSuccess**</span></span>

<span data-ttu-id="18853-237">Gibt an, wie oft ein einziger Bitfehler korrigiert wurde und zu einer guten Seite geführt hat.</span><span class="sxs-lookup"><span data-stu-id="18853-237">The number of times a one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="18853-238">**logtimeeccfixsuccess**</span><span class="sxs-lookup"><span data-stu-id="18853-238">**logtimeECCFixSuccess**</span></span>

<span data-ttu-id="18853-239">Stellt das Datum und die Uhrzeit dar, zu der der letzte Bitfehler korrigiert wurde, und führte zu einer guten Seite.</span><span class="sxs-lookup"><span data-stu-id="18853-239">Represents the date and time the last one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="18853-240">**uleccfixerfolgreiches verkauft**</span><span class="sxs-lookup"><span data-stu-id="18853-240">**ulECCFixSuccessOld**</span></span>

<span data-ttu-id="18853-241">Stellt die Häufigkeit dar, mit der ein einzelnes Bitfehler behoben wurde und zu einer guten Seite vor der letzten Reparatur geführt hat.</span><span class="sxs-lookup"><span data-stu-id="18853-241">Represents the number of times a one bit error was fixed and resulted in a good page before last repair.</span></span>

<span data-ttu-id="18853-242">**uleccfixfail**</span><span class="sxs-lookup"><span data-stu-id="18853-242">**ulECCFixFail**</span></span>

<span data-ttu-id="18853-243">Gibt an, wie oft ein einziger Bitfehler korrigiert wurde und zu einer ungültigen Seite geführt hat.</span><span class="sxs-lookup"><span data-stu-id="18853-243">The number of times a one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="18853-244">**logtimeeccfixfail**</span><span class="sxs-lookup"><span data-stu-id="18853-244">**logtimeECCFixFail**</span></span>

<span data-ttu-id="18853-245">Stellt das Datum und die Uhrzeit dar, zu der der letzte Bitfehler korrigiert wurde, und führte zu einer ungültigen Seite.</span><span class="sxs-lookup"><span data-stu-id="18853-245">Represents the date and time the last one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="18853-246">**uleccfixfailold**</span><span class="sxs-lookup"><span data-stu-id="18853-246">**ulECCFixFailOld**</span></span>

<span data-ttu-id="18853-247">Gibt an, wie oft ein ein-Bit-Fehler korrigiert wurde und zu einer ungültigen Seite vor der letzten Reparatur geführt hat.</span><span class="sxs-lookup"><span data-stu-id="18853-247">The number of times a one bit error was fixed and resulted in a bad page before last repair.</span></span>

<span data-ttu-id="18853-248">**ulbadchecksum**</span><span class="sxs-lookup"><span data-stu-id="18853-248">**ulBadChecksum**</span></span>

<span data-ttu-id="18853-249">Gibt an, wie oft ein nicht korrigier barer ECC/Checksum-Fehler gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="18853-249">The number of times a non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="18853-250">**logtimebadchecksum**</span><span class="sxs-lookup"><span data-stu-id="18853-250">**logtimeBadChecksum**</span></span>

<span data-ttu-id="18853-251">Stellt das Datum und die Uhrzeit des letzten nicht korrigierbaren ECC/Checksum-Fehlers dar.</span><span class="sxs-lookup"><span data-stu-id="18853-251">Represents the date and time the last non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="18853-252">**ulbadchecksumold**</span><span class="sxs-lookup"><span data-stu-id="18853-252">**ulBadChecksumOld**</span></span>

<span data-ttu-id="18853-253">Gibt an, wie oft ein nicht korrigier barer ECC/Checksum-Fehler vor der letzten Reparatur gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="18853-253">The number of times a non-correctable ECC/checksum error was found before last repair.</span></span>

### <a name="requirements"></a><span data-ttu-id="18853-254">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18853-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18853-255"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="18853-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="18853-256">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="18853-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18853-257"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="18853-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="18853-258">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="18853-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18853-259"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="18853-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="18853-260">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="18853-260">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="18853-261">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="18853-261">See Also</span></span>

[<span data-ttu-id="18853-262">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="18853-262">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="18853-263">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="18853-263">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="18853-264">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="18853-264">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="18853-265">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="18853-265">JET_SIGNATURE</span></span>](./jet-signature-structure.md)  
[<span data-ttu-id="18853-266">Jetgetdatabaseingefo</span><span class="sxs-lookup"><span data-stu-id="18853-266">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)  
[<span data-ttu-id="18853-267">Jetgetdatabasefileingefo</span><span class="sxs-lookup"><span data-stu-id="18853-267">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
