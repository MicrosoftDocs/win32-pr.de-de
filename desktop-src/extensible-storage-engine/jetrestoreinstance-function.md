---
description: 'Weitere Informationen zu: jetrestorerstance-Funktion'
title: JetRestoreInstance-Funktion
TOCTitle: JetRestoreInstance Function
ms:assetid: 7ba2b6ee-96f5-44c5-9842-5e58580f60f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269306(v=EXCHG.10)
ms:contentKeyID: 32765597
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestoreInstanceW
- JetRestoreInstance
- JetRestoreInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb7af096a63880a88496631999ddbc26a975cac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218130"
---
# <a name="jetrestoreinstance-function"></a><span data-ttu-id="659a8-103">JetRestoreInstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="659a8-103">JetRestoreInstance Function</span></span>


<span data-ttu-id="659a8-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="659a8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrestoreinstance-function"></a><span data-ttu-id="659a8-105">JetRestoreInstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="659a8-105">JetRestoreInstance Function</span></span>

<span data-ttu-id="659a8-106">Die **jetrestoreinstance** -Funktion stellt eine Streamingsicherung einer Instanz wieder her, die alle angefügten Datenbanken einschließt.</span><span class="sxs-lookup"><span data-stu-id="659a8-106">The **JetRestoreInstance** function restores and recovers a streaming backup of an instance including all the attached databases.</span></span> <span data-ttu-id="659a8-107">Es ist für die Arbeit mit einer mit der [jetbackupinstance](./jetbackupinstance-function.md) -Funktion erstellten Sicherung konzipiert.</span><span class="sxs-lookup"><span data-stu-id="659a8-107">It is designed to work with a backup created with the [JetBackupInstance](./jetbackupinstance-function.md) function.</span></span> <span data-ttu-id="659a8-108">Dies ist die einfachste und am meisten gekapselte Wiederherstellungs Funktion.</span><span class="sxs-lookup"><span data-stu-id="659a8-108">This is the simplest and most encapsulated one restore function.</span></span>

<span data-ttu-id="659a8-109">**Windows XP:**  **jetrestoreinstance** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="659a8-109">**Windows XP:**  **JetRestoreInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRestoreInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="659a8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="659a8-110">Parameters</span></span>

<span data-ttu-id="659a8-111">*lichen*</span><span class="sxs-lookup"><span data-stu-id="659a8-111">*instance*</span></span>

<span data-ttu-id="659a8-112">Gibt die-Instanz an, die für diesen Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="659a8-112">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="659a8-113">Für Windows XP und spätere Versionen hängt die Verwendung dieses Parameters vom Betriebsmodus der Engine ab.</span><span class="sxs-lookup"><span data-stu-id="659a8-113">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="659a8-114">Wenn die Engine im Legacy Modus betrieben wird (Windows 2000-Kompatibilitätsmodus), in dem nur eine Instanz unterstützt wird, kann dieser Parameter entweder NULL sein, oder er kann auf einen gültigen Ausgabepuffer festgelegt werden, der NULL oder JET_instanceNil enthält, der das globale Instanzhandle zurückgibt, das als Nebeneffekt der Initialisierung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="659a8-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported then this parameter may either be NULL or it may be set to a valid output buffer containing NULL or JET_instanceNil that will return the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="659a8-115">Dieser Instanzhandle kann dann an jede andere API weitergegeben werden, die eine-Instanz annimmt.</span><span class="sxs-lookup"><span data-stu-id="659a8-115">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="659a8-116">Wenn die Engine im Modus für mehrere Instanzen betrieben wird, muss dieser Parameter auf einen gültigen Eingabepuffer festgelegt werden, der das von [jetkreateinstance](./jetcreateinstance-function.md) zurückgegebene Instanzhandle enthält, das initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="659a8-116">If the engine is operating in multi-instance mode then this parameter must be set to a valid input buffer that contains the instance handle returned by [JetCreateInstance](./jetcreateinstance-function.md) that is being initialized.</span></span>

<span data-ttu-id="659a8-117">*RT*</span><span class="sxs-lookup"><span data-stu-id="659a8-117">*sz*</span></span>

<span data-ttu-id="659a8-118">Der Ordner, in dem sich die Sicherung befindet.</span><span class="sxs-lookup"><span data-stu-id="659a8-118">The folder where the backup is located.</span></span> <span data-ttu-id="659a8-119">Die Sicherung muss mithilfe der [JetBackup](./jetbackup-function.md) -APIs generiert werden.</span><span class="sxs-lookup"><span data-stu-id="659a8-119">The backup should have been generated using the [JetBackup](./jetbackup-function.md) APIs.</span></span>

<span data-ttu-id="659a8-120">*szdest*</span><span class="sxs-lookup"><span data-stu-id="659a8-120">*szDest*</span></span>

<span data-ttu-id="659a8-121">Der Name des Ordners, in den die Datenbankdateien aus dem Sicherungs Satz kopiert und wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="659a8-121">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="659a8-122">Wenn dies auf NULL festgelegt ist (Dies ist der Fall für den Legacy- [jetrestore](./jetrestore-function.md)), werden die Datenbankdateien kopiert und an Ihrem ursprünglichen Speicherort wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="659a8-122">If this is set to NULL (which is the case for the legacy [JetRestore](./jetrestore-function.md)), the database files will be copied and recovered to their original location.</span></span>

<span data-ttu-id="659a8-123">*PFN*</span><span class="sxs-lookup"><span data-stu-id="659a8-123">*pfn*</span></span>

<span data-ttu-id="659a8-124">Der optionale Zeiger auf die Funktion, die als Benachrichtigungs Informationen zum Fortschritt des Wiederherstellungs Vorgangs aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="659a8-124">The optional pointer to the function which will be called as notification information about the progress of the restore operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="659a8-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="659a8-125">Return Value</span></span>

<span data-ttu-id="659a8-126">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="659a8-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="659a8-127">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="659a8-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="659a8-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="659a8-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="659a8-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="659a8-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="659a8-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="659a8-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="659a8-131">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="659a8-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="659a8-132">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="659a8-132">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="659a8-133">Der Vorgang ist fehlgeschlagen, da die Engine für diese Instanz bereits initialisiert ist.</span><span class="sxs-lookup"><span data-stu-id="659a8-133">The operation failed because the engine is already initialized for this instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="659a8-134">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="659a8-134">JET_errInvalidLogSequence</span></span></p></td>
<td><p><span data-ttu-id="659a8-135">Der Satz von Protokolldateien aus dem Sicherungs Satz und aus dem aktuellen Protokoll Pfad stimmt nicht mit dem Satz der Protokolldateien identisch.</span><span class="sxs-lookup"><span data-stu-id="659a8-135">The set of log files from the backup set and from the current log path do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="659a8-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="659a8-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="659a8-137">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="659a8-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="659a8-138">Dieser Fehler wird von <strong>jetrestoreinstance</strong> zurückgegeben, wenn sich die Engine im multiinstanzmodus befindet und pinstance auf eine ungültige Instanz von Windows XP und höheren Versionen verweist.</span><span class="sxs-lookup"><span data-stu-id="659a8-138">This error will be returned by <strong>JetRestoreInstance</strong> when the engine is in multi-instance mode and pinstance refers to an invalid instance Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="659a8-139">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="659a8-139">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="659a8-140">Der Vorgang ist fehlgeschlagen, weil einige der angegebenen Pfade ungültig sind (der Sicherungs Pfad, der Zielpfad, der Protokoll-oder Systempfad für die Instanz).</span><span class="sxs-lookup"><span data-stu-id="659a8-140">The operation failed because some of paths provided are invalid (the backup path, the destination path, the log or system path for the instance).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="659a8-141">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="659a8-141">JET_errPageSizeMismatch</span></span></p></td>
<td><p><span data-ttu-id="659a8-142">Der Vorgang ist fehlgeschlagen, da die Engine für die Verwendung einer Datenbankseiten Größe (mit <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> für <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) konfiguriert ist, die nicht mit der Datenbankseiten Größe identisch ist, die zum Erstellen der Transaktionsprotokoll Dateien oder der Datenbanken verwendet wird, die den Transaktionsprotokoll Dateien zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="659a8-142">The operation failed because the engine is configured to use a database page size (using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) that does not match the database page size used to create the transaction log files or the databases associated with the transaction log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="659a8-143">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="659a8-143">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="659a8-144">Der Vorgang ist fehlgeschlagen, weil die Parameter den einzelinstanzmodus (Windows 2000-Kompatibilitätsmodus) impliziert haben und sich die Engine bereits im Modus für mehrere Instanzen befindet.</span><span class="sxs-lookup"><span data-stu-id="659a8-144">The operation failed because the parameters implied single instance mode (Windows 2000 compatibility mode) and the engine is already in multi-instance mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="659a8-145">Bei Erfolg werden Datenbankdateien aus dem Sicherungs Satz an ihrem Speicherort wieder hergestellt, und die Wiederherstellung wird ausgeführt, sodass sich die Datenbanken in einem sauberen Transaktions Konsistenz Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="659a8-145">On success, database files from the backup set will be restored over to their location and recovery will be run such that the databases will be in a clean transactional consistency state.</span></span> <span data-ttu-id="659a8-146">Bei der Wiederherstellung werden die Protokolldateien aus dem Sicherungs Satz und die Protokolldateien aus dem Protokoll Pfad wiedergegeben, wenn solche Dateien vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="659a8-146">Recovery will replay the log files from the backup set and the log files from the log path if such files do exists.</span></span> <span data-ttu-id="659a8-147">Diese Wiederherstellung führt zu Änderungen an der Prüf Punkt Datei, den Transaktionsprotokoll Dateien und allen Datenbanken, auf die von diesen Transaktionsprotokoll Dateien verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="659a8-147">This recovery will result in changes to the checkpoint file, the transaction log files, and any databases referenced by those transaction log files.</span></span>

<span data-ttu-id="659a8-148">Bei einem Fehler verbleibt die Instanz in einem nicht initialisierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="659a8-148">On failure, the instance remains in an uninitialized state.</span></span> <span data-ttu-id="659a8-149">Der Status der Transaktionsprotokoll Dateien und sämtlicher Datenbanken, auf die von diesen Transaktionsprotokoll Dateien verwiesen wird, wurde bei dem Versuch, die Wiederherstellung zu initialisieren und die Datenbanken wiederherzustellen, wahrscheinlich geändert.</span><span class="sxs-lookup"><span data-stu-id="659a8-149">The state of the transaction log files and any databases referenced by those transaction log files will likely have been changed in the attempt to initialize the restore and recover the databases.</span></span>

#### <a name="remarks"></a><span data-ttu-id="659a8-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="659a8-150">Remarks</span></span>

<span data-ttu-id="659a8-151">Beim Wiederherstellungs Vorgang werden die Datenbanken, die während der Sicherung an die Instanz angefügt sind, rekonstruiert und die Änderungen in den Datenbankdateien wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="659a8-151">The recovery process will reconstruct the databases attached to the instance during the backup and save the changes back to the database files.</span></span> <span data-ttu-id="659a8-152">Das Ergebnis sind Datenbanken, die Transaktions konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="659a8-152">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="659a8-153">Wenn möglich, werden die Änderungen, die seit der Sicherung vorgenommen wurden, auch in der Datenbank gespeichert, bis die letzte Änderung in den Transaktions Protokollen gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="659a8-153">If possible, it will also save to the database the changes done since the backup was taken until the most recent change found in the transaction logs.</span></span> <span data-ttu-id="659a8-154">Dies wäre möglich, wenn die seit der Sicherung generierten Transaktionsprotokolle weiterhin im Transaktionsprotokoll Verzeichnis vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="659a8-154">This would be possible if the transaction logs generated since the backup was taken are still present in the transaction log directory.</span></span> <span data-ttu-id="659a8-155">Beachten Sie Folgendes: Wenn die zirkuläre Protokollierung für die Instanz aktiviert wurde, werden die generierten Transaktionsprotokolle so wieder verwendet, dass die Wiederherstellung die Änderungen speichern kann, die bis zum Sicherungs Zeitpunkt stattfinden.</span><span class="sxs-lookup"><span data-stu-id="659a8-155">Note that if circular logging was enabled for the instance, the transaction logs generated are reused such that the recovery will be able to save the changes which took place up to the backup moment.</span></span> <span data-ttu-id="659a8-156">In jedem Fall ist es möglich, dass dieser Vorgang sehr viel Zeit in Anspruch nimmt, wenn die Anzahl der Transaktionsprotokoll Dateien, die für die Datenbanken wiedergegeben werden sollen, groß ist.</span><span class="sxs-lookup"><span data-stu-id="659a8-156">In any case, it is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="659a8-157">**Jetrestoreinstance** muss für eine Instanz aufgerufen werden, die bereits mit [jetkreateinstance](./jetcreateinstance-function.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="659a8-157">**JetRestoreInstance** must be called on an instance which was already created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

<span data-ttu-id="659a8-158">Da bei der Wiederherstellung eine beträchtliche Anzahl von Datenbankseiten und Transaktions Protokollen verwendet wird, gibt es eine ganze Reihe von Fehlern, die von diesen Funktionen zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="659a8-158">Because during recovery a significant number of database pages and transaction logs will be used, there is an entire series of error which might be returned by these functions.</span></span> <span data-ttu-id="659a8-159">Solche Fehler können aus temporären Ressourcen Zuordnungs Fehlern wie JET_errOutOfMemory zu Fehlern bestehen, die physische Beschädigungen wie JET_errReadVerifyFailure, JET_errLogFileCorrupt oder JET_errBadPageLink darstellen.</span><span class="sxs-lookup"><span data-stu-id="659a8-159">Such errors can be from temporary resource allocation failures like Jet_errOutOfMemory to errors representing physical corruptions like JET_errReadVerifyFailure, JET_errLogFileCorrupt or JET_errBadPageLink.</span></span> <span data-ttu-id="659a8-160">Diese Fehler werden fast immer durch Hardwareprobleme verursacht und können daher nicht vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="659a8-160">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="659a8-161">Die Datei Misswirtschaft wird am häufigsten als JET_errMissingLogFile oder JET_errAttachedDatabaseMismatch oder JET_errDatabaseSharingViolation oder JET_errInvalidLogSequence Manifest.</span><span class="sxs-lookup"><span data-stu-id="659a8-161">File mismanagement will manifest itself most often as JET_errMissingLogFile or JET_errAttachedDatabaseMismatch or JET_errDatabaseSharingViolation or JET_errInvalidLogSequence.</span></span> <span data-ttu-id="659a8-162">Diese Fehler können von der Anwendung verhindert werden.</span><span class="sxs-lookup"><span data-stu-id="659a8-162">These errors are preventable by the application.</span></span> <span data-ttu-id="659a8-163">Die Anwendung muss darauf achten, das Repository dieser Dateien vor der Bearbeitung durch externe Kräfte wie z. b. den Benutzer oder andere Anwendungen zu schützen.</span><span class="sxs-lookup"><span data-stu-id="659a8-163">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="659a8-164">Wenn die Anwendung eine Instanz vollständig zerstören möchte, müssen alle Dateien, die der Instanz zugeordnet sind, gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="659a8-164">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="659a8-165">Hierzu gehören die Prüf Punkt Datei, die Transaktionsprotokoll Dateien und alle Datenbankdateien, die an die Instanz angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="659a8-165">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="659a8-166">In den verschiedenen Schritten der Wiederherstellung werden Ereignisprotokoll Einträge generiert, einschließlich des Status der Wiedergabe des Transaktions Protokolls und des Endergebnis der Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="659a8-166">The different steps of the recovery will have Event Log entries generated including the transaction log replay progress and the final result of the restore.</span></span>

#### <a name="requirements"></a><span data-ttu-id="659a8-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="659a8-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="659a8-168"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="659a8-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="659a8-169">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="659a8-169">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="659a8-170"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="659a8-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="659a8-171">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="659a8-171">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="659a8-172"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="659a8-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="659a8-173">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="659a8-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="659a8-174"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="659a8-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="659a8-175">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="659a8-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="659a8-176"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="659a8-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="659a8-177">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="659a8-177">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="659a8-178"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="659a8-178"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="659a8-179">Implementiert als <strong>jetrestoreingestancew</strong> (Unicode) und <strong>jetrestoreingestancea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="659a8-179">Implemented as <strong>JetRestoreInstanceW</strong> (Unicode) and <strong>JetRestoreInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="659a8-180">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="659a8-180">See Also</span></span>

[<span data-ttu-id="659a8-181">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="659a8-181">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="659a8-182">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="659a8-182">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="659a8-183">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="659a8-183">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="659a8-184">JetBackup</span><span class="sxs-lookup"><span data-stu-id="659a8-184">JetBackup</span></span>](./jetbackup-function.md)  
[<span data-ttu-id="659a8-185">Jetbackupinstance</span><span class="sxs-lookup"><span data-stu-id="659a8-185">JetBackupInstance</span></span>](./jetbackupinstance-function.md)  
[<span data-ttu-id="659a8-186">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="659a8-186">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="659a8-187">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="659a8-187">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
