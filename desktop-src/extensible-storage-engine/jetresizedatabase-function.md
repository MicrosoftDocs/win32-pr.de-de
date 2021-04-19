---
description: 'Weitere Informationen zu: jetresizedatabase-Funktion'
title: Jetresizedatabase-Funktion
TOCTitle: JetResizeDatabase Function
ms:assetid: b6420de7-acff-480e-838b-f0e5acc29c65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835047(v=EXCHG.10)
ms:contentKeyID: 49894669
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetResizeDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dadaa7eaa310c5b3a6a2730d316218bc2607d100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362749"
---
# <a name="jetresizedatabase-function"></a><span data-ttu-id="371eb-103">Jetresizedatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="371eb-103">JetResizeDatabase Function</span></span>


<span data-ttu-id="371eb-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="371eb-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="371eb-105">Die **jetresizedatabase** -Funktion erweitert oder verkleinert die Größe einer Datenbank, die derzeit geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="371eb-105">The **JetResizeDatabase** function extends or shrinks the size of a database that is currently open.</span></span>

<span data-ttu-id="371eb-106">Die **jetresizedatabase** -Funktion wurde im Windows 8-Betriebssystem eingeführt.</span><span class="sxs-lookup"><span data-stu-id="371eb-106">The **JetResizeDatabase** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetResizeDatabase(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          unsigned long cpg,
  __out         unsigned long* pcpgActual,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="371eb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="371eb-107">Parameters</span></span>

<span data-ttu-id="371eb-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="371eb-108">*sesid*</span></span>

<span data-ttu-id="371eb-109">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="371eb-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="371eb-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="371eb-110">*dbid*</span></span>

<span data-ttu-id="371eb-111">Die Datenbank, die erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="371eb-111">The database that will be extended.</span></span>

<span data-ttu-id="371eb-112">*Verbrauchsgüter*</span><span class="sxs-lookup"><span data-stu-id="371eb-112">*cpg*</span></span>

<span data-ttu-id="371eb-113">Die angeforderte Größe der Datenbank in Seiten.</span><span class="sxs-lookup"><span data-stu-id="371eb-113">The requested size of the database, in pages.</span></span>

<span data-ttu-id="371eb-114">*pcpgactual*</span><span class="sxs-lookup"><span data-stu-id="371eb-114">*pcpgActual*</span></span>

<span data-ttu-id="371eb-115">Ein Zeiger auf eine Zahl, die die Größe der Datenbank in Seiten nach dem API-Befehl erhält.</span><span class="sxs-lookup"><span data-stu-id="371eb-115">A pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="371eb-116">Wenn der API-Rückruf fehlschlägt, ist der Inhalt des *pcpgactual* -Parameters nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="371eb-116">If the API call fails, the contents of *pcpgActual* parameter are undefined.</span></span>

<span data-ttu-id="371eb-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="371eb-117">*grbit*</span></span>

<span data-ttu-id="371eb-118">Eine Gruppe von Bits, die 0 (null) oder mehr der in der folgenden Tabelle aufgeführten Werte angibt.</span><span class="sxs-lookup"><span data-stu-id="371eb-118">A group of bits that specifies zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="371eb-119">Wert</span><span class="sxs-lookup"><span data-stu-id="371eb-119">Value</span></span></p></th>
<th><p><span data-ttu-id="371eb-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="371eb-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="371eb-121">JET_bitResizeDatabaseOnlyGrow</span><span class="sxs-lookup"><span data-stu-id="371eb-121">JET_bitResizeDatabaseOnlyGrow</span></span></p></td>
<td><p><span data-ttu-id="371eb-122">Vergrößern Sie nur die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="371eb-122">Only grow the database.</span></span> <span data-ttu-id="371eb-123">Wenn der Größenänderung die Datenbank verkleinern würde, führen Sie keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="371eb-123">If the resize call would shrink the database, do nothing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="371eb-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="371eb-124">Return value</span></span>

<span data-ttu-id="371eb-125">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der in der folgenden Tabelle aufgelisteten Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="371eb-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the return codes listed in the following table.</span></span> <span data-ttu-id="371eb-126">Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Fehler Behandlungsparameter](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="371eb-126">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="371eb-127">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="371eb-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="371eb-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="371eb-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="371eb-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="371eb-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="371eb-130">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="371eb-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="371eb-131">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="371eb-131">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="371eb-132">Auf dem Volume ist nicht genügend freier Speicherplatz vorhanden, um die Vergrößerung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="371eb-132">There is insufficient free space on the volume to perform the grow operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="371eb-133">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="371eb-133">JET_errDiskIO</span></span></p></td>
<td><p><span data-ttu-id="371eb-134">Von der <a href="gg269242(v=exchg.10).md">jetsetdatabasesize</a> -Funktion wurde ein Datei bezogener Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="371eb-134">A file-related error was returned by the <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a> function.</span></span> <span data-ttu-id="371eb-135">Weitere Informationen zu anderen Datei bezogenen Fehlern, die zurückgegeben werden können, finden Sie unter <a href="gg269242(v=exchg.10).md">jetsetdatabasesize</a>.</span><span class="sxs-lookup"><span data-stu-id="371eb-135">For more information about other file-related errors that might be returned, see <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="371eb-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="371eb-136">Remarks</span></span>

<span data-ttu-id="371eb-137">Wenn die **jetresizedatabase** -Funktion vor dem Einfügen großer Datenmengen aufgerufen wird, wird die Datenbankdatei in einem Vorgang vergrößert.</span><span class="sxs-lookup"><span data-stu-id="371eb-137">If the **JetResizeDatabase** function is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="371eb-138">Dadurch wird die Wahrscheinlichkeit verringert, dass die Datenbankdatei auf Dateisystem Ebene fragmentiert wird. Außerdem wird die Häufigkeit reduziert, mit der die Datenbankdatei vergrößert werden muss.</span><span class="sxs-lookup"><span data-stu-id="371eb-138">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="371eb-139">Wenn Sie die Datenbankdatei einmal vergrößern, kann Sie schneller sein, als Sie mehrmals anwachsen.</span><span class="sxs-lookup"><span data-stu-id="371eb-139">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="371eb-140">Informationen zum Festlegen der Größe einer Datenbank, die nicht geöffnet wird, finden Sie unter [jetsetdatabasesize](./jetsetdatabasesize-function.md).</span><span class="sxs-lookup"><span data-stu-id="371eb-140">To set the size of a database that is not opened, see [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span></span>

<span data-ttu-id="371eb-141">Die Dateigröße stimmt möglicherweise nicht mit der Anzahl der Seiten, die im *pcpgreal* -Parameter zurückgegeben werden, ab.</span><span class="sxs-lookup"><span data-stu-id="371eb-141">The file size might not match the number of pages that are returned in the *pcpgReal* parameter.</span></span> <span data-ttu-id="371eb-142">Zwei weitere reservierte Seiten können im *pcpgreal* -Parameter nicht gezählt werden.</span><span class="sxs-lookup"><span data-stu-id="371eb-142">Two additional reserved pages might not be counted in the *pcpgReal* parameter.</span></span>

#### <a name="requirements"></a><span data-ttu-id="371eb-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="371eb-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="371eb-144"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="371eb-144"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="371eb-145">Erfordert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="371eb-145">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="371eb-146"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="371eb-146"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="371eb-147">Erfordert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="371eb-147">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="371eb-148"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="371eb-148"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="371eb-149">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="371eb-149">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="371eb-150"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="371eb-150"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="371eb-151">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="371eb-151">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="371eb-152"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="371eb-152"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="371eb-153">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="371eb-153">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="371eb-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="371eb-154">See also</span></span>

[<span data-ttu-id="371eb-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="371eb-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="371eb-156">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="371eb-156">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="371eb-157">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="371eb-157">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="371eb-158">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="371eb-158">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="371eb-159">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="371eb-159">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="371eb-160">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="371eb-160">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="371eb-161">Jetsetdatabasesize</span><span class="sxs-lookup"><span data-stu-id="371eb-161">JetSetDatabaseSize</span></span>](./jetsetdatabasesize-function.md)
