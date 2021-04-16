---
description: 'Weitere Informationen finden Sie unter: jetreadfilinput Stance-Funktion'
title: JetReadFileInstance-Funktion
TOCTitle: JetReadFileInstance Function
ms:assetid: b17b4b43-86e5-4507-8a85-bbd5eac0aa3c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294060(v=EXCHG.10)
ms:contentKeyID: 32765675
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9aad9828a92d67f2e7411aa534103696d913934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524959"
---
# <a name="jetreadfileinstance-function"></a><span data-ttu-id="a8dc3-103">JetReadFileInstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="a8dc3-103">JetReadFileInstance Function</span></span>


<span data-ttu-id="a8dc3-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a8dc3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetreadfileinstance-function"></a><span data-ttu-id="a8dc3-105">JetReadFileInstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="a8dc3-105">JetReadFileInstance Function</span></span>

<span data-ttu-id="a8dc3-106">Die **jetreadfileinstance** -Funktion Ruft den Inhalt einer Datei ab, die mit der [jetopenfileinstance](./jetopenfileinstance-function.md) -Funktion geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-106">The **JetReadFileInstance** function retrieves the contents of a file opened with the [JetOpenFileInstance](./jetopenfileinstance-function.md) function.</span></span>

<span data-ttu-id="a8dc3-107">**Windows XP**:   **jetreadfileinstance** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-107">**Windows XP**:   **JetReadFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetReadFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcb
    );
```

### <a name="parameters"></a><span data-ttu-id="a8dc3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8dc3-108">Parameters</span></span>

<span data-ttu-id="a8dc3-109">*lichen*</span><span class="sxs-lookup"><span data-stu-id="a8dc3-109">*instance*</span></span>

<span data-ttu-id="a8dc3-110">Die-Instanz, die für einen bestimmten API-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-110">The instance to use for a particular API call.</span></span>

<span data-ttu-id="a8dc3-111">Beachten Sie, dass die API-Variante für Windows 2000 nicht verfügbar ist, da nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-111">Note that for Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="a8dc3-112">In diesem Fall wird die Verwendung dieser globalen Instanz impliziert.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="a8dc3-113">Für Windows XP und spätere Versionen können Sie die API-Variante aufrufen, die diesen Parameter nicht akzeptiert, wenn sich die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) befindet, in Fällen, in denen nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-113">For Windows XP and later releases, you can call the API variant that does not accept this parameter only when the engine is in legacy mode (Windows 2000 compatibility mode) in cases where only one instance is supported.</span></span> <span data-ttu-id="a8dc3-114">Andernfalls schlägt der Vorgang fehl, und es wird der JET_errRunningInMultiInstanceMode Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-114">Otherwise, the operation will fail and return the JET_errRunningInMultiInstanceMode error.</span></span>

<span data-ttu-id="a8dc3-115">*hffile*</span><span class="sxs-lookup"><span data-stu-id="a8dc3-115">*hfFile*</span></span>

<span data-ttu-id="a8dc3-116">Das Handle der zu lesenden Datei.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-116">The handle of the file to be read.</span></span>

<span data-ttu-id="a8dc3-117">*teuren*</span><span class="sxs-lookup"><span data-stu-id="a8dc3-117">*pv*</span></span>

<span data-ttu-id="a8dc3-118">Der Ausgabepuffer, der die Datei Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-118">The output buffer that will receive the file data.</span></span>

<span data-ttu-id="a8dc3-119">*betrieben*</span><span class="sxs-lookup"><span data-stu-id="a8dc3-119">*cb*</span></span>

<span data-ttu-id="a8dc3-120">Die maximale Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-120">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="a8dc3-121">*PCB*</span><span class="sxs-lookup"><span data-stu-id="a8dc3-121">*pcb*</span></span>

<span data-ttu-id="a8dc3-122">Die tatsächliche Menge an Datei Daten, die abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-122">The actual amount of file data retrieved.</span></span>

### <a name="return-value"></a><span data-ttu-id="a8dc3-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8dc3-123">Return Value</span></span>

<span data-ttu-id="a8dc3-124">Diese Funktion vereinfacht die Rückgabe von [JET_ERR](./jet-err.md) Datentypen, die in der ESE-API (Extensible Storage Engine) definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-124">This function facilitates the return of any [JET_ERR](./jet-err.md) data types that are defined in the Extensible Storage Engine (ESE) API.</span></span> <span data-ttu-id="a8dc3-125">Weitere Informationen zu Jet-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a8dc3-125">For more information about JET errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8dc3-126">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a8dc3-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="a8dc3-127">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a8dc3-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8dc3-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a8dc3-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a8dc3-129">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8dc3-130">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="a8dc3-130">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="a8dc3-131">Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen-Befehl der <a href="gg269240(v=exchg.10).md">jetstopservice</a> -Funktion abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-131">The operation failed because the current external backup has been aborted by a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span> <span data-ttu-id="a8dc3-132">Dieser Fehler wird nur von Windows XP und neueren Windows-Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-132">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8dc3-133">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a8dc3-133">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a8dc3-134">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens der <a href="gg269240(v=exchg.10).md">jetstopservice</a> -Funktion beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-134">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8dc3-135">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a8dc3-135">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a8dc3-136">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-136">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error requiring that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="a8dc3-137">Dieser Fehler wird nur von Windows XP und neueren Windows-Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-137">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8dc3-138">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a8dc3-138">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a8dc3-139">Einer der angegebenen Parameter enthielt entweder einen unerwarteten Wert oder einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-139">One of the specified parameters contained either an unexpected value or a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="a8dc3-140">Dies kann für die <strong>jetreadfilinput Stance</strong> -Funktion auftreten, wenn eine der folgenden Aktionen auftritt:</span><span class="sxs-lookup"><span data-stu-id="a8dc3-140">This can happen for the <strong>JetReadFileInstance</strong> function when any of the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="a8dc3-141">Das angegebene Instanzhandle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-141">The specified instance handle is invalid.</span></span> <span data-ttu-id="a8dc3-142">Windows XP und neuere Windows-Versionen.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-142">Windows XP and later Windows versions.</span></span></p></li>
<li><p><span data-ttu-id="a8dc3-143">Bei der Ausgabepuffergröße handelt es sich nicht um ein Vielfaches der Seitengröße der Datenbank (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span><span class="sxs-lookup"><span data-stu-id="a8dc3-143">The output buffer size is not a multiple of the database page size (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span></span> <span data-ttu-id="a8dc3-144">Windows XP und neuere Windows-Versionen.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-144">Windows XP and later Windows versions.</span></span></p></li>
<li><p><span data-ttu-id="a8dc3-145">Die Ausgabepuffergröße ist kleiner als drei Datenbankseiten (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Dies ist der erste Rückruf der <strong>jetreadfileinstance</strong> -Funktion für das angegebene Handle.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-145">The output buffer size is smaller than three database pages (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), and this is the first call to the <strong>JetReadFileInstance</strong> function for the specified handle.</span></span> <span data-ttu-id="a8dc3-146">Windows XP und neuere Windows-Versionen.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-146">Windows XP and later Windows versions.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8dc3-147">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="a8dc3-147">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="a8dc3-148">Der Vorgang ist fehlgeschlagen, weil nicht BEHEB bare Daten beim Lesen einer Transaktionsprotokoll Datei erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-148">The operation failed because unrecoverable data corruption was detected while reading a transaction log file.</span></span> <span data-ttu-id="a8dc3-149">Dieser Fehler wird nur von Windows XP und neueren Windows-Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-149">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8dc3-150">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="a8dc3-150">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="a8dc3-151">Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-151">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8dc3-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a8dc3-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a8dc3-153">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die dieser Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-153">It is not possible to complete the operation because the instance associated with this session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8dc3-154">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="a8dc3-154">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="a8dc3-155">Der Vorgang ist fehlgeschlagen, da nicht BEHEB bare Daten beim Lesen einer Datenbankseite aus einer Datenbankdatei oder einer Datenbank-Patchdatei erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-155">The operation failed because unrecoverable data corruption was detected while reading a database page from a database file or database patch file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8dc3-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a8dc3-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a8dc3-157">Der Vorgang kann nicht abgeschlossen werden, da für die Instanz, die dieser Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8dc3-158">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="a8dc3-158">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="a8dc3-159">Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in einem Fall, in dem nur eine Instanz unterstützt wird, aber mehrere Instanzen bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-159">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) in a case where only one instance is supported but multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8dc3-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a8dc3-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a8dc3-161">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die dieser Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-161">It is not possible to complete the operation because the instance associated with this session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a8dc3-162">Bei Erfolg wird der nächste Datenblock aus der Datei in den Ausgabepuffer eingelesen.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-162">On success, the next chunk of data from the file will be read into the output buffer.</span></span> <span data-ttu-id="a8dc3-163">Die tatsächliche Anzahl der abgerufenen Bytes wird ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-163">The actual number of bytes retrieved will also be returned.</span></span> <span data-ttu-id="a8dc3-164">Der Dateioffset, bei dem der nächste Lesevorgang stattfindet, wird um diesen Betrag erweitert.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-164">The file offset at which the next read will occur will be advanced by this amount.</span></span>

<span data-ttu-id="a8dc3-165">Bei einem Fehler ist der Status des Ausgabepuffers nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-165">On failure, the state of the output buffer is undefined.</span></span> <span data-ttu-id="a8dc3-166">Der Fehler führt dazu, dass der gesamte Sicherungsprozess für die aktuelle Instanz abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-166">The failure will result in the cancellation of the entire backup process for the current instance.</span></span> <span data-ttu-id="a8dc3-167">In Windows XP und neueren Windows-Versionen wird die Sicherung nicht abgebrochen, wenn beim Lesen einer Datenbankdatei ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-167">In Windows XP and later Windows versions, the backup will not be canceled if an error occurred while reading a database file.</span></span> <span data-ttu-id="a8dc3-168">Die Sicherung der Datenbankdatei wird jedoch weiterhin abgebrochen, und das entsprechende Handle wird automatisch geschlossen.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-168">However, the backup of that database file will still be canceled and the corresponding handle will automatically be closed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a8dc3-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8dc3-169">Remarks</span></span>

<span data-ttu-id="a8dc3-170">Jeder Aufrufe der **jetreadfileinstance** -Funktion, die mithilfe eines Handles vorgenommen wurde, das bereits alle Daten in der zugrunde liegenden Datei zurückgegeben hat (z. b., wenn ein vorheriger-Rückruf weniger Bytes zurückgegeben hat als die Größe des Ausgabepuffers), wird immer erfolgreich ausgeführt, gibt aber NULL Bytes an Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-170">Any call to the **JetReadFileInstance** function made by using a handle that has already returned all the data in the underlying file (such as if a previous call returned fewer bytes than the size of the output buffer) will always succeed but will return zero bytes of data.</span></span>

<span data-ttu-id="a8dc3-171">Sie sollten einen großen Ausgabepuffer verwenden, um die Sicherungsleistung zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-171">You should use a large output buffer to maximize backup performance.</span></span> <span data-ttu-id="a8dc3-172">Möglicherweise müssen Sie experimentieren, um den optimalen Kompromiss zwischen Ressourcenverbrauch und Durchsatz für eine bestimmte Situation zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-172">You might need to experiment to find the optimal tradeoff between resource consumption and throughput for a particular situation.</span></span> <span data-ttu-id="a8dc3-173">In jedem Fall sollte der Ausgabepuffer nicht kleiner als 64 KB sein.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-173">In any case, the output buffer should be no smaller than 64 KB.</span></span> <span data-ttu-id="a8dc3-174">Der Zeiger, den Sie an **jetreadfilinput Stance** übergeben, muss an einer Seitenbegrenzung für den Arbeitsspeicher (4 KB oder 8 KB) ausgerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-174">The pointer that you pass to **JetReadFileInstance** must be aligned with a memory page boundary (either 4 KB or 8 KB).</span></span> <span data-ttu-id="a8dc3-175">Dies können Sie erreichen, indem Sie die **virtualzuweisung** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-175">You can do this by calling the **VirtualAlloc** function.</span></span>

<span data-ttu-id="a8dc3-176">Mehrere gleichzeitige Aufrufe von **jetreadfileinstance** , die mithilfe desselben Datei Handles durchgeführt werden, werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-176">Multiple concurrent calls to **JetReadFileInstance** made by using the same file handle are not supported.</span></span> <span data-ttu-id="a8dc3-177">Dies bedeutet, dass es nicht möglich ist, mehrere Puffer in die Warteschlange zu stellen, um gleichzeitige Lesevorgänge für dieselbe Datei durchzuführen</span><span class="sxs-lookup"><span data-stu-id="a8dc3-177">This means that it is not possible to queue several buffers for concurrent reading against the same file to achieve high sequential throughput.</span></span> <span data-ttu-id="a8dc3-178">Verwenden Sie stattdessen einen einzelnen großen Puffer.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-178">You should use a single large buffer instead.</span></span>

<span data-ttu-id="a8dc3-179">Wenn Sie eine bestimmte Instanz so konfiguriert haben, dass die Datenbankseiten Bereinigung aktiviert ist (siehe den [JET_paramCircularLog](./transaction-log-parameters.md) Parameter in [System Parametern](./extensible-storage-engine-system-parameters.md)), werden gelöschte Daten aus der Datenbank als Nebeneffekt eines Aufrufes **jetreadfileinstance** für die Datenbankdatei entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-179">If you have configured a particular instance such that database page scrubbing is enabled (see the [JET_paramCircularLog](./transaction-log-parameters.md) parameter in [System Parameters](./extensible-storage-engine-system-parameters.md)), deleted data will be removed from the database as a side-effect of a call to **JetReadFileInstance** against the database file.</span></span>

<span data-ttu-id="a8dc3-180">Es ist sehr wichtig zu verstehen, wie Sicherungen und Daten Beschädigungen interagieren.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-180">It is very important to understand how backup and data corruption interact.</span></span> <span data-ttu-id="a8dc3-181">Wenn die Datenbank-Engine während einer Sicherung Daten Beschädigungen erkennt, schlägt die Sicherung der betroffenen Datenbank oder der gesamten Instanz fehl.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-181">If the database engine detects data corruption during a backup, it will fail the backup of either the affected database or the entire instance.</span></span> <span data-ttu-id="a8dc3-182">Dies ist eine bewusste Entwurfs Entscheidung, die vor Datenverlusten geschützt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-182">This is a conscious design decision intended to protect against data loss.</span></span> <span data-ttu-id="a8dc3-183">Wenn die Datenbank-Engine die erfolgreiche Ausführung einer Sicherung bei einer Daten Beschädigung gestattet hat, kann es vorkommen, dass eine ältere, nicht beschädigte Sicherung als Ergebnis verworfen wird.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-183">If the database engine allowed a backup to succeed where data corruption was present, it is possible that an older, uncorrupted backup could be discarded as a result.</span></span> <span data-ttu-id="a8dc3-184">Dies wäre leider nicht möglich, da es dann möglich wäre, die Daten Beschädigung auf der Live Instanz zu beheben, indem diese Sicherung wieder hergestellt und alle Transaktionsprotokoll Dateien für diese Datenbank wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-184">This would be unfortunate because then it would be possible to fix the data corruption on the live instance by restoring that backup and replaying all the transaction log files against that database.</span></span> <span data-ttu-id="a8dc3-185">Bei diesem Szenario mit Null Datenverlust wird davon ausgegangen, dass die zirkuläre Protokollierung nicht aktiviert ist (siehe [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parametern](./extensible-storage-engine-system-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="a8dc3-185">This zero-data-loss scenario presumes that circular logging is not enabled (see [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md)).</span></span>

<span data-ttu-id="a8dc3-186">Es ist auch wichtig zu verstehen, dass die Fälle von Daten Beschädigungen bei der Streamingsicherung zuerst erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-186">It is also important to understand that cases of data corruption are usually first detected during streaming backup.</span></span> <span data-ttu-id="a8dc3-187">Dies liegt daran, dass die Streamingsicherung der einzige Prozess ist, der routinemäßig jede einzelne Seite der Datenbankdatei scannt.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-187">This is because streaming backup is the only process that routinely scans every single page of the database file.</span></span> <span data-ttu-id="a8dc3-188">Außerdem ist es wahrscheinlich, dass die Streamingsicherung der erste Prozess zum Erkennen der frühen Anzeichen eines Hardwarefehlers ist, wie es bei zeitweiligen Daten Beschädigungen der Fall ist, weil die von der Sicherung abgerufenen Datenmenge und die Geschwindigkeit, mit der die Daten abgerufen werden, auftreten.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-188">It is also likely that streaming backup will be the first process to detect the early signs of hardware failure as manifested by intermittent data corruption errors, because of both the amount of data retrieved by backup and the speed at which that data is retrieved.</span></span>

<span data-ttu-id="a8dc3-189">Daten Beschädigungen werden von der Datenbank-Engine durch die Verwendung von Block Prüfsummen erkannt.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-189">Data corruption is detected by the database engine through the use of block checksums.</span></span> <span data-ttu-id="a8dc3-190">Diese Prüfsummen werden direkt vor dem Schreiben einer Datenbankseite festgelegt und auf dem Lesevorgang einer Datenbankseite überprüft.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-190">These checksums are set just before a database page write and are verified on a database page read.</span></span> <span data-ttu-id="a8dc3-191">Mit diesem Schema kann die Datenbank-Engine ermitteln, dass die Daten zu einem bestimmten Zeitpunkt beschädigt wurden, aber die Datenbank-Engine kann die Quelle dieser Beschädigung nicht ermitteln.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-191">This scheme enables the database engine to determine that data has been corrupted at some point, but it does not enable the database engine to determine the source of that corruption.</span></span> <span data-ttu-id="a8dc3-192">In der Vergangenheit stammen Instanzen solcher Daten Beschädigungen aus anderen Quellen als der Datenbank-Engine selbst.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-192">Historically, instances of such data corruption have originated from sources other than the database engine itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a8dc3-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8dc3-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8dc3-194">Client</span><span class="sxs-lookup"><span data-stu-id="a8dc3-194">Client</span></span></p></td>
<td><p><span data-ttu-id="a8dc3-195">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-195">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8dc3-196">Server</span><span class="sxs-lookup"><span data-stu-id="a8dc3-196">Server</span></span></p></td>
<td><p><span data-ttu-id="a8dc3-197">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-197">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8dc3-198">Header</span><span class="sxs-lookup"><span data-stu-id="a8dc3-198">Header</span></span></p></td>
<td><p><span data-ttu-id="a8dc3-199">Wird in "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-199">Is declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8dc3-200">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a8dc3-200">Library</span></span></p></td>
<td><p><span data-ttu-id="a8dc3-201">Verwendet ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-201">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8dc3-202">DLL</span><span class="sxs-lookup"><span data-stu-id="a8dc3-202">DLL</span></span></p></td>
<td><p><span data-ttu-id="a8dc3-203">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-203">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a8dc3-204">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a8dc3-204">See Also</span></span>

[<span data-ttu-id="a8dc3-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a8dc3-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a8dc3-206">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="a8dc3-206">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="a8dc3-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a8dc3-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a8dc3-208">Jetopeinfileinstance</span><span class="sxs-lookup"><span data-stu-id="a8dc3-208">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="a8dc3-209">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="a8dc3-209">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="a8dc3-210">System Parameter</span><span class="sxs-lookup"><span data-stu-id="a8dc3-210">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
