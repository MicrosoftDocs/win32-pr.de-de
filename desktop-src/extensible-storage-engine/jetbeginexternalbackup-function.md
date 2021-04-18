---
description: Weitere Informationen finden Sie in der jetbeginexternalbackup-Funktion.
title: Jetbeginexternalbackup-Funktion
TOCTitle: JetBeginExternalBackup Function
ms:assetid: 702e6cbf-4648-40f2-b2eb-6194759d4cde
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269292(v=EXCHG.10)
ms:contentKeyID: 32765584
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d410adb592c3d56d2f9880ec809749396318258a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351076"
---
# <a name="jetbeginexternalbackup-function"></a><span data-ttu-id="98a42-103">Jetbeginexternalbackup-Funktion</span><span class="sxs-lookup"><span data-stu-id="98a42-103">JetBeginExternalBackup Function</span></span>


<span data-ttu-id="98a42-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="98a42-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginexternalbackup-function"></a><span data-ttu-id="98a42-105">Jetbeginexternalbackup-Funktion</span><span class="sxs-lookup"><span data-stu-id="98a42-105">JetBeginExternalBackup Function</span></span>

<span data-ttu-id="98a42-106">Die **jetbeginexternalbackup** -Funktion initiiert eine externe Sicherung, während die Engine und die Datenbank online und aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="98a42-106">The **JetBeginExternalBackup** function initiates an external backup while the engine and database is online and active.</span></span> <span data-ttu-id="98a42-107">**Jetbeginexternalbackup** ist das erste in einer Reihe von Funktionen, die aufgerufen werden müssen, um eine erfolgreiche (nicht auf VSS basierende) Online Sicherung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="98a42-107">**JetBeginExternalBackup** is the first in a series of functions that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="98a42-108">Eine externe Sicherung kann zum Implementieren von vollständigen, inkrementellen oder differenziellen Sicherungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="98a42-108">An external backup can be used to implement full, incremental, or differential backups.</span></span>

<span data-ttu-id="98a42-109">Bei der Sicherung handelt es sich um einen fuzzywert, da die Sicherung mit einem bestimmten Zeitpunkt im Transaktionsverlauf konsistent ist, aber das Steuern des genauen Zeitraums nicht möglich ist.</span><span class="sxs-lookup"><span data-stu-id="98a42-109">The backup will be fuzzy, in that the backup will be consistent to a single point in time in the transaction history, but controlling the exact point in time is not possible.</span></span>

```cpp
    JET_ERR JET_API JetBeginExternalBackup(
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="98a42-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="98a42-110">Parameters</span></span>

<span data-ttu-id="98a42-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="98a42-111">*grbit*</span></span>

<span data-ttu-id="98a42-112">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angeben.</span><span class="sxs-lookup"><span data-stu-id="98a42-112">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="98a42-113">Wert</span><span class="sxs-lookup"><span data-stu-id="98a42-113">Value</span></span></p></th>
<th><p><span data-ttu-id="98a42-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="98a42-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98a42-115">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="98a42-115">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="98a42-116">Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="98a42-116">This flag is deprecated.</span></span> <span data-ttu-id="98a42-117">Die Verwendung dieses Bits führt dazu, dass JET_errInvalidgrbit zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="98a42-117">Usage of this bit will result in JET_errInvalidgrbit being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98a42-118">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="98a42-118">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="98a42-119">Erstellt im Gegensatz zu einer vollständigen Sicherung eine inkrementelle Sicherung.</span><span class="sxs-lookup"><span data-stu-id="98a42-119">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="98a42-120">Dies bedeutet, dass nur die Protokolldateien seit der letzten vollständigen oder inkrementellen Sicherung gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="98a42-120">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98a42-121">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="98a42-121">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="98a42-122">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="98a42-122">Reserved for future use.</span></span> <span data-ttu-id="98a42-123">Definiert für Windows XP.</span><span class="sxs-lookup"><span data-stu-id="98a42-123">Defined for Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="98a42-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98a42-124">Return Value</span></span>

<span data-ttu-id="98a42-125">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="98a42-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="98a42-126">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="98a42-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="98a42-127">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="98a42-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="98a42-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98a42-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98a42-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="98a42-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="98a42-130">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="98a42-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98a42-131">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="98a42-131">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="98a42-132">Wenn bereits eine externe Sicherung oder Momentaufnahme Sicherung in Verarbeitung ist, wird dieser Fehler zurückgegeben, bis <strong>jetbeginexternalbackup</strong> (oder eine der Varianten davon) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="98a42-132">If an external backup or snapshot backup is already in process, this error will be returned, until <strong>JetBeginExternalBackup</strong> (or one of the variants of it) is called.</span></span> <span data-ttu-id="98a42-133">ESE ermöglicht jeweils nur eine Online Sicherung.</span><span class="sxs-lookup"><span data-stu-id="98a42-133">ESE allows only one online backup at a time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98a42-134">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="98a42-134">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="98a42-135">Die Instanz oder Datenbank-Engine befindet sich entweder in der Wiederherstellung oder in einer Beendigungs-oder Beendigungs Phase.</span><span class="sxs-lookup"><span data-stu-id="98a42-135">The instance or database engine is either in recovery or in a shutdown or termination phase.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98a42-136">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="98a42-136">JET_errCheckpointCorrupt</span></span></p></td>
<td><p><span data-ttu-id="98a42-137">Bei einer vollständigen Sicherung konnte die Prüf Punkt Datei nicht gelesen werden, oder die Datei konnte nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="98a42-137">On a full backup, the checkpoint file could not be read, or the file could not be verified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98a42-138">JET_errCheckpointFileNotFound</span><span class="sxs-lookup"><span data-stu-id="98a42-138">JET_errCheckpointFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="98a42-139">Bei einer vollständigen Sicherung konnte die Prüf Punkt Datei nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="98a42-139">On a full backup, the checkpoint file could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98a42-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="98a42-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="98a42-141">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="98a42-141">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98a42-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="98a42-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="98a42-143">Der Vorgang kann nicht ausgeführt werden, da der-Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="98a42-143">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="98a42-144"><strong>Windows XP:  </strong> Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="98a42-144"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98a42-145">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="98a42-145">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="98a42-146">Die zirkuläre Protokollierung ist aktiviert, und der angegebene Sicherungstyp ist JET_bitBackupIncremental.</span><span class="sxs-lookup"><span data-stu-id="98a42-146">Circular logging is enabled and the backup type specified is JET_bitBackupIncremental.</span></span> <span data-ttu-id="98a42-147">Informationen dazu, wie Sie zirkuläre oder nicht zirkuläre Protokollierung steuern, finden Sie unter <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> in den <strong>Transaktionsprotokoll Fehlern</strong> .</span><span class="sxs-lookup"><span data-stu-id="98a42-147">See <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> in the <strong>Transaction Log Errors</strong> for information about how to control circular or non-circular logging.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98a42-148">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="98a42-148">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="98a42-149">Mindestens ein <em>grbit</em> -Member war ungültig.</span><span class="sxs-lookup"><span data-stu-id="98a42-149">One or more of the <em>grbit</em> members was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98a42-150">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="98a42-150">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="98a42-151">Wiederherstellung oder Protokollierung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="98a42-151">Recovery or logging is disabled.</span></span> <span data-ttu-id="98a42-152">Wenn die Protokollierung deaktiviert ist, können Sie keine Online Sicherung durchführen.</span><span class="sxs-lookup"><span data-stu-id="98a42-152">You cannot do an online backup if logging is disabled.</span></span> <span data-ttu-id="98a42-153">Weitere Informationen zur Protokollierung und Wiederherstellung finden Sie unter <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</span><span class="sxs-lookup"><span data-stu-id="98a42-153">For more information about logging and recovery, see <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98a42-154">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="98a42-154">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="98a42-155">Die Engine hat das Schreiben auf das Protokoll Laufwerk beendet, da die Protokolldatei voll ist oder die e/a-Fehler aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="98a42-155">The engine has stopped writing to the log drive, due to log being full or disk IO errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98a42-156">JET_errMissingFullBackup</span><span class="sxs-lookup"><span data-stu-id="98a42-156">JET_errMissingFullBackup</span></span></p></td>
<td><p><span data-ttu-id="98a42-157">Die inkrementelle Sicherung wurde angegeben (mit JET_bitBackupIncremental), und nie war eine vollständige Sicherung für eine der angefügten Datenbanken für den Protokollierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="98a42-157">The incremental backup was specified (with JET_bitBackupIncremental), and never was a full backup taken for one of the attached databases for the logging set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98a42-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="98a42-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="98a42-159">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="98a42-159">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98a42-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="98a42-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="98a42-161">Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="98a42-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98a42-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="98a42-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="98a42-163">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="98a42-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98a42-164">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="98a42-164">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="98a42-165">Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="98a42-165">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98a42-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="98a42-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="98a42-167">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="98a42-167">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="98a42-168">Wenn die Funktion erfolgreich ausgeführt wird, wird eine externe Sicherung initiiert, und die Sicherungs Zustands-Engine wird initialisiert.</span><span class="sxs-lookup"><span data-stu-id="98a42-168">If the function succeeds, an external backup is initiated and the backup state engine is initialized.</span></span> <span data-ttu-id="98a42-169">Nachfolgende APIs können jetzt aufgerufen werden, um die externe Sicherungs Sequenz und den Stream abzuschließen oder die Datenbankdatei, die Datenbank-Patchdatei (falls unterstützt) und die Protokolldatei auszulesen.</span><span class="sxs-lookup"><span data-stu-id="98a42-169">Subsequent APIs can now be called to complete the external backup sequence and stream or read off the database file, the database patch file (if supported), and the log file.</span></span> <span data-ttu-id="98a42-170">Ein Ereignis kann protokolliert werden, dass eine externe Sicherung begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="98a42-170">An event can be logged that an external backup has begun.</span></span>

<span data-ttu-id="98a42-171">Wenn die Funktion fehlschlägt, wird die Sicherungs Sitzung nicht initiiert.</span><span class="sxs-lookup"><span data-stu-id="98a42-171">If the function fails, the backup session will not be initiated.</span></span> <span data-ttu-id="98a42-172">Wenn eine andere Sicherungs Sitzung ausgeführt wird, wird Sie nicht abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="98a42-172">If another backup session is in progress, it will not be cancelled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="98a42-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98a42-173">Remarks</span></span>

<span data-ttu-id="98a42-174">Der externe Sicherungsprozess (wie von **jetbeginexternalbackup** gestartet) ist so konzipiert, dass eine Fuzzy Transaction-Online Sicherung der gesamten Instanz auf einem Zielgerät als Stream zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="98a42-174">The external backup process (as started by **JetBeginExternalBackup**) is designed to allow a fuzzy transaction online backup of the entire instance to a target device as a stream.</span></span> <span data-ttu-id="98a42-175">Die Sicherung enthält alle Datenbankdateien, die mithilfe von [jetattachdatabase](./jetattachdatabase-function.md) (für eine vollständige Sicherung) an die Instanz angefügt sind, gefolgt von den zugehörigen datenbankpatchdateien (falls unterstützt), und schließlich von den Transaktionsprotokoll Dateien, die während des Sicherungs Vorgangs generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="98a42-175">The backup will contain all the database files that are attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) (for a full backup), followed by their associated database patch files (if supported), and finally by the transaction log files that were generated during the backup process.</span></span> <span data-ttu-id="98a42-176">Das Endergebnis ist ein Satz von Dateien, der aus dem Stream wieder hergestellt werden kann, möglicherweise mit vorhandenen Datenbank-und Protokolldateien kombiniert und schließlich in einem konsistenten Zustand wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="98a42-176">The end result will be a set of files that can be restored from the stream, possibly combined with existing database and log files, and finally recovered to a consistent state.</span></span>

<span data-ttu-id="98a42-177">Die allgemeine Reihenfolge von Vorgängen für eine vollständige Sicherung besteht aus den folgenden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="98a42-177">The general order of operations for a full backup consists of the following calls.</span></span> <span data-ttu-id="98a42-178">Zuerst wird **jetbeginexternalbackup** aufgerufen, um den Sicherungsprozess zu starten.</span><span class="sxs-lookup"><span data-stu-id="98a42-178">First, **JetBeginExternalBackup** is called to start the backup process.</span></span> <span data-ttu-id="98a42-179">Anschließend wird [jetgetattachinfo](./jetgetattachinfo-function.md) aufgerufen, um die Liste der Datenbanken zu erhalten, die an die zu sichernde Instanz angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="98a42-179">Then, [JetGetAttachInfo](./jetgetattachinfo-function.md) is called to get the list of databases that are attached to the instance that needs to be backed up.</span></span> <span data-ttu-id="98a42-180">Für jede dieser Datenbanken wird [jetopumfile](./jetopenfile-function.md) aufgerufen, gefolgt von einer Reihe von [jetreadfile](./jetreadfile-function.md) -aufrufen und dann durch einen Aufruf von [jetclosefile](./jetclosefile-function.md).</span><span class="sxs-lookup"><span data-stu-id="98a42-180">For each of these databases, [JetOpenFile](./jetopenfile-function.md) is called, followed by a number of [JetReadFile](./jetreadfile-function.md) calls, and then by a call to [JetCloseFile](./jetclosefile-function.md).</span></span> <span data-ttu-id="98a42-181">Anschließend wird [jetgetloginfo](./jetgetloginfo-function.md) aufgerufen, um eine Liste der zu sichernden datenbankpatch-und-Protokolldateien zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="98a42-181">Then, [JetGetLogInfo](./jetgetloginfo-function.md) is called to get a list of database patch and log files to be backed up.</span></span> <span data-ttu-id="98a42-182">Für jede dieser Dateien wird eine weitere Abfolge von [jetopenfile](./jetopenfile-function.md)-, [jetreadfile](./jetreadfile-function.md)-und [jetclosefile](./jetclosefile-function.md) -aufrufen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="98a42-182">For each of these files, another sequence of [JetOpenFile](./jetopenfile-function.md), [JetReadFile](./jetreadfile-function.md), and [JetCloseFile](./jetclosefile-function.md) calls are made.</span></span> <span data-ttu-id="98a42-183">Anschließend werden alle unerwünschten Transaktionsprotokoll Dateien mithilfe von [jettruneurelog](./jettruncatelog-function.md)gelöscht.</span><span class="sxs-lookup"><span data-stu-id="98a42-183">Then, any undesired transaction log files are deleted using [JetTruncateLog](./jettruncatelog-function.md).</span></span> <span data-ttu-id="98a42-184">Schließlich wird die Sicherung durch einen [calltendexternalbackup](./jetendexternalbackup-function.md)-Befehl beendet.</span><span class="sxs-lookup"><span data-stu-id="98a42-184">Finally, the backup is ended by a call to [JetEndExternalBackup](./jetendexternalbackup-function.md).</span></span>

<span data-ttu-id="98a42-185">Es ist auch möglich, diesen Satz von Schritten zu ändern, um eine inkrementelle Sicherung der-Instanz auszuführen.</span><span class="sxs-lookup"><span data-stu-id="98a42-185">It is also possible to modify this set of steps to perform an incremental backup of the instance.</span></span> <span data-ttu-id="98a42-186">Eine inkrementelle Sicherung listet Protokolldateien auf und sichert Sie.</span><span class="sxs-lookup"><span data-stu-id="98a42-186">An incremental backup enumerates and backs up log files.</span></span> <span data-ttu-id="98a42-187">Inkrementelle Sicherungen sind nur möglich, wenn zirkuläre Protokollierung nicht aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="98a42-187">Incremental backups are only possible if circular logging is not enabled.</span></span>

<span data-ttu-id="98a42-188">Es ist auch möglich, diesen Satz von Schritten so zu ändern, dass nachfolgende differenzielle Sicherungen der Instanz ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="98a42-188">It is also possible to modify this set of steps to allow subsequent differential backups of the instance to be performed.</span></span> <span data-ttu-id="98a42-189">Um eine differenzielle Sicherung auszuführen, nennen Sie [jettruneurelog](./jettruncatelog-function.md) nicht in der vorherigen vollständigen oder inkrementellen Sicherung.</span><span class="sxs-lookup"><span data-stu-id="98a42-189">To perform a differential backup, do not call [JetTruncateLog](./jettruncatelog-function.md) in the previous full or incremental backup.</span></span> <span data-ttu-id="98a42-190">Durch das Aufrufen von [jettruneurelog](./jettruncatelog-function.md)können nachfolgende Sicherungen in Bezug auf die letzte vollständige oder inkrementelle Sicherung differenziell sein.</span><span class="sxs-lookup"><span data-stu-id="98a42-190">By not calling [JetTruncateLog](./jettruncatelog-function.md), you enable subsequent backups to be differential with respect to the last full or incremental backup.</span></span> <span data-ttu-id="98a42-191">Differenzielle Sicherungen sind nur möglich, wenn die zirkuläre Protokollierung nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="98a42-191">Differential backups are only possible if circular logging is not enabled.</span></span>

<span data-ttu-id="98a42-192">Die Datenbank-Patchdatei ist eine spezielle Hilfsdatei, die zum Speichern von Datenbankseiten Images unter bestimmten Umständen während der Sicherung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="98a42-192">The database patch file is a special auxiliary file that is used to store database page images under certain circumstances during the backup.</span></span> <span data-ttu-id="98a42-193">Diese Datei muss bei einem Wiederherstellungs Vorgang am gleichen Speicherort wie die zugehörige Datenbank vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="98a42-193">This file must be present in the same location as its associated database during a restore operation.</span></span> <span data-ttu-id="98a42-194">Diese Datei wird nur in Windows 2000 verwendet.</span><span class="sxs-lookup"><span data-stu-id="98a42-194">This file is only used in Windows 2000.</span></span> <span data-ttu-id="98a42-195">Daher müssen alle Anwendungen, die für Windows 2000 und andere Releases geschrieben werden, Daten Bank Patchdateien unterstützen, wenn Sie vorhanden sind, aber auch nicht fehlschlagen dürfen, wenn Sie nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="98a42-195">As a result, any application that is written to work against Windows 2000 and other releases must support database patch files, if they are present, but also must not fail if they are not present.</span></span>

#### <a name="requirements"></a><span data-ttu-id="98a42-196">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98a42-196">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98a42-197"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="98a42-197"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="98a42-198">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="98a42-198">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98a42-199"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="98a42-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="98a42-200">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="98a42-200">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98a42-201"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="98a42-201"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="98a42-202">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="98a42-202">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98a42-203"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="98a42-203"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="98a42-204">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="98a42-204">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98a42-205"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="98a42-205"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="98a42-206">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="98a42-206">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="98a42-207">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="98a42-207">See Also</span></span>

[<span data-ttu-id="98a42-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="98a42-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="98a42-209">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="98a42-209">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="98a42-210">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="98a42-210">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="98a42-211">Jetattachdatabase</span><span class="sxs-lookup"><span data-stu-id="98a42-211">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="98a42-212">Jetbeginexternalbackupinstance</span><span class="sxs-lookup"><span data-stu-id="98a42-212">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="98a42-213">Jetclosefile</span><span class="sxs-lookup"><span data-stu-id="98a42-213">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="98a42-214">Jetendexternalbackup</span><span class="sxs-lookup"><span data-stu-id="98a42-214">JetEndExternalBackup</span></span>](./jetendexternalbackup-function.md)  
[<span data-ttu-id="98a42-215">JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="98a42-215">JetEndExternalBackupInstance2</span></span>](./jetendexternalbackupinstance2-function.md)  
[<span data-ttu-id="98a42-216">Jetgetattachinfo</span><span class="sxs-lookup"><span data-stu-id="98a42-216">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="98a42-217">Jetgetloginfo</span><span class="sxs-lookup"><span data-stu-id="98a42-217">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="98a42-218">Jetopumfile</span><span class="sxs-lookup"><span data-stu-id="98a42-218">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="98a42-219">Jetreadfile</span><span class="sxs-lookup"><span data-stu-id="98a42-219">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="98a42-220">Jetstopbackup</span><span class="sxs-lookup"><span data-stu-id="98a42-220">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="98a42-221">Jettruneurelog</span><span class="sxs-lookup"><span data-stu-id="98a42-221">JetTruncateLog</span></span>](./jettruncatelog-function.md)
