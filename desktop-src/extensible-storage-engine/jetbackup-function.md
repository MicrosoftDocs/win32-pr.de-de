---
description: 'Weitere Informationen zu: JetBackup-Funktion'
title: JetBackup-Funktion
TOCTitle: JetBackup Function
ms:assetid: afff995f-378a-4e67-b522-d5eafcbad57e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294058(v=EXCHG.10)
ms:contentKeyID: 32765673
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupA
- JetBackup
- JetBackupW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f225053df36ebe98bc890a8e036d84ee31b6b154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351134"
---
# <a name="jetbackup-function"></a><span data-ttu-id="1df5d-103">JetBackup-Funktion</span><span class="sxs-lookup"><span data-stu-id="1df5d-103">JetBackup Function</span></span>


<span data-ttu-id="1df5d-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1df5d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbackup-function"></a><span data-ttu-id="1df5d-105">JetBackup-Funktion</span><span class="sxs-lookup"><span data-stu-id="1df5d-105">JetBackup Function</span></span>

<span data-ttu-id="1df5d-106">Die **JetBackup** -Funktion erstellt eine Sicherung der Datenbank, während die Datenbank online ist.</span><span class="sxs-lookup"><span data-stu-id="1df5d-106">The **JetBackup** function creates a backup of the database while the database is online.</span></span> <span data-ttu-id="1df5d-107">Bei dieser Funktion handelt es sich hauptsächlich um Abwärtskompatibilität mit Windows 2000 und früheren Datenbank-Engines, bei denen nur eine Instanz einer Datenbank zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="1df5d-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="1df5d-108">In diesem Fall ist die aktive Instanz die Instanz, die gesichert wird.</span><span class="sxs-lookup"><span data-stu-id="1df5d-108">In this case, the active instance is the instance that is backed up.</span></span>

```cpp
    JET_ERR JET_API JetBackup(
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a><span data-ttu-id="1df5d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1df5d-109">Parameters</span></span>

<span data-ttu-id="1df5d-110">*szbackuppath*</span><span class="sxs-lookup"><span data-stu-id="1df5d-110">*szBackupPath*</span></span>

<span data-ttu-id="1df5d-111">Das Verzeichnis, in dem die Sicherung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="1df5d-111">The directory where the backup is stored.</span></span> <span data-ttu-id="1df5d-112">Wenn der Sicherungs Pfad NULL ist, schneidet die Funktion die Protokolle nach Möglichkeit ab.</span><span class="sxs-lookup"><span data-stu-id="1df5d-112">If the backup path is NULL, the function will truncate the logs, if possible.</span></span>

<span data-ttu-id="1df5d-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="1df5d-113">*grbit*</span></span>

<span data-ttu-id="1df5d-114">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="1df5d-114">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1df5d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1df5d-115">Value</span></span></p></th>
<th><p><span data-ttu-id="1df5d-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1df5d-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1df5d-117">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="1df5d-117">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="1df5d-118">Erstellt eine vollständige Sicherung der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1df5d-118">Creates a full backup of the database.</span></span> <span data-ttu-id="1df5d-119">Dies ermöglicht die Beibehaltung einer vorhandenen Sicherung im gleichen Verzeichnis, wenn die neue Sicherung nicht ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1df5d-119">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1df5d-120">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="1df5d-120">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="1df5d-121">Erstellt im Gegensatz zu einer vollständigen Sicherung eine inkrementelle Sicherung.</span><span class="sxs-lookup"><span data-stu-id="1df5d-121">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="1df5d-122">Dies bedeutet, dass nur die Protokolldateien seit der letzten vollständigen oder inkrementellen Sicherung gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="1df5d-122">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1df5d-123">*pfnstatus*</span><span class="sxs-lookup"><span data-stu-id="1df5d-123">*pfnStatus*</span></span>

<span data-ttu-id="1df5d-124">Ein Zeiger auf die [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) Callback-Funktion, die Benachrichtigungs Informationen zum Fortschritt des Sicherungs Vorgangs bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="1df5d-124">Pointer to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function, which provides notification information about the progress of the backup operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="1df5d-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1df5d-125">Return Value</span></span>

<span data-ttu-id="1df5d-126">Die-Funktion gibt einen der [JET_ERR](./jet-err.md) Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="1df5d-126">The function returns one of the [JET_ERR](./jet-err.md) error codes.</span></span> <span data-ttu-id="1df5d-127">Im folgenden finden Sie die am häufigsten zurückgegebenen.</span><span class="sxs-lookup"><span data-stu-id="1df5d-127">The following are the most commonly returned.</span></span> <span data-ttu-id="1df5d-128">(Eine komplette Liste der Fehler für diese API finden Sie unter [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)</span><span class="sxs-lookup"><span data-stu-id="1df5d-128">(For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1df5d-129">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1df5d-129">Return code</span></span></p></th>
<th><p><span data-ttu-id="1df5d-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1df5d-130">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1df5d-131">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1df5d-131">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1df5d-132">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1df5d-132">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1df5d-133">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="1df5d-133">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="1df5d-134">Für dieselbe Instanz wird bereits eine Sicherung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1df5d-134">A backup is already in progress for the same instance.</span></span> <span data-ttu-id="1df5d-135">Mehrere Sicherungen sind gleichzeitig nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="1df5d-135">Multiple backups are not allowed at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1df5d-136">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="1df5d-136">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="1df5d-137">Die Instanz ist noch nicht für die Sicherung bereit, während Sie initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="1df5d-137">The instance is not ready yet for backup as it is initializing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1df5d-138">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="1df5d-138">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="1df5d-139">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="1df5d-139">The operation cannot complete because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1df5d-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="1df5d-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="1df5d-141">Der Vorgang kann nicht ausgeführt werden, da der der Sitzung zugeordnete-Instanz einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="1df5d-141">The operation cannot complete because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="1df5d-142"><strong>Windows XP:  </strong> Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1df5d-142"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1df5d-143">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="1df5d-143">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="1df5d-144">Eine inkrementelle Sicherung ist nicht zulässig, wenn die zirkuläre Protokollierung on</span><span class="sxs-lookup"><span data-stu-id="1df5d-144">An incremental backup is not allowed if circular logging is on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1df5d-145">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="1df5d-145">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="1df5d-146">Die angegebenen Optionen sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="1df5d-146">The specified options are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1df5d-147">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1df5d-147">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1df5d-148">Ein ungültiger Parameter wurde an die API übergeben.</span><span class="sxs-lookup"><span data-stu-id="1df5d-148">An invalid parameter was passed into the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1df5d-149">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="1df5d-149">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="1df5d-150">Der Zielpfad ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1df5d-150">The destination path does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1df5d-151">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="1df5d-151">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="1df5d-152">Die Instanz wird ohne Protokollierung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1df5d-152">The instance is running without logging.</span></span> <span data-ttu-id="1df5d-153">Es ist keine Sicherung zulässig.</span><span class="sxs-lookup"><span data-stu-id="1df5d-153">No backup is allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1df5d-154">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="1df5d-154">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="1df5d-155">Bei einer Protokolldatei ist ein Prüfsummen Überprüfungs Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1df5d-155">There was a checksum verification error on a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1df5d-156">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="1df5d-156">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="1df5d-157">Die Protokollierung für die Instanz ist aufgrund eines unerwarteten Fehlers temporär oder dauerhaft deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1df5d-157">The logging for the instance is temporary or permanently disabled due to an unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1df5d-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="1df5d-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="1df5d-159">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1df5d-159">The operation cannot complete because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1df5d-160">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="1df5d-160">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="1df5d-161">Auf einer Datenbankseite ist ein Prüfsummen Überprüfungs Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1df5d-161">There was a checksum verification error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1df5d-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="1df5d-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="1df5d-163">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1df5d-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1df5d-164">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="1df5d-164">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="1df5d-165">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1df5d-165">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="1df5d-166"><strong>Windows XP:  </strong> Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1df5d-166"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1df5d-167">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="1df5d-167">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="1df5d-168">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="1df5d-168">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1df5d-169">Wenn die Funktion erfolgreich ausgeführt wird, sind alle Dateien, die für eine Wiederherstellung bis zum Zeitpunkt der Sicherung benötigt werden, im Sicherungs Verzeichnis enthalten.</span><span class="sxs-lookup"><span data-stu-id="1df5d-169">If the function succeeds, all the files needed for a restore up to the moment of the backup will be contained in the backup directory.</span></span> <span data-ttu-id="1df5d-170">Wenn es sich um eine vollständige Sicherung handelt, sind die Dateien die Datenbankdateien und die Protokolldateien, die erforderlich sind, um die Datenbank in einen konsistenten Zustand zu bringen.</span><span class="sxs-lookup"><span data-stu-id="1df5d-170">If this is a full backup, the files will be the database files and the log files needed to bring the database to a consistent state.</span></span> <span data-ttu-id="1df5d-171">Wenn es sich um eine inkrementelle Sicherung handelt, werden den Verzeichnissen nur Protokolldateien hinzugefügt, aber die bereits vorhandenen Dateien (Datenbanken und Protokolldateien) können zusammen mit den neuen Protokolldateien wieder hergestellt werden, um die Datenbank wieder in den Zustand zu bringen, in dem Sie sich zum Zeitpunkt der Sicherung befand.</span><span class="sxs-lookup"><span data-stu-id="1df5d-171">If this is an incremental backup, only log files will be added to the directories, but the already existing files (databases and log files), together with the new log files, will be able to be restored to bring the database back to the state it was in at the moment that the backup began.</span></span>

<span data-ttu-id="1df5d-172">Als Nebeneffekt der Sicherung werden die Protokolldateien, die nicht mehr benötigt werden, abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="1df5d-172">As a side effect of the backup, the log files which are no longer needed will be truncated.</span></span>

<span data-ttu-id="1df5d-173">Gleichzeitig werden die Daten Bank Header mit den Informationen aktualisiert, wann die letzte Sicherung erfolgte.</span><span class="sxs-lookup"><span data-stu-id="1df5d-173">In the same time, the database headers will be updated with the information when the last backup took place.</span></span>

<span data-ttu-id="1df5d-174">Wenn die Funktion fehlschlägt, sind keine Dateien im Sicherungs Verzeichnis vorhanden, sodass keine Wiederherstellung möglich ist.</span><span class="sxs-lookup"><span data-stu-id="1df5d-174">If the function fails, there will not be any files in the backup directory destination so no restore will be possible.</span></span> <span data-ttu-id="1df5d-175">Gleichzeitig werden die aktuellen Protokolldateien nicht abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="1df5d-175">In the same time, the current log files will not be truncated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="1df5d-176">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1df5d-176">Remarks</span></span>

<span data-ttu-id="1df5d-177">In den verschiedenen Schritten der Sicherung werden Ereignisprotokoll Einträge generiert, einschließlich der Dateinamen, der Protokoll Verkürzung und des Endergebnisses der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="1df5d-177">The different steps of the backup will have Event Log entries generated, including the file names, the log truncation, and the final result of the backup.</span></span>

<span data-ttu-id="1df5d-178">Inkrementelle Sicherungen können erst nach dem Erstellen einer vollständigen Sicherung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1df5d-178">Incremental backups are possible only after a full backup was taken.</span></span> <span data-ttu-id="1df5d-179">Außerdem sind inkrementelle Sicherungen nur möglich, wenn die zirkuläre Protokollierung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1df5d-179">Also, incremental backups are possible only if circular logging is turned off.</span></span> <span data-ttu-id="1df5d-180">Es wird empfohlen, dass das Sicherungs Verzeichnis keine Dateien enthält, die nicht in der Sicherung verwendet wurden oder von einer vorherigen erfolgreichen Sicherung hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="1df5d-180">It is recommended that the backup directory should not contain any files other than the one used in the backup or added by a previous successful backup.</span></span>

<span data-ttu-id="1df5d-181">Das Sicherungs Verzeichnis sollte vorhanden sein, es sei denn, der Parameter *JET_paramCreatePathIfNotExist* für die Instanz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1df5d-181">The backup directory should exist unless the parameter *JET_paramCreatePathIfNotExist* is set for the instance.</span></span> <span data-ttu-id="1df5d-182">Weitere Informationen finden Sie unter [System Parameter](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1df5d-182">For information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="1df5d-183">Die Sicherung führt eine Prüfsummen Überprüfung auf allen verwendeten Datenbankseiten und ab Windows Server 2003 in den Protokolldateien aus.</span><span class="sxs-lookup"><span data-stu-id="1df5d-183">The backup will do a checksum verification on all the used database pages and starting with Windows Server 2003, on the log files as well.</span></span> <span data-ttu-id="1df5d-184">Dadurch haben Sie die Möglichkeit, die Integrität der Datenbank zu schätzen, auch für Seiten, die während des normalen Betriebs nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="1df5d-184">This gives an opportunity to estimate the health of the database, even for pages which are not read during normal operations.</span></span> <span data-ttu-id="1df5d-185">Wenn eine solche Beschädigung aufgetreten ist, tritt bei der Sicherung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="1df5d-185">If any such corruption is encountered, the backup will fail.</span></span>

<span data-ttu-id="1df5d-186">Während der Sicherung wird die aktuelle Protokolldatei fertiggestellt, und es wird ein neues Protokoll generiert.</span><span class="sxs-lookup"><span data-stu-id="1df5d-186">During the backup, the current log file will be finished and a new log will be generated.</span></span> <span data-ttu-id="1df5d-187">Auf diese Weise können alle erforderlichen Protokolldateien kopiert werden, da das aktuelle Protokoll nicht mehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1df5d-187">This way, all of the necessary log files can be copies, because the current log will not be in use anymore.</span></span>

<span data-ttu-id="1df5d-188">Es wird dringend empfohlen, die Sicherung nicht für andere Zwecke als die Sicherung und Wiederherstellung auf Engine-Ebene zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1df5d-188">It is strongly recommended that the backup not be used for any purpose other than the backup and restore at the engine level.</span></span> <span data-ttu-id="1df5d-189">Dadurch wird die Wahrscheinlichkeit minimiert, dass während der Sicherungs-und Wiederherstellungs Vorgänge Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="1df5d-189">This will minimize the chance of getting errors during the backup and restore operations.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1df5d-190">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1df5d-190">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1df5d-191"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="1df5d-191"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1df5d-192">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1df5d-192">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1df5d-193"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1df5d-193"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1df5d-194">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1df5d-194">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1df5d-195"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1df5d-195"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1df5d-196">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="1df5d-196">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1df5d-197"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="1df5d-197"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1df5d-198">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1df5d-198">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1df5d-199"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1df5d-199"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1df5d-200">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1df5d-200">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1df5d-201"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="1df5d-201"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="1df5d-202">Implementiert als <strong>jetbackupw</strong> (Unicode) und <strong>jetbackupa</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="1df5d-202">Implemented as <strong>JetBackupW</strong> (Unicode) and <strong>JetBackupA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1df5d-203">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1df5d-203">See Also</span></span>

[<span data-ttu-id="1df5d-204">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="1df5d-204">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="1df5d-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1df5d-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1df5d-206">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1df5d-206">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1df5d-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="1df5d-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="1df5d-208">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="1df5d-208">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="1df5d-209">Jetrestore</span><span class="sxs-lookup"><span data-stu-id="1df5d-209">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="1df5d-210">JetRestore2</span><span class="sxs-lookup"><span data-stu-id="1df5d-210">JetRestore2</span></span>](./jetrestore2-function.md)  
[<span data-ttu-id="1df5d-211">Jetrestoreingestance</span><span class="sxs-lookup"><span data-stu-id="1df5d-211">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="1df5d-212">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="1df5d-212">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="1df5d-213">System Parameter</span><span class="sxs-lookup"><span data-stu-id="1df5d-213">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
