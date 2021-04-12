---
description: 'Weitere Informationen über: JET_PFNREALLOC Callback-Funktion'
title: JET_PFNREALLOC Callback-Funktion
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 032c1edcfd18166b79f4c8b2868d53d0b84434d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218594"
---
# <a name="jet_pfnrealloc-callback-function"></a><span data-ttu-id="03658-103">JET_PFNREALLOC Callback-Funktion</span><span class="sxs-lookup"><span data-stu-id="03658-103">JET_PFNREALLOC Callback Function</span></span>


<span data-ttu-id="03658-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="03658-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pfnrealloc-callback-function"></a><span data-ttu-id="03658-105">JET_PFNREALLOC Callback-Funktion</span><span class="sxs-lookup"><span data-stu-id="03658-105">JET_PFNREALLOC Callback Function</span></span>

<span data-ttu-id="03658-106">Die JET_PFNREALLOC-Funktion ist ein [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) -kompatibler Rückruf, der von [jetenumeratecolumns](./jetenumeratecolumns-function.md) verwendet wird, um Speicher für die Ausgabepuffer zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="03658-106">The JET_PFNREALLOC function is a [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback used by [JetEnumerateColumns](./jetenumeratecolumns-function.md) to allocate memory for its output buffers.</span></span>

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a><span data-ttu-id="03658-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="03658-107">Parameters</span></span>

<span data-ttu-id="03658-108">*pvcontext*</span><span class="sxs-lookup"><span data-stu-id="03658-108">*pvContext*</span></span>

<span data-ttu-id="03658-109">Der für [jetenumeratecolumns](./jetenumeratecolumns-function.md)angegebene Kontext Zeiger.</span><span class="sxs-lookup"><span data-stu-id="03658-109">The context pointer given to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span> <span data-ttu-id="03658-110">Dieser Kontext Zeiger kann verwendet werden, um den Zustand des Aufrufers von [jetenumeratecolumns](./jetenumeratecolumns-function.md) an die Implementierung dieses Rückrufs zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="03658-110">This context pointer can be used to convey state from the caller of [JetEnumerateColumns](./jetenumeratecolumns-function.md) to the implementation of this callback.</span></span>

<span data-ttu-id="03658-111">*teuren*</span><span class="sxs-lookup"><span data-stu-id="03658-111">*pv*</span></span>

<span data-ttu-id="03658-112">Wenn der Wert ungleich NULL ist, wird ein Zeiger auf einen Speicherblock angegeben, der zuvor von diesem Rückruf zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="03658-112">If non-NULL, specifies a pointer to a memory block previously allocated by this callback.</span></span> <span data-ttu-id="03658-113">Wenn der Wert NULL ist, wird ein neuer Speicherblock der angeforderten Größe zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="03658-113">If NULL, a new memory block of the requested size will be allocated.</span></span>

<span data-ttu-id="03658-114">*betrieben*</span><span class="sxs-lookup"><span data-stu-id="03658-114">*cb*</span></span>

<span data-ttu-id="03658-115">Die neue Größe des Speicherblocks in Bytes.</span><span class="sxs-lookup"><span data-stu-id="03658-115">The new size of the memory block in bytes.</span></span> <span data-ttu-id="03658-116">Wenn dieser Parameter 0 (null) ist und ein Speicherblock angegeben wird, wird dieser Speicherblock freigegeben.</span><span class="sxs-lookup"><span data-stu-id="03658-116">If this parameter is 0 (zero) and a memory block is specified, that memory block will be freed.</span></span>

### <a name="return-value"></a><span data-ttu-id="03658-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03658-117">Return Value</span></span>

<span data-ttu-id="03658-118">Das System generiert möglicherweise Erfolgs-oder Fehlercodes, wenn diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="03658-118">The system may generate success or failure codes as a result of a call to this function.</span></span> <span data-ttu-id="03658-119">Informationen dazu, wie diese Codes als HRESULTs zurückgegeben werden, finden Sie unter [Fehler bei Extensible Storage Engine](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="03658-119">For information about how to return these codes as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03658-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="03658-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="03658-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03658-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03658-122">Erfolg</span><span class="sxs-lookup"><span data-stu-id="03658-122">Success</span></span></p></td>
<td><p><span data-ttu-id="03658-123">Wenn ein zuvor zugewiesener Speicherblock angegeben wurde und eine neue Größe von 0 (null) angegeben wurde, wird der Block freigegeben, und es wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="03658-123">If a previously allocated memory block was specified and a new size of zero was specified then that block is freed and NULL will be returned.</span></span> <span data-ttu-id="03658-124">Wenn ein zuvor zugewiesener Speicherblock angegeben wurde und eine neue Größe ungleich 0 (null) angegeben wurde, wird der neu zugeordnete Speicherblock zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="03658-124">If a previously allocated memory block was specified and a non-zero new size was specified then the reallocated memory block is returned.</span></span> <span data-ttu-id="03658-125">Wenn kein Speicherblock angegeben wurde, wird ein neu zugeordneter Speicherblock der angegebenen Größe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="03658-125">If no memory block was specified then a newly allocated memory block of the specified size is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03658-126">Fehler</span><span class="sxs-lookup"><span data-stu-id="03658-126">Failure</span></span></p></td>
<td><p><span data-ttu-id="03658-127">NULL wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="03658-127">NULL will be returned.</span></span> <span data-ttu-id="03658-128">Wenn ein zuvor zugeordneter Speicherblock bereitgestellt wurde, bleibt dieser Block reserviert.</span><span class="sxs-lookup"><span data-stu-id="03658-128">If a previously allocated memory block was provided then that block will remain allocated.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="03658-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03658-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03658-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="03658-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="03658-131">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="03658-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03658-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="03658-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="03658-133">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="03658-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03658-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="03658-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="03658-135">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="03658-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="03658-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="03658-136">See Also</span></span>

[<span data-ttu-id="03658-137">Jetenreeratecolumschlag</span><span class="sxs-lookup"><span data-stu-id="03658-137">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)
