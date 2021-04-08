---
description: 'Weitere Informationen finden Sie hier: JetExternalRestore2-Funktion'
title: JetExternalRestore2-Funktion
TOCTitle: JetExternalRestore2 Function
ms:assetid: 66331be0-7abc-43a0-8b8b-dbdd227c918e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269272(v=EXCHG.10)
ms:contentKeyID: 32765574
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestore2W
- JetExternalRestore2A
- JetExternalRestore2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96314e401a81271f5a71bc056faa95fc1ae0dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960197"
---
# <a name="jetexternalrestore2-function"></a><span data-ttu-id="c73bf-103">JetExternalRestore2-Funktion</span><span class="sxs-lookup"><span data-stu-id="c73bf-103">JetExternalRestore2 Function</span></span>


<span data-ttu-id="c73bf-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c73bf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetexternalrestore2-function"></a><span data-ttu-id="c73bf-105">JetExternalRestore2-Funktion</span><span class="sxs-lookup"><span data-stu-id="c73bf-105">JetExternalRestore2 Function</span></span>

<span data-ttu-id="c73bf-106">Die **JetExternalRestore2** -Funktion stellt eine externe Sicherung wieder her, die mit den externen Backup-APIs erstellt wurde, und stellt Prüfpunkte für zirkuläre Protokollierungs Vorgänge bereit.</span><span class="sxs-lookup"><span data-stu-id="c73bf-106">The **JetExternalRestore2** function restores an external backup that was taken with the external backup APIs and provides checkpoints to use for circular logging operations.</span></span> <span data-ttu-id="c73bf-107">Dies wird als harte Wiederherstellung bezeichnet, die ähnlich, aber von der Soft-Wiederherstellung abweicht, wie von der [jetinit](./jetinit-function.md) -Funktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c73bf-107">This is known as hard recovery, which is similar but different than soft recovery as performed by the [JetInit](./jetinit-function.md) function.</span></span>

<span data-ttu-id="c73bf-108">**Windows XP: JetExternalRestore2** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c73bf-108">**Windows XP:  JetExternalRestore2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetExternalRestore2(
      __in          JET_PSTR szCheckpointFilePath,
      __in          JET_PSTR szLogPath,
      __in_opt      JET_RSTMAP* rgrstmap,
      __in          long crstfilemap,
      __in          JET_PSTR szBackupLogPath,
      __in_out      JET_LOGINFO* pLogInfo,
      __in_opt      JET_PSTR szTargetInstanceName,
      __in_opt      JET_PSTR szTargetInstanceLogPath,
      __in_opt      JET_PSTR szTargetInstanceCheckpointPath,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="c73bf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c73bf-109">Parameters</span></span>

<span data-ttu-id="c73bf-110">*szcheckpointfilepath*</span><span class="sxs-lookup"><span data-stu-id="c73bf-110">*szCheckpointFilePath*</span></span>

<span data-ttu-id="c73bf-111">Der Pfad für die Prüf Punkt Datei, die während der Wiederherstellung verwendet werden soll, wenn *sztargetinstancecheckpointpath* nicht angegeben ist oder der Pfad eine aktive oder ausgeführte Instanz aufweist.</span><span class="sxs-lookup"><span data-stu-id="c73bf-111">The path for the checkpoint file to use during recovery if *szTargetInstanceCheckpointPath* is not specified or that path has an active or running instance.</span></span>

<span data-ttu-id="c73bf-112">*szlogpath*</span><span class="sxs-lookup"><span data-stu-id="c73bf-112">*szLogPath*</span></span>

<span data-ttu-id="c73bf-113">Der Pfad oder das Verzeichnis für die Protokolle für die letzte Phase (rückgängig) der Wiederherstellung und möglicherweise für die Roll Forward-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="c73bf-113">The path or directory for the logs for the final phase (undo) of the recovery and possibly for the roll forward logs.</span></span> <span data-ttu-id="c73bf-114">Dieser Pfad kann mit dem *szbackuplogpath* identisch sein.</span><span class="sxs-lookup"><span data-stu-id="c73bf-114">This path may be the same as the *szBackupLogPath*.</span></span>

<span data-ttu-id="c73bf-115">*rgrstmap*</span><span class="sxs-lookup"><span data-stu-id="c73bf-115">*rgrstmap*</span></span>

<span data-ttu-id="c73bf-116">Dies ist ein Array von [JET_RSTMAP](./jet-rstmap-structure.md) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="c73bf-116">This is an array of [JET_RSTMAP](./jet-rstmap-structure.md) structures.</span></span> <span data-ttu-id="c73bf-117">Dabei handelt es sich um eine Zuordnung von alten und neuen Daten Bank Pfaden oder Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="c73bf-117">This is a map of old and new database paths or filenames.</span></span> <span data-ttu-id="c73bf-118">Dies wird verwendet, da die Datenbanken möglicherweise an einem anderen Speicherort als dem Speicherort wieder hergestellt werden müssen, von dem aus Sie gesichert wurden.</span><span class="sxs-lookup"><span data-stu-id="c73bf-118">This is used because the databases may need to be recovered to a location other than the location they were backed up from.</span></span> <span data-ttu-id="c73bf-119">Wenn mehrere Datenbanken an einen einzelnen protokolliersatz angefügt werden, kann die Restore Map eine Teilmenge der wiederherzustellenden Datenbanken angeben.</span><span class="sxs-lookup"><span data-stu-id="c73bf-119">In the case where multiple databases are attached to a single logging set, the restore map can specify a subset of the databases to restore.</span></span>

<span data-ttu-id="c73bf-120">*crstfilemap*</span><span class="sxs-lookup"><span data-stu-id="c73bf-120">*crstfilemap*</span></span>

<span data-ttu-id="c73bf-121">Die Anzahl der Einträge im *rgrstmap* -Array Parameter.</span><span class="sxs-lookup"><span data-stu-id="c73bf-121">The number of entries in the *rgrstmap* array parameter.</span></span>

<span data-ttu-id="c73bf-122">*szbackuplogpath*</span><span class="sxs-lookup"><span data-stu-id="c73bf-122">*szBackupLogPath*</span></span>

<span data-ttu-id="c73bf-123">Der Pfad zu dem Verzeichnis, in dem die Protokolldateien wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c73bf-123">The path to the directory where the log files are restored.</span></span> <span data-ttu-id="c73bf-124">Dabei handelt es sich um die Protokolle, die während der externen Sicherungs Sequenz gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="c73bf-124">These are the logs that were read off during the external backup sequence.</span></span> <span data-ttu-id="c73bf-125">Dieser Pfad kann mit dem *szlogpath* identisch sein.</span><span class="sxs-lookup"><span data-stu-id="c73bf-125">This path may be the same as the *szLogPath*.</span></span>

<span data-ttu-id="c73bf-126">*ploginfo*</span><span class="sxs-lookup"><span data-stu-id="c73bf-126">*pLogInfo*</span></span>

<span data-ttu-id="c73bf-127">*Ploginfo* beschreibt verschiedene Aspekte der Sicherungs Protokolle für die Wiederherstellung. dieser Parameter ermöglicht es **JetExternalRestore2** , die expliziten *genlow* -und *genhigh* -Parameter, die **JetExternalRestore2** haben, sowie den Basisprotokoll Namen anstelle eines vermuteten Protokoll Basis namens "edb" zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c73bf-127">The *pLogInfo* describes several aspects of the backup logs to recovery, this parameter allows **JetExternalRestore2** to take the explicit *genLow* and *genHigh* parameters that **JetExternalRestore2** has, as well as the base log name, instead of a presumed log base name of "edb".</span></span>

<span data-ttu-id="c73bf-128">*sztargetinstancename*</span><span class="sxs-lookup"><span data-stu-id="c73bf-128">*szTargetInstanceName*</span></span>

<span data-ttu-id="c73bf-129">Dieser Parameter ist veraltet und kann nicht in der Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c73bf-129">This parameter is deprecated and cannot be used in your application.</span></span>

<span data-ttu-id="c73bf-130">*sztargetinstancelogpath*</span><span class="sxs-lookup"><span data-stu-id="c73bf-130">*szTargetInstanceLogPath*</span></span>

<span data-ttu-id="c73bf-131">Der Pfad für die rollforwardprotokolle, wenn sich der Speicherort der Protokolle, für die Sie ein Roll Forward ausführen möchten, in einem aktiven Protokollierungs Satz oder einer Instanz befindet.</span><span class="sxs-lookup"><span data-stu-id="c73bf-131">The path for the roll forward logs if the location of the logs you would like to roll forward are in an active logging set or instance.</span></span> <span data-ttu-id="c73bf-132">Dieser Wert sollte nicht angegeben werden, wenn die Ziel Instanz die zirkuläre Protokollierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c73bf-132">This should not be specified if the target instance is using circular logging.</span></span>

<span data-ttu-id="c73bf-133">*sztargetinstancecheckpointpath*</span><span class="sxs-lookup"><span data-stu-id="c73bf-133">*szTargetInstanceCheckpointPath*</span></span>

<span data-ttu-id="c73bf-134">Der Pfad für den Prüfpunkt während der Wiederherstellung, wenn keine aktive Instanz an diesem Ziel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c73bf-134">The path for the checkpoint during recovery if there is no active instance running at this target.</span></span> <span data-ttu-id="c73bf-135">Dieser Wert sollte nicht angegeben werden, wenn die Ziel Instanz die zirkuläre Protokollierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c73bf-135">This should not be specified if the target instance is using circular logging.</span></span>

<span data-ttu-id="c73bf-136">*PFN*</span><span class="sxs-lookup"><span data-stu-id="c73bf-136">*pfn*</span></span>

<span data-ttu-id="c73bf-137">Der Status Rückruf, der den Fortschritt der Wiederherstellung meldet.</span><span class="sxs-lookup"><span data-stu-id="c73bf-137">The status callback, which reports the progress of the recovery.</span></span>

### <a name="return-value"></a><span data-ttu-id="c73bf-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c73bf-138">Return Value</span></span>

<span data-ttu-id="c73bf-139">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="c73bf-139">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c73bf-140">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c73bf-140">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c73bf-141">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c73bf-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="c73bf-142">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c73bf-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c73bf-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c73bf-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c73bf-144">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c73bf-144">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c73bf-145">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="c73bf-145">JET_errBadRestoreTargetInstance</span></span></p></td>
<td><p><span data-ttu-id="c73bf-146">Der angegebene <em>sztargetinstancelogpath</em> gehört nicht zu einer initialisierten Instanz.</span><span class="sxs-lookup"><span data-stu-id="c73bf-146">The <em>szTargetInstanceLogPath</em> specified does not belong to an initialized instance.</span></span> <span data-ttu-id="c73bf-147">Dieser Fehler wird nur in Windows XP und höher zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c73bf-147">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c73bf-148">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="c73bf-148">JET_errDatabaseCorrupted</span></span></p></td>
<td><p><span data-ttu-id="c73bf-149">Dies weist darauf hin, dass die Datenbank beschädigt wurde, oder eine unbekannte Datei.</span><span class="sxs-lookup"><span data-stu-id="c73bf-149">This indicates the database was corrupted, or an unrecognized file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c73bf-150">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="c73bf-150">JET_errEndingRestoreLogTooLow</span></span></p></td>
<td><p><span data-ttu-id="c73bf-151">Dieser Fehler wird zurückgegeben, wenn für die Protokolldateien im <em>szbackuplogpath</em>eine Protokoll Generierung oberhalb der in <em>genhigh</em> oder <em>ploginfo. ulgenhigh</em>angegebenen Protokolldateien vorliegt.</span><span class="sxs-lookup"><span data-stu-id="c73bf-151">This error is returned if one for the log files in the <em>szBackupLogPath</em>, has a log generation above that specified in <em>genHigh</em> or <em>pLogInfo.ulGenHigh</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c73bf-152">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="c73bf-152">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="c73bf-153">Der Vorgang ist fehlgeschlagen, da die angeforderte Datei nicht geöffnet werden konnte, da Sie im angegebenen Pfad nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="c73bf-153">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c73bf-154">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c73bf-154">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c73bf-155">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="c73bf-155">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="c73bf-156">Dies kann bei <a href="gg294088(v=exchg.10).md">jetexternalrestore</a>der Fall sein, wenn " <em>sztargetcheckpointpath</em> " und " <em>sztargetinstancelogpath</em> " nicht beide angegeben oder nicht angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c73bf-156">This can happen for <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>, and so on when the <em>szTargetCheckpointPath</em> and the <em>szTargetInstanceLogPath</em> are either not both specified or not both unspecified.</span></span> <span data-ttu-id="c73bf-157">Das heißt, Sie müssen abgeglichen werden und beide angegeben oder nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c73bf-157">That is, they must match, and be both specified or both unspecified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c73bf-158">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="c73bf-158">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="c73bf-159">Der Vorgang ist fehlgeschlagen, da der angegebene Pfad nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="c73bf-159">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c73bf-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="c73bf-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="c73bf-161">Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c73bf-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c73bf-162">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="c73bf-162">JET_errRestoreOfNonBackupDatabase</span></span></p></td>
<td><p><span data-ttu-id="c73bf-163">Dieser Fehler wird zurückgegeben, wenn es sich bei der während der Wiederherstellung angegebenen Datenbankdatei nicht um eine Datenbank handelt, die mit externer Sicherung gesichert wurde.</span><span class="sxs-lookup"><span data-stu-id="c73bf-163">This error is returned if the database file specified during restore is not a database that was backed up with external backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c73bf-164">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="c73bf-164">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="c73bf-165">Die Datenbank-Engine kann eine externe Wiederherstellung oder eine feste Wiederherstellung nicht im Single Instance-Modus ausführen.</span><span class="sxs-lookup"><span data-stu-id="c73bf-165">The database engine cannot run external restore or hard recovery in single instance mode.</span></span> <span data-ttu-id="c73bf-166">Dieser Fehler wird nur in Windows XP und höher zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c73bf-166">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c73bf-167">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="c73bf-167">JET_errStartingRestoreLogTooHigh</span></span></p></td>
<td><p><span data-ttu-id="c73bf-168">Dieser Fehler wird zurückgegeben, wenn eine der Protokolldateien im <em>szbackuplogpath</em>eine Protokoll Generierung unterhalb der von <em>genlow</em> oder <em>ploginfo. ulgenlow</em>angegebenen Protokolldateien aufweist.</span><span class="sxs-lookup"><span data-stu-id="c73bf-168">This error is returned if one of the log files in the <em>szBackupLogPath</em>, has a log generation below that specified by the <em>genLow</em> or <em>pLogInfo.ulGenLow</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c73bf-169">Bei Erfolg werden alle Datenbanken aus der *rgrstmap* vollständig wieder hergestellt und sind in einem sauberen oder konsistenten Zustand.</span><span class="sxs-lookup"><span data-stu-id="c73bf-169">On success, all databases from the *rgrstmap* are completely recovered and in a clean or consistent state.</span></span> <span data-ttu-id="c73bf-170">An diesem Punkt kann die Datenbank erneut an eine vorhandene Instanz bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c73bf-170">At this point the database can be remounted to an existing instance.</span></span>

<span data-ttu-id="c73bf-171">Bei einem Fehler konnte die Engine die Datenbank nicht wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="c73bf-171">On failure, the engine could not recover the database.</span></span> <span data-ttu-id="c73bf-172">Die Datenbank befindet sich in einem ungültigen Status. um eine Wiederherstellung zu versuchen, muss die gesamte Datenbank wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c73bf-172">The database is in an invalid state, and in order to retry hard recovery the entire database must be restored again.</span></span> <span data-ttu-id="c73bf-173">In der Regel handelt es sich bei einer solchen Situation um eine Datenträger-oder Protokoll Beschädigung oder eine andere Form der Protokoll Misswirtschaft oder um einen nicht kontinuierlichen Protokoll Satz.</span><span class="sxs-lookup"><span data-stu-id="c73bf-173">Typically, the source of such a situation is disk or log corruption, or some other form of log mismanagement, or a non-continuous log set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c73bf-174">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c73bf-174">Remarks</span></span>

<span data-ttu-id="c73bf-175">Siehe [jetexternalrestore](./jetexternalrestore-function.md).</span><span class="sxs-lookup"><span data-stu-id="c73bf-175">See [JetExternalRestore](./jetexternalrestore-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="c73bf-176">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c73bf-176">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c73bf-177"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c73bf-177"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c73bf-178">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c73bf-178">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c73bf-179"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c73bf-179"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c73bf-180">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c73bf-180">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c73bf-181"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c73bf-181"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c73bf-182">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="c73bf-182">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c73bf-183"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="c73bf-183"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c73bf-184">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c73bf-184">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c73bf-185"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c73bf-185"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c73bf-186">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c73bf-186">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c73bf-187"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="c73bf-187"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="c73bf-188">Implementiert als <strong>JetExternalRestore2W</strong> (Unicode) und <strong>JetExternalRestore2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c73bf-188">Implemented as <strong>JetExternalRestore2W</strong> (Unicode) and <strong>JetExternalRestore2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c73bf-189">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c73bf-189">See Also</span></span>

[<span data-ttu-id="c73bf-190">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c73bf-190">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c73bf-191">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="c73bf-191">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="c73bf-192">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="c73bf-192">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="c73bf-193">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="c73bf-193">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="c73bf-194">Jetbeginexternalbackup</span><span class="sxs-lookup"><span data-stu-id="c73bf-194">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="c73bf-195">Jetexternalrestore</span><span class="sxs-lookup"><span data-stu-id="c73bf-195">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="c73bf-196">JetInit</span><span class="sxs-lookup"><span data-stu-id="c73bf-196">JetInit</span></span>](./jetinit-function.md)
