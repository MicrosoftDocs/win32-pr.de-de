---
description: Weitere Informationen finden Sie in der jetgettruneureloginfoinstance-Funktion.
title: Jetgettruneureloginfoinstance-Funktion
TOCTitle: JetGetTruncateLogInfoInstance Function
ms:assetid: 1ecb2f2f-2cad-4c55-9296-5e5893b57695
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269199(v=EXCHG.10)
ms:contentKeyID: 32765502
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTruncateLogInfoInstanceA
- JetGetTruncateLogInfoInstanceW
- JetGetTruncateLogInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d51243ff6ca4b2bbaec77233bbe00437f55e0f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363742"
---
# <a name="jetgettruncateloginfoinstance-function"></a><span data-ttu-id="3b379-103">Jetgettruneureloginfoinstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="3b379-103">JetGetTruncateLogInfoInstance Function</span></span>


<span data-ttu-id="3b379-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3b379-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettruncateloginfoinstance-function"></a><span data-ttu-id="3b379-105">Jetgettruneureloginfoinstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="3b379-105">JetGetTruncateLogInfoInstance Function</span></span>

<span data-ttu-id="3b379-106">Die **jetgettrunkateloginfoinstance** -Funktion wird während einer Sicherung verwendet, die von [jetbeginexternalbackup](./jetbeginexternalbackup-function.md) initiiert wird, um eine Instanz nach den Namen der Transaktionsprotokoll Dateien abzufragen, die nach erfolgreichem Abschluss der Sicherung sicher gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="3b379-106">The **JetGetTruncateLogInfoInstance** function is used during a backup that is initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of the transaction log files that can be safely deleted after the backup has successfully completed.</span></span>

<span data-ttu-id="3b379-107">**Windows XP:**  **jetgettrun-eloginfoinstance** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3b379-107">**Windows XP:**  **JetGetTruncateLogInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetTruncateLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="3b379-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b379-108">Parameters</span></span>

<span data-ttu-id="3b379-109">*lichen*</span><span class="sxs-lookup"><span data-stu-id="3b379-109">*instance*</span></span>

<span data-ttu-id="3b379-110">Die-Instanz, die für diesen Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b379-110">The instance to use for this call.</span></span>

<span data-ttu-id="3b379-111">*Szz*</span><span class="sxs-lookup"><span data-stu-id="3b379-111">*szz*</span></span>

<span data-ttu-id="3b379-112">Der Ausgabepuffer, der die Liste der mit NULL endenden Zeichen folgen empfängt, die den Satz von Transaktionsprotokoll Dateien beschreiben, die nach dem erfolgreichen Abschluss der Sicherung sicher gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="3b379-112">The output buffer that receives the list of null-terminated strings describing the set of transaction log files that can be safely deleted after the backup has been completed successfully.</span></span>

<span data-ttu-id="3b379-113">Die Liste der Zeichen folgen, die in diesem Puffer zurückgegeben werden, hat das gleiche Format wie eine von der Registrierung verwendete Multizeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3b379-113">The list of strings that are returned in this buffer is in the same format as a multi-string that is used by the registry.</span></span> <span data-ttu-id="3b379-114">Jede mit NULL endenden Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="3b379-114">Each null-terminated string is returned in sequence and followed by a final null terminator.</span></span>

<span data-ttu-id="3b379-115">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="3b379-115">*cbMax*</span></span>

<span data-ttu-id="3b379-116">Die maximale Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="3b379-116">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="3b379-117">*pcbactual*</span><span class="sxs-lookup"><span data-stu-id="3b379-117">*pcbActual*</span></span>

<span data-ttu-id="3b379-118">Ein Zeiger auf den Ausgabepuffer, der die tatsächliche Menge an Zeichen folgen Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="3b379-118">Pointer to the output buffer that receives the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="3b379-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b379-119">Return Value</span></span>

<span data-ttu-id="3b379-120">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="3b379-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3b379-121">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3b379-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b379-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3b379-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="3b379-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b379-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b379-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3b379-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3b379-125">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="3b379-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b379-126">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="3b379-126">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="3b379-127">Einer der angegebenen Parameter enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte führte zu einem unerwarteten Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="3b379-127">One of the provided parameters contained an unexpected value or the combination of several parameter values resulted in an unexpected result.</span></span></p>
<p><span data-ttu-id="3b379-128"><strong>Windows XP und höher:</strong>  Dies kann bei <strong>jetgettruneureloginfoinstance</strong> vorkommen, wenn das angegebene Instanzhandle ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="3b379-128"><strong>Windows XP and later:</strong>  This can happen for <strong>JetGetTruncateLogInfoInstance</strong> when the specified instance handle is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b379-129">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="3b379-129">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="3b379-130">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3b379-130">The operation cannot complete because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b379-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="3b379-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="3b379-132">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="3b379-132">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b379-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="3b379-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="3b379-134">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität dieser Daten zu schützen</span><span class="sxs-lookup"><span data-stu-id="3b379-134">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="3b379-135"><strong>Windows XP:</strong>  Dieser Rückgabewert wurde in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3b379-135"><strong>Windows XP:</strong>  This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b379-136">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="3b379-136">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="3b379-137">Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen <a href="gg294067(v=exchg.10).md">jetstopbackup</a>-Befehl abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="3b379-137">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p>
<p><span data-ttu-id="3b379-138"><strong>Windows XP:</strong>  Dieser Rückgabewert wurde in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3b379-138"><strong>Windows XP:</strong>  This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b379-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="3b379-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="3b379-140">Der Sicherungs Vorgang ist fehlgeschlagen, da er außerhalb der Reihenfolge aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="3b379-140">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b379-141">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="3b379-141">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="3b379-142">Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b379-142">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b379-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="3b379-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="3b379-144">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b379-144">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b379-145">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="3b379-145">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="3b379-146">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="3b379-146">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b379-147"><strong>Jetgettruneureloginfoinstance</strong></span><span class="sxs-lookup"><span data-stu-id="3b379-147"><strong>JetGetTruncateLogInfoInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="3b379-148">Es gibt ausstehende Datei Handles, die mit <a href="gg269249(v=exchg.10).md">jetopenfile</a> für die-Instanz erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="3b379-148">There are outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3b379-149">Wenn diese Funktion erfolgreich ausgeführt wird, werden die angeforderten Informationen zu dem Satz von Transaktionsprotokoll Dateien, die nach dem erfolgreichen Abschluss der Sicherung sicher gelöscht werden können, in die Ausgabepuffer eingefügt, in denen Sie bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3b379-149">If this function succeeds, the requested information about the set of transaction log files that can be safely deleted after the backup has been completed successfully will be placed in the output buffers where they are provided.</span></span> <span data-ttu-id="3b379-150">Der Sicherungs Zustands Automat wird so erweitert, dass die Sicherung von Datenbankdateien nicht mehr zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="3b379-150">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="3b379-151">Nur datenbankpatchdateien und Transaktionsprotokoll Dateien können über diesen Punkt hinaus zur Sicherung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="3b379-151">Only database patch files and transaction log files can be opened for backup beyond this point.</span></span>

<span data-ttu-id="3b379-152">Wenn diese Funktion fehlschlägt, ist der Status der Ausgabepuffer nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="3b379-152">If this function fails, the state of the output buffers is undefined.</span></span> <span data-ttu-id="3b379-153">Der Fehler führt dazu, dass der gesamte Sicherungsprozess für die Instanz abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="3b379-153">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="3b379-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b379-154">Remarks</span></span>

<span data-ttu-id="3b379-155">Diese API gibt keinen Fehler oder eine Warnung zurück, wenn der Ausgabepuffer zu klein ist, um die vollständige Liste der Dateien zu akzeptieren, die Bestandteil des Sicherungsdatei Satzes sein sollten.</span><span class="sxs-lookup"><span data-stu-id="3b379-155">This API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="3b379-156">Die Anwendung sollte immer einen Puffer bereitstellen, um die tatsächliche Größe dieser Liste zu erhalten, und anhand dieser Informationen ermitteln, ob die Liste abgeschnitten wurde.</span><span class="sxs-lookup"><span data-stu-id="3b379-156">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3b379-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b379-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b379-158"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3b379-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3b379-159">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3b379-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b379-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3b379-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3b379-161">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3b379-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b379-162"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="3b379-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3b379-163">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="3b379-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b379-164"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="3b379-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3b379-165">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3b379-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b379-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3b379-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3b379-167">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3b379-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b379-168"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="3b379-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="3b379-169">Implementiert als <strong>jetgettruneureloginfoinstancew</strong> (Unicode) und <strong>jetgettrun-eloginfoinstancea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="3b379-169">Implemented as <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) and <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3b379-170">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3b379-170">See Also</span></span>

[<span data-ttu-id="3b379-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3b379-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3b379-172">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="3b379-172">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="3b379-173">Jetbeginexternalbackup</span><span class="sxs-lookup"><span data-stu-id="3b379-173">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="3b379-174">Jetclosedatabase</span><span class="sxs-lookup"><span data-stu-id="3b379-174">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="3b379-175">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="3b379-175">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="3b379-176">Jetendsession</span><span class="sxs-lookup"><span data-stu-id="3b379-176">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="3b379-177">Jetopumfile</span><span class="sxs-lookup"><span data-stu-id="3b379-177">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="3b379-178">Jetresessioncontext</span><span class="sxs-lookup"><span data-stu-id="3b379-178">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="3b379-179">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="3b379-179">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="3b379-180">Jetstopbackup</span><span class="sxs-lookup"><span data-stu-id="3b379-180">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="3b379-181">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="3b379-181">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="3b379-182">Jetterm</span><span class="sxs-lookup"><span data-stu-id="3b379-182">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="3b379-183">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="3b379-183">JetTerm2</span></span>](./jetterm2-function.md)
