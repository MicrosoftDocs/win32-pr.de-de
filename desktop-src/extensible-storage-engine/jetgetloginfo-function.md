---
description: 'Weitere Informationen zu: jetgetloginfo-Funktion'
title: Jetgetloginfo-Funktion
TOCTitle: JetGetLogInfo Function
ms:assetid: a9d14830-d731-4d47-bdc2-c0660a08678e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294055(v=EXCHG.10)
ms:contentKeyID: 32765665
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoA
- JetGetLogInfoW
- JetGetLogInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c96827be0ac62502e7545a9acb1fe157f3b28fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758485"
---
# <a name="jetgetloginfo-function"></a><span data-ttu-id="7c44e-103">Jetgetloginfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="7c44e-103">JetGetLogInfo Function</span></span>


<span data-ttu-id="7c44e-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7c44e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetloginfo-function"></a><span data-ttu-id="7c44e-105">Jetgetloginfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="7c44e-105">JetGetLogInfo Function</span></span>

<span data-ttu-id="7c44e-106">Die **jetgetloginfo** -Funktion wird bei einer von [jetbeginexternalbackup](./jetbeginexternalbackup-function.md) initiierten Sicherung verwendet, um eine Instanz nach den Namen von datenbankpatchdateien und Transaktionsprotokoll Dateien abzufragen, die Teil der Sicherungsdatei Gruppe werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7c44e-106">The **JetGetLogInfo** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database patch files and transaction log files that should become part of the backup file set.</span></span> <span data-ttu-id="7c44e-107">Diese Dateien können anschließend mit [jetopesfile](./jetopenfile-function.md) geöffnet und mit [jetreadfile](./jetreadfile-function.md)gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="7c44e-107">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetLogInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="7c44e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c44e-108">Parameters</span></span>

<span data-ttu-id="7c44e-109">*Szz*</span><span class="sxs-lookup"><span data-stu-id="7c44e-109">*szz*</span></span>

<span data-ttu-id="7c44e-110">Der Ausgabepuffer, der die Liste der null-terminierten Zeichen folgen empfängt, die den Satz von datenbankpatchdateien und Transaktionsprotokoll Dateien beschreiben, die Teil des Sicherungsdatei Satzes sein sollen.</span><span class="sxs-lookup"><span data-stu-id="7c44e-110">The output buffer that will receive the list of null terminated strings describing the set of database patch files and transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="7c44e-111">Die Liste der in diesem Puffer zurückgegebenen Zeichen folgen weist das gleiche Format auf wie eine von der Registrierung verwendete Multizeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7c44e-111">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="7c44e-112">Jede mit NULL endend beendete Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="7c44e-112">Each null terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="7c44e-113">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="7c44e-113">*cbMax*</span></span>

<span data-ttu-id="7c44e-114">Die maximale Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="7c44e-114">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="7c44e-115">*pcbactual*</span><span class="sxs-lookup"><span data-stu-id="7c44e-115">*pcbActual*</span></span>

<span data-ttu-id="7c44e-116">Empfängt die tatsächliche Menge an Zeichen folgen Daten, die im Ausgabepuffer empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="7c44e-116">Receives the actual amount of string data received in the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="7c44e-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c44e-117">Return Value</span></span>

<span data-ttu-id="7c44e-118">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="7c44e-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7c44e-119">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7c44e-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c44e-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7c44e-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="7c44e-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c44e-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c44e-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7c44e-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7c44e-123">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7c44e-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c44e-124">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="7c44e-124">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="7c44e-125">Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen <a href="gg294067(v=exchg.10).md">jetstopbackup</a>-Befehl abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="7c44e-125">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="7c44e-126">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7c44e-126">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c44e-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="7c44e-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="7c44e-128">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="7c44e-128">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c44e-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="7c44e-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="7c44e-130">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="7c44e-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="7c44e-131">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7c44e-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c44e-132">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="7c44e-132">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="7c44e-133">Der Sicherungs Vorgang ist fehlgeschlagen, da er außerhalb der Reihenfolge aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7c44e-133">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="7c44e-134"><strong>Jetgetloginfo</strong> gibt diesen Fehler zurück, wenn ausstehende Datei Handles mit <a href="gg269249(v=exchg.10).md">jetopenfile</a> für die Instanz erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="7c44e-134"><strong>JetGetLogInfo</strong> will return this error if there are any outstanding file handles created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c44e-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="7c44e-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="7c44e-136">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="7c44e-136">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="7c44e-137">Dies kann bei <strong>jetgetloginfo</strong> vorkommen, wenn das angegebene Instanzhandle ungültig ist (Windows XP und spätere Releases).</span><span class="sxs-lookup"><span data-stu-id="7c44e-137">This can happen for <strong>JetGetLogInfo</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c44e-138">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="7c44e-138">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="7c44e-139">Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c44e-139">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c44e-140">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="7c44e-140">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="7c44e-141">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7c44e-141">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c44e-142">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="7c44e-142">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="7c44e-143">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c44e-143">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c44e-144">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="7c44e-144">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="7c44e-145">Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7c44e-145">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c44e-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="7c44e-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="7c44e-147">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="7c44e-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7c44e-148">Bei Erfolg werden die angeforderten Informationen zu dem Satz von Datenbank-Patchdateien und Transaktionsprotokoll Dateien, die Teil des Sicherungsdatei Satzes sein sollen, in den Ausgabe Puffern platziert, sofern bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7c44e-148">On success, the requested information on the set of database patch files and transaction log files that should be part of the backup file set will be placed in the output buffers where provided.</span></span> <span data-ttu-id="7c44e-149">Der Sicherungs Zustands Automat wird so erweitert, dass die Sicherung von Datenbankdateien nicht mehr zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="7c44e-149">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="7c44e-150">Nur datenbankpatchdateien und Transaktionsprotokoll Dateien dürfen über diesen Punkt hinaus zur Sicherung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="7c44e-150">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="7c44e-151">Bei einem Fehler ist der Status der Ausgabepuffer nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="7c44e-151">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="7c44e-152">Der Fehler führt dazu, dass der gesamte Sicherungsprozess für die Instanz abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="7c44e-152">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7c44e-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c44e-153">Remarks</span></span>

<span data-ttu-id="7c44e-154">Beachten Sie, dass diese API keinen Fehler oder keine Warnung zurückgibt, wenn der Ausgabepuffer zu klein ist, um die vollständige Liste der Dateien zu akzeptieren, die Bestandteil des Sicherungsdatei Satzes sein sollten.</span><span class="sxs-lookup"><span data-stu-id="7c44e-154">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="7c44e-155">Die Anwendung sollte immer einen Puffer bereitstellen, um die tatsächliche Größe dieser Liste zu erhalten, und anhand dieser Informationen ermitteln, ob die Liste abgeschnitten wurde.</span><span class="sxs-lookup"><span data-stu-id="7c44e-155">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7c44e-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c44e-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c44e-157"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="7c44e-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7c44e-158">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="7c44e-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c44e-159"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7c44e-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7c44e-160">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7c44e-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c44e-161"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7c44e-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7c44e-162">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="7c44e-162">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c44e-163"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="7c44e-163"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7c44e-164">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7c44e-164">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c44e-165"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7c44e-165"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7c44e-166">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7c44e-166">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c44e-167"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="7c44e-167"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="7c44e-168">Implementiert als <strong>jetgetloginfow</strong> (Unicode) und <strong>jetgetloginfoa</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="7c44e-168">Implemented as <strong>JetGetLogInfoW</strong> (Unicode) and <strong>JetGetLogInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7c44e-169">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7c44e-169">See Also</span></span>

[<span data-ttu-id="7c44e-170">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7c44e-170">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7c44e-171">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="7c44e-171">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="7c44e-172">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="7c44e-172">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="7c44e-173">Jetbeginexternalbackup</span><span class="sxs-lookup"><span data-stu-id="7c44e-173">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="7c44e-174">Jetopumfile</span><span class="sxs-lookup"><span data-stu-id="7c44e-174">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="7c44e-175">Jetreadfile</span><span class="sxs-lookup"><span data-stu-id="7c44e-175">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="7c44e-176">Jetstopbackup</span><span class="sxs-lookup"><span data-stu-id="7c44e-176">JetStopBackup</span></span>](./jetstopbackup-function.md)
