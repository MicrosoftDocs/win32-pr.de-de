---
description: 'Weitere Informationen zu: jeesssnapshottruneurelog-Funktion'
title: Jeto ssnapshottruneurelog-Funktion
TOCTitle: JetOSSnapshotTruncateLog Function
ms:assetid: 3df8f5b2-8083-49b7-a325-fd13187f785c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269231(v=EXCHG.10)
ms:contentKeyID: 32765533
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0a3cebd743a3c8cd9a3d86f1f637dcb5b2c9c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364152"
---
# <a name="jetossnapshottruncatelog-function"></a><span data-ttu-id="c485a-103">Jeto ssnapshottruneurelog-Funktion</span><span class="sxs-lookup"><span data-stu-id="c485a-103">JetOSSnapshotTruncateLog Function</span></span>


<span data-ttu-id="c485a-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c485a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshottruncatelog-function"></a><span data-ttu-id="c485a-105">Jeto ssnapshottruneurelog-Funktion</span><span class="sxs-lookup"><span data-stu-id="c485a-105">JetOSSnapshotTruncateLog Function</span></span>

<span data-ttu-id="c485a-106">Die **jetossnapshottruneurelog** -Funktion ermöglicht das Abschneiden von Protokollen für alle Instanzen, die Teil der Momentaufnahme Sitzung sind.</span><span class="sxs-lookup"><span data-stu-id="c485a-106">The **JetOSSnapshotTruncateLog** function enables log truncation for all instances that are part of the snapshot session.</span></span>

<span data-ttu-id="c485a-107">**Windows Vista:**  **jedessnapshottruneurelog** wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c485a-107">**Windows Vista:**  **JetOSSnapshotTruncateLog** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLog(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="c485a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c485a-108">Parameters</span></span>

<span data-ttu-id="c485a-109">*snapid*</span><span class="sxs-lookup"><span data-stu-id="c485a-109">*snapId*</span></span>

<span data-ttu-id="c485a-110">Der Bezeichner der Momentaufnahme Sitzung.</span><span class="sxs-lookup"><span data-stu-id="c485a-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="c485a-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="c485a-111">*grbit*</span></span>

<span data-ttu-id="c485a-112">Die Optionen für diesen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="c485a-112">The options for this call.</span></span> <span data-ttu-id="c485a-113">Dieser Parameter kann eine Kombination der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c485a-113">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c485a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c485a-114">Value</span></span></p></th>
<th><p><span data-ttu-id="c485a-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c485a-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c485a-116">JET_bitAllDatabasesSnapshot</span><span class="sxs-lookup"><span data-stu-id="c485a-116">JET_bitAllDatabasesSnapshot</span></span></p></td>
<td><p><span data-ttu-id="c485a-117">Alle Datenbanken werden angefügt, sodass die Speicher-Engine die Protokoll Verkürzung berechnen und durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="c485a-117">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c485a-118">0 (null)</span><span class="sxs-lookup"><span data-stu-id="c485a-118">0 (zero)</span></span></p></td>
<td><p><span data-ttu-id="c485a-119">Es erfolgt kein abschneiden.</span><span class="sxs-lookup"><span data-stu-id="c485a-119">No truncation will occur.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="c485a-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c485a-120">Return Value</span></span>

<span data-ttu-id="c485a-121">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="c485a-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c485a-122">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c485a-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c485a-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c485a-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="c485a-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c485a-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c485a-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c485a-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c485a-126">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c485a-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c485a-127">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="c485a-127">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="c485a-128">Der <em>grbit</em> -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c485a-128">The <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c485a-129">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="c485a-129">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="c485a-130">Die Momentaufnahme Sitzung befindet sich nicht in dem Status, in dem ein Abschneiden erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="c485a-130">The snapshot session is not in the state in which a truncation can occur.</span></span> <span data-ttu-id="c485a-131">Mögliche Ursachen sind:</span><span class="sxs-lookup"><span data-stu-id="c485a-131">Possible causes are:</span></span></p>
<ul>
<li><p><span data-ttu-id="c485a-132">der-Vorgang erfolgt nach dem Timeout der Momentaufnahme Sitzung.</span><span class="sxs-lookup"><span data-stu-id="c485a-132">the call is done after the snapshot session timed-out</span></span></p></li>
<li><p><span data-ttu-id="c485a-133">die Sitzung wurde als Kopier Momentaufnahme angegeben.</span><span class="sxs-lookup"><span data-stu-id="c485a-133">the session was specified as a copy snapshot</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c485a-134">Bei Erfolg werden die Protokolldateien für eine oder alle Instanzen, die Teil der Momentaufnahme Sitzung sind, nach Möglichkeit abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="c485a-134">On success, the log files for one or all the instances part of the snapshot session will be truncated, if possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c485a-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c485a-135">Remarks</span></span>

<span data-ttu-id="c485a-136">Diese Funktion sollte nur aufgerufen werden, wenn die Momentaufnahme mit der JET_bitContinueAfterThaw-Option erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c485a-136">This function should be called only if the snapshot was created with the JET_bitContinueAfterThaw option.</span></span> <span data-ttu-id="c485a-137">Andernfalls würde die Momentaufnahme Sitzung nach dem [jedessnapshotthaw](./jetossnapshotthaw-function.md) -Befehl beendet werden.</span><span class="sxs-lookup"><span data-stu-id="c485a-137">Otherwise, the snapshot session would have ended after the [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) call.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c485a-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c485a-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c485a-139"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c485a-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c485a-140">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c485a-140">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c485a-141"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c485a-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c485a-142">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c485a-142">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c485a-143"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c485a-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c485a-144">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="c485a-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c485a-145"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="c485a-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c485a-146">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c485a-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c485a-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c485a-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c485a-148">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c485a-148">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c485a-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c485a-149">See Also</span></span>

[<span data-ttu-id="c485a-150">Fehler Behandlungsparameter</span><span class="sxs-lookup"><span data-stu-id="c485a-150">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="c485a-151">Erweiterbare Speicher-Engine-Fehler</span><span class="sxs-lookup"><span data-stu-id="c485a-151">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="c485a-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c485a-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c485a-153">Jeto ssnapshotend</span><span class="sxs-lookup"><span data-stu-id="c485a-153">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="c485a-154">Jeto ssnapshotfreeze</span><span class="sxs-lookup"><span data-stu-id="c485a-154">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="c485a-155">Jejessnapshotprepare</span><span class="sxs-lookup"><span data-stu-id="c485a-155">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="c485a-156">Jejessnapshotthaw</span><span class="sxs-lookup"><span data-stu-id="c485a-156">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
