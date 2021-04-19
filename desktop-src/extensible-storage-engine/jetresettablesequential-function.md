---
description: 'Weitere Informationen zu: jetresettablesequential-Funktion'
title: Jetresettablesequential-Funktion
TOCTitle: JetResetTableSequential Function
ms:assetid: 5fe9daf2-5ef1-46d6-b0c3-ef92fb57d8bb
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269261(v=EXCHG.10)
ms:contentKeyID: 32765563
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetResetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86de80ac935af81fd2b4e8fdfef8b20dbb8d27d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349890"
---
# <a name="jetresettablesequential-function"></a><span data-ttu-id="e8d5e-103">Jetresettablesequential-Funktion</span><span class="sxs-lookup"><span data-stu-id="e8d5e-103">JetResetTableSequential Function</span></span>


<span data-ttu-id="e8d5e-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e8d5e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetresettablesequential-function"></a><span data-ttu-id="e8d5e-105">Jetresettablesequential-Funktion</span><span class="sxs-lookup"><span data-stu-id="e8d5e-105">JetResetTableSequential Function</span></span>

<span data-ttu-id="e8d5e-106">Die **jetresettablesequential** -Funktion benachrichtigt die Datenbank-Engine, dass die Anwendung den gesamten aktuellen Index, der einen bestimmten Cursor enthält, nicht mehr scannt.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-106">The **JetResetTableSequential** function notifies the database engine that the application is no longer scanning the entire current index containing a given cursor.</span></span> <span data-ttu-id="e8d5e-107">Dieser Rückruf kehrt eine von [jetsettablesequential](./jetsettablesequential-function.md)gesendete Benachrichtigung um.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-107">This call reverses a notification sent by [JetSetTableSequential](./jetsettablesequential-function.md).</span></span>

<span data-ttu-id="e8d5e-108">**Windows XP:**   **jetresettablesequential** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-108">**Windows XP:**   **JetResetTableSequential** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetResetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="e8d5e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8d5e-109">Parameters</span></span>

<span data-ttu-id="e8d5e-110">*-sid*</span><span class="sxs-lookup"><span data-stu-id="e8d5e-110">*sesid*</span></span>

<span data-ttu-id="e8d5e-111">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-111">The session to use for this call.</span></span>

<span data-ttu-id="e8d5e-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="e8d5e-112">*tableid*</span></span>

<span data-ttu-id="e8d5e-113">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-113">The cursor to use for this call.</span></span>

<span data-ttu-id="e8d5e-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e8d5e-114">*grbit*</span></span>

<span data-ttu-id="e8d5e-115">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-115">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="e8d5e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8d5e-116">Return Value</span></span>

<span data-ttu-id="e8d5e-117">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e8d5e-118">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e8d5e-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8d5e-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e8d5e-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="e8d5e-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8d5e-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8d5e-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e8d5e-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e8d5e-122">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8d5e-123">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e8d5e-123">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e8d5e-124">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-124">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8d5e-125">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e8d5e-125">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e8d5e-126">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-126">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="e8d5e-127">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8d5e-128">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e8d5e-128">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e8d5e-129">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-129">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8d5e-130">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e8d5e-130">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e8d5e-131">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-131">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8d5e-132">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e8d5e-132">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e8d5e-133">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-133">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e8d5e-134">Bei Erfolg ist der aktuelle Index des Cursors nicht mehr für einen sequenziellen Scan des gesamten Indexes optimiert.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-134">On success, the current index of the cursor is no longer optimized for a sequential scan of the entire index.</span></span> <span data-ttu-id="e8d5e-135">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-135">No change to the database state will occur.</span></span>

<span data-ttu-id="e8d5e-136">Bei einem Fehler tritt keine Änderung an der Konfiguration des Cursors auf.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-136">On failure, no change to the configuration of the cursor will occur.</span></span> <span data-ttu-id="e8d5e-137">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-137">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e8d5e-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8d5e-138">Remarks</span></span>

<span data-ttu-id="e8d5e-139">Es ist sicher, diesen Vorgang für einen Cursor durchführen zu lassen, der zuvor nicht durch einen-Befehl von [jetsettablesequenziell](./jetsettablesequential-function.md)konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-139">It is safe to make this call against a cursor that has not been previously configured by a call to [JetSetTableSequential](./jetsettablesequential-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="e8d5e-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8d5e-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8d5e-141"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e8d5e-141"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e8d5e-142">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-142">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8d5e-143"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e8d5e-143"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e8d5e-144">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-144">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8d5e-145"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e8d5e-145"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e8d5e-146">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-146">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8d5e-147"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="e8d5e-147"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e8d5e-148">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-148">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8d5e-149"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e8d5e-149"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e8d5e-150">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e8d5e-150">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e8d5e-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e8d5e-151">See Also</span></span>

[<span data-ttu-id="e8d5e-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e8d5e-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e8d5e-153">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e8d5e-153">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e8d5e-154">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e8d5e-154">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e8d5e-155">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e8d5e-155">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e8d5e-156">Jetsettablesequential</span><span class="sxs-lookup"><span data-stu-id="e8d5e-156">JetSetTableSequential</span></span>](./jetsettablesequential-function.md)  
[<span data-ttu-id="e8d5e-157">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="e8d5e-157">JetStopService</span></span>](./jetstopservice-function.md)
