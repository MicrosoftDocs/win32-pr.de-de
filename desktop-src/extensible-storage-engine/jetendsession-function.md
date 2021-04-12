---
description: 'Weitere Informationen zu: jetendsession-Funktion'
title: Jetendsession-Funktion
TOCTitle: JetEndSession Function
ms:assetid: a9a8f98a-258e-4fbb-bed0-657581984a07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294054(v=EXCHG.10)
ms:contentKeyID: 32765660
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndSession
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46bea6f5db745252a5e0ac6e8e03550dfead1b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346668"
---
# <a name="jetendsession-function"></a><span data-ttu-id="6e819-103">Jetendsession-Funktion</span><span class="sxs-lookup"><span data-stu-id="6e819-103">JetEndSession Function</span></span>


<span data-ttu-id="6e819-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6e819-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendsession-function"></a><span data-ttu-id="6e819-105">Jetendsession-Funktion</span><span class="sxs-lookup"><span data-stu-id="6e819-105">JetEndSession Function</span></span>

<span data-ttu-id="6e819-106">Die **jetendsession** -Funktion beendet die Sitzung und bereinigt alle Ressourcen, die der angegebenen Sitzung zugeordnet sind, und hebt die Zuordnung auf.</span><span class="sxs-lookup"><span data-stu-id="6e819-106">The **JetEndSession** function ends the session, and cleans up and deallocates any resources associated with the specified session.</span></span>

```cpp
    JET_ERR JET_API JetEndSession(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="6e819-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e819-107">Parameters</span></span>

<span data-ttu-id="6e819-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="6e819-108">*sesid*</span></span>

<span data-ttu-id="6e819-109">Die Sitzung, die beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e819-109">The session to end.</span></span> <span data-ttu-id="6e819-110">Zugehörige Ressourcen werden freigegeben, wenn die Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="6e819-110">Associated resources are released when the session ends.</span></span>

<span data-ttu-id="6e819-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="6e819-111">*grbit*</span></span>

<span data-ttu-id="6e819-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="6e819-112">Reserved.</span></span> <span data-ttu-id="6e819-113">Dieser Parameter kann das JET_bitForceSessionClosed-Flag enthalten, aber dieses Flag ist reserviert, und die Einstellung hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="6e819-113">This parameter can contain the JET_bitForceSessionClosed flag, but this flag is reserved and setting it has no effect.</span></span>

### <a name="return-value"></a><span data-ttu-id="6e819-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e819-114">Return Value</span></span>

<span data-ttu-id="6e819-115">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="6e819-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6e819-116">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6e819-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e819-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6e819-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="6e819-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e819-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e819-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6e819-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6e819-120">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6e819-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e819-121">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="6e819-121">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="6e819-122">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="6e819-122">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e819-123">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="6e819-123">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="6e819-124">Einer der Parameter, die bereitgestellt wurden, enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte hat ein unerwartetes Ergebnis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6e819-124">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e819-125">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="6e819-125">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="6e819-126">Die Sitzung war keine gültige Jet-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="6e819-126">The session was not a valid JET session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e819-127">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="6e819-127">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="6e819-128">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6e819-128">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e819-129">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="6e819-129">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="6e819-130">Der Vorgang konnte nicht ausgeführt werden, da kein Arbeitsspeicher zugeordnet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="6e819-130">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e819-131">JET_errSessionInUse</span><span class="sxs-lookup"><span data-stu-id="6e819-131">JET_errSessionInUse</span></span></p></td>
<td><p><span data-ttu-id="6e819-132">Dies bedeutet, dass die Sitzung in einem anderen Thread verwendet wurde oder die Sitzung nicht ordnungsgemäß festgelegt oder zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="6e819-132">This means the session was in use on another thread, or the session was not set or reset properly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e819-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="6e819-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="6e819-134">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="6e819-134">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="6e819-135">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6e819-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e819-136">JET_errOutOfBuffers</span><span class="sxs-lookup"><span data-stu-id="6e819-136">JET_errOutOfBuffers</span></span></p></td>
<td><p><span data-ttu-id="6e819-137">System Fehler, der angibt, dass keine Puffer mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6e819-137">System error that indicates that there are no more buffers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e819-138">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="6e819-138">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="6e819-139">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e819-139">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e819-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="6e819-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="6e819-141">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="6e819-141">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6e819-142">Bei Erfolg wird das Sitzungs Handle geschlossen und ist nicht verfügbar, und alle mit dieser Sitzung verbundenen Ressourcen werden bereinigt.</span><span class="sxs-lookup"><span data-stu-id="6e819-142">On success, the session handle is closed, and unavailable, and all resources related to this session are cleaned up.</span></span>

<span data-ttu-id="6e819-143">Bei einem Fehler gibt es mehrere zusätzliche Fehler, die als Teil der Sortierung "Close", "Cursor Close" und des Transaktions Rollbacks auftreten können.</span><span class="sxs-lookup"><span data-stu-id="6e819-143">On failure, there are several additional errors that could occur as part of sort table close, cursor close, and transaction rollback.</span></span> <span data-ttu-id="6e819-144">Diese Fehler sind recht unwahrscheinlich und sehr unwahrscheinlich, wenn Ihre Sitzungen nicht in Gebrauch sind, wenn **jetendsession** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6e819-144">These errors are fairly unlikely, and extremely unlikely if your sessions are completely not in use when **JetEndSession** is called.</span></span> <span data-ttu-id="6e819-145">Diese Fehler werden zurückgegeben, wenn ein Teil der Sitzung nicht ordnungsgemäß bereinigt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="6e819-145">These errors will be returned if some part of the session was unable to be cleaned up properly.</span></span>

#### <a name="remarks"></a><span data-ttu-id="6e819-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e819-146">Remarks</span></span>

<span data-ttu-id="6e819-147">Diese API führt ein Rollback für alle geöffneten Transaktionen aus (kein Commit auf Ebene 0).</span><span class="sxs-lookup"><span data-stu-id="6e819-147">This API will rollback any open transactions (not committed to level 0).</span></span> <span data-ttu-id="6e819-148">Außerdem werden alle dieser Sitzung zugeordneten Cursor und alle erstellten oder geöffneten Sortier Tabellen bereinigt.</span><span class="sxs-lookup"><span data-stu-id="6e819-148">Also all cursors associated with this session, and any sort tables that have been created or opened will be cleaned up.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6e819-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e819-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e819-150"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6e819-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6e819-151">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6e819-151">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e819-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6e819-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6e819-153">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6e819-153">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e819-154"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="6e819-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6e819-155">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="6e819-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e819-156"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="6e819-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6e819-157">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6e819-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e819-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6e819-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6e819-159">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6e819-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6e819-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6e819-160">See Also</span></span>

[<span data-ttu-id="6e819-161">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6e819-161">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6e819-162">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6e819-162">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6e819-163">Jetbeginsession</span><span class="sxs-lookup"><span data-stu-id="6e819-163">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="6e819-164">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="6e819-164">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="6e819-165">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="6e819-165">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="6e819-166">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="6e819-166">JetStopService</span></span>](./jetstopservice-function.md)
