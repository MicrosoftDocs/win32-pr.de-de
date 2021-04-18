---
description: 'Weitere Informationen: jetgetthreadstats-Funktion'
title: Jetgetthreadstats-Funktion
TOCTitle: JetGetThreadStats Function
ms:assetid: 1b8df8cd-fc61-44fe-a15c-a166f7097c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269196(v=EXCHG.10)
ms:contentKeyID: 32765499
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetThreadStats
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85d45021910f818f297cd0bc9829580a18b7a296
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344032"
---
# <a name="jetgetthreadstats-function"></a><span data-ttu-id="4a781-103">Jetgetthreadstats-Funktion</span><span class="sxs-lookup"><span data-stu-id="4a781-103">JetGetThreadStats Function</span></span>


<span data-ttu-id="4a781-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4a781-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetthreadstats-function"></a><span data-ttu-id="4a781-105">Jetgetthreadstats-Funktion</span><span class="sxs-lookup"><span data-stu-id="4a781-105">JetGetThreadStats Function</span></span>

<span data-ttu-id="4a781-106">Die **jetgetthreadstats** -Funktion ruft Leistungsinformationen aus der Datenbank-Engine für den aktuellen Thread ab.</span><span class="sxs-lookup"><span data-stu-id="4a781-106">The **JetGetThreadStats** function retrieves performance information from the database engine for the current thread.</span></span> <span data-ttu-id="4a781-107">Mehrere Aufrufe können verwendet werden, um Statistiken zu sammeln, die die Aktivität der Datenbank-Engine in diesem Thread zwischen diesen Aufrufen widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="4a781-107">Multiple calls can be used to collect statistics that reflect the activity of the database engine on this thread between those calls.</span></span>

<span data-ttu-id="4a781-108">**Windows Vista:**  **jetgetthreadstats** wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4a781-108">**Windows Vista:**  **JetGetThreadStats** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a><span data-ttu-id="4a781-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a781-109">Parameters</span></span>

<span data-ttu-id="4a781-110">*pvresult*</span><span class="sxs-lookup"><span data-stu-id="4a781-110">*pvResult*</span></span>

<span data-ttu-id="4a781-111">Der Ausgabepuffer, der die Thread Statistikdaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="4a781-111">The output buffer which receives the thread statistics data.</span></span> <span data-ttu-id="4a781-112">Der Puffer enthält eine [JET_THREADSTATS](./jet-threadstats-structure.md) Struktur nach einem erfolgreichen-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="4a781-112">The buffer contains a [JET_THREADSTATS](./jet-threadstats-structure.md) structure after a successful call.</span></span>

<span data-ttu-id="4a781-113">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="4a781-113">*cbMax*</span></span>

<span data-ttu-id="4a781-114">Die maximale Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="4a781-114">The maximum size in bytes of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="4a781-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a781-115">Return Value</span></span>

<span data-ttu-id="4a781-116">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="4a781-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4a781-117">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4a781-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4a781-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4a781-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="4a781-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a781-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a781-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4a781-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4a781-121">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4a781-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a781-122">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="4a781-122">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="4a781-123">Der Vorgang ist fehlgeschlagen, da der angegebene Ausgabepuffer zu klein war, um die angeforderten Daten zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="4a781-123">The operation failed because the provided output buffer was too small to contain the requested data.</span></span> <span data-ttu-id="4a781-124">Die <strong>jetgetthreadstats</strong> -Funktion gibt diesen Fehler zurück, wenn der Ausgabepuffer zu klein ist, um die kleinste Version der <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> Struktur zu enthalten, die von der Datenbank-Engine unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="4a781-124">The <strong>JetGetThreadStats</strong> function will return this error when the output buffer is too small to contain the smallest version of the <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> structure supported by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4a781-125">Bei Erfolg enthält der Ausgabepuffer eine [JET_THREADSTATS](./jet-threadstats-structure.md) Struktur, die Datenbank-Engine-Statistiken für den aktuellen Thread enthält.</span><span class="sxs-lookup"><span data-stu-id="4a781-125">On success, the output buffer will contain a [JET_THREADSTATS](./jet-threadstats-structure.md) structure that contains database engine statistics for the current thread.</span></span>

<span data-ttu-id="4a781-126">Bei einem Fehler ist der Status des Ausgabepuffers nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="4a781-126">On failure, the state of the output buffer is undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4a781-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a781-127">Remarks</span></span>

<span data-ttu-id="4a781-128">Die Informationen, die von zwei aufeinander folgenden Aufrufen dieser API bereitgestellt werden, sollen verwendet werden, um die Kosten anderer Datenbankmodul Vorgänge im aktuellen Thread zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="4a781-128">The information provided by two consecutive calls of this API are intended to be used to compute the expense of any other database engine operations on the current thread.</span></span> <span data-ttu-id="4a781-129">Im Allgemeinen wird dies erreicht, indem ein vor und nach dem Lesen der Statistiken durchgeführt wird und die nach Anzahl von der vorher-Anzahl subtrahieren, um die Netto Anzahl der ausgeführten Vorgänge zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4a781-129">Generally, this is done by taking a before and after reading of the statistics and subtracting the after count from the before count to get the net count of operations performed.</span></span>

<span data-ttu-id="4a781-130">Beispielsweise könnte eine Anwendung **jetgetthreadstats** einmal aufrufen, um das erste Lesen der Statistiken für den aktuellen Thread zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4a781-130">For example, an application could call **JetGetThreadStats** once to get an initial reading of the statistics for the current thread.</span></span> <span data-ttu-id="4a781-131">Anschließend kann die [jetmove](./jetmove-function.md) -Funktion aufgerufen werden, wobei der " *cRow* "-Parameter auf JET_MoveNext festgelegt ist, um zum nächsten Index Eintrag eines Indexes zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="4a781-131">It could then call the [JetMove](./jetmove-function.md) function with the *cRow* parameter set to JET_MoveNext to move to the next index entry on an index.</span></span> <span data-ttu-id="4a781-132">Anschließend kann **jetgetthreadstats** erneut aufgerufen werden, um ein weiteres lesen der Thread Statistik zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4a781-132">It could then call **JetGetThreadStats** again to get another reading of the thread's statistics.</span></span> <span data-ttu-id="4a781-133">Der cpagereferenzierte-Counter kann dann vom zweiten Lesevorgang aus dem ersten gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="4a781-133">It could then subtract the cPageReferenced counter from the second reading from the first.</span></span> <span data-ttu-id="4a781-134">Das Ergebnis ist die Anzahl der Datenbankseiten, auf die von der Datenbank-Engine verwiesen wird, um den [jetmove](./jetmove-function.md) -Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4a781-134">The result would be the number of database pages referenced by the database engine to perform the [JetMove](./jetmove-function.md) operation.</span></span>

<span data-ttu-id="4a781-135">Die Statistiken für jeden Thread werden für die Lebensdauer dieses Threads akkumuliert.</span><span class="sxs-lookup"><span data-stu-id="4a781-135">The statistics for each thread are accumulated for the lifetime of that thread.</span></span> <span data-ttu-id="4a781-136">Die Statistiken werden zurückgesetzt, wenn die dll der Datenbank-Engine aus dem Host Prozess entladen wird.</span><span class="sxs-lookup"><span data-stu-id="4a781-136">The statistics are reset if the database engine's DLL is unloaded from the host process.</span></span>

<span data-ttu-id="4a781-137">Die [JET_THREADSTATS](./jet-threadstats-structure.md) Struktur wird in Zukunft wahrscheinlich erweitert, um mehr Statistiken zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="4a781-137">The [JET_THREADSTATS](./jet-threadstats-structure.md) structure will likely be expanded in the future to contain more statistics.</span></span> <span data-ttu-id="4a781-138">Neue Statistiken werden am Ende der Struktur hinzugefügt und können mit einer erweiterten Ausgabepuffergröße abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4a781-138">New statistics will be added to the end of the structure and can be retrieved with an increased output buffer size.</span></span> <span data-ttu-id="4a781-139">Das vorhanden sein zusätzlicher Statistiken kann durch einen größeren cbStruct-Wert abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="4a781-139">The presence of additional statistics can be inferred by a larger cbStruct value.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4a781-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a781-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a781-141"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="4a781-141"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4a781-142">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4a781-142">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a781-143"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4a781-143"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4a781-144">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="4a781-144">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a781-145"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4a781-145"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4a781-146">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="4a781-146">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a781-147"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="4a781-147"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4a781-148">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4a781-148">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a781-149"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4a781-149"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4a781-150">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4a781-150">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4a781-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4a781-151">See Also</span></span>

[<span data-ttu-id="4a781-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4a781-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4a781-153">JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="4a781-153">JET_THREADSTATS</span></span>](./jet-threadstats-structure.md)  
[<span data-ttu-id="4a781-154">Jetmove</span><span class="sxs-lookup"><span data-stu-id="4a781-154">JetMove</span></span>](./jetmove-function.md)
