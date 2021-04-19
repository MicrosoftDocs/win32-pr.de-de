---
description: 'Weitere Informationen finden Sie hier: JetGetLogInfoInstance2-Funktion'
title: JetGetLogInfoInstance2-Funktion
TOCTitle: JetGetLogInfoInstance2 Function
ms:assetid: 50fdae92-611c-4dbf-846e-86cc836a23db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269247(v=EXCHG.10)
ms:contentKeyID: 32765549
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance2W
- JetGetLogInfoInstance2
- JetGetLogInfoInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f58a04c49a82604fb5ded09b6328e9e03df7963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356203"
---
# <a name="jetgetloginfoinstance2-function"></a><span data-ttu-id="054d4-103">JetGetLogInfoInstance2-Funktion</span><span class="sxs-lookup"><span data-stu-id="054d4-103">JetGetLogInfoInstance2 Function</span></span>


<span data-ttu-id="054d4-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="054d4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetloginfoinstance2-function"></a><span data-ttu-id="054d4-105">JetGetLogInfoInstance2-Funktion</span><span class="sxs-lookup"><span data-stu-id="054d4-105">JetGetLogInfoInstance2 Function</span></span>

<span data-ttu-id="054d4-106">Die **JetGetLogInfoInstance2** -Funktion wird bei einer von [jetbeginexternalbackup](./jetbeginexternalbackup-function.md) initiierten Sicherung verwendet, um eine Instanz nach den Namen von datenbankpatchdateien und Transaktionsprotokoll Dateien abzufragen, die Teil der Sicherungsdatei Gruppe werden sollen.</span><span class="sxs-lookup"><span data-stu-id="054d4-106">The **JetGetLogInfoInstance2** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database patch files and transaction log files that should become part of the backup file set.</span></span> <span data-ttu-id="054d4-107">Diese Dateien können anschließend mit [jetopesfile](./jetopenfile-function.md) geöffnet und mit [jetreadfile](./jetreadfile-function.md)gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="054d4-107">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

<span data-ttu-id="054d4-108">**Windows XP: JetGetLogInfoInstance2** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="054d4-108">**Windows XP:  JetGetLogInfoInstance2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetLogInfoInstance2(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in_out_opt  JET_LOGINFO* pLogInfo
    );
```

### <a name="parameters"></a><span data-ttu-id="054d4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="054d4-109">Parameters</span></span>

<span data-ttu-id="054d4-110">*lichen*</span><span class="sxs-lookup"><span data-stu-id="054d4-110">*instance*</span></span>

<span data-ttu-id="054d4-111">Die-Instanz, die für diesen Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="054d4-111">The instance to use for this call.</span></span>

<span data-ttu-id="054d4-112">Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="054d4-112">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="054d4-113">In diesem Fall wird die Verwendung dieser globalen Instanz impliziert.</span><span class="sxs-lookup"><span data-stu-id="054d4-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="054d4-114">Für Windows XP und spätere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) befindet, in dem nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="054d4-114">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="054d4-115">Andernfalls schlägt der Vorgang mit JET_errRunningInMultiInstanceMode fehl.</span><span class="sxs-lookup"><span data-stu-id="054d4-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="054d4-116">*Szz*</span><span class="sxs-lookup"><span data-stu-id="054d4-116">*szz*</span></span>

<span data-ttu-id="054d4-117">Der Ausgabepuffer, der die Liste der null-terminierten Zeichen folgen empfängt, die den Satz von datenbankpatchdateien und Transaktionsprotokoll Dateien beschreiben, die Teil des Sicherungsdatei Satzes sein sollen.</span><span class="sxs-lookup"><span data-stu-id="054d4-117">The output buffer that will receive the list of null terminated strings describing the set of database patch files and transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="054d4-118">Die Liste der in diesem Puffer zurückgegebenen Zeichen folgen weist das gleiche Format auf wie eine von der Registrierung verwendete Multizeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="054d4-118">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="054d4-119">Jede mit NULL endend beendete Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="054d4-119">Each null terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="054d4-120">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="054d4-120">*cbMax*</span></span>

<span data-ttu-id="054d4-121">Die maximale Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="054d4-121">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="054d4-122">*pcbactual*</span><span class="sxs-lookup"><span data-stu-id="054d4-122">*pcbActual*</span></span>

<span data-ttu-id="054d4-123">Empfängt die tatsächliche Menge an Zeichen folgen Daten, die im Ausgabepuffer empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="054d4-123">Receives the actual amount of string data received in the output buffer.</span></span>

<span data-ttu-id="054d4-124">*ploginfo*</span><span class="sxs-lookup"><span data-stu-id="054d4-124">*pLogInfo*</span></span>

<span data-ttu-id="054d4-125">Empfängt strukturierte Informationen zu den Transaktionsprotokoll Dateien, die Teil des Sicherungsdatei Satzes sein sollten.</span><span class="sxs-lookup"><span data-stu-id="054d4-125">Receives structured information on the transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="054d4-126">Wenn dieser Parameter nicht vorhanden ist, wird davon ausgegangen, dass sein Wert NULL ist.</span><span class="sxs-lookup"><span data-stu-id="054d4-126">When this parameter is not present, its value is presumed to be NULL.</span></span>

### <a name="return-value"></a><span data-ttu-id="054d4-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="054d4-127">Return Value</span></span>

<span data-ttu-id="054d4-128">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="054d4-128">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="054d4-129">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="054d4-129">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="054d4-130">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="054d4-130">Return code</span></span></p></th>
<th><p><span data-ttu-id="054d4-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="054d4-131">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="054d4-132">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="054d4-132">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="054d4-133">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="054d4-133">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054d4-134">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="054d4-134">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="054d4-135">Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen <a href="gg294067(v=exchg.10).md">jetstopbackup</a>-Befehl abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="054d4-135">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="054d4-136">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="054d4-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054d4-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="054d4-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="054d4-138">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="054d4-138">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054d4-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="054d4-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="054d4-140">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="054d4-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="054d4-141">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="054d4-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054d4-142">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="054d4-142">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="054d4-143">Der Sicherungs Vorgang ist fehlgeschlagen, da er außerhalb der Reihenfolge aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="054d4-143">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="054d4-144"><a href="gg294055(v=exchg.10).md">Jetgetloginfo</a> gibt diesen Fehler zurück, wenn ausstehende Datei Handles mit <a href="gg269249(v=exchg.10).md">jetopenfile</a> für die Instanz erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="054d4-144"><a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> will return this error if there are any outstanding file handles created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054d4-145">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="054d4-145">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="054d4-146">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="054d4-146">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="054d4-147">Dies kann bei <a href="gg294055(v=exchg.10).md">jetgetloginfo</a> vorkommen, wenn das angegebene Instanzhandle ungültig ist (Windows XP und spätere Releases).</span><span class="sxs-lookup"><span data-stu-id="054d4-147">This can happen for <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054d4-148">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="054d4-148">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="054d4-149">Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="054d4-149">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054d4-150">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="054d4-150">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="054d4-151">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="054d4-151">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054d4-152">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="054d4-152">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="054d4-153">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="054d4-153">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054d4-154">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="054d4-154">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="054d4-155">Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="054d4-155">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054d4-156">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="054d4-156">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="054d4-157">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="054d4-157">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="054d4-158">Bei Erfolg werden die angeforderten Informationen zu dem Satz von Datenbank-Patchdateien und Transaktionsprotokoll Dateien, die Teil des Sicherungsdatei Satzes sein sollen, in den Ausgabe Puffern platziert, sofern bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="054d4-158">On success, the requested information on the set of database patch files and transaction log files that should be part of the backup file set will be placed in the output buffers where provided.</span></span> <span data-ttu-id="054d4-159">Der Sicherungs Zustands Automat wird so erweitert, dass die Sicherung von Datenbankdateien nicht mehr zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="054d4-159">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="054d4-160">Nur datenbankpatchdateien und Transaktionsprotokoll Dateien dürfen über diesen Punkt hinaus zur Sicherung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="054d4-160">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="054d4-161">Bei einem Fehler ist der Status der Ausgabepuffer nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="054d4-161">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="054d4-162">Der Fehler führt dazu, dass der gesamte Sicherungsprozess für die Instanz abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="054d4-162">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="054d4-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="054d4-163">Remarks</span></span>

<span data-ttu-id="054d4-164">Beachten Sie, dass diese API keinen Fehler oder keine Warnung zurückgibt, wenn der Ausgabepuffer zu klein ist, um die vollständige Liste der Dateien zu akzeptieren, die Bestandteil des Sicherungsdatei Satzes sein sollten.</span><span class="sxs-lookup"><span data-stu-id="054d4-164">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="054d4-165">Die Anwendung sollte immer einen Puffer bereitstellen, um die tatsächliche Größe dieser Liste zu erhalten, und anhand dieser Informationen ermitteln, ob die Liste abgeschnitten wurde.</span><span class="sxs-lookup"><span data-stu-id="054d4-165">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="054d4-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="054d4-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="054d4-167"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="054d4-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="054d4-168">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="054d4-168">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054d4-169"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="054d4-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="054d4-170">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="054d4-170">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054d4-171"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="054d4-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="054d4-172">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="054d4-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054d4-173"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="054d4-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="054d4-174">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="054d4-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="054d4-175"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="054d4-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="054d4-176">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="054d4-176">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="054d4-177"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="054d4-177"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="054d4-178">Implementiert als <strong>JetGetLogInfoInstance2W</strong> (Unicode) und <strong>JetGetLogInfoInstance2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="054d4-178">Implemented as <strong>JetGetLogInfoInstance2W</strong> (Unicode) and <strong>JetGetLogInfoInstance2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="054d4-179">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="054d4-179">See Also</span></span>

[<span data-ttu-id="054d4-180">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="054d4-180">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="054d4-181">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="054d4-181">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="054d4-182">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="054d4-182">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="054d4-183">Jetbeginexternalbackup</span><span class="sxs-lookup"><span data-stu-id="054d4-183">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="054d4-184">Jetopumfile</span><span class="sxs-lookup"><span data-stu-id="054d4-184">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="054d4-185">Jetreadfile</span><span class="sxs-lookup"><span data-stu-id="054d4-185">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="054d4-186">Jetstopbackup</span><span class="sxs-lookup"><span data-stu-id="054d4-186">JetStopBackup</span></span>](./jetstopbackup-function.md)
