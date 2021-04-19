---
description: 'Weitere Informationen zu: jetopenfile-Funktion'
title: JetOpenFile-Funktion
TOCTitle: JetOpenFile Function
ms:assetid: 52f69050-ca1c-4a6b-a188-22bd7cb96bf5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269249(v=EXCHG.10)
ms:contentKeyID: 32765551
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileW
- JetOpenFile
- JetOpenFileA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2996ffc46e2f6b37cdfec12cd4ee2fc62efa188a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343222"
---
# <a name="jetopenfile-function"></a><span data-ttu-id="6ed9b-103">JetOpenFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="6ed9b-103">JetOpenFile Function</span></span>


<span data-ttu-id="6ed9b-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6ed9b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopenfile-function"></a><span data-ttu-id="6ed9b-105">JetOpenFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="6ed9b-105">JetOpenFile Function</span></span>

<span data-ttu-id="6ed9b-106">Die **jetopenfile** -Funktion öffnet eine angefügte Datenbank, datenbankpatchdatei oder Transaktionsprotokoll Datei einer aktiven Instanz zum Ausführen einer Streaming-Fuzzy-Sicherung.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-106">The **JetOpenFile** function opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="6ed9b-107">Die Daten aus diesen Dateien können anschließend mithilfe von [jetreadfile](./jetreadfile-function.md)über das zurückgegebene Handle gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-107">The data from these files can subsequently be read through the returned handle using [JetReadFile](./jetreadfile-function.md).</span></span> <span data-ttu-id="6ed9b-108">Das zurückgegebene Handle muss mithilfe von [jetclosefile](./jetclosefile-function.md)geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-108">The returned handle must be closed using [JetCloseFile](./jetclosefile-function.md).</span></span> <span data-ttu-id="6ed9b-109">Eine externe Sicherung der-Instanz muss zuvor mithilfe von [jetbeginexternalbackup](./jetbeginexternalbackup-function.md)initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-109">An external backup of the instance must have been previously initiated using [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

```cpp
    JET_ERR JET_API JetOpenFile(
      __in          const tchar* szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a><span data-ttu-id="6ed9b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ed9b-110">Parameters</span></span>

<span data-ttu-id="6ed9b-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="6ed9b-111">*szFileName*</span></span>

<span data-ttu-id="6ed9b-112">Der relative oder absolute Pfad zu einer angefügten Datenbank, datenbankpatchdatei oder Transaktionsprotokoll Datei, die von der-Instanz verwaltet wird und für die Sicherung gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-112">The relative or absolute path to an attached database, database patch file, or transaction log file managed by the instance that will be read for backup.</span></span>

<span data-ttu-id="6ed9b-113">*phffile*</span><span class="sxs-lookup"><span data-stu-id="6ed9b-113">*phfFile*</span></span>

<span data-ttu-id="6ed9b-114">Der Ausgabepuffer, der ein Handle für die zu lesende Datei empfängt.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-114">The output buffer that receives a handle to the file to be read.</span></span>

<span data-ttu-id="6ed9b-115">*pulfilesizelow*</span><span class="sxs-lookup"><span data-stu-id="6ed9b-115">*pulFileSizeLow*</span></span>

<span data-ttu-id="6ed9b-116">Der Ausgabepuffer, der die wenigsten signifikanten 32 Bits der Dateigröße empfängt.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-116">The output buffer that receives the least significant 32 bits of the size of the file.</span></span>

<span data-ttu-id="6ed9b-117">*pulfilesizehigh*</span><span class="sxs-lookup"><span data-stu-id="6ed9b-117">*pulFileSizeHigh*</span></span>

<span data-ttu-id="6ed9b-118">Der Ausgabepuffer, der die signifi32 kantesten Bits der Größe der Datei empfängt.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-118">The output buffer that receives the most significant 32 bits of the size of the file.</span></span>

### <a name="return-value"></a><span data-ttu-id="6ed9b-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ed9b-119">Return Value</span></span>

<span data-ttu-id="6ed9b-120">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6ed9b-121">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6ed9b-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6ed9b-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6ed9b-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="6ed9b-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ed9b-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ed9b-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6ed9b-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6ed9b-125">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed9b-126">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="6ed9b-126">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="6ed9b-127">Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen <a href="gg294067(v=exchg.10).md">jetstopbackup</a>-Befehl abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-127">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="6ed9b-128">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-128">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed9b-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="6ed9b-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="6ed9b-130">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-130">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed9b-131">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="6ed9b-131">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="6ed9b-132">Der Vorgang ist fehlgeschlagen, da die angeforderte Datei aufgrund einer Freigabe Verletzung oder unzureichender Berechtigungen nicht geöffnet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-132">The operation failed because it could not open the requested file due to a sharing violation or insufficient privileges.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed9b-133">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="6ed9b-133">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="6ed9b-134">Der Vorgang ist fehlgeschlagen, da die angeforderte Datei nicht geöffnet werden konnte, da Sie im angegebenen Pfad nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-134">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span> <span data-ttu-id="6ed9b-135">Dieser Fehler wird nur von Windows 2000 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-135">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed9b-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="6ed9b-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="6ed9b-137">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="6ed9b-138">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed9b-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="6ed9b-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="6ed9b-140">Der Sicherungs Vorgang ist fehlgeschlagen, da er außerhalb der Reihenfolge aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-140">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed9b-141">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="6ed9b-141">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="6ed9b-142">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-142">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="6ed9b-143">Dies kann bei <strong>jetopatfile</strong> vorkommen, wenn Folgendes geschieht:</span><span class="sxs-lookup"><span data-stu-id="6ed9b-143">This can happen for <strong>JetOpenFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="6ed9b-144">Das angegebene Instanzhandle ist ungültig (Windows XP und spätere Releases).</span><span class="sxs-lookup"><span data-stu-id="6ed9b-144">The specified instance handle is invalid (Windows XP and later releases).</span></span></p></li>
<li><p><span data-ttu-id="6ed9b-145">Der angegebene filename-Parameter ist NULL oder eine Zeichenfolge der Länge 0 (null) (Windows XP und spätere Releases).</span><span class="sxs-lookup"><span data-stu-id="6ed9b-145">The specified filename parameter is NULL or a zero length string (Windows XP and later releases).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed9b-146">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="6ed9b-146">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="6ed9b-147">Der Vorgang ist fehlgeschlagen, da der angegebene Pfad nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-147">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed9b-148">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="6ed9b-148">JET_errMissingFileToBackup</span></span></p></td>
<td><p><span data-ttu-id="6ed9b-149">Die angeforderte Datei konnte nicht für die Sicherung geöffnet werden, da Sie nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-149">The requested file could not be opened for backup because it could not be found.</span></span> <span data-ttu-id="6ed9b-150">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed9b-151">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="6ed9b-151">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="6ed9b-152">Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-152">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed9b-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="6ed9b-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="6ed9b-154">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed9b-155">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="6ed9b-155">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="6ed9b-156">Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-156">The operation failed because not enough memory could be allocated to complete it.</span></span> <span data-ttu-id="6ed9b-157"><strong>Jetopenfile</strong> gibt JET_errOutOfMemory zurück, wenn versucht wird, eine andere Datei zu öffnen, bevor die vorherige Datei, die mit <strong>jetopenfile</strong> geöffnet wurde, von <a href="gg294127(v=exchg.10).md">jetclosefile</a>geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-157"><strong>JetOpenFile</strong> will return JET_errOutOfMemory if an attempt is made to open another file before the previous file opened using <strong>JetOpenFile</strong> has been closed by <a href="gg294127(v=exchg.10).md">JetCloseFile</a>.</span></span> <span data-ttu-id="6ed9b-158">Zurzeit wird nur ein ausstehendes Datei Handle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-158">Only one outstanding file handle is currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed9b-159">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="6ed9b-159">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="6ed9b-160">Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-160">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed9b-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="6ed9b-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="6ed9b-162">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span> <span data-ttu-id="6ed9b-163">JET_errRestoreInProgress der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-163">JET_errRestoreInProgress It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6ed9b-164">Bei Erfolg wird ein Handle für die angeforderte Datei zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-164">On success, a handle to the requested file will be returned.</span></span> <span data-ttu-id="6ed9b-165">Wenn das Handle für eine Datenbankdatei vorgesehen ist, wird diese Datenbankdatei für die Streamingsicherung vorbereitet. Dies kann dazu führen, dass eine datenbankpatchdatei am gleichen Speicherort wie die Datenbankdatei erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-165">If the handle is for a database file, that database file will be prepared for streaming backup which may result in the creation of a database patch file in the same location as the database file.</span></span> <span data-ttu-id="6ed9b-166">Die Datenbank-Patchdatei weist genau denselben Pfad und Dateinamen wie die Datenbankdatei auf, verfügt aber über eine. Pat-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-166">The database patch file has the exact same path and filename as the database file, but has a .PAT extension.</span></span> <span data-ttu-id="6ed9b-167">Die Größe der Datei wird ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-167">The size of the file will also be returned.</span></span>

<span data-ttu-id="6ed9b-168">Bei einem Fehler wird der Status der Ausgabepuffer nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-168">On failure, the state of the output buffers will be undefined.</span></span> <span data-ttu-id="6ed9b-169">Eine Datenbank-Patchdatei wird möglicherweise temporär auf dem Datenträger erstellt, und alle vorhandenen Dateien am Speicherort der Patchdatei können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-169">A database patch file may be temporarily created on disk and any existing file at the patch file location may be deleted.</span></span> <span data-ttu-id="6ed9b-170">Der Fehler führt dazu, dass der gesamte Sicherungsprozess für die Instanz abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-170">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="6ed9b-171">Unter Windows XP und höheren Versionen wird die Sicherung nicht abgebrochen, wenn versucht wurde, eine Datenbank zu sichern, die zum Zeitpunkt des Aufrufens nicht an die Instanz angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-171">On Windows XP and later releases, the backup will not be canceled if an attempt was made to backup a database that was not attached to the instance at the time of the call.</span></span>

<span data-ttu-id="6ed9b-172">**Warnung**  Aus Sicherheitsgründen ist es wichtig zu beachten, dass **jetopenfile** nicht überprüft, ob der angeforderte Dateipfad mit dem Satz von Dateien verknüpft ist, die für die Instanz gesichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-172">**Warning**  For security reasons, it is important to note that **JetOpenFile** does not verify that the requested file path is associated with the set of files that should be backed up for the instance.</span></span> <span data-ttu-id="6ed9b-173">Daher ist es möglich, diese Funktion für den Zugriff auf eine beliebige Datei zu verwenden, die durch den aktuellen Sicherheitskontext des Threads geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-173">As a result, it is possible to use this function to access any file that can be opened by the current security context of the thread.</span></span> <span data-ttu-id="6ed9b-174">Es ist zwingend erforderlich, dass die Anwendung die an diese Funktion weiter gegebenen Pfade an einen bekannten Satz von guten Dateipfaden einschränkt oder eine Offenlegung von Informations Angriffen möglich wäre.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-174">It is imperative that the application restrict the paths passed to this function to a known set of good file paths or a disclosure of information attack could be made possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="6ed9b-175">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ed9b-175">Remarks</span></span>

<span data-ttu-id="6ed9b-176">Die Ausgabepuffer für die Handle-und Dateigröße müssen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-176">The handle and file size output buffers are required to be present.</span></span> <span data-ttu-id="6ed9b-177">Wenn Sie nicht vorhanden sind, stürzt die Engine ab, da die Ausgabepuffer Parameter nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-177">If they are not present then the engine will crash because the output buffer parameters are not validated.</span></span>

<span data-ttu-id="6ed9b-178">Zurzeit kann jeweils nur eine Datei für die Sicherung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-178">At this time, only one file can be open for backup at any one time.</span></span>

<span data-ttu-id="6ed9b-179">**Jetopenfile** bestätigt die Sicherungs Berechtigung nicht vor dem Öffnen der angeforderten Datei.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-179">**JetOpenFile** does not assert the backup privilege prior to opening the requested file.</span></span>

<span data-ttu-id="6ed9b-180">Die Größe der zu lesenden Datei, wie von dieser Funktion gemeldet, stimmt möglicherweise nicht mit der Größe der Datei auf dem Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-180">The size of the file to be read as reported by this function may not match the size of the file on disk.</span></span> <span data-ttu-id="6ed9b-181">Unter Windows XP und höheren Versionen können zusätzliche Informationen an eine Datenbankdatei angehängt werden, die während eines Wiederherstellungs Vorgangs von der Datenbank-Engine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-181">On Windows XP and later releases, extra information may be appended to a database file which is used by the database engine during a restore operation.</span></span> <span data-ttu-id="6ed9b-182">Daher sollte die Anwendung nur die von **jetopenfile** zurückgegebene Dateigröße oder die tatsächliche Anzahl von Daten bytes, die von [jetreadfile](./jetreadfile-function.md)zurückgegeben werden, verlassen.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-182">As such, the application should only rely on the file size returned by **JetOpenFile** or on the actual number of bytes of data returned by [JetReadFile](./jetreadfile-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="6ed9b-183">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ed9b-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ed9b-184"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6ed9b-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed9b-185">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed9b-186"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6ed9b-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed9b-187">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed9b-188"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="6ed9b-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed9b-189">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed9b-190"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="6ed9b-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed9b-191">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ed9b-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6ed9b-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed9b-193">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed9b-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="6ed9b-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6ed9b-195">Implementiert als <strong>jetopenfilew</strong> (Unicode) und <strong>jetopenfilea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="6ed9b-195">Implemented as <strong>JetOpenFileW</strong> (Unicode) and <strong>JetOpenFileA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6ed9b-196">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6ed9b-196">See Also</span></span>

[<span data-ttu-id="6ed9b-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6ed9b-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6ed9b-198">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="6ed9b-198">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="6ed9b-199">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="6ed9b-199">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="6ed9b-200">Jetattachdatabase</span><span class="sxs-lookup"><span data-stu-id="6ed9b-200">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="6ed9b-201">Jetbeginexternalbackup</span><span class="sxs-lookup"><span data-stu-id="6ed9b-201">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="6ed9b-202">Jetclosefile</span><span class="sxs-lookup"><span data-stu-id="6ed9b-202">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="6ed9b-203">Jetgetattachinfo</span><span class="sxs-lookup"><span data-stu-id="6ed9b-203">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="6ed9b-204">Jetgetloginfo</span><span class="sxs-lookup"><span data-stu-id="6ed9b-204">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="6ed9b-205">Jetreadfile</span><span class="sxs-lookup"><span data-stu-id="6ed9b-205">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="6ed9b-206">Jetstopbackup</span><span class="sxs-lookup"><span data-stu-id="6ed9b-206">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="6ed9b-207">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="6ed9b-207">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="6ed9b-208">Jettruneurelog</span><span class="sxs-lookup"><span data-stu-id="6ed9b-208">JetTruncateLog</span></span>](./jettruncatelog-function.md)
