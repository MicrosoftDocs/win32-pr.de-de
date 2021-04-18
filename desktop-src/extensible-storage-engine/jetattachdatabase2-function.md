---
description: 'Weitere Informationen finden Sie hier: JetAttachDatabase2-Funktion'
title: JetAttachDatabase2-Funktion
TOCTitle: JetAttachDatabase2 Function
ms:assetid: 8667f3fc-d178-49f1-9474-f09352614f92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269322(v=EXCHG.10)
ms:contentKeyID: 32765612
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase2A
- JetAttachDatabase2
- JetAttachDatabase2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a5839559751fe45ec18a55de14c565116a0f9a4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351533"
---
# <a name="jetattachdatabase2-function"></a><span data-ttu-id="3b0cc-103">JetAttachDatabase2-Funktion</span><span class="sxs-lookup"><span data-stu-id="3b0cc-103">JetAttachDatabase2 Function</span></span>


<span data-ttu-id="3b0cc-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3b0cc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetattachdatabase2-function"></a><span data-ttu-id="3b0cc-105">JetAttachDatabase2-Funktion</span><span class="sxs-lookup"><span data-stu-id="3b0cc-105">JetAttachDatabase2 Function</span></span>

<span data-ttu-id="3b0cc-106">Die **JetAttachDatabase2** -Funktion fügt eine Datenbankdatei für die Verwendung mit einer Daten Bank Instanz an und gibt eine maximale Größe für diese Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-106">The **JetAttachDatabase2** function attaches a database file for use with a database instance and specifies a maximum size for that database.</span></span> <span data-ttu-id="3b0cc-107">Damit die Datenbank verwendet werden kann, muss Sie anschließend mit [jetopend Database](./jetopendatabase-function.md)geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-107">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetAttachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="3b0cc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b0cc-108">Parameters</span></span>

<span data-ttu-id="3b0cc-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="3b0cc-109">*sesid*</span></span>

<span data-ttu-id="3b0cc-110">Der Daten Bank Sitzungs Kontext, der für den API-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-110">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="3b0cc-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="3b0cc-111">*szFilename*</span></span>

<span data-ttu-id="3b0cc-112">Der Name der anzufügenden Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-112">The name of the database to attach.</span></span>

<span data-ttu-id="3b0cc-113">*cpgdatabasesizemax*</span><span class="sxs-lookup"><span data-stu-id="3b0cc-113">*cpgDatabaseSizeMax*</span></span>

<span data-ttu-id="3b0cc-114">Die maximale Größe (in Datenbankseiten) für die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-114">The maximum size, in database pages, for database.</span></span> <span data-ttu-id="3b0cc-115">Die standardmäßige Datenbankseiten Größe beträgt 4 Kilobytes, die mithilfe der [jetsetsystemparameter](./jetsetsystemparameter-function.md) -Funktion geändert werden können, bevor eine Datenbank erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-115">The default database page size is 4 kilobytes, which can be changed using the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function prior to creating a database.</span></span>

<span data-ttu-id="3b0cc-116">Das übergeben von NULL bedeutet, dass kein Maximum von der Datenbank-Engine erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-116">Passing zero means that there is no maximum enforced by the database engine.</span></span>

<span data-ttu-id="3b0cc-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="3b0cc-117">*grbit*</span></span>

<span data-ttu-id="3b0cc-118">Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten:</span><span class="sxs-lookup"><span data-stu-id="3b0cc-118">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b0cc-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3b0cc-119">Value</span></span></p></th>
<th><p><span data-ttu-id="3b0cc-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3b0cc-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b0cc-121">JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="3b0cc-121">JET_bitDbDeleteCorruptIndexes</span></span></p></td>
<td><p><span data-ttu-id="3b0cc-122">Wenn <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> festgelegt wurde, werden alle Indizes für Unicode-Daten gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-122">If <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> has been set, all indexes over Unicode data will be deleted.</span></span> <span data-ttu-id="3b0cc-123">Weitere Details finden Sie im Abschnitt „Anmerkungen“.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-123">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b0cc-124">JET_bitDbDeleteUnicodeIndexes</span><span class="sxs-lookup"><span data-stu-id="3b0cc-124">JET_bitDbDeleteUnicodeIndexes</span></span></p></td>
<td><p><span data-ttu-id="3b0cc-125">Alle Indizes für Unicode-Daten werden unabhängig von der Einstellung <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-125">All indexes over Unicode data will be deleted, regardless of the setting of <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span></span> <span data-ttu-id="3b0cc-126">Weitere Details finden Sie im Abschnitt „Anmerkungen“.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-126">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b0cc-127">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="3b0cc-127">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="3b0cc-128">Verhindert Änderungen an der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-128">Prevents modifications to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b0cc-129">JET_bitDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="3b0cc-129">JET_bitDbUpgrade</span></span></p></td>
<td><p><span data-ttu-id="3b0cc-130">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-130">Reserved for future use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="3b0cc-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b0cc-131">Return Value</span></span>

<span data-ttu-id="3b0cc-132">Die-Funktion gibt einen der [JET_ERR](./jet-err.md) Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-132">The function returns one of the [JET_ERR](./jet-err.md) error codes.</span></span> <span data-ttu-id="3b0cc-133">Im folgenden finden Sie die am häufigsten zurückgegebenen.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-133">The following are the most commonly returned.</span></span> <span data-ttu-id="3b0cc-134">(Eine komplette Liste der Fehler für diese API finden Sie unter [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)</span><span class="sxs-lookup"><span data-stu-id="3b0cc-134">(For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b0cc-135">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3b0cc-135">Return code</span></span></p></th>
<th><p><span data-ttu-id="3b0cc-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b0cc-136">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b0cc-137">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3b0cc-137">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3b0cc-138">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-138">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b0cc-139">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="3b0cc-139">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="3b0cc-140">Das Anfügen einer Datenbank ist während einer Sicherung nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-140">Attaching a database is not allowed during a backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b0cc-141">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="3b0cc-141">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="3b0cc-142">Die von <em>szFilename</em> angegebene Datenbankdatei muss beschreibbar sein.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-142">The database file specified by <em>szFilename</em> must be writable.</span></span> <span data-ttu-id="3b0cc-143">Das Read-Only-Attribut darf nicht festgelegt werden, und der laufende Prozess muss über ausreichende Berechtigungen zum Schreiben in die Datei verfügen.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-143">The Read-Only attribute must not be set, and the running process must have sufficient privileges to write to the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b0cc-144">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="3b0cc-144">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="3b0cc-145">Die Datenbankdatei wurde bereits von einem anderen Prozess geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-145">The database file is already opened by another process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b0cc-146">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="3b0cc-146">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="3b0cc-147">In " <em>szFilename</em>" wurde ein ungültiger Pfad angegeben.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-147">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="3b0cc-148">" <em>szFilename</em> " darf nicht NULL sein und verweist auf einen gültigen Pfad.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-148"><em>szFilename</em> must be non-NULL and refer to a valid path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b0cc-149">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="3b0cc-149">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="3b0cc-150">Die Datenbankdatei wurde bereits durch eine andere Sitzung angefügt.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-150">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b0cc-151">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="3b0cc-151">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="3b0cc-152">Die in <em>szFilename</em> angegebene Datei ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-152">The file given in <em>szFilename</em> does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b0cc-153">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="3b0cc-153">JET_errPrimaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="3b0cc-154">Fehler beim primären Index.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-154">There is an error with the primary index.</span></span> <span data-ttu-id="3b0cc-155">Dies kann von physischer Beschädigung (z. b. Datenträger-oder Speicher Beschädigung) verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-155">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="3b0cc-156">Sie kann auch zurückgegeben werden, wenn eine Datenbank zuletzt an einem älteren Betriebssystem geändert wird und der primäre Index eine Spalte mit Unicode-Daten ist.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-156">It may also be returned when attaching a database last modified on an older operating system and the primary index is over a column with Unicode data.</span></span> <span data-ttu-id="3b0cc-157">Weitere Informationen zu Indizes für Unicode-Daten finden Sie in den hinweisen.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-157">See the remarks for more information on indexes over Unicode data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b0cc-158">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="3b0cc-158">JET_errSecondaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="3b0cc-159">Es ist ein Fehler mit einem sekundären Index aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-159">There is an error with a secondary index.</span></span> <span data-ttu-id="3b0cc-160">Dies kann von physischer Beschädigung (z. b. Datenträger-oder Speicher Beschädigung) verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-160">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="3b0cc-161">Sie kann auch zurückgegeben werden, wenn eine Datenbank zuletzt an einem älteren Betriebssystem geändert und ein sekundärer Index über eine Spalte mit Unicode-Daten verfügt.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-161">It may also be returned when attaching a database last modified on an older operating system and a secondary index is over a column with Unicode data.</span></span> <span data-ttu-id="3b0cc-162">Weitere Informationen zu Indizes für Unicode-Daten finden Sie in den hinweisen.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-162">See the remarks for more information on indexes over Unicode data.</span></span> <span data-ttu-id="3b0cc-163">Sekundäre Indizes werden vollständig neu erstellt, wenn eine Datenbank mit einem Offline-Hilfsprogramm mit folgendem Befehl ( <strong>Esentutl-d</strong>) zerlegt wird.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-163">Secondary indexes are completely rebuilt when a database is defragmented with an offline utility using the following command: <strong>esentutl -d</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b0cc-164">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="3b0cc-164">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="3b0cc-165">Pro Instanz kann nur eine endliche Anzahl von Datenbanken angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-165">Only a finite number of databases can be attached per instance.</span></span> <span data-ttu-id="3b0cc-166">Das Limit beträgt derzeit sieben Datenbanken pro Instanz.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-166">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b0cc-167">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="3b0cc-167">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="3b0cc-168">Eine nicht schwerwiegende Warnung, die angibt, dass die Datenbankdatei bereits von dieser Sitzung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-168">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="3b0cc-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b0cc-169">Remarks</span></span>

<span data-ttu-id="3b0cc-170">Die Datenbankdatei wird mithilfe von [jetdetachdatabase](./jetdetachdatabase-function.md) oder [JetDetachDatabase2](./jetdetachdatabase2-function.md)getrennt.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-170">The database file is detached using [JetDetachDatabase](./jetdetachdatabase-function.md) or [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span></span>

<span data-ttu-id="3b0cc-171">Weitere Hinweise finden Sie unter [jetattachdatabase](./jetattachdatabase-function.md) .</span><span class="sxs-lookup"><span data-stu-id="3b0cc-171">See [JetAttachDatabase](./jetattachdatabase-function.md) for remarks.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3b0cc-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b0cc-172">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b0cc-173"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3b0cc-173"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3b0cc-174">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-174">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b0cc-175"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3b0cc-175"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3b0cc-176">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-176">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b0cc-177"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="3b0cc-177"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3b0cc-178">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-178">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b0cc-179"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="3b0cc-179"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3b0cc-180">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-180">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b0cc-181"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3b0cc-181"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3b0cc-182">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3b0cc-182">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b0cc-183"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="3b0cc-183"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="3b0cc-184">Implementiert als <strong>JetAttachDatabase2W</strong> (Unicode) und <strong>JetAttachDatabase2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="3b0cc-184">Implemented as <strong>JetAttachDatabase2W</strong> (Unicode) and <strong>JetAttachDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3b0cc-185">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3b0cc-185">See Also</span></span>

[<span data-ttu-id="3b0cc-186">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="3b0cc-186">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="3b0cc-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3b0cc-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3b0cc-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="3b0cc-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="3b0cc-189">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3b0cc-189">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3b0cc-190">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3b0cc-190">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="3b0cc-191">Jetattachdatabase</span><span class="sxs-lookup"><span data-stu-id="3b0cc-191">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="3b0cc-192">Jetkreatedatabase</span><span class="sxs-lookup"><span data-stu-id="3b0cc-192">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="3b0cc-193">Jetopumdatabase</span><span class="sxs-lookup"><span data-stu-id="3b0cc-193">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="3b0cc-194">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="3b0cc-194">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
