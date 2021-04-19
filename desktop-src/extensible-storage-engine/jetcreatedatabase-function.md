---
description: 'Weitere Informationen zu: jetkreatedatabase-Funktion'
title: JetCreateDatabase-Funktion
TOCTitle: JetCreateDatabase Function
ms:assetid: 2b13b038-1694-46d8-b903-9be64384cb06
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269212(v=EXCHG.10)
ms:contentKeyID: 32765515
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase
- JetCreateDatabaseA
- JetCreateDatabaseW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8fbec76e3b38f9b42c36156b2312a8e77a6b43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362271"
---
# <a name="jetcreatedatabase-function"></a><span data-ttu-id="20f25-103">JetCreateDatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="20f25-103">JetCreateDatabase Function</span></span>


<span data-ttu-id="20f25-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="20f25-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatedatabase-function"></a><span data-ttu-id="20f25-105">JetCreateDatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="20f25-105">JetCreateDatabase Function</span></span>

<span data-ttu-id="20f25-106">Die **jetkreatedatabase** -Funktion erstellt eine Datenbankdatei und fügt Sie an, die für die ESE-Datenbank-Engine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="20f25-106">The **JetCreateDatabase** function creates and attaches a database file to be used with the ESE database engine.</span></span> <span data-ttu-id="20f25-107">Das Aufrufen von [JetCreateDatabase2](./jetcreatedatabase2-function.md) mit dem auf NULL festgelegten *cpgdatabasesizemax* ist mit dem Aufrufen von **jetcreatedatabase** identisch, wobei *szconnect* auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="20f25-107">Calling [JetCreateDatabase2](./jetcreatedatabase2-function.md) with *cpgDatabaseSizeMax* set to zero is identical to calling **JetCreateDatabase** with *szConnect* set to NULL.</span></span> <span data-ttu-id="20f25-108">Zurzeit können bis zu sieben Datenbanken pro Instanz erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="20f25-108">Currently, up to seven databases can be created per instance.</span></span>

```cpp
    JET_ERR JET_API JetCreateDatabase(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szFilename,
      __in_opt      JET_PCSTR szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="20f25-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="20f25-109">Parameters</span></span>

<span data-ttu-id="20f25-110">*-sid*</span><span class="sxs-lookup"><span data-stu-id="20f25-110">*sesid*</span></span>

<span data-ttu-id="20f25-111">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="20f25-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="20f25-112">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="20f25-112">*szFilename*</span></span>

<span data-ttu-id="20f25-113">Der Name der zu erstellenden Datenbank.</span><span class="sxs-lookup"><span data-stu-id="20f25-113">The name of the database to be created.</span></span>

<span data-ttu-id="20f25-114">*szconnect*</span><span class="sxs-lookup"><span data-stu-id="20f25-114">*szConnect*</span></span>

<span data-ttu-id="20f25-115">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="20f25-115">Reserved for future use.</span></span> <span data-ttu-id="20f25-116">Auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="20f25-116">Set to NULL.</span></span>

<span data-ttu-id="20f25-117">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="20f25-117">*pdbid*</span></span>

<span data-ttu-id="20f25-118">Ein Zeiger auf einen Puffer, der bei einem erfolgreichen-Aufrufwert den Bezeichner der Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="20f25-118">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="20f25-119">Bei einem Fehler ist der Wert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="20f25-119">On failure, the value is undefined.</span></span>

<span data-ttu-id="20f25-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="20f25-120">*grbit*</span></span>

<span data-ttu-id="20f25-121">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="20f25-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20f25-122">Wert</span><span class="sxs-lookup"><span data-stu-id="20f25-122">Value</span></span></p></th>
<th><p><span data-ttu-id="20f25-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="20f25-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20f25-124">JET_bitDbOverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="20f25-124">JET_bitDbOverwriteExisting</span></span></p></td>
<td><p><span data-ttu-id="20f25-125">Wenn <strong>jetkreatedatabase</strong> aufgerufen wird und die Datenbank bereits vorhanden ist, schlägt der API-Aufruf standardmäßig fehl, und die ursprüngliche Datenbank wird nicht überschrieben.</span><span class="sxs-lookup"><span data-stu-id="20f25-125">By default, if <strong>JetCreateDatabase</strong> is called and the database already exists, the API call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="20f25-126">JET_bitDbOverwriteExisting ändert dieses Verhalten, und die alte Datenbank wird mit einem neuen überschrieben.</span><span class="sxs-lookup"><span data-stu-id="20f25-126">JET_bitDbOverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span> <span data-ttu-id="20f25-127">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="20f25-127">Windows XP and later.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20f25-128">JET_bitDbRecoveryOff</span><span class="sxs-lookup"><span data-stu-id="20f25-128">JET_bitDbRecoveryOff</span></span></p></td>
<td><p><span data-ttu-id="20f25-129">JET_bitDbRecoveryOff deaktiviert die Protokollierung.</span><span class="sxs-lookup"><span data-stu-id="20f25-129">JET_bitDbRecoveryOff turns off logging.</span></span> <span data-ttu-id="20f25-130">Das Festlegen dieses Bits verliert die Möglichkeit, Protokolldateien wiederzugeben und die Datenbank nach einem katastrophalen Ereignis in einem konsistenten verwendbaren Zustand wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="20f25-130">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a catastrophic event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20f25-131">JET_bitDbShadowingOff</span><span class="sxs-lookup"><span data-stu-id="20f25-131">JET_bitDbShadowingOff</span></span></p></td>
<td><p><span data-ttu-id="20f25-132">Wenn Sie JET_bitDbShadowingOff festlegen, wird die Duplizierung einiger interner Datenbankstrukturen (shadowingup) deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="20f25-132">Setting JET_bitDbShadowingOff will disable the duplication of some internal database structures (shadowing).</span></span> <span data-ttu-id="20f25-133">Die Duplizierung dieser Strukturen erfolgt aus Gründen der Resilienz, sodass durch das Festlegen von JET_bitDbShadowingOff diese Resilienz entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="20f25-133">The duplication of these structures is done for resiliency, so setting JET_bitDbShadowingOff will remove that resiliency.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="20f25-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20f25-134">Return Value</span></span>

<span data-ttu-id="20f25-135">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="20f25-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="20f25-136">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="20f25-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20f25-137">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="20f25-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="20f25-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20f25-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20f25-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="20f25-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="20f25-140">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="20f25-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20f25-141">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="20f25-141">JET_errDatabaseDuplicate</span></span></p></td>
<td><p><span data-ttu-id="20f25-142">Die in <em>szFilename</em> benannte Datenbank ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="20f25-142">The database named in <em>szFilename</em> already exists.</span></span> <span data-ttu-id="20f25-143">Wenn dieser Fehler zurückgegeben wird, wird die Datenbank nicht angefügt.</span><span class="sxs-lookup"><span data-stu-id="20f25-143">When this error is returned, the database does not get attached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20f25-144">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="20f25-144">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="20f25-145">Kann zurückgegeben werden, wenn exklusiver Zugriff angefordert wurde, jedoch nicht erteilt werden konnte oder wenn die Datenbank bereits von einer anderen Sitzung bereits geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="20f25-145">Can be returned if exclusive access was requested, but could not be granted, or if another session has already opened the database exclusively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20f25-146">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="20f25-146">JET_errDatabaseInvalidPages</span></span></p></td>
<td><p><span data-ttu-id="20f25-147">Wird zurückgegeben, wenn <em>cpgdatabasesizemax</em> größer ist als die maximale Anzahl von Seiten, die in einer Datenbank zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="20f25-147">Returned when <em>cpgDatabaseSizeMax</em> is larger than the maximum number of pages allowed in a database.</span></span> <span data-ttu-id="20f25-148">Der aktuelle Höchstwert ist 2147483646 (0x7ffffffe).</span><span class="sxs-lookup"><span data-stu-id="20f25-148">The current maximum is 2147483646 (0x7ffffffe).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20f25-149">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="20f25-149">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="20f25-150">In " <em>szFilename</em>" wurde ein ungültiger Pfad angegeben.</span><span class="sxs-lookup"><span data-stu-id="20f25-150">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="20f25-151">" <em>szFilename</em> " darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="20f25-151"><em>szFilename</em> must be non-NULL.</span></span> <span data-ttu-id="20f25-152">Standardmäßig muss " <em>szFilename</em> " auf ein Verzeichnis verweisen, das vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="20f25-152">By default, <em>szFilename</em> must point to a directory that exists.</span></span> <span data-ttu-id="20f25-153">Der Pfad wird erstellt, wenn <em>JET_paramCreatePathIfNotExist</em> festgelegt ist (siehe <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a>).</span><span class="sxs-lookup"><span data-stu-id="20f25-153">The path will be created if <em>JET_paramCreatePathIfNotExist</em> is set (See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20f25-154">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="20f25-154">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="20f25-155">Gibt an, dass eine andere Sitzung die Datenbank bereits exklusiv geöffnet hat (mit JET_bitDbExclusive).</span><span class="sxs-lookup"><span data-stu-id="20f25-155">Indicates that another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20f25-156">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="20f25-156">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="20f25-157">Die Datenbank wurde zuvor nicht angefügt (siehe <a href="gg294074(v=exchg.10).md">jetattachdatabase</a>).</span><span class="sxs-lookup"><span data-stu-id="20f25-157">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20f25-158">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="20f25-158">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="20f25-159">Die Datenbankdatei wurde bereits durch eine andere Sitzung angefügt.</span><span class="sxs-lookup"><span data-stu-id="20f25-159">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20f25-160">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="20f25-160">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="20f25-161">Es wurde versucht, eine Datenbank zu erstellen, während eine Transaktion durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="20f25-161">An attempt was made to create a database while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20f25-162">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="20f25-162">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="20f25-163">Es wurde versucht, eine Datei zu öffnen, die keine gültige Datenbankdatei ist.</span><span class="sxs-lookup"><span data-stu-id="20f25-163">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20f25-164">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="20f25-164">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="20f25-165">Es wurde versucht, mehr als eine Datenbank zu öffnen, und JET_paramOneDatabasePerSession wurde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="20f25-165">An attempt was made to open more than one database, and JET_paramOneDatabasePerSession was set.</span></span> <span data-ttu-id="20f25-166">Siehe <a href="gg269337(v=exchg.10).md">Daten Bank Parameter</a>.</span><span class="sxs-lookup"><span data-stu-id="20f25-166">See <a href="gg269337(v=exchg.10).md">Database Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20f25-167">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="20f25-167">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="20f25-168">Der Vorgang konnte nicht ausgeführt werden, da kein Arbeitsspeicher zugeordnet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="20f25-168">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20f25-169">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="20f25-169">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="20f25-170">Pro Instanz kann nur eine endliche Anzahl von Datenbanken angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="20f25-170">Only a finite number of database can be attached per instance.</span></span> <span data-ttu-id="20f25-171">Das Limit beträgt derzeit sieben Datenbanken pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="20f25-171">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20f25-172">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="20f25-172">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="20f25-173">Eine nicht schwerwiegende Warnung, die angibt, dass die Datenbankdatei bereits von dieser Sitzung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="20f25-173">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20f25-174">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="20f25-174">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="20f25-175">JET_wrnFileOpenReadOnly gibt an, dass die Datei schreibgeschützt angefügt wurde, aber <strong>jetkreatedatabase</strong> nicht JET_bitDbReadOnly bestanden hat.</span><span class="sxs-lookup"><span data-stu-id="20f25-175">JET_wrnFileOpenReadOnly indicates that the file was attached read-only, but <strong>JetCreateDatabase</strong> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="20f25-176">Die Datenbank wird immer noch mit Schreib geschütztem Zugriff geöffnet.</span><span class="sxs-lookup"><span data-stu-id="20f25-176">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="20f25-177">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20f25-177">Remarks</span></span>

<span data-ttu-id="20f25-178">Wenn die in *szFilename* angegebene Datenbank vorhanden ist und JET_bitDbOverwriteExisting nicht übermittelt wurde, tritt beim API-Befehl ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="20f25-178">If the database specified in *szFilename* exists and JET_bitDbOverwriteExisting was not passed in, the API call will fail.</span></span> <span data-ttu-id="20f25-179">Wenn JET_bitDbOverwriteExisting übermittelt wurde, wird die alte Datenbankdatei zuerst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="20f25-179">If JET_bitDbOverwriteExisting was passed in, the old database file will be deleted first.</span></span>

<span data-ttu-id="20f25-180">Wenn die API eine Datenbankdatei erstellt und dann auf einen anderen Fehler stößt, wird die Datei bereinigt und gelöscht.</span><span class="sxs-lookup"><span data-stu-id="20f25-180">If the API creates a database file and then hits another error, it will clean up and delete the file.</span></span>

<span data-ttu-id="20f25-181">**Jetkreatedatabase** öffnet die Datenbank implizit.</span><span class="sxs-lookup"><span data-stu-id="20f25-181">**JetCreateDatabase** will implicitly open the database.</span></span> <span data-ttu-id="20f25-182">Es ist nicht zwingend notwendig, anschließend [jetopbank](./jetopendatabase-function.md)zu nennen.</span><span class="sxs-lookup"><span data-stu-id="20f25-182">It is not necessarily to subsequently call [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="20f25-183">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20f25-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20f25-184"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="20f25-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="20f25-185">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="20f25-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20f25-186"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="20f25-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="20f25-187">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="20f25-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20f25-188"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="20f25-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="20f25-189">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="20f25-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20f25-190"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="20f25-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="20f25-191">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="20f25-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20f25-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="20f25-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="20f25-193">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="20f25-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20f25-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="20f25-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="20f25-195">Implementiert als <strong>jetkreatedatabasew</strong> (Unicode) und <strong>jetkreatedatabasea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="20f25-195">Implemented as <strong>JetCreateDatabaseW</strong> (Unicode) and <strong>JetCreateDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="20f25-196">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="20f25-196">See Also</span></span>

[<span data-ttu-id="20f25-197">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="20f25-197">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="20f25-198">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="20f25-198">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="20f25-199">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="20f25-199">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="20f25-200">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="20f25-200">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="20f25-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="20f25-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="20f25-202">Jetattachdatabase</span><span class="sxs-lookup"><span data-stu-id="20f25-202">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="20f25-203">Jetclosedatabase</span><span class="sxs-lookup"><span data-stu-id="20f25-203">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="20f25-204">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="20f25-204">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="20f25-205">Jetopumdatabase</span><span class="sxs-lookup"><span data-stu-id="20f25-205">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="20f25-206">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="20f25-206">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="20f25-207">System Parameter</span><span class="sxs-lookup"><span data-stu-id="20f25-207">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
