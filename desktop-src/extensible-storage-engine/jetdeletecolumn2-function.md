---
description: 'Weitere Informationen finden Sie hier: JetDeleteColumn2-Funktion'
title: JetDeleteColumn2-Funktion
TOCTitle: JetDeleteColumn2 Function
ms:assetid: 840b5acd-8bbf-4524-9741-5d74e3427329
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269320(v=EXCHG.10)
ms:contentKeyID: 32765610
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumn2
- JetDeleteColumn2A
- JetDeleteColumn2W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35e19eb7ac7b133bb690b268426fec9822efefea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366507"
---
# <a name="jetdeletecolumn2-function"></a><span data-ttu-id="d707f-103">JetDeleteColumn2-Funktion</span><span class="sxs-lookup"><span data-stu-id="d707f-103">JetDeleteColumn2 Function</span></span>


<span data-ttu-id="d707f-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d707f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletecolumn2-function"></a><span data-ttu-id="d707f-105">JetDeleteColumn2-Funktion</span><span class="sxs-lookup"><span data-stu-id="d707f-105">JetDeleteColumn2 Function</span></span>

<span data-ttu-id="d707f-106">Die **JetDeleteColumn2** -Funktion löscht eine Spalte aus einer ESE-Datenbanktabelle und ermöglicht die Festlegung einer *grbit* -Option.</span><span class="sxs-lookup"><span data-stu-id="d707f-106">The **JetDeleteColumn2** function deletes a column from an ESE database table and enables a *grbit* option to be set.</span></span>

<span data-ttu-id="d707f-107">**Windows XP: JetDeleteColumn2** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d707f-107">**Windows XP:  JetDeleteColumn2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetDeleteColumn2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szColumnName,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="d707f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d707f-108">Parameters</span></span>

<span data-ttu-id="d707f-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="d707f-109">*sesid*</span></span>

<span data-ttu-id="d707f-110">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="d707f-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="d707f-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="d707f-111">*tableid*</span></span>

<span data-ttu-id="d707f-112">Die Tabelle, die die zu löschende Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="d707f-112">The table that contains the column to be deleted.</span></span>

<span data-ttu-id="d707f-113">*szcolumnname*</span><span class="sxs-lookup"><span data-stu-id="d707f-113">*szColumnName*</span></span>

<span data-ttu-id="d707f-114">Der Name der zu löschenden Spalte.</span><span class="sxs-lookup"><span data-stu-id="d707f-114">The name of the column to be deleted.</span></span>

<span data-ttu-id="d707f-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d707f-115">*grbit*</span></span>

<span data-ttu-id="d707f-116">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="d707f-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d707f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d707f-117">Value</span></span></p></th>
<th><p><span data-ttu-id="d707f-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d707f-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d707f-119">JET_bitDeleteColumnIgnoreTemplateColumns</span><span class="sxs-lookup"><span data-stu-id="d707f-119">JET_bitDeleteColumnIgnoreTemplateColumns</span></span></p></td>
<td><p><span data-ttu-id="d707f-120">Das Festlegen von JET_bitDeleteColumIgnoreTemplateColumns bewirkt, dass die API nur versucht, Spalten in der abgeleiteten Tabelle zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d707f-120">Setting JET_bitDeleteColumIgnoreTemplateColumns will cause the API to only attempt to delete columns in the derived table.</span></span> <span data-ttu-id="d707f-121">Wenn eine Spalte mit diesem Namen in der Basistabelle vorhanden ist, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d707f-121">If a column of that name exists in the base table it will be ignored.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d707f-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d707f-122">Return Value</span></span>

<span data-ttu-id="d707f-123">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="d707f-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d707f-124">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d707f-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d707f-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d707f-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="d707f-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d707f-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d707f-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d707f-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d707f-128">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d707f-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d707f-129">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="d707f-129">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="d707f-130">Die Spalte wird derzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="d707f-130">The column is currently in use.</span></span> <span data-ttu-id="d707f-131">Sie kann derzeit von einem Index verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d707f-131">It may be currently used by an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d707f-132">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="d707f-132">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="d707f-133">Es wurde versucht, die festgelegte DDL zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d707f-133">An attempt was made to modify the fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d707f-134">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="d707f-134">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="d707f-135">Die in <em>szcolumnname</em> genannte Spalte ist in der Vorlagen Tabelle vorhanden, und die DDL einer Vorlagen Tabelle kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d707f-135">The column named in <em>szColumnName</em> exists in the template table, and the DDL of a template table cannot be modified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d707f-136">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="d707f-136">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="d707f-137">Dieser Fehler kann zurückgegeben werden, wenn ein ungültiger Name für <em>szcolumnname</em> angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="d707f-137">This may be returned if a bad name for <em>szColumnName</em> was given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d707f-138">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="d707f-138">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="d707f-139">Die Tabelle ist nicht beschreibbar.</span><span class="sxs-lookup"><span data-stu-id="d707f-139">The table is not writable.</span></span> <span data-ttu-id="d707f-140">Dies kann zurückgegeben werden, wenn die Datenbank im schreibgeschützten Modus geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="d707f-140">This may get returned if the database was opened in read-only mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d707f-141">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="d707f-141">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="d707f-142">Bei der Transaktion handelt es sich um eine schreibgeschützte Transaktion.</span><span class="sxs-lookup"><span data-stu-id="d707f-142">The transaction is a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="d707f-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d707f-143">Remarks</span></span>

<span data-ttu-id="d707f-144">Der Aufruf von [jetdeletecolumn](./jetdeletecolumn-function.md) ist mit dem Aufrufen von **JetDeleteColumn2** identisch, wobei *grbit* auf NULL (0) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d707f-144">Calling [JetDeleteColumn](./jetdeletecolumn-function.md) is identical to calling **JetDeleteColumn2** with *grbit* set to zero (0).</span></span>

#### <a name="requirements"></a><span data-ttu-id="d707f-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d707f-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d707f-146"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d707f-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d707f-147">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d707f-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d707f-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d707f-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d707f-149">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d707f-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d707f-150"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d707f-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d707f-151">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="d707f-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d707f-152"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="d707f-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d707f-153">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d707f-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d707f-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d707f-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d707f-155">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d707f-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d707f-156"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="d707f-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="d707f-157">Implementiert als <strong>JetDeleteColumn2W</strong> (Unicode) und <strong>JetDeleteColumn2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="d707f-157">Implemented as <strong>JetDeleteColumn2W</strong> (Unicode) and <strong>JetDeleteColumn2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d707f-158">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d707f-158">See Also</span></span>

[<span data-ttu-id="d707f-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d707f-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d707f-160">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d707f-160">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d707f-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d707f-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d707f-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d707f-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d707f-163">Jetdeletecolumn</span><span class="sxs-lookup"><span data-stu-id="d707f-163">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)
