---
description: 'Weitere Informationen finden Sie unter: jetdeletecolumn-Funktion'
title: Jetdeletecolumn-Funktion
TOCTitle: JetDeleteColumn Function
ms:assetid: b2f4be8c-7ea9-4f66-925b-4e9c14d9d475
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294062(v=EXCHG.10)
ms:contentKeyID: 32765677
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumnA
- JetDeleteColumnW
- JetDeleteColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7d577447942e36cd49763727473d3f6ddc659b4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103961777"
---
# <a name="jetdeletecolumn-function"></a><span data-ttu-id="13283-103">Jetdeletecolumn-Funktion</span><span class="sxs-lookup"><span data-stu-id="13283-103">JetDeleteColumn Function</span></span>


<span data-ttu-id="13283-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="13283-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletecolumn-function"></a><span data-ttu-id="13283-105">Jetdeletecolumn-Funktion</span><span class="sxs-lookup"><span data-stu-id="13283-105">JetDeleteColumn Function</span></span>

<span data-ttu-id="13283-106">Die **jetdeletecolumn** -Funktion löscht eine Spalte aus einer ESE-Datenbanktabelle.</span><span class="sxs-lookup"><span data-stu-id="13283-106">The **JetDeleteColumn** function deletes a column from an ESE database table.</span></span>

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a><span data-ttu-id="13283-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="13283-107">Parameters</span></span>

<span data-ttu-id="13283-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="13283-108">*sesid*</span></span>

<span data-ttu-id="13283-109">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="13283-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="13283-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="13283-110">*tableid*</span></span>

<span data-ttu-id="13283-111">Die Tabelle, aus der die Spalte gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="13283-111">The table from which to delete the column.</span></span>

<span data-ttu-id="13283-112">*szcolumnname*</span><span class="sxs-lookup"><span data-stu-id="13283-112">*szColumnName*</span></span>

<span data-ttu-id="13283-113">Der Name der zu löschenden Spalte.</span><span class="sxs-lookup"><span data-stu-id="13283-113">The name of the column to be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="13283-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13283-114">Return Value</span></span>

<span data-ttu-id="13283-115">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="13283-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="13283-116">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="13283-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="13283-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="13283-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="13283-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13283-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13283-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="13283-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="13283-120">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="13283-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13283-121">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="13283-121">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="13283-122">Die Spalte wird derzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="13283-122">The column is currently in use.</span></span> <span data-ttu-id="13283-123">Sie kann derzeit von einem Index verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13283-123">It may be currently used by an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13283-124">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="13283-124">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="13283-125">Es wurde versucht, die festgelegte DDL zu ändern.</span><span class="sxs-lookup"><span data-stu-id="13283-125">An attempt was made to modify the fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13283-126">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="13283-126">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="13283-127">Die in <em>szcolumnname</em> genannte Spalte ist in der Vorlagen Tabelle vorhanden, und die DDL einer Vorlagen Tabelle kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="13283-127">The column named in <em>szColumnName</em> exists in the template table, and the DDL of a template table cannot be modified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13283-128">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="13283-128">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="13283-129">Dieser Fehler kann zurückgegeben werden, wenn ein ungültiger Name für <em>szcolumnname</em> angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="13283-129">This may be returned if a bad name for <em>szColumnName</em> was given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13283-130">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="13283-130">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="13283-131">Die Tabelle ist nicht beschreibbar.</span><span class="sxs-lookup"><span data-stu-id="13283-131">The table is not writable.</span></span> <span data-ttu-id="13283-132">Dies kann zurückgegeben werden, wenn die Datenbank im schreibgeschützten Modus geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="13283-132">This may get returned if the database was opened in read-only mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13283-133">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="13283-133">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="13283-134">Bei der Transaktion handelt es sich um eine schreibgeschützte Transaktion.</span><span class="sxs-lookup"><span data-stu-id="13283-134">The transaction is a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="13283-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13283-135">Remarks</span></span>

<span data-ttu-id="13283-136">Der Aufruf von **jetdeletecolumn** ist mit dem Aufrufen von [JetDeleteColumn2](./jetdeletecolumn2-function.md) identisch, wobei *grbit* auf NULL (0) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="13283-136">Calling **JetDeleteColumn** is identical to calling [JetDeleteColumn2](./jetdeletecolumn2-function.md) with *grbit* set to zero (0).</span></span>

#### <a name="requirements"></a><span data-ttu-id="13283-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13283-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13283-138"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="13283-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="13283-139">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="13283-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13283-140"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="13283-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="13283-141">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="13283-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13283-142"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="13283-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="13283-143">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="13283-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13283-144"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="13283-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="13283-145">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="13283-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13283-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="13283-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="13283-147">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="13283-147">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13283-148"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="13283-148"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="13283-149">Implementiert als <strong>jetdeletecolumnw</strong> (Unicode) und <strong>jetdeletecolumna</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="13283-149">Implemented as <strong>JetDeleteColumnW</strong> (Unicode) and <strong>JetDeleteColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="13283-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="13283-150">See Also</span></span>

[<span data-ttu-id="13283-151">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="13283-151">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="13283-152">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="13283-152">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="13283-153">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="13283-153">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="13283-154">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="13283-154">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="13283-155">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="13283-155">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
