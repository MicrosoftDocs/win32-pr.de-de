---
description: 'Weitere Informationen finden Sie hier: jejessnapshotabort-Funktion'
title: Jejessnapshotabort-Funktion
TOCTitle: JetOSSnapshotAbort Function
ms:assetid: 629455af-b526-4366-9b9a-112757f72c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269265(v=EXCHG.10)
ms:contentKeyID: 32765567
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotAbort
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d976f027a940bcf0199016d0e617d515273183ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349998"
---
# <a name="jetossnapshotabort-function"></a><span data-ttu-id="b3873-103">Jejessnapshotabort-Funktion</span><span class="sxs-lookup"><span data-stu-id="b3873-103">JetOSSnapshotAbort Function</span></span>


<span data-ttu-id="b3873-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b3873-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotabort-function"></a><span data-ttu-id="b3873-105">Jejessnapshotabort-Funktion</span><span class="sxs-lookup"><span data-stu-id="b3873-105">JetOSSnapshotAbort Function</span></span>

<span data-ttu-id="b3873-106">Die **jedessnapshotabort** -Funktion benachrichtigt die Engine, dass Sie normale e/a-Vorgänge fortsetzen kann, nachdem eine Sperrfrist mit einem fehlerhaften Snapshot erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="b3873-106">The **JetOSSnapshotAbort** function notifies the engine that it can resume normal IO operations after a freeze period ended with a failed snapshot.</span></span>

<span data-ttu-id="b3873-107">**Windows Server 2003:**  **jedessnapshotabort** wurde in Windows Server 2003 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b3873-107">**Windows Server 2003:**  **JetOSSnapshotAbort** is introduced in Windows Server 2003.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="b3873-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3873-108">Parameters</span></span>

<span data-ttu-id="b3873-109">*snapid*</span><span class="sxs-lookup"><span data-stu-id="b3873-109">*snapId*</span></span>

<span data-ttu-id="b3873-110">Der Bezeichner der Momentaufnahme Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b3873-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="b3873-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b3873-111">*grbit*</span></span>

<span data-ttu-id="b3873-112">Die Optionen für diesen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="b3873-112">The options for this call.</span></span> <span data-ttu-id="b3873-113">Dieser Parameter ist für die zukünftige Verwendung reserviert, und der einzige gültige Wert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b3873-113">This parameter is reserved for future use and the only valid value supported is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="b3873-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3873-114">Return Value</span></span>

<span data-ttu-id="b3873-115">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="b3873-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b3873-116">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b3873-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b3873-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b3873-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="b3873-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3873-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3873-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b3873-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b3873-120">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b3873-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3873-121">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b3873-121">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b3873-122">Die Momentaufnahme Sitzung ist ungültig, oder der grbit-Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b3873-122">The snapshot session is invalid or the grbit parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3873-123">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="b3873-123">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="b3873-124">Der Bezeichner für die Momentaufnahme Sitzung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b3873-124">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b3873-125">Wenn diese Funktion erfolgreich ausgeführt wird, wird die Momentaufnahme Sitzung beendet, und das normale Engine-Verhalten wird fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="b3873-125">If this function succeeds, the snapshot session will end and the normal engine behavior will resume.</span></span> <span data-ttu-id="b3873-126">Eine neue Momentaufnahme Sitzung kann zu einem späteren Zeitpunkt gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="b3873-126">A new snapshot session can be started at a later point.</span></span>

<span data-ttu-id="b3873-127">Wenn diese Funktion fehlschlägt, wird die Momentaufnahme Sitzung nicht abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="b3873-127">If this function fails, the snapshot session will not be aborted.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b3873-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3873-128">Remarks</span></span>

<span data-ttu-id="b3873-129">Diese Funktion sollte anstelle von [jedessnapshotthaw](./jetossnapshotthaw-function.md) aufgerufen werden, um die Engine darüber zu informieren, dass die Momentaufnahme aus Gründen, die nicht mit der Engine in Beziehung stehen, abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="b3873-129">This function should be called instead of [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) to inform the engine that the snapshot was aborted for reasons that don't relate to the engine.</span></span> <span data-ttu-id="b3873-130">Diese Informationen können später verwendet werden, um Ereignisprotokoll Meldungen über die Momentaufnahme Sitzung auszugeben oder um andere geeignete Aktionen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="b3873-130">This information can be used later to help issue event log messages about the snapshot session or to help determine other appropriate actions.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b3873-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3873-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3873-132"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b3873-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b3873-133">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b3873-133">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3873-134"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b3873-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b3873-135">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b3873-135">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3873-136"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b3873-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b3873-137">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="b3873-137">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3873-138"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="b3873-138"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b3873-139">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b3873-139">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3873-140"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b3873-140"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b3873-141">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b3873-141">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b3873-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b3873-142">See Also</span></span>

[<span data-ttu-id="b3873-143">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b3873-143">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b3873-144">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="b3873-144">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="b3873-145">Jeto ssnapshotfreeze</span><span class="sxs-lookup"><span data-stu-id="b3873-145">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="b3873-146">Jejessnapshotprepare</span><span class="sxs-lookup"><span data-stu-id="b3873-146">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="b3873-147">Jejessnapshotthaw</span><span class="sxs-lookup"><span data-stu-id="b3873-147">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
