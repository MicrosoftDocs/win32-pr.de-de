---
description: Weitere Informationen finden Sie in der jettruneurelog-Funktion.
title: Jettruneurelog-Funktion
TOCTitle: JetTruncateLog Function
ms:assetid: 60cbf563-4228-452a-9b20-c7b1330c4514
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269263(v=EXCHG.10)
ms:contentKeyID: 32765565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e196a1570f769d8ae2619e962521bb181d506d63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750480"
---
# <a name="jettruncatelog-function"></a><span data-ttu-id="7b2b4-103">Jettruneurelog-Funktion</span><span class="sxs-lookup"><span data-stu-id="7b2b4-103">JetTruncateLog Function</span></span>


<span data-ttu-id="7b2b4-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7b2b4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jettruncatelog-function"></a><span data-ttu-id="7b2b4-105">Jettruneurelog-Funktion</span><span class="sxs-lookup"><span data-stu-id="7b2b4-105">JetTruncateLog Function</span></span>

<span data-ttu-id="7b2b4-106">Die **jettrun-** Funktion wird während einer Sicherung verwendet, die von [jetbeginexternalbackup](./jetbeginexternalbackup-function.md) initiiert wird, um Transaktionsprotokoll Dateien zu löschen, die nicht mehr benötigt werden, nachdem die aktuelle Sicherung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-106">The **JetTruncateLog** function is used during a backup that is initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

```cpp
    JET_ERR JET_API JetTruncateLog(void);
```

### <a name="parameters"></a><span data-ttu-id="7b2b4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b2b4-107">Parameters</span></span>

<span data-ttu-id="7b2b4-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-108">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="7b2b4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b2b4-109">Return Value</span></span>

<span data-ttu-id="7b2b4-110">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-110">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7b2b4-111">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7b2b4-111">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7b2b4-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7b2b4-112">Return code</span></span></p></th>
<th><p><span data-ttu-id="7b2b4-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b2b4-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b2b4-114">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7b2b4-114">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7b2b4-115">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-115">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b2b4-116">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="7b2b4-116">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="7b2b4-117">Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen <a href="gg294067(v=exchg.10).md">jetstopbackup</a>-Befehl abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-117">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p>
<p><span data-ttu-id="7b2b4-118"><strong>Windows Server 2003:</strong>  Dieser Rückgabewert wird in Windows Server 2003 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-118"><strong>Windows Server 2003:</strong>  This return value is introduced in Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b2b4-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="7b2b4-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="7b2b4-120">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-120">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b2b4-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="7b2b4-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="7b2b4-122">Der Vorgang kann nicht ausgeführt werden, da der-Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-122">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="7b2b4-123"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-123"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b2b4-124">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="7b2b4-124">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="7b2b4-125">Der Sicherungs Vorgang ist fehlgeschlagen, da er außerhalb der Reihenfolge aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-125">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="7b2b4-126"><strong>Jettruneurelog</strong> gibt diesen Fehler zurück, wenn ausstehende Datei Handles vorhanden sind, die mit <a href="gg269249(v=exchg.10).md">jetopenfile</a> für die Instanz erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-126"><strong>JetTruncateLog</strong> will return this error if there are any outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b2b4-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="7b2b4-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="7b2b4-128">Einer der Parameter, die bereitgestellt wurden, enthielt einen unerwarteten Wert, oder die Kombination aus mehreren Parametern hat ein unerwartetes Ergebnis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-128">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="7b2b4-129">Dies kann bei <strong>jettruneurelog</strong> vorkommen, wenn das angegebene Instanzhandle ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-129">This can happen for <strong>JetTruncateLog</strong> when the specified instance handle is invalid.</span></span></p>
<p><span data-ttu-id="7b2b4-130"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-130"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b2b4-131">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="7b2b4-131">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="7b2b4-132">Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-132">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b2b4-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="7b2b4-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="7b2b4-134">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-134">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b2b4-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="7b2b4-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="7b2b4-136">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-136">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b2b4-137">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="7b2b4-137">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="7b2b4-138">Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn in der Tat mehrere Instanzen bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-138">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b2b4-139">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="7b2b4-139">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="7b2b4-140">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-140">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7b2b4-141">Wenn diese Funktion erfolgreich ausgeführt wird, werden die Transaktionsprotokoll Dateien, die nicht mehr benötigt werden, nachdem die aktuelle Sicherung erfolgreich abgeschlossen wurde, gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-141">If this function succeeds, the set of transaction log files that will no longer be needed once the current backup completes successfully are deleted.</span></span> <span data-ttu-id="7b2b4-142">Der Sicherungs Zustands Automat wird so erweitert, dass die Sicherung von Datenbankdateien nicht mehr zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-142">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="7b2b4-143">Nur datenbankpatchdateien und Transaktionsprotokoll Dateien dürfen über diesen Punkt hinaus zur Sicherung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-143">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="7b2b4-144">Wenn diese Funktion fehlschlägt, kann der Sicherungs Zustands Automat so erweitert werden, dass die Sicherung von Datenbankdateien nicht mehr zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-144">If this function fails, the backup state machine can be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="7b2b4-145">Möglicherweise wird eine bestimmte Anzahl von Transaktionsprotokoll Dateien gelöscht, die kleiner als die gewünschte Anzahl ist, aber Sie werden immer vom ältesten zum jüngsten gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-145">Some number of transaction log files might be deleted that is less than the desired number, but they will always be deleted from oldest to youngest.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7b2b4-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b2b4-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b2b4-147"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="7b2b4-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7b2b4-148">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-148">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b2b4-149"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7b2b4-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7b2b4-150">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-150">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b2b4-151"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7b2b4-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7b2b4-152">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b2b4-153"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="7b2b4-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7b2b4-154">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b2b4-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7b2b4-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7b2b4-156">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7b2b4-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7b2b4-157">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7b2b4-157">See Also</span></span>

[<span data-ttu-id="7b2b4-158">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="7b2b4-158">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="7b2b4-159">Jetbeginexternalbackup</span><span class="sxs-lookup"><span data-stu-id="7b2b4-159">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="7b2b4-160">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7b2b4-160">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7b2b4-161">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="7b2b4-161">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="7b2b4-162">Jetopumfile</span><span class="sxs-lookup"><span data-stu-id="7b2b4-162">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="7b2b4-163">Jetstopbackup</span><span class="sxs-lookup"><span data-stu-id="7b2b4-163">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="7b2b4-164">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="7b2b4-164">JetStopService</span></span>](./jetstopservice-function.md)
