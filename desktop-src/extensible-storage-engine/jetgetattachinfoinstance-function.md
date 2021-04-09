---
description: Weitere Informationen finden Sie in der jetgetattachinfoinstance-Funktion.
title: Jetgetattachinfoinstance-Funktion
TOCTitle: JetGetAttachInfoInstance Function
ms:assetid: 978e7817-0720-42fc-a5c1-46e4d44239f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269350(v=EXCHG.10)
ms:contentKeyID: 32765637
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfoInstanceW
- JetGetAttachInfoInstanceA
- JetGetAttachInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 28abf76632f147b6e909c1b8fb036062d5d3af74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865627"
---
# <a name="jetgetattachinfoinstance-function"></a><span data-ttu-id="d4b50-103">Jetgetattachinfoinstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="d4b50-103">JetGetAttachInfoInstance Function</span></span>


<span data-ttu-id="d4b50-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d4b50-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetattachinfoinstance-function"></a><span data-ttu-id="d4b50-105">Jetgetattachinfoinstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="d4b50-105">JetGetAttachInfoInstance Function</span></span>

<span data-ttu-id="d4b50-106">Die **jetgetattachinfoinstance** -Funktion wird bei einer von [jetbeginexternalbackupinstance](./jetbeginexternalbackupinstance-function.md) initiierten Sicherung verwendet, um eine Instanz nach den Namen von Datenbankdateien abzufragen, die Teil der Sicherungsdatei Gruppe werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4b50-106">The **JetGetAttachInfoInstance** function is used during a backup initiated by [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="d4b50-107">Nur Datenbanken, die zurzeit an die Instanz mit [jetattachdatabase](./jetattachdatabase-function.md) angefügt sind, werden berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="d4b50-107">Only databases that are currently attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) will be considered.</span></span> <span data-ttu-id="d4b50-108">Diese Dateien können anschließend mit [jetopanfileinstance](./jetopenfileinstance-function.md) geöffnet und mit [jetreadfileinstance](./jetreadfileinstance-function.md)gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="d4b50-108">These files may subsequently be opened using [JetOpenFileInstance](./jetopenfileinstance-function.md) and read using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

<span data-ttu-id="d4b50-109">**Windows XP: jetgetattachinfoinstance** wurde in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d4b50-109">**Windows XP:  JetGetAttachInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetAttachInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="d4b50-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4b50-110">Parameters</span></span>

<span data-ttu-id="d4b50-111">*lichen*</span><span class="sxs-lookup"><span data-stu-id="d4b50-111">*instance*</span></span>

<span data-ttu-id="d4b50-112">Die-Instanz, die für diesen Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4b50-112">The instance to use for this call.</span></span>

<span data-ttu-id="d4b50-113">Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d4b50-113">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="d4b50-114">In diesem Fall wird die Verwendung dieser globalen Instanz impliziert.</span><span class="sxs-lookup"><span data-stu-id="d4b50-114">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="d4b50-115">Für Windows XP und spätere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) befindet, in dem nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d4b50-115">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="d4b50-116">Andernfalls schlägt der Vorgang mit JET_errRunningInMultiInstanceMode fehl.</span><span class="sxs-lookup"><span data-stu-id="d4b50-116">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="d4b50-117">*Szz*</span><span class="sxs-lookup"><span data-stu-id="d4b50-117">*szz*</span></span>

<span data-ttu-id="d4b50-118">Der Ausgabepuffer, der die Liste der null-terminierten Zeichen folgen empfängt, die den Satz von Datenbankdateien beschreiben, die Teil des Sicherungsdatei Satzes sein sollen.</span><span class="sxs-lookup"><span data-stu-id="d4b50-118">The output buffer that receives the list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="d4b50-119">Die Liste der in diesem Puffer zurückgegebenen Zeichen folgen weist das gleiche Format auf wie eine von der Registrierung verwendete Multizeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d4b50-119">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="d4b50-120">Jede NULL terminierte Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="d4b50-120">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="d4b50-121">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="d4b50-121">*cbMax*</span></span>

<span data-ttu-id="d4b50-122">Die maximale Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d4b50-122">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="d4b50-123">*pcbactual*</span><span class="sxs-lookup"><span data-stu-id="d4b50-123">*pcbActual*</span></span>

<span data-ttu-id="d4b50-124">Ein Zeiger auf den Ausgabepuffer, der die tatsächliche Menge an Zeichen folgen Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="d4b50-124">Pointer to the output buffer that receives the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="d4b50-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4b50-125">Return Value</span></span>

<span data-ttu-id="d4b50-126">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="d4b50-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d4b50-127">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d4b50-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d4b50-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d4b50-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="d4b50-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4b50-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4b50-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d4b50-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d4b50-131">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d4b50-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4b50-132">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="d4b50-132">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="d4b50-133">Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen Befehl von <a href="gg269309(v=exchg.10).md">jetstopbackupinstance</a>abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="d4b50-133">The operation failed because the current external backup has been aborted by a call to <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span></span> <span data-ttu-id="d4b50-134">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d4b50-134">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4b50-135">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d4b50-135">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d4b50-136">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg294108(v=exchg.10).md">jetstopserviceinstance</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d4b50-136">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4b50-137">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d4b50-137">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d4b50-138">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="d4b50-138">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="d4b50-139">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d4b50-139">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4b50-140">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="d4b50-140">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="d4b50-141">Der Sicherungs Vorgang ist fehlgeschlagen, da er außerhalb der Reihenfolge aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="d4b50-141">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="d4b50-142"><strong>Jetgetattachinfoinstance</strong> gibt diesen Fehler zurück, wenn es sich bei der aktuellen Sicherung nicht um eine vollständige Sicherung handelt.</span><span class="sxs-lookup"><span data-stu-id="d4b50-142"><strong>JetGetAttachInfoInstance</strong> will return this error if the current backup is not a full backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4b50-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d4b50-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d4b50-144">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="d4b50-144">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="d4b50-145">Dies kann bei <strong>jetgetattachinfoinstance</strong> vorkommen, wenn das angegebene Instanzhandle ungültig ist (Windows XP und spätere Releases).</span><span class="sxs-lookup"><span data-stu-id="d4b50-145">This can happen for <strong>JetGetAttachInfoInstance</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4b50-146">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="d4b50-146">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="d4b50-147">Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4b50-147">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4b50-148">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d4b50-148">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d4b50-149">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d4b50-149">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4b50-150">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d4b50-150">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d4b50-151">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4b50-151">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4b50-152">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="d4b50-152">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="d4b50-153">Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d4b50-153">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4b50-154">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d4b50-154">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d4b50-155">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="d4b50-155">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d4b50-156">Bei Erfolg werden die angeforderten Informationen zu dem Satz von Datenbankdateien, die Teil des Sicherungsdatei Satzes sein sollen, in den Ausgabe Puffern platziert, sofern bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d4b50-156">On success, the requested information on the set of database files that should be part of the backup file set will be placed in the output buffers where provided.</span></span>

<span data-ttu-id="d4b50-157">Bei einem Fehler ist der Status der Ausgabepuffer nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="d4b50-157">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="d4b50-158">Der Fehler führt dazu, dass der gesamte Sicherungsprozess für die Instanz abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="d4b50-158">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d4b50-159">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4b50-159">Remarks</span></span>

<span data-ttu-id="d4b50-160">Beachten Sie, dass diese API keinen Fehler oder keine Warnung zurückgibt, wenn der Ausgabepuffer zu klein ist, um die vollständige Liste der Dateien zu akzeptieren, die Bestandteil des Sicherungsdatei Satzes sein sollten.</span><span class="sxs-lookup"><span data-stu-id="d4b50-160">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="d4b50-161">Die Anwendung sollte immer einen Puffer bereitstellen, um die tatsächliche Größe dieser Liste zu erhalten, und anhand dieser Informationen ermitteln, ob die Liste abgeschnitten wurde.</span><span class="sxs-lookup"><span data-stu-id="d4b50-161">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d4b50-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4b50-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4b50-163"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d4b50-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d4b50-164">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d4b50-164">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4b50-165"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d4b50-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d4b50-166">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d4b50-166">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4b50-167"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d4b50-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d4b50-168">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="d4b50-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4b50-169"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="d4b50-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d4b50-170">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d4b50-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4b50-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d4b50-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d4b50-172">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d4b50-172">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4b50-173"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="d4b50-173"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="d4b50-174">Implementiert als <strong>jetgetattachinfoinstancew</strong> (Unicode) und <strong>jetgetattachinfoinstancea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="d4b50-174">Implemented as <strong>JetGetAttachInfoInstanceW</strong> (Unicode) and <strong>JetGetAttachInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d4b50-175">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d4b50-175">See Also</span></span>

[<span data-ttu-id="d4b50-176">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d4b50-176">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d4b50-177">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="d4b50-177">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="d4b50-178">Jetattachdatabase</span><span class="sxs-lookup"><span data-stu-id="d4b50-178">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="d4b50-179">Jetbeginexternalbackupinstance</span><span class="sxs-lookup"><span data-stu-id="d4b50-179">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="d4b50-180">Jetopeinfileinstance</span><span class="sxs-lookup"><span data-stu-id="d4b50-180">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="d4b50-181">Jetreadfilinput Stance</span><span class="sxs-lookup"><span data-stu-id="d4b50-181">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="d4b50-182">Jetstopbackupinstance</span><span class="sxs-lookup"><span data-stu-id="d4b50-182">JetStopBackupInstance</span></span>](./jetstopbackupinstance-function.md)  
[<span data-ttu-id="d4b50-183">Jetstopserviczustance</span><span class="sxs-lookup"><span data-stu-id="d4b50-183">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)
