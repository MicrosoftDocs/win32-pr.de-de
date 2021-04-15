---
description: 'Weitere Informationen finden Sie hier: JET_DBINFOMISC Struktur'
title: JET_DBINFOMISC-Struktur
TOCTitle: JET_DBINFOMISC Structure
ms:assetid: ff287087-35b8-495e-9922-418ec2439e19
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294147(v=EXCHG.10)
ms:contentKeyID: 32765761
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 649e16e956e5dcd272e6201f779cdddd352a7bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525052"
---
# <a name="jet_dbinfomisc-structure"></a><span data-ttu-id="60d79-103">JET_DBINFOMISC-Struktur</span><span class="sxs-lookup"><span data-stu-id="60d79-103">JET_DBINFOMISC Structure</span></span>


<span data-ttu-id="60d79-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="60d79-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfomisc-structure"></a><span data-ttu-id="60d79-105">JET_DBINFOMISC-Struktur</span><span class="sxs-lookup"><span data-stu-id="60d79-105">JET_DBINFOMISC Structure</span></span>

<span data-ttu-id="60d79-106">Die **JET_DBINFOMISC** -Struktur enthält verschiedene Informationen zu einer-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="60d79-106">The **JET_DBINFOMISC** structure holds miscellaneous information about a database.</span></span> <span data-ttu-id="60d79-107">Dies sind die Informationen, die im Daten Bank Header enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="60d79-107">This is the information that is contained in the database header.</span></span>

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
    } JET_DBINFOMISC;
```

### <a name="members"></a><span data-ttu-id="60d79-108">Member</span><span class="sxs-lookup"><span data-stu-id="60d79-108">Members</span></span>

<span data-ttu-id="60d79-109">**ulversion**</span><span class="sxs-lookup"><span data-stu-id="60d79-109">**ulVersion**</span></span>

<span data-ttu-id="60d79-110">Die native Version der Datenbank-Engine, die die Datenbank erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="60d79-110">The native version of the database engine that created the database.</span></span> <span data-ttu-id="60d79-111">Informationen zum Abrufen der systemeigenen Version für die aktuelle Datenbank-Engine finden Sie unter [jetgetversion](./jetgetversion-function.md) .</span><span class="sxs-lookup"><span data-stu-id="60d79-111">See [JetGetVersion](./jetgetversion-function.md) to retrieve the native version for the current database engine.</span></span>

<span data-ttu-id="60d79-112">**ulupdate**</span><span class="sxs-lookup"><span data-stu-id="60d79-112">**ulUpdate**</span></span>

<span data-ttu-id="60d79-113">Verfolgt inkrementelle Datenbankformat Updates, die abwärts kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="60d79-113">Tracks incremental database format updates that are backward compatible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60d79-114">ulversion, ulupdate =</span><span class="sxs-lookup"><span data-stu-id="60d79-114">ulVersion, ulUpdate =</span></span></p></th>
<th><p><span data-ttu-id="60d79-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="60d79-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60d79-116">0x620, 0</span><span class="sxs-lookup"><span data-stu-id="60d79-116">0x620,0</span></span></p></td>
<td><p><span data-ttu-id="60d79-117">Ursprüngliches Betriebssystem-Beta Format (4/22/97).</span><span class="sxs-lookup"><span data-stu-id="60d79-117">Original operating system Beta format (4/22/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d79-118">0x620, 1</span><span class="sxs-lookup"><span data-stu-id="60d79-118">0x620,1</span></span></p></td>
<td><p><span data-ttu-id="60d79-119">Fügen Sie im Katalog Spalten für die bedingte Indizierung und die alte (5/29/97) hinzu.</span><span class="sxs-lookup"><span data-stu-id="60d79-119">Add columns in the catalog for conditional indexing and OLD (5/29/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d79-120">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="60d79-120">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="60d79-121">Fügen Sie das flocalizedtext-Flag in IDB (6/5/97) hinzu.</span><span class="sxs-lookup"><span data-stu-id="60d79-121">Add the fLocalizedText flag in IDB (6/5/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d79-122">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="60d79-122">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="60d79-123">Fügen Sie den Stamm Seiten der Speicherplatz Struktur SPLIT_BUFFER hinzu (10/30/97).</span><span class="sxs-lookup"><span data-stu-id="60d79-123">Add SPLIT_BUFFER to space tree root pages (10/30/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d79-124">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="60d79-124">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="60d79-125">Revision wiederherstellen, damit ESE97 vorwärts kompatibel bleibt (1/28/98).</span><span class="sxs-lookup"><span data-stu-id="60d79-125">Revert revision in order for ESE97 to remain forward-compatible (1/28/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d79-126">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="60d79-126">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="60d79-127">Fügen Sie dem Katalog neue markierte Spalten hinzu ( &quot; callBackData &quot; und &quot; callbackdependen) &quot; .</span><span class="sxs-lookup"><span data-stu-id="60d79-127">Add new tagged columns to catalog (&quot;CallbackData&quot; and &quot;CallbackDependencies&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d79-128">0x620, 4</span><span class="sxs-lookup"><span data-stu-id="60d79-128">0x620,4</span></span></p></td>
<td><p><span data-ttu-id="60d79-129">SLV-Unterstützung: signslv, fslvvorhanden in DB-Header (5/5/98).</span><span class="sxs-lookup"><span data-stu-id="60d79-129">SLV support: signSLV, fSLVExists in db header (5/5/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d79-130">0x620, 5</span><span class="sxs-lookup"><span data-stu-id="60d79-130">0x620,5</span></span></p></td>
<td><p><span data-ttu-id="60d79-131">Neue SLV-Raumstruktur (5/29/98).</span><span class="sxs-lookup"><span data-stu-id="60d79-131">New SLV space tree (5/29/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d79-132">0x620, 6</span><span class="sxs-lookup"><span data-stu-id="60d79-132">0x620,6</span></span></p></td>
<td><p><span data-ttu-id="60d79-133">SLV-Speicherplatz Zuordnung (10/12/98).</span><span class="sxs-lookup"><span data-stu-id="60d79-133">SLV space map (10/12/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d79-134">0x620, 7</span><span class="sxs-lookup"><span data-stu-id="60d79-134">0x620,7</span></span></p></td>
<td><p><span data-ttu-id="60d79-135">4-Byte-idxsekunden (12/10/98).</span><span class="sxs-lookup"><span data-stu-id="60d79-135">4-byte IDXSEG (12/10/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d79-136">0x620, 8</span><span class="sxs-lookup"><span data-stu-id="60d79-136">0x620,8</span></span></p></td>
<td><p><span data-ttu-id="60d79-137">Neues Vorlagen Spalten Format (1/25/99).</span><span class="sxs-lookup"><span data-stu-id="60d79-137">New template column format (1/25/99).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d79-138">0x620, 9</span><span class="sxs-lookup"><span data-stu-id="60d79-138">0x620,9</span></span></p></td>
<td><p><span data-ttu-id="60d79-139">Sortierte Vorlagen Spalten (6/24/99).</span><span class="sxs-lookup"><span data-stu-id="60d79-139">Sorted template columns (6/24/99).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d79-140">0x623, 0</span><span class="sxs-lookup"><span data-stu-id="60d79-140">0x623,0</span></span></p></td>
<td><p><span data-ttu-id="60d79-141">Neuer Speicherplatz-Manager (5/15/99).</span><span class="sxs-lookup"><span data-stu-id="60d79-141">New Space Manager (5/15/99).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="60d79-142">**signdb**</span><span class="sxs-lookup"><span data-stu-id="60d79-142">**signDb**</span></span>

<span data-ttu-id="60d79-143">Signatur der Datenbank (einschließlich Erstellungszeit).</span><span class="sxs-lookup"><span data-stu-id="60d79-143">Signature of the database (including creation time).</span></span> <span data-ttu-id="60d79-144">Diese Struktur hat 28 bytes.</span><span class="sxs-lookup"><span data-stu-id="60d79-144">This structure is 28 bytes.</span></span>

<span data-ttu-id="60d79-145">**dbstate**</span><span class="sxs-lookup"><span data-stu-id="60d79-145">**dbstate**</span></span>

<span data-ttu-id="60d79-146">Dies ist der Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="60d79-146">This is the database state.</span></span>

<span data-ttu-id="60d79-147">Die folgenden Optionen sind für diesen Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="60d79-147">The following options are available for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60d79-148">Wert</span><span class="sxs-lookup"><span data-stu-id="60d79-148">Value</span></span></p></th>
<th><p><span data-ttu-id="60d79-149">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="60d79-149">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60d79-150">JET_dbstateJustCreated</span><span class="sxs-lookup"><span data-stu-id="60d79-150">JET_dbstateJustCreated</span></span><br />
<span data-ttu-id="60d79-151">1</span><span class="sxs-lookup"><span data-stu-id="60d79-151">1</span></span></p></td>
<td><p><span data-ttu-id="60d79-152">Die Datenbank wurde soeben erstellt.</span><span class="sxs-lookup"><span data-stu-id="60d79-152">The database was just created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d79-153">JET_dbstateDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="60d79-153">JET_dbstateDirtyShutdown</span></span><br />
<span data-ttu-id="60d79-154">2</span><span class="sxs-lookup"><span data-stu-id="60d79-154">2</span></span></p></td>
<td><p><span data-ttu-id="60d79-155">Für die Datenbank muss eine harte oder weiche Wiederherstellung ausgeführt werden, damit Sie verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="60d79-155">The database requires hard or soft recovery to be run in order to become usable or moveable.</span></span> <span data-ttu-id="60d79-156">Es sollte nicht versucht werden, Datenbanken in diesem Zustand zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="60d79-156">One should not try to move databases in this state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d79-157">JET_dbstateCleanShutdown</span><span class="sxs-lookup"><span data-stu-id="60d79-157">JET_dbstateCleanShutdown</span></span><br />
<span data-ttu-id="60d79-158">3</span><span class="sxs-lookup"><span data-stu-id="60d79-158">3</span></span></p></td>
<td><p><span data-ttu-id="60d79-159">Die Datenbank befindet sich in einem sauberen Zustand.</span><span class="sxs-lookup"><span data-stu-id="60d79-159">The database is in a clean state.</span></span> <span data-ttu-id="60d79-160">Die Datenbank kann ohne Protokolldateien angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="60d79-160">The database can be attached without any log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d79-161">JET_dbstateBeingConverted</span><span class="sxs-lookup"><span data-stu-id="60d79-161">JET_dbstateBeingConverted</span></span><br />
<span data-ttu-id="60d79-162">4</span><span class="sxs-lookup"><span data-stu-id="60d79-162">4</span></span></p></td>
<td><p><span data-ttu-id="60d79-163">Die Datenbank wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="60d79-163">The database is being upgraded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d79-164">JET_dbstateForceDetach</span><span class="sxs-lookup"><span data-stu-id="60d79-164">JET_dbstateForceDetach</span></span><br />
<span data-ttu-id="60d79-165">5</span><span class="sxs-lookup"><span data-stu-id="60d79-165">5</span></span></p></td>
<td><p><span data-ttu-id="60d79-166">Intern.</span><span class="sxs-lookup"><span data-stu-id="60d79-166">Internal.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="60d79-167">**lgposkonsistent**</span><span class="sxs-lookup"><span data-stu-id="60d79-167">**lgposConsistent**</span></span>

<span data-ttu-id="60d79-168">NULL, wenn sich die Datenbank in einem fehlerhaften Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="60d79-168">Null if the database is in a dirty state.</span></span> <span data-ttu-id="60d79-169">Dies ist die Protokoll Position, die verwendet wurde, als die Datenbank zuletzt in den Zustand "fehlerfreies Herunterfahren" gebracht wurde.</span><span class="sxs-lookup"><span data-stu-id="60d79-169">This is the log position that was used when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="60d79-170">**logtimekonsistent**</span><span class="sxs-lookup"><span data-stu-id="60d79-170">**logtimeConsistent**</span></span>

<span data-ttu-id="60d79-171">NULL, wenn sich die Datenbank in einem fehlerhaften Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="60d79-171">Null if the database is in a dirty state.</span></span> <span data-ttu-id="60d79-172">Dies ist der Zeitpunkt, zu dem die Datenbank zuletzt in den Zustand "sauberes Herunterfahren" versetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="60d79-172">This is the time when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="60d79-173">**logtimeattach**</span><span class="sxs-lookup"><span data-stu-id="60d79-173">**logtimeAttach**</span></span>

<span data-ttu-id="60d79-174">Der Zeitpunkt, zu dem die Datenbank zuletzt an [jetattachdatabase](./jetattachdatabase-function.md)angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="60d79-174">The time when the database was last attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="60d79-175">**lgposattach**</span><span class="sxs-lookup"><span data-stu-id="60d79-175">**lgposAttach**</span></span>

<span data-ttu-id="60d79-176">Die Protokoll Position, die beim letzten Anfügen der Datenbank mit [jetattachdatabase](./jetattachdatabase-function.md)verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="60d79-176">The log position that was used the last time the database was attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="60d79-177">**logtimedetach**</span><span class="sxs-lookup"><span data-stu-id="60d79-177">**logtimeDetach**</span></span>

<span data-ttu-id="60d79-178">Der Zeitpunkt, zu dem die Datenbank zuletzt mit [jetdetachdatabase](./jetdetachdatabase-function.md)getrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="60d79-178">The time when the database was last detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="60d79-179">**lgposdetach**</span><span class="sxs-lookup"><span data-stu-id="60d79-179">**lgposDetach**</span></span>

<span data-ttu-id="60d79-180">Die Protokoll Position, die beim letzten Trennen der Datenbank mit [jetdetachdatabase](./jetdetachdatabase-function.md)verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="60d79-180">The log position that was used the last time the database was detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="60d79-181">**signlog**</span><span class="sxs-lookup"><span data-stu-id="60d79-181">**signLog**</span></span>

<span data-ttu-id="60d79-182">Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60d79-182">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="60d79-183">**bkinfofullprev**</span><span class="sxs-lookup"><span data-stu-id="60d79-183">**bkinfoFullPrev**</span></span>

<span data-ttu-id="60d79-184">Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60d79-184">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="60d79-185">**bkinfoincprev**</span><span class="sxs-lookup"><span data-stu-id="60d79-185">**bkinfoIncPrev**</span></span>

<span data-ttu-id="60d79-186">Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60d79-186">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="60d79-187">**bkinfofullcur**</span><span class="sxs-lookup"><span data-stu-id="60d79-187">**bkinfoFullCur**</span></span>

<span data-ttu-id="60d79-188">Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60d79-188">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="60d79-189">**' f ' wingdeaktiviert**</span><span class="sxs-lookup"><span data-stu-id="60d79-189">**fShadowingDisabled**</span></span>

<span data-ttu-id="60d79-190">Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60d79-190">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="60d79-191">**FUpgrade DB**</span><span class="sxs-lookup"><span data-stu-id="60d79-191">**fUpgradeDb**</span></span>

<span data-ttu-id="60d79-192">Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60d79-192">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="60d79-193">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="60d79-193">**dwMajorVersion**</span></span>

<span data-ttu-id="60d79-194">Stellt die Windows NT-Versionsnummern beim Aktualisieren der Datenbankindizes dar.</span><span class="sxs-lookup"><span data-stu-id="60d79-194">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="60d79-195">Wird zum Aktualisieren von Indizes verwendet.</span><span class="sxs-lookup"><span data-stu-id="60d79-195">Used for updating indexes.</span></span>

<span data-ttu-id="60d79-196">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="60d79-196">**dwMinorVersion**</span></span>

<span data-ttu-id="60d79-197">Stellt die Windows NT-Versionsnummern beim Aktualisieren der Datenbankindizes dar.</span><span class="sxs-lookup"><span data-stu-id="60d79-197">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="60d79-198">Wird zum Aktualisieren von Indizes verwendet.</span><span class="sxs-lookup"><span data-stu-id="60d79-198">Used for updating indexes.</span></span>

<span data-ttu-id="60d79-199">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="60d79-199">**dwBuildNumber**</span></span>

<span data-ttu-id="60d79-200">Stellt die Windows NT-Versionsnummern beim Aktualisieren der Datenbankindizes dar.</span><span class="sxs-lookup"><span data-stu-id="60d79-200">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="60d79-201">Wird zum Aktualisieren von Indizes verwendet.</span><span class="sxs-lookup"><span data-stu-id="60d79-201">Used for updating indexes.</span></span>

<span data-ttu-id="60d79-202">**lspnumber**</span><span class="sxs-lookup"><span data-stu-id="60d79-202">**lSPNumber**</span></span>

<span data-ttu-id="60d79-203">Stellt die Windows NT-Versionsnummern beim Aktualisieren der Datenbankindizes dar.</span><span class="sxs-lookup"><span data-stu-id="60d79-203">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="60d79-204">Wird zum Aktualisieren von Indizes verwendet.</span><span class="sxs-lookup"><span data-stu-id="60d79-204">Used for updating indexes.</span></span>

<span data-ttu-id="60d79-205">**cbpagesize**</span><span class="sxs-lookup"><span data-stu-id="60d79-205">**cbPageSize**</span></span>

<span data-ttu-id="60d79-206">Größe der Datenbankseite.</span><span class="sxs-lookup"><span data-stu-id="60d79-206">Database page size.</span></span> <span data-ttu-id="60d79-207">0 bedeutet, dass die Seitengröße 4 KB beträgt.</span><span class="sxs-lookup"><span data-stu-id="60d79-207">0 means the page size is 4 KB.</span></span>

<span data-ttu-id="60d79-208">Dieser Wert wird nur abgerufen, wenn JET_DbInfoMisc an [jetgetdatabaseingefo](./jetgetdatabaseinfo-function.md) oder [jetgetdatabasefilinput Info](./jetgetdatabasefileinfo-function.md)übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="60d79-208">This value is retrieved only if JET_DbInfoMisc was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="60d79-209">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60d79-209">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60d79-210"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="60d79-210"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="60d79-211">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="60d79-211">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d79-212"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="60d79-212"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="60d79-213">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="60d79-213">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d79-214"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="60d79-214"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="60d79-215">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="60d79-215">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="60d79-216">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="60d79-216">See Also</span></span>

[<span data-ttu-id="60d79-217">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="60d79-217">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="60d79-218">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="60d79-218">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="60d79-219">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="60d79-219">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="60d79-220">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="60d79-220">JET_SIGNATURE</span></span>](./jet-signature-structure.md)  
[<span data-ttu-id="60d79-221">Jetgetdatabaseingefo</span><span class="sxs-lookup"><span data-stu-id="60d79-221">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)  
[<span data-ttu-id="60d79-222">Jetgetdatabasefileingefo</span><span class="sxs-lookup"><span data-stu-id="60d79-222">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
