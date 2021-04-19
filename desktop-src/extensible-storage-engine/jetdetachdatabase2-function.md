---
description: 'Weitere Informationen finden Sie hier: JetDetachDatabase2-Funktion'
title: JetDetachDatabase2-Funktion
TOCTitle: JetDetachDatabase2 Function
ms:assetid: d79c06ab-d470-4d83-a0f4-fa0f4e5f80b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294105(v=EXCHG.10)
ms:contentKeyID: 32765720
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabase2
- JetDetachDatabase2W
- JetDetachDatabase2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7688df9a18d8e13a85e4a244fc8502a7147e154f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362839"
---
# <a name="jetdetachdatabase2-function"></a><span data-ttu-id="d1a55-103">JetDetachDatabase2-Funktion</span><span class="sxs-lookup"><span data-stu-id="d1a55-103">JetDetachDatabase2 Function</span></span>


<span data-ttu-id="d1a55-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d1a55-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdetachdatabase2-function"></a><span data-ttu-id="d1a55-105">JetDetachDatabase2-Funktion</span><span class="sxs-lookup"><span data-stu-id="d1a55-105">JetDetachDatabase2 Function</span></span>

<span data-ttu-id="d1a55-106">Die **JetDetachDatabase2** -Funktion gibt eine Datenbankdatei frei, die zuvor an eine Daten banksitzung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="d1a55-106">The **JetDetachDatabase2** function releases a database file that was previously attached to a database session.</span></span>

<span data-ttu-id="d1a55-107">**Windows XP:**  **JetDetachDatabase2** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d1a55-107">**Windows XP:**  **JetDetachDatabase2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetDetachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="d1a55-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1a55-108">Parameters</span></span>

<span data-ttu-id="d1a55-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="d1a55-109">*sesid*</span></span>

<span data-ttu-id="d1a55-110">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="d1a55-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="d1a55-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="d1a55-111">*szFilename*</span></span>

<span data-ttu-id="d1a55-112">Der Name der zu trennenden Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d1a55-112">The name of the database to detach.</span></span> <span data-ttu-id="d1a55-113">Wenn *szFilename* **null** oder eine leere Zeichenfolge ist, werden alle an die " *gsid* " angefügten Datenbanken getrennt.</span><span class="sxs-lookup"><span data-stu-id="d1a55-113">If *szFilename* is **NULL** or an empty string, all databases attached to *sesid* will be detached.</span></span>

<span data-ttu-id="d1a55-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d1a55-114">*grbit*</span></span>

<span data-ttu-id="d1a55-115">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="d1a55-115">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d1a55-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d1a55-116">Value</span></span></p></th>
<th><p><span data-ttu-id="d1a55-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d1a55-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1a55-118">JET_bitForceCloseAndDetach</span><span class="sxs-lookup"><span data-stu-id="d1a55-118">JET_bitForceCloseAndDetach</span></span></p></td>
<td><p><span data-ttu-id="d1a55-119">Erzwingt, dass die Datenbank geschlossen und getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="d1a55-119">Forces the database to be closed and detached.</span></span> <span data-ttu-id="d1a55-120">Wird JET_bitForceCloseAndDetach nicht unterstützt, wird JET_errForceDetachNotAllowed zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d1a55-120">If JET_bitForceCloseAndDetach is not supported, JET_errForceDetachNotAllowed will be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1a55-121">JET_bitForceDetach</span><span class="sxs-lookup"><span data-stu-id="d1a55-121">JET_bitForceDetach</span></span></p></td>
<td><p><span data-ttu-id="d1a55-122">Erzwingt, dass die Datenbank getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="d1a55-122">Forces the database to be detached.</span></span> <span data-ttu-id="d1a55-123">Wird JET_bitForceDetach nicht unterstützt, wird JET_errForceDetachNotAllowed zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d1a55-123">If JET_bitForceDetach is not supported, JET_errForceDetachNotAllowed will be returned.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d1a55-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1a55-124">Return Value</span></span>

<span data-ttu-id="d1a55-125">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="d1a55-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d1a55-126">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d1a55-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d1a55-127">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d1a55-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="d1a55-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1a55-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1a55-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d1a55-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d1a55-130">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d1a55-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1a55-131">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="d1a55-131">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="d1a55-132">Die Datenbank wird gesichert und kann nicht getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="d1a55-132">The database is being backed up, and cannot be detached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1a55-133">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="d1a55-133">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="d1a55-134">Die Datenbank wurde von <a href="gg269299(v=exchg.10).md">jetopbank</a>geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d1a55-134">The database has been opened by <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span></span> <span data-ttu-id="d1a55-135">Datenbanken müssen vor dem Trennen geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="d1a55-135">Databases must be closed prior to detaching.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1a55-136">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="d1a55-136">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="d1a55-137">Die Datenbank war zuvor nicht angefügt (siehe <a href="gg294074(v=exchg.10).md">jetattachdatabase</a> oder <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span><span class="sxs-lookup"><span data-stu-id="d1a55-137">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> or <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1a55-138">JET_errForceDetachNotAllowed</span><span class="sxs-lookup"><span data-stu-id="d1a55-138">JET_errForceDetachNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="d1a55-139">JET_bitForceDetach wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d1a55-139">JET_bitForceDetach is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1a55-140">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="d1a55-140">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="d1a55-141">Es wurde versucht, eine Datenbank zu trennen, während eine Transaktion durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="d1a55-141">An attempt was made to detach a database while in a transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="d1a55-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1a55-142">Remarks</span></span>

<span data-ttu-id="d1a55-143">Wenn eine angefügte Datenbank (mit [jetattachdatabase](./jetattachdatabase-function.md)) geöffnet wurde, muss Sie vor dem trennen mit [jetclosedatabase](./jetclosedatabase-function.md) geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="d1a55-143">If an attached database was opened (with [JetAttachDatabase](./jetattachdatabase-function.md)), it must be closed with [JetCloseDatabase](./jetclosedatabase-function.md) prior to detaching.</span></span>

<span data-ttu-id="d1a55-144">Nur Windows 2000: Datenbanken, die vor dem Aufrufen von [jetterm](./jetterm-function.md) nicht getrennt wurden, werden automatisch erneut angefügt, wenn [jetinit das](./jetinit-function.md) nächste Mal aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d1a55-144">Windows 2000 only: Databases which have not been detached prior to calling [JetTerm](./jetterm-function.md) will automatically be re-attached when [JetInit](./jetinit-function.md) is next called.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d1a55-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1a55-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1a55-146"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d1a55-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d1a55-147">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d1a55-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1a55-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d1a55-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d1a55-149">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d1a55-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1a55-150"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d1a55-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d1a55-151">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="d1a55-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1a55-152"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="d1a55-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d1a55-153">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d1a55-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1a55-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d1a55-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d1a55-155">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d1a55-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1a55-156"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="d1a55-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="d1a55-157">Implementiert als <strong>JetDetachDatabase2W</strong> (Unicode) und <strong>JetDetachDatabase2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="d1a55-157">Implemented as <strong>JetDetachDatabase2W</strong> (Unicode) and <strong>JetDetachDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d1a55-158">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d1a55-158">See Also</span></span>

[<span data-ttu-id="d1a55-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d1a55-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d1a55-160">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d1a55-160">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d1a55-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d1a55-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d1a55-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d1a55-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d1a55-163">Jetattachdatabase</span><span class="sxs-lookup"><span data-stu-id="d1a55-163">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="d1a55-164">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="d1a55-164">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="d1a55-165">Jetclosedatabase</span><span class="sxs-lookup"><span data-stu-id="d1a55-165">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="d1a55-166">Jetkreatedatabase</span><span class="sxs-lookup"><span data-stu-id="d1a55-166">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="d1a55-167">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="d1a55-167">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="d1a55-168">JetInit</span><span class="sxs-lookup"><span data-stu-id="d1a55-168">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="d1a55-169">Jetopumdatabase</span><span class="sxs-lookup"><span data-stu-id="d1a55-169">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="d1a55-170">Jetterm</span><span class="sxs-lookup"><span data-stu-id="d1a55-170">JetTerm</span></span>](./jetterm-function.md)
