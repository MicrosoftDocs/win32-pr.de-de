---
description: 'Weitere Informationen finden Sie hier: JetRestore2-Funktion'
title: JetRestore2-Funktion
TOCTitle: JetRestore2 Function
ms:assetid: 7f7fc2e3-727a-43e4-8497-64ff56d92b9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269313(v=EXCHG.10)
ms:contentKeyID: 32765603
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore2
- JetRestore2A
- JetRestore2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb297aac0bc26e50bba519206eff346abb7943c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352320"
---
# <a name="jetrestore2-function"></a><span data-ttu-id="88dc0-103">JetRestore2-Funktion</span><span class="sxs-lookup"><span data-stu-id="88dc0-103">JetRestore2 Function</span></span>


<span data-ttu-id="88dc0-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="88dc0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrestore2-function"></a><span data-ttu-id="88dc0-105">JetRestore2-Funktion</span><span class="sxs-lookup"><span data-stu-id="88dc0-105">JetRestore2 Function</span></span>

<span data-ttu-id="88dc0-106">Der **JetRestore2** stellt eine Streamingsicherung einer Instanz wieder her, einschließlich aller angefügten Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="88dc0-106">The **JetRestore2** restores and recovers a streaming backup of an instance, including all the attached databases.</span></span> <span data-ttu-id="88dc0-107">Bei dieser Funktion handelt es sich hauptsächlich um Abwärtskompatibilität mit Windows 2000 und früheren Datenbank-Engines, bei denen nur eine Instanz einer Datenbank zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="88dc0-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="88dc0-108">In diesem Fall ist die aktive Instanz die Instanz, die wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="88dc0-108">In this case, the active instance is the instance that is restored.</span></span>

```cpp
    JET_ERR JET_API JetRestore2(
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="88dc0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="88dc0-109">Parameters</span></span>

<span data-ttu-id="88dc0-110">*RT*</span><span class="sxs-lookup"><span data-stu-id="88dc0-110">*sz*</span></span>

<span data-ttu-id="88dc0-111">Der Ordner, in dem sich die Sicherung befindet.</span><span class="sxs-lookup"><span data-stu-id="88dc0-111">The folder where the backup is located.</span></span> <span data-ttu-id="88dc0-112">Die Sicherung muss mithilfe der [JetBackup](./jetbackup-function.md) -APIs generiert werden.</span><span class="sxs-lookup"><span data-stu-id="88dc0-112">The backup should have been generated using the [JetBackup](./jetbackup-function.md) APIs.</span></span>

<span data-ttu-id="88dc0-113">*szdest*</span><span class="sxs-lookup"><span data-stu-id="88dc0-113">*szDest*</span></span>

<span data-ttu-id="88dc0-114">Der Name des Ordners, in den die Datenbankdateien aus dem Sicherungs Satz kopiert und wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="88dc0-114">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="88dc0-115">Wenn dies auf NULL festgelegt ist (Dies ist der Fall für den Legacy- [jetrestore](./jetrestore-function.md)), werden die Datenbankdateien kopiert und an Ihrem ursprünglichen Speicherort wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="88dc0-115">If this is set to NULL (which is the case for the legacy [JetRestore](./jetrestore-function.md)), the database files will be copied and recovered to their original location.</span></span>

<span data-ttu-id="88dc0-116">*PFN*</span><span class="sxs-lookup"><span data-stu-id="88dc0-116">*pfn*</span></span>

<span data-ttu-id="88dc0-117">Der optionale Zeiger auf die Funktion, die als Benachrichtigungs Informationen zum Fortschritt des Wiederherstellungs Vorgangs aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="88dc0-117">The optional pointer to the function which will be called as notification information about the progress of the restore operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="88dc0-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88dc0-118">Return Value</span></span>

<span data-ttu-id="88dc0-119">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="88dc0-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="88dc0-120">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="88dc0-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="88dc0-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="88dc0-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="88dc0-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88dc0-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88dc0-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="88dc0-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="88dc0-124">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="88dc0-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88dc0-125">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="88dc0-125">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="88dc0-126">Der Vorgang ist fehlgeschlagen, da die Engine für diese Instanz bereits initialisiert ist.</span><span class="sxs-lookup"><span data-stu-id="88dc0-126">The operation failed because the engine is already initialized for this instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88dc0-127">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="88dc0-127">JET_errInvalidLogSequence</span></span></p></td>
<td><p><span data-ttu-id="88dc0-128">Der Satz von Protokolldateien aus dem Sicherungs Satz und aus dem aktuellen Protokoll Pfad stimmt nicht mit dem Satz der Protokolldateien identisch.</span><span class="sxs-lookup"><span data-stu-id="88dc0-128">The set of log files from the backup set and from the current log path do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88dc0-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="88dc0-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="88dc0-130">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="88dc0-130">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="88dc0-131">Dieser Fehler wird von <a href="gg269306(v=exchg.10).md">jetrestoreinstance</a> zurückgegeben, wenn sich die Engine im multiinstanzmodus befindet und pinstance auf eine ungültige Instanz von Windows XP und höheren Versionen verweist.</span><span class="sxs-lookup"><span data-stu-id="88dc0-131">This error will be returned by <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> when the engine is in multi-instance mode and pinstance refers to an invalid instance Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88dc0-132">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="88dc0-132">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="88dc0-133">Der Vorgang ist fehlgeschlagen, weil einige der angegebenen Pfade ungültig sind (der Sicherungs Pfad, der Zielpfad, der Protokoll-oder Systempfad für die Instanz).</span><span class="sxs-lookup"><span data-stu-id="88dc0-133">The operation failed because some of paths provided are invalid (the backup path, the destination path, the log or system path for the instance).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88dc0-134">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="88dc0-134">JET_errPageSizeMismatch</span></span></p></td>
<td><p><span data-ttu-id="88dc0-135">Der Vorgang ist fehlgeschlagen, da die Engine für die Verwendung einer Datenbankseiten Größe (mit <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> für <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) konfiguriert ist, die nicht mit der Datenbankseiten Größe identisch ist, die zum Erstellen der Transaktionsprotokoll Dateien oder der Datenbanken verwendet wird, die den Transaktionsprotokoll Dateien zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="88dc0-135">The operation failed because the engine is configured to use a database page size (using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) that does not match the database page size used to create the transaction log files or the databases associated with the transaction log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88dc0-136">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="88dc0-136">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="88dc0-137">Der Vorgang ist fehlgeschlagen, weil die Parameter den einzelinstanzmodus (Windows 2000-Kompatibilitätsmodus) impliziert haben und sich die Engine bereits im Modus für mehrere Instanzen befindet.</span><span class="sxs-lookup"><span data-stu-id="88dc0-137">The operation failed because the parameters implied single instance mode (Windows 2000 compatibility mode) and the engine is already in multi-instance mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="88dc0-138">Bei Erfolg werden Datenbankdateien aus dem Sicherungs Satz an ihrem Speicherort wieder hergestellt, und die Wiederherstellung wird ausgeführt, sodass sich die Datenbanken in einem sauberen Transaktions Konsistenz Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="88dc0-138">On success, database files from the backup set will be restored over to their location and recovery will be run such that the databases will be in a clean transactional consistency state.</span></span> <span data-ttu-id="88dc0-139">Bei der Wiederherstellung werden die Protokolldateien aus dem Sicherungs Satz und die Protokolldateien aus dem Protokoll Pfad wiedergegeben, wenn solche Dateien vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="88dc0-139">Recovery will replay the log files from the backup set and the log files from the log path if such files do exists.</span></span> <span data-ttu-id="88dc0-140">Diese Wiederherstellung führt zu Änderungen an der Prüf Punkt Datei, den Transaktionsprotokoll Dateien und allen Datenbanken, auf die von diesen Transaktionsprotokoll Dateien verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="88dc0-140">This recovery will result in changes to the checkpoint file, the transaction log files, and any databases referenced by those transaction log files.</span></span>

<span data-ttu-id="88dc0-141">Bei einem Fehler verbleibt die Instanz in einem nicht initialisierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="88dc0-141">On failure, the instance remains in an uninitialized state.</span></span> <span data-ttu-id="88dc0-142">Der Status der Transaktionsprotokoll Dateien und sämtlicher Datenbanken, auf die von diesen Transaktionsprotokoll Dateien verwiesen wird, wurde bei dem Versuch, die Wiederherstellung zu initialisieren und die Datenbanken wiederherzustellen, wahrscheinlich geändert.</span><span class="sxs-lookup"><span data-stu-id="88dc0-142">The state of the transaction log files and any databases referenced by those transaction log files will likely have been changed in the attempt to initialize the restore and recover the databases.</span></span>

#### <a name="remarks"></a><span data-ttu-id="88dc0-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88dc0-143">Remarks</span></span>

<span data-ttu-id="88dc0-144">Beim Wiederherstellungs Vorgang werden die Datenbanken, die während der Sicherung an die Instanz angefügt sind, rekonstruiert und die Änderungen in den Datenbankdateien wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="88dc0-144">The recovery process will reconstruct the databases attached to the instance during the backup and save the changes back to the database files.</span></span> <span data-ttu-id="88dc0-145">Das Ergebnis sind Datenbanken, die Transaktions konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="88dc0-145">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="88dc0-146">Wenn möglich, werden die Änderungen, die seit der Sicherung vorgenommen wurden, auch in der Datenbank gespeichert, bis die letzte Änderung in den Transaktions Protokollen gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="88dc0-146">If possible, it will also save to the database the changes done since the backup was taken until the most recent change found in the transaction logs.</span></span> <span data-ttu-id="88dc0-147">Dies wäre möglich, wenn die seit der Sicherung generierten Transaktionsprotokolle weiterhin im Transaktionsprotokoll Verzeichnis vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="88dc0-147">This would be possible if the transaction logs generated since the backup was taken are still present in the transaction log directory.</span></span> <span data-ttu-id="88dc0-148">Beachten Sie Folgendes: Wenn die zirkuläre Protokollierung für die Instanz aktiviert wurde, werden die generierten Transaktionsprotokolle so wieder verwendet, dass die Wiederherstellung die Änderungen speichern kann, die bis zum Sicherungs Zeitpunkt stattfinden.</span><span class="sxs-lookup"><span data-stu-id="88dc0-148">Note that if circular logging was enabled for the instance, the transaction logs generated are reused such that the recovery will be able to save the changes which took place up to the backup moment.</span></span> <span data-ttu-id="88dc0-149">In jedem Fall ist es möglich, dass dieser Vorgang sehr viel Zeit in Anspruch nimmt, wenn die Anzahl der Transaktionsprotokoll Dateien, die für die Datenbanken wiedergegeben werden sollen, groß ist.</span><span class="sxs-lookup"><span data-stu-id="88dc0-149">In any case, it is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="88dc0-150">[Jetrestore](./jetrestore-function.md) -Funktionen müssen für eine Instanz aufgerufen werden, bevor [jetinit](./jetinit-function.md) für diese Instanz aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="88dc0-150">[JetRestore](./jetrestore-function.md) functions must be called on an instance before [JetInit](./jetinit-function.md) is called for that instance.</span></span>

<span data-ttu-id="88dc0-151">Da bei der Wiederherstellung eine beträchtliche Anzahl von Datenbankseiten und Transaktions Protokollen verwendet wird, gibt es eine ganze Reihe von Fehlern, die von diesen Funktionen zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="88dc0-151">Because during recovery a significant number of database pages and transaction logs will be used, there is an entire series of error which might be returned by these functions.</span></span> <span data-ttu-id="88dc0-152">Solche Fehler können aus temporären Ressourcen Zuordnungs Fehlern wie JET_errOutOfMemory zu Fehlern bestehen, die physische Beschädigungen wie JET_errReadVerifyFailure, JET_errLogFileCorrupt oder JET_errBadPageLink darstellen.</span><span class="sxs-lookup"><span data-stu-id="88dc0-152">Such errors can be from temporary resource allocation failures like Jet_errOutOfMemory to errors representing physical corruptions like JET_errReadVerifyFailure, JET_errLogFileCorrupt or JET_errBadPageLink.</span></span> <span data-ttu-id="88dc0-153">Diese Fehler werden fast immer durch Hardwareprobleme verursacht und können daher nicht vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="88dc0-153">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="88dc0-154">Die Datei Misswirtschaft wird am häufigsten als JET_errMissingLogFile oder JET_errAttachedDatabaseMismatch oder JET_errDatabaseSharingViolation oder JET_errInvalidLogSequence Manifest.</span><span class="sxs-lookup"><span data-stu-id="88dc0-154">File mismanagement will manifest itself most often as JET_errMissingLogFile or JET_errAttachedDatabaseMismatch or JET_errDatabaseSharingViolation or JET_errInvalidLogSequence.</span></span> <span data-ttu-id="88dc0-155">Diese Fehler können von der Anwendung verhindert werden.</span><span class="sxs-lookup"><span data-stu-id="88dc0-155">These errors are preventable by the application.</span></span> <span data-ttu-id="88dc0-156">Die Anwendung muss darauf achten, das Repository dieser Dateien vor der Bearbeitung durch externe Kräfte wie z. b. den Benutzer oder andere Anwendungen zu schützen.</span><span class="sxs-lookup"><span data-stu-id="88dc0-156">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="88dc0-157">Wenn die Anwendung eine Instanz vollständig zerstören möchte, müssen alle Dateien, die der Instanz zugeordnet sind, gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="88dc0-157">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="88dc0-158">Hierzu gehören die Prüf Punkt Datei, die Transaktionsprotokoll Dateien und alle Datenbankdateien, die an die Instanz angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="88dc0-158">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="88dc0-159">In den verschiedenen Schritten der Wiederherstellung werden Ereignisprotokoll Einträge generiert, einschließlich des Status der Wiedergabe des Transaktions Protokolls und des Endergebnis der Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="88dc0-159">The different steps of the recovery will have Event Log entries generated including the transaction log replay progress and the final result of the restore.</span></span>

#### <a name="requirements"></a><span data-ttu-id="88dc0-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88dc0-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88dc0-161"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="88dc0-161"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="88dc0-162">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="88dc0-162">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88dc0-163"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="88dc0-163"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="88dc0-164">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="88dc0-164">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88dc0-165"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="88dc0-165"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="88dc0-166">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="88dc0-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88dc0-167"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="88dc0-167"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="88dc0-168">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="88dc0-168">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88dc0-169"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="88dc0-169"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="88dc0-170">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="88dc0-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88dc0-171"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="88dc0-171"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="88dc0-172">Implementiert als <strong>JetRestore2W</strong> (Unicode) und <strong>JetRestore2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="88dc0-172">Implemented as <strong>JetRestore2W</strong> (Unicode) and <strong>JetRestore2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="88dc0-173">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="88dc0-173">See Also</span></span>

[<span data-ttu-id="88dc0-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="88dc0-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="88dc0-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="88dc0-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="88dc0-176">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="88dc0-176">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="88dc0-177">JetBackup</span><span class="sxs-lookup"><span data-stu-id="88dc0-177">JetBackup</span></span>](./jetbackup-function.md)  
[<span data-ttu-id="88dc0-178">Jetbackupinstance</span><span class="sxs-lookup"><span data-stu-id="88dc0-178">JetBackupInstance</span></span>](./jetbackupinstance-function.md)  
[<span data-ttu-id="88dc0-179">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="88dc0-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="88dc0-180">JetInit</span><span class="sxs-lookup"><span data-stu-id="88dc0-180">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="88dc0-181">Jetrestore</span><span class="sxs-lookup"><span data-stu-id="88dc0-181">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="88dc0-182">Jetrestoreingestance</span><span class="sxs-lookup"><span data-stu-id="88dc0-182">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="88dc0-183">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="88dc0-183">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
