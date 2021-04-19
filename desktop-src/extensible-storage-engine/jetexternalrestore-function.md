---
description: 'Weitere Informationen finden Sie hier: jetexternalrestore-Funktion'
title: Jetexternalrestore-Funktion
TOCTitle: JetExternalRestore Function
ms:assetid: c930689a-3ea6-4c5a-9318-76f519f23343
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294088(v=EXCHG.10)
ms:contentKeyID: 32765703
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestoreA
- JetExternalRestore
- JetExternalRestoreW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 087949817ac0bcbe2effe2ff136a6ce80084daa2
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106373551"
---
# <a name="jetexternalrestore-function"></a><span data-ttu-id="834e9-103">Jetexternalrestore-Funktion</span><span class="sxs-lookup"><span data-stu-id="834e9-103">JetExternalRestore Function</span></span>


<span data-ttu-id="834e9-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="834e9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetexternalrestore-function"></a><span data-ttu-id="834e9-105">Jetexternalrestore-Funktion</span><span class="sxs-lookup"><span data-stu-id="834e9-105">JetExternalRestore Function</span></span>

<span data-ttu-id="834e9-106">Die **jetexternalrestore** -Funktion stellt eine externe Sicherung wieder her, die mit den externen Backup-APIs erstellt wurde, und gibt einen Bereich von Protokoll Dateinummern an, die während der Wiedergabe wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="834e9-106">The **JetExternalRestore** function restores an external backup that was taken with the external backup APIs and specifies a range of log file numbers to replay during the restore process.</span></span> <span data-ttu-id="834e9-107">Dies wird als "feste Wiederherstellung" bezeichnet. Dies ähnelt der von der [jetinit](./jetinit-function.md) -Funktion ausgeführten Soft-Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="834e9-107">This is known as hard recovery, which is similar to but different than soft recovery as performed by the [JetInit](./jetinit-function.md) function.</span></span>

```cpp
JET_ERR JET_API JetExternalRestore(
  __in          JET_PSTR szCheckpointFilePath,
  __in          JET_PSTR szLogPath,
  __in_opt      JET_RSTMAP* rgrstmap,
  __in          long crstfilemap,
  __in          JET_PSTR szBackupLogPath,
  __in          long genLow,
  __in          long genHigh,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a><span data-ttu-id="834e9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="834e9-108">Parameters</span></span>

<span data-ttu-id="834e9-109">*szcheckpointfilepath*</span><span class="sxs-lookup"><span data-stu-id="834e9-109">*szCheckpointFilePath*</span></span>

<span data-ttu-id="834e9-110">Der Pfad für die Prüf Punkt Datei, die während der Wiederherstellung verwendet werden soll, wenn *sztargetinstancecheckpointpath* nicht angegeben ist oder bereits über eine aktive oder ausgeführte Instanz verfügt.</span><span class="sxs-lookup"><span data-stu-id="834e9-110">The path for the checkpoint file to use during recovery if *szTargetInstanceCheckpointPath* is not specified or already has an active or running instance.</span></span>

<span data-ttu-id="834e9-111">*szlogpath*</span><span class="sxs-lookup"><span data-stu-id="834e9-111">*szLogPath*</span></span>

<span data-ttu-id="834e9-112">Der Pfad oder das Verzeichnis für die Protokolle für die letzte Phase (rückgängig) der Wiederherstellung und möglicherweise für die Roll Forward-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="834e9-112">The path or directory for the logs for the final phase (undo) of recovery, and possibly for the roll forward logs.</span></span> <span data-ttu-id="834e9-113">Dieser Pfad kann mit dem *szbackuplogpath* identisch sein.</span><span class="sxs-lookup"><span data-stu-id="834e9-113">This path may be the same as the *szBackupLogPath*.</span></span>

<span data-ttu-id="834e9-114">*rgrstmap*</span><span class="sxs-lookup"><span data-stu-id="834e9-114">*rgrstmap*</span></span>

<span data-ttu-id="834e9-115">Dies ist ein Array von [JET_RSTMAP](./jet-rstmap-structure.md) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="834e9-115">This is an array of [JET_RSTMAP](./jet-rstmap-structure.md) structures.</span></span> <span data-ttu-id="834e9-116">Dabei handelt es sich um eine Zuordnung von alten und neuen Daten Bank Pfaden oder Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="834e9-116">This is a map of old and new database paths or filenames.</span></span> <span data-ttu-id="834e9-117">Dies wird verwendet, da die Datenbanken möglicherweise an einem anderen Speicherort als dem Speicherort wieder hergestellt werden müssen, von dem aus Sie gesichert wurden.</span><span class="sxs-lookup"><span data-stu-id="834e9-117">This is used because the databases may need to be recovered to a location other than the location they were backed up from.</span></span> <span data-ttu-id="834e9-118">Wenn mehrere Datenbanken an einen einzelnen protokolliersatz angefügt werden, kann die Restore Map eine Teilmenge der wiederherzustellenden Datenbanken angeben.</span><span class="sxs-lookup"><span data-stu-id="834e9-118">In the case where multiple databases are attached to a single logging set, the restore map can specify a subset of databases to restore.</span></span>

<span data-ttu-id="834e9-119">*crstfilemap*</span><span class="sxs-lookup"><span data-stu-id="834e9-119">*crstfilemap*</span></span>

<span data-ttu-id="834e9-120">Die Anzahl der Einträge im *rgrstmap* -Array Parameter.</span><span class="sxs-lookup"><span data-stu-id="834e9-120">The number of entries in the *rgrstmap* array parameter.</span></span>

<span data-ttu-id="834e9-121">*szbackuplogpath*</span><span class="sxs-lookup"><span data-stu-id="834e9-121">*szBackupLogPath*</span></span>

<span data-ttu-id="834e9-122">Der Pfad zu dem Verzeichnis, in dem die Protokolldateien wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="834e9-122">The path to the directory where the log files are restored.</span></span> <span data-ttu-id="834e9-123">Dabei handelt es sich um die Protokolle, die während der externen Sicherungs Sequenz gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="834e9-123">These are the logs that were read off during the external backup sequence.</span></span> <span data-ttu-id="834e9-124">Dieser Pfad kann mit dem szlogpath identisch sein.</span><span class="sxs-lookup"><span data-stu-id="834e9-124">This path may be the same as the szLogPath.</span></span>

<span data-ttu-id="834e9-125">*genlow*</span><span class="sxs-lookup"><span data-stu-id="834e9-125">*genLow*</span></span>

<span data-ttu-id="834e9-126">Die niedrigste Protokolldatei Nummer, die von *szbackuplogpath* wiedergegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="834e9-126">The lowest log file number that is to be replayed from *szBackupLogPath*.</span></span> <span data-ttu-id="834e9-127">Die vollständige Genauigkeit eines langen Zeichens ohne Vorzeichen sollte beibehalten werden, aber in den aktuellen Versionen der Engine ist diese Zahl eine hexadezimale Zahl im Bereich von 0x00000 bis 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="834e9-127">The full fidelity of an unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="834e9-128">Dies kann sich in zukünftigen Versionen ändern.</span><span class="sxs-lookup"><span data-stu-id="834e9-128">This may change in future versions.</span></span>

<span data-ttu-id="834e9-129">*genhoch*</span><span class="sxs-lookup"><span data-stu-id="834e9-129">*genHigh*</span></span>

<span data-ttu-id="834e9-130">Die höchste Protokoll dateizahl, die von *szbackuplogpath* wiedergegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="834e9-130">The highest log file number that is to be replayed from *szBackupLogPath*.</span></span> <span data-ttu-id="834e9-131">Die vollständige Genauigkeit eines langen Zeichens ohne Vorzeichen sollte beibehalten werden, aber in den aktuellen Versionen der Engine ist diese Zahl eine hexadezimale Zahl im Bereich von 0x00000 bis 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="834e9-131">The full fidelity of a unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="834e9-132">Dies kann sich in zukünftigen Versionen ändern.</span><span class="sxs-lookup"><span data-stu-id="834e9-132">This may change in future versions.</span></span>

<span data-ttu-id="834e9-133">*PFN*</span><span class="sxs-lookup"><span data-stu-id="834e9-133">*pfn*</span></span>

<span data-ttu-id="834e9-134">Der Status Rückruf, um den Fortschritt der Wiederherstellung zu melden.</span><span class="sxs-lookup"><span data-stu-id="834e9-134">The status callback, to report progress of the recovery.</span></span>

### <a name="return-value"></a><span data-ttu-id="834e9-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="834e9-135">Return Value</span></span>

<span data-ttu-id="834e9-136">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="834e9-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="834e9-137">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="834e9-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="834e9-138">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="834e9-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="834e9-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="834e9-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="834e9-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="834e9-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="834e9-141">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="834e9-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="834e9-142">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="834e9-142">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="834e9-143">Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="834e9-143">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="834e9-144">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="834e9-144">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="834e9-145">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="834e9-145">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="834e9-146">Dies kann bei <strong>jetexternalrestore</strong>der Fall sein, wenn " <em>sztargetcheckpointpath</em> " und " <em>sztargetinstancelogpath</em> " nicht beide angegeben oder nicht angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="834e9-146">This can happen for <strong>JetExternalRestore</strong>, and so on when the <em>szTargetCheckpointPath</em> and the <em>szTargetInstanceLogPath</em> are either not both specified or not both unspecified.</span></span> <span data-ttu-id="834e9-147">Das heißt, Sie müssen abgeglichen werden und beide angegeben oder nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="834e9-147">That is, they must match, and be both specified or both unspecified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="834e9-148">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="834e9-148">JET_errDatabaseCorrupted</span></span></p></td>
<td><p><span data-ttu-id="834e9-149">Dies weist darauf hin, dass die Datenbank beschädigt wurde, oder eine unbekannte Datei.</span><span class="sxs-lookup"><span data-stu-id="834e9-149">This indicates the database was corrupted, or an unrecognized file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="834e9-150">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="834e9-150">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="834e9-151">Der Vorgang ist fehlgeschlagen, da die angeforderte Datei nicht geöffnet werden konnte, da Sie im angegebenen Pfad nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="834e9-151">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="834e9-152">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="834e9-152">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="834e9-153">Der Vorgang ist fehlgeschlagen, da der angegebene Pfad nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="834e9-153">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="834e9-154">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="834e9-154">JET_errRestoreOfNonBackupDatabase</span></span></p></td>
<td><p><span data-ttu-id="834e9-155">Dieser Fehler wird zurückgegeben, wenn es sich bei der während der Wiederherstellung angegebenen Datenbankdatei nicht um eine Datenbank handelt, die mit externer Sicherung gesichert wurde.</span><span class="sxs-lookup"><span data-stu-id="834e9-155">This error is returned if the database file specified during restore is not a database that was backed up with external backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="834e9-156">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="834e9-156">JET_errStartingRestoreLogTooHigh</span></span></p></td>
<td><p><span data-ttu-id="834e9-157">Dieser Fehler wird zurückgegeben, wenn eine der Protokolldateien im <em>szbackuplogpath</em>eine Protokoll Generierung unterhalb der von <em>genlow</em> oder <em>ploginfo. ulgenlow</em>angegebenen Protokolldateien aufweist.</span><span class="sxs-lookup"><span data-stu-id="834e9-157">This error is returned if one of the log files in the <em>szBackupLogPath</em>, has a log generation below that specified by the <em>genLow</em> or <em>pLogInfo.ulGenLow</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="834e9-158">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="834e9-158">JET_errEndingRestoreLogTooLow</span></span></p></td>
<td><p><span data-ttu-id="834e9-159">Dieser Fehler wird zurückgegeben, wenn eine der Protokolldateien im <em>szbackuplogpath</em>die Protokolldateien enthält, die über eine in <em>genhigh</em> oder <em>ploginfo. ulgenhigh</em>angegebene Protokoll Generierung verfügen.</span><span class="sxs-lookup"><span data-stu-id="834e9-159">This error is returned if one fo the log files in the <em>szBackupLogPath</em>, has a log generation above that specified in <em>genHigh</em> or <em>pLogInfo.ulGenHigh</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="834e9-160">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="834e9-160">JET_errBadRestoreTargetInstance</span></span></p></td>
<td><p><span data-ttu-id="834e9-161">Der angegebene <em>sztargetinstancelogpath</em> gehört nicht zu einer initialisierten Instanz.</span><span class="sxs-lookup"><span data-stu-id="834e9-161">The <em>szTargetInstanceLogPath</em> specified does not belong to an initialized instance.</span></span> <span data-ttu-id="834e9-162">Dieser Fehler wird nur in Windows XP und höher zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="834e9-162">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="834e9-163">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="834e9-163">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="834e9-164">Die Datenbank-Engine kann eine externe Wiederherstellung oder eine feste Wiederherstellung nicht im Single Instance-Modus ausführen.</span><span class="sxs-lookup"><span data-stu-id="834e9-164">The database engine cannot run external restore or hard recovery in single instance mode.</span></span> <span data-ttu-id="834e9-165">Dieser Fehler wird nur in Windows XP und höher zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="834e9-165">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="834e9-166">Bei Erfolg werden alle Datenbanken aus der *rgrstmap* vollständig wieder hergestellt und sind in einem sauberen oder konsistenten Zustand.</span><span class="sxs-lookup"><span data-stu-id="834e9-166">On success, all databases from the *rgrstmap* are completely recovered and in a clean or consistent state.</span></span> <span data-ttu-id="834e9-167">An diesem Punkt kann die Datenbank erneut an eine vorhandene Instanz bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="834e9-167">At this point the database can be remounted to an existing instance.</span></span>

<span data-ttu-id="834e9-168">Bei einem Fehler konnte die Engine die Datenbank nicht wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="834e9-168">On failure, the engine could not recover the database.</span></span> <span data-ttu-id="834e9-169">Die Datenbank befindet sich in einem ungültigen Status. um eine Wiederherstellung zu versuchen, muss die gesamte Datenbank wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="834e9-169">The database is in an invalid state, and in order to retry hard recovery the entire database must be restored again.</span></span> <span data-ttu-id="834e9-170">In der Regel handelt es sich bei einer solchen Situation um eine Datenträger-oder Protokoll Beschädigung oder eine andere Form der Protokoll Misswirtschaft oder um einen nicht kontinuierlichen Protokoll Satz.</span><span class="sxs-lookup"><span data-stu-id="834e9-170">Typically, the source of such a situation is disk or log corruption, or some other form of log mismanagement, or a non-continuous log set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="834e9-171">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="834e9-171">Remarks</span></span>

<span data-ttu-id="834e9-172">Um zu verstehen, wie eine "harte" Wiederherstellung funktioniert, müssen Sie verstehen, dass es drei Phasen der Wiederherstellung gibt und die zweite Phase zwei Teile haben kann.</span><span class="sxs-lookup"><span data-stu-id="834e9-172">To understand how a "hard" recovery works, you must understand that there are three phases of recovery, and the second phase can have two parts.</span></span> <span data-ttu-id="834e9-173">In Phase I sind Protokolle erforderlich, um eine gesicherte Datenbank in Konsistenz zu bringen (oder es kann ein ursprünglicher Satz inkrementeller Protokolle verwendet werden).</span><span class="sxs-lookup"><span data-stu-id="834e9-173">In Phase I, logs are required to bring a backed up database to consistency (or an initial set of incremental logs can be used).</span></span> <span data-ttu-id="834e9-174">In Phase II werden alle verfügbaren zusätzlichen Roll Forward-Protokolle genutzt, um die Datenbank konsistent zu machen.</span><span class="sxs-lookup"><span data-stu-id="834e9-174">In Phase II, any additional roll forward logs that are available are consumed to make the database consistent.</span></span> <span data-ttu-id="834e9-175">Außerdem gibt es eine Wiedergabe der zusätzlichen rollforwardprotokolle.</span><span class="sxs-lookup"><span data-stu-id="834e9-175">There is also a replay of the additional roll forward logs.</span></span> <span data-ttu-id="834e9-176">Phase III ist die Roll Back Phase der Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="834e9-176">Phase III is the undo phase of recovery.</span></span>

<span data-ttu-id="834e9-177">Phase I: die Wiedergabe des Satzes von Protokollen, die wieder hergestellt werden müssen, damit die Datenbank in einen konsistenten Status (oder einen anfänglichen Satz von Protokolldateien) gebracht wird.</span><span class="sxs-lookup"><span data-stu-id="834e9-177">Phase I: The replay of the set of logs that must be restored for the database to be brought to a consistent state (or an initial set of log files) is performed.</span></span> <span data-ttu-id="834e9-178">Im Grunde handelt es sich hierbei um die Wiedergabe des Satzes von Protokolldateien, die für die wiederherzustellenden Datenbanken nicht optional sind.</span><span class="sxs-lookup"><span data-stu-id="834e9-178">Basically, this is the replay of the set of log files that are not optional for the databases being restored.</span></span> <span data-ttu-id="834e9-179">Wenn in diesem Bereich von Protokollen fehlende Protokolle vorhanden sind, tritt bei der Wiederherstellung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="834e9-179">If there are missing logs from this range of logs then the restore will fail.</span></span> <span data-ttu-id="834e9-180">Diese Protokolle sollten in dem Verzeichnis abgelegt werden, das im Parameter " *szbackuplogpath* " angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="834e9-180">These logs should be put in the directory specified in the *szBackupLogPath* parameter.</span></span>

<span data-ttu-id="834e9-181">Phase II: Optional können Protokolldateien, die aus inkrementellen oder differenziellen Sicherungen und aus den Protokolldateien einer aktiven Instanz stammen, über eine Reihe von Protokolldateien verfügen.</span><span class="sxs-lookup"><span data-stu-id="834e9-181">Phase II: Optionally, there may be some sets of log files that are roll forward log files that come from incremental or differential backups and from the log files of an active instance.</span></span> <span data-ttu-id="834e9-182">Im Fall von Protokolldateien aus inkrementellen oder differenziellen Sicherungen können die Protokolldateien in den Verzeichnissen abgelegt werden, die entweder in den Parametern *szbackuplogpath* oder *sztargetinstancelogpath* angegeben sind, wobei das erste das empfohlene Verzeichnis ist.</span><span class="sxs-lookup"><span data-stu-id="834e9-182">In the case of log files from incremental or differential backups, the log files can be placed in the directories specified in either the *szBackupLogPath* or the *szTargetInstanceLogPath* parameters, with the former being the recommended directory.</span></span> <span data-ttu-id="834e9-183">Die Protokolle, die für die Rollforwardphase (Phase II) verwendet werden, sollten aus derselben Reihe von Protokollen stammen, die während der Phase i abgespielt wurden, und sollten die Protokoll Nummern kontinuierlich erhöhen, ohne dass Lücken aus der Phase i protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="834e9-183">The logs used for the roll forward phase (phase II) should come from the same series of logs played during Phase I and should have continuously incrementing log numbers with no gaps from the Phase I logs.</span></span> <span data-ttu-id="834e9-184">Um eine Datenbank vollständig auf dem neuesten Stand zu halten, um die Protokolldateien zu verwenden, die derzeit von einer aktiven Instanz verwendet werden, müssen die Parameter *sztargetinstancelogpath* und *sztargetinstancecheckpointpath* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="834e9-184">To play a database to be fully up to date with the log files currently being used by an active instance, the *szTargetInstanceLogPath* and *szTargetInstanceCheckpointPath* parameters must be specified.</span></span> <span data-ttu-id="834e9-185">Dies ist auch dann möglich, wenn andere Datenbanken an diesen Protokoll Satz angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="834e9-185">This can be done even while other databases are attached to that log set.</span></span>

<span data-ttu-id="834e9-186">Phase III: in der letzten Wiederherstellungs Phase wird für alle Transaktionen, für die kein Commit ausgeführt wurde, ein Rollback ausgeführt. hierfür müssen neue Protokolldateien erstellt und die Prüf Punkt Datei aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="834e9-186">Phase III: In the final phase of recovery, any uncommitted transactions are rolled back, which requires generating new log files and updating the checkpoint file.</span></span> <span data-ttu-id="834e9-187">Diese Phase wird manchmal als "Rückgängig" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="834e9-187">This phase is sometimes referred to as "undo".</span></span> <span data-ttu-id="834e9-188">Der in dieser Phase zu verwendende Pfad der Prüf Punkt Datei ist der Pfad analog zum Protokoll Speicherort in Phase III, d. h., wenn *szlogpath* für Phase III verwendet wird, wird *szcheckpointfilepath* verwendet, wenn " *sztargetinstancelogpath* " für Phase III der Wiederherstellungs Sitzung " *sztargetinstancecheckpointpath* " verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="834e9-188">The checkpoint file path to use during this phase is the path analogous to the phase III log location, that is, if *szLogPath* is used for Phase III, *szCheckpointFilePath* will be used, if *szTargetInstanceLogPath* is used for phase III of recovery *szTargetInstanceCheckpointPath* will be used.</span></span>

<span data-ttu-id="834e9-189">Verwenden Sie dieses Flussdiagramm, um zu verstehen, wie die Pfade funktionieren:</span><span class="sxs-lookup"><span data-stu-id="834e9-189">To understand how the paths work, use this flow chart:</span></span>

<span data-ttu-id="834e9-190">![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")</span><span class="sxs-lookup"><span data-stu-id="834e9-190">![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")</span></span>

#### <a name="requirements"></a><span data-ttu-id="834e9-191">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="834e9-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="834e9-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="834e9-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="834e9-193">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="834e9-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="834e9-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="834e9-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="834e9-195">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="834e9-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="834e9-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="834e9-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="834e9-197">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="834e9-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="834e9-198"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="834e9-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="834e9-199">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="834e9-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="834e9-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="834e9-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="834e9-201">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="834e9-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="834e9-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="834e9-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="834e9-203">Implementiert als <strong>jetexternalrestorew</strong> (Unicode) und <strong>jetexternalrestorea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="834e9-203">Implemented as <strong>JetExternalRestoreW</strong> (Unicode) and <strong>JetExternalRestoreA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="834e9-204">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="834e9-204">See Also</span></span>

[<span data-ttu-id="834e9-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="834e9-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="834e9-206">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="834e9-206">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="834e9-207">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="834e9-207">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="834e9-208">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="834e9-208">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="834e9-209">Jetbeginexternalbackup</span><span class="sxs-lookup"><span data-stu-id="834e9-209">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="834e9-210">JetInit</span><span class="sxs-lookup"><span data-stu-id="834e9-210">JetInit</span></span>](./jetinit-function.md)
