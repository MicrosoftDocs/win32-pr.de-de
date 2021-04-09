---
description: 'Weitere Informationen zu: jethssnapshotthaw-Funktion'
title: Jejessnapshotthaw-Funktion
TOCTitle: JetOSSnapshotThaw Function
ms:assetid: 3b001113-6299-4082-ab15-461f2e33e996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269229(v=EXCHG.10)
ms:contentKeyID: 32765531
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotThaw
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da7d5037cfc6b9a5f001dede57581127e4de60b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868940"
---
# <a name="jetossnapshotthaw-function"></a><span data-ttu-id="b7fed-103">Jejessnapshotthaw-Funktion</span><span class="sxs-lookup"><span data-stu-id="b7fed-103">JetOSSnapshotThaw Function</span></span>


<span data-ttu-id="b7fed-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b7fed-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotthaw-function"></a><span data-ttu-id="b7fed-105">Jejessnapshotthaw-Funktion</span><span class="sxs-lookup"><span data-stu-id="b7fed-105">JetOSSnapshotThaw Function</span></span>

<span data-ttu-id="b7fed-106">Die **jedessnapshotthaw** -Funktion benachrichtigt die Engine, dass Sie normale e/a-Vorgänge nach einem Sperr Zeitraum und einer erfolgreichen Momentaufnahme wieder aufnehmen kann.</span><span class="sxs-lookup"><span data-stu-id="b7fed-106">The **JetOSSnapshotThaw** function notifies the engine that it can resume normal IO operations after a freeze period and a successful snapshot.</span></span>

<span data-ttu-id="b7fed-107">**Windows XP:**  **jedessnapshotthaw** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7fed-107">**Windows XP:**  **JetOSSnapshotThaw** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotThaw(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="b7fed-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7fed-108">Parameters</span></span>

<span data-ttu-id="b7fed-109">*snapid*</span><span class="sxs-lookup"><span data-stu-id="b7fed-109">*snapId*</span></span>

<span data-ttu-id="b7fed-110">Der Bezeichner der Momentaufnahme Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b7fed-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="b7fed-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b7fed-111">*grbit*</span></span>

<span data-ttu-id="b7fed-112">Dieser Parameter ist für die zukünftige Verwendung reserviert, und der einzige gültige Wert ist 0.</span><span class="sxs-lookup"><span data-stu-id="b7fed-112">This parameter is reserved for future use and the only valid value supported is 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="b7fed-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7fed-113">Return Value</span></span>

<span data-ttu-id="b7fed-114">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="b7fed-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b7fed-115">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b7fed-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7fed-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b7fed-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="b7fed-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7fed-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7fed-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b7fed-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b7fed-119">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b7fed-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7fed-120">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b7fed-120">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b7fed-121">Die Momentaufnahme Sitzung ist ungültig, oder der <em>grbit</em> -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b7fed-121">The snapshot session is invalid or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7fed-122">JET_errOSSnapshotTimeOut</span><span class="sxs-lookup"><span data-stu-id="b7fed-122">JET_errOSSnapshotTimeOut</span></span></p></td>
<td><p><span data-ttu-id="b7fed-123">In der Momentaufnahme Sitzung war vor dem Auftreten dieses Aufrufes ein internes Timeout aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b7fed-123">The snapshot session had an internal timeout before this call occurred.</span></span> <span data-ttu-id="b7fed-124">Folglich werden e/a-Vorgänge vor dem Ausführen dieses Aufrufes normal zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b7fed-124">Consequently, IO operations returned to normal before this call was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7fed-125">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="b7fed-125">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="b7fed-126">Der Bezeichner für die Momentaufnahme Sitzung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b7fed-126">The identifier for snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b7fed-127">Wenn diese Funktion erfolgreich ausgeführt wird, wird eine Momentaufnahme Sitzung beendet, und das normale Engine-Verhalten wird fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="b7fed-127">If this function succeeds, a snapshot session ends and the normal engine behavior resumes.</span></span> <span data-ttu-id="b7fed-128">Eine neue Momentaufnahme Sitzung kann später gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="b7fed-128">A new snapshot session can be started later.</span></span>

<span data-ttu-id="b7fed-129">Wenn diese Funktion fehlschlägt, wird die aktuelle Momentaufnahme Sitzung beendet, aber das Einfrieren von IOS während des Momentaufnahme Zeitraums wurde intern nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="b7fed-129">If this function fails, the current snapshot session ends but the freeze of IOs during the snapshot period was not respected internally.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b7fed-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7fed-130">Remarks</span></span>

<span data-ttu-id="b7fed-131">Ereignisprotokoll Einträge werden für die verschiedenen Schritte der Momentaufnahme generiert.</span><span class="sxs-lookup"><span data-stu-id="b7fed-131">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b7fed-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7fed-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7fed-133"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b7fed-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b7fed-134">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b7fed-134">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7fed-135"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b7fed-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b7fed-136">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b7fed-136">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7fed-137"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b7fed-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b7fed-138">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="b7fed-138">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7fed-139"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="b7fed-139"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b7fed-140">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b7fed-140">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7fed-141"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b7fed-141"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b7fed-142">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b7fed-142">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b7fed-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b7fed-143">See Also</span></span>

[<span data-ttu-id="b7fed-144">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b7fed-144">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b7fed-145">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="b7fed-145">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="b7fed-146">Jejessnapshotabort</span><span class="sxs-lookup"><span data-stu-id="b7fed-146">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="b7fed-147">Jeto ssnapshotfreeze</span><span class="sxs-lookup"><span data-stu-id="b7fed-147">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="b7fed-148">Jejessnapshotprepare</span><span class="sxs-lookup"><span data-stu-id="b7fed-148">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)
