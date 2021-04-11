---
description: Weitere Informationen finden Sie in der jetbackupinstance-Funktion.
title: JetBackupInstance-Funktion
TOCTitle: JetBackupInstance Function
ms:assetid: 82486441-5037-440b-8632-038e953ad870
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269318(v=EXCHG.10)
ms:contentKeyID: 32765608
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupInstanceW
- JetBackupInstanceA
- JetBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fab20676267333ae8f60e4fe4f07d98a8b45e88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128176"
---
# <a name="jetbackupinstance-function"></a><span data-ttu-id="133fe-103">JetBackupInstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="133fe-103">JetBackupInstance Function</span></span>


<span data-ttu-id="133fe-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="133fe-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbackupinstance-function"></a><span data-ttu-id="133fe-105">JetBackupInstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="133fe-105">JetBackupInstance Function</span></span>

<span data-ttu-id="133fe-106">Die **jetbackupinstance** -Funktion führt eine Streamingsicherung einer Instanz, einschließlich aller angefügten Datenbanken, in ein Verzeichnis aus.</span><span class="sxs-lookup"><span data-stu-id="133fe-106">The **JetBackupInstance** function performs a streaming backup of an instance, including all the attached databases, to a directory.</span></span> <span data-ttu-id="133fe-107">Mit mehreren Sicherungsmethoden, die von der-Engine unterstützt werden, ist dies die einfachste und gekapselte Funktion.</span><span class="sxs-lookup"><span data-stu-id="133fe-107">With multiple backup methods supported by the engine, this is the simplest and most encapsulated function.</span></span>

<span data-ttu-id="133fe-108">**Windows XP: jetbackupinstance** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="133fe-108">**Windows XP:  JetBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a><span data-ttu-id="133fe-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="133fe-109">Parameters</span></span>

<span data-ttu-id="133fe-110">*lichen*</span><span class="sxs-lookup"><span data-stu-id="133fe-110">*instance*</span></span>

<span data-ttu-id="133fe-111">Die Instanz der Datenbank, die gesichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="133fe-111">The instance of the database to backup.</span></span>

<span data-ttu-id="133fe-112">*szbackuppath*</span><span class="sxs-lookup"><span data-stu-id="133fe-112">*szBackupPath*</span></span>

<span data-ttu-id="133fe-113">Das Verzeichnis, in dem die Sicherung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="133fe-113">The directory where the backup is stored.</span></span> <span data-ttu-id="133fe-114">Wenn der Sicherungs Pfad für die Verwendung von NULL ist, schneidet die-Funktion die Protokolle ab, sofern dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="133fe-114">If the backup path is NULL to use the function will truncate the logs, if possible.</span></span>

<span data-ttu-id="133fe-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="133fe-115">*grbit*</span></span>

<span data-ttu-id="133fe-116">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="133fe-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="133fe-117">Wert</span><span class="sxs-lookup"><span data-stu-id="133fe-117">Value</span></span></p></th>
<th><p><span data-ttu-id="133fe-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="133fe-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="133fe-119">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="133fe-119">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="133fe-120">Erstellt eine vollständige Sicherung der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="133fe-120">Creates a full backup of the database.</span></span> <span data-ttu-id="133fe-121">Dies ermöglicht die Beibehaltung einer vorhandenen Sicherung im gleichen Verzeichnis, wenn die neue Sicherung nicht ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="133fe-121">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="133fe-122">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="133fe-122">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="133fe-123">Erstellt im Gegensatz zu einer vollständigen Sicherung eine inkrementelle Sicherung.</span><span class="sxs-lookup"><span data-stu-id="133fe-123">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="133fe-124">Dies bedeutet, dass nur die Protokolldateien gesichert werden, die seit der letzten vollständigen oder inkrementellen Sicherung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="133fe-124">This means that only the log files created since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="133fe-125">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="133fe-125">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="133fe-126">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="133fe-126">Reserved for future use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="133fe-127">*pfnstatus*</span><span class="sxs-lookup"><span data-stu-id="133fe-127">*pfnStatus*</span></span>

<span data-ttu-id="133fe-128">Ein Zeiger auf die [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) Callback-Funktion, die Benachrichtigungs Informationen zum Fortschritt des Sicherungs Vorgangs bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="133fe-128">Pointer to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function, which provides notification information about the progress of the backup operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="133fe-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="133fe-129">Return Value</span></span>

<span data-ttu-id="133fe-130">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="133fe-130">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="133fe-131">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="133fe-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="133fe-132">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="133fe-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="133fe-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="133fe-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="133fe-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="133fe-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="133fe-135">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="133fe-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="133fe-136">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="133fe-136">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="133fe-137">Für dieselbe Instanz wird bereits eine Sicherung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="133fe-137">A backup is already in progress for the same instance.</span></span> <span data-ttu-id="133fe-138">Mehrere Sicherungen sind gleichzeitig nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="133fe-138">Multiple backups are not allowed at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="133fe-139">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="133fe-139">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="133fe-140">Die Instanz ist noch nicht für die Sicherung bereit, während Sie initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="133fe-140">The instance is not ready yet for backup as it is initializing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="133fe-141">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="133fe-141">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="133fe-142">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg294108(v=exchg.10).md">jetstopserviceinstance</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="133fe-142">The operation cannot complete because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="133fe-143">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="133fe-143">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="133fe-144">Der Vorgang kann nicht ausgeführt werden, da der der Sitzung zugeordnete-Instanz einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="133fe-144">The operation cannot complete because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="133fe-145"><strong>Windows XP:  </strong> Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="133fe-145"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="133fe-146">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="133fe-146">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="133fe-147">Eine inkrementelle Sicherung ist nicht zulässig, wenn die zirkuläre Protokollierung on</span><span class="sxs-lookup"><span data-stu-id="133fe-147">An incremental backup is not allowed if circular logging is on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="133fe-148">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="133fe-148">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="133fe-149">Die angegebenen Optionen sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="133fe-149">The specified options are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="133fe-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="133fe-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="133fe-151">Ein ungültiger Parameter wurde an die API übergeben.</span><span class="sxs-lookup"><span data-stu-id="133fe-151">An invalid parameter was passed into the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="133fe-152">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="133fe-152">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="133fe-153">Der Zielpfad ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="133fe-153">The destination path does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="133fe-154">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="133fe-154">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="133fe-155">Die Instanz wird ohne Protokollierung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="133fe-155">The instance is running without logging.</span></span> <span data-ttu-id="133fe-156">Es ist keine Sicherung zulässig.</span><span class="sxs-lookup"><span data-stu-id="133fe-156">No backup is allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="133fe-157">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="133fe-157">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="133fe-158">Bei einer Protokolldatei ist ein Prüfsummen Überprüfungs Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="133fe-158">There was a checksum verification error on a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="133fe-159">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="133fe-159">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="133fe-160">Die Protokollierung für die Instanz ist aufgrund eines unerwarteten Fehlers temporär oder dauerhaft deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="133fe-160">The logging for the instance is temporary or permanently disabled due to an unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="133fe-161">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="133fe-161">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="133fe-162">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="133fe-162">The operation cannot complete because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="133fe-163">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="133fe-163">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="133fe-164">Auf einer Datenbankseite ist ein Prüfsummen Überprüfungs Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="133fe-164">There was a checksum verification error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="133fe-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="133fe-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="133fe-166">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="133fe-166">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="133fe-167">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="133fe-167">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="133fe-168">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="133fe-168">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="133fe-169"><strong>Windows XP:  </strong> Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="133fe-169"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="133fe-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="133fe-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="133fe-171">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="133fe-171">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="133fe-172">Nachdem die Funktion erfolgreich zurückgegeben wurde, sind im Sicherungs Verzeichnis alle Dateien vorhanden, die für eine Wiederherstellung bis zum Zeitpunkt der Sicherung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="133fe-172">After the function returns success, in the backup directory all the files needed for a restore up to the moment of the backup will be present.</span></span> <span data-ttu-id="133fe-173">Wenn es sich um eine vollständige Sicherung handelt, sind die Dateien die Datenbankdateien und die Protokolldateien, die erforderlich sind, um die Datenbank in einen konsistenten Zustand zu bringen.</span><span class="sxs-lookup"><span data-stu-id="133fe-173">If this is a full backup, the files will be the database files and the log files needed to bring the database to a consistent state.</span></span> <span data-ttu-id="133fe-174">Wenn es sich um eine inkrementelle Sicherung handelt, werden den Verzeichnissen nur Protokolldateien hinzugefügt, aber die bereits vorhandenen Dateien (Datenbanken und Protokolldateien) zusammen mit den neuen Protokolldateien können wieder hergestellt werden, und die Datenbank wird zum Zeitpunkt der Sicherung wieder in den Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="133fe-174">If this is an incremental backup, only log files will be added to the directories but the already existing files (databases and log files) together with the new log files will be able to be restored and bring the database back to the state at the moment of the backup.</span></span>

<span data-ttu-id="133fe-175">Als Nebeneffekt der Sicherung werden die Protokolldateien, die nicht mehr benötigt werden, abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="133fe-175">As a side effect of the backup, the log files which are not longer needed will be truncated.</span></span>

<span data-ttu-id="133fe-176">Gleichzeitig werden die Daten Bank Header mit den Informationen aktualisiert, wann die letzte Sicherung erfolgte.</span><span class="sxs-lookup"><span data-stu-id="133fe-176">In the same time, the database headers will be updated with the information when the last backup took place.</span></span>

<span data-ttu-id="133fe-177">Bei einem Fehler werden keine Dateien im Sicherungs Verzeichnis Ziel vorhanden sein, sodass keine Wiederherstellung möglich ist.</span><span class="sxs-lookup"><span data-stu-id="133fe-177">On failure, there will not be any files in the backup directory destination so no restore will be possible.</span></span> <span data-ttu-id="133fe-178">Gleichzeitig werden die aktuellen Protokolldateien nicht abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="133fe-178">In the same time, the current log files will not be truncated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="133fe-179">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="133fe-179">Remarks</span></span>

<span data-ttu-id="133fe-180">In den verschiedenen Schritten der Sicherung werden Ereignisprotokoll Einträge generiert, einschließlich der Dateinamen, der Protokoll Verkürzung und des Endergebnisses der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="133fe-180">The different steps of the backup will have Event Log entries generated including the file names, the log truncation and the final result of the backup.</span></span>

<span data-ttu-id="133fe-181">Die inkrementelle Sicherung ist nur möglich, nachdem eine vollständige Sicherung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="133fe-181">Incremental backup are possible only after a full backup was taken.</span></span> <span data-ttu-id="133fe-182">Außerdem sind inkrementelle Sicherungen nur möglich, wenn die zirkuläre Protokollierung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="133fe-182">Also, incremental backups are possible only if circular logging is turned off.</span></span> <span data-ttu-id="133fe-183">Es wird empfohlen, dass das Sicherungs Verzeichnis keine anderen Dateien enthält, dann das, das in der Sicherung enthalten ist, oder das von einer vorherigen erfolgreichen Sicherung hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="133fe-183">It is recommended that the backup directory should not contain other files then the one involved in the backup or added by a previous successful backup.</span></span>

<span data-ttu-id="133fe-184">Das Sicherungs Verzeichnis sollte vorhanden sein, es sei denn, der Parameter *JET_paramCreatePathIfNotExist* für die Instanz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="133fe-184">The backup directory should exist unless the parameter *JET_paramCreatePathIfNotExist* is set for the instance.</span></span> <span data-ttu-id="133fe-185">Weitere Informationen finden Sie unter [System Parameter](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="133fe-185">For information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="133fe-186">Bei der Sicherung wird die Prüfsummen Überprüfung auf allen verwendeten Datenbankseiten und beginnend mit Windows Server 2003 in den Protokolldateien durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="133fe-186">The backup will do checksum verification on all the used database pages and starting with Windows Server 2003, on the log files as well.</span></span> <span data-ttu-id="133fe-187">Dadurch haben Sie die Möglichkeit, die Integrität der Datenbank zu schätzen, auch für Seiten, die während des normalen Betriebs nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="133fe-187">This gives an opportunity to estimate the health of the database even for pages which are not read during normal operations.</span></span> <span data-ttu-id="133fe-188">Wenn eine solche Beschädigung auftritt, tritt bei der Sicherung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="133fe-188">If any such corruption will be encountered, the backup will fail.</span></span>

<span data-ttu-id="133fe-189">Während der Sicherung wird die aktuelle Protokolldatei fertiggestellt, und es wird eine neue Protokoll Generierung gestartet.</span><span class="sxs-lookup"><span data-stu-id="133fe-189">During the backup, the current log file will be finished and we will start a new log generation.</span></span> <span data-ttu-id="133fe-190">Dadurch wird das Kopieren der erforderlichen Protokolldateien ermöglicht, da das letzte benötigte Protokoll nicht mehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="133fe-190">This will allow copying the needed log files because the last needed one will not be in use anymore.</span></span>

<span data-ttu-id="133fe-191">Es wird dringend empfohlen, die Sicherung nicht für andere Zwecke der Sicherung zu verwenden und auf der Engine-Ebene wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="133fe-191">It is strongly recommended that the backup should not be used for other purposed other then the backup and restored at the engine level.</span></span> <span data-ttu-id="133fe-192">Dadurch wird die Änderung von Fehlern bei Sicherungs-und Wiederherstellungs Vorgängen minimiert.</span><span class="sxs-lookup"><span data-stu-id="133fe-192">This will minimize the change of getting errors during the backup and restore operations.</span></span>

#### <a name="requirements"></a><span data-ttu-id="133fe-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="133fe-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="133fe-194"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="133fe-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="133fe-195">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="133fe-195">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="133fe-196"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="133fe-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="133fe-197">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="133fe-197">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="133fe-198"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="133fe-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="133fe-199">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="133fe-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="133fe-200"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="133fe-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="133fe-201">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="133fe-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="133fe-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="133fe-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="133fe-203">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="133fe-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="133fe-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="133fe-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="133fe-205">Implementiert als <strong>jetbackupinstancew</strong> (Unicode) und <strong>jetbackupinstancea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="133fe-205">Implemented as <strong>JetBackupInstanceW</strong> (Unicode) and <strong>JetBackupInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="133fe-206">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="133fe-206">See Also</span></span>

[<span data-ttu-id="133fe-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="133fe-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="133fe-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="133fe-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="133fe-209">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="133fe-209">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="133fe-210">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="133fe-210">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="133fe-211">Jetrestore</span><span class="sxs-lookup"><span data-stu-id="133fe-211">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="133fe-212">JetRestore2</span><span class="sxs-lookup"><span data-stu-id="133fe-212">JetRestore2</span></span>](./jetrestore2-function.md)  
[<span data-ttu-id="133fe-213">Jetrestoreingestance</span><span class="sxs-lookup"><span data-stu-id="133fe-213">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="133fe-214">Jetstopserviczustance</span><span class="sxs-lookup"><span data-stu-id="133fe-214">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)  
[<span data-ttu-id="133fe-215">System Parameter</span><span class="sxs-lookup"><span data-stu-id="133fe-215">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
