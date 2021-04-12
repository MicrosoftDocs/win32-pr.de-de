---
description: 'Weitere Informationen finden Sie unter: jetreadfile-Funktion'
title: Jetreadfile-Funktion
TOCTitle: JetReadFile Function
ms:assetid: 59dc9e04-7e02-4835-9aed-95cfcf74d780
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269257(v=EXCHG.10)
ms:contentKeyID: 32765559
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFile
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57e11f3b5478f18bc7883974c2f598bf24dcb8fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217051"
---
# <a name="jetreadfile-function"></a><span data-ttu-id="ef7bd-103">Jetreadfile-Funktion</span><span class="sxs-lookup"><span data-stu-id="ef7bd-103">JetReadFile Function</span></span>


<span data-ttu-id="ef7bd-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ef7bd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetreadfile-function"></a><span data-ttu-id="ef7bd-105">Jetreadfile-Funktion</span><span class="sxs-lookup"><span data-stu-id="ef7bd-105">JetReadFile Function</span></span>

<span data-ttu-id="ef7bd-106">Die **jetreadfile** -Funktion Ruft den Inhalt einer Datei ab, die mit [jetopenfile](./jetopenfile-function.md)geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-106">The **JetReadFile** function retrieves the contents of a file opened with [JetOpenFile](./jetopenfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetReadFile(
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="ef7bd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef7bd-107">Parameters</span></span>

<span data-ttu-id="ef7bd-108">*hffile*</span><span class="sxs-lookup"><span data-stu-id="ef7bd-108">*hfFile*</span></span>

<span data-ttu-id="ef7bd-109">Das Handle der zu lesenden Datei.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-109">The handle of the file to be read.</span></span>

<span data-ttu-id="ef7bd-110">*teuren*</span><span class="sxs-lookup"><span data-stu-id="ef7bd-110">*pv*</span></span>

<span data-ttu-id="ef7bd-111">Ausgabepuffer, von dem die Datei Daten empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-111">Output buffer that will receive the file data.</span></span>

<span data-ttu-id="ef7bd-112">*betrieben*</span><span class="sxs-lookup"><span data-stu-id="ef7bd-112">*cb*</span></span>

<span data-ttu-id="ef7bd-113">Die maximale Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-113">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="ef7bd-114">*pcbactual*</span><span class="sxs-lookup"><span data-stu-id="ef7bd-114">*pcbActual*</span></span>

<span data-ttu-id="ef7bd-115">Empfängt die tatsächliche Menge an Datei Daten, die abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-115">Receives the actual amount of file data retrieved.</span></span>

### <a name="return-value"></a><span data-ttu-id="ef7bd-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef7bd-116">Return Value</span></span>

<span data-ttu-id="ef7bd-117">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ef7bd-118">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ef7bd-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef7bd-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ef7bd-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="ef7bd-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef7bd-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef7bd-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ef7bd-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ef7bd-122">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef7bd-123">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="ef7bd-123">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="ef7bd-124">Der Vorgang konnte nicht ausgeführt werden, da die aktuelle externe Sicherung durch einen <a href="gg269240(v=exchg.10).md">jetstopservice</a>-Befehl abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-124">The operation failed because the current external backup has been aborted by a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span> <span data-ttu-id="ef7bd-125">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-125">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef7bd-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="ef7bd-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="ef7bd-127">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef7bd-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ef7bd-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ef7bd-129">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="ef7bd-130">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef7bd-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ef7bd-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ef7bd-132">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="ef7bd-133">Dies kann bei <strong>jetreadfile</strong> vorkommen, wenn Folgendes geschieht:</span><span class="sxs-lookup"><span data-stu-id="ef7bd-133">This can happen for <strong>JetReadFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="ef7bd-134">Das angegebene Instanzhandle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-134">The specified instance handle is invalid.</span></span> <span data-ttu-id="ef7bd-135">Windows XP und spätere Versionen.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-135">Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="ef7bd-136">Bei der Ausgabepuffergröße handelt es sich nicht um ein Vielfaches der Seitengröße der Datenbank (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span><span class="sxs-lookup"><span data-stu-id="ef7bd-136">The output buffer size is not a multiple of the database page size (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span></span> <span data-ttu-id="ef7bd-137">Windows XP und spätere Versionen.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-137">Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="ef7bd-138">Die Ausgabepuffergröße ist kleiner als drei Datenbankseiten (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Dies ist der erste <strong>jetreadfile</strong> -Rückruf für das angegebene Handle.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-138">The output buffer size is smaller than three database pages (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) and this is the first call to <strong>JetReadFile</strong> for the specified handle.</span></span> <span data-ttu-id="ef7bd-139">Windows XP und spätere Versionen.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-139">Windows XP and later releases.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef7bd-140">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="ef7bd-140">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="ef7bd-141">Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-141">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef7bd-142">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ef7bd-142">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ef7bd-143">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-143">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef7bd-144">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="ef7bd-144">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="ef7bd-145">Der Vorgang ist fehlgeschlagen, weil beim Lesen einer Datenbankseite aus einer Datenbankdatei oder einer Datenbank-Patchdatei eine nicht wiederherstellbare Daten Beschädigung festgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-145">The operation failed because non-recoverable data corruption was detected while reading a database page from a database file or database patch file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef7bd-146">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="ef7bd-146">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="ef7bd-147">Der Vorgang ist fehlgeschlagen, weil beim Lesen einer Transaktionsprotokoll Datei eine nicht wiederherstellbare Daten Beschädigung festgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-147">The operation failed because non-recoverable data corruption was detected while reading a transaction log file.</span></span> <span data-ttu-id="ef7bd-148">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-148">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef7bd-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ef7bd-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ef7bd-150">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef7bd-151">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="ef7bd-151">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="ef7bd-152">Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-152">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef7bd-153">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ef7bd-153">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ef7bd-154">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-154">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef7bd-155">Bei Erfolg wird der nächste Datenblock aus der Datei in den Ausgabepuffer eingelesen.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-155">On success, the next chunk of data from the file will be read into the output buffer.</span></span> <span data-ttu-id="ef7bd-156">Die tatsächliche Anzahl der abgerufenen Bytes wird ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-156">The actual number of bytes retrieved will also be returned.</span></span> <span data-ttu-id="ef7bd-157">Der Dateioffset, bei dem der nächste Lesevorgang stattfindet, wird um diesen Betrag erweitert.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-157">The file offset at which the next read will occur will be advanced by this amount.</span></span>

<span data-ttu-id="ef7bd-158">Bei einem Fehler ist der Status des Ausgabepuffers nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-158">On failure, the state of the output buffer is undefined.</span></span> <span data-ttu-id="ef7bd-159">Der Fehler führt dazu, dass der gesamte Sicherungsprozess für die Instanz abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-159">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="ef7bd-160">Unter Windows XP und höheren Versionen wird die Sicherung nicht abgebrochen, wenn beim Lesen einer Datenbankdatei ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-160">On Windows XP and later releases, the backup will not be canceled if an error occurred while reading a database file.</span></span> <span data-ttu-id="ef7bd-161">Die Sicherung der Datenbankdatei wird jedoch weiterhin abgebrochen, und das entsprechende Handle wird automatisch geschlossen.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-161">However, the backup of that database file will still be canceled and the corresponding handle will automatically be closed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ef7bd-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef7bd-162">Remarks</span></span>

<span data-ttu-id="ef7bd-163">Jeder **jetreadfile** -Befehl, der ein Handle verwendet, das bereits alle Daten in der zugrunde liegenden Datei zurückgegeben hat (z. b. ein vorheriger-Rückruf, der weniger Bytes zurückgegeben hat als die Größe des Ausgabepuffers), ist immer erfolgreich, aber gibt NULL Bytes an Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-163">Any call to **JetReadFile** using a handle that has already returned all the data in the underlying file (such as a previous call returned less bytes than the size of the output buffer) will always succeed but return zero bytes of data.</span></span>

<span data-ttu-id="ef7bd-164">Ein großer Ausgabepuffer sollte verwendet werden, um die Sicherungsleistung zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-164">A large output buffer should be used to maximize backup performance.</span></span> <span data-ttu-id="ef7bd-165">Einige Experimente sind möglicherweise erforderlich, um den richtigen Kompromiss zwischen Ressourcenverbrauch und Durchsatz für eine bestimmte Situation zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-165">Some experimentation may be required to find the right tradeoff between resource consumption and throughput for a given situation.</span></span> <span data-ttu-id="ef7bd-166">Der Ausgabepuffer sollte in jedem Fall nicht kleiner als 64 KB sein.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-166">The output buffer should be no smaller than 64KB in any case.</span></span>

<span data-ttu-id="ef7bd-167">Mehrere gleichzeitige Aufrufe von **jetreadfile** mit demselben Datei Handle werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-167">Multiple concurrent calls to **JetReadFile** using the same file handle are not supported.</span></span> <span data-ttu-id="ef7bd-168">Dies bedeutet, dass es nicht möglich ist, mehrere Puffer für einen gleichzeitigen Lesevorgang in eine Warteschlange zu stellen, um einen hohen sequenziellen Durchsatz zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-168">This means that it is not possible to queue several buffers for read concurrently against the same file to achieve high sequential throughput.</span></span> <span data-ttu-id="ef7bd-169">Stattdessen sollte ein einzelner großer Puffer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-169">A single large buffer should be used instead.</span></span>

<span data-ttu-id="ef7bd-170">Wenn die-Instanz so konfiguriert ist, dass das Bereinigen der Datenbankseite aktiviert ist (siehe JET_paramZeroDatabaseDuringBackup in System Parametern), werden gelöschte Daten aus der Datenbank als Nebeneffekt eines **jetreadfile** -Aufrufes in der Datenbankdatei entfernt.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-170">If the instance is configured such that database page scrubbing is enabled (see JET_paramZeroDatabaseDuringBackup in System Parameters) then deleted data will be removed from the database as a side effect of a call to **JetReadFile** against the database file.</span></span>

<span data-ttu-id="ef7bd-171">Es ist sehr wichtig zu verstehen, wie Sicherungen und Daten Beschädigungen interagieren.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-171">It is very important to understand how backup and data corruption interact.</span></span> <span data-ttu-id="ef7bd-172">Wenn die Datenbank-Engine Daten Beschädigungen während einer Sicherung erkennt, schlägt die Sicherung der betroffenen Datenbank oder der gesamten Instanz fehl.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-172">If the database engine detects data corruption during a backup then it will either fail the backup of the affected database or of the entire instance.</span></span> <span data-ttu-id="ef7bd-173">Dies ist eine bewusste Entwurfs Entscheidung, die vor Datenverlusten geschützt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-173">This is a conscious design decision intended to protect against data loss.</span></span> <span data-ttu-id="ef7bd-174">Wenn die Datenbank-Engine die erfolgreiche Ausführung einer Sicherung bei einer Daten Beschädigung gestattet hat, kann es vorkommen, dass eine ältere, nicht beschädigte Sicherung als Ergebnis verworfen wird.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-174">If the database engine allowed a backup to succeed where data corruption was present then it is possible that an older, uncorrupted backup could be discarded as a result.</span></span> <span data-ttu-id="ef7bd-175">Dies wäre leider nicht möglich, da es möglich wäre, die Daten Beschädigung auf der Live Instanz zu beheben, indem diese Sicherung wieder hergestellt und alle Transaktionsprotokoll Dateien für diese Datenbank wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-175">This would be unfortunate because it would be possible to fix the data corruption on the live instance by restoring that backup and replaying all the transaction log files against that database.</span></span> <span data-ttu-id="ef7bd-176">Bei diesem Szenario mit Null Datenverlust wird davon ausgegangen, dass die zirkuläre Protokollierung nicht aktiviert ist (siehe [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parametern](./extensible-storage-engine-system-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="ef7bd-176">This zero data loss scenario presumes that circular logging is not enabled (see [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md)).</span></span>

<span data-ttu-id="ef7bd-177">Es ist auch wichtig zu wissen, dass die streamingingsicherung am wahrscheinlichsten ist, wenn Daten beschädigt werden.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-177">It is also important to understand that when data corruption is present streaming backup will be the most likely place that it will first be detected.</span></span> <span data-ttu-id="ef7bd-178">Dies ist der Fall, da die Streamingsicherung der einzige Prozess ist, der routinemäßig jede einzelne Seite der Datenbankdatei scannt.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-178">This is the case because streaming backup is the only process that routinely scans every single page of the database file.</span></span> <span data-ttu-id="ef7bd-179">Außerdem ist es wahrscheinlich, dass die Streamingsicherung der erste Prozess zum Erkennen der frühen Anzeichen eines Hardwarefehlers ist, wie es bei zeitweiligen Daten Beschädigungen der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-179">It is also likely that streaming backup will be the first process to detect the early signs of hardware failure as manifested by intermittent data corruption errors.</span></span> <span data-ttu-id="ef7bd-180">Der Grund hierfür ist die Menge der von der Sicherung abgerufenen Daten sowie die Geschwindigkeit, mit der Sie abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-180">This is due to the amount of data retrieved by backup as well as the speed at which it is retrieved.</span></span>

<span data-ttu-id="ef7bd-181">Daten Beschädigungen werden von der Datenbank-Engine durch die Verwendung von Block Prüfsummen erkannt.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-181">Data corruption is detected by the database engine through the use of block checksums.</span></span> <span data-ttu-id="ef7bd-182">Diese Prüfsummen werden direkt vor dem Schreiben einer Datenbankseite festgelegt und auf dem Lesevorgang einer Datenbankseite überprüft.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-182">These checksums are set just prior to a database page write and are verified on a database page read.</span></span> <span data-ttu-id="ef7bd-183">Mit diesem Schema kann die Datenbank-Engine feststellen, dass die Daten zu einem bestimmten Zeitpunkt beschädigt wurden, aber die Datenbank-Engine kann die Quelle dieser Beschädigung nicht ermitteln.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-183">This scheme enables the database engine to determine that data has been corrupted at some point but it does not enable the database engine to determine the source of that corruption.</span></span> <span data-ttu-id="ef7bd-184">In der Vergangenheit wurde die vorherrschende Ursache für derartige Beschädigungen aus anderen Quellen als der Datenbank-Engine selbst herausgefunden.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-184">Historically, the predominant cause of such corruption has been found to come from sources other than the database engine itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ef7bd-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef7bd-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef7bd-186"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ef7bd-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ef7bd-187">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef7bd-188"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ef7bd-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ef7bd-189">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef7bd-190"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ef7bd-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ef7bd-191">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef7bd-192"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="ef7bd-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ef7bd-193">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef7bd-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ef7bd-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ef7bd-195">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-195">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ef7bd-196">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ef7bd-196">See Also</span></span>

[<span data-ttu-id="ef7bd-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ef7bd-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ef7bd-198">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="ef7bd-198">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="ef7bd-199">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="ef7bd-199">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="ef7bd-200">Jetopumfile</span><span class="sxs-lookup"><span data-stu-id="ef7bd-200">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="ef7bd-201">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="ef7bd-201">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="ef7bd-202">System Parameter</span><span class="sxs-lookup"><span data-stu-id="ef7bd-202">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
