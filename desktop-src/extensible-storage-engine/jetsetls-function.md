---
description: 'Weitere Informationen zu: jetsetls-Funktion'
title: JetSetLS-Funktion
TOCTitle: JetSetLS Function
ms:assetid: 4fc77e09-7173-42e8-9dfd-9a8d8de2fb9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269243(v=EXCHG.10)
ms:contentKeyID: 32765545
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetLS
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae1c68a039c11cd8a3f9b1299494c5057513caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525556"
---
# <a name="jetsetls-function"></a><span data-ttu-id="96e94-103">JetSetLS-Funktion</span><span class="sxs-lookup"><span data-stu-id="96e94-103">JetSetLS Function</span></span>


<span data-ttu-id="96e94-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="96e94-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetls-function"></a><span data-ttu-id="96e94-105">JetSetLS-Funktion</span><span class="sxs-lookup"><span data-stu-id="96e94-105">JetSetLS Function</span></span>

<span data-ttu-id="96e94-106">Die **jetsetls** -Funktion ermöglicht es der Anwendung, ein Kontext Handle, das als lokaler Speicher bezeichnet wird, einem Cursor oder der diesem Cursor zugeordneten Tabelle zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="96e94-106">The **JetSetLS** function enables the application to associate a context handle known as Local Storage with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="96e94-107">Dieses Kontext Handle kann von der Anwendung verwendet werden, um zusätzliche Daten zu speichern, die einem Cursor oder einer Tabelle zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="96e94-107">This context handle can be used by the application to store auxiliary data that is associated with a cursor or table.</span></span> <span data-ttu-id="96e94-108">Die Anwendung wird später mithilfe eines Lauf Zeit Rückrufs benachrichtigt, wenn das Kontext Handle freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="96e94-108">The application is later notified using a runtime callback when the context handle must be released.</span></span> <span data-ttu-id="96e94-109">Dadurch ist es möglich, einem Cursor oder einer Tabelle dynamisch zugeordneten Zustand zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="96e94-109">This makes it possible to associate dynamically allocated state with a cursor or table.</span></span>

<span data-ttu-id="96e94-110">**Windows XP:**  **jetsetls** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="96e94-110">**Windows XP:**  **JetSetLS** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="96e94-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="96e94-111">Parameters</span></span>

<span data-ttu-id="96e94-112">*-sid*</span><span class="sxs-lookup"><span data-stu-id="96e94-112">*sesid*</span></span>

<span data-ttu-id="96e94-113">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="96e94-113">The session to use for this call.</span></span>

<span data-ttu-id="96e94-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="96e94-114">*tableid*</span></span>

<span data-ttu-id="96e94-115">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="96e94-115">The cursor to use for this call.</span></span>

<span data-ttu-id="96e94-116">*ls*</span><span class="sxs-lookup"><span data-stu-id="96e94-116">*ls*</span></span>

<span data-ttu-id="96e94-117">Das Kontext Handle, das dem Cursor oder der Tabelle zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="96e94-117">The context handle to be associated with the cursor or table.</span></span>

<span data-ttu-id="96e94-118">Wenn JET_bitLSReset angegeben wird, wird der tatsächliche Wert dieses Parameters ignoriert und JET_LSNil verwendet.</span><span class="sxs-lookup"><span data-stu-id="96e94-118">When JET_bitLSReset is specified then the actual value of this parameter is ignored and JET_LSNil is used.</span></span>

<span data-ttu-id="96e94-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="96e94-119">*grbit*</span></span>

<span data-ttu-id="96e94-120">Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="96e94-120">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96e94-121">Wert</span><span class="sxs-lookup"><span data-stu-id="96e94-121">Value</span></span></p></th>
<th><p><span data-ttu-id="96e94-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="96e94-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96e94-123">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="96e94-123">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="96e94-124">Diese Option gibt an, dass das Kontext Handle dem angegebenen Cursor zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="96e94-124">This option indicates that the context handle should be associated with the given cursor.</span></span></p>
<p><span data-ttu-id="96e94-125">Wenn weder JET_bitLSCursor noch JET_bitLSTable angegeben wird, wird JET_bitLSCursor angenommen.</span><span class="sxs-lookup"><span data-stu-id="96e94-125">If neither JET_bitLSCursor nor JET_bitLSTable is specified then JET_bitLSCursor is presumed.</span></span></p>
<p><span data-ttu-id="96e94-126">Diese Option kann nicht mit JET_bitLSTable verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96e94-126">It is illegal to use this option with JET_bitLSTable.</span></span> <span data-ttu-id="96e94-127">Der Vorgang schlägt mit JET_errInvalidgrbit fehl, wenn ein Versuch unternommen wird.</span><span class="sxs-lookup"><span data-stu-id="96e94-127">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96e94-128">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="96e94-128">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="96e94-129">Diese Option gibt an, dass das angegebene Kontext Handle ignoriert werden soll und dass das Kontext Handle für das ausgewählte Objekt auf JET_LSNil zurückgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="96e94-129">This option indicates that the specified context handle should be ignored and that the context handle for the chosen object should be reset to JET_LSNil.</span></span></p>
<p><span data-ttu-id="96e94-130">Beachten Sie, dass diese Aktion nicht zu einem Rückruf führt, um den vorherigen Wert des Kontext Handles für das ausgewählte Objekt zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="96e94-130">It is important to note that this action will not result in a callback to cleanup the previous value of the context handle for the chosen object.</span></span> <span data-ttu-id="96e94-131">Eine ordnungsgemäße Bereinigung des vorherigen Kontext Handles kann mithilfe von <a href="gg269234(v=exchg.10).md">jetgetls</a> mit JET_bitLSReset erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="96e94-131">Proper cleanup of the previous context handle can be achieved using <a href="gg269234(v=exchg.10).md">JetGetLS</a> with JET_bitLSReset.</span></span> <span data-ttu-id="96e94-132">Weitere Informationen finden Sie unter <a href="gg269234(v=exchg.10).md">jetgetls</a> .</span><span class="sxs-lookup"><span data-stu-id="96e94-132">See <a href="gg269234(v=exchg.10).md">JetGetLS</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96e94-133">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="96e94-133">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="96e94-134">Diese Option gibt an, dass das Kontext Handle der Tabelle zugeordnet werden soll, die dem angegebenen Cursor zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="96e94-134">This option indicates that the context handle should be associated with the table associated with the given cursor.</span></span></p>
<p><span data-ttu-id="96e94-135">Diese Option kann nicht mit JET_bitLSCursor verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96e94-135">It is illegal to use this option with JET_bitLSCursor.</span></span> <span data-ttu-id="96e94-136">Der Vorgang schlägt mit JET_errInvalidgrbit fehl, wenn ein Versuch unternommen wird.</span><span class="sxs-lookup"><span data-stu-id="96e94-136">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="96e94-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96e94-137">Return Value</span></span>

<span data-ttu-id="96e94-138">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="96e94-138">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="96e94-139">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="96e94-139">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96e94-140">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="96e94-140">Return code</span></span></p></th>
<th><p><span data-ttu-id="96e94-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96e94-141">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96e94-142">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="96e94-142">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="96e94-143">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="96e94-143">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96e94-144">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="96e94-144">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="96e94-145">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="96e94-145">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96e94-146">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="96e94-146">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="96e94-147">Eine der angeforderten Optionen war ungültig, wurde falsch verwendet oder nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="96e94-147">One of the options requested was invalid, used incorrectly, or not implemented.</span></span> <span data-ttu-id="96e94-148">Dies kann bei <strong>jetsetls</strong> vorkommen, wenn JET_bitLSCursor und JET_bitLSTable angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="96e94-148">This can happen for <strong>JetSetLS</strong> when JET_bitLSCursor and JET_bitLSTable are both specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96e94-149">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="96e94-149">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="96e94-150">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="96e94-150">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="96e94-151">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="96e94-151">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96e94-152">JET_errLSAlreadySet</span><span class="sxs-lookup"><span data-stu-id="96e94-152">JET_errLSAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="96e94-153">Das angegebene Kontext Handle konnte dem angeforderten Objekt nicht zugeordnet werden, da ihm bereits ein Kontext Handle zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="96e94-153">The given context handle could not be associated with the requested object because it already had a context handle associated with it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96e94-154">JET_errLSCallbackNotSpecified</span><span class="sxs-lookup"><span data-stu-id="96e94-154">JET_errLSCallbackNotSpecified</span></span></p></td>
<td><p><span data-ttu-id="96e94-155">Das angegebene Kontext Handle konnte dem angeforderten Objekt nicht zugeordnet werden, weil der Lauf Zeit Rückruf nicht für die Instanz konfiguriert wurde, die der Sitzung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="96e94-155">The given context handle could not be associated with the requested object because the runtime callback has not been configured for the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96e94-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="96e94-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="96e94-157">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="96e94-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96e94-158">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="96e94-158">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="96e94-159">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96e94-159">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96e94-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="96e94-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="96e94-161">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="96e94-161">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="96e94-162">Bei Erfolg wurde das angegebene Kontext Handle erfolgreich dem angeforderten Objekt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="96e94-162">On success, the given context handle was successfully associated with the requested object.</span></span> <span data-ttu-id="96e94-163">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="96e94-163">No change to the database state will occur.</span></span>

<span data-ttu-id="96e94-164">Bei einem Fehler ist keine Änderung des Zustands des angeforderten Objekts aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="96e94-164">On failure, no change to the state of the requested object has occurred.</span></span> <span data-ttu-id="96e94-165">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="96e94-165">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="96e94-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96e94-166">Remarks</span></span>

<span data-ttu-id="96e94-167">Der lokale Speicher für einen Cursor oder eine Tabelle sollte als flüchtiger Cache angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="96e94-167">The Local Storage for a cursor or table should be viewed as a volatile cache.</span></span> <span data-ttu-id="96e94-168">Die Anwendung sollte zuerst versuchen, das Kontext Handle mithilfe von [jetgetls](./jetgetls-function.md)abzurufen.</span><span class="sxs-lookup"><span data-stu-id="96e94-168">The application should first try to retrieve the context handle using [JetGetLS](./jetgetls-function.md).</span></span> <span data-ttu-id="96e94-169">Wenn der Wert nicht festgelegt ist (d. h., er ist JET_LSNil), sollte die Anwendung einen neuen Kontext erstellen und mithilfe von **jetsetls** in den Cache laden.</span><span class="sxs-lookup"><span data-stu-id="96e94-169">If the value is not set (that is it is JET_LSNil) then the application should create a new context and load it into the cache using **JetSetLS**.</span></span> <span data-ttu-id="96e94-170">Die Anwendung kann den Cache mithilfe eines Aufrufens von [jetgetls](./jetgetls-function.md) mit JET_bitLSReset löschen.</span><span class="sxs-lookup"><span data-stu-id="96e94-170">The application can purge the cache using a call to [JetGetLS](./jetgetls-function.md) with JET_bitLSReset.</span></span> <span data-ttu-id="96e94-171">Wenn die Datenbank-Engine den Cache löscht, wird ein Lauf Zeit Rückruf generiert, um der Anwendung die Möglichkeit zu geben, diesen Kontext zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="96e94-171">If the database engine purges the cache then a runtime callback will be generated to give the application a chance to cleanup that context.</span></span> <span data-ttu-id="96e94-172">Der Rückruftyp wird für ein Kontext Handle JET_cbtypFreeCursorLS, das einem Cursor zugeordnet ist, und JET_cbtypFreeTableLS für ein Kontext Handle, das einer Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="96e94-172">The callback type will be JET_cbtypFreeCursorLS for a context handle associated with a cursor and JET_cbtypFreeTableLS for a context handle associated with a table.</span></span> <span data-ttu-id="96e94-173">In beiden Fällen wird das Kontext Handle als pvArg1.</span><span class="sxs-lookup"><span data-stu-id="96e94-173">In either case, the context handle will be passed as pvArg1.</span></span> <span data-ttu-id="96e94-174">Weitere Informationen finden Sie unter [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="96e94-174">See [JET_CALLBACK](./jet-callback-callback-function.md) for more information.</span></span>

<span data-ttu-id="96e94-175">Der Lauf Zeit Rückruf muss für die-Instanz, die der angegebenen Sitzung zugeordnet ist, ordnungsgemäß konfiguriert werden, bevor der lokale Speicher verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="96e94-175">The runtime callback must be properly configured for the instance associated with the given session before Local Storage can be used.</span></span> <span data-ttu-id="96e94-176">Dieser Rückruf kann mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md) mit [JET_paramRuntimeCallback](./callback-parameters.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="96e94-176">This callback can be set using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramRuntimeCallback](./callback-parameters.md).</span></span> <span data-ttu-id="96e94-177">Weitere Informationen finden Sie unter [jetsetsystemparameter](./jetsetsystemparameter-function.md) und [JET_paramRuntimeCallback](./callback-parameters.md) in System Parametern.</span><span class="sxs-lookup"><span data-stu-id="96e94-177">See [JetSetSystemParameter](./jetsetsystemparameter-function.md) and [JET_paramRuntimeCallback](./callback-parameters.md) in System Parameters for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="96e94-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96e94-178">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96e94-179"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="96e94-179"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="96e94-180">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="96e94-180">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96e94-181"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="96e94-181"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="96e94-182">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="96e94-182">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96e94-183"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="96e94-183"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="96e94-184">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="96e94-184">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96e94-185"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="96e94-185"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="96e94-186">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="96e94-186">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96e94-187"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="96e94-187"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="96e94-188">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="96e94-188">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="96e94-189">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="96e94-189">See Also</span></span>

[<span data-ttu-id="96e94-190">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="96e94-190">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="96e94-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="96e94-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="96e94-192">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="96e94-192">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="96e94-193">JET_LS</span><span class="sxs-lookup"><span data-stu-id="96e94-193">JET_LS</span></span>](./jet-ls.md)  
[<span data-ttu-id="96e94-194">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="96e94-194">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="96e94-195">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="96e94-195">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="96e94-196">Jetgetls</span><span class="sxs-lookup"><span data-stu-id="96e94-196">JetGetLS</span></span>](./jetgetls-function.md)  
[<span data-ttu-id="96e94-197">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="96e94-197">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="96e94-198">System Parameter</span><span class="sxs-lookup"><span data-stu-id="96e94-198">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
