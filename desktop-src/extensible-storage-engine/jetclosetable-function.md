---
description: Weitere Informationen finden Sie in der jetclosetable-Funktion.
title: Jetclosetable-Funktion
TOCTitle: JetCloseTable Function
ms:assetid: c8975145-e48a-4029-9522-1509263019ae
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294087(v=EXCHG.10)
ms:contentKeyID: 32765702
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b38ba9b14c34d20b01b6530f2ed3406e55b3bc3f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531100"
---
# <a name="jetclosetable-function"></a><span data-ttu-id="caec2-103">Jetclosetable-Funktion</span><span class="sxs-lookup"><span data-stu-id="caec2-103">JetCloseTable Function</span></span>


<span data-ttu-id="caec2-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="caec2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosetable-function"></a><span data-ttu-id="caec2-105">Jetclosetable-Funktion</span><span class="sxs-lookup"><span data-stu-id="caec2-105">JetCloseTable Function</span></span>

<span data-ttu-id="caec2-106">Die **jetclosetable** -Funktion schließt eine geöffnete Tabelle in einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="caec2-106">The **JetCloseTable** function closes an open table in a database.</span></span> <span data-ttu-id="caec2-107">Bei der Tabelle kann es sich um eine temporäre Tabelle oder eine normale Tabelle handeln.</span><span class="sxs-lookup"><span data-stu-id="caec2-107">The table may be a temporary table or a normal table.</span></span>

```cpp
JET_ERR JET_API JetCloseTable(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid
);
```

### <a name="parameters"></a><span data-ttu-id="caec2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="caec2-108">Parameters</span></span>

<span data-ttu-id="caec2-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="caec2-109">*sesid*</span></span>

<span data-ttu-id="caec2-110">Identifiziert den Daten Bank Sitzungs Kontext, der für den API-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="caec2-110">Identifies the database session context that will be used for the API call.</span></span>

<span data-ttu-id="caec2-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="caec2-111">*tableid*</span></span>

<span data-ttu-id="caec2-112">Identifiziert die Tabelle, die geschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="caec2-112">Identifies the table to be closed.</span></span>

<span data-ttu-id="caec2-113">Legen Sie *TableID* auf JET_tableidNil, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="caec2-113">Set *tableid* to JET_tableidNil to release memory.</span></span>

### <a name="return-value"></a><span data-ttu-id="caec2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="caec2-114">Return Value</span></span>

<span data-ttu-id="caec2-115">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="caec2-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="caec2-116">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="caec2-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="caec2-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="caec2-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="caec2-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="caec2-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="caec2-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="caec2-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="caec2-120">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="caec2-120">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="caec2-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="caec2-121">Remarks</span></span>

<span data-ttu-id="caec2-122">Diese Funktion muss für alle mit [jetopentable](./jetopentable-function.md)geöffneten Tabellen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="caec2-122">This function must be called on all tables opened with [JetOpenTable](./jetopentable-function.md).</span></span>

<span data-ttu-id="caec2-123">Die Ausnahme von dieser Regel tritt auf, wenn [jetopentable](./jetopentable-function.md) in einer Transaktion aufgerufen wird und für die Transaktion ein Rollback ausgeführt wird (mit [jetrollback](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="caec2-123">The exception to this rule happens when [JetOpenTable](./jetopentable-function.md) is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="caec2-124">Beim Rollback einer Transaktion wird die Tabelle automatisch geschlossen.</span><span class="sxs-lookup"><span data-stu-id="caec2-124">When rolling back a transaction, the table is automatically closed.</span></span> <span data-ttu-id="caec2-125">In diesem Fall ist es ein Fehler, die Tabelle mit **jetclosetable** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="caec2-125">In this case, it is an error to close the table with **JetCloseTable**.</span></span>

#### <a name="requirements"></a><span data-ttu-id="caec2-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="caec2-126">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="caec2-127"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="caec2-127"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="caec2-128">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="caec2-128">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caec2-129"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="caec2-129"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="caec2-130">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="caec2-130">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caec2-131"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="caec2-131"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="caec2-132">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="caec2-132">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caec2-133"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="caec2-133"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="caec2-134">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="caec2-134">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caec2-135"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="caec2-135"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="caec2-136">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="caec2-136">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="caec2-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="caec2-137">See Also</span></span>

[<span data-ttu-id="caec2-138">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="caec2-138">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="caec2-139">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="caec2-139">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="caec2-140">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="caec2-140">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="caec2-141">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="caec2-141">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="caec2-142">Jetopentable</span><span class="sxs-lookup"><span data-stu-id="caec2-142">JetOpenTable</span></span>](./jetopentable-function.md)  
[<span data-ttu-id="caec2-143">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="caec2-143">JetRollback</span></span>](./jetrollback-function.md)
