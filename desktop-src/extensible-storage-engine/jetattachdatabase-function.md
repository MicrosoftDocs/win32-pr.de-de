---
description: 'Weitere Informationen zu: jetattachdatabase-Funktion'
title: JetAttachDatabase-Funktion
TOCTitle: JetAttachDatabase Function
ms:assetid: bc4c9a76-203c-424a-ac17-f096e3a6e04e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294074(v=EXCHG.10)
ms:contentKeyID: 32765689
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase
- JetAttachDatabaseW
- JetAttachDatabaseA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5968fe7906ace720dad3f94e278f37d992710d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214385"
---
# <a name="jetattachdatabase-function"></a><span data-ttu-id="b2131-103">JetAttachDatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="b2131-103">JetAttachDatabase Function</span></span>


<span data-ttu-id="b2131-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b2131-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetattachdatabase-function"></a><span data-ttu-id="b2131-105">JetAttachDatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="b2131-105">JetAttachDatabase Function</span></span>

<span data-ttu-id="b2131-106">Die **jetattachdatabase** -Funktion fügt eine Datenbankdatei für die Verwendung mit einer Daten Bank Instanz an.</span><span class="sxs-lookup"><span data-stu-id="b2131-106">The **JetAttachDatabase** function attaches a database file for use with a database instance.</span></span> <span data-ttu-id="b2131-107">Damit die Datenbank verwendet werden kann, muss Sie anschließend mit [jetopend Database](./jetopendatabase-function.md)geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="b2131-107">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="b2131-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2131-108">Parameters</span></span>

<span data-ttu-id="b2131-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="b2131-109">*sesid*</span></span>

<span data-ttu-id="b2131-110">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="b2131-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="b2131-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="b2131-111">*szFilename*</span></span>

<span data-ttu-id="b2131-112">Der Name der anzufügenden Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b2131-112">The name of the database to attach.</span></span>

<span data-ttu-id="b2131-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b2131-113">*grbit*</span></span>

<span data-ttu-id="b2131-114">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angeben.</span><span class="sxs-lookup"><span data-stu-id="b2131-114">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b2131-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b2131-115">Value</span></span></p></th>
<th><p><span data-ttu-id="b2131-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b2131-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2131-117">JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="b2131-117">JET_bitDbDeleteCorruptIndexes</span></span></p></td>
<td><p><span data-ttu-id="b2131-118">Wenn <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> festgelegt wurde, werden alle Indizes für Unicode-Daten gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b2131-118">If <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> has been set, all indexes over Unicode data will be deleted.</span></span> <span data-ttu-id="b2131-119">Weitere Details finden Sie im Abschnitt „Anmerkungen“.</span><span class="sxs-lookup"><span data-stu-id="b2131-119">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2131-120">JET_bitDbDeleteUnicodeIndexes</span><span class="sxs-lookup"><span data-stu-id="b2131-120">JET_bitDbDeleteUnicodeIndexes</span></span></p></td>
<td><p><span data-ttu-id="b2131-121">Alle Indizes für Unicode-Daten werden unabhängig von der Einstellung <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b2131-121">All indexes over Unicode data will be deleted, regardless of the setting of <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span></span> <span data-ttu-id="b2131-122">Weitere Details finden Sie im Abschnitt „Anmerkungen“.</span><span class="sxs-lookup"><span data-stu-id="b2131-122">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2131-123">JET_bitDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="b2131-123">JET_bitDbUpgrade</span></span></p></td>
<td><p><span data-ttu-id="b2131-124">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b2131-124">Obsolete.</span></span> <span data-ttu-id="b2131-125">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2131-125">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2131-126">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="b2131-126">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="b2131-127">Verhindert Änderungen an der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b2131-127">Prevents modifications to the database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="b2131-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2131-128">Return Value</span></span>

<span data-ttu-id="b2131-129">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="b2131-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b2131-130">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b2131-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b2131-131">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b2131-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="b2131-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2131-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2131-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b2131-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b2131-134">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b2131-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2131-135">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="b2131-135">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="b2131-136">Das Anfügen einer Datenbank ist während einer Sicherung nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="b2131-136">Attaching a database is not allowed during a backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2131-137">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="b2131-137">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="b2131-138">Die von <em>szFilename</em> angegebene Datenbankdatei muss beschreibbar sein.</span><span class="sxs-lookup"><span data-stu-id="b2131-138">The database file specified by <em>szFilename</em> must be writable.</span></span> <span data-ttu-id="b2131-139">Das Read-Only-Attribut darf nicht festgelegt werden, und der laufende Prozess muss über ausreichende Berechtigungen zum Schreiben in die Datei verfügen.</span><span class="sxs-lookup"><span data-stu-id="b2131-139">The Read-Only attribute must not be set, and the running process must have sufficient privileges to write to the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2131-140">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="b2131-140">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="b2131-141">Die Datenbankdatei wurde bereits von einem anderen Prozess geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b2131-141">The database file is already opened by another process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2131-142">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="b2131-142">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="b2131-143">In " <em>szFilename</em>" wurde ein ungültiger Pfad angegeben.</span><span class="sxs-lookup"><span data-stu-id="b2131-143">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="b2131-144">" <em>szFilename</em> " darf nicht NULL sein und verweist auf einen gültigen Pfad.</span><span class="sxs-lookup"><span data-stu-id="b2131-144"><em>szFilename</em> must be non-NULL and refer to a valid path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2131-145">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="b2131-145">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="b2131-146">Die Datenbankdatei wurde bereits durch eine andere Sitzung angefügt.</span><span class="sxs-lookup"><span data-stu-id="b2131-146">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2131-147">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="b2131-147">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="b2131-148">Die Datenbank-Engine kann die Datenbankdatei nicht öffnen.</span><span class="sxs-lookup"><span data-stu-id="b2131-148">The database engine cannot open the database file.</span></span> <span data-ttu-id="b2131-149">Die Datei wird möglicherweise von einem anderen Prozess verwendet, oder der Aufrufer verfügt möglicherweise nicht über ausreichende Berechtigungen zum Öffnen der Datei.</span><span class="sxs-lookup"><span data-stu-id="b2131-149">The file may be in use by another process or the caller may not have sufficient privileges to open the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2131-150">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="b2131-150">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="b2131-151">Die in <em>szFilename</em> angegebene Datei ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b2131-151">The file given in <em>szFilename</em> does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2131-152">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="b2131-152">JET_errPrimaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="b2131-153">Fehler beim primären Index.</span><span class="sxs-lookup"><span data-stu-id="b2131-153">There is an error with the primary index.</span></span> <span data-ttu-id="b2131-154">Dies kann von physischer Beschädigung (z. b. Datenträger-oder Speicher Beschädigung) verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="b2131-154">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="b2131-155">Sie kann auch zurückgegeben werden, wenn eine Datenbank zuletzt an einem älteren Betriebssystem geändert wird und der primäre Index eine Spalte mit Unicode-Daten ist.</span><span class="sxs-lookup"><span data-stu-id="b2131-155">It may also be returned when attaching a database last modified on an older operating system and the primary index is over a column with Unicode data.</span></span> <span data-ttu-id="b2131-156">Weitere Informationen zu Indizes für Unicode-Daten finden Sie in den hinweisen.</span><span class="sxs-lookup"><span data-stu-id="b2131-156">See the remarks for more information on indexes over Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2131-157">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="b2131-157">JET_errSecondaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="b2131-158">Es ist ein Fehler mit einem sekundären Index aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b2131-158">There is an error with a secondary index.</span></span> <span data-ttu-id="b2131-159">Dies kann von physischer Beschädigung (z. b. Datenträger-oder Speicher Beschädigung) verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="b2131-159">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="b2131-160">Sie kann auch zurückgegeben werden, wenn eine Datenbank zuletzt an einem älteren Betriebssystem geändert und ein sekundärer Index über eine Spalte mit Unicode-Daten verfügt.</span><span class="sxs-lookup"><span data-stu-id="b2131-160">It may also be returned when attaching a database last modified on an older operating system and a secondary index is over a column with Unicode data.</span></span> <span data-ttu-id="b2131-161">Weitere Informationen zu Indizes für Unicode-Daten finden Sie in den hinweisen.</span><span class="sxs-lookup"><span data-stu-id="b2131-161">See the remarks for more information on indexes over Unicode data.</span></span> <span data-ttu-id="b2131-162">Sekundäre Indizes werden vollständig neu erstellt, wenn eine Datenbank mit einem Offline-Hilfsprogramm mit folgendem Befehl ( <strong>Esentutl-d</strong>) zerlegt wird.</span><span class="sxs-lookup"><span data-stu-id="b2131-162">Secondary indexes are completely rebuilt when a database is defragmented with an offline utility using the following command: <strong>esentutl -d</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2131-163">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="b2131-163">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="b2131-164">Pro Instanz kann nur eine endliche Anzahl von Datenbanken angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b2131-164">Only a finite number of databases can be attached per instance.</span></span> <span data-ttu-id="b2131-165">Das Limit beträgt derzeit sieben Datenbanken pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="b2131-165">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2131-166">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="b2131-166">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="b2131-167">Eine nicht schwerwiegende Warnung, die angibt, dass die Datenbankdatei bereits von dieser Sitzung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b2131-167">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="b2131-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2131-168">Remarks</span></span>

<span data-ttu-id="b2131-169">Der Aufruf von **jetattachdatabase** entspricht dem Aufrufen von [JetAttachDatabase2](./jetattachdatabase2-function.md) und dem übergeben des Werts 0 (null), d. h. es gibt keine Begrenzung für den *cpgdatabasesizemax* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="b2131-169">Calling **JetAttachDatabase** is equivalent to calling [JetAttachDatabase2](./jetattachdatabase2-function.md) and passing a value of zero, meaning there is no limit, for the *cpgDatabaseSizeMax* parameter.</span></span>

<span data-ttu-id="b2131-170">Wenn Sie eine beschreibbare Datenbank anfügen (d. h., wenn JET_bitDbReadOnly nicht im *grbit* -Parameter angegeben wurde), wird die Datei exklusiv auf Betriebssystemebene geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b2131-170">Attaching a writable database (that is, if JET_bitDbReadOnly was not specified in the *grbit* parameter) will open the file exclusively at the operating system level.</span></span> <span data-ttu-id="b2131-171">Ein anderer Prozess kann die Datei nicht öffnen.</span><span class="sxs-lookup"><span data-stu-id="b2131-171">No other process will be able open the file.</span></span> <span data-ttu-id="b2131-172">Es ist möglich, dass mehrere Prozesse eine einzelne Datenbank anfügen, indem Sie Sie im schreibgeschützten Modus öffnen.</span><span class="sxs-lookup"><span data-stu-id="b2131-172">It is possible for multiple processes to attach a single database by opening them in read-only mode.</span></span>

<span data-ttu-id="b2131-173">Die Datenbankdatei wird mithilfe von [jetdetachdatabase](./jetdetachdatabase-function.md) oder [JetDetachDatabase2](./jetdetachdatabase2-function.md)getrennt.</span><span class="sxs-lookup"><span data-stu-id="b2131-173">The database file is detached using [JetDetachDatabase](./jetdetachdatabase-function.md) or [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span></span>

<span data-ttu-id="b2131-174">Parameter für die Index Überprüfung</span><span class="sxs-lookup"><span data-stu-id="b2131-174">Index-checking parameters</span></span>

<span data-ttu-id="b2131-175">Verschiedene Versionen von Windows normalisieren Unicode-Text auf unterschiedliche Weise.</span><span class="sxs-lookup"><span data-stu-id="b2131-175">Different versions of Windows normalize Unicode text in different ways.</span></span> <span data-ttu-id="b2131-176">Dies bedeutet, dass Indizes, die unter einer Windows-Version erstellt wurden, in anderen Versionen möglicherweise nicht funktionieren.</span><span class="sxs-lookup"><span data-stu-id="b2131-176">That means indexes built under one version of Windows may not work on other versions.</span></span>

<span data-ttu-id="b2131-177">Vor Windows Server 2003, bei Änderung der Betriebssystemversion (einschließlich der Installation eines Service Packs), war jeder Index über Unicode-Daten möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="b2131-177">Prior to Windows Server 2003, when the operating system version changed (including installation of a Service Pack), every index over Unicode data was in a potentially corrupt state.</span></span>

<span data-ttu-id="b2131-178">Indizes, die in Windows Server 2003 und höher erstellt wurden, werden mit der Version der Unicode-Normalisierung gekennzeichnet, mit der Sie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b2131-178">Indexes created in Windows Server 2003 and later are flagged with the version of Unicode normalization with which they were built.</span></span> <span data-ttu-id="b2131-179">Ältere Indizes enthalten keine Versionsinformationen.</span><span class="sxs-lookup"><span data-stu-id="b2131-179">Older indexes contain no version information.</span></span> <span data-ttu-id="b2131-180">Die meisten Unicode-normalisierungs Änderungen umfassen das Hinzufügen neuer Zeichen, Code Punkte, die zuvor nicht definiert waren, werden nun definiert und unterschiedlich normalisiert.</span><span class="sxs-lookup"><span data-stu-id="b2131-180">Most Unicode normalization changes consist of adding new characters, code points which were previously undefined are now defined and normalize differently.</span></span> <span data-ttu-id="b2131-181">Wenn Binärdaten in einer Unicode-Spalte gespeichert werden, normalisiert Sie daher anders, wenn neue Code Punkte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="b2131-181">Thus, if binary data is stored in a Unicode column, it will normalize differently as new code points are defined.</span></span>

<span data-ttu-id="b2131-182">Ab Windows Server 2003 verfolgt die ESE-Datenbank-Engine Unicode-Indexeinträge, die nicht definierte Code Punkte enthalten.</span><span class="sxs-lookup"><span data-stu-id="b2131-182">As of Windows Server 2003, the ESE database engine tracks Unicode index entries that contain undefined code points.</span></span> <span data-ttu-id="b2131-183">Diese können verwendet werden, um einen Index zu korrigieren, wenn sich der Satz definierter Unicode-Zeichen ändert.</span><span class="sxs-lookup"><span data-stu-id="b2131-183">These can be used to fix an index when the set of defined Unicode characters changes.</span></span>

<span data-ttu-id="b2131-184">Diese Parameter steuern, was geschieht, wenn die ESE-Datenbank-Engine an eine Datenbank angefügt wird, die zuletzt unter einem anderen Build des Betriebssystems verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b2131-184">These parameters control what happens when the ESE database engine attaches to a database that was last used under a different build of the operating system.</span></span> <span data-ttu-id="b2131-185">Die Betriebssystemversion wird in den Daten Bank Header gestempelt.</span><span class="sxs-lookup"><span data-stu-id="b2131-185">The operating system version is stamped in the database header.</span></span>

<span data-ttu-id="b2131-186">Wenn [JET_paramEnableIndexChecking](./database-parameters.md) auf **true** festgelegt ist und die Datenbank potenziell beschädigte Indizes enthält:</span><span class="sxs-lookup"><span data-stu-id="b2131-186">If [JET_paramEnableIndexChecking](./database-parameters.md) is set to **TRUE**, and the database contains potentially corrupt indexes:</span></span>

  - <span data-ttu-id="b2131-187">**Jetattachdatabase** löscht die potenziell beschädigten Indizes, wenn *grbit* JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="b2131-187">**JetAttachDatabase** will delete the potentially corrupt indexes if *grbit* contains JET_bitDbDeleteCorruptIndexes</span></span>

  - <span data-ttu-id="b2131-188">**Jetattachdatabase** gibt einen Fehler zurück, wenn *grbit* keine JET_bitDbDeleteCorruptIndexes enthält und Indizes vorhanden sind, die gelöscht werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b2131-188">**JetAttachDatabase** will return an error if *grbit* does not contain JET_bitDbDeleteCorruptIndexes and there are indexes which need deletion.</span></span>

<span data-ttu-id="b2131-189">Wenn [JET_paramEnableIndexChecking](./database-parameters.md) auf **false** festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="b2131-189">If [JET_paramEnableIndexChecking](./database-parameters.md) is set to **FALSE**:</span></span>

  - <span data-ttu-id="b2131-190">**Jetattachdatabase** ignoriert potenziell beschädigte Indizes und gibt JET_errSuccess zurück (unter der Voraussetzung, dass keine anderen Fehler aufgetreten sind).</span><span class="sxs-lookup"><span data-stu-id="b2131-190">**JetAttachDatabase** will ignore potentially corrupt indexes, and return JET_errSuccess (assuming there were no other errors).</span></span>

<span data-ttu-id="b2131-191">Windows Server 2003 und höher: Wenn [JET_paramEnableIndexChecking](./database-parameters.md) nicht zurückgesetzt wurde, wird die interne fixuptabelle verwendet, um Indexeinträge zu fixieren.</span><span class="sxs-lookup"><span data-stu-id="b2131-191">Windows Server 2003 and later: If [JET_paramEnableIndexChecking](./database-parameters.md) has not been reset, the internal fixup table will be used to fixup index entries.</span></span> <span data-ttu-id="b2131-192">Dadurch werden möglicherweise nicht alle Index Beschädigungen behoben, Sie sind jedoch für die Anwendung transparent.</span><span class="sxs-lookup"><span data-stu-id="b2131-192">This may not fix all index corruptions but will be transparent to the application.</span></span>

<span data-ttu-id="b2131-193">Wenn die Datenbank als schreibgeschützt angefügt wurde, kann der Index nicht korrigiert oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="b2131-193">If the database was attached as read-only the index cannot be fixed or deleted.</span></span> <span data-ttu-id="b2131-194">In diesem Fall gibt die API stattdessen einen Fehler zurück, z. b. JET_errSecondaryIndexCorrupted oder JET_errPrimaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="b2131-194">In this case, the API will instead return an error, such as JET_errSecondaryIndexCorrupted or JET_errPrimaryIndexCorrupted.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b2131-195">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2131-195">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2131-196"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b2131-196"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b2131-197">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b2131-197">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2131-198"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b2131-198"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b2131-199">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b2131-199">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2131-200"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b2131-200"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b2131-201">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="b2131-201">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2131-202"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="b2131-202"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b2131-203">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b2131-203">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2131-204"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b2131-204"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b2131-205">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b2131-205">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2131-206"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="b2131-206"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="b2131-207">Implementiert als <strong>jetaddcolumnw</strong> (Unicode) und <strong>jetaddcolumna</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="b2131-207">Implemented as <strong>JetAddColumnW</strong> (Unicode) and <strong>JetAddColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b2131-208">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b2131-208">See Also</span></span>

[<span data-ttu-id="b2131-209">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="b2131-209">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="b2131-210">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b2131-210">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b2131-211">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b2131-211">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b2131-212">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b2131-212">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b2131-213">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b2131-213">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="b2131-214">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="b2131-214">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="b2131-215">Jetkreatedatabase</span><span class="sxs-lookup"><span data-stu-id="b2131-215">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="b2131-216">Jetdetachdatabase</span><span class="sxs-lookup"><span data-stu-id="b2131-216">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="b2131-217">JetDetachDatabase2</span><span class="sxs-lookup"><span data-stu-id="b2131-217">JetDetachDatabase2</span></span>](./jetdetachdatabase2-function.md)  
[<span data-ttu-id="b2131-218">Jetopumdatabase</span><span class="sxs-lookup"><span data-stu-id="b2131-218">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="b2131-219">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="b2131-219">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
