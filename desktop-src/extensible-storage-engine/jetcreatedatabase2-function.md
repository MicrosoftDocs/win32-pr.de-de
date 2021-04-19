---
description: 'Weitere Informationen finden Sie hier: JetCreateDatabase2-Funktion'
title: JetCreateDatabase2-Funktion
TOCTitle: JetCreateDatabase2 Function
ms:assetid: 267ac69f-49d3-4741-b324-d8510d7a36d3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269208(v=EXCHG.10)
ms:contentKeyID: 32765511
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase2A
- JetCreateDatabase2W
- JetCreateDatabase2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a370f88f95a2eb8217dc06124b50c9ed165eb679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349613"
---
# <a name="jetcreatedatabase2-function"></a><span data-ttu-id="1d4e9-103">JetCreateDatabase2-Funktion</span><span class="sxs-lookup"><span data-stu-id="1d4e9-103">JetCreateDatabase2 Function</span></span>


<span data-ttu-id="1d4e9-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1d4e9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatedatabase2-function"></a><span data-ttu-id="1d4e9-105">JetCreateDatabase2-Funktion</span><span class="sxs-lookup"><span data-stu-id="1d4e9-105">JetCreateDatabase2 Function</span></span>

<span data-ttu-id="1d4e9-106">Mit der **JetCreateDatabase2** -Funktion wird eine Datenbankdatei erstellt und angefügt, die mit der ESE-Datenbank-Engine mit einer angegebenen maximalen Datenbankgröße verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-106">The **JetCreateDatabase2** function creates and attaches a database file to be used with the ESE database engine with a maximum database size specified.</span></span> <span data-ttu-id="1d4e9-107">Das Aufrufen von **JetCreateDatabase2** mit dem auf NULL festgelegten *cpgdatabasesizemax* ist mit dem Aufrufen von [jetcreatedatabase](./jetcreatedatabase-function.md) identisch, wobei *szconnect* auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-107">Calling **JetCreateDatabase2** with *cpgDatabaseSizeMax* set to zero is identical to calling [JetCreateDatabase](./jetcreatedatabase-function.md) with *szConnect* set to NULL.</span></span> <span data-ttu-id="1d4e9-108">Zurzeit können bis zu sieben Datenbanken pro Instanz erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-108">Currently up to seven databases can be created per instance.</span></span>

```cpp
    JET_ERR JET_API JetCreateDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="1d4e9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d4e9-109">Parameters</span></span>

<span data-ttu-id="1d4e9-110">*-sid*</span><span class="sxs-lookup"><span data-stu-id="1d4e9-110">*sesid*</span></span>

<span data-ttu-id="1d4e9-111">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="1d4e9-112">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="1d4e9-112">*szFilename*</span></span>

<span data-ttu-id="1d4e9-113">Der Name der zu erstellenden Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-113">The name of the database to be created.</span></span>

<span data-ttu-id="1d4e9-114">*cpgdatabasesizemax*</span><span class="sxs-lookup"><span data-stu-id="1d4e9-114">*cpgDatabaseSizeMax*</span></span>

<span data-ttu-id="1d4e9-115">Die maximale Größe (in Datenbankseiten) für die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-115">The maximum size, in database pages, for the database.</span></span> <span data-ttu-id="1d4e9-116">Die standardmäßige Datenbankseiten Größe beträgt 4 KB und kann mit [jetsetsystemparameter](./jetsetsystemparameter-function.md) geändert werden, bevor eine Datenbank erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-116">The default database page size is 4 kilobytes, and can be changed with [JetSetSystemParameter](./jetsetsystemparameter-function.md) prior to creating a database.</span></span>

<span data-ttu-id="1d4e9-117">Das übergeben von NULL bedeutet, dass kein Maximum von der Datenbank-Engine erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-117">Passing zero means that there is no maximum enforced by the database engine.</span></span>

<span data-ttu-id="1d4e9-118">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="1d4e9-118">*pdbid*</span></span>

<span data-ttu-id="1d4e9-119">Ein Zeiger auf einen Puffer, der bei einem erfolgreichen-Aufrufwert den Bezeichner der Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-119">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="1d4e9-120">Bei einem Fehler ist der Wert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-120">On failure, the value is undefined.</span></span>

<span data-ttu-id="1d4e9-121">*grbit*</span><span class="sxs-lookup"><span data-stu-id="1d4e9-121">*grbit*</span></span>

<span data-ttu-id="1d4e9-122">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-122">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d4e9-123">Wert</span><span class="sxs-lookup"><span data-stu-id="1d4e9-123">Value</span></span></p></th>
<th><p><span data-ttu-id="1d4e9-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1d4e9-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d4e9-125">JET_bitDbOverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="1d4e9-125">JET_bitDbOverwriteExisting</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-126">Wenn <a href="gg269212(v=exchg.10).md">jetkreatedatabase</a> oder <strong>JetCreateDatabase2</strong> aufgerufen wird und die Datenbank bereits vorhanden ist, schlägt der API-Aufruf standardmäßig fehl, und die ursprüngliche Datenbank wird nicht überschrieben.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-126">By default, if <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> or <strong>JetCreateDatabase2</strong> is called and the database already exists, the API call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="1d4e9-127">JET_bitDbOverwriteExisting ändert dieses Verhalten, und die alte Datenbank wird mit einem neuen überschrieben.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-127">JET_bitDbOverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span> <span data-ttu-id="1d4e9-128">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-128">Windows XP and later.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d4e9-129">JET_bitDbRecoveryOff</span><span class="sxs-lookup"><span data-stu-id="1d4e9-129">JET_bitDbRecoveryOff</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-130">JET_bitDbRecoveryOff deaktiviert die Protokollierung.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-130">JET_bitDbRecoveryOff turns off logging.</span></span> <span data-ttu-id="1d4e9-131">Das Festlegen dieses Bits verliert die Möglichkeit, Protokolldateien wiederzugeben und die Datenbank nach einem katastrophalen Ereignis in einem konsistenten verwendbaren Zustand wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-131">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a catastrophic event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d4e9-132">JET_bitDbShadowingOff</span><span class="sxs-lookup"><span data-stu-id="1d4e9-132">JET_bitDbShadowingOff</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-133">Wenn Sie JET_bitDbShadowingOff festlegen, wird die Duplizierung einiger interner Datenbankstrukturen (shadowingup) deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-133">Setting JET_bitDbShadowingOff will disable the duplication of some internal database structures (shadowing).</span></span> <span data-ttu-id="1d4e9-134">Die Duplizierung dieser Strukturen erfolgt aus Gründen der Resilienz, sodass durch das Festlegen von JET_bitDbShadowingOff diese Resilienz entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-134">The duplication of these structures is done for resiliency, so setting JET_bitDbShadowingOff will remove that resiliency.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="1d4e9-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d4e9-135">Return Value</span></span>

<span data-ttu-id="1d4e9-136">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1d4e9-137">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1d4e9-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d4e9-138">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1d4e9-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="1d4e9-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d4e9-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d4e9-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1d4e9-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-141">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d4e9-142">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="1d4e9-142">JET_errDatabaseDuplicate</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-143">Die in <em>szFilename</em> benannte Datenbank ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-143">The database named in <em>szFilename</em> already exists.</span></span> <span data-ttu-id="1d4e9-144">Wenn dieser Fehler zurückgegeben wird, wird die Datenbank nicht angefügt.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-144">When this error is returned, the database does not get attached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d4e9-145">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="1d4e9-145">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-146">Kann zurückgegeben werden, wenn exklusiver Zugriff angefordert wurde, jedoch nicht erteilt werden konnte oder wenn die Datenbank bereits von einer anderen Sitzung bereits geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-146">Can be returned if exclusive access was requested, but could not be granted, or if another session has already opened the database exclusively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d4e9-147">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="1d4e9-147">JET_errDatabaseInvalidPages</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-148">Wird zurückgegeben, wenn <em>cpgdatabasesizemax</em> größer ist als die maximale Anzahl von Seiten, die in einer Datenbank zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-148">Returned when <em>cpgDatabaseSizeMax</em> is larger than the maximum number of pages allowed in a database.</span></span> <span data-ttu-id="1d4e9-149">Der aktuelle Höchstwert ist 2147483646 (0x7ffffffe).</span><span class="sxs-lookup"><span data-stu-id="1d4e9-149">The current maximum is 2147483646 (0x7ffffffe).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d4e9-150">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="1d4e9-150">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-151">In " <em>szFilename</em>" wurde ein ungültiger Pfad angegeben.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-151">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="1d4e9-152">" <em>szFilename</em> " darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-152"><em>szFilename</em> must be non-NULL.</span></span> <span data-ttu-id="1d4e9-153">Standardmäßig muss " <em>szFilename</em> " auf ein Verzeichnis verweisen, das vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-153">By default, <em>szFilename</em> must point to a directory that exists.</span></span> <span data-ttu-id="1d4e9-154">Der Pfad wird erstellt, wenn <em>JET_paramCreatePathIfNotExist</em> festgelegt ist (siehe <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a>).</span><span class="sxs-lookup"><span data-stu-id="1d4e9-154">The path will be created if <em>JET_paramCreatePathIfNotExist</em> is set (See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d4e9-155">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="1d4e9-155">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-156">Gibt an, dass eine andere Sitzung die Datenbank bereits exklusiv geöffnet hat (mit JET_bitDbExclusive).</span><span class="sxs-lookup"><span data-stu-id="1d4e9-156">Indicates that another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d4e9-157">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="1d4e9-157">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-158">Die Datenbank wurde zuvor nicht angefügt (siehe <a href="gg294074(v=exchg.10).md">jetattachdatabase</a>).</span><span class="sxs-lookup"><span data-stu-id="1d4e9-158">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d4e9-159">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="1d4e9-159">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-160">Die Datenbankdatei wurde bereits durch eine andere Sitzung angefügt.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-160">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d4e9-161">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="1d4e9-161">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-162">Es wurde versucht, eine Datenbank zu erstellen, während eine Transaktion durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-162">An attempt was made to create a database while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d4e9-163">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="1d4e9-163">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-164">Es wurde versucht, eine Datei zu öffnen, die keine gültige Datenbankdatei ist.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-164">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d4e9-165">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="1d4e9-165">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-166">Es wurde versucht, mehr als eine Datenbank zu öffnen, und JET_paramOneDatabasePerSession wurde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-166">An attempt was made to open more than one database, and JET_paramOneDatabasePerSession was set.</span></span> <span data-ttu-id="1d4e9-167">Siehe <a href="gg294139(v=exchg.10).md">System Parameter</a>.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-167">See <a href="gg294139(v=exchg.10).md">System Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d4e9-168">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="1d4e9-168">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-169">Das System verfügt über wenig Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-169">The system ran low on resources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d4e9-170">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="1d4e9-170">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-171">Pro Instanz kann nur eine endliche Anzahl von Datenbanken angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-171">Only a finite number of database can be attached per instance.</span></span> <span data-ttu-id="1d4e9-172">Das Limit beträgt derzeit sieben Datenbanken pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-172">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d4e9-173">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="1d4e9-173">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-174">Eine nicht schwerwiegende Warnung, die angibt, dass die Datenbankdatei bereits von dieser Sitzung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-174">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d4e9-175">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="1d4e9-175">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="1d4e9-176">JET_wrnFileOpenReadOnly gibt an, dass die Datei schreibgeschützt angefügt wurde, aber <a href="gg269212(v=exchg.10).md">jetkreatedatabase</a> nicht JET_bitDbReadOnly bestanden hat.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-176">JET_wrnFileOpenReadOnly indicates that the file was attached read-only, but <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="1d4e9-177">Die Datenbank wird immer noch mit Schreib geschütztem Zugriff geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-177">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="1d4e9-178">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d4e9-178">Remarks</span></span>

<span data-ttu-id="1d4e9-179">Wenn die in *szFilename* angegebene Datenbank vorhanden ist und JET_bitDbOverwriteExisting nicht übermittelt wurde, tritt beim API-Befehl ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-179">If the database specified in *szFilename* exists and JET_bitDbOverwriteExisting was not passed in, the API call will fail.</span></span> <span data-ttu-id="1d4e9-180">Wenn JET_bitDbOverwriteExisting übermittelt wurde, wird die alte Datenbankdatei zuerst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-180">If JET_bitDbOverwriteExisting was passed in, the old database file will be deleted first.</span></span>

<span data-ttu-id="1d4e9-181">Wenn die API eine Datenbankdatei erstellt und dann auf einen anderen Fehler stößt, wird die Datei bereinigt und gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-181">If the API creates a database file and then hits another error, it will clean up and delete the file.</span></span>

<span data-ttu-id="1d4e9-182">**JetCreateDatabase2** öffnet die Datenbank implizit.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-182">**JetCreateDatabase2** will implicitly open the database.</span></span> <span data-ttu-id="1d4e9-183">Es ist nicht erforderlich, anschließend [jetopendatabase](./jetopendatabase-function.md)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-183">It is not necessary to subsequently call [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="1d4e9-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d4e9-184">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d4e9-185"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="1d4e9-185"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1d4e9-186">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-186">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d4e9-187"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1d4e9-187"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1d4e9-188">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-188">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d4e9-189"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1d4e9-189"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1d4e9-190">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-190">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d4e9-191"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="1d4e9-191"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1d4e9-192">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-192">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d4e9-193"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1d4e9-193"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1d4e9-194">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1d4e9-194">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d4e9-195"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="1d4e9-195"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="1d4e9-196">Implementiert als <strong>JetCreateDatabase2W</strong> (Unicode) und <strong>JetCreateDatabase2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="1d4e9-196">Implemented as <strong>JetCreateDatabase2W</strong> (Unicode) and <strong>JetCreateDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1d4e9-197">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1d4e9-197">See Also</span></span>

[<span data-ttu-id="1d4e9-198">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="1d4e9-198">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="1d4e9-199">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1d4e9-199">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1d4e9-200">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="1d4e9-200">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="1d4e9-201">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1d4e9-201">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1d4e9-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1d4e9-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1d4e9-203">Jetattachdatabase</span><span class="sxs-lookup"><span data-stu-id="1d4e9-203">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="1d4e9-204">Jetclosedatabase</span><span class="sxs-lookup"><span data-stu-id="1d4e9-204">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="1d4e9-205">Jetkreatedatabase</span><span class="sxs-lookup"><span data-stu-id="1d4e9-205">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="1d4e9-206">Jetopumdatabase</span><span class="sxs-lookup"><span data-stu-id="1d4e9-206">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="1d4e9-207">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="1d4e9-207">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="1d4e9-208">System Parameter</span><span class="sxs-lookup"><span data-stu-id="1d4e9-208">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
