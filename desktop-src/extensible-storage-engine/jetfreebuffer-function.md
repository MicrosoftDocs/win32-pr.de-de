---
description: 'Weitere Informationen über: jetfrebuffer-Funktion'
title: Jetfrebuffer-Funktion
TOCTitle: JetFreeBuffer Function
ms:assetid: f37d35f6-4bea-46ba-a334-7b8ad7a1568c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294134(v=EXCHG.10)
ms:contentKeyID: 32765748
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetFreeBuffer
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe638e2aab1d37324a6fd6bf477a578f02b9ac58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352288"
---
# <a name="jetfreebuffer-function"></a><span data-ttu-id="f7268-103">Jetfrebuffer-Funktion</span><span class="sxs-lookup"><span data-stu-id="f7268-103">JetFreeBuffer Function</span></span>


<span data-ttu-id="f7268-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f7268-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetfreebuffer-function"></a><span data-ttu-id="f7268-105">Jetfrebuffer-Funktion</span><span class="sxs-lookup"><span data-stu-id="f7268-105">JetFreeBuffer Function</span></span>

<span data-ttu-id="f7268-106">Die **jetfrebuffer** -Funktion gibt Arbeitsspeicher frei, der durch einen Datenbank-Engine-Befehl zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="f7268-106">The **JetFreeBuffer** function frees memory that was allocated by a database engine call.</span></span>

<span data-ttu-id="f7268-107">**Windows XP: jetfrebuffer** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f7268-107">**Windows XP:  JetFreeBuffer** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetFreeBuffer(
      __in          char* pbBuf
    );
```

### <a name="parameters"></a><span data-ttu-id="f7268-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7268-108">Parameters</span></span>

<span data-ttu-id="f7268-109">*pbbuf*</span><span class="sxs-lookup"><span data-stu-id="f7268-109">*pbBuf*</span></span>

<span data-ttu-id="f7268-110">Ein Zeiger auf einen Speicherbereich, der zuvor durch einen Datenbankmodul-aufrufswert zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="f7268-110">Pointer to a region of memory that was previously allocated by a call to the database engine.</span></span> <span data-ttu-id="f7268-111">**Null** ist akzeptabel und wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f7268-111">**NULL** is acceptable, and will be ignored.</span></span>

### <a name="return-value"></a><span data-ttu-id="f7268-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f7268-112">Return Value</span></span>

<span data-ttu-id="f7268-113">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="f7268-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f7268-114">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f7268-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7268-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f7268-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="f7268-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7268-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7268-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f7268-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f7268-118">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f7268-118">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="f7268-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7268-119">Remarks</span></span>

<span data-ttu-id="f7268-120">Es ist nicht definiertes Verhalten, Arbeitsspeicher, der nicht von der Datenbank-Engine in zugewiesen wurde, an *pbbuf* zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="f7268-120">It is undefined behavior to pass memory that was not allocated by the database engine in to *pbBuf*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f7268-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7268-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7268-122"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f7268-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f7268-123">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f7268-123">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7268-124"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f7268-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f7268-125">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f7268-125">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7268-126"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f7268-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f7268-127">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="f7268-127">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7268-128"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="f7268-128"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f7268-129">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f7268-129">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7268-130"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f7268-130"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f7268-131">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f7268-131">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f7268-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f7268-132">See Also</span></span>

[<span data-ttu-id="f7268-133">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f7268-133">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f7268-134">Jetgetinstanceingefo</span><span class="sxs-lookup"><span data-stu-id="f7268-134">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)
