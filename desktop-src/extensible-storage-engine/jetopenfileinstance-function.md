---
description: 'Weitere Informationen zu: jetopenfileinstance-Funktion'
title: JetOpenFileInstance-Funktion
TOCTitle: JetOpenFileInstance Function
ms:assetid: 44af9549-77ef-48f4-8580-507f7199f281
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269238(v=EXCHG.10)
ms:contentKeyID: 32765540
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileInstanceA
- JetOpenFileInstanceW
- JetOpenFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6065914fcd5b03d8c8b05996d57331a474ad7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350983"
---
# <a name="jetopenfileinstance-function"></a><span data-ttu-id="cbf67-103">JetOpenFileInstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="cbf67-103">JetOpenFileInstance Function</span></span>


<span data-ttu-id="cbf67-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cbf67-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopenfileinstance-function"></a><span data-ttu-id="cbf67-105">JetOpenFileInstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="cbf67-105">JetOpenFileInstance Function</span></span>

<span data-ttu-id="cbf67-106">Die **jetopenfileinstance** -Funktion öffnet eine angefügte Datenbank, datenbankpatchdatei oder Transaktionsprotokoll Datei einer aktiven Instanz zum Ausführen einer Streaming-Fuzzy-Sicherung.</span><span class="sxs-lookup"><span data-stu-id="cbf67-106">The **JetOpenFileInstance** function opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="cbf67-107">Die Daten aus diesen Dateien können anschließend mithilfe von [jetreadfileinstance](./jetreadfileinstance-function.md)durch das zurückgegebene Handle gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="cbf67-107">The data from these files can subsequently be read through the returned handle using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span> <span data-ttu-id="cbf67-108">Das zurückgegebene Handle muss mithilfe von [jetclosefilinput Stance](./jetclosefileinstance-function.md)geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="cbf67-108">The returned handle must be closed using [JetCloseFileInstance](./jetclosefileinstance-function.md).</span></span> <span data-ttu-id="cbf67-109">Eine externe Sicherung der Instanz muss mithilfe von [jetbeginexternalbackupinstance](./jetbeginexternalbackupinstance-function.md)initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="cbf67-109">An external backup of the instance must have been previously initiated using [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md).</span></span>

<span data-ttu-id="cbf67-110">**Windows XP:**  **jetoperfileinstance** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="cbf67-110">**Windows XP:**  **JetOpenFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOpenFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a><span data-ttu-id="cbf67-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cbf67-111">Parameters</span></span>

<span data-ttu-id="cbf67-112">*lichen*</span><span class="sxs-lookup"><span data-stu-id="cbf67-112">*instance*</span></span>

<span data-ttu-id="cbf67-113">Die-Instanz, die für diesen Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbf67-113">The instance to use for this call.</span></span>

<span data-ttu-id="cbf67-114">Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="cbf67-114">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="cbf67-115">In diesem Fall wird die Verwendung dieser globalen Instanz impliziert.</span><span class="sxs-lookup"><span data-stu-id="cbf67-115">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="cbf67-116">Für Windows XP und spätere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) befindet, in dem nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="cbf67-116">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="cbf67-117">Andernfalls schlägt der Vorgang mit JET_errRunningInMultiInstanceMode fehl.</span><span class="sxs-lookup"><span data-stu-id="cbf67-117">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="cbf67-118">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="cbf67-118">*szFileName*</span></span>

<span data-ttu-id="cbf67-119">Der relative oder absolute Pfad zu einer angefügten Datenbank, datenbankpatchdatei oder Transaktionsprotokoll Datei, die von der-Instanz verwaltet wird, die für die Sicherung gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="cbf67-119">The relative or absolute path to an attached database, database patch file, or transaction log file managed by the instance that is read for backup.</span></span>

<span data-ttu-id="cbf67-120">*phffile*</span><span class="sxs-lookup"><span data-stu-id="cbf67-120">*phfFile*</span></span>

<span data-ttu-id="cbf67-121">Ein Zeiger auf den Ausgabepuffer, der ein Handle für die zu lesende Datei empfängt.</span><span class="sxs-lookup"><span data-stu-id="cbf67-121">Pointer to the output buffer that receives a handle to the file to be read.</span></span>

<span data-ttu-id="cbf67-122">*pulfilesizelow*</span><span class="sxs-lookup"><span data-stu-id="cbf67-122">*pulFileSizeLow*</span></span>

<span data-ttu-id="cbf67-123">Ein Zeiger auf den Ausgabepuffer, der die wenigsten signifikanten 32 Bits der Größe der Datei empfängt.</span><span class="sxs-lookup"><span data-stu-id="cbf67-123">Pointer to the output buffer that receives the least significant 32 bits of the size of the file.</span></span>

<span data-ttu-id="cbf67-124">*pulfilesizehigh*</span><span class="sxs-lookup"><span data-stu-id="cbf67-124">*pulFileSizeHigh*</span></span>

<span data-ttu-id="cbf67-125">Ein Zeiger auf den Ausgabepuffer, der die signifi32 kantesten Bits der Größe der Datei empfängt.</span><span class="sxs-lookup"><span data-stu-id="cbf67-125">Pointer to the output buffer that receives the most significant 32 bits of the size of the file.</span></span>

### <a name="return-value"></a><span data-ttu-id="cbf67-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cbf67-126">Return Value</span></span>

<span data-ttu-id="cbf67-127">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="cbf67-127">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="cbf67-128">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cbf67-128">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cbf67-129">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cbf67-129">Return code</span></span></p></th>
<th><p><span data-ttu-id="cbf67-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbf67-130">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cbf67-131">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="cbf67-131">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="cbf67-132">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cbf67-132">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbf67-133">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="cbf67-133">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="cbf67-134">Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen Befehl von <a href="gg269309(v=exchg.10).md">jetstopbackupinstance</a>abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="cbf67-134">The operation failed because the current external backup has been aborted by a call to <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span></span> <span data-ttu-id="cbf67-135">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cbf67-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbf67-136">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="cbf67-136">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="cbf67-137">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg294108(v=exchg.10).md">jetstopserviceinstance</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="cbf67-137">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbf67-138">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="cbf67-138">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="cbf67-139">Der Vorgang ist fehlgeschlagen, da die angeforderte Datei aufgrund einer Freigabe Verletzung oder unzureichender Berechtigungen nicht geöffnet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="cbf67-139">The operation failed because it could not open the requested file due to a sharing violation or insufficient privileges.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbf67-140">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="cbf67-140">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="cbf67-141">Der Vorgang ist fehlgeschlagen, da die angeforderte Datei nicht geöffnet werden konnte, da Sie im angegebenen Pfad nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="cbf67-141">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span> <span data-ttu-id="cbf67-142">Dieser Fehler wird nur von Windows 2000 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cbf67-142">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbf67-143">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="cbf67-143">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="cbf67-144">Der Sicherungs Vorgang ist fehlgeschlagen, da er außerhalb der Reihenfolge aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="cbf67-144">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbf67-145">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="cbf67-145">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="cbf67-146">Der Vorgang ist fehlgeschlagen, da der angegebene Pfad nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="cbf67-146">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbf67-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="cbf67-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="cbf67-148">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="cbf67-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="cbf67-149">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cbf67-149">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbf67-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="cbf67-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="cbf67-151">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="cbf67-151">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="cbf67-152">Dies kann bei <strong>jetopin fileinstance</strong> vorkommen, wenn Folgendes geschieht:</span><span class="sxs-lookup"><span data-stu-id="cbf67-152">This can happen for <strong>JetOpenFileInstance</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="cbf67-153">Das angegebene Instanzhandle ist ungültig (Windows XP und spätere Releases).</span><span class="sxs-lookup"><span data-stu-id="cbf67-153">The specified instance handle is invalid (Windows XP and later releases).</span></span></p></li>
<li><p><span data-ttu-id="cbf67-154">Der angegebene filename-Parameter ist NULL oder eine Zeichenfolge der Länge 0 (null) (Windows XP und spätere Releases).</span><span class="sxs-lookup"><span data-stu-id="cbf67-154">The specified filename parameter is NULL or a zero length string (Windows XP and later releases).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbf67-155">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="cbf67-155">JET_errMissingFileToBackup</span></span></p></td>
<td><p><span data-ttu-id="cbf67-156">Die angeforderte Datei konnte nicht für die Sicherung geöffnet werden, da Sie nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="cbf67-156">The requested file could not be opened for backup because it could not be found.</span></span> <span data-ttu-id="cbf67-157">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cbf67-157">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbf67-158">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="cbf67-158">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="cbf67-159">Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cbf67-159">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbf67-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="cbf67-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="cbf67-161">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="cbf67-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbf67-162">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="cbf67-162">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="cbf67-163">Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="cbf67-163">The operation failed because not enough memory could be allocated to complete it.</span></span> <span data-ttu-id="cbf67-164"><strong>Jetopenfileinstance</strong> gibt JET_errOutOfMemory zurück, wenn versucht wird, eine andere Datei zu öffnen, bevor die vorherige Datei, die mit <strong>jetopenfileinstance</strong> geöffnet wurde, von <a href="gg269270(v=exchg.10).md">jetclosefileinstance</a>geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="cbf67-164"><strong>JetOpenFileInstance</strong> will return JET_errOutOfMemory if an attempt is made to open another file before the previous file opened using <strong>JetOpenFileInstance</strong> has been closed by <a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>.</span></span> <span data-ttu-id="cbf67-165">Zurzeit wird nur ein ausstehendes Datei Handle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cbf67-165">Only one outstanding file handle is currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbf67-166">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="cbf67-166">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="cbf67-167">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cbf67-167">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbf67-168">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="cbf67-168">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="cbf67-169">Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="cbf67-169">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbf67-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="cbf67-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="cbf67-171">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="cbf67-171">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cbf67-172">Bei Erfolg wird ein Handle für die angeforderte Datei zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cbf67-172">On success, a handle to the requested file is returned.</span></span> <span data-ttu-id="cbf67-173">Wenn das Handle für eine Datenbankdatei vorgesehen ist, wird die Datenbankdatei auf eine Streamingsicherung vorbereitet. Dies kann dazu führen, dass eine datenbankpatchdatei am gleichen Speicherort wie die Datenbankdatei erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="cbf67-173">If the handle is for a database file, that database file will be prepared for a streaming backup which may result in the creation of a database patch file in the same location as the database file.</span></span> <span data-ttu-id="cbf67-174">Die Datenbank-Patchdatei hat genau denselben Pfad und Dateinamen wie die Datenbankdatei, aber mit einem. Pat-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="cbf67-174">The database patch file has the exact same path and filename as the database file but with a .PAT extension.</span></span> <span data-ttu-id="cbf67-175">Die Größe der Datei wird ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cbf67-175">The size of the file will also be returned.</span></span>

<span data-ttu-id="cbf67-176">Bei einem Fehler wird der Status der Ausgabepuffer nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="cbf67-176">On failure, the state of the output buffers will be undefined.</span></span> <span data-ttu-id="cbf67-177">Eine Datenbank-Patchdatei wird möglicherweise temporär auf dem Datenträger erstellt, und alle vorhandenen Dateien am Speicherort der Patchdatei können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="cbf67-177">A database patch file may be temporarily created on disk and any existing file at the patch file location may be deleted.</span></span> <span data-ttu-id="cbf67-178">Der Fehler führt dazu, dass der gesamte Sicherungsprozess für die Instanz abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="cbf67-178">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="cbf67-179">Unter Windows XP und höheren Versionen wird die Sicherung nicht abgebrochen, wenn versucht wurde, eine Datenbank zu sichern, die zum Zeitpunkt des Aufrufens nicht an die Instanz angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="cbf67-179">On Windows XP and later releases, the backup will not be canceled if an attempt was made to backup a database that was not attached to the instance at the time of the call.</span></span>

<span data-ttu-id="cbf67-180">**Warnung**  Aus Sicherheitsgründen ist es wichtig zu beachten, dass **jetopenfileinstance** nicht überprüft, ob der angeforderte Dateipfad mit dem Satz von Dateien verknüpft ist, die für die Instanz gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="cbf67-180">**Warning**  For security reasons, it is important to note that **JetOpenFileInstance** does not verify that the requested file path is associated with the set of files that are backed up for the instance.</span></span> <span data-ttu-id="cbf67-181">Daher ist es möglich, diese Funktion für den Zugriff auf eine beliebige Datei zu verwenden, die durch den aktuellen Sicherheitskontext des Threads geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="cbf67-181">As a result, it is possible to use this function to access any file that can be opened by the current security context of the thread.</span></span> <span data-ttu-id="cbf67-182">Es ist zwingend erforderlich, dass die Anwendung die an diese Funktion weiter gegebenen Pfade an einen bekannten Satz von guten Dateipfaden einschränkt oder eine Offenlegung von Informations Angriffen möglich wäre.</span><span class="sxs-lookup"><span data-stu-id="cbf67-182">It is imperative that the application restrict the paths passed to this function to a known set of good file paths or a disclosure of information attack could be made possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cbf67-183">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbf67-183">Remarks</span></span>

<span data-ttu-id="cbf67-184">Die Ausgabepuffer für die Handle-und Dateigröße müssen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="cbf67-184">The handle and file size output buffers are required to be present.</span></span> <span data-ttu-id="cbf67-185">Wenn Sie nicht vorhanden sind, stürzt die Engine ab, da die Ausgabepuffer Parameter nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="cbf67-185">If they are not present then the engine will crash because the output buffer parameters are not validated.</span></span>

<span data-ttu-id="cbf67-186">Zurzeit kann jeweils nur eine Datei für die Sicherung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="cbf67-186">At this time, only one file can be open for backup at any one time.</span></span>

<span data-ttu-id="cbf67-187">**Jetopenfileinstance** bestätigt die Sicherungs Berechtigung nicht vor dem Öffnen der angeforderten Datei.</span><span class="sxs-lookup"><span data-stu-id="cbf67-187">**JetOpenFileInstance** does not assert the backup privilege prior to opening the requested file.</span></span>

<span data-ttu-id="cbf67-188">Die Größe der zu lesenden Datei, wie von dieser Funktion gemeldet, stimmt möglicherweise nicht mit der Größe der Datei auf dem Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="cbf67-188">The size of the file to be read as reported by this function may not match the size of the file on disk.</span></span> <span data-ttu-id="cbf67-189">Unter Windows XP und höheren Versionen können zusätzliche Informationen an eine Datenbankdatei angehängt werden, die während eines Wiederherstellungs Vorgangs von der Datenbank-Engine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cbf67-189">On Windows XP and later releases, extra information may be appended to a database file which is used by the database engine during a restore operation.</span></span> <span data-ttu-id="cbf67-190">Daher sollte die Anwendung nur auf die von **jetopenfileinstance** zurückgegebene Dateigröße oder auf die tatsächliche Anzahl der von [jetreadfileinstance](./jetreadfileinstance-function.md)zurückgegebenen Daten zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="cbf67-190">As such, the application should only rely on the file size returned by **JetOpenFileInstance** or on the actual number of bytes of data returned by [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="cbf67-191">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cbf67-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cbf67-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="cbf67-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cbf67-193">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cbf67-193">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbf67-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cbf67-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cbf67-195">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cbf67-195">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbf67-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="cbf67-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cbf67-197">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="cbf67-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbf67-198"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="cbf67-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="cbf67-199">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="cbf67-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbf67-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="cbf67-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="cbf67-201">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="cbf67-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbf67-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="cbf67-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="cbf67-203">Wird als <strong>jetopenfileinstancew</strong> (Unicode) und <strong>jetopenfileinstancea</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="cbf67-203">Implemented as <strong>JetOpenFileInstanceW</strong> (Unicode) and <strong>JetOpenFileInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cbf67-204">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cbf67-204">See Also</span></span>

[<span data-ttu-id="cbf67-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cbf67-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cbf67-206">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="cbf67-206">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="cbf67-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="cbf67-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="cbf67-208">Jetattachdatabase</span><span class="sxs-lookup"><span data-stu-id="cbf67-208">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="cbf67-209">Jetbeginexternalbackupinstance</span><span class="sxs-lookup"><span data-stu-id="cbf67-209">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="cbf67-210">Jetclosefilinput Stance</span><span class="sxs-lookup"><span data-stu-id="cbf67-210">JetCloseFileInstance</span></span>](./jetclosefileinstance-function.md)  
[<span data-ttu-id="cbf67-211">Jetgetattachinfoinstance</span><span class="sxs-lookup"><span data-stu-id="cbf67-211">JetGetAttachInfoInstance</span></span>](./jetgetattachinfoinstance-function.md)  
[<span data-ttu-id="cbf67-212">Jetgetloginfoinstance</span><span class="sxs-lookup"><span data-stu-id="cbf67-212">JetGetLogInfoInstance</span></span>](./jetgetloginfoinstance-function.md)  
[<span data-ttu-id="cbf67-213">Jetreadfilinput Stance</span><span class="sxs-lookup"><span data-stu-id="cbf67-213">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="cbf67-214">Jetstopbackupinstance</span><span class="sxs-lookup"><span data-stu-id="cbf67-214">JetStopBackupInstance</span></span>](./jetstopbackupinstance-function.md)  
[<span data-ttu-id="cbf67-215">Jettruneureloginstance</span><span class="sxs-lookup"><span data-stu-id="cbf67-215">JetTruncateLogInstance</span></span>](./jettruncateloginstance-function.md)
