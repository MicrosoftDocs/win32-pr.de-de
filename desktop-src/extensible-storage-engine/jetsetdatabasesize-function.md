---
description: 'Weitere Informationen zu: jetsetdatabasesize-Funktion'
title: Jetsetdatabasesize-Funktion
TOCTitle: JetSetDatabaseSize Function
ms:assetid: 4a87bf43-c8f7-4966-9f1f-68c16d1cb558
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269242(v=EXCHG.10)
ms:contentKeyID: 32765544
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetDatabaseSizeW
- JetSetDatabaseSize
- JetSetDatabaseSizeA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd450a0afed0256b0b80d97a278dccf99418a900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128152"
---
# <a name="jetsetdatabasesize-function"></a><span data-ttu-id="da3c9-103">Jetsetdatabasesize-Funktion</span><span class="sxs-lookup"><span data-stu-id="da3c9-103">JetSetDatabaseSize Function</span></span>


<span data-ttu-id="da3c9-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="da3c9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetdatabasesize-function"></a><span data-ttu-id="da3c9-105">Jetsetdatabasesize-Funktion</span><span class="sxs-lookup"><span data-stu-id="da3c9-105">JetSetDatabaseSize Function</span></span>

<span data-ttu-id="da3c9-106">Die **jetsetdatabasesize** -Funktion legt die Größe einer nicht geöffneten Datenbankdatei fest.</span><span class="sxs-lookup"><span data-stu-id="da3c9-106">The **JetSetDatabaseSize** function sets the size of an unopened database file.</span></span>

```cpp
    JET_ERR JET_API JetSetDatabaseSize(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseName,
      __in          unsigned long cpg,
      __out         unsigned long* pcpgReal
    );
```

### <a name="parameters"></a><span data-ttu-id="da3c9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="da3c9-107">Parameters</span></span>

<span data-ttu-id="da3c9-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="da3c9-108">*sesid*</span></span>

<span data-ttu-id="da3c9-109">Identifiziert den Daten Bank Sitzungs Kontext, der für den API-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="da3c9-109">Identifies the database session context to use for the API call.</span></span>

<span data-ttu-id="da3c9-110">*szdatabasename*</span><span class="sxs-lookup"><span data-stu-id="da3c9-110">*szDatabaseName*</span></span>

<span data-ttu-id="da3c9-111">Identifiziert den Namen der Datenbankdatei, deren Größe geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="da3c9-111">Identifies the name of the database file whose size is to be altered.</span></span>

<span data-ttu-id="da3c9-112">*Verbrauchsgüter*</span><span class="sxs-lookup"><span data-stu-id="da3c9-112">*cpg*</span></span>

<span data-ttu-id="da3c9-113">Gibt die gewünschte Größe der Datenbank in Seiten an.</span><span class="sxs-lookup"><span data-stu-id="da3c9-113">Specifies the desired size of the database, in pages.</span></span>

<span data-ttu-id="da3c9-114">*pcpgreal*</span><span class="sxs-lookup"><span data-stu-id="da3c9-114">*pcpgReal*</span></span>

<span data-ttu-id="da3c9-115">Zeiger auf eine Zahl, die die Größe der Datenbank in Seiten nach dem API-Befehl empfängt.</span><span class="sxs-lookup"><span data-stu-id="da3c9-115">Pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="da3c9-116">Wenn der API-Befehl nicht erfolgreich war, ist der Inhalt von *pcpgreal* nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="da3c9-116">If the API call was unsuccessful, the contents of *pcpgReal* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="da3c9-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da3c9-117">Return Value</span></span>

<span data-ttu-id="da3c9-118">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="da3c9-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="da3c9-119">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="da3c9-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da3c9-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="da3c9-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="da3c9-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da3c9-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da3c9-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="da3c9-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="da3c9-123">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="da3c9-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da3c9-124">JET_errDatabaseInconsistent</span><span class="sxs-lookup"><span data-stu-id="da3c9-124">JET_errDatabaseInconsistent</span></span><br />
<span data-ttu-id="da3c9-125">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="da3c9-125">JET_errDatabaseDirtyShutdown</span></span></p></td>
<td><p><span data-ttu-id="da3c9-126">JET_errDatabaseInconsistent und JET_errDatabaseDirtyShutdown haben denselben numerischen Wert.</span><span class="sxs-lookup"><span data-stu-id="da3c9-126">JET_errDatabaseInconsistent and JET_errDatabaseDirtyShutdown are the same numeric value.</span></span> <span data-ttu-id="da3c9-127">Die Datenbank, deren Größe angepasst werden soll, muss sich in einem sauberen Herunterfahren befinden, das als einheitlicher Zustand bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="da3c9-127">The database whose size is to be adjusted must be in a clean shutdown, known as a consistent state.</span></span> <span data-ttu-id="da3c9-128">Eine inkonsistente Datenbank ist nicht beschädigt, erfordert jedoch, dass Protokolldateien wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="da3c9-128">An inconsistent database is not corrupted, but it requires log files to be replayed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da3c9-129">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="da3c9-129">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="da3c9-130"><em>szdatabasename</em> darf keine leere Zeichenfolge sein, die nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="da3c9-130"><em>szDatabaseName</em> must not be an empty, non-NULL string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da3c9-131">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="da3c9-131">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="da3c9-132">Auf dem Volume ist nicht genügend freier Speicherplatz vorhanden, um die Vergrößerung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="da3c9-132">There is insufficient free space on the volume to perform the grow operation.</span></span> <span data-ttu-id="da3c9-133"><strong>Jetsetdatabasesize</strong> kann auch eine Vielzahl von Datei bezogenen Fehlern zurückgeben, einschließlich, aber nicht beschränkt auf:</span><span class="sxs-lookup"><span data-stu-id="da3c9-133"><strong>JetSetDatabaseSize</strong> may also return many file-related errors, including, but not limited to:</span></span></p>
<ul>
<li><p><span data-ttu-id="da3c9-134">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="da3c9-134">JET_errDiskIO</span></span></p></li>
<li><p><span data-ttu-id="da3c9-135">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="da3c9-135">JET_errFileNotFound</span></span></p></li>
<li><p><span data-ttu-id="da3c9-136">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="da3c9-136">JET_errInvalidPath</span></span></p></li>
<li><p><span data-ttu-id="da3c9-137">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="da3c9-137">JET_errFileAccessDenied</span></span></p></li>
<li><p><span data-ttu-id="da3c9-138">JET_errOutOfFileHandles</span><span class="sxs-lookup"><span data-stu-id="da3c9-138">JET_errOutOfFileHandles</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da3c9-139">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="da3c9-139">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="da3c9-140">Dieser Fehler kann zurückgegeben werden, wenn <em>Verbrauchsgüter</em> die minimale Datenbankgröße erreicht.</span><span class="sxs-lookup"><span data-stu-id="da3c9-140">One of the reasons this error may be returned is if <em>cpg</em> does meet the minimum database size.</span></span> <span data-ttu-id="da3c9-141">Die aktuelle minimale Datenbankgröße beträgt 256 Seiten.</span><span class="sxs-lookup"><span data-stu-id="da3c9-141">The current minimum database size is 256 pages.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da3c9-142">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="da3c9-142">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="da3c9-143">Das System verfügt nicht über genügend Arbeitsspeicher Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="da3c9-143">The system is low on memory resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="da3c9-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da3c9-144">Remarks</span></span>

<span data-ttu-id="da3c9-145">Wenn **jetsetdatabasesize** aufgerufen wird, bevor große Datenmengen eingefügt werden, wird die Datenbankdatei in einem Vorgang vergrößert.</span><span class="sxs-lookup"><span data-stu-id="da3c9-145">If **JetSetDatabaseSize** is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="da3c9-146">Dadurch wird die Wahrscheinlichkeit verringert, dass die Datenbankdatei auf Dateisystem Ebene fragmentiert wird. Außerdem wird die Häufigkeit reduziert, mit der die Datenbankdatei vergrößert werden muss.</span><span class="sxs-lookup"><span data-stu-id="da3c9-146">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="da3c9-147">Wenn Sie die Datenbankdatei einmal vergrößern, kann Sie schneller sein, als Sie mehrmals anwachsen.</span><span class="sxs-lookup"><span data-stu-id="da3c9-147">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="da3c9-148">Derzeit wird nur die Vergrößerung der Datei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="da3c9-148">Only growing the file is currently supported.</span></span> <span data-ttu-id="da3c9-149">Um eine Datei zu verkleinern, verwenden Sie die Defragmentierungs Funktion des Programms esentutl.exe Hilfsprogramms.</span><span class="sxs-lookup"><span data-stu-id="da3c9-149">To shrink a file, use the defragmentation feature of the esentutl.exe utility program.</span></span>

<span data-ttu-id="da3c9-150">Wenn *Verbrauchsgüter* kleiner als die aktuelle Größe der Datenbank ist, wird der Vorgang ignoriert.</span><span class="sxs-lookup"><span data-stu-id="da3c9-150">If *cpg* is smaller than the current size of the database, the operation will be ignored.</span></span> <span data-ttu-id="da3c9-151">Wenn *Verbrauchsgüter* kleiner ist als die minimale Datenbankgröße (derzeit 256 Seiten), wird JET_errInvalidParameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="da3c9-151">If *cpg* is less than the minimum database size (currently 256 pages), it will return JET_errInvalidParameter.</span></span>

<span data-ttu-id="da3c9-152">Informationen zum Festlegen der Größe einer Datenbank, die geöffnet wird, finden Sie unter [jetgrowdatabase](./jetgrowdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="da3c9-152">To set the size of a database that is opened, see [JetGrowDatabase](./jetgrowdatabase-function.md).</span></span>

<span data-ttu-id="da3c9-153">Die Dateigröße entspricht möglicherweise nicht der Anzahl der Seiten, die in *pcpgreal* zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="da3c9-153">The file size may not match the number of pages returned in *pcpgReal*.</span></span> <span data-ttu-id="da3c9-154">Es gibt zwei weitere reservierte Seiten, die möglicherweise nicht in *pcpgreal* gezählt werden.</span><span class="sxs-lookup"><span data-stu-id="da3c9-154">There are two additional reserved pages that may not be counted in *pcpgReal*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="da3c9-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da3c9-155">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da3c9-156"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="da3c9-156"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="da3c9-157">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="da3c9-157">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da3c9-158"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="da3c9-158"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="da3c9-159">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="da3c9-159">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da3c9-160"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="da3c9-160"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="da3c9-161">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="da3c9-161">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da3c9-162"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="da3c9-162"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="da3c9-163">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="da3c9-163">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da3c9-164"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="da3c9-164"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="da3c9-165">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="da3c9-165">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da3c9-166"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="da3c9-166"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="da3c9-167">Implementiert als <strong>jetsetdatabasesizew</strong> (Unicode) und <strong>jetsetdatabasesizea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="da3c9-167">Implemented as <strong>JetSetDatabaseSizeW</strong> (Unicode) and <strong>JetSetDatabaseSizeA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="da3c9-168">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="da3c9-168">See Also</span></span>

[<span data-ttu-id="da3c9-169">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="da3c9-169">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="da3c9-170">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="da3c9-170">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="da3c9-171">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="da3c9-171">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="da3c9-172">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="da3c9-172">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="da3c9-173">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="da3c9-173">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="da3c9-174">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="da3c9-174">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="da3c9-175">Jetgrowdatabase</span><span class="sxs-lookup"><span data-stu-id="da3c9-175">JetGrowDatabase</span></span>](./jetgrowdatabase-function.md)
