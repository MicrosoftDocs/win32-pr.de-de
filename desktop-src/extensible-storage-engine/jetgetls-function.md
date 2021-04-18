---
description: 'Weitere Informationen: jetgetls-Funktion'
title: Jetgetls-Funktion
TOCTitle: JetGetLS Function
ms:assetid: 411baf34-d167-4633-81af-be4886f4a646
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269234(v=EXCHG.10)
ms:contentKeyID: 32765536
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLS
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7a89cf4e20798a2c412ba6eb39b08f99a60a464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351532"
---
# <a name="jetgetls-function"></a><span data-ttu-id="49833-103">Jetgetls-Funktion</span><span class="sxs-lookup"><span data-stu-id="49833-103">JetGetLS Function</span></span>


<span data-ttu-id="49833-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="49833-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetls-function"></a><span data-ttu-id="49833-105">Jetgetls-Funktion</span><span class="sxs-lookup"><span data-stu-id="49833-105">JetGetLS Function</span></span>

<span data-ttu-id="49833-106">Die **jetgetls** -Funktion ermöglicht der Anwendung das Abrufen des Kontext Handles, das als lokaler Speicher bezeichnet wird, der einem Cursor oder der diesem Cursor zugeordneten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="49833-106">The **JetGetLS** function enables the application to retrieve the context handle known as Local Storage that is associated with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="49833-107">Dieses Kontext Handle muss zuvor mithilfe von [jetsetls](./jetsetls-function.md)festgelegt worden sein.</span><span class="sxs-lookup"><span data-stu-id="49833-107">This context handle must have been previously set using [JetSetLS](./jetsetls-function.md).</span></span> <span data-ttu-id="49833-108">**Jetgetls** kann auch zum gleichzeitigen Abrufen des aktuellen Kontext Handles für einen Cursor oder eine Tabelle und zum Zurücksetzen dieses Kontext Handles verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49833-108">**JetGetLS** can also be used to simultaneously fetch the current context handle for a cursor or table and reset that context handle.</span></span>

<span data-ttu-id="49833-109">**Windows XP: jetgetls** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="49833-109">**Windows XP:  JetGetLS** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_LS* pls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="49833-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="49833-110">Parameters</span></span>

<span data-ttu-id="49833-111">*-sid*</span><span class="sxs-lookup"><span data-stu-id="49833-111">*sesid*</span></span>

<span data-ttu-id="49833-112">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="49833-112">The session to use for this call.</span></span>

<span data-ttu-id="49833-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="49833-113">*tableid*</span></span>

<span data-ttu-id="49833-114">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="49833-114">The cursor to use for this call.</span></span>

<span data-ttu-id="49833-115">*pls*</span><span class="sxs-lookup"><span data-stu-id="49833-115">*pls*</span></span>

<span data-ttu-id="49833-116">Der Ausgabepuffer, der das Kontext Handle empfängt, das momentan dem Cursor oder der Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="49833-116">The output buffer that receives the context handle currently associated with the cursor or table.</span></span>

<span data-ttu-id="49833-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="49833-117">*grbit*</span></span>

<span data-ttu-id="49833-118">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="49833-118">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49833-119">Wert</span><span class="sxs-lookup"><span data-stu-id="49833-119">Value</span></span></p></th>
<th><p><span data-ttu-id="49833-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="49833-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49833-121">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="49833-121">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="49833-122">Gibt an, dass das dem angegebenen Cursor zugeordnete Kontext Handle abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="49833-122">Indicates that the context handle associated with the given cursor should be retrieved.</span></span></p>
<p><span data-ttu-id="49833-123">Wenn weder JET_bitLSCursor noch JET_bitLSTable angegeben wird, wird JET_bitLSCursor angenommen.</span><span class="sxs-lookup"><span data-stu-id="49833-123">If neither JET_bitLSCursor nor JET_bitLSTable is specified then JET_bitLSCursor is presumed.</span></span></p>
<p><span data-ttu-id="49833-124">Diese Option kann nicht mit JET_bitLSTable verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49833-124">This option cannot be used with JET_bitLSTable.</span></span> <span data-ttu-id="49833-125">Der Vorgang schlägt mit JET_errInvalidgrbit fehl, wenn ein Versuch unternommen wird.</span><span class="sxs-lookup"><span data-stu-id="49833-125">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49833-126">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="49833-126">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="49833-127">Gibt an, dass das Kontext Handle, das der Tabelle zugeordnet ist, die den angegebenen Cursor enthält, abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="49833-127">Indicates that the context handle associated to the table that contains the given cursor should be retrieved.</span></span> <span data-ttu-id="49833-128">Diese Option kann nicht mit JET_bitLSCursor verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49833-128">It is illegal to use this option with JET_bitLSCursor.</span></span> <span data-ttu-id="49833-129">Der Vorgang schlägt mit JET_errInvalidgrbit fehl, wenn ein Versuch unternommen wird.</span><span class="sxs-lookup"><span data-stu-id="49833-129">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49833-130">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="49833-130">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="49833-131">Gibt an, dass das Kontext Handle für das ausgewählte Objekt auf JET_LSNil zurückgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="49833-131">Indicates that the context handle for the chosen object should be reset to JET_LSNil.</span></span> <span data-ttu-id="49833-132">Der aktuelle Wert des Kontext Handles wird im Ausgabepuffer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="49833-132">The current value of the context handle is returned in the output buffer.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="49833-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49833-133">Return Value</span></span>

<span data-ttu-id="49833-134">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="49833-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="49833-135">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="49833-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49833-136">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="49833-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="49833-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49833-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49833-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="49833-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="49833-139">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="49833-139">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49833-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="49833-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="49833-141">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="49833-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49833-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="49833-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="49833-143">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="49833-143">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="49833-144">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="49833-144">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49833-145">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="49833-145">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="49833-146">Eine der angeforderten Optionen war ungültig, wird in unzulässiger Weise verwendet oder nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="49833-146">One of the options requested was invalid, used in an illegal manner, or not implemented.</span></span></p>
<p><span data-ttu-id="49833-147">Dies kann bei <strong>jetgetls</strong> vorkommen, wenn sowohl JET_bitLSCursor als auch JET_bitLSTable festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="49833-147">This can happen for <strong>JetGetLS</strong> when both JET_bitLSCursor and JET_bitLSTable are set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49833-148">JET_errLSNotSet</span><span class="sxs-lookup"><span data-stu-id="49833-148">JET_errLSNotSet</span></span></p></td>
<td><p><span data-ttu-id="49833-149">Das Kontext Handle konnte nicht zurückgegeben werden, da dem angeforderten Objekt derzeit kein Kontext Handle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="49833-149">The context handle could not be returned because no context handle is currently associated with the requested object.</span></span></p>
<p><span data-ttu-id="49833-150"><strong>Hinweis  </strong> Dieser Fehler wird nicht zurückgegeben, wenn JET_bitLSReset angegeben wurde, dem angeforderten Objekt aber kein Kontext Handle zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="49833-150"><strong>Note  </strong> This error is not returned if JET_bitLSReset is specified yet no context handle was associated with the requested object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49833-151">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="49833-151">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="49833-152">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="49833-152">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49833-153">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="49833-153">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="49833-154">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49833-154">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49833-155">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="49833-155">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="49833-156">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="49833-156">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="49833-157">Bei Erfolg wurde das Kontext Handle erfolgreich aus dem angeforderten Objekt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="49833-157">On success, the context handle was successfully retrieved from the requested object.</span></span> <span data-ttu-id="49833-158">Wenn JET_bitLSReset angegeben wurde, wurde dieses Kontext Handle ebenfalls erfolgreich aus dem Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="49833-158">If JET_bitLSReset was specified then that context handle was also successfully removed from the object.</span></span> <span data-ttu-id="49833-159">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="49833-159">No change to the database state will occur.</span></span>

<span data-ttu-id="49833-160">Bei einem Fehler ist keine Änderung des Zustands des angeforderten Objekts aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="49833-160">On failure, no change to the state of the requested object has occurred.</span></span> <span data-ttu-id="49833-161">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="49833-161">No change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="49833-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49833-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49833-163"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="49833-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="49833-164">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="49833-164">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49833-165"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="49833-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="49833-166">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="49833-166">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49833-167"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="49833-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="49833-168">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="49833-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49833-169"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="49833-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="49833-170">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="49833-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49833-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="49833-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="49833-172">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="49833-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="49833-173">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="49833-173">See Also</span></span>

[<span data-ttu-id="49833-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="49833-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="49833-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="49833-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="49833-176">JET_LS</span><span class="sxs-lookup"><span data-stu-id="49833-176">JET_LS</span></span>](./jet-ls.md)  
[<span data-ttu-id="49833-177">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="49833-177">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="49833-178">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="49833-178">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="49833-179">Jetsetls</span><span class="sxs-lookup"><span data-stu-id="49833-179">JetSetLS</span></span>](./jetsetls-function.md)
