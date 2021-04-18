---
description: 'Weitere Informationen finden Sie hier: JetEndExternalBackupInstance2-Funktion'
title: JetEndExternalBackupInstance2-Funktion
TOCTitle: JetEndExternalBackupInstance2 Function
ms:assetid: a30961f7-a1fb-44fe-881a-d46bf8f743b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294047(v=EXCHG.10)
ms:contentKeyID: 32765646
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17e719885cc61ff3f3193046b632e9969b8d660f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347694"
---
# <a name="jetendexternalbackupinstance2-function"></a><span data-ttu-id="296f8-103">JetEndExternalBackupInstance2-Funktion</span><span class="sxs-lookup"><span data-stu-id="296f8-103">JetEndExternalBackupInstance2 Function</span></span>


<span data-ttu-id="296f8-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="296f8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackupinstance2-function"></a><span data-ttu-id="296f8-105">JetEndExternalBackupInstance2-Funktion</span><span class="sxs-lookup"><span data-stu-id="296f8-105">JetEndExternalBackupInstance2 Function</span></span>

<span data-ttu-id="296f8-106">Die **JetEndExternalBackupInstance2** -Funktion beendet eine externe Sicherungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="296f8-106">The **JetEndExternalBackupInstance2** function ends an external backup session.</span></span> <span data-ttu-id="296f8-107">Diese API ist die letzte API in einer Reihe von APIs, die aufgerufen werden muss, um eine erfolgreiche (nicht auf VSS basierende) Online Sicherung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="296f8-107">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="296f8-108">**Windows XP: JetEndExternalBackupInstance2** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="296f8-108">**Windows XP:  JetEndExternalBackupInstance2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="296f8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="296f8-109">Parameters</span></span>

<span data-ttu-id="296f8-110">*lichen*</span><span class="sxs-lookup"><span data-stu-id="296f8-110">*instance*</span></span>

<span data-ttu-id="296f8-111">Die-Instanz, die für diesen Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="296f8-111">The instance to use for this call.</span></span>

<span data-ttu-id="296f8-112">**Windows 2000:** Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="296f8-112">**Windows 2000:** For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="296f8-113">In diesem Fall wird die Verwendung dieser globalen Instanz impliziert.</span><span class="sxs-lookup"><span data-stu-id="296f8-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="296f8-114">**Windows XP:** Für Windows XP und spätere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) befindet, in dem nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="296f8-114">**Windows XP:** For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="296f8-115">Andernfalls schlägt der Vorgang mit JET_errRunningInMultiInstanceMode fehl.</span><span class="sxs-lookup"><span data-stu-id="296f8-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="296f8-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="296f8-116">*grbit*</span></span>

<span data-ttu-id="296f8-117">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="296f8-117">A group of bits that specifies zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="296f8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="296f8-118">Value</span></span></p></th>
<th><p><span data-ttu-id="296f8-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="296f8-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="296f8-120">JET_bitBackupEndAbort</span><span class="sxs-lookup"><span data-stu-id="296f8-120">JET_bitBackupEndAbort</span></span><br />
<span data-ttu-id="296f8-121">0x0002</span><span class="sxs-lookup"><span data-stu-id="296f8-121">0x0002</span></span></p></td>
<td><p><span data-ttu-id="296f8-122">Die Sicherung wird von der Client Anwendung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="296f8-122">The client application is aborting the backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="296f8-123">JET_bitBackupEndNormal</span><span class="sxs-lookup"><span data-stu-id="296f8-123">JET_bitBackupEndNormal</span></span><br />
<span data-ttu-id="296f8-124">0x0001</span><span class="sxs-lookup"><span data-stu-id="296f8-124">0x0001</span></span></p></td>
<td><p><span data-ttu-id="296f8-125">Die Client Anwendung hat die Sicherung vollständig abgeschlossen und wird normal beendet.</span><span class="sxs-lookup"><span data-stu-id="296f8-125">The client application finished the backup completely, and is ending normally.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="296f8-126">JET_bitBackupTruncateDone</span><span class="sxs-lookup"><span data-stu-id="296f8-126">JET_bitBackupTruncateDone</span></span><br />
<span data-ttu-id="296f8-127">0x0100</span><span class="sxs-lookup"><span data-stu-id="296f8-127">0x0100</span></span></p></td>
<td><p><span data-ttu-id="296f8-128"><strong>Windows Vista:  </strong> JET_bitBackupTruncateDone wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="296f8-128"><strong>Windows Vista:  </strong>JET_bitBackupTruncateDone is introduced in Windows Vista.</span></span></p>
<p><span data-ttu-id="296f8-129">Die Engine kann die Daten Bank Header nach Bedarf markieren (z. b. eine vollständige Sicherung abgeschlossen), obwohl der Abschneidevorgang nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="296f8-129">The engine can mark the database headers as appropriate (for example, a full backup completed), even though the call to truncate was not completed.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="296f8-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="296f8-130">Return Value</span></span>

<span data-ttu-id="296f8-131">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="296f8-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="296f8-132">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="296f8-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="296f8-133">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="296f8-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="296f8-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="296f8-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="296f8-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="296f8-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="296f8-136">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="296f8-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="296f8-137">JET_errBackupAbortByCaller</span><span class="sxs-lookup"><span data-stu-id="296f8-137">JET_errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="296f8-138"><strong>Windows XP:  </strong> Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="296f8-138"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="296f8-139">Der Aufrufer hat eine Sicherung in der Mitte der Sicherungs Sequenz beendet, ohne die Absicht mit <a href="gg294067(v=exchg.10).md">jetstopbackup</a>zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="296f8-139">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="296f8-140">Dieser Fehler ist das Ergebnis eines Fehlers im Sicherungs Client in Windows Server 2003 und höher.</span><span class="sxs-lookup"><span data-stu-id="296f8-140">This error is result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="296f8-141">In Windows XP wird dieser Fehler für eine absichtliche Beendigung der externen Sicherungs Sequenz zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="296f8-141">In Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="296f8-142">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="296f8-142">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="296f8-143"><strong>Windows Server 2003:  </strong> Dieser Rückgabewert wird in Windows Server 2003 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="296f8-143"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="296f8-144">Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen <a href="gg294067(v=exchg.10).md">jetstopbackup</a>-Befehl abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="296f8-144">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="296f8-145">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="296f8-145">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="296f8-146">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="296f8-146">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="296f8-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="296f8-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="296f8-148"><strong>Windows XP:  </strong> Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="296f8-148"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="296f8-149">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität dieser Daten zu schützen</span><span class="sxs-lookup"><span data-stu-id="296f8-149">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="296f8-150">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="296f8-150">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="296f8-151">Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="296f8-151">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="296f8-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="296f8-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="296f8-153">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="296f8-153">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="296f8-154">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="296f8-154">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="296f8-155">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="296f8-155">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="296f8-156">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="296f8-156">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="296f8-157">Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn in der Tat mehrere Instanzen bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="296f8-157">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="296f8-158">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="296f8-158">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="296f8-159">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="296f8-159">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="296f8-160">Wenn die Funktion erfolgreich ausgeführt wird, war die externe Sicherung erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="296f8-160">If the function succeeds, the external backup was a success.</span></span> <span data-ttu-id="296f8-161">Erfolg gibt an, dass alle Dateien (z. b. Datenbanken und Protokolle), die für den Sicherungstyp (in [jetbeginexternalbackup](./jetbeginexternalbackup-function.md)angegeben) geeignet sind, von der Sicherungs-Engine abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="296f8-161">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="296f8-162">Die gesicherten Dateien können mit Hard Recovery ([jetexternalrestore](./jetexternalrestore-function.md)) wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="296f8-162">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="296f8-163">Wenn diese Funktion fehlschlägt, wird die externe Sicherung normalerweise beendet.</span><span class="sxs-lookup"><span data-stu-id="296f8-163">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="296f8-164">"Fehler" bedeutet, dass die Sicherung aufgrund eines Fehlers bei der Client-oder Anwendungs Verwendung ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="296f8-164">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="296f8-165">Es ist wichtig, den Rückgabecode für diese API zu überprüfen, um zu überprüfen, ob die Sicherungs Sequenz erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="296f8-165">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="296f8-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="296f8-166">Remarks</span></span>

<span data-ttu-id="296f8-167">Wenn die Engine zum Protokollieren von Ereignissen konfiguriert ist, wird ein Ereignis protokolliert, um die Auflösung der externen Sicherung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="296f8-167">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="296f8-168">Wenn die Sicherungs Sequenz nicht in der richtigen Reihenfolge und mit einem erfolgreichen Rückruf von [jetendexternalbackup](./jetendexternalbackup-function.md)abgeschlossen ist, können nachfolgende inkrementelle Sicherungen mehr Daten enthalten, als die Anwendung erwartet hat.</span><span class="sxs-lookup"><span data-stu-id="296f8-168">If the backup sequence is not completed in order and with a successful call to [JetEndExternalBackup](./jetendexternalbackup-function.md), subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="296f8-169">Weitere Informationen zur API-Sequenz für die externe Sicherung finden Sie unter [jetbeginexternalbackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="296f8-169">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="296f8-170">Vor Windows Vista hat die Engine, wenn die Protokoll Verkürzung nicht durchgeführt wurde, die Sicherung als Kopier Sicherung angesehen.</span><span class="sxs-lookup"><span data-stu-id="296f8-170">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="296f8-171">Allerdings kann es sich bei der Sicherung um eine normale Sicherung handeln, bei der die abkürzen nicht durchgeführt wurde (z. b. Wenn separate Datenbanken vorhanden sind).</span><span class="sxs-lookup"><span data-stu-id="296f8-171">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="296f8-172">Mithilfe der Option JET_bitBackupTruncateDone können Sie die Engine über diese Informationen informieren und entsprechende Daten Bank Header Änderungen zulassen.</span><span class="sxs-lookup"><span data-stu-id="296f8-172">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow appropriate database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="296f8-173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="296f8-173">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="296f8-174"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="296f8-174"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="296f8-175">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="296f8-175">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="296f8-176"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="296f8-176"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="296f8-177">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="296f8-177">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="296f8-178"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="296f8-178"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="296f8-179">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="296f8-179">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="296f8-180"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="296f8-180"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="296f8-181">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="296f8-181">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="296f8-182"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="296f8-182"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="296f8-183">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="296f8-183">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="296f8-184">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="296f8-184">See Also</span></span>

[<span data-ttu-id="296f8-185">Fehler Behandlungsparameter</span><span class="sxs-lookup"><span data-stu-id="296f8-185">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="296f8-186">Erweiterbare Speicher-Engine-Fehler</span><span class="sxs-lookup"><span data-stu-id="296f8-186">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="296f8-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="296f8-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="296f8-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="296f8-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="296f8-189">Jetattachdatabase</span><span class="sxs-lookup"><span data-stu-id="296f8-189">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="296f8-190">Jetbeginexternalbackup</span><span class="sxs-lookup"><span data-stu-id="296f8-190">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="296f8-191">Jetbeginexternalbackupinstance</span><span class="sxs-lookup"><span data-stu-id="296f8-191">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="296f8-192">Jetclosefile</span><span class="sxs-lookup"><span data-stu-id="296f8-192">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="296f8-193">Jetexternalrestore</span><span class="sxs-lookup"><span data-stu-id="296f8-193">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="296f8-194">Jetgetattachinfo</span><span class="sxs-lookup"><span data-stu-id="296f8-194">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="296f8-195">Jetgetloginfo</span><span class="sxs-lookup"><span data-stu-id="296f8-195">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="296f8-196">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="296f8-196">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="296f8-197">Jetopumfile</span><span class="sxs-lookup"><span data-stu-id="296f8-197">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="296f8-198">Jetreadfile</span><span class="sxs-lookup"><span data-stu-id="296f8-198">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="296f8-199">Jetstopbackup</span><span class="sxs-lookup"><span data-stu-id="296f8-199">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="296f8-200">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="296f8-200">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="296f8-201">Jettruneurelog</span><span class="sxs-lookup"><span data-stu-id="296f8-201">JetTruncateLog</span></span>](./jettruncatelog-function.md)
