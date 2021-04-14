---
description: 'Weitere Informationen zu: jetdetachdatabase-Funktion'
title: JetDetachDatabase-Funktion
TOCTitle: JetDetachDatabase Function
ms:assetid: 629f19e5-99f3-425a-b6ba-de18daec7efe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269266(v=EXCHG.10)
ms:contentKeyID: 32765568
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabaseW
- JetDetachDatabase
- JetDetachDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e4437955acc0ed5714f7fbfb9f42fd4abafa58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349928"
---
# <a name="jetdetachdatabase-function"></a><span data-ttu-id="2ca37-103">JetDetachDatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="2ca37-103">JetDetachDatabase Function</span></span>


<span data-ttu-id="2ca37-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2ca37-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdetachdatabase-function"></a><span data-ttu-id="2ca37-105">JetDetachDatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="2ca37-105">JetDetachDatabase Function</span></span>

<span data-ttu-id="2ca37-106">Die **jetdetachdatabase** -Funktion gibt eine Datenbankdatei frei, die zuvor an eine Daten banksitzung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="2ca37-106">The **JetDetachDatabase** function releases a database file that was previously attached to a database session.</span></span>

```cpp
    JET_ERR JET_API JetDetachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename
    );
```

### <a name="parameters"></a><span data-ttu-id="2ca37-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ca37-107">Parameters</span></span>

<span data-ttu-id="2ca37-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="2ca37-108">*sesid*</span></span>

<span data-ttu-id="2ca37-109">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="2ca37-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="2ca37-110">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="2ca37-110">*szFilename*</span></span>

<span data-ttu-id="2ca37-111">Der Name der zu trennenden Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2ca37-111">The name of the database to detach.</span></span> <span data-ttu-id="2ca37-112">Wenn *szFilename* **null** oder eine leere Zeichenfolge ist, werden alle an die " *gsid* " angefügten Datenbanken getrennt.</span><span class="sxs-lookup"><span data-stu-id="2ca37-112">If *szFilename* is **NULL** or an empty string, all databases attached to *sesid* will be detached.</span></span>

### <a name="return-value"></a><span data-ttu-id="2ca37-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ca37-113">Return Value</span></span>

<span data-ttu-id="2ca37-114">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="2ca37-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2ca37-115">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2ca37-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2ca37-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2ca37-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="2ca37-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ca37-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ca37-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2ca37-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2ca37-119">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="2ca37-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ca37-120">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="2ca37-120">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="2ca37-121">Die Datenbank wird gesichert und kann nicht getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="2ca37-121">The database is being backed up, and cannot be detached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ca37-122">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="2ca37-122">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="2ca37-123">Die Datenbank wurde von <a href="gg269299(v=exchg.10).md">jetopbank</a>geöffnet.</span><span class="sxs-lookup"><span data-stu-id="2ca37-123">The database has been opened by <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span></span> <span data-ttu-id="2ca37-124">Datenbanken müssen vor dem Trennen geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="2ca37-124">Databases must be closed prior to detaching.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ca37-125">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="2ca37-125">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="2ca37-126">Die Datenbank war zuvor nicht angefügt (siehe <a href="gg294074(v=exchg.10).md">jetattachdatabase</a> oder <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span><span class="sxs-lookup"><span data-stu-id="2ca37-126">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> or <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ca37-127">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="2ca37-127">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="2ca37-128">Es wurde versucht, eine Datenbank zu trennen, während eine Transaktion durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="2ca37-128">An attempt was made to detach a database while in a transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="2ca37-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ca37-129">Remarks</span></span>

<span data-ttu-id="2ca37-130">Wenn eine angefügte Datenbank (mit [jetattachdatabase](./jetattachdatabase-function.md)) geöffnet wurde, muss Sie vor dem trennen mit [jetclosedatabase](./jetclosedatabase-function.md) geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="2ca37-130">If an attached database was opened (with [JetAttachDatabase](./jetattachdatabase-function.md)), it must be closed with [JetCloseDatabase](./jetclosedatabase-function.md) prior to detaching.</span></span>

<span data-ttu-id="2ca37-131">Nur Windows 2000: Datenbanken, die vor dem Aufrufen von [jetterm](./jetterm-function.md) nicht getrennt wurden, werden automatisch erneut angefügt, wenn [jetinit das](./jetinit-function.md) nächste Mal aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2ca37-131">Windows 2000 only: Databases which have not been detached prior to calling [JetTerm](./jetterm-function.md) will automatically be re-attached when [JetInit](./jetinit-function.md) is next called.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2ca37-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ca37-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ca37-133"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2ca37-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2ca37-134">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="2ca37-134">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ca37-135"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2ca37-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2ca37-136">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2ca37-136">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ca37-137"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="2ca37-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2ca37-138">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="2ca37-138">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ca37-139"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="2ca37-139"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2ca37-140">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2ca37-140">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ca37-141"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2ca37-141"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2ca37-142">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2ca37-142">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ca37-143"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="2ca37-143"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="2ca37-144">Implementiert als <strong>jetdetachdatabasew</strong> (Unicode) und <strong>jetdetachdatabasea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="2ca37-144">Implemented as <strong>JetDetachDatabaseW</strong> (Unicode) and <strong>JetDetachDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2ca37-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2ca37-145">See Also</span></span>

[<span data-ttu-id="2ca37-146">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2ca37-146">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2ca37-147">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="2ca37-147">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="2ca37-148">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="2ca37-148">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="2ca37-149">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="2ca37-149">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="2ca37-150">Jetattachdatabase</span><span class="sxs-lookup"><span data-stu-id="2ca37-150">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="2ca37-151">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="2ca37-151">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="2ca37-152">Jetkreatedatabase</span><span class="sxs-lookup"><span data-stu-id="2ca37-152">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="2ca37-153">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="2ca37-153">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="2ca37-154">Jetclosedatabase</span><span class="sxs-lookup"><span data-stu-id="2ca37-154">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="2ca37-155">Jetterm</span><span class="sxs-lookup"><span data-stu-id="2ca37-155">JetTerm</span></span>](./jetterm-function.md)
