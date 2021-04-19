---
description: 'Weitere Informationen finden Sie hier: jejessnapshotprepare-Funktion'
title: JetOSSnapshotPrepare-Funktion
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 67ccf9a5b21ccb9a4f94ba5aa4f995e4bb9017bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364101"
---
# <a name="jetossnapshotprepare-function"></a><span data-ttu-id="39c76-103">JetOSSnapshotPrepare-Funktion</span><span class="sxs-lookup"><span data-stu-id="39c76-103">JetOSSnapshotPrepare Function</span></span>


<span data-ttu-id="39c76-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="39c76-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotprepare-function"></a><span data-ttu-id="39c76-105">JetOSSnapshotPrepare-Funktion</span><span class="sxs-lookup"><span data-stu-id="39c76-105">JetOSSnapshotPrepare Function</span></span>

<span data-ttu-id="39c76-106">Die **jedessnapshotprepare** -Funktion beginnt die Vorbereitung für eine Momentaufnahme Sitzung.</span><span class="sxs-lookup"><span data-stu-id="39c76-106">The **JetOSSnapshotPrepare** function begins the preparations for a snapshot session.</span></span> <span data-ttu-id="39c76-107">Eine Momentaufnahme Sitzung ist ein kurzes Zeitintervall, in dem die Engine keine Schreibvorgänge auf dem Datenträger ausgibt, sodass die Engine an einer volumemomentaufnahmensitzung teilnehmen kann (wenn Sie von einem Momentaufnahme-Writer gesteuert wird).</span><span class="sxs-lookup"><span data-stu-id="39c76-107">A snapshot session is a short time interval in which the engine does not issue any write IOs to disk, so that the engine can participate in a volume snapshot session (when driven by a snapshot writer).</span></span>

<span data-ttu-id="39c76-108">**Windows XP:**  **jedessnapshotprepare** wurde in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="39c76-108">**Windows XP:**  **JetOSSnapshotPrepare** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="39c76-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="39c76-109">Parameters</span></span>

<span data-ttu-id="39c76-110">*psnapid*</span><span class="sxs-lookup"><span data-stu-id="39c76-110">*psnapId*</span></span>

<span data-ttu-id="39c76-111">Der Bezeichner der Momentaufnahme Sitzung, die gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="39c76-111">The identifier of the snapshot session to be started.</span></span>

<span data-ttu-id="39c76-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="39c76-112">*grbit*</span></span>

<span data-ttu-id="39c76-113">Die Optionen für diesen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="39c76-113">The options for this call.</span></span> <span data-ttu-id="39c76-114">Dieser Parameter kann eine Kombination der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="39c76-114">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39c76-115">Wert</span><span class="sxs-lookup"><span data-stu-id="39c76-115">Value</span></span></p></th>
<th><p><span data-ttu-id="39c76-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="39c76-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39c76-117">0</span><span class="sxs-lookup"><span data-stu-id="39c76-117">0</span></span></p></td>
<td><p><span data-ttu-id="39c76-118">Normale Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="39c76-118">Normal snapshot.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c76-119">JET_bitIncrementalSnapshot</span><span class="sxs-lookup"><span data-stu-id="39c76-119">JET_bitIncrementalSnapshot</span></span></p></td>
<td><p><span data-ttu-id="39c76-120">Es werden nur Protokolldateien erstellt.</span><span class="sxs-lookup"><span data-stu-id="39c76-120">Only log files will be taken.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c76-121">JET_bitCopySnapshot</span><span class="sxs-lookup"><span data-stu-id="39c76-121">JET_bitCopySnapshot</span></span></p></td>
<td><p><span data-ttu-id="39c76-122">Eine Kopier Momentaufnahme (normal oder inkrementell) ohne Protokoll abkürzen.</span><span class="sxs-lookup"><span data-stu-id="39c76-122">A copy snapshot (normal or incremental) with no log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c76-123">JET_bitContinueAfterThaw</span><span class="sxs-lookup"><span data-stu-id="39c76-123">JET_bitContinueAfterThaw</span></span></p></td>
<td><p><span data-ttu-id="39c76-124">Die Momentaufnahme Sitzung tritt nach <a href="gg269229(v=exchg.10).md">jeto ssnapshotthaw</a> auf und erfordert einen <a href="gg294136(v=exchg.10).md">jedessnapshotend</a> -Funktions Aufruf.</span><span class="sxs-lookup"><span data-stu-id="39c76-124">The snapshot session occurs after <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> and will require a <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd</a> function call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c76-125">JET_bitExplicitPrepare</span><span class="sxs-lookup"><span data-stu-id="39c76-125">JET_bitExplicitPrepare</span></span></p></td>
<td><p><span data-ttu-id="39c76-126">Standardmäßig werden keine Instanzen vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="39c76-126">No instances will be prepared by default.</span></span></p>
<p><span data-ttu-id="39c76-127"><strong>Windows 7:</strong>  JET_bitExplicitPrepare wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="39c76-127"><strong>Windows 7:</strong>  JET_bitExplicitPrepare is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="39c76-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39c76-128">Return Value</span></span>

<span data-ttu-id="39c76-129">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="39c76-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="39c76-130">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="39c76-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39c76-131">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="39c76-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="39c76-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39c76-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39c76-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="39c76-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="39c76-134">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="39c76-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c76-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="39c76-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="39c76-136">Der Momentaufnahme-ID-Zeiger ist NULL, oder der <em>grbit</em> -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="39c76-136">The snapshot ID pointer is NULL or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c76-137">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="39c76-137">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="39c76-138">Eine Momentaufnahme Sitzung wird bereits ausgeführt, und der Vorgang darf nicht mehr als eine Momentaufnahme Sitzung zu einem bestimmten Zeitpunkt aufweisen.</span><span class="sxs-lookup"><span data-stu-id="39c76-138">A snapshot session is already in progress and the operation is not allowed to have more then one snapshot session at any given time.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="39c76-139">Wenn diese Funktion erfolgreich ausgeführt wird, kann eine Momentaufnahme Sitzung jederzeit mit der e/a-Sperr Phase gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="39c76-139">If this function succeeds, a snapshot session will be able to start at any time with the IO freeze phase.</span></span> <span data-ttu-id="39c76-140">Der Bezeichner für die Sitzung wird zurückgegeben und muss in den nachfolgenden Aufrufen für die Momentaufnahme Sitzung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39c76-140">The identifier for the session will be returned and must be used in the subsequent calls for the snapshot session.</span></span>

<span data-ttu-id="39c76-141">Die laufenden Instanzen der Engine werden nun als Teil der Momentaufnahme Sitzung betrachtet.</span><span class="sxs-lookup"><span data-stu-id="39c76-141">The running instances of the engine will now be considered part of the snapshot session.</span></span>

<span data-ttu-id="39c76-142">**Windows Vista:**  Um eine andere Teilmenge von Instanzen anzugeben, kann die [jechanssnapshotprepareinstance](./jetossnapshotprepareinstance-function.md) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="39c76-142">**Windows Vista:**  To specify a different subset of instances, the [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) can be called.</span></span>

<span data-ttu-id="39c76-143">Der reguläre API-Sequenz Aufruf lautet: **jedessnapshotprepare**, optional gefolgt von einem oder mehreren Aufrufen von [jedessnapshotprepareinstance](./jetossnapshotprepareinstance-function.md)und anschließendem [jeto ssnapshotfreeze](./jetossnapshotfreeze-function.md).</span><span class="sxs-lookup"><span data-stu-id="39c76-143">The normal API sequence call is: **JetOSSnapshotPrepare**, optionally followed by one or more calls to [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md), then followed by [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span></span> <span data-ttu-id="39c76-144">Nachdem das Einfrieren gestartet wurde, kann es mit [jeto ssnapshotthaw](./jetossnapshotthaw-function.md)beendet werden.</span><span class="sxs-lookup"><span data-stu-id="39c76-144">Once the freeze is started, it can be terminated using [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span> <span data-ttu-id="39c76-145">Nach der Vorbereitung kann die Momentaufnahme Sitzung jederzeit mit [jedessnapshotabort](./jetossnapshotabort-function.md)beendet werden.</span><span class="sxs-lookup"><span data-stu-id="39c76-145">At any time after the prepare, the snapshot session can be abruptly terminated with [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span></span>

<span data-ttu-id="39c76-146">Wenn JET_bitContinueAfterThaw nach [jedessnapshotthaw](./jetossnapshotthaw-function.md)angegeben wird, bleibt die Momentaufnahme Sitzung erhalten (obwohl die e/a-Vorgänge fortgesetzt werden).</span><span class="sxs-lookup"><span data-stu-id="39c76-146">If JET_bitContinueAfterThaw is specified after [JetOSSnapshotThaw](./jetossnapshotthaw-function.md), the snapshot session will remain (although the I/O will resume).</span></span> <span data-ttu-id="39c76-147">Dadurch wird die Momentaufnahme überprüft, und bei Bedarf wird die Protokoll Verkürzung mithilfe von [jetossnapshottruneurelog](./jetossnapshottruncatelog-function.md) aktiviert, und es wird ein Anruf von [jetossnapshotend](./jetossnapshotend-function.md)benötigt.</span><span class="sxs-lookup"><span data-stu-id="39c76-147">This will enable a verification of the snapshot, and if needed, will enable log truncation using [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) and will require a call to [JetOSSnapshotEnd](./jetossnapshotend-function.md).</span></span>

<span data-ttu-id="39c76-148">Wenn diese Funktion fehlschlägt, erfolgt keine Änderung des Engine-Zustands.</span><span class="sxs-lookup"><span data-stu-id="39c76-148">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="39c76-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39c76-149">Remarks</span></span>

<span data-ttu-id="39c76-150">Ereignisprotokoll Einträge werden für die verschiedenen Schritte der Momentaufnahme generiert.</span><span class="sxs-lookup"><span data-stu-id="39c76-150">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="39c76-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39c76-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39c76-152"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="39c76-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="39c76-153">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="39c76-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c76-154"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="39c76-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="39c76-155">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="39c76-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c76-156"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="39c76-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="39c76-157">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="39c76-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c76-158"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="39c76-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="39c76-159">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="39c76-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c76-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="39c76-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="39c76-161">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="39c76-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="39c76-162">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="39c76-162">See Also</span></span>

[<span data-ttu-id="39c76-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="39c76-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="39c76-164">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="39c76-164">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="39c76-165">Jejessnapshotabort</span><span class="sxs-lookup"><span data-stu-id="39c76-165">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="39c76-166">Jeto ssnapshotend</span><span class="sxs-lookup"><span data-stu-id="39c76-166">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="39c76-167">Jeto ssnapshotfreeze</span><span class="sxs-lookup"><span data-stu-id="39c76-167">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="39c76-168">Jejessnapshotprepareingestance</span><span class="sxs-lookup"><span data-stu-id="39c76-168">JetOSSnapshotPrepareInstance</span></span>](./jetossnapshotprepareinstance-function.md)  
[<span data-ttu-id="39c76-169">Jejessnapshotthaw</span><span class="sxs-lookup"><span data-stu-id="39c76-169">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)  
[<span data-ttu-id="39c76-170">Jeto ssnapshottruneurelog</span><span class="sxs-lookup"><span data-stu-id="39c76-170">JetOSSnapshotTruncateLog</span></span>](./jetossnapshottruncatelog-function.md)
