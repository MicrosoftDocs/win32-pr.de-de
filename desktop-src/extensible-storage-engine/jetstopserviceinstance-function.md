---
description: 'Weitere Informationen finden Sie unter: jetstopserviczustance-Funktion'
title: Jetstopserviczustance-Funktion
TOCTitle: JetStopServiceInstance Function
ms:assetid: d8d3d047-91d6-4054-b3e1-44174666900e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294108(v=EXCHG.10)
ms:contentKeyID: 32765723
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopServiceInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9b2e3307f13a63d00cbbaf33f491750bbfcdb9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346917"
---
# <a name="jetstopserviceinstance-function"></a><span data-ttu-id="1e221-103">Jetstopserviczustance-Funktion</span><span class="sxs-lookup"><span data-stu-id="1e221-103">JetStopServiceInstance Function</span></span>


<span data-ttu-id="1e221-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1e221-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopserviceinstance-function"></a><span data-ttu-id="1e221-105">Jetstopserviczustance-Funktion</span><span class="sxs-lookup"><span data-stu-id="1e221-105">JetStopServiceInstance Function</span></span>

<span data-ttu-id="1e221-106">Die **jetstopserviceinstance** -Funktion bereitet eine Instanz für die Beendigung vor.</span><span class="sxs-lookup"><span data-stu-id="1e221-106">The **JetStopServiceInstance** function prepares an instance for termination.</span></span>

<span data-ttu-id="1e221-107">**Windows XP:**  **jetstopserviceinstance** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1e221-107">**Windows XP:**  **JetStopServiceInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetStopServiceInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="1e221-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e221-108">Parameters</span></span>

<span data-ttu-id="1e221-109">*lichen*</span><span class="sxs-lookup"><span data-stu-id="1e221-109">*instance*</span></span>

<span data-ttu-id="1e221-110">Die für den API-Befehl zu verwendende-Instanz.</span><span class="sxs-lookup"><span data-stu-id="1e221-110">The running instance to use for the API call.</span></span>

### <a name="return-value"></a><span data-ttu-id="1e221-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e221-111">Return Value</span></span>

<span data-ttu-id="1e221-112">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="1e221-112">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1e221-113">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1e221-113">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e221-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1e221-114">Return code</span></span></p></th>
<th><p><span data-ttu-id="1e221-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e221-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e221-116">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1e221-116">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1e221-117">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1e221-117">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e221-118">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1e221-118">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1e221-119">Der angegebene Instanzparameter weist einen ungültigen Wert auf (keine Instanz, die derzeit ausgeführt wird).</span><span class="sxs-lookup"><span data-stu-id="1e221-119">The specified instance parameter has an invalid value (not an instance that is currently running).</span></span></p>
<p><span data-ttu-id="1e221-120"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1e221-120"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1e221-121">Wenn diese Funktion erfolgreich ausgeführt wird, wird eine zukünftige Beendigung vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="1e221-121">If this function succeeds, it prepares for a future termination.</span></span> <span data-ttu-id="1e221-122">Die Schritte zur Vorbereitung auf eine Beendigung umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1e221-122">The steps taken to prepare for a termination include the following:</span></span>

  - <span data-ttu-id="1e221-123">Stoppt die Online Defragmentierung, wenn Sie ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e221-123">Stop online defragmentation if it is running.</span></span>

  - <span data-ttu-id="1e221-124">Starten Sie eine Bereinigung des Versionsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1e221-124">Start a version store clean-up.</span></span>

  - <span data-ttu-id="1e221-125">Verringern Sie die Prüf Punkt Tiefe, indem Sie mit dem leeren von geänderten Seiten im Puffer-Manager beginnen.</span><span class="sxs-lookup"><span data-stu-id="1e221-125">Reduce the checkpoint depth by starting to flush dirty pages in the buffer manager.</span></span>

  - <span data-ttu-id="1e221-126">Vermeiden Sie zukünftige Aufrufe der meisten Funktionen für diese Instanz.</span><span class="sxs-lookup"><span data-stu-id="1e221-126">Prevent future calls to most functions for that instance.</span></span>

<span data-ttu-id="1e221-127">Wenn diese Funktion fehlschlägt, wird keiner der Schritte zur Vorbereitung auf das Beenden einer Instanz durchgeführt, sodass keine Änderung am Instanzstatus erfolgt.</span><span class="sxs-lookup"><span data-stu-id="1e221-127">If this function fails, none of the steps to prepare for an instance termination will be taken, so no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="1e221-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e221-128">Remarks</span></span>

<span data-ttu-id="1e221-129">Diese Funktion reduziert die Arbeit, die die Instanz ausführen muss, wenn Sie beendet wird, die Instanz jedoch nicht beendet.</span><span class="sxs-lookup"><span data-stu-id="1e221-129">This function will reduce the work the instance will have to do when terminated but will not terminate the instance.</span></span> <span data-ttu-id="1e221-130">Daher ist diese Funktion nur eine Optimierung und ist nicht für die Verwendung von obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="1e221-130">As a result, this function is just an optimization and is not mandatory to use.</span></span> <span data-ttu-id="1e221-131">Beachten Sie, dass der Aufwand für die Vorbereitung in Windows 2000 und Windows XP geringer war.</span><span class="sxs-lookup"><span data-stu-id="1e221-131">Note that the amount of work done in preparation was less in Windows 2000 and Windows XP.</span></span> <span data-ttu-id="1e221-132">Wenn die Funktion erfolgreich ausgeführt wird, wird das Aufrufen von Funktionen, die nicht mehr zulässig sind, JET_errClientRequestToStopJetService zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1e221-132">Once the function succeeds, calling functions that are no longer allowed will return JET_errClientRequestToStopJetService.</span></span> <span data-ttu-id="1e221-133">Funktionen, die nach diesem Aufrufvorgang weiterhin zulässig sind: [jetrollback](./jetrollback-function.md), [jetclosetable](./jetclosetable-function.md), [jetendsession](./jetendsession-function.md), [jetclosedatabase](./jetclosedatabase-function.md), [jetdetachdatabase](./jetdetachdatabase-function.md) und [jetressitzungscontext](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="1e221-133">Functions that are still allowed after this call are: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="1e221-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e221-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e221-135"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="1e221-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1e221-136">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1e221-136">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e221-137"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1e221-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1e221-138">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1e221-138">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e221-139"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1e221-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1e221-140">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="1e221-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e221-141"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="1e221-141"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1e221-142">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1e221-142">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e221-143"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1e221-143"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1e221-144">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1e221-144">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1e221-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1e221-145">See Also</span></span>

[<span data-ttu-id="1e221-146">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1e221-146">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1e221-147">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="1e221-147">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="1e221-148">Jetclosedatabase</span><span class="sxs-lookup"><span data-stu-id="1e221-148">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="1e221-149">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="1e221-149">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="1e221-150">Jetdetachdatabase</span><span class="sxs-lookup"><span data-stu-id="1e221-150">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="1e221-151">Jetendsession</span><span class="sxs-lookup"><span data-stu-id="1e221-151">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="1e221-152">Jetresessioncontext</span><span class="sxs-lookup"><span data-stu-id="1e221-152">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="1e221-153">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="1e221-153">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="1e221-154">Jetterm</span><span class="sxs-lookup"><span data-stu-id="1e221-154">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="1e221-155">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="1e221-155">JetTerm2</span></span>](./jetterm2-function.md)
