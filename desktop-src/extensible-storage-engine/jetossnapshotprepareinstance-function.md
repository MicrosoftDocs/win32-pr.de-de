---
description: 'Weitere Informationen finden Sie hier: jeum-Funktion'
title: Jeto ssnapshotprepareingestance-Funktion
TOCTitle: JetOSSnapshotPrepareInstance Function
ms:assetid: b4f06342-633f-47c6-be32-64ec058920fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294064(v=EXCHG.10)
ms:contentKeyID: 32765679
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepareInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cc5179a55aabfa3324e3caab7005f4abe437a6d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104394282"
---
# <a name="jetossnapshotprepareinstance-function"></a><span data-ttu-id="415da-103">Jeto ssnapshotprepareingestance-Funktion</span><span class="sxs-lookup"><span data-stu-id="415da-103">JetOSSnapshotPrepareInstance Function</span></span>


<span data-ttu-id="415da-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="415da-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotprepareinstance-function"></a><span data-ttu-id="415da-105">Jeto ssnapshotprepareingestance-Funktion</span><span class="sxs-lookup"><span data-stu-id="415da-105">JetOSSnapshotPrepareInstance Function</span></span>

<span data-ttu-id="415da-106">Die **jedessnapshotprepareinstance** -Funktion wählt eine bestimmte Instanz aus, die Teil der Momentaufnahme Sitzung sein soll.</span><span class="sxs-lookup"><span data-stu-id="415da-106">The **JetOSSnapshotPrepareInstance** function selects a specific instance to be part of the snapshot session.</span></span>

<span data-ttu-id="415da-107">**Windows Vista:** **jedessnapshotprepareinstance** wurde in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="415da-107">**Windows Vista:** **JetOSSnapshotPrepareInstance** was introduced in Windows Vista.</span></span>

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
  __in          JET_INSTANCE instance,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="415da-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="415da-108">Parameters</span></span>

<span data-ttu-id="415da-109">*snapid*</span><span class="sxs-lookup"><span data-stu-id="415da-109">*snapId*</span></span>

<span data-ttu-id="415da-110">Der Bezeichner der Momentaufnahme Sitzung.</span><span class="sxs-lookup"><span data-stu-id="415da-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="415da-111">*lichen*</span><span class="sxs-lookup"><span data-stu-id="415da-111">*instance*</span></span>

<span data-ttu-id="415da-112">Die-Instanz, die für diesen-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="415da-112">The instance that will be used for this call.</span></span>

<span data-ttu-id="415da-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="415da-113">*grbit*</span></span>

<span data-ttu-id="415da-114">Die Optionen für diesen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="415da-114">The options for this call.</span></span> <span data-ttu-id="415da-115">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="415da-115">This parameter is reserved for future use.</span></span> <span data-ttu-id="415da-116">Der einzige gültige Wert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="415da-116">The only valid value is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="415da-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="415da-117">Return Value</span></span>

<span data-ttu-id="415da-118">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="415da-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="415da-119">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="415da-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="415da-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="415da-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="415da-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="415da-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="415da-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="415da-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="415da-123">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="415da-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="415da-124">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="415da-124">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="415da-125">Der Momentaufnahme-ID-Zeiger ist <strong>null</strong> , oder der <em>grbit</em> -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="415da-125">The snapshot id pointer is <strong>NULL</strong> or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="415da-126">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="415da-126">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="415da-127">Eine Momentaufnahme Sitzung wird bereits ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="415da-127">A snapshot session is already in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="415da-128">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="415da-128">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="415da-129">Der Bezeichner für die Momentaufnahme Sitzung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="415da-129">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="415da-130">Wenn diese Funktion erfolgreich ausgeführt wird, ist die angegebene Instanz Teil der Momentaufnahme Sitzung.</span><span class="sxs-lookup"><span data-stu-id="415da-130">If this function succeeds, the specified instance will be part of the snapshot session.</span></span>

<span data-ttu-id="415da-131">Wenn diese Funktion fehlschlägt, erfolgt keine Änderung des Engine-Zustands.</span><span class="sxs-lookup"><span data-stu-id="415da-131">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="415da-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="415da-132">Remarks</span></span>

<span data-ttu-id="415da-133">Der reguläre API-Sequenz Aufruf lautet: [jedessnapshotprepare](./jetossnapshotprepare-function.md), optional gefolgt von einem oder mehreren Aufrufen von **jedessnapshotprepareinstance** und anschließendem [jeto ssnapshotfreeze](./jetossnapshotfreeze-function.md).</span><span class="sxs-lookup"><span data-stu-id="415da-133">The normal API sequence call is: [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), optionally followed by one or more calls to **JetOSSnapshotPrepareInstance**, then followed by [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span></span> <span data-ttu-id="415da-134">Nachdem das Einfrieren gestartet wurde, kann es mit [jeto ssnapshotthaw](./jetossnapshotthaw-function.md)beendet werden.</span><span class="sxs-lookup"><span data-stu-id="415da-134">Once the freeze is started, it can be terminated using [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span> <span data-ttu-id="415da-135">Nach der Vorbereitung kann die Momentaufnahme Sitzung jederzeit mit [jedessnapshotabort](./jetossnapshotabort-function.md)beendet werden.</span><span class="sxs-lookup"><span data-stu-id="415da-135">At any time after the prepare, the snapshot session can be abruptly terminated with [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span></span> <span data-ttu-id="415da-136">Ereignisprotokoll Einträge werden für die verschiedenen Schritte der Momentaufnahme generiert.</span><span class="sxs-lookup"><span data-stu-id="415da-136">Event log entries will be generated for the different steps of the snapshot.</span></span>

<span data-ttu-id="415da-137">Wenn **jedessnapshotprepareinstance** zwischen dem Start der Sitzung ([jedessnapshotprepare](./jetossnapshotprepare-function.md)) und dem Freeze-Moment ([jedessnapshotfreeze](./jetossnapshotfreeze-function.md)) nicht aufgerufen wird, werden alle derzeit in der Engine laufenden Instanzen fixiert und in die Momentaufnahme Sitzung aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="415da-137">If **JetOSSnapshotPrepareInstance** is not called between the start of the session ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) and the freeze moment ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), all the running instances in the engine will freeze and become part of the snapshot session.</span></span> <span data-ttu-id="415da-138">Dies geschieht aus zwei Gründen:</span><span class="sxs-lookup"><span data-stu-id="415da-138">This occurs for two reasons:</span></span>

  - <span data-ttu-id="415da-139">Der Code für Benutzer, die alle Instanzen wünschen, wird vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="415da-139">It simplifies the code for users who want all instances.</span></span>

  - <span data-ttu-id="415da-140">Sie ermöglicht die Abwärtskompatibilität für die Aufrufer der Momentaufnahme-APIs.</span><span class="sxs-lookup"><span data-stu-id="415da-140">It allows backward compatibility for the callers of the snapshot APIs.</span></span>

#### <a name="requirements"></a><span data-ttu-id="415da-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="415da-141">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="415da-142"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="415da-142"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="415da-143">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="415da-143">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="415da-144"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="415da-144"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="415da-145">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="415da-145">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="415da-146"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="415da-146"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="415da-147">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="415da-147">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="415da-148"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="415da-148"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="415da-149">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="415da-149">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="415da-150"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="415da-150"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="415da-151">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="415da-151">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="415da-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="415da-152">See Also</span></span>

[<span data-ttu-id="415da-153">Fehler Behandlungsparameter</span><span class="sxs-lookup"><span data-stu-id="415da-153">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="415da-154">Erweiterbare Speicher-Engine-Fehler</span><span class="sxs-lookup"><span data-stu-id="415da-154">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="415da-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="415da-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="415da-156">Jejessnapshotabort</span><span class="sxs-lookup"><span data-stu-id="415da-156">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="415da-157">Jeto ssnapshotend</span><span class="sxs-lookup"><span data-stu-id="415da-157">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="415da-158">Jeto ssnapshotfreeze</span><span class="sxs-lookup"><span data-stu-id="415da-158">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="415da-159">Jejessnapshotprepare</span><span class="sxs-lookup"><span data-stu-id="415da-159">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="415da-160">Jejessnapshotthaw</span><span class="sxs-lookup"><span data-stu-id="415da-160">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
