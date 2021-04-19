---
description: Weitere Informationen finden Sie in der jetgetloginfoinstance-Funktion.
title: Jetgetloginfoinstance-Funktion
TOCTitle: JetGetLogInfoInstance Function
ms:assetid: 505500b1-2827-43f1-a0fe-5e84e00b0260
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269246(v=EXCHG.10)
ms:contentKeyID: 32765548
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance
- JetGetLogInfoInstanceW
- JetGetLogInfoInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2056859bdce13dfdc28d4cbbf8716925d5bc1cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350120"
---
# <a name="jetgetloginfoinstance-function"></a><span data-ttu-id="cd208-103">Jetgetloginfoinstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="cd208-103">JetGetLogInfoInstance Function</span></span>


<span data-ttu-id="cd208-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cd208-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetloginfoinstance-function"></a><span data-ttu-id="cd208-105">Jetgetloginfoinstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="cd208-105">JetGetLogInfoInstance Function</span></span>

<span data-ttu-id="cd208-106">Die **jetgetloginfoinstance** -Funktion wird bei einer von [jetbeginexternalbackup](./jetbeginexternalbackup-function.md) initiierten Sicherung verwendet, um eine Instanz nach den Namen von datenbankpatchdateien und Transaktionsprotokoll Dateien abzufragen, die Teil der Sicherungsdatei Gruppe werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cd208-106">The **JetGetLogInfoInstance** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database patch files and transaction log files that should become part of the backup file set.</span></span> <span data-ttu-id="cd208-107">Diese Dateien können anschließend mit [jetopesfile](./jetopenfile-function.md) geöffnet und mit [jetreadfile](./jetreadfile-function.md)gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="cd208-107">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

<span data-ttu-id="cd208-108">**Windows XP: jetgetloginfoinstance** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="cd208-108">**Windows XP:  JetGetLogInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="cd208-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd208-109">Parameters</span></span>

<span data-ttu-id="cd208-110">*lichen*</span><span class="sxs-lookup"><span data-stu-id="cd208-110">*instance*</span></span>

<span data-ttu-id="cd208-111">Die-Instanz, die für diesen Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd208-111">The instance to use for this call.</span></span>

<span data-ttu-id="cd208-112">Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="cd208-112">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="cd208-113">In diesem Fall wird die Verwendung dieser globalen Instanz impliziert.</span><span class="sxs-lookup"><span data-stu-id="cd208-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="cd208-114">Für Windows XP und spätere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) befindet, in dem nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="cd208-114">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="cd208-115">Andernfalls schlägt der Vorgang mit JET_errRunningInMultiInstanceMode fehl.</span><span class="sxs-lookup"><span data-stu-id="cd208-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="cd208-116">*Szz*</span><span class="sxs-lookup"><span data-stu-id="cd208-116">*szz*</span></span>

<span data-ttu-id="cd208-117">Der Ausgabepuffer, der die Liste der null-terminierten Zeichen folgen empfängt, die den Satz von datenbankpatchdateien und Transaktionsprotokoll Dateien beschreiben, die Teil des Sicherungsdatei Satzes sein sollen.</span><span class="sxs-lookup"><span data-stu-id="cd208-117">The output buffer that will receive the list of null terminated strings describing the set of database patch files and transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="cd208-118">Die Liste der in diesem Puffer zurückgegebenen Zeichen folgen weist das gleiche Format auf wie eine von der Registrierung verwendete Multizeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cd208-118">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="cd208-119">Jede mit NULL endend beendete Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="cd208-119">Each null terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="cd208-120">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="cd208-120">*cbMax*</span></span>

<span data-ttu-id="cd208-121">Die maximale Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="cd208-121">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="cd208-122">*pcbactual*</span><span class="sxs-lookup"><span data-stu-id="cd208-122">*pcbActual*</span></span>

<span data-ttu-id="cd208-123">Empfängt die tatsächliche Menge an Zeichen folgen Daten, die im Ausgabepuffer empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="cd208-123">Receives the actual amount of string data received in the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="cd208-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd208-124">Return Value</span></span>

<span data-ttu-id="cd208-125">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="cd208-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="cd208-126">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cd208-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd208-127">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cd208-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="cd208-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd208-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd208-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="cd208-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="cd208-130">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cd208-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd208-131">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="cd208-131">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="cd208-132">Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen <a href="gg294067(v=exchg.10).md">jetstopbackup</a>-Befehl abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="cd208-132">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="cd208-133">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cd208-133">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd208-134">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="cd208-134">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="cd208-135">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="cd208-135">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd208-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="cd208-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="cd208-137">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="cd208-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="cd208-138">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cd208-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd208-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="cd208-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="cd208-140">Der Sicherungs Vorgang ist fehlgeschlagen, da er außerhalb der Reihenfolge aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="cd208-140">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="cd208-141"><a href="gg294055(v=exchg.10).md">Jetgetloginfo</a> gibt diesen Fehler zurück, wenn ausstehende Datei Handles mit <a href="gg269249(v=exchg.10).md">jetopenfile</a> für die Instanz erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="cd208-141"><a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> will return this error if there are any outstanding file handles created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd208-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="cd208-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="cd208-143">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="cd208-143">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="cd208-144">Dies kann bei <a href="gg294055(v=exchg.10).md">jetgetloginfo</a> vorkommen, wenn das angegebene Instanzhandle ungültig ist (Windows XP und spätere Releases).</span><span class="sxs-lookup"><span data-stu-id="cd208-144">This can happen for <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd208-145">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="cd208-145">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="cd208-146">Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd208-146">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd208-147">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="cd208-147">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="cd208-148">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="cd208-148">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd208-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="cd208-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="cd208-150">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd208-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd208-151">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="cd208-151">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="cd208-152">Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="cd208-152">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd208-153">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="cd208-153">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="cd208-154">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="cd208-154">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd208-155">Bei Erfolg werden die angeforderten Informationen zu dem Satz von Datenbank-Patchdateien und Transaktionsprotokoll Dateien, die Teil des Sicherungsdatei Satzes sein sollen, in den Ausgabe Puffern platziert, sofern bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="cd208-155">On success, the requested information on the set of database patch files and transaction log files that should be part of the backup file set will be placed in the output buffers where provided.</span></span> <span data-ttu-id="cd208-156">Der Sicherungs Zustands Automat wird so erweitert, dass die Sicherung von Datenbankdateien nicht mehr zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="cd208-156">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="cd208-157">Nur datenbankpatchdateien und Transaktionsprotokoll Dateien dürfen über diesen Punkt hinaus zur Sicherung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="cd208-157">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="cd208-158">Bei einem Fehler ist der Status der Ausgabepuffer nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="cd208-158">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="cd208-159">Der Fehler führt dazu, dass der gesamte Sicherungsprozess für die Instanz abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="cd208-159">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cd208-160">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd208-160">Remarks</span></span>

<span data-ttu-id="cd208-161">Beachten Sie, dass diese API keinen Fehler oder keine Warnung zurückgibt, wenn der Ausgabepuffer zu klein ist, um die vollständige Liste der Dateien zu akzeptieren, die Bestandteil des Sicherungsdatei Satzes sein sollten.</span><span class="sxs-lookup"><span data-stu-id="cd208-161">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="cd208-162">Die Anwendung sollte immer einen Puffer bereitstellen, um die tatsächliche Größe dieser Liste zu erhalten, und anhand dieser Informationen ermitteln, ob die Liste abgeschnitten wurde.</span><span class="sxs-lookup"><span data-stu-id="cd208-162">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="cd208-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd208-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd208-164"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="cd208-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cd208-165">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cd208-165">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd208-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cd208-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cd208-167">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cd208-167">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd208-168"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="cd208-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cd208-169">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="cd208-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd208-170"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="cd208-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="cd208-171">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="cd208-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd208-172"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="cd208-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="cd208-173">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="cd208-173">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd208-174"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="cd208-174"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="cd208-175">Implementiert als <strong>jetgetloginfoinstancew</strong> (Unicode) und <strong>jetgetloginfoinstancea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="cd208-175">Implemented as <strong>JetGetLogInfoInstanceW</strong> (Unicode) and <strong>JetGetLogInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cd208-176">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cd208-176">See Also</span></span>

[<span data-ttu-id="cd208-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cd208-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cd208-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="cd208-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="cd208-179">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="cd208-179">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="cd208-180">Jetbeginexternalbackup</span><span class="sxs-lookup"><span data-stu-id="cd208-180">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="cd208-181">Jetopumfile</span><span class="sxs-lookup"><span data-stu-id="cd208-181">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="cd208-182">Jetreadfile</span><span class="sxs-lookup"><span data-stu-id="cd208-182">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="cd208-183">Jetstopbackup</span><span class="sxs-lookup"><span data-stu-id="cd208-183">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="cd208-184">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="cd208-184">JetStopService</span></span>](./jetstopservice-function.md)
