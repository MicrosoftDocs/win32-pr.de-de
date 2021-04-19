---
description: 'Weitere Informationen finden Sie hier: JetBeginTransaction3-Funktion'
title: JetBeginTransaction3-Funktion
TOCTitle: JetBeginTransaction3 Function
ms:assetid: 7f8ed059-0b97-46fa-9925-e46cdcbee6ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835043(v=EXCHG.10)
ms:contentKeyID: 49894665
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetBeginTransaction3
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b263cb18c09df8205a49e1c4a1a683e339803f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346677"
---
# <a name="jetbegintransaction3-function"></a><span data-ttu-id="556d8-103">JetBeginTransaction3-Funktion</span><span class="sxs-lookup"><span data-stu-id="556d8-103">JetBeginTransaction3 Function</span></span>


<span data-ttu-id="556d8-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="556d8-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="556d8-105">Die **JetBeginTransaction3** -Funktion bewirkt, dass eine Sitzung eine Transaktion eingibt und einen neuen Sicherungspunkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="556d8-105">The **JetBeginTransaction3** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="556d8-106">Diese Funktion kann mehrmals in einer einzelnen Sitzung aufgerufen werden, um zusätzliche Speicherpunkte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="556d8-106">This function can be called more than once in a single session to create additional save points.</span></span> <span data-ttu-id="556d8-107">Diese Speicherpunkte können verwendet werden, um die Änderungen an der Datenbank selektiv beizubehalten oder zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="556d8-107">These save points can be used to selectively to keep or discard changes to the database.</span></span>

<span data-ttu-id="556d8-108">Die **JetBeginTransaction3** -Funktion wurde im Windows 8-Betriebssystem eingeführt.</span><span class="sxs-lookup"><span data-stu-id="556d8-108">The **JetBeginTransaction3** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetBeginTransaction3(
  __in          JET_SESID sesid,
  __in          int64 trxid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="556d8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="556d8-109">Parameters</span></span>

<span data-ttu-id="556d8-110">*-sid*</span><span class="sxs-lookup"><span data-stu-id="556d8-110">*sesid*</span></span>

<span data-ttu-id="556d8-111">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="556d8-111">The session to use for this call.</span></span>

<span data-ttu-id="556d8-112">*trxid*</span><span class="sxs-lookup"><span data-stu-id="556d8-112">*trxid*</span></span>

<span data-ttu-id="556d8-113">Ein optionaler Bezeichner, der vom Benutzer zur Identifizierung der Transaktion bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="556d8-113">An optional identifier supplied by the user to identify the transaction.</span></span>

<span data-ttu-id="556d8-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="556d8-114">*grbit*</span></span>

<span data-ttu-id="556d8-115">Eine Gruppe von Bits, die NULL oder mehr der in der folgenden Tabelle aufgeführten aufrufoptions Werte angibt.</span><span class="sxs-lookup"><span data-stu-id="556d8-115">A group of bits that that specifies zero or more of the call option values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="556d8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="556d8-116">Value</span></span></p></th>
<th><p><span data-ttu-id="556d8-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="556d8-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="556d8-118">JET_bitTransactionReadOnly</span><span class="sxs-lookup"><span data-stu-id="556d8-118">JET_bitTransactionReadOnly</span></span></p></td>
<td><p><span data-ttu-id="556d8-119">Die Datenbank wird von der Transaktion nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="556d8-119">The transaction will not modify the database.</span></span> <span data-ttu-id="556d8-120">Wenn ein Update versucht wird, schlägt dieser Vorgang mit JET_errTransReadOnly Antwort Codes fehl.</span><span class="sxs-lookup"><span data-stu-id="556d8-120">If an update is attempted, that operation will fail with JET_errTransReadOnly response code.</span></span> <span data-ttu-id="556d8-121">Diese Option wird ignoriert, es sei denn, Sie wird angefordert, wenn die angegebene Sitzung nicht bereits in einer Transaktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="556d8-121">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span> <span data-ttu-id="556d8-122">Diese Option ist ab Windows XP in Versionen des Windows-Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="556d8-122">This option is available in versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="556d8-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="556d8-123">Return value</span></span>

<span data-ttu-id="556d8-124">Diese Funktion gibt den [JET_ERR](./jet-err.md) -Datentyp mit einem der in der folgenden Tabelle aufgelisteten Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="556d8-124">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="556d8-125">Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Fehler Behandlungsparameter](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="556d8-125">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="556d8-126">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="556d8-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="556d8-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="556d8-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="556d8-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="556d8-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="556d8-129">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="556d8-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="556d8-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="556d8-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="556d8-131">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens der <a href="gg269240(v=exchg.10).md">jetstopservice</a> -Funktion beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="556d8-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="556d8-132">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="556d8-132">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="556d8-133">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="556d8-133">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="556d8-134">Dieser Rückgabecode wird von Windows-Versionen ab Windows XP zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="556d8-134">This return code is returned by versions of Windows starting with Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="556d8-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="556d8-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="556d8-136">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="556d8-136">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="556d8-137">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="556d8-137">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="556d8-138">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="556d8-138">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="556d8-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="556d8-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="556d8-140">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="556d8-140">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="556d8-141">Dieser Fehler wird von Windows-Versionen ab Windows XP zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="556d8-141">This error is returned by versions of Windows starting with Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="556d8-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="556d8-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="556d8-143">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="556d8-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="556d8-144">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="556d8-144">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="556d8-145">Eine neue Transaktion kann nicht gestartet werden, da die Sitzung bereits die maximale Speicherpunkt Tiefe hat, die von der Datenbank-Engine zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="556d8-145">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="556d8-146">Bei Erfolg wird die angegebene Sitzung innerhalb einer Transaktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="556d8-146">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="556d8-147">Wenn sich die Sitzung zuvor in einer Transaktion befunden hat, wird ein neuer Sicherungspunkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="556d8-147">If the session was previously inside a transaction, a new save point will be created.</span></span>

<span data-ttu-id="556d8-148">Bei einem Fehler bleibt der Transaktionsstatus der Sitzung unverändert.</span><span class="sxs-lookup"><span data-stu-id="556d8-148">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="556d8-149">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="556d8-149">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="556d8-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="556d8-150">Remarks</span></span>

<span data-ttu-id="556d8-151">Weitere Informationen zur Funktionsweise von Transaktionen finden Sie unter [jetbegintransaction](./jetbegintransaction-function.md).</span><span class="sxs-lookup"><span data-stu-id="556d8-151">For more information about how transactions work, see [JetBeginTransaction](./jetbegintransaction-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="556d8-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="556d8-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="556d8-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="556d8-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="556d8-154">Erfordert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="556d8-154">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="556d8-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="556d8-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="556d8-156">Erfordert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="556d8-156">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="556d8-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="556d8-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="556d8-158">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="556d8-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="556d8-159"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="556d8-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="556d8-160">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="556d8-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="556d8-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="556d8-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="556d8-162">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="556d8-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="556d8-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="556d8-163">See also</span></span>

[<span data-ttu-id="556d8-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="556d8-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="556d8-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="556d8-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="556d8-166">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="556d8-166">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="556d8-167">Jetbegintransaction</span><span class="sxs-lookup"><span data-stu-id="556d8-167">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="556d8-168">Jetcommittransaction</span><span class="sxs-lookup"><span data-stu-id="556d8-168">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="556d8-169">Jetgetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="556d8-169">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="556d8-170">Jetresessioncontext</span><span class="sxs-lookup"><span data-stu-id="556d8-170">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="556d8-171">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="556d8-171">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="556d8-172">Jetabessioncontext</span><span class="sxs-lookup"><span data-stu-id="556d8-172">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="556d8-173">System Parameter</span><span class="sxs-lookup"><span data-stu-id="556d8-173">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
