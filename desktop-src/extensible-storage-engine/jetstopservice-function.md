---
description: Weitere Informationen finden Sie in der jetstopservice-Funktion
title: JetStopService-Funktion
TOCTitle: JetStopService Function
ms:assetid: 46aeb9ed-ee72-49cc-99e3-791a51a55b02
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269240(v=EXCHG.10)
ms:contentKeyID: 32765542
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopService
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e66b4e5242710c89ca7e7964ecd0a72774b719d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368118"
---
# <a name="jetstopservice-function"></a><span data-ttu-id="26f2d-103">JetStopService-Funktion</span><span class="sxs-lookup"><span data-stu-id="26f2d-103">JetStopService Function</span></span>


<span data-ttu-id="26f2d-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="26f2d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopservice-function"></a><span data-ttu-id="26f2d-105">JetStopService-Funktion</span><span class="sxs-lookup"><span data-stu-id="26f2d-105">JetStopService Function</span></span>

<span data-ttu-id="26f2d-106">Die **jetstopservice** -Funktion bereitet eine Instanz für die Beendigung vor.</span><span class="sxs-lookup"><span data-stu-id="26f2d-106">The **JetStopService** function prepares an instance for termination.</span></span>

<span data-ttu-id="26f2d-107">**Jetstopservice** ist der Legacy-Befehl, wenn nur eine Instanz zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="26f2d-107">**JetStopService** is the legacy call when only one instance is allowed.</span></span> <span data-ttu-id="26f2d-108">In diesem Fall ist die einzige aktive Instanz die, die für die Beendigung vorbereitet wird.</span><span class="sxs-lookup"><span data-stu-id="26f2d-108">In this case, the only active instance is the one being prepared for termination.</span></span>

```cpp
    JET_ERR JET_API JetStopService(void);
```

### <a name="parameters"></a><span data-ttu-id="26f2d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="26f2d-109">Parameters</span></span>

<span data-ttu-id="26f2d-110">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="26f2d-110">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="26f2d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26f2d-111">Return Value</span></span>

<span data-ttu-id="26f2d-112">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="26f2d-112">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="26f2d-113">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="26f2d-113">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26f2d-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="26f2d-114">Return code</span></span></p></th>
<th><p><span data-ttu-id="26f2d-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26f2d-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26f2d-116">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="26f2d-116">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="26f2d-117">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="26f2d-117">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f2d-118">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="26f2d-118">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="26f2d-119">Es ist nicht klar, welche Instanz für die Beendigung vorbereitet werden soll, wenn <strong>jetstopservice</strong> im Modus für mehrere Instanzen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="26f2d-119">It is not clear which instance to prepare for termination when using <strong>JetStopService</strong> with multiple instance mode.</span></span></p>
<p><span data-ttu-id="26f2d-120"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="26f2d-120"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="26f2d-121">Wenn diese Funktion erfolgreich ausgeführt wird, wird eine zukünftige Beendigung vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="26f2d-121">If this function succeeds, it prepares for a future termination.</span></span> <span data-ttu-id="26f2d-122">Die Schritte zur Vorbereitung auf eine Beendigung umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="26f2d-122">The steps taken to prepare for a termination include the following:</span></span>

  - <span data-ttu-id="26f2d-123">Stoppt die Online Defragmentierung, wenn Sie ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26f2d-123">Stop online defragmentation if it is running.</span></span>

  - <span data-ttu-id="26f2d-124">Starten Sie eine Bereinigung des Versionsspeicher.</span><span class="sxs-lookup"><span data-stu-id="26f2d-124">Start a version store clean-up.</span></span>

  - <span data-ttu-id="26f2d-125">Verringern Sie die Prüf Punkt Tiefe, indem Sie mit dem leeren von geänderten Seiten im Puffer-Manager beginnen.</span><span class="sxs-lookup"><span data-stu-id="26f2d-125">Reduce the checkpoint depth by starting to flush dirty pages in the buffer manager.</span></span>

  - <span data-ttu-id="26f2d-126">Vermeiden Sie zukünftige Aufrufe der meisten Funktionen für diese Instanz.</span><span class="sxs-lookup"><span data-stu-id="26f2d-126">Prevent future calls to most functions for that instance.</span></span>

<span data-ttu-id="26f2d-127">Wenn diese Funktion fehlschlägt, wird keiner der Schritte zur Vorbereitung auf das Beenden einer Instanz durchgeführt, sodass keine Änderung am Instanzstatus erfolgt.</span><span class="sxs-lookup"><span data-stu-id="26f2d-127">If this function fails, none of the steps to prepare for an instance termination will be taken, so no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26f2d-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26f2d-128">Remarks</span></span>

<span data-ttu-id="26f2d-129">Diese Funktion reduziert den Arbeitsaufwand, den die-Instanz ausführen muss, wenn Sie beendet wird, beendet jedoch nicht die-Instanz.</span><span class="sxs-lookup"><span data-stu-id="26f2d-129">This function reduces the work the instance will have to do when terminated, but will not terminate the instance.</span></span> <span data-ttu-id="26f2d-130">Daher ist diese Funktion nur eine Optimierung und ist nicht für die Verwendung von obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="26f2d-130">As a result, this function is just an optimization and is not mandatory to use.</span></span> <span data-ttu-id="26f2d-131">Beachten Sie, dass der Aufwand für die Vorbereitung in Windows 2000 und Windows XP geringer war.</span><span class="sxs-lookup"><span data-stu-id="26f2d-131">Note that the amount of work done in preparation was less in Windows 2000 and Windows XP.</span></span> <span data-ttu-id="26f2d-132">Wenn die Funktion erfolgreich ausgeführt wird, wird das Aufrufen von Funktionen, die nicht mehr zulässig sind, JET_errClientRequestToStopJetService zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="26f2d-132">Once the function succeeds, calling functions that are no longer allowed will return JET_errClientRequestToStopJetService.</span></span> <span data-ttu-id="26f2d-133">Funktionen, die nach diesem Aufrufvorgang weiterhin zulässig sind: [jetrollback](./jetrollback-function.md), [jetclosetable](./jetclosetable-function.md), [jetendsession](./jetendsession-function.md), [jetclosedatabase](./jetclosedatabase-function.md), [jetdetachdatabase](./jetdetachdatabase-function.md) und [jetressitzungscontext](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="26f2d-133">Functions that are still allowed after this call are: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="26f2d-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26f2d-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26f2d-135"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="26f2d-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="26f2d-136">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="26f2d-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f2d-137"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="26f2d-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="26f2d-138">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="26f2d-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26f2d-139"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="26f2d-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="26f2d-140">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="26f2d-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26f2d-141"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="26f2d-141"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="26f2d-142">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="26f2d-142">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26f2d-143"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="26f2d-143"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="26f2d-144">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="26f2d-144">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="26f2d-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="26f2d-145">See Also</span></span>

[<span data-ttu-id="26f2d-146">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="26f2d-146">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="26f2d-147">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="26f2d-147">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="26f2d-148">Jetclosedatabase</span><span class="sxs-lookup"><span data-stu-id="26f2d-148">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="26f2d-149">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="26f2d-149">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="26f2d-150">Jetdetachdatabase</span><span class="sxs-lookup"><span data-stu-id="26f2d-150">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="26f2d-151">Jetendsession</span><span class="sxs-lookup"><span data-stu-id="26f2d-151">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="26f2d-152">Jetresessioncontext</span><span class="sxs-lookup"><span data-stu-id="26f2d-152">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="26f2d-153">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="26f2d-153">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="26f2d-154">Jetterm</span><span class="sxs-lookup"><span data-stu-id="26f2d-154">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="26f2d-155">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="26f2d-155">JetTerm2</span></span>](./jetterm2-function.md)
