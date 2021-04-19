---
description: 'Weitere Informationen zu: jetgrowdatabase-Funktion'
title: Jetgrowdatabase-Funktion
TOCTitle: JetGrowDatabase Function
ms:assetid: d9719991-6c80-4dcb-a1d6-f0c7de61f459
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294109(v=EXCHG.10)
ms:contentKeyID: 32765724
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGrowDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ed8ee9888a2e4ab7908b72cc071f7b8143ca6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348657"
---
# <a name="jetgrowdatabase-function"></a><span data-ttu-id="fef24-103">Jetgrowdatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="fef24-103">JetGrowDatabase Function</span></span>


<span data-ttu-id="fef24-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fef24-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgrowdatabase-function"></a><span data-ttu-id="fef24-105">Jetgrowdatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="fef24-105">JetGrowDatabase Function</span></span>

<span data-ttu-id="fef24-106">Die **jetgrowdatabase** -Funktion erweitert die Größe einer Datenbank, die derzeit geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="fef24-106">The **JetGrowDatabase** function extends the size of a database that is currently open.</span></span>

```cpp
    JET_ERR JET_API JetGrowDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          unsigned long cpg,
      __in          unsigned long* pcpgReal
    );
```

### <a name="parameters"></a><span data-ttu-id="fef24-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fef24-107">Parameters</span></span>

<span data-ttu-id="fef24-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="fef24-108">*sesid*</span></span>

<span data-ttu-id="fef24-109">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="fef24-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="fef24-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="fef24-110">*dbid*</span></span>

<span data-ttu-id="fef24-111">Die Datenbank, die erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="fef24-111">The database that will be extended.</span></span>

<span data-ttu-id="fef24-112">*Verbrauchsgüter*</span><span class="sxs-lookup"><span data-stu-id="fef24-112">*cpg*</span></span>

<span data-ttu-id="fef24-113">Die gewünschte Größe der Datenbank in Seiten.</span><span class="sxs-lookup"><span data-stu-id="fef24-113">The desired size of the database, in pages.</span></span>

<span data-ttu-id="fef24-114">*pcpgreal*</span><span class="sxs-lookup"><span data-stu-id="fef24-114">*pcpgReal*</span></span>

<span data-ttu-id="fef24-115">Zeiger auf eine Zahl, die die Größe der Datenbank in Seiten nach dem API-Befehl empfängt.</span><span class="sxs-lookup"><span data-stu-id="fef24-115">Pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="fef24-116">Wenn der API-Rückruf fehlschlägt, ist der Inhalt von *pcpgreal* nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="fef24-116">If the API call fails, the contents of *pcpgReal* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="fef24-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fef24-117">Return Value</span></span>

<span data-ttu-id="fef24-118">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="fef24-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="fef24-119">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fef24-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fef24-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fef24-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="fef24-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fef24-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fef24-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fef24-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fef24-123">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="fef24-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fef24-124">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="fef24-124">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="fef24-125">Auf dem Volume ist nicht genügend freier Speicherplatz vorhanden, um die Vergrößerung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="fef24-125">There is insufficient free space on the volume to perform the grow operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fef24-126">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="fef24-126">JET_errDiskIO</span></span></p></td>
<td><p><span data-ttu-id="fef24-127">Von <a href="gg269242(v=exchg.10).md">jetsetdatabasesize</a>wurde ein Datei bezogener Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fef24-127">A file-related error was returned by <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span> <span data-ttu-id="fef24-128">Weitere Informationen zu anderen Datei bezogenen Fehlern, die zurückgegeben werden können, finden Sie unter <a href="gg269242(v=exchg.10).md">jetsetdatabasesize</a>.</span><span class="sxs-lookup"><span data-stu-id="fef24-128">For more information about other file-related errors that might be returned, see <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="fef24-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fef24-129">Remarks</span></span>

<span data-ttu-id="fef24-130">Wenn **jetgrowdatabase** vor dem Einfügen großer Datenmengen aufgerufen wird, wird die Datenbankdatei in einem Vorgang vergrößert.</span><span class="sxs-lookup"><span data-stu-id="fef24-130">If **JetGrowDatabase** is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="fef24-131">Dadurch wird die Wahrscheinlichkeit verringert, dass die Datenbankdatei auf Dateisystem Ebene fragmentiert wird. Außerdem wird die Häufigkeit reduziert, mit der die Datenbankdatei vergrößert werden muss.</span><span class="sxs-lookup"><span data-stu-id="fef24-131">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="fef24-132">Wenn Sie die Datenbankdatei einmal vergrößern, kann Sie schneller sein, als Sie mehrmals anwachsen.</span><span class="sxs-lookup"><span data-stu-id="fef24-132">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="fef24-133">Derzeit wird nur die Vergrößerung der Datei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fef24-133">Only growing the file is currently supported.</span></span> <span data-ttu-id="fef24-134">Um eine Datei zu verkleinern, verwenden Sie die Defragmentierungs Funktion des Programms **esentutl.exe** Hilfsprogramms.</span><span class="sxs-lookup"><span data-stu-id="fef24-134">To shrink a file, use the defragmentation feature of the **esentutl.exe** utility program.</span></span>

<span data-ttu-id="fef24-135">Informationen zum Festlegen der Größe einer Datenbank, die nicht geöffnet wird, finden Sie unter [jetsetdatabasesize](./jetsetdatabasesize-function.md).</span><span class="sxs-lookup"><span data-stu-id="fef24-135">To set the size of a database that is not opened, see [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span></span>

<span data-ttu-id="fef24-136">Die Dateigröße stimmt möglicherweise nicht mit der Anzahl der Seiten, die in *pcpgreal* zurückgegeben werden, ab.</span><span class="sxs-lookup"><span data-stu-id="fef24-136">The file size might not match the number of pages that are returned in *pcpgReal*.</span></span> <span data-ttu-id="fef24-137">Es gibt zwei weitere reservierte Seiten, die möglicherweise nicht in *pcpgreal* gezählt werden.</span><span class="sxs-lookup"><span data-stu-id="fef24-137">There are two additional reserved pages that might not be counted in *pcpgReal*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="fef24-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fef24-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fef24-139"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="fef24-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fef24-140">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="fef24-140">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fef24-141"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="fef24-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fef24-142">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fef24-142">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fef24-143"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="fef24-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fef24-144">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="fef24-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fef24-145"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="fef24-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fef24-146">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="fef24-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fef24-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="fef24-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fef24-148">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="fef24-148">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fef24-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fef24-149">See Also</span></span>

[<span data-ttu-id="fef24-150">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fef24-150">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fef24-151">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fef24-151">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fef24-152">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fef24-152">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="fef24-153">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="fef24-153">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="fef24-154">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="fef24-154">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="fef24-155">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="fef24-155">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="fef24-156">Jetsetdatabasesize</span><span class="sxs-lookup"><span data-stu-id="fef24-156">JetSetDatabaseSize</span></span>](./jetsetdatabasesize-function.md)
