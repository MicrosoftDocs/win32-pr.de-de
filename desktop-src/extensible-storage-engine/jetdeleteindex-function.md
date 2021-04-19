---
description: 'Weitere Informationen zu: jetdelta eteindex-Funktion'
title: Jetdelta eteindex-Funktion
TOCTitle: JetDeleteIndex Function
ms:assetid: c540503b-d5a6-47f2-9113-9650891c4b6d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294081(v=EXCHG.10)
ms:contentKeyID: 32765696
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteIndexW
- JetDeleteIndexA
- JetDeleteIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52a29e619d6643df4984bd7f296dcef4ef0a5ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106361701"
---
# <a name="jetdeleteindex-function"></a><span data-ttu-id="40f27-103">Jetdelta eteindex-Funktion</span><span class="sxs-lookup"><span data-stu-id="40f27-103">JetDeleteIndex Function</span></span>


<span data-ttu-id="40f27-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="40f27-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeleteindex-function"></a><span data-ttu-id="40f27-105">Jetdelta eteindex-Funktion</span><span class="sxs-lookup"><span data-stu-id="40f27-105">JetDeleteIndex Function</span></span>

<span data-ttu-id="40f27-106">Die **jetdelta eteindex** -Funktion löscht einen Index aus einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="40f27-106">The **JetDeleteIndex** function deletes an index from a table.</span></span>

```cpp
    JET_ERR JET_API JetDeleteIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="40f27-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="40f27-107">Parameters</span></span>

<span data-ttu-id="40f27-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="40f27-108">*sesid*</span></span>

<span data-ttu-id="40f27-109">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="40f27-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="40f27-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="40f27-110">*tableid*</span></span>

<span data-ttu-id="40f27-111">Die Tabelle, die die Spalte enthält, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="40f27-111">The table that contains the column that is to be deleted.</span></span>

<span data-ttu-id="40f27-112">*szindexname*</span><span class="sxs-lookup"><span data-stu-id="40f27-112">*szIndexName*</span></span>

<span data-ttu-id="40f27-113">Der Name des zu löschenden Indexes.</span><span class="sxs-lookup"><span data-stu-id="40f27-113">The name of the index to be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="40f27-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40f27-114">Return Value</span></span>

<span data-ttu-id="40f27-115">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="40f27-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="40f27-116">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="40f27-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40f27-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="40f27-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="40f27-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40f27-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40f27-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="40f27-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="40f27-120">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="40f27-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f27-121">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="40f27-121">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="40f27-122">Es wurde versucht, einen Index aus einer Tabelle mit fester Größe (z. b. mit JET_bitTableCreateFixedDDL erstellt) zu löschen.</span><span class="sxs-lookup"><span data-stu-id="40f27-122">An attempt was made to delete an index from a fixed table (for example, one created with JET_bitTableCreateFixedDDL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f27-123">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="40f27-123">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="40f27-124">Es wurde versucht, einen Index aus einer Vorlagen Tabelle zu löschen.</span><span class="sxs-lookup"><span data-stu-id="40f27-124">An attempt was made to delete an index from a template table.</span></span> <span data-ttu-id="40f27-125">Eine Vorlagen Tabelle verfügt über eine festgelegte DDL.</span><span class="sxs-lookup"><span data-stu-id="40f27-125">A template table has fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f27-126">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="40f27-126">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="40f27-127">Der in <em>szindexname</em> benannte Index wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="40f27-127">The index named in <em>szIndexName</em> was not found.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f27-128">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="40f27-128">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="40f27-129">Die Tabelle kann nicht aktualisiert werden, da sie schreibgeschützt geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="40f27-129">The table cannot be updated because it was opened read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f27-130">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="40f27-130">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="40f27-131">Mehrere Threads haben versucht, dieselbe Daten banksitzung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="40f27-131">Multiple threads attempted to use the same database session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f27-132">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="40f27-132">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="40f27-133">Die Transaktion wurde als schreibgeschützte Transaktion geöffnet.</span><span class="sxs-lookup"><span data-stu-id="40f27-133">The transaction was opened as a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="40f27-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40f27-134">Remarks</span></span>

<span data-ttu-id="40f27-135">Bei erfolgreicher Ausführung wird der Index gelöscht und kann daher nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40f27-135">When successful, the index is deleted and therefore cannot be used subsequently.</span></span> <span data-ttu-id="40f27-136">Es darf keine aktive Transaktion vorhanden sein, die den Index verwendet.</span><span class="sxs-lookup"><span data-stu-id="40f27-136">There must not be any active transaction using the index.</span></span>

<span data-ttu-id="40f27-137">Bei Erfolg wird die Währung vor dem ersten Datensatz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="40f27-137">On success, the currency is set before the first record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="40f27-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40f27-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40f27-139"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="40f27-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="40f27-140">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="40f27-140">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f27-141"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="40f27-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="40f27-142">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="40f27-142">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f27-143"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="40f27-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="40f27-144">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="40f27-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f27-145"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="40f27-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="40f27-146">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="40f27-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f27-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="40f27-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="40f27-148">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="40f27-148">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f27-149"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="40f27-149"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="40f27-150">Implementiert als <strong>jetdelta eteindexw</strong> (Unicode) und <strong>jetdelta-eindexa</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="40f27-150">Implemented as <strong>JetDeleteIndexW</strong> (Unicode) and <strong>JetDeleteIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="40f27-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="40f27-151">See Also</span></span>

[<span data-ttu-id="40f27-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="40f27-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="40f27-153">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="40f27-153">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="40f27-154">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="40f27-154">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="40f27-155">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="40f27-155">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="40f27-156">Jetkreateingedex</span><span class="sxs-lookup"><span data-stu-id="40f27-156">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="40f27-157">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="40f27-157">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)
