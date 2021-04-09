---
description: Weitere Informationen finden Sie in der Funktion "jeto ssnapshotend".
title: Jeto ssnapshotend-Funktion
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de1237de9af0b1b75f645346fc30a128a1b8e907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128169"
---
# <a name="jetossnapshotend-function"></a><span data-ttu-id="35a5c-103">Jeto ssnapshotend-Funktion</span><span class="sxs-lookup"><span data-stu-id="35a5c-103">JetOSSnapshotEnd Function</span></span>


<span data-ttu-id="35a5c-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="35a5c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotend-function"></a><span data-ttu-id="35a5c-105">Jeto ssnapshotend-Funktion</span><span class="sxs-lookup"><span data-stu-id="35a5c-105">JetOSSnapshotEnd Function</span></span>

<span data-ttu-id="35a5c-106">Die **jedessnapshotend** -Funktion benachrichtigt die Engine, dass die Momentaufnahme Sitzung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="35a5c-106">The **JetOSSnapshotEnd** function notifies the engine that the snapshot session finished.</span></span>

<span data-ttu-id="35a5c-107">**Windows Vista:**  **jedessnapshotend** wird in Windows Vista eingeführt:.</span><span class="sxs-lookup"><span data-stu-id="35a5c-107">**Windows Vista:**  **JetOSSnapshotEnd** is introduced in Windows Vista:.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="35a5c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="35a5c-108">Parameters</span></span>

<span data-ttu-id="35a5c-109">*snapid*</span><span class="sxs-lookup"><span data-stu-id="35a5c-109">*snapId*</span></span>

<span data-ttu-id="35a5c-110">Der Bezeichner der Momentaufnahme Sitzung.</span><span class="sxs-lookup"><span data-stu-id="35a5c-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="35a5c-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="35a5c-111">*grbit*</span></span>

<span data-ttu-id="35a5c-112">Die Optionen für diesen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="35a5c-112">The options for this call.</span></span> <span data-ttu-id="35a5c-113">Dieser Parameter kann eine Kombination der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="35a5c-113">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35a5c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="35a5c-114">Value</span></span></p></th>
<th><p><span data-ttu-id="35a5c-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="35a5c-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35a5c-116">0</span><span class="sxs-lookup"><span data-stu-id="35a5c-116">0</span></span></p></td>
<td><p><span data-ttu-id="35a5c-117">Das erfolgreiche Ende der Momentaufnahme Sitzung.</span><span class="sxs-lookup"><span data-stu-id="35a5c-117">The successful end of the snapshot session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35a5c-118">JET_bitAbortSnapshot</span><span class="sxs-lookup"><span data-stu-id="35a5c-118">JET_bitAbortSnapshot</span></span></p></td>
<td><p><span data-ttu-id="35a5c-119">Die Momentaufnahme Sitzung wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="35a5c-119">The snapshot session aborted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="35a5c-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35a5c-120">Return Value</span></span>

<span data-ttu-id="35a5c-121">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="35a5c-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="35a5c-122">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="35a5c-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35a5c-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="35a5c-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="35a5c-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35a5c-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35a5c-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="35a5c-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="35a5c-126">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="35a5c-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35a5c-127">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="35a5c-127">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="35a5c-128">Eine der angeforderten Optionen ist ungültig, wird falsch oder nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="35a5c-128">One of the options requested is invalid, used incorrectly, or not implemented.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35a5c-129">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="35a5c-129">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="35a5c-130">Eine Momentaufnahme Sitzung wird bereits ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35a5c-130">A snapshot session is already in progress.</span></span> <span data-ttu-id="35a5c-131">Dies ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="35a5c-131">This is not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35a5c-132">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="35a5c-132">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="35a5c-133">Der Bezeichner für die Momentaufnahme Sitzung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="35a5c-133">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35a5c-134">JET_errOSSnapshotTimeOut</span><span class="sxs-lookup"><span data-stu-id="35a5c-134">JET_errOSSnapshotTimeOut</span></span></p></td>
<td><p><span data-ttu-id="35a5c-135">In der Momentaufnahme Sitzung war vor dem Auftreten dieses Aufrufes ein internes Timeout aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="35a5c-135">The snapshot session had an internal timeout before this call occurred.</span></span> <span data-ttu-id="35a5c-136">Folglich werden die e/a-Vorgänge vor dem Auftreten dieses Aufrufes normal zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="35a5c-136">As a result, the IO operations returned to normal before this call was made.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="35a5c-137">Wenn diese Funktion erfolgreich ausgeführt wird, wird eine Momentaufnahme Sitzung abgeschlossen, und das normale Engine-Verhalten wird fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="35a5c-137">If this function succeeds, a snapshot session will complete and the normal engine behavior will resume.</span></span> <span data-ttu-id="35a5c-138">Eine neue Momentaufnahme Sitzung kann später gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="35a5c-138">A new snapshot session can be started later.</span></span>

<span data-ttu-id="35a5c-139">Wenn diese Funktion fehlschlägt, gibt der JET_errOSSnapshotTimeOut Rückgabecode zurück, und die aktuelle Momentaufnahme Sitzung wird beendet, aber das Einfrieren von IOS während des Momentaufnahme Zeitraums wurde intern nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="35a5c-139">If this function fails, the JET_errOSSnapshotTimeOut return code returns and the current snapshot session ends but the freeze of IOs during the snapshot period was not respected internally.</span></span> <span data-ttu-id="35a5c-140">Bei allen anderen Fehlern wird der Sitzungs Status der Momentaufnahme nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="35a5c-140">For all other errors, the snapshot session state will not be changed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="35a5c-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35a5c-141">Remarks</span></span>

<span data-ttu-id="35a5c-142">Diese Funktion wird nur aufgerufen, wenn [jeto ssnapshotthaw](./jetossnapshotthaw-function.md) mit JET_bitContinueAfterThaw aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="35a5c-142">This function is called only if [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) was called with JET_bitContinueAfterThaw.</span></span>

<span data-ttu-id="35a5c-143">Die Momentaufnahme Sitzung muss fertiggestellt werden, damit die Momentaufnahme Überprüfung und das Abschneiden des Protokolls stattfinden.</span><span class="sxs-lookup"><span data-stu-id="35a5c-143">The snapshot session must complete for the snapshot verification and log truncation to take place.</span></span> <span data-ttu-id="35a5c-144">Ereignisprotokoll Einträge werden für die verschiedenen Schritte der Momentaufnahme generiert.</span><span class="sxs-lookup"><span data-stu-id="35a5c-144">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="35a5c-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35a5c-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35a5c-146"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="35a5c-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="35a5c-147">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="35a5c-147">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35a5c-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="35a5c-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="35a5c-149">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="35a5c-149">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35a5c-150"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="35a5c-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="35a5c-151">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="35a5c-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35a5c-152"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="35a5c-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="35a5c-153">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="35a5c-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35a5c-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="35a5c-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="35a5c-155">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="35a5c-155">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="35a5c-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="35a5c-156">See Also</span></span>

[<span data-ttu-id="35a5c-157">Fehler Behandlungsparameter</span><span class="sxs-lookup"><span data-stu-id="35a5c-157">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="35a5c-158">Erweiterbare Speicher-Engine-Fehler</span><span class="sxs-lookup"><span data-stu-id="35a5c-158">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="35a5c-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="35a5c-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="35a5c-160">Jejessnapshotthaw</span><span class="sxs-lookup"><span data-stu-id="35a5c-160">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
