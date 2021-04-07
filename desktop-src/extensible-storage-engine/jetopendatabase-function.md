---
description: 'Weitere Informationen zu: jetopendatabase-Funktion'
title: JetOpenDatabase-Funktion
TOCTitle: JetOpenDatabase Function
ms:assetid: 7764f0c2-6795-4b93-be3d-f6830cdce369
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269299(v=EXCHG.10)
ms:contentKeyID: 32765591
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenDatabase
- JetOpenDatabaseW
- JetOpenDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3492a037ac0c52a78bbe3265bd629969c301771c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760537"
---
# <a name="jetopendatabase-function"></a><span data-ttu-id="884ff-103">JetOpenDatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="884ff-103">JetOpenDatabase Function</span></span>


<span data-ttu-id="884ff-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="884ff-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopendatabase-function"></a><span data-ttu-id="884ff-105">JetOpenDatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="884ff-105">JetOpenDatabase Function</span></span>

<span data-ttu-id="884ff-106">Die **jetopendatabase** -Funktion öffnet eine zuvor angefügte Datenbank mithilfe der [jetattachdatabase](./jetattachdatabase-function.md) -Funktion oder der [JetAttachDatabase2](./jetattachdatabase2-function.md) -Funktion für die Verwendung mit einer Daten banksitzung.</span><span class="sxs-lookup"><span data-stu-id="884ff-106">The **JetOpenDatabase** function opens a previously attached database, using the [JetAttachDatabase](./jetattachdatabase-function.md) or [JetAttachDatabase2](./jetattachdatabase2-function.md) functions, for use with a database session.</span></span> <span data-ttu-id="884ff-107">Diese Funktion kann für dieselbe Datenbank mehrmals aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="884ff-107">This function can be called multiple times for the same database.</span></span>

```cpp
    JET_ERR JET_API JetOpenDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in_opt      const tchar* szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="884ff-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="884ff-108">Parameters</span></span>

<span data-ttu-id="884ff-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="884ff-109">*sesid*</span></span>

<span data-ttu-id="884ff-110">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="884ff-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="884ff-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="884ff-111">*szFilename*</span></span>

<span data-ttu-id="884ff-112">Der Name der Datenbank, die geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="884ff-112">The name of the database to open.</span></span>

<span data-ttu-id="884ff-113">*szconnect*</span><span class="sxs-lookup"><span data-stu-id="884ff-113">*szConnect*</span></span>

<span data-ttu-id="884ff-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="884ff-114">Reserved.</span></span> <span data-ttu-id="884ff-115">Auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="884ff-115">Set to NULL.</span></span>

<span data-ttu-id="884ff-116">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="884ff-116">*pdbid*</span></span>

<span data-ttu-id="884ff-117">Ein Zeiger auf einen Puffer, der bei einem erfolgreichen-Aufrufwert den Bezeichner der Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="884ff-117">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="884ff-118">Wenn der-Befehl fehlschlägt, ist der Wert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="884ff-118">If the call fails, the value is undefined.</span></span>

<span data-ttu-id="884ff-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="884ff-119">*grbit*</span></span>

<span data-ttu-id="884ff-120">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angeben.</span><span class="sxs-lookup"><span data-stu-id="884ff-120">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="884ff-121">Wert</span><span class="sxs-lookup"><span data-stu-id="884ff-121">Value</span></span></p></th>
<th><p><span data-ttu-id="884ff-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="884ff-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="884ff-123">JET_bitDbExclusive</span><span class="sxs-lookup"><span data-stu-id="884ff-123">JET_bitDbExclusive</span></span></p></td>
<td><p><span data-ttu-id="884ff-124">Ermöglicht nur einer einzelnen Sitzung das Anfügen einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="884ff-124">Allows only a single session to attach a database.</span></span> <span data-ttu-id="884ff-125">In der Regel können mehrere Sitzungen eine Datenbank öffnen.</span><span class="sxs-lookup"><span data-stu-id="884ff-125">Normally, several sessions can open a database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="884ff-126">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="884ff-126">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="884ff-127">Verhindert Änderungen an der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="884ff-127">Prevents modifications to the database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="884ff-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="884ff-128">Return Value</span></span>

<span data-ttu-id="884ff-129">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="884ff-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="884ff-130">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="884ff-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="884ff-131">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="884ff-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="884ff-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="884ff-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="884ff-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="884ff-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="884ff-134">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="884ff-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="884ff-135">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="884ff-135">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="884ff-136">Exklusiver Zugriff wurde angefordert, konnte aber nicht erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="884ff-136">Exclusive access was requested, but could not be granted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="884ff-137">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="884ff-137">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="884ff-138">In " <em>szFilename</em>" wurde ein ungültiger Pfad angegeben.</span><span class="sxs-lookup"><span data-stu-id="884ff-138">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="884ff-139">" <em>szFilename</em> " darf nicht NULL sein und muss auf eine gültige Datei verweisen.</span><span class="sxs-lookup"><span data-stu-id="884ff-139"><em>szFilename</em> must be non-NULL and refer to a valid file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="884ff-140">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="884ff-140">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="884ff-141">Eine andere Sitzung hat die Datenbank bereits exklusiv (mit JET_bitDbExclusive) geöffnet.</span><span class="sxs-lookup"><span data-stu-id="884ff-141">Another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="884ff-142">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="884ff-142">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="884ff-143">Die Datenbank wurde zuvor nicht angefügt (siehe <a href="gg294074(v=exchg.10).md">jetattachdatabase</a>).</span><span class="sxs-lookup"><span data-stu-id="884ff-143">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="884ff-144">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="884ff-144">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="884ff-145">Es wurde versucht, eine Datei zu öffnen, die keine gültige Datenbankdatei ist.</span><span class="sxs-lookup"><span data-stu-id="884ff-145">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="884ff-146">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="884ff-146">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="884ff-147">Es wurde versucht, mehr als eine Datenbank zu öffnen, und <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> wurde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="884ff-147">An attempt was made to open more than one database, and <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> was set.</span></span> <span data-ttu-id="884ff-148">Weitere Informationen finden Sie unter <a href="gg294139(v=exchg.10).md">System Parameter</a>.</span><span class="sxs-lookup"><span data-stu-id="884ff-148">For more information, see <a href="gg294139(v=exchg.10).md">System Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="884ff-149">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="884ff-149">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="884ff-150">Die Datei wurde als schreibgeschützt angefügt, aber <strong>jetopsdatabase</strong> hat JET_bitDbReadOnly nicht bestanden.</span><span class="sxs-lookup"><span data-stu-id="884ff-150">The file was attached as read-only, but <strong>JetOpenDatabase</strong> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="884ff-151">Die Datenbank wird immer noch mit Schreib geschütztem Zugriff geöffnet.</span><span class="sxs-lookup"><span data-stu-id="884ff-151">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="884ff-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="884ff-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="884ff-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="884ff-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="884ff-154">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="884ff-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="884ff-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="884ff-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="884ff-156">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="884ff-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="884ff-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="884ff-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="884ff-158">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="884ff-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="884ff-159"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="884ff-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="884ff-160">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="884ff-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="884ff-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="884ff-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="884ff-162">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="884ff-162">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="884ff-163"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="884ff-163"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="884ff-164">Implementiert als <strong>jetopendatabasew</strong> (Unicode) und <strong>jetopendatabasea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="884ff-164">Implemented as <strong>JetOpenDatabaseW</strong> (Unicode) and <strong>JetOpenDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="884ff-165">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="884ff-165">See Also</span></span>

[<span data-ttu-id="884ff-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="884ff-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="884ff-167">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="884ff-167">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="884ff-168">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="884ff-168">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="884ff-169">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="884ff-169">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="884ff-170">Jetattachdatabase</span><span class="sxs-lookup"><span data-stu-id="884ff-170">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="884ff-171">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="884ff-171">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="884ff-172">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="884ff-172">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="884ff-173">System Parameter</span><span class="sxs-lookup"><span data-stu-id="884ff-173">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
