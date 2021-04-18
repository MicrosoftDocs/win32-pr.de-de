---
description: 'Weitere Informationen zu: jetgetattachinfo-Funktion'
title: JetGetAttachInfo-Funktion
TOCTitle: JetGetAttachInfo Function
ms:assetid: 6b1392f3-f40a-4eb0-aea8-1508b23ed649
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269286(v=EXCHG.10)
ms:contentKeyID: 32765578
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfo
- JetGetAttachInfoA
- JetGetAttachInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa1e51931c11e0fce0b18c0c102c4d54c0b47976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350881"
---
# <a name="jetgetattachinfo-function"></a><span data-ttu-id="9f2c9-103">JetGetAttachInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="9f2c9-103">JetGetAttachInfo Function</span></span>


<span data-ttu-id="9f2c9-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9f2c9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetattachinfo-function"></a><span data-ttu-id="9f2c9-105">JetGetAttachInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="9f2c9-105">JetGetAttachInfo Function</span></span>

<span data-ttu-id="9f2c9-106">Die **jetgetattachinfo** -Funktion wird bei einer von [jetbeginexternalbackup](./jetbeginexternalbackup-function.md) initiierten Sicherung verwendet, um eine Instanz für die Namen von Datenbankdateien abzufragen, die Teil der Sicherungsdatei Gruppe werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-106">The **JetGetAttachInfo** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="9f2c9-107">Nur Datenbanken, die zurzeit an die Instanz mit [jetattachdatabase](./jetattachdatabase-function.md) angefügt sind, werden berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-107">Only databases currently attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) will be considered.</span></span> <span data-ttu-id="9f2c9-108">Diese Dateien können anschließend mit [jetopesfile](./jetopenfile-function.md) geöffnet und mit [jetreadfile](./jetreadfile-function.md)gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-108">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetAttachInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="9f2c9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f2c9-109">Parameters</span></span>

<span data-ttu-id="9f2c9-110">*Szz*</span><span class="sxs-lookup"><span data-stu-id="9f2c9-110">*szz*</span></span>

<span data-ttu-id="9f2c9-111">Der Ausgabepuffer, der die Liste der null-terminierten Zeichen folgen empfängt, die den Satz von Datenbankdateien beschreiben, die Teil des Sicherungsdatei Satzes sein sollen.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-111">The output buffer that receives the list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="9f2c9-112">Die Liste der in diesem Puffer zurückgegebenen Zeichen folgen weist das gleiche Format auf wie eine von der Registrierung verwendete Multizeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-112">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="9f2c9-113">Jede NULL terminierte Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-113">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="9f2c9-114">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="9f2c9-114">*cbMax*</span></span>

<span data-ttu-id="9f2c9-115">Die maximale Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-115">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="9f2c9-116">*pcbactual*</span><span class="sxs-lookup"><span data-stu-id="9f2c9-116">*pcbActual*</span></span>

<span data-ttu-id="9f2c9-117">Zeiger auf den Ausgabepuffer, der die tatsächliche Menge an Zeichen folgen Daten empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-117">Pointer to the output buffer that received the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="9f2c9-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f2c9-118">Return Value</span></span>

<span data-ttu-id="9f2c9-119">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9f2c9-120">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9f2c9-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9f2c9-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9f2c9-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="9f2c9-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f2c9-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f2c9-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9f2c9-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9f2c9-124">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f2c9-125">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="9f2c9-125">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="9f2c9-126">Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen <a href="gg294067(v=exchg.10).md">jetstopbackup</a>-Befehl abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-126">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="9f2c9-127">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f2c9-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9f2c9-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9f2c9-129">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f2c9-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9f2c9-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9f2c9-131">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="9f2c9-132">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f2c9-133">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="9f2c9-133">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="9f2c9-134">Der Sicherungs Vorgang ist fehlgeschlagen, da er außerhalb der Reihenfolge aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-134">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="9f2c9-135"><strong>Jetgetattachinfo</strong> gibt diesen Fehler zurück, wenn es sich bei der aktuellen Sicherung nicht um eine vollständige Sicherung handelt.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-135"><strong>JetGetAttachInfo</strong> will return this error if the current backup is not a full backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f2c9-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="9f2c9-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="9f2c9-137">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="9f2c9-138">Dies kann bei <strong>jetgetattachinfo</strong> vorkommen, wenn das angegebene Instanzhandle ungültig ist (Windows XP und spätere Releases).</span><span class="sxs-lookup"><span data-stu-id="9f2c9-138">This can happen for <strong>JetGetAttachInfo</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f2c9-139">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="9f2c9-139">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="9f2c9-140">Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-140">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f2c9-141">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9f2c9-141">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9f2c9-142">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-142">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f2c9-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9f2c9-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9f2c9-144">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-144">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f2c9-145">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="9f2c9-145">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="9f2c9-146">Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-146">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f2c9-147">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9f2c9-147">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9f2c9-148">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-148">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9f2c9-149">Bei Erfolg werden die angeforderten Informationen zu dem Satz von Datenbankdateien, die Teil des Sicherungsdatei Satzes sein sollen, in den Ausgabe Puffern platziert, sofern bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-149">On success, the requested information on the set of database files that should be part of the backup file set will be placed in the output buffers where provided.</span></span>

<span data-ttu-id="9f2c9-150">Bei einem Fehler ist der Status der Ausgabepuffer nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-150">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="9f2c9-151">Der Fehler führt dazu, dass der gesamte Sicherungsprozess für die Instanz abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-151">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9f2c9-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f2c9-152">Remarks</span></span>

<span data-ttu-id="9f2c9-153">Beachten Sie, dass diese API keinen Fehler oder keine Warnung zurückgibt, wenn der Ausgabepuffer zu klein ist, um die vollständige Liste der Dateien zu akzeptieren, die Bestandteil des Sicherungsdatei Satzes sein sollten.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-153">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="9f2c9-154">Die Anwendung sollte immer einen Puffer bereitstellen, um die tatsächliche Größe dieser Liste zu erhalten, und anhand dieser Informationen ermitteln, ob die Liste abgeschnitten wurde.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-154">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9f2c9-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f2c9-155">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f2c9-156"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9f2c9-156"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9f2c9-157">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-157">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f2c9-158"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9f2c9-158"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9f2c9-159">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-159">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f2c9-160"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9f2c9-160"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9f2c9-161">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-161">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f2c9-162"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="9f2c9-162"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9f2c9-163">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-163">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f2c9-164"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9f2c9-164"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9f2c9-165">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9f2c9-165">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f2c9-166"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="9f2c9-166"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="9f2c9-167">Implementiert als <strong>jetgetattachinfow</strong> (Unicode) und <strong>jetgetattachinfoa</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="9f2c9-167">Implemented as <strong>JetGetAttachInfoW</strong> (Unicode) and <strong>JetGetAttachInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9f2c9-168">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9f2c9-168">See Also</span></span>

[<span data-ttu-id="9f2c9-169">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9f2c9-169">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9f2c9-170">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="9f2c9-170">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="9f2c9-171">Jetattachdatabase</span><span class="sxs-lookup"><span data-stu-id="9f2c9-171">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="9f2c9-172">Jetbeginexternalbackup</span><span class="sxs-lookup"><span data-stu-id="9f2c9-172">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="9f2c9-173">Jetopumfile</span><span class="sxs-lookup"><span data-stu-id="9f2c9-173">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="9f2c9-174">Jetreadfile</span><span class="sxs-lookup"><span data-stu-id="9f2c9-174">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="9f2c9-175">Jetstopbackup</span><span class="sxs-lookup"><span data-stu-id="9f2c9-175">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="9f2c9-176">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="9f2c9-176">JetStopService</span></span>](./jetstopservice-function.md)
