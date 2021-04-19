---
description: 'Weitere Informationen finden Sie hier: JetBeginTransaction2-Funktion'
title: JetBeginTransaction2-Funktion
TOCTitle: JetBeginTransaction2 Function
ms:assetid: 638af3f1-b342-46bd-9fd0-dc281936355c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269268(v=EXCHG.10)
ms:contentKeyID: 32765570
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d21bb88301a1f5d30df673a56032ef91c3847599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366100"
---
# <a name="jetbegintransaction2-function"></a><span data-ttu-id="ab7fa-103">JetBeginTransaction2-Funktion</span><span class="sxs-lookup"><span data-stu-id="ab7fa-103">JetBeginTransaction2 Function</span></span>


<span data-ttu-id="ab7fa-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ab7fa-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbegintransaction2-function"></a><span data-ttu-id="ab7fa-105">JetBeginTransaction2-Funktion</span><span class="sxs-lookup"><span data-stu-id="ab7fa-105">JetBeginTransaction2 Function</span></span>

<span data-ttu-id="ab7fa-106">Die **JetBeginTransaction2** -Funktion bewirkt, dass eine Sitzung eine Transaktion eingibt und einen neuen Sicherungspunkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-106">The **JetBeginTransaction2** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="ab7fa-107">Diese Funktion kann mehrmals in einer einzelnen Sitzung aufgerufen werden, um zusätzliche Speicherpunkte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-107">This function can be called more than once in a single session to create additional save points.</span></span> <span data-ttu-id="ab7fa-108">Diese Speicherpunkte können verwendet werden, um die Änderungen an der Datenbank selektiv beizubehalten oder zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-108">These save points can be used to selectively to keep or discard changes to the database.</span></span>

```cpp
    JET_ERR JET_API JetBeginTransaction2(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="ab7fa-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab7fa-109">Parameters</span></span>

<span data-ttu-id="ab7fa-110">*-sid*</span><span class="sxs-lookup"><span data-stu-id="ab7fa-110">*sesid*</span></span>

<span data-ttu-id="ab7fa-111">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-111">The session to use for this call.</span></span>

<span data-ttu-id="ab7fa-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="ab7fa-112">*grbit*</span></span>

<span data-ttu-id="ab7fa-113">Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-113">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab7fa-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ab7fa-114">Value</span></span></p></th>
<th><p><span data-ttu-id="ab7fa-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ab7fa-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab7fa-116">JET_bitTransactionReadOnly</span><span class="sxs-lookup"><span data-stu-id="ab7fa-116">JET_bitTransactionReadOnly</span></span></p></td>
<td><p><span data-ttu-id="ab7fa-117">Die Datenbank wird von der Transaktion nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-117">The transaction will not modify the database.</span></span> <span data-ttu-id="ab7fa-118">Wenn versucht wird, ein Update auszuführen, schlägt dieser Vorgang mit JET_errTransReadOnly fehl.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-118">If an update is attempted, that operation will fail with JET_errTransReadOnly.</span></span> <span data-ttu-id="ab7fa-119">Diese Option wird ignoriert, es sei denn, Sie wird angefordert, wenn die angegebene Sitzung nicht bereits in einer Transaktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-119">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span> <span data-ttu-id="ab7fa-120">Diese Option ist nur ab Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-120">This option is only available as of Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="ab7fa-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab7fa-121">Return Value</span></span>

<span data-ttu-id="ab7fa-122">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ab7fa-123">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ab7fa-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab7fa-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ab7fa-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="ab7fa-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab7fa-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab7fa-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ab7fa-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ab7fa-127">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab7fa-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="ab7fa-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="ab7fa-129">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab7fa-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ab7fa-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ab7fa-131">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="ab7fa-132">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab7fa-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ab7fa-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ab7fa-134">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-134">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab7fa-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ab7fa-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ab7fa-136">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-136">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab7fa-137">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="ab7fa-137">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="ab7fa-138">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-138">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="ab7fa-139">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-139">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab7fa-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ab7fa-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ab7fa-141">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-141">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab7fa-142">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="ab7fa-142">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="ab7fa-143">Eine neue Transaktion kann nicht gestartet werden, da die Sitzung bereits die maximale Speicherpunkt Tiefe hat, die von der Datenbank-Engine zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-143">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ab7fa-144">Bei Erfolg wird die angegebene Sitzung innerhalb einer Transaktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-144">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="ab7fa-145">Wenn sich die Sitzung zuvor in einer Transaktion befand, wird ein neuer Sicherungspunkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-145">If the session was previously inside of a transaction then a new save point will be created.</span></span>

<span data-ttu-id="ab7fa-146">Bei einem Fehler bleibt der Transaktionsstatus der Sitzung unverändert.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-146">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="ab7fa-147">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-147">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ab7fa-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab7fa-148">Remarks</span></span>

<span data-ttu-id="ab7fa-149">Weitere Informationen zur Funktionsweise von Transaktionen finden Sie unter [jetbegintransaction](./jetbegintransaction-function.md).</span><span class="sxs-lookup"><span data-stu-id="ab7fa-149">For more information about how transactions work, see [JetBeginTransaction](./jetbegintransaction-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="ab7fa-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab7fa-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab7fa-151"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ab7fa-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ab7fa-152">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-152">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab7fa-153"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ab7fa-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ab7fa-154">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-154">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab7fa-155"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ab7fa-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ab7fa-156">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab7fa-157"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="ab7fa-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ab7fa-158">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab7fa-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ab7fa-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ab7fa-160">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ab7fa-161">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ab7fa-161">See Also</span></span>

[<span data-ttu-id="ab7fa-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ab7fa-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ab7fa-163">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ab7fa-163">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ab7fa-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ab7fa-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ab7fa-165">Jetbegintransaction</span><span class="sxs-lookup"><span data-stu-id="ab7fa-165">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="ab7fa-166">Jetcommittransaction</span><span class="sxs-lookup"><span data-stu-id="ab7fa-166">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="ab7fa-167">Jetgetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="ab7fa-167">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="ab7fa-168">Jetresessioncontext</span><span class="sxs-lookup"><span data-stu-id="ab7fa-168">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="ab7fa-169">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="ab7fa-169">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="ab7fa-170">Jetabessioncontext</span><span class="sxs-lookup"><span data-stu-id="ab7fa-170">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="ab7fa-171">System Parameter</span><span class="sxs-lookup"><span data-stu-id="ab7fa-171">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
