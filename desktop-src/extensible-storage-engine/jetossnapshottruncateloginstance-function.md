---
description: 'Weitere Informationen finden Sie hier: jejessnapshottruneureloginstance-Funktion'
title: Jejessnapshottruneureloginstance-Funktion
TOCTitle: JetOSSnapshotTruncateLogInstance Function
ms:assetid: ddc51957-5b89-4abf-9193-c34ef626a63e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294115(v=EXCHG.10)
ms:contentKeyID: 32765729
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLogInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cef30d012c28c809bb35d59a82fd596ba69bd175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749704"
---
# <a name="jetossnapshottruncateloginstance-function"></a><span data-ttu-id="f76c4-103">Jejessnapshottruneureloginstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="f76c4-103">JetOSSnapshotTruncateLogInstance Function</span></span>


<span data-ttu-id="f76c4-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f76c4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshottruncateloginstance-function"></a><span data-ttu-id="f76c4-105">Jejessnapshottruneureloginstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="f76c4-105">JetOSSnapshotTruncateLogInstance Function</span></span>

<span data-ttu-id="f76c4-106">Die **jetossnapshottruneureloginstance** -Funktion verkürzt das Protokoll für eine angegebene Instanz während einer Momentaufnahme Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f76c4-106">The **JetOSSnapshotTruncateLogInstance** function truncates the log for a specified instance during a snapshot session.</span></span>

<span data-ttu-id="f76c4-107">**Windows Vista:**  **jedessnapshottruneureloginstance** wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f76c4-107">**Windows Vista:**  **JetOSSnapshotTruncateLogInstance** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLogInstance(
      __in          const JET_OSSNAPID snapId,
      __in          JET_INSTANCE instance,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="f76c4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f76c4-108">Parameters</span></span>

<span data-ttu-id="f76c4-109">*snapid*</span><span class="sxs-lookup"><span data-stu-id="f76c4-109">*snapId*</span></span>

<span data-ttu-id="f76c4-110">Der Bezeichner der Momentaufnahme Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f76c4-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="f76c4-111">*lichen*</span><span class="sxs-lookup"><span data-stu-id="f76c4-111">*instance*</span></span>

<span data-ttu-id="f76c4-112">Die-Instanz, die für diesen-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f76c4-112">The instance that will be used for this call.</span></span>

<span data-ttu-id="f76c4-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f76c4-113">*grbit*</span></span>

<span data-ttu-id="f76c4-114">Die Optionen für diesen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="f76c4-114">The options for this call.</span></span> <span data-ttu-id="f76c4-115">Dieser Parameter kann eine Kombination der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f76c4-115">This parameter can have a combination of the following values.</span></span>

<span data-ttu-id="f76c4-116">bei *grbit* kann es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="f76c4-116">*grbit* can be one of the following values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f76c4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f76c4-117">Value</span></span></p></th>
<th><p><span data-ttu-id="f76c4-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f76c4-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f76c4-119">JET_bitAllDatabasesSnapshot</span><span class="sxs-lookup"><span data-stu-id="f76c4-119">JET_bitAllDatabasesSnapshot</span></span></p></td>
<td><p><span data-ttu-id="f76c4-120">Alle Datenbanken werden angefügt, sodass die Speicher-Engine die Protokoll Verkürzung berechnen und durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="f76c4-120">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f76c4-121">0 (null)</span><span class="sxs-lookup"><span data-stu-id="f76c4-121">0 (zero)</span></span></p></td>
<td><p><span data-ttu-id="f76c4-122">Es erfolgt kein abschneiden.</span><span class="sxs-lookup"><span data-stu-id="f76c4-122">No truncation will occur.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f76c4-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f76c4-123">Return Value</span></span>

<span data-ttu-id="f76c4-124">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="f76c4-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f76c4-125">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f76c4-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f76c4-126">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f76c4-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="f76c4-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f76c4-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f76c4-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f76c4-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f76c4-129">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f76c4-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f76c4-130">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="f76c4-130">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="f76c4-131">Der <em>grbit</em> -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f76c4-131">The <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f76c4-132">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="f76c4-132">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="f76c4-133">Die Momentaufnahme Sitzung befindet sich nicht in dem Status, in dem ein Abschneiden erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="f76c4-133">The snapshot session is not in the state in which a truncation can occur.</span></span> <span data-ttu-id="f76c4-134">Mögliche Ursachen sind:</span><span class="sxs-lookup"><span data-stu-id="f76c4-134">Possible causes are:</span></span></p>
<ul>
<li><p><span data-ttu-id="f76c4-135">Der-Vorgang wird abgeschlossen, nachdem die Momentaufnahme Sitzung abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="f76c4-135">The call completes after the snapshot session timed out.</span></span></p></li>
<li><p><span data-ttu-id="f76c4-136">Die Sitzung wurde als Kopier Momentaufnahme angegeben.</span><span class="sxs-lookup"><span data-stu-id="f76c4-136">The session was specified as a copy snapshot.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f76c4-137">Wenn diese Funktion erfolgreich ausgeführt wird, werden die Protokolldateien für eine oder alle Instanzen, die Teil der Momentaufnahme Sitzung sind, nach Möglichkeit abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="f76c4-137">If this function succeeds, the log files for one or all of the instances that are part of the snapshot session will be truncated, if possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f76c4-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f76c4-138">Remarks</span></span>

<span data-ttu-id="f76c4-139">Diese Funktion sollte nur aufgerufen werden, wenn die Momentaufnahme mit der JET_bitContinueAfterThaw-Option erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f76c4-139">This function should be called only if the snapshot was created with the JET_bitContinueAfterThaw option.</span></span> <span data-ttu-id="f76c4-140">Andernfalls wird die Momentaufnahme Sitzung nach dem Rückruf von [jedessnapshotthaw](./jetossnapshotthaw-function.md)beendet.</span><span class="sxs-lookup"><span data-stu-id="f76c4-140">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="f76c4-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f76c4-141">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f76c4-142"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f76c4-142"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f76c4-143">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f76c4-143">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f76c4-144"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f76c4-144"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f76c4-145">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f76c4-145">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f76c4-146"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f76c4-146"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f76c4-147">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="f76c4-147">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f76c4-148"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="f76c4-148"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f76c4-149">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f76c4-149">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f76c4-150"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f76c4-150"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f76c4-151">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f76c4-151">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f76c4-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f76c4-152">See Also</span></span>

[<span data-ttu-id="f76c4-153">Fehler Behandlungsparameter</span><span class="sxs-lookup"><span data-stu-id="f76c4-153">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="f76c4-154">Erweiterbare Speicher-Engine-Fehler</span><span class="sxs-lookup"><span data-stu-id="f76c4-154">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="f76c4-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f76c4-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f76c4-156">Jeto ssnapshotend</span><span class="sxs-lookup"><span data-stu-id="f76c4-156">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="f76c4-157">Jeto ssnapshotfreeze</span><span class="sxs-lookup"><span data-stu-id="f76c4-157">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="f76c4-158">Jejessnapshotprepare</span><span class="sxs-lookup"><span data-stu-id="f76c4-158">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="f76c4-159">Jejessnapshotthaw</span><span class="sxs-lookup"><span data-stu-id="f76c4-159">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
