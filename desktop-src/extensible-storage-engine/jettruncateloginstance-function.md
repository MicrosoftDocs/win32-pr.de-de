---
description: Weitere Informationen finden Sie in der jettruneureloginstance-Funktion
title: Jettruneureloginstance-Funktion
TOCTitle: JetTruncateLogInstance Function
ms:assetid: 9b6852c6-a991-4d7b-bc54-49092f788751
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269352(v=EXCHG.10)
ms:contentKeyID: 32765639
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLogInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7286b97b80c323eb6bba7b9d28057bf45eec3920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354516"
---
# <a name="jettruncateloginstance-function"></a><span data-ttu-id="89d97-103">Jettruneureloginstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="89d97-103">JetTruncateLogInstance Function</span></span>


<span data-ttu-id="89d97-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="89d97-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jettruncateloginstance-function"></a><span data-ttu-id="89d97-105">Jettruneureloginstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="89d97-105">JetTruncateLogInstance Function</span></span>

<span data-ttu-id="89d97-106">Die **jettruneureloginstance** -Funktion wird bei einer von [jetbeginexternalbackup](./jetbeginexternalbackup-function.md) initiierten Sicherung verwendet, um Transaktionsprotokoll Dateien zu löschen, die nicht mehr benötigt werden, nachdem die aktuelle Sicherung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="89d97-106">The **JetTruncateLogInstance** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

<span data-ttu-id="89d97-107">**Windows XP:**  **jettruneureloginstance** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="89d97-107">**Windows XP:**  **JetTruncateLogInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetTruncateLogInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="89d97-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="89d97-108">Parameters</span></span>

<span data-ttu-id="89d97-109">*lichen*</span><span class="sxs-lookup"><span data-stu-id="89d97-109">*instance*</span></span>

<span data-ttu-id="89d97-110">Die-Instanz, die für diesen Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="89d97-110">The instance to use for this call.</span></span>

<span data-ttu-id="89d97-111">Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="89d97-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="89d97-112">In diesem Fall wird die Verwendung dieser globalen Instanz impliziert.</span><span class="sxs-lookup"><span data-stu-id="89d97-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="89d97-113">Für Windows XP und spätere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) befindet, in dem nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="89d97-113">For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="89d97-114">Andernfalls schlägt der Vorgang mit JET_errRunningInMultiInstanceMode fehl.</span><span class="sxs-lookup"><span data-stu-id="89d97-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

### <a name="return-value"></a><span data-ttu-id="89d97-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89d97-115">Return Value</span></span>

<span data-ttu-id="89d97-116">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="89d97-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="89d97-117">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="89d97-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89d97-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="89d97-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="89d97-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89d97-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89d97-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="89d97-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="89d97-121">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="89d97-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89d97-122">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="89d97-122">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="89d97-123"><strong>Windows Server 2003:</strong>  Dieser Rückgabewert wird in Windows Server 2003 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="89d97-123"><strong>Windows Server 2003:</strong>  This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="89d97-124">Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen <a href="gg294067(v=exchg.10).md">jetstopbackup</a>-Befehl abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="89d97-124">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89d97-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="89d97-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="89d97-126">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="89d97-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89d97-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="89d97-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="89d97-128">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität dieser Daten zu schützen</span><span class="sxs-lookup"><span data-stu-id="89d97-128">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="89d97-129">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="89d97-129">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89d97-130">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="89d97-130">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="89d97-131">Der Sicherungs Vorgang ist fehlgeschlagen, da er außerhalb der Reihenfolge aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="89d97-131">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="89d97-132"><a href="gg269263(v=exchg.10).md">Jettruneurelog</a> gibt diesen Fehler zurück, wenn ausstehende Datei Handles vorhanden sind, die mit <a href="gg269249(v=exchg.10).md">jetopenfile</a> für die Instanz erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="89d97-132"><a href="gg269263(v=exchg.10).md">JetTruncateLog</a> will return this error if there are any outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89d97-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="89d97-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="89d97-134">Einer der Parameter, die bereitgestellt wurden, enthielt einen unerwarteten Wert, oder die Kombination aus mehreren Parametern hat ein unerwartetes Ergebnis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="89d97-134">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="89d97-135">Dies kann bei <a href="gg269263(v=exchg.10).md">jettruneurelog</a> vorkommen, wenn das angegebene Instanzhandle ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="89d97-135">This can happen for <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> when the specified instance handle is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89d97-136">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="89d97-136">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="89d97-137">Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89d97-137">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89d97-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="89d97-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="89d97-139">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="89d97-139">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89d97-140">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="89d97-140">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="89d97-141">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89d97-141">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89d97-142">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="89d97-142">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="89d97-143">Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="89d97-143">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89d97-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="89d97-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="89d97-145">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="89d97-145">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="89d97-146">Wenn diese Funktion erfolgreich ausgeführt wird, werden die Transaktionsprotokoll Dateien, die nicht mehr benötigt werden, nachdem die aktuelle Sicherung erfolgreich abgeschlossen wurde, gelöscht.</span><span class="sxs-lookup"><span data-stu-id="89d97-146">If this function succeeds, the set of transaction log files that will no longer be needed once the current backup completes successfully are deleted.</span></span> <span data-ttu-id="89d97-147">Der Sicherungs Zustands Automat wird so erweitert, dass die Sicherung von Datenbankdateien nicht mehr zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="89d97-147">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="89d97-148">Nur datenbankpatchdateien und Transaktionsprotokoll Dateien dürfen über diesen Punkt hinaus zur Sicherung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="89d97-148">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="89d97-149">Wenn diese Funktion fehlschlägt, kann der Sicherungs Zustands Automat so erweitert werden, dass die Sicherung von Datenbankdateien nicht mehr zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="89d97-149">If this function fails, the backup state machine can be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="89d97-150">Möglicherweise wird eine bestimmte Anzahl von Transaktionsprotokoll Dateien gelöscht, die kleiner als die gewünschte Anzahl ist, aber Sie werden immer vom ältesten zum jüngsten gelöscht.</span><span class="sxs-lookup"><span data-stu-id="89d97-150">Some number of transaction log files might be deleted that is less than the desired number, but they will always be deleted from oldest to youngest.</span></span>

#### <a name="requirements"></a><span data-ttu-id="89d97-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89d97-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89d97-152"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="89d97-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="89d97-153">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="89d97-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89d97-154"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="89d97-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="89d97-155">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="89d97-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89d97-156"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="89d97-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="89d97-157">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="89d97-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89d97-158"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="89d97-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="89d97-159">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="89d97-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89d97-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="89d97-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="89d97-161">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="89d97-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="89d97-162">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="89d97-162">See Also</span></span>

[<span data-ttu-id="89d97-163">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="89d97-163">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="89d97-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="89d97-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="89d97-165">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="89d97-165">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="89d97-166">Jetbeginexternalbackup</span><span class="sxs-lookup"><span data-stu-id="89d97-166">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="89d97-167">Jetopumfile</span><span class="sxs-lookup"><span data-stu-id="89d97-167">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="89d97-168">Jetstopbackup</span><span class="sxs-lookup"><span data-stu-id="89d97-168">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="89d97-169">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="89d97-169">JetStopService</span></span>](./jetstopservice-function.md)
